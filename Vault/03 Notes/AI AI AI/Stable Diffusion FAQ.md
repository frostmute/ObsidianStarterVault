
1. [Stable Diffusion FAQ](https://rentry.org/SD_help_FAQ#stable-diffusion-faq)
    1. [General Topics](https://rentry.org/SD_help_FAQ#general-topics)
        1. [Abbreviations and names](https://rentry.org/SD_help_FAQ#abbreviations-and-names)
        2. [Video guides](https://rentry.org/SD_help_FAQ#video-guides)
        3. [About SD](https://rentry.org/SD_help_FAQ#about-sd)
        4. [Installation and first runs](https://rentry.org/SD_help_FAQ#installation-and-first-runs)
            1. [Running locally on your computer](https://rentry.org/SD_help_FAQ#running-locally-on-your-computer)
                1. [System requirements](https://rentry.org/SD_help_FAQ#system-requirements)
                    1. [Minimum](https://rentry.org/SD_help_FAQ#minimum)
                    2. [Recommended](https://rentry.org/SD_help_FAQ#recommended)
                    3. [Professional/DreamBooth-capable](https://rentry.org/SD_help_FAQ#professionaldreambooth-capable)
            2. [Run remotely](https://rentry.org/SD_help_FAQ#run-remotely)
            3. [Using other models](https://rentry.org/SD_help_FAQ#using-other-models)
                1. [Where to find trained models](https://rentry.org/SD_help_FAQ#where-to-find-trained-models)
                2. [I want to generate images of myself/my pet/a specific style. How can I do this?](https://rentry.org/SD_help_FAQ#i-want-to-generate-images-of-myselfmy-peta-specific-style-how-can-i-do-this)
        5. [Uninstalling the webui](https://rentry.org/SD_help_FAQ#uninstalling-the-webui)
        6. [Using Git (Updates and revert back to previous versions)](https://rentry.org/SD_help_FAQ#using-git-updates-and-revert-back-to-previous-versions)
            1. [Updating through "git pull"](https://rentry.org/SD_help_FAQ#updating-through-git-pull)
            2. [Reverting to a previous version](https://rentry.org/SD_help_FAQ#reverting-to-a-previous-version)
            3. [Common issues when using Git](https://rentry.org/SD_help_FAQ#common-issues-when-using-git)
                1. ["fatal: not a git repository"](https://rentry.org/SD_help_FAQ#fatal-not-a-git-repository)
                    1. [New installation](https://rentry.org/SD_help_FAQ#new-installation)
                    2. [Make it a Git repository in place](https://rentry.org/SD_help_FAQ#make-it-a-git-repository-in-place)
                2. ["fatal: git detected dubious ownership in repository"](https://rentry.org/SD_help_FAQ#fatal-git-detected-dubious-ownership-in-repository)
                3. ["error: Your local changes to the following files would be overwritten by merge"](https://rentry.org/SD_help_FAQ#error-your-local-changes-to-the-following-files-would-be-overwritten-by-merge)
                4. [Changing from Gitgud to Github](https://rentry.org/SD_help_FAQ#changing-from-gitgud-to-github)
        7. [Common problems and questions (with a focus on AUTOMATIC1111's stable-diffusion-webui)](https://rentry.org/SD_help_FAQ#common-problems-and-questions-with-a-focus-on-automatic1111s-stable-diffusion-webui)
            1. [Installation stuck at "pip install torch"](https://rentry.org/SD_help_FAQ#installation-stuck-at-pip-install-torch)
            2. [Error: Torch is not able to use GPU!](https://rentry.org/SD_help_FAQ#error-torch-is-not-able-to-use-gpu)
            3. [No model found! Where to get one?](https://rentry.org/SD_help_FAQ#no-model-found-where-to-get-one)
                1. [Version 1.5](https://rentry.org/SD_help_FAQ#version-15)
                2. [Version 2](https://rentry.org/SD_help_FAQ#version-2)
            4. [What is a “flag”?](https://rentry.org/SD_help_FAQ#what-is-a-flag)
            5. [What is batch size and count?](https://rentry.org/SD_help_FAQ#what-is-batch-size-and-count)
            6. [I’ve seen additional settings in one of the videos that don’t show up for me.](https://rentry.org/SD_help_FAQ#ive-seen-additional-settings-in-one-of-the-videos-that-dont-show-up-for-me)
            7. [How to install a VAE file?](https://rentry.org/SD_help_FAQ#how-to-install-a-vae-file)
            8. [What is a VAE?](https://rentry.org/SD_help_FAQ#what-is-a-vae)
            9. [Image generation is slow! How to speed it up?](https://rentry.org/SD_help_FAQ#image-generation-is-slow-how-to-speed-it-up)
            10. [Error: Cuda out of memory. What to do?](https://rentry.org/SD_help_FAQ#error-cuda-out-of-memory-what-to-do)
                1. [When generating images](https://rentry.org/SD_help_FAQ#when-generating-images)
                2. [When training](https://rentry.org/SD_help_FAQ#when-training)
            11. [It generates Black or Green images!](https://rentry.org/SD_help_FAQ#it-generates-black-or-green-images)
            12. [Error: No module named pip](https://rentry.org/SD_help_FAQ#error-no-module-named-pip)
            13. [CUDA error: no kernel image is available for execution on the device after enabling xformers](https://rentry.org/SD_help_FAQ#cuda-error-no-kernel-image-is-available-for-execution-on-the-device-after-enabling-xformers)
            14. [RuntimeError: Sizes of tensors must match except in dimension 0. Expected size 1024 but got size 768 for tensor number 1 in the list.](https://rentry.org/SD_help_FAQ#runtimeerror-sizes-of-tensors-must-match-except-in-dimension-0-expected-size-1024-but-got-size-768-for-tensor-number-1-in-the-list)
            15. [ValueError: Query/Key/Value should all have the same dtype](https://rentry.org/SD_help_FAQ#valueerror-querykeyvalue-should-all-have-the-same-dtype)
            16. [Why GPU usage in task manager is low?](https://rentry.org/SD_help_FAQ#why-gpu-usage-in-task-manager-is-low)
    2. [Credits](https://rentry.org/SD_help_FAQ#credits)

## General Topics

### Abbreviations and names

- "SD" stands for "Stable Diffusion"
- "Super Stable Diffusion 2.0" refers to the AUTOMATIC1111 SD repository
- "Checkpoint" and "model" are synonyms and can be used interchangeably

### Video guides

You can find many tutorials and videos about Stable Diffusion on [Aitrepreneur's Youtube Channel](https://www.youtube.com/c/Aitrepreneur)  
Please keep in mind that the project is constantly evolving, so some videos may be outdated or may not reflect current program interfaces.

### About SD

**Q: What is SD?**  
_A: It is an open-source project by **[Stability.AI](http://stability.ai/)**_

**Q: Who is AUTOMATIC1111?**  
_A: AUTOMATIC1111 is the creator of the most feature-rich WebUI to date!_

### Installation and first runs

#### Running locally on your computer

There are several options for running SD locally on your computer.

- The most popular program is probably [AUTOMATIC1111's stable-diffusion-webui](https://github.com/AUTOMATIC1111/stable-diffusion-webui) ([wiki](https://github.com/AUTOMATIC1111/stable-diffusion-webui/wiki/Install-and-Run-on-NVidia-GPUs))
    - You can also follow this video tutorial by @aitrepreneur: [https://youtu.be/VXEyhM3Djqg](https://youtu.be/VXEyhM3Djqg)
- Another web interface: [InvokeAI](https://github.com/invoke-ai/InvokeAI)
- Stand alone application: [NMDK](https://nmkd.itch.io/t2i-gui)

Please refer to the installation instructions for each option. For the web interfaces, you will need Python 3.7 or later (up to 3.10). It is recommended to install version 3.10.  
**Python 3.11 is not compatible with some dependencies.**

##### System requirements

The system requirements may vary depending on the software you choose to use. The following recommendations are based on [NMDK's docs](https://github.com/n00mkrad/text2image-gui/blob/main/README.md#system-requirements)

###### Minimum

- **GPU:** Nvidia GPU with 4 GB VRAM, Maxwell Architecture (2014) or newer
    - Apple M1 or newer
    - AMD cards are not officially supported, but may work on Linux with [these instructions](https://github.com/AUTOMATIC1111/stable-diffusion-webui/wiki/Install-and-Run-on-AMD-GPUs)
- **RAM:** 8 GB RAM (note: it is recommended to enable the pagefile as swapping will occur with only 8 GB of RAM)
- **Disk:** 12 GB (it is recommended to have an additional 5 GB of free space for temporary files)

###### Recommended

- **GPU:** Nvidia GPU with 8 GB VRAM, Pascal Architecture (2016) or newer
- **RAM:** 16 GB RAM
- **Disk:** 12 GB on SSD (it is recommended to have an additional 5 GB of free space for temporary files)

###### Professional/DreamBooth-capable

- **GPU:** Nvidia GPU with at least 12 GB VRAM, Turing Architecture (2018) or newer when using some optimized settings. **24 GB recommended!**
- **RAM:** 32 GB RAM
- **Disk:** 12 GB on NVME SSD (it is recommended to have an additional 25 GB of free space for temporary files)

#### Run remotely

If your computer does not meet the recommended system requirements, you can run SD remotely using a website that offers free access, such as [https://playgroundai.com](https://playgroundai.com/) or [https://beta.dreamstudio.ai](https://beta.dreamstudio.ai/) (which provides 200 free credits). Alternatively, you can use a Google Colab notebook, as described in [these instructions](https://github.com/AUTOMATIC1111/stable-diffusion-webui/wiki/Online-Services). The best is maintained by TheLastBen.

#### Using other models

##### Where to find trained models

Yes, there are a number of trained models available for download. You can find a list of these models at [https://rentry.org/sdmodels](https://rentry.org/sdmodels). However, it's important to be aware that some of these models may contain viruses, so it's a good idea to be cautious when downloading models from unfamiliar sources. You can learn more about the potential risks of downloading untrusted models in this video: [https://youtu.be/Qto8R9j6VaI](https://youtu.be/Qto8R9j6VaI).

##### I want to generate images of myself/my pet/a specific style. How can I do this?

To generate images of specific people or subjects, you will need to train a model using Dreambooth. The process of training a model using Dreambooth is explained in detail in this tutorial playlist: [https://www.youtube.com/playlist?list=PLkIRB85csS_vK9iGRXNHG618HTQKhDrZX](https://www.youtube.com/playlist?list=PLkIRB85csS_vK9iGRXNHG618HTQKhDrZX).  
Alternatively, you can use textual inversion but the results may be not as good as those obtained using Dreambooth.

### Uninstalling the webui

1. Delete the `stable-diffusion-webui` directory
2. Navigate to `%userprofile%\.cache` and delete any folders related to the webui or Huggingface. Don't worry if you delete too much, all needed files will be downloaded again in case they are needed.
3. (Optional) Uninstall Python, if you don't need it anymore, and delete the directory where it was installed
4. (Optional) Uninstall Git, if you don't need it anymore.
5. (Optional) Clean your PATH variable in case the uninstallers didn't do it automatically:
    - Open `SystemPropertiesAdvanced.exe`
    - Click on "Environmental Variables"
    - Look for `Path` in both user and system variables and remove entries that are no longer needed. Be sure to leave any entries you don't recognize, as other programs may stop working properly without them.

### Using Git (Updates and revert back to previous versions)

All projects on Github and similar sites are managed through a program called Git: It helps developers keep track of changes made to their code. It allows multiple people to work on the same codebase simultaneously, and it also helps developers keep a history of their work, so they can easily revert to earlier versions of their code if necessary. Git is widely used in the software development industry, and it is often used in conjunction with a hosting service like GitHub, which allows developers to share their code with others and collaborate on projects.

Thanks to this software it's easy to update or go back to a previous code base in case something breaks. The following sections explain how to use it. For more information on Git and all the advanced features, you might want to look up a tutorial.

You can get the software at [https://git-scm.com/download/win](https://git-scm.com/download/win)

#### Updating through "git pull"

You can update the webui automatically every time you launch it by adding `git pull` to the `webui-user.bat` file. To do this, follow these steps:

1. Open `webui-user.bat` with a text editor.
2. Add `git pull` before the `call webui.bat` line. The file should look like this:  
    
    |   |   |
    |---|---|
    |[1](https://rentry.org/SD_help_FAQ#L-1-1)<br> [2](https://rentry.org/SD_help_FAQ#L-1-2)<br> [3](https://rentry.org/SD_help_FAQ#L-1-3)<br> [4](https://rentry.org/SD_help_FAQ#L-1-4)<br> [5](https://rentry.org/SD_help_FAQ#L-1-5)<br> [6](https://rentry.org/SD_help_FAQ#L-1-6)<br> [7](https://rentry.org/SD_help_FAQ#L-1-7)<br> [8](https://rentry.org/SD_help_FAQ#L-1-8)<br> [9](https://rentry.org/SD_help_FAQ#L-1-9)<br>[10](https://rentry.org/SD_help_FAQ#L-1-10)|@echo off<br>set PYTHON=<br>set GIT=<br>set VENV_DIR=<br>set COMMANDLINE_ARGS=<br>git pull<br>call webui.bat|
    

Alternatively, you can update the webui manually by following these steps:

1. Open the Command Prompt (CMD) and navigate to the directory where you have installed "stable-diffusion-webui". You can do this by running `cd /d c:\AI\stable-diffusion-webui\`.
2. Run the command `git pull`.

#### Reverting to a previous version

You can view the history of the project on [GitHub](https://github.com/AUTOMATIC1111/stable-diffusion-webui/commits/master). To do so, open the project's GitHub page and click on the number of commits. This will show you a list of all the changes made to the codebase. Each change is identified by a commit ID, which is a long string of letters and numbers.  
![](https://i.imgur.com/baTogEw.png)

You can click on any of the buttons in column 1 to copy the commit ID. Column 2 shows the shorthand ID of the commit and, if you click on it, opens detailed information about the changes. This is only helpful if you want to look what changed in the source code.  
![](https://i.imgur.com/3HUbQ1t.png)

For example, the commit [3246a2d6b898da6a98fe9df4dc67944635a41bd3](https://github.com/AUTOMATIC1111/stable-diffusion-webui/commit/3246a2d6b898da6a98fe9df4dc67944635a41bd3) has the shorthand of `3246a2d`. You can use either the full ID or the short hand to revert to a specific version.

To revert to a previous version:

1. Open the Command Prompt (CMD) and navigate to the directory where you have installed "stable-diffusion-webui". You can do this by running `cd /d "c:\AI\stable-diffusion-webui\"`.
2. Run the command `git checkout 3246a2d`, where `3246a2d` is the commit ID you want to go to.

The expected output should look like this, which is shown only once after running the command:  

|   |   |
|---|---|
|[1](https://rentry.org/SD_help_FAQ#L-2-1)<br> [2](https://rentry.org/SD_help_FAQ#L-2-2)<br> [3](https://rentry.org/SD_help_FAQ#L-2-3)<br> [4](https://rentry.org/SD_help_FAQ#L-2-4)<br> [5](https://rentry.org/SD_help_FAQ#L-2-5)<br> [6](https://rentry.org/SD_help_FAQ#L-2-6)<br> [7](https://rentry.org/SD_help_FAQ#L-2-7)<br> [8](https://rentry.org/SD_help_FAQ#L-2-8)<br> [9](https://rentry.org/SD_help_FAQ#L-2-9)<br>[10](https://rentry.org/SD_help_FAQ#L-2-10)<br>[11](https://rentry.org/SD_help_FAQ#L-2-11)<br>[12](https://rentry.org/SD_help_FAQ#L-2-12)<br>[13](https://rentry.org/SD_help_FAQ#L-2-13)<br>[14](https://rentry.org/SD_help_FAQ#L-2-14)<br>[15](https://rentry.org/SD_help_FAQ#L-2-15)<br>[16](https://rentry.org/SD_help_FAQ#L-2-16)<br>[17](https://rentry.org/SD_help_FAQ#L-2-17)<br>[18](https://rentry.org/SD_help_FAQ#L-2-18)|Note: switching to '3246a2d6b898da6a98fe9df4dc67944635a41bd3'.<br>You are in 'detached HEAD' state. You can look around, make experimental<br>changes and commit them, and you can discard any commits you make in this<br>state without impacting any branches by switching back to a branch.<br>If you want to create a new branch to retain commits you create, you may<br>do so (now or later) by using -c with the switch command. Example:<br>  git switch -c <new-branch-name><br>Or undo this operation with:<br>  git switch -<br>Turn off this advice by setting config variable advice.detachedHead to false<br>HEAD is now at 3246a2d Add files via upload|

Please note that `git pull` will not work in this state. To return to the most recent version, you can run `git switch master` followed by `git pull`.

#### Common issues when using Git

##### "fatal: not a git repository"

The "fatal: not a git repository" error occurs when you try to use Git commands in a directory that is not a Git repository. There are two ways to deal with this:

###### New installation

1. Open the Command Prompt (CMD) and navigate to the directory where you want to install "stable-diffusion-webui". You can do this by running `cd /d "c:\AI\"`.
2. Run the command `git clone https://github.com/AUTOMATIC1111/stable-diffusion-webui` to create a local copy of the Git repository.
3. Feel free to move or copy any of these files to the new folder:
    - Models
    - Embeddings
    - `config.json`
    - `ui-config.json`
    - `webui-user.bat` (for Windows) or [webui-user.sh](http://webui-user.sh/) (for Mac or Linux)
    - The entire `venv` folder

Going forward, you'll be able to update by running `git pull`.

###### Make it a Git repository in place

In case you don't want to install it again, you can run the following commands:

1. Open the Command Prompt (CMD) and navigate to the directory where you have installed "stable-diffusion-webui". You can do this by running `cd /d "c:\AI\stable-diffusion-webui\"`.
2. Run the command `git init` to initialize an empty Git repository in the current directory.
3. Run the command `git remote add origin https://github.com/AUTOMATIC1111/stable-diffusion-webui` to add a remote repository as the origin of your local repository.
4. Run the command `git fetch` to retrieve the latest version of the repository from the remote repository.
5. Run the command `git reset --hard origin/master` to reset your local repository to the state of the remote repository. This command will delete all changes you made to files that are being tracked by Git.
6. Run the command `git branch --set-upstream-to=origin/master master` to set the remote repository as the upstream repository for your local repository.

Going forward, you'll be able to update by running `git pull`.

##### "fatal: git detected dubious ownership in repository"

This error may occur when using Git on a FAT32 drive on Windows. It is caused by the file system's inability to store the correct user ownership information for the files in the repository.

To fix this issue, you have two options:

1. Move the repository to a drive that is formatted with the NTFS file system. NTFS is able to store the correct user ownership information, so this error will not occur.
2. Run the following command:  
    `git config --global --add safe.directory PATH_TO_DIRECTORY`  
    This will allow Git to store the repository on a FAT32 drive without generating the "dubious ownership" error. However, please note that this might not solve the issue in all cases.

If the repository is already on a NTFS formatted drive and you are still encountering this error, check if you have the correct permissions to access the folder.

##### "error: Your local changes to the following files would be overwritten by merge"

If you run `git pull` and receive an error similar to the one below, it means that git cannot automatically update the file because you have made local changes to it:  

|   |   |
|---|---|
|[1](https://rentry.org/SD_help_FAQ#L-3-1)<br>[2](https://rentry.org/SD_help_FAQ#L-3-2)<br>[3](https://rentry.org/SD_help_FAQ#L-3-3)<br>[4](https://rentry.org/SD_help_FAQ#L-3-4)|error: Your local changes to the following files would be overwritten by merge:<br>        webui.py<br>Please commit your changes or stash them before you merge.<br>Aborting|

Delete the file(s) listed in the error message and run `git pull` again. To avoid issues in the future, avoid changing any `*.py` file and only change the `webui-user.bat`. It is also being tracked by Git but the developers don't change the file so it won't cause issues with `git pull`. If you want to be on the safe side, feel free to create a copy of it and make changes to the copy instead.

Note: It is generally a good practice to avoid making changes to files that are being tracked by Git, as it can lead to conflicts when pulling updates.

##### Changing from Gitgud to Github

1. Open the Command Prompt (CMD) and navigate to the directory where you have installed "stable-diffusion-webui". You can do this by running `cd /d "c:\AI\stable-diffusion-webui\"`.
2. Run the command `git remote -v` to verify that the current remote repository is not Github.
3. Run the following commands in the Command Prompt:  
    
    |   |   |
    |---|---|
    |[1](https://rentry.org/SD_help_FAQ#L-4-1)<br>[2](https://rentry.org/SD_help_FAQ#L-4-2)<br>[3](https://rentry.org/SD_help_FAQ#L-4-3)<br>[4](https://rentry.org/SD_help_FAQ#L-4-4)<br>[5](https://rentry.org/SD_help_FAQ#L-4-5)<br>[6](https://rentry.org/SD_help_FAQ#L-4-6)|git switch -f master<br>git remote remove origin<br>git remote add origin https://github.com/AUTOMATIC1111/stable-diffusion-webui<br>git fetch<br>git reset --hard origin/master<br>git branch --set-upstream-to=origin/master master|
    

### Common problems and questions (with a focus on AUTOMATIC1111's stable-diffusion-webui)

#### Installation stuck at "pip install torch"

This step can take a long time to complete because it involves downloading multiple GBs of data. The speed of the installation will vary depending on your internet connection, and it may take up to 30-40 minutes for some users. If the installation does not seem to be making progress, try deleting the "venv" folder and restarting the installation process.

#### Error: Torch is not able to use GPU!

This error usually indicates that you are using an AMD graphics card instead of an NVIDIA one. In this case, you should follow the [AMD installation guide](https://github.com/AUTOMATIC1111/stable-diffusion-webui/wiki/Install-and-Run-on-AMD-GPUs) instead.

#### No model found! Where to get one?

##### Version 1.5

There are 2 "1.5" models for 2 different payloads.

- For text-to-image generation: [https://huggingface.co/runwayml/stable-diffusion-v1-5/blob/main/v1-5-pruned-emaonly.ckpt](https://huggingface.co/runwayml/stable-diffusion-v1-5/blob/main/v1-5-pruned-emaonly.ckpt)
- For "inpainting", "img2img" and "outpainting": [https://huggingface.co/runwayml/stable-diffusion-inpainting/blob/main/sd-v1-5-inpainting.ckpt](https://huggingface.co/runwayml/stable-diffusion-inpainting/blob/main/sd-v1-5-inpainting.ckpt)  
    After downloading the .CKPT files, place them in the "Stable-diffusion" folder located at `stable-diffusion-webui\models\Stable-diffusion` (in your SD WebUI installation).

##### Version 2

For information on obtaining and installing version 2 models, see [https://github.com/AUTOMATIC1111/stable-diffusion-webui/wiki/Features#stable-diffusion-20](https://github.com/AUTOMATIC1111/stable-diffusion-webui/wiki/Features#stable-diffusion-20)

#### What is a “flag”?

A "flag" is a setting that controls the start-up and behavior of the SD WebUI. To use them, you will need to right-click on the `webui-user.bat` file and edit it with a text editor. Then, on the line `set COMMANDLINE_ARGS=`, input one or more arguments (starting with `--`). Save the file and then double-click on `webui-user.bat` to relaunch SD. For more information on flags, see [https://github.com/AUTOMATIC1111/stable-diffusion-webui/wiki/Command-Line-Arguments-and-Settings#webui-user](https://github.com/AUTOMATIC1111/stable-diffusion-webui/wiki/Command-Line-Arguments-and-Settings#webui-user)

#### What is batch size and count?

Batch count refers to the number of groups of images that will be generated, while batch size determines the size of each group. It is generally recommended to increase batch size before increasing batch count to make the most efficient use of your GPU's resources.

#### I’ve seen additional settings in one of the videos that don’t show up for me.

To access additional settings, go to the settings/user interface menu and add the following options to the quick settings list: `sd_vae, sd_model_checkpoint, inpainting_mask_weight, sd_vae, CLIP_stop_at_last_layers`. Once you have saved your changes, you can either click the button to refresh UI components or restart the WebUI to see the new settings.  
If you want to add something else and you don't know the name of the setting, do the following:

1. In the settings, navigate to the setting you want to add.
2. Open the inspection tool (F12).
3. Select the setting and check what the ID is called.
4. The name for the quick settings is the ID name minus the setting_ part. For example, the ID setting_img2img_color_correction becomes img2img_color_correction in the quick settings list.

#### How to install a VAE file?

To install a VAE file, you can download it from the relevant repository and place it in the `models/VAE` folder. If the file has the `.ckpt` extension, you will need to rename it to `.vae.pt` before it can be used.

#### What is a VAE?

A VAE (variational autoencoder) is a type of fine-tuning model that can be used to correct some imperfections in the output of the base model. Depending on the specific VAE file being used, this may involve adjusting the color or improving the overall appearance of the generated images. VAE files can be useful in cases where the output of the base model alone is not satisfactory.

#### Image generation is slow! How to speed it up?

There is an optional module called "xformers" that can improve the speed of image generation. To use it, you can add `--xformers` to the `set COMMANDLINE_ARGS=` line in the `webui-user.bat` file. Here are some examples of flag combinations that may help improve performance based on your GPU and VRAM capacity:

- For a 16xx card: `set COMMANDLINE_ARGS=--no-half --precision full --xformers --always-batch-cond-uncond --opt-split-attention`
- For a GPU with 4 GB VRAM: `set COMMANDLINE_ARGS=--medvram --xformers`
- For a GPU with more than 4 GB VRAM: `set COMMANDLINE_ARGS=--xformers`  
    If you get a "NameError: name 'xformers' is not defined" error, make sure you are using Python 3.10. If you are using Linux and the `--xformers` flag isn't working, you can try compiling them using the instructions in the [webui wiki](https://github.com/AUTOMATIC1111/stable-diffusion-webui/wiki/Xformers).  
    Note that using the `--xformers` flag may only result in noticeable speed improvements when generating large batches of images, especially if you are using either `--lowvram` or `--medvram`.

#### Error: Cuda out of memory. What to do?

##### When generating images

This error occurs when your GPU does not have enough VRAM to run the operation. You can try using command-line arguments (also known as "[flags](https://rentry.org/SD_help_FAQ#what-is-a-flag)") to enable various optimizations that may reduce the VRAM requirements at the expense of some performance. Here are some suggested flag combinations based on your VRAM capacity and image size goals:

- If you have 4 GB VRAM and want to make 512x512 (or possibly up to 640x640) images, use `--medvram.
- If you have 4 GB VRAM and want to make 512x512 images, but still get an out-of-memory error with `--medvram`, use `--medvram --opt-split-attention` instead.
- If you have 4 GB VRAM and want to make 512x512 images, but still get an out-of-memory error with the above flag combination, use `--lowvram --always-batch-cond-uncond --opt-split-attention` instead.
- If you have 4 GB VRAM and want to make images larger than 512x512 with `--medvram`, use `--lowvram --opt-split-attention`.
- If you have more VRAM and want to make larger images than you can usually make (e.g. 1024x1024 instead of 512x512), use `--medvram --opt-split-attention`. You can also try `--lowvram`, but the effect may be minimal.

If none of these flag combinations solve the out-of-memory error, you may need to reduce the size of your input images or use a GPU with more VRAM.

##### When training

Training can be very VRAM-intensive, especially for certain methods. For example, training textual inversion (embedding) and hypernetworks typically requires less VRAM compared to Dreambooth, which may require at least 12 GB VRAM to run comfortably. For the best performance, it is recommended to use a GPU with 24 GB VRAM or more.  
If your hardware is not capable of handling the VRAM requirements for training, you may want to consider using a cloud-based service such as [Google Colab](https://rentry.org/SD_help_FAQ#run-remotely-run_remotely), or a paid service that offers access to more powerful hardware like [vast.ai](http://vast.ai/), or [runpod.io](http://runpod.io/).

#### It generates Black or Green images!

If your GPU does not support half-precision floating point numbers (a known issue with 16xx cards), the generated images may be black or green. You can try using the command-line arguments `--precision full --no-half` to fix this issue, but keep in mind that these flags will significantly increase the VRAM usage. You may also want to use the `--medvram` flag to help manage VRAM usage. To use these flags, you can add the following line to the `webui-user.bat` file: `set COMMANDLINE_ARGS=--precision full --no-half --medvram`.

#### Error: No module named pip

For some reason the module manager `pip` did not get installed. To do that manually, follow these steps:

1. Open the Command Prompt (CMD) and navigate to the directory where you have installed "stable-diffusion-webui". You can do this by running `cd /d "c:\AI\stable-diffusion-webui\"`.
2. Run the command `.\venv\Scripts\python -m ensurepip --upgrade`
3. Once the installation is complete, launch webui-user.bat again.

#### CUDA error: no kernel image is available for execution on the device after enabling xformers

If you encounter this error after enabling the xformers module, it may be because the installed version of xformers is incompatible with your GPU. To fix this, you can try adding `--reinstall-xformers --xformers` to your `COMMANDLINE_ARGS` in the `webui-user.bat` file. This will upgrade to a version of xformers that is compatible with your GPU. Note that this fix is only applicable if you are using Python 3.10, have a Pascal or newer GPU, and are running on Windows. Once the xformers module has been upgraded, you can remove the `--reinstall-xformers` flag.

#### RuntimeError: Sizes of tensors must match except in dimension 0. Expected size 1024 but got size 768 for tensor number 1 in the list.

This error is caused by using an incompatible embedding file. Embeddings trained on version 1.x models are not compatible with version 2.x models, and vice versa. Make sure that you are using the correct embedding file for the version of the model that you are using. If you are not sure which model to use, you can check the documentation for your embedding.

#### ValueError: Query/Key/Value should all have the same dtype

In the webui, go to settings -> Stable Diffusion and make sure "Upcast cross attention layer to float32" is checked.

#### Why GPU usage in task manager is low?

Some exceptions

In Windows 11 (22H2 and later for sure) you don't need to change the graphs, since 3D cores and CUDA cores are both displayed as 3D cores, so you should see the usage in the `Processes` and `Perfomance` tab without any issues.

It is important to note that the task manager's `Processes` tab displays the usage of 3D cores, also known as shading cores, which are dedicated solely for 3D graphics. However, for machine learning purposes, the usage of CUDA cores should be considered.

To view the usage of CUDA cores, please follow these steps:

1. Switch to the `Performance` tab;
2. Select `GPU 0` (or `GPU 1` if your CPU has integrated graphics);
3. Click the arrow near any graph label; and
4. select `CUDA` from the dropdown menu.

You should now see the graph display the usage of CUDA cores.

Windows 10 task manager:  
![Windows 10 Task Manager Example](https://i.imgur.com/GiuWHol.png "Windows 10 Task Manager Example")

## Credits

Written by @Spaceginner#7688, @Camulorix#8583 & @aitrepreneur#8057, grammar enhanced by chatGPT. If you want to contribute, feel free to contact us.

[Edit](https://rentry.org/SD_help_FAQ/edit)

Export

Pub: 30 Dec 2022 15:41 UTC  
Edit: 05 Mar 2023 13:14 UTC  
Views: 18244  

---

[new](https://rentry.org/)·[what](https://rentry.org/what)·[how](https://rentry.org/how)·[langs](https://rentry.org/langs)·[contacts](https://rentry.org/what#contacts)