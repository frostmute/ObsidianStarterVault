# PowerShell - Get-GitHubRelease

*Source: [Get-GitHubRelease.ps1](https://gist.github.com/jimbrig/03aa65c9b20dc3ad86bbb442f723672a)*

See Also: [Bash - Download Private GitHub Repo Release Assets](../Bash/Bash%20-%20Download%20Private%20GitHub%20Repo%20Release%20Assets.md)

````powershell
#!/usr/bin/env pwsh

Function Get-GitHubRelease {
    <#
        .SYNOPSIS
            Get the latest release of a GitHub repository
        .DESCRIPTION
            Get the latest release of a GitHub repository
        .PARAMETER User
            The GitHub user or organization
        .PARAMETER Repository
            The GitHub repository (can be private)
        .PARAMETER Token
            The GitHub API token (PAT)
            If not supplied will look for an Environment Variable `$env:GITHUB_API_TOKEN`.
        .PARAMETER Tag
            The tag to get the release for (i.e. `v1.0.0`)
        .PARAMETER File
            The asset to get the download URL for
        .PARAMETER OutputPath
            The path to save the asset to
            [NOTE]: Use the directory output, not the path + file + extension.
        .EXAMPLE
            Get-GitHubRelease -User 'jimbrig' -Repository 'property_allocation_demo' -Tag 'v1.0.0' -Asset 'property_allocation_demo-master.zip' -OutputPath "$HOME\Downloads"
    #>
    
    [CmdletBinding()]
    
    Param (
        [Parameter(Mandatory=$true)]
        [string]$User,
        [Parameter(Mandatory=$true)]
        [string]$Repository,
        [Parameter(Mandatory=$false)]
        [string]$Token = $env:GITHUB_API_TOKEN,
        [Parameter(Mandatory=$true)]
        [string]$Tag,
        [Parameter(Mandatory=$true)]
        [string]$File,
        [Parameter(Mandatory=$true)]
        [string]$OutputPath
    )

    $url = "https://api.github.com/repos/$User/$Repository/releases/tags/$Tag"

    $headers = @{
        'Authorization' = "token $Token"
        'Accept' = 'application/vnd.github.v3+json'
    }

    $response = Invoke-RestMethod -Uri $url -Headers $headers -Method Get

    $asset = $response.assets | Where-Object { $_.name -eq $File }

    $asset_url = $asset.browser_download_url

    $asset_path = Join-Path $OutputPath $File

    # Private
    $private_headers = @{
        'Authorization' = "token $Token"
        'Accept' = 'application/octet-stream'
    } 

    $private_uri = "https://$($Token):@api.github.com/repos/$User/$Repository/releases/assets/$($asset.id)"

    Invoke-WebRequest -SkipCertificateCheck -Uri $private_uri -Headers $private_headers -OutFile $asset_path -Resume -PassThru

}
````

---

## Appendix: Links

* *Code*
* [Development](../../MOCs/Development.md)
* [Microsoft](../../MOCs/Microsoft.md)
* [Windows Command Line](../../../3-Resources/Tools/Developer%20Tools/Shell/Microsoft%20DOS.md)
* [PowerShell (MOC)](../../MOCs/PowerShell.md)
* *PowerShell (Tools)*
* [PowerShell (Code)](_README.md)

*Backlinks:*

````dataview
list from [[PowerShell - Get-GitHubRelease]] AND -"Changelog"
````
