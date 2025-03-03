---
feature: "![[../03 - MEDIA & FILES/422a6e87f364c87d1ebec3fc37ecd7d6_MD5.png]]"
---
A composite vault is defined -- just now, by yours truly, and probably not for the first time -- as a vault that contains other vaults.

Why would you do so? You kinda get the best of both worlds. You can have the separation normally offered by Obsidian via separate vaults, while still being able to keep _some_ of the configs the same across all of them -- E.g. if you have a _part_ of your vault where some plugins apply, but these plugins don't even work on mobile. You thus can have a separate, sub-vault for it _while_ still keep using themes and hot keys from the main vault.

To summarize, a _composite vault_ achieves the following:

- Individual vaults that can still combine into a single, larger vault.
- Synced settings -- with customizable extent of synchronization

Here's a guide -- what attempts to resemble one, anyway -- on how to achieve that.

### Prerequisites

- This is an OSX based setup. The same can probably also be done in Windows, but I don't know how well that'd work. Ask a friend?
- The guide assumes a basic level of familiarity with the OSX terminal.

### Warnings

- If you don't feel safe about the phrase _symbolic links_, maybe stop reading.
- _Probably_ don't try to sync a composite vault. If you do, either **only sync the main vault**, or non-overlapping subvaults. The former is what I did.
    - Addendum on syncing -- if you use Obsidian Sync, note that it doesn't index hidden subfolders that are not the main config folder. If you are syncing the main vault, the subvaults' configs will _not_ be synced. As such, this setup only really works for a single-driver setup. If you need to sync between two equally usable devices (as opposed to one desktop and 3 mobile devices), consider the drawbacks.
- You might need to re-sign-in and/or reconfigure Sync due to vault structure changes. Conveniently, this prevents your subvaults from accidentally syncing and messing things up.
- If you are gonna do anything with your real data, _back the heck up_.
- **I will not be held responsible for anything that happens to your vault if you try to follow this -- I am not saying this is something you _should_ do, _even if_ it matches your needs.**
- (This is probably not as dangerous as I'm making it out to be, but I also don't want your vault wiped accidentally.)

## The Simple(?) Example

![composite_vault_2.png](../03%20-%20MEDIA%20&%20FILES/422a6e87f364c87d1ebec3fc37ecd7d6_MD5.png)

Let's start with a Simple™ example. Find a folder that you are partial to, like maybe `Documents`, and make a new folder in there, like `ObsidianExperiment`, or a name you believe fitting for the big ol' composite vault. Imma do these steps in the shell if you wanna follow, but you can do these bits perfectly fine using Finder.

```zsh
cd ~/Documents
mkdir ObsidianExperiment
cd ObsidianExperiment
```

Inside the new folder that is to become your new vault, make some more folders. Name them things appropriate for sub vaults. You might do `School`, `Art`, and `Leisure`; I went the creative route with `SubVault1`, `SubVault2` and `SubVault3`. If you are going to use your own names, remember to substitute them in in all the upcoming commands.

```zsh
mkdir SubVault1
mkdir SubVault2
mkdir SubVault3
```

Notice how so far we've _not_ opened Obsidian yet? Keep it that way.

Next, while still in `ObsidianExperiment`, make a folder called `.obsidian`.

```zsh
mkdir obsidian
```

And here's the fun part. If you just open Obsidian now and open these folders as vaults, then all their configurations will be isolated, not synchronized. Surely we don't want that. I mean, who has the time and energy to manage four identical sets of configs?

This next bit, do it in the shell. If you are _not_ following the previous steps, now would be a good time to open the Terminal app, and then do `cd ~/Documents/ObsidianExperiment`. Having linked up with the readers who did follow in the shell, here are the next steps.

```zsh
ln -s $(pwd)/.obsidian $(pwd)/SubVault1/.obsidian
ln -s $(pwd)/.obsidian $(pwd)/SubVault2/.obsidian
ln -s $(pwd)/.obsidian $(pwd)/SubVault3/.obsidian
```

Now you can go ahead and finally open Obsidian. We laid the foundation for four vaults in total -- `ObsidianExperiment`, which contains `SubVault1`, `SubVault2` and `SubVault3`. Open each in Obsidian using `Open folder as vault`. Play around with them, change settings, choose themes, all that. You should notice that the changes you made to one vault, will show up when you open another.

Now dump notes into these vaults! Or not.

![vault1.png](../03%20-%20MEDIA%20&%20FILES/093da51b8fb27ea3eb6107696b0e8097_MD5.png)

## The Not Harder, but More Annoying customization

> What if I want the vaults to have the same themes and core settings, but different sets of plugins?

I'm glad you (or me, really) are asking the very piercing questions. Turns out, if you followed the perhaps overly simplified guide above, you'll notice that all configs -- and I mean _all_ configs -- are synced, leaving no room to per vault customization.

What if, for example, you want `SubVault3` to be your DnD vault, and you want the plugins within to be solely restricted to that vault and no others? Back to the shell we go!

Oh and quit Obsidian first.

```zsh
# Assuming $CWD is still ~/Documents/ObsidianExperiment -- you
# still remember how to get there in the shell, right?
cd SubVault3
rm .obsidian
mkdir .obsidian
cd .obsidian
ln -s ~/Documents/ObsidianExperiment/.obsidian/* ./
```

What these steps does is, instead of using a synced `.obsidian` folder, it instead makes a normal folder, and syncs all the individual config files over instead. And now, you want your plugins independent-ified...

```zsh
rm community-plugins.json
# plugins is a symlink to a folder, so no -rf needed
rm plugins
# probably also this next one if you want to save your DnD workspace
rm workspace workspaces.json
```

Now you can setup your community plugins in `SubVault3` and they will be completely unrelated to the main vault or the other two, _while_ still receiving sync settings on themes and hotkeys and stuff.

What if you want to customize different aspects? Well, I'm sure the names of these files in `.obsidian` in the _subvaults_ are sufficiently self-explanatory. It's the same process:

- Remove the previously symlinked folder
- Create a new `.obsidian` folder from scratch
- Symlink all files from the root vault's `.obsidian`
- Remove the ones you want to customize -- this is so that your local version that will be created when you open obsidian will be unlinked.
- Customize your vault as usual

![vault3.png](../03%20-%20MEDIA%20&%20FILES/04a2e75ec9ce952f97e9e72f8cb0e30f_MD5.png)

## Questions, Frequently Asked or Not

> Why?

If you don't see a need for this, that's totally fine. I don't aim to persuade.

> This is not very beginner friendly.

I'm terribly sorry but that's kinda what I'm going for.

> How would this translate to Windows?

I don't know. I don't use my Windows machine for anything other than video games. If I have an answer here, it'd be something I just Googled and haven't personally verified.

> How would this translate to Linux?

Identically.

> How would this work on Mobile?

It doesn't. I think.

> Can I sync vaults set up like so?

I sync my main vault and it seems unbroken so far. The main things to note are already listed above. Basically, don't sync main _and_ subvaults, and this won't work on more than one main driver devices.

> How would this work with git?

I don't know since I don't use git in my setup. If you are using git, you hopefully know enough about it to deduce the outcome; if you don't, probably don't try.

> I already have a vault and would like this setup, how do I apply these retroactively?

The gist is the same. Pick the folders you want to make vaults of, then either jsut link over the main `.obsidian` for fully-synced setups, or create `.obsidian` and link over only the settings you want synced.

> Can I have a composite vault with subvaults located in multiple different locations, but not have to take their lowest common ancestor in the filesystem tree?

I haven't tried but it should be similar: individual subvault setup process is the same, then just symlink all the subvaults to the empty main vault folder.

> Can I have _some_ but not all of the plugins synced between my main and this one subvault?

I don't know of a way.

## TLDR for the Shell Masters

- Pick folders you want to become subvaults
- Create `.obsidian` in them and symlink from main vault the settings you want to _keep_, remove those you want to keep independent.
- Open these folders as vaults.
- Sync only the main vault.

![symlink_in_ob.png](../03%20-%20MEDIA%20&%20FILES/d584806658524515a3c224956c779efc_MD5.png)