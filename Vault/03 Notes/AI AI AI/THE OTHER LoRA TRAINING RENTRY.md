  **Stable Diffusion LoRA training science and notes**By yours truly, The Other LoRA Rentry Guy.

This is not a how to install guide, it is a guide about how to improve your results, describe what options do, and hints on how to train characters using bad or few images.

Due to the higher prevalence of LyCORIS contents, I'll start referring to "regular LoRA" as LoRA-LierLa. If I left any plain "LoRA" around, assume it's talking about LoRA-LierLa. LyCORIS types will be referred to as LyCORIS-(type), such as LyCORIS-LoKR, if not specified, consider it applies to most or all types.

Training SDXL with about 8GB of VRAM is possible!

### 20230807

I found how to train and run SDXL in my hardware, so started a SDXL section [here](https://rentry.org/59xed3#sdxl).

### 20230801

I had a few questions about resuming training from an existing LoRA.  
Never tried it before but turned out to be very effective for models that need just a bit more time in the oven, so added [resuming training](https://rentry.org/59xed3#resuming-training) for this specific approach.  
I also tested a bit of a multi-step strategy which, at least in the first experiment, seemed to work nicely. Like, bake most epochs with a linear scheduler then do a couple more with cosine or logarithmic.

### 20230731

Spent the entire weekend experimenting with LyCORIS and well, I think I can call it wraps on the section for now.  
They are great for style and concept stuff, but it can only learn "simple" characters well. Which prompted a new section [Character difficulty](https://rentry.org/59xed3#character-difficulty). Which in retrospect I should have added earlier.  
With that in mind **I cannot recommend LyCORIS in general (locon is fine though) for characters**, unless it's characters in the lower categories. It can handle "realistically plausible" anime girls fine, but beyond that you'll need to fiddle with settings a bit too much or use too much time training, or use settings requiring more than 8GB of VRAM, which counters many of the seemingly juicy advantages that it has on paper.  
**Still, for styles and concepts, they seem to be the way to go**. Those tend to be longer bakes anyway, so it being a bit slower or taking a couple more epochs is not as much of a problem because it seems to be able to digest 10000+ datasets very well and usually at a smaller size, the dampening it has on learning rates is also somewhat beneficial for styles and concepts, so it seems like LyCORIS is very well suited for them, at least Locon and maybe DyLoRA.

- Reviewed [Min. SNR Gamma](https://rentry.org/59xed3#min-snr-gamma_1) with more conclusive results
- Added [Scale Weight Norms](https://rentry.org/59xed3#scale-weight-norms) information.
- [LyCORIS (LoHA/LoCon/Etc)](https://rentry.org/59xed3#lycoris-lohaloconetc) wrapped up, I think.
- Reviewed [Learn dampening](https://rentry.org/59xed3#learn-dampening) section a bit.
- Some notes about [Loss](https://rentry.org/59xed3#loss).
- Glossary updated further.

### 20230728

- Updated a few more sections in general.
- While it's been known from the start that LoRAs could be mixed with checkpoints (as the original recipe for LoRAs made large checkpoints instead of the smaller files we deal with today), I've seen it mentioned as a "new thing". I decided to elaborate a bit about it here: [Mixing LoRAs into checkpoints](https://rentry.org/59xed3#mixing-loras-into-checkpoints) to bring more attention to the fact that it's a thing you can make use of.
- Expanded [Weighted training](https://rentry.org/59xed3#weighted-training) a bit more.
- [LyCORIS (LoHA/LoCon/Etc)](https://rentry.org/59xed3#lycoris-lohaloconetc) updated some more.
- What? SDXL 1.0 is out already? I'll have to check it out. I read CitivAI is doing some contest, if my machine is up to the task I'll add some info here to try to help out contestants. I'm not participating, can't deal with the PR time waste of uploading models unless asked to, so it's purely for the science.
    - Oof, seems 8GB aren't enough for SDXL. This is unfortunate.

### 20230727

- [LyCORIS (LoHA/LoCon/Etc)](https://rentry.org/59xed3#lycoris-lohaloconetc) section updated accordingly.
- Made the warning about lower network ranks/alpha requiring bigger learning rates more visible as seems people were missing it.
    - Note that adaptive optimizers should already take this into account so it's only necessary if you are specifying learning rates manually.
    - Although adding a few more epochs to adaptive ones can help counter the dampening.
- Overhauled the [Rare character/OC HOWTO](https://rentry.org/59xed3#rare-characteroc-howto) with some more details.
- I'll expand the weights section further soon.

### 20230726

Ah, LyCORIS now is integrated directly with sd-webui, meaning its integration is not an issue anymore.  
This negates most issues with LyCORIS as a container, making it far more viable to train with, as it is now a first-class citizen in the ecosystem.  
This is pretty great news!

### 20230722

Changed [Starting settings](https://rentry.org/59xed3#starting-settings) a bit.  
I'll give SDXL a shot when 1.0 is released. I don't know if 8GB can handle it, but if it can I'll expand upon it.  
At this point I've given `Prodigy` enough testing to call it good, keep it in mind.

### 20230720

Made some major rewrites to a bunch of sections with updated knowledge, removed things that don't matter anymore and put emphasis on that **you should not be giving training rates manually anymore, use adaptive optimizers to remove the guesswork**. You should only do it if you don't have enough VRAM for them, or if you want a challenge.

Things have changed a lot since the guide was started, haven't they? It's so easy to train first try now. I don't think I have struggled with any character training since `DAdaptAdam` outside of "2 more epochs" or "bit more rank" or "cleaning up tags".  
It's still a good idea to keep this guide up with explanations and a bit more detail so there's a middle ground between "_layman's knowledge_" and "_literal scientific paper_".

- Added a section about furry characters because I keep getting asked.
- Should I remove the scripts? People seems to mostly be using bmaltais' Kohya GUI nowadays, which is a good idea for most situations.
    - I still use scripts myself, but more so I can batch works while I am outside or sleeping and then shut the computer down when finished, but few people are gonna bother doing that and they probably already know how to write some scripts.
- Added a bit about testing models in multiple checkpoints, as it's more relevant now than when the guide started.
- Updated [Net dim (network dimensions)/Rank](https://rentry.org/59xed3#net-dim-network-dimensionsrank) accordingly.
- Updated the [LyCORIS (LoHA/LoCon/Etc)](https://rentry.org/59xed3#lycoris-lohaloconetc) part a bit. I don't really like them for characters, but they really work nicely for styles and concepts, articles of clothing and such.
- Added a tiny blurb about the seed because I have now witnessed more than one situation where it mattered. Just in case.

## PREAMBLE

This guide is meant to co-exist with other guides about LORA training.  
It's intended to be a middle-ground between "brutally dry scientific papers" and "my first LoRA for grandmas and newbies", detailing the effects of options and explanations about what they are supposed to be doing to the best of my ability, as well as detailing my results and sharing my tips and tricks.

While I'd love to make the guide fairly image-heavy, the sheer amount of them would be troublesome if someone is checking the guide in a phone or a slow internet connection, so I'll try to be as descriptive as possible.

My end goal is making it so everyone can train a character, specially obscure or forgotten ones. But if something is obviously useful for styles or concepts I'll mention it as well.

I'll also note things that can improve your results when uploading to CivitAI or such services by pointing less-than-ideal or wasteful settings. And advice on the opposite, tweaking models for your own specific taste, as well.

1. [20230807](https://rentry.org/59xed3#20230807)
2. [20230801](https://rentry.org/59xed3#20230801)
3. [20230731](https://rentry.org/59xed3#20230731)
4. [20230728](https://rentry.org/59xed3#20230728)
5. [20230727](https://rentry.org/59xed3#20230727)
6. [20230726](https://rentry.org/59xed3#20230726)
7. [20230722](https://rentry.org/59xed3#20230722)
8. [20230720](https://rentry.org/59xed3#20230720)
9. [PREAMBLE](https://rentry.org/59xed3#preamble)
10. [INSTALLING KOHYA'S TRAINING SCRIPT](https://rentry.org/59xed3#installing-kohyas-training-script)
    1. [Ubuntu 23.04 step-by-step guerrilla installing.](https://rentry.org/59xed3#ubuntu-2304-step-by-step-guerrilla-installing)
        1. [Python 3.10 is not available in Ubuntu >=23.04](https://rentry.org/59xed3#python-310-is-not-available-in-ubuntu-2304)
            1. [Building Python](https://rentry.org/59xed3#building-python)
            2. [Setting up special venv](https://rentry.org/59xed3#setting-up-special-venv)
            3. [Phantom library versions](https://rentry.org/59xed3#phantom-library-versions)
    2. [Kohya-ss by bmaltais](https://rentry.org/59xed3#kohya-ss-by-bmaltais)
        1. [Ubuntu 23.04](https://rentry.org/59xed3#ubuntu-2304)
11. [ANCIENT NINJA WISDOM](https://rentry.org/59xed3#ancient-ninja-wisdom)
    1. [Glossary](https://rentry.org/59xed3#glossary)
    2. [Why so many scripts, it's confusing!](https://rentry.org/59xed3#why-so-many-scripts-its-confusing)
    3. [Why aren't there more precise numbers?](https://rentry.org/59xed3#why-arent-there-more-precise-numbers)
    4. [I want to make a perfect LORA, I'm carefully arranging all the elements until it's perfect and...](https://rentry.org/59xed3#i-want-to-make-a-perfect-lora-im-carefully-arranging-all-the-elements-until-its-perfect-and)
        1. [So what do I do first?](https://rentry.org/59xed3#so-what-do-i-do-first)
    5. [Is dreambooth useless now?](https://rentry.org/59xed3#is-dreambooth-useless-now)
        1. [But I heard LoRA sucks compared to dreambooth.](https://rentry.org/59xed3#but-i-heard-lora-sucks-compared-to-dreambooth)
        2. [Are hypernetworks useless now?](https://rentry.org/59xed3#are-hypernetworks-useless-now)
        3. [Are embeds (textual inversion) useless now?](https://rentry.org/59xed3#are-embeds-textual-inversion-useless-now)
    6. [Making LORAs from the difference between two models ("distill")](https://rentry.org/59xed3#making-loras-from-the-difference-between-two-models-distill)
    7. [Mixing LoRAs into checkpoints](https://rentry.org/59xed3#mixing-loras-into-checkpoints)
12. [Getting started](https://rentry.org/59xed3#getting-started)
    1. [What do I need to get started?](https://rentry.org/59xed3#what-do-i-need-to-get-started)
    2. [Character difficulty](https://rentry.org/59xed3#character-difficulty)
        1. [Female bias](https://rentry.org/59xed3#female-bias)
        2. [Prior training](https://rentry.org/59xed3#prior-training)
        3. [Intended results](https://rentry.org/59xed3#intended-results)
        4. [Character difficulty and settings](https://rentry.org/59xed3#character-difficulty-and-settings)
        5. [Vehicles](https://rentry.org/59xed3#vehicles)
    3. [Starting settings](https://rentry.org/59xed3#starting-settings)
        1. [Optimal settings](https://rentry.org/59xed3#optimal-settings)
        2. [The "Easy settings" ⭐⭐](https://rentry.org/59xed3#the-easy-settings)
    4. [What model to train from?](https://rentry.org/59xed3#what-model-to-train-from)
        1. [Legal concerns over NAI](https://rentry.org/59xed3#legal-concerns-over-nai)
        2. [AnyLoRA](https://rentry.org/59xed3#anylora)
        3. [The furries keep asking](https://rentry.org/59xed3#the-furries-keep-asking)
13. [LEARNING RATES](https://rentry.org/59xed3#learning-rates)
    1. [Text encoder learning rate](https://rentry.org/59xed3#text-encoder-learning-rate)
    2. [Unet learning rate](https://rentry.org/59xed3#unet-learning-rate)
    3. [Optimizers](https://rentry.org/59xed3#optimizers)
        1. [Lion](https://rentry.org/59xed3#lion)
        2. [AdaFactor](https://rentry.org/59xed3#adafactor)
        3. [DAdaptation ⭐](https://rentry.org/59xed3#dadaptation)
        4. [Prodigy](https://rentry.org/59xed3#prodigy)
        5. [d](https://rentry.org/59xed3#d)
        6. [d_coef](https://rentry.org/59xed3#d_coef)
        7. [Schedulers](https://rentry.org/59xed3#schedulers)
        8. [Min. SNR Gamma](https://rentry.org/59xed3#min-snr-gamma)
    4. [Scheduler](https://rentry.org/59xed3#scheduler)
14. [TYPES OF TRAINING](https://rentry.org/59xed3#types-of-training)
    1. ["Finetune style" (Default)](https://rentry.org/59xed3#finetune-style-default)
        1. [Multiple concept support](https://rentry.org/59xed3#multiple-concept-support)
    2. ["Dreambooth style"](https://rentry.org/59xed3#dreambooth-style)
        1. [When to use "finetune" or "dreambooth style" training](https://rentry.org/59xed3#when-to-use-finetune-or-dreambooth-style-training)
    3. ["Keyword style"](https://rentry.org/59xed3#keyword-style)
    4. [Resuming training](https://rentry.org/59xed3#resuming-training)
    5. [LyCORIS (LoHA/LoCon/Etc)](https://rentry.org/59xed3#lycoris-lohaloconetc)
        1. [Pros](https://rentry.org/59xed3#pros)
        2. [Cons](https://rentry.org/59xed3#cons)
        3. [LyCORIS-LoCon](https://rentry.org/59xed3#lycoris-locon)
        4. [LyCORIS-LoHA](https://rentry.org/59xed3#lycoris-loha)
        5. [LyCORIS-LoKR](https://rentry.org/59xed3#lycoris-lokr)
        6. [LyCORIS-(IA)^3](https://rentry.org/59xed3#lycoris-ia3)
        7. [Conclusion (character-oriented)](https://rentry.org/59xed3#conclusion-character-oriented)
    6. [SDXL](https://rentry.org/59xed3#sdxl)
        1. [Be careful](https://rentry.org/59xed3#be-careful)
    7. [Weighted training](https://rentry.org/59xed3#weighted-training)
        1. [The Unet and its blocks](https://rentry.org/59xed3#the-unet-and-its-blocks)
        2. [LoRA blocks](https://rentry.org/59xed3#lora-blocks)
        3. [Testing weights before training](https://rentry.org/59xed3#testing-weights-before-training)
            1. [LyCORIS](https://rentry.org/59xed3#lycoris)
        4. [Setting up](https://rentry.org/59xed3#setting-up)
15. [PREPARING IMAGES](https://rentry.org/59xed3#preparing-images)
    1. [Selecting images](https://rentry.org/59xed3#selecting-images)
    2. [The short version](https://rentry.org/59xed3#the-short-version)
    3. [The long version](https://rentry.org/59xed3#the-long-version)
        1. [Consistency of individual elements](https://rentry.org/59xed3#consistency-of-individual-elements)
        2. [Teaching individual elements](https://rentry.org/59xed3#teaching-individual-elements)
    4. [Image size/aspect ratio](https://rentry.org/59xed3#image-sizeaspect-ratio)
    5. [REGULARIZATION IMAGES](https://rentry.org/59xed3#regularization-images)
        1. [Easy route](https://rentry.org/59xed3#easy-route)
            1. [Easy explanation:](https://rentry.org/59xed3#easy-explanation)
        2. [Hard route](https://rentry.org/59xed3#hard-route)
            1. [Hard explanation:](https://rentry.org/59xed3#hard-explanation)
        3. [Random images](https://rentry.org/59xed3#random-images)
    6. [TAGGING YOUR IMAGES (FINETUNING ONLY, IMPORTANT!!!!)](https://rentry.org/59xed3#tagging-your-images-finetuning-only-important)
        1. [When to tag characters/styles](https://rentry.org/59xed3#when-to-tag-charactersstyles)
        2. [Tags and details](https://rentry.org/59xed3#tags-and-details)
            1. [What to tag](https://rentry.org/59xed3#what-to-tag)
            2. [What not to tag](https://rentry.org/59xed3#what-not-to-tag)
            3. [False positives/autotagging](https://rentry.org/59xed3#false-positivesautotagging)
            4. [Consolidating tags](https://rentry.org/59xed3#consolidating-tags)
            5. [Tag debugging](https://rentry.org/59xed3#tag-debugging)
16. [OTHER TRAINING PARAMETERS](https://rentry.org/59xed3#other-training-parameters)
    1. [CLIP skip](https://rentry.org/59xed3#clip-skip)
    2. [Number of steps/epochs](https://rentry.org/59xed3#number-of-stepsepochs)
    3. [Learn dampening](https://rentry.org/59xed3#learn-dampening)
    4. [Net dim (network dimensions)/Rank](https://rentry.org/59xed3#net-dim-network-dimensionsrank)
    5. [Network Alpha](https://rentry.org/59xed3#network-alpha)
    6. [Noise offset](https://rentry.org/59xed3#noise-offset)
    7. [Resolution](https://rentry.org/59xed3#resolution)
    8. [Augmentations](https://rentry.org/59xed3#augmentations)
    9. [Min. SNR Gamma](https://rentry.org/59xed3#min-snr-gamma_1)
    10. [Scale Weight Norms](https://rentry.org/59xed3#scale-weight-norms)
    11. [Seed](https://rentry.org/59xed3#seed)
    12. [Loss](https://rentry.org/59xed3#loss)
17. [TESTING AND DEBUGGING MODELS](https://rentry.org/59xed3#testing-and-debugging-models)
    1. [Why testing?](https://rentry.org/59xed3#why-testing)
    2. [Strength (at generation time)](https://rentry.org/59xed3#strength-at-generation-time)
    3. [Test your model with multiple checkpoints](https://rentry.org/59xed3#test-your-model-with-multiple-checkpoints)
    4. [Overfitting](https://rentry.org/59xed3#overfitting)
        1. [If you have the additional-networks extension](https://rentry.org/59xed3#if-you-have-the-additional-networks-extension)
    5. [Debugging tagging](https://rentry.org/59xed3#debugging-tagging)
18. [Rare character/OC HOWTO](https://rentry.org/59xed3#rare-characteroc-howto)
    1. [Image preparation](https://rentry.org/59xed3#image-preparation)
    2. [Image editing](https://rentry.org/59xed3#image-editing)
        1. [Quick Krita starter pack](https://rentry.org/59xed3#quick-krita-starter-pack)
    3. [Using the AI to help you out](https://rentry.org/59xed3#using-the-ai-to-help-you-out)
    4. [Using raw AI outputs as inputs](https://rentry.org/59xed3#using-raw-ai-outputs-as-inputs)
    5. [The GACHAMAX Temporary LoRA approach (last resort)](https://rentry.org/59xed3#the-gachamax-temporary-lora-approach-last-resort)
    6. [General advice](https://rentry.org/59xed3#general-advice)
    7. [For readers with art skills](https://rentry.org/59xed3#for-readers-with-art-skills)
19. [SAMPLE POWERSHELL SCRIPT (WINDOWS)](https://rentry.org/59xed3#sample-powershell-script-windows)
20. [SAMPLE BASH SCRIPT (LINUX)](https://rentry.org/59xed3#sample-bash-script-linux)

## INSTALLING KOHYA'S TRAINING SCRIPT

Clone [https://github.com/kohya-ss/sd-scripts](https://github.com/kohya-ss/sd-scripts) and follow the install instructions.

**DO NOT INSTALL IT IN THE SAME PLACE AS YOUR WEBUI INSTALL! MAKE A NEW PYTHON VIRTUAL ENV!**

⚠ The script uses different library versions and WILL break your webui. ⚠  
Once you've followed the install instructions, grab the bash (linux) or powershell (windows) scripts at the bottom of this rentry and edit paths as required to launch Kohya's script. I'll add command line arguments as I keep testing stuff.

Some features require to be added separately now, such as DAdaptation. They will be noted as necessary.

### Ubuntu 23.04 step-by-step guerrilla installing.

#### Python 3.10 is not available in Ubuntu >=23.04

While not as much of an issue with sd-webui, Kohya scripts require very specific versions. You need to force things a little. This has the _happy accident_ side effect of a ~5% speed boost compared to defaults, which is always welcomed.  
You must build a separate version of Python 3.10 and use it for the venv. Procure the latest tarball for Python, unpack it somewhere and get a terminal running there.

- Ensure installing `libssl-dev` (or pip won't be able to download anything)
- Ensure installing `libbz2-dev` (it's a default library that needs to be there for Kohya's scripts)
- Of course, build-essential and such must be installed. Libraries like tk (for tkinter) and such are not required (??).  
    `sudo apt install libssl-dev libbz2-dev` will get it done.

##### Building Python

|   |   |
|---|---|
|[1](https://rentry.org/59xed3#L-1-1)<br>[2](https://rentry.org/59xed3#L-1-2)|./configure --enable-optimizations --with-ensurepip=install --prefix="/mnt/DATA/AI/Python310" --with-ssl-default-suites=openssl<br>make -j8 && make install   # No root privileges required since it'll be a local folder.|

##### Setting up special venv

Once Python 3.10.x is all set up, we want to use that specific version to set up the virtual env.  

|   |   |
|---|---|
|[1](https://rentry.org/59xed3#L-2-1)<br>[2](https://rentry.org/59xed3#L-2-2)|/mnt/DATA/AI/Python310/bin/python3.10 -m venv venv   # Of course, change path as necessary.<br>. venv/bin/activate                                  # We should now be able to proceed.|

##### Phantom library versions

After the install is complete, xformers is likely to have been left behind because there's no built package for Linux systems that is compatible with the default install of PyTorch. The solution is to let it install the default packages then override a few versions. These are proven to work properly.  

|   |   |
|---|---|
|[1](https://rentry.org/59xed3#L-3-1)<br>[2](https://rentry.org/59xed3#L-3-2)|pip install torch==2.0.0 torchvision==0.15.1 -f https://download.pytorch.org/whl/cu117<br>pip install xformers==0.0.17|

### Kohya-ss by bmaltais

[kohya_ss](https://github.com/bmaltais/kohya_ss#installation) is an alternate setup that frequently synchronizes with the Kohya scripts and provides a more accessible user interface.  
Head to the link to see the installation instructions. Similar to the above, do **not** install it in the same place as your webui.  
This is exactly the same thing as using scripts and is much more accessible, and recommended, for Windows users.  
Option names and things should be mostly the same, so use it for a more hassle-free experience.

#### Ubuntu 23.04

- The use the same steps for building python and setting up the special venv. However, `tkinter` is used in kohya-ss, so make sure you have `tk8.6-dev` installed (`sudo apt install tk8.6-dev`) when building python 3.10.
    - The output of make will show a `The necessary bits to build these optional modules were not found:` list near the end. Make sure `tkinter` is not there.
- The installing script will set everything else up.

## ANCIENT NINJA WISDOM

### Glossary

|Term|Description|Term|Description|
|---|---|---|---|
|Model|Also known as "checkpoint", it's the results of training, usually distributed as a single file containing "weights"|Embed|Also known as "textual inversion". It's an older style that only trains the text encoder|
|Baking|Household name for training a model|Hypernetwork|Similar to an embed, but acting on the Unet instead|
|Ninja Scrolls|Funny nickname for the full documentation of Kohya's scripts (In Japanese)|Subject|Training a character, object, vehicle, background...into a model|
|Kohya|Developer of the training scripts and other Stable Diffusion-related technologies|Style|Training a model to reproduce a specific aesthetic|
|WebUI|The most common Stable Diffusion generation tool|Concept|Training a model to reproduce something like a pose or composition|
|Extension|An extension for WebUI, like a plugin. Can be added from WebUI's extensions tab.|Training set|A combination of your training images and tags|
|Voldy|AUTOMATIC1111, author of webui|Distilling|Household term for extracting a LORA from a bigger model|
|Unet|The system that controls how the machine learns images and some unknown decision/association properties|Overfitting|A model tries to reproduce the training set too aggressively|
|Text Encoder(TE)|The system that translates your prompt's words or tokens into data the AI understands|Deep-frying|An effect where the generated images have very saturated colors, usually a result of high CFG scale|
|CLIP|A text encoder, typically the one we will be training. Stable Diffusion v2 models use OpenCLIP instead|Interrogator|A smaller AI that gives you the tags of the things it finds in an image|
|Net Dim|Also known as "rank", it's the total capacity of the model, usually reflected as a bigger file|Inference|The process that generates the AI's output. Can be used as a synonym for "generating"|
|AI|Actually, this is less of an AI and more "machine learning", but it's easier to call it "AI" informally|LyCORIS|Lora beYond Conventional methods, Other Rank adaptation Implementations, a different way to implement LoRA|
|Dreambooth|A different type of training, resulting in bigger files (2-4GB)|LierLa|(or LoRA-LierLA) LoRA for _Li_n_e_a_r_ _La_yers, the original LoRA|
|LORA|The type of training covered in this guide. The formal spelling is "LoRA", from "Low Rank Adaptation"|C3Lier|(or LoRA-C3Lier) LoRA for _C_olutional _3_x3 Kernel and _Li_near Layers. An alternate LoRA type, not commonly used.|
|Body Plan|The composition of a body, where all parts go, like the position of the arms, head, eyes and such.|||

### Why so many scripts, it's confusing!

The Powershell/Bash script is just to _launch_ the _Kohya_ script with a bunch of long and tedious arguments that are a pain to write manually.  
If you know what you are doing you don't need either.The Powershell/Bash scripts are a convenience feature, even if it can get confusing. Imagine typing and changing all that stuff by hand every time!  
It's also a base for craftier users to automate training batches and the like.  
**Today you have alternatives like bmaltais' user interface, in a similar style to sd-webui, so you can just ignore the scripts.** So you don't need to bother with them unless you want to.

### Why aren't there more precise numbers?

Everything is highly approximated and abstract because we are dealing with something subjective like art quality and expectations, so it's difficult to get precise measurements for anything that isn't obvious. That the results are heavily randomized doesn't help.

### I want to make a perfect LORA, I'm carefully arranging all the elements until it's perfect and...

Don't. Stop. You are spending too much time planning and too little time baking.  
It's **impossible** to entirely predict what the AI is going to do, what elements it's going to struggle with, how it will accept the given images and so on.

#### So what do I do first?

Bake a test model first and troubleshoot it later. It's the only way to know how the AI has understood the training set. Use some default numbers and then come here when troubles arise so you can figure out how to solve or improve on it.  
It doesn't take long to bake and you might just get lucky and get it first try, even with a sloppy training set.

### Is dreambooth useless now?

No. While it's a lot more economical and usually faster to train a LORA, dreambooths are still useful as:

- Making full models to mix with.
- Making models to train from (like, a dreambooth for the style of a series, then train the characters from that dreambooth).
- Styles in general.

#### But I heard LoRA sucks compared to dreambooth.

Not really. You are probably remembering the _good_ dreambooths. A poorly trained dreambooth is as sad as a poorly trained LoRA.  
LoRA training just made it easier (faster/using regular hardware) to notice a lot of bad practices and advice that was floating around before it became accessible.  
A well trained LoRA is comparable to a dreambooth in results _at a similar scope_ (one/few characters, a style, etc), and with modern techniques it's definitely better, and much more sustainable (Do you _really_ want to use 2/4GB for every character?).

#### Are hypernetworks useless now?

They can still be used for styles, but it's admittedly the most obsolete technique by now, specially since you can now select separate Unets in webui for a similar (although less controllable) effect.  
However if you have a hypernetwork you like and use, there's no reason to stop using it, since it's still maintained.

#### Are embeds (textual inversion) useless now?

They have proven to be quite useful for negative embeddings and simplifying certain complicated prompts.

### Making LORAs from the difference between two models ("distill")

The sacred ninja scrolls mention a very useful tool included with the scripts.  
This individual script allows you to create a LORA from a first model and a second model trained from that first model. For example, you could create a model out of the difference between NAI and HLL, or NAI and Anything v3.  
The obvious advantage is that you can then plug that LORA when generating with any other model and obtain benefits similar to a mix, but adjustable on the fly. Models that have only one gimmick or multiple versions with subtle differences can probably be safely converted to LORAs and give your hard disk a break. Just extract the juice.  
From my testing it's about 95% as good as the finetuned model, but takes a lot less time to swap and is friendlier to experiment with when generating images.

To set it up, first you need to go into the sd-scripts directory and open a terminal.

Enter your python virtual env first.

And then run the `networks/extract_lora_from_models.py` script as follows:  

|   |   |
|---|---|
|[1](https://rentry.org/59xed3#L-4-1)|python networks/extract_lora_from_models.py --model_org <original model (eg. NAI)> --model_tuned <model you want to extract juice from> --save_to <output file.safetensors> --dim <dimensions, more = bigger and more precise, 256 works well for me>|

You can then load the resulting LORA as any other.

[This](https://pixeldrain.com/u/RjE3psRf) LORA is a sample distilled version of the HLL2 model. Was created with dim 192. Works fine for me.

### Mixing LoRAs into checkpoints

With checkpoint I'm referring to a large model such as AOM3 or Anything.  
LoRAs can indeed be using as mixing ingredients. Certain extensions such as [supermerger](https://rentry.org/59xed3) will allow you to merge a LoRA into a checkpoint, like you would mix another model.  
Supermerger is a bit intimidating, but in the LoRA tab you can find the settings to merge LoRA to a checkpoint (usually the **checkpoint the LoRA was trained from**) or even a quick, scriptless version to distill/extract a LoRA (also comparing to the checkpoint it was trained from), then you can mix the results normally.

Originally LoRAs were supposed to be full-blown models, 2/4GB a pop. My storage disk thanks Kohya for making it so we are only using the deltas (difference) instead.

This is a common technique used in many modern mixes to influence the result, meaning you can basically make a checkpoint with a specific style or traits with a bit of normal training, much cheaper (in compute/power bill/hardware terms) and faster than a finetune and still gives nice results.

## Getting started

### What do I need to get started?

- You'll need to have installed the [Kohya scripts](https://github.com/kohya-ss/sd-scripts#windows-installation), from 10 to 50 images for a character, 100-4000 for styles or 50-2000 for concepts.
    - Alternatively, specially if on Windows, use [kohya_ss](https://github.com/bmaltais/kohya_ss#installation) by bmaltais. It has an interface so you don't need the scripts, just tweak the knobs.
        - This is a pretty good UI, and synchronizes with the Kohya scripts fast enough, I can trust this.
- You will need a video card with at least 6GB of VRAM, preferably nVidia for CUDA, or use an online compute service like [Google Colab](https://colab.research.google.com/github/Linaqruf/kohya-trainer/blob/main/kohya-LoRA-dreambooth.ipynb#scrollTo=wmnsZwClN1XL). (I'm not the author of this Colab, it was just recommended.).
- You'll also need a base model to train from. As of right now, the best ones to train from are the NovelAI leaked model for anything drawn (anime, cartoon, etc) and Stable Diffusion 1.5 for realistic subjects. Other checkpoints are also suitable, but they tend to give me worse results unless using that one checkpoint. Refer to [What model to train from?](https://rentry.org/59xed3#what-model-to-train-from) for more details.
- You'll need a text editor. Notepad can work, but I recommend something a bit more programming oriented like [Notepad++](https://notepad-plus-plus.org/), [VSCode](https://code.visualstudio.com/), Sublime Text, Vim, Emacs, or whatever you have.
    - Not necessary if using bmaltais' repository, but you should have a decent text editor anyway!
- Optionally, have an image editor like Photoshop, [Krita](https://krita.org/) (recommended), [GIMP](https://www.gimp.org/), [Paint.NET](https://getpaint.net/) or whatever you have. You may not need it, but it can be useful.
    - If you have to make edits to images, you can afford to be a bit sloppy, you don't need to flex your art skill.
- If not using bmaltais' user interface, grab the scripts [SAMPLE POWERSHELL SCRIPT (WINDOWS)](https://rentry.org/59xed3#sample-powershell-script-windows) or [SAMPLE BASH SCRIPT (LINUX)](https://rentry.org/59xed3#sample-bash-script-linux) and edit them to taste to launch the scripts.
- An interrogator to generate captions if using finetuning. I recommend using [this extension](https://github.com/toshiaki1729/stable-diffusion-webui-dataset-tag-editor) with your webui. It'll allow you to batch-caption images with various settings.
- Patience. If it doesn't work the first time **don't ragequit**, it's likely possible to fix it. And quality takes time.

### Character difficulty

Not all characters are created equal (literally and obviously). Some characters are more elaborate or ornate than others, and this complexity needs to be given consideration.  
After much training, I think characters can be separated in the following categories.

|Category|Description|Ranks|Training type|
|---|---|---|---|
|A|Simple "realistic" female characters without unusual clothing or details.|4-8|Textual inversion, LoRA-LierLa, LyCORIS-LoKR|
|B|Female characters with unusual faces, hairstyles, colors or clothes.|4-16|LoRA-LierLa, LyCORIS-LoKR, LyCORIS-LoHa|
|C|Very elaborate details, extra elements like wings, armor, tails,|8-32|LoRA-LierLa, LyCORIS-LoKR, LyCORIS-LoHa|
|D|Humanoids, furry characters with humanlike features, humanoid pokemon. Realistic humans.|32-64|LoRA-LierLa, LyCORIS-LoHa|
|E|More unusual types, pokemon with chibi proportions but still having two arms and legs.|64|LoRA-LierLa|
|F|Animals, pokemon with more animalistic body plans, dragons, humanoid robots. Humans with ridiculously ornate costumes or armor.|64-128|LoRA-LierLa|
|G|Humanoid mechs like a Gundam or EVA, aliens, demons, humanoids with multiple limbs.|128|LoRA-LierLa|
|H|Non-humanoid robots, monsters, insects, non-cartoony dragons, realistic animals.|128-192|LoRA-LierLa|
|I|Eldritch abominations|192-256?|LoRA-LierLa|

#### Female bias

Most existing checkpoints have a solid bias towards female characters, so male characters tend to be a tiny bit harder to train, consider them the ".5" of the above categories until category <=D or so.

#### Prior training

A thing to keep in mind and which will reduce training time/difficulty is whether the checkpoint has some prior knowledge of the character or not.  
For example, Monika from Doki Doki Literature Club is doable with just prompting in NAI, and still has enough likeness of her in mixes. That means training a Monika model is borderline trivial and can be achieved even with textual inversion or a 300-step LoRA. This is more about removing gacha when generating her standard uniform or so.  
If training robots, a Gundam is obviously more well known than a Gespenst Type-RV, so it already has some knowledge to take advantage of.

Check if your checkpoint (either the one you'll train from or use to generate images) has some knowledge of what you want first, and use the same tags to take advantage of it. Unless you want to ignore the prior knowledge on purpose, then use a different tag.

#### Intended results

Of course, what **you** want to use the model for also influences the training.  
I see a bunch of character models are oriented to just generate the character nude and thus it doesn't need to be accurate. Be mindful of that when uploading models to CivitAI or so, because people may be expecting accuracy that is not there (not everyone downloads or trains stuff for porn, get your mind out of the gutter).  
However, that aside, if that's the **intended result** then all you care about is getting the face right, so you won't need to train very aggressively.  
If you want more accuracy with clothes, hairstyles, facial details, body structure or such, then you will need to train for longer and with more optimized settings and a less lazy training set to ensure variety of poses and accuracy of details.

If you are training something like a pokemon or furry character you are going to think of what you are going to use the model for. If you want to make the critter humanoid then you want a bit more strategy, less learning rate, less epochs, weighted blocks... but if you want it to remain accurate then you'll need more epochs, more aggressive training rates and so on, so the body plan and details are properly learned and applied.

#### Character difficulty and settings

More complicated characters (Category >=E) will usually make better use of **higher dim/rank**, or either **higher learning rates**, and **more training time**. Lower ranks don't seem to be able to fully wrap its head around complicated body plans, so they either require more aggressive training or time to fit, and the result might not be as good anyway.  
Consider this when using **certain types of LyCORIS**, as options like LoKR **aren't very good at characters in category >=D** because their reduced rank and size cannot hold the necessary "expressive level". They need a lot more time to come out alright.  
A standard LoRA-LierLa at 128 rank is able to hold characters up to category G.

This said, the opposide is true. Using 64 rank for a character of category A or B is an absolute waste of disk space and your own compute resources, use lower rank for lower categories.

#### Vehicles

I haven't tested this intensively, but it seems vehicles would be somewhere between categories C-G, also based on their complexity and level of detail.  
If you are training vehicles you probably want them to be more true-to-life, so you may want to "round up" and err on the side of bigger ranks, but I think it should be fine to use LyCORIS-LoKR to obtain a decently realistic vehicle at rank 64 if enough training time is given, let it slow cook.  
Of course, keep in mind the intended results policy. If you want to turn your ride into anime you may want to dial it down a bit, but for full realism it can be worth giving it the extra space and try for a 128 rank Lora-LierLa. But if you don't want it super detailed and realistic, in that case I'd recommend "rounding down" to 32 and 64 and see how it comes out.

### Starting settings

This is a work in progress, ranges and parameters may change as I train more models.

These are the standard ranges for general training. Every training set has different requisites, but these seem safe enough.

|Category|Images|Net Dim/Rank|Alpha|Unet LR|TE LR|Regularization|Total Steps|Resolution|
|---|---|---|---|---|---|---|---|---|
|Character (good inputs)|35-100|32-96|1-rank|0.0001|0.00005|No|1000+|512-768|
|Character (bad inputs)|15-30|32-64|1-rank|0.0001|0.000045|Yes|1600+|512-768|
|Style|100-10000+|96-192|1 to (rank/2) torank|0.0001|0.00004|No|~3000+|576-768|
|Concept|50-2000|8(!)-128|1 to (rank/2) to rank|0.0001|0.000045|TBD|TBD|512-768|
|⭐My current settings (characters)|50-100|64|64|Adaptive|Adaptive|Either|~1000|512-576|

Total steps depend on options, number and quality of images, and so on, but you usually want something above 1000 for things to stick.

- Higher ranks will help with more "unusual" characters and if your image count is massive (10000+), but otherwise will offer diminishing returns after a point.
- Alpha should never be higher than rank.
- Refer to [Number of steps/epochs](https://rentry.org/59xed3#number-of-stepsepochs) for details about steps.

There used to be advice about doing more repeats than epochs, but seems that doesn't hold true anymore, so do epochs unless you are balancing multiple subjects or concepts at once so the numbers match by using repetitions, otherwise just do 1 repeat and enough epochs to reach about 1000 steps.

**Run the script once and take note of the total steps it'll perform** to have an exact number to work with.

**It's a good idea to divide them in at least some epochs so it can save snapshots**, that you can use to track progress or debug with. I save mine every 4 epochs.

#### Optimal settings

There are no optimal numbers you can just punch into the training scripts to get good results.  
You can get good results with the defaults, or get disastrous results with the defaults. You won't really know until you try.  
A _perfect_ model will require a bunch of tries, troubleshooting and patience. All is based on the complexity of the subject, how clear it is to the AI, how properly tagged it is, and so on. It also depends on your personal standards, of course.  
Nowadays, adaptive optimizers make it a lot easier to keep a consistent set of settings all across, but you still want to adjust a few settings if the first try is not great, namely epochs, rank/alpha and maybe resolution, but most issues will be the training set's fault using those, removing a lot of guesswork.

The settings in the next section have served me well.

#### The "Easy settings" ⭐⭐

After many tries and experiments I have gotten used to using DAdaptAdam as the simplest, easiest way to get a model going.  
I've gotten good results with and without tagging, 1000 total steps on average and about 50-100 images. Works every time and for every character I've thrown at it.  
I've had reports of cases where it didn't work because the training set was rough or the AI stubbornly refusing to learn, but it's been consistent for me.

|Setting|Value|
|---|---|
|Optimizer|DAdaptAdam|
|Learn rate (Unet)|1.0|
|Learn rate (TE)|1.0|
|Total steps|Around 1000, adjust epochs to fit your source images|
|scheduler|Constant|
|Alpha|1|
|Net dim (Rank)|64 (32 will be fine for characters and concepts too)|
|Resolution|512 (576 is also fine)|
|Bucket size|min:320, max:768-1024|
|min_snr_gamma|5|
|Max token length|225|
|Optional|--flip-aug|
|optimizer_args|--optimizer_args "decouple=True" "weight_decay=0.01" "betas=0.9,0.999"|

The same settings but with `Prodigy` (just change the optimizer args for it) have also been giving really good results as well. Prodigy seems more future-proof so I may switch to it entirely.

Everything I've trained since I discovered this combination of options has come out pretty good. Some rare cases where it needed 2 epochs (200 steps) more or less, but otherwise pretty excellent. With these settings you can be sure your model will come out _alright_ as long as the input images aren't terrible.

I also accidentally **trained an style** with this setup and it..._worked surprisingly well_. So yeah, it's not just for characters.  
It works fine for dreambooth style (keyword only) and finetune style (with tags), so if you want a LoRA made with minimum effort, this is the ticket.

### What model to train from?

"training from" because you are resuming training from a model, also known as a "checkpoint".

**Short answer**: NAI for anything 2D (anime, cartoon, sketches,etc), and SD1.5 for realism/misc.  
Usually, you want to train from a model with a lot of "shared ancestry". For example most known mixes contain or are derived from NAI, so training a model from NAI makes it compatible with all of them.  
But if you go too far, it could be affected by "mixing dementia", so if you train 2D in SD1.5, it might come out poor in mixes.

- You can train from mixes, but the effects are hard to predict when generating with different models.
- The tagging has to be compatible (don't use NAI tags with models trained on e6 or Waifu Diffusion tags etc, they'll "point to the wrong places" and cause who knows what).
    - Happy accidents happen, but avoid unless you are being experimental on purpose.  
        There are newer options like AnyLoRA or such that you can use as well. Personal preference is in effect here, but I still recommend NAI as gold standard. I could never get my models to come out as good with AnyLoRA, even if they are technically functional.

#### Legal concerns over NAI

If your concerns are more on the moral side, then use SD1.5 or SDXL to train (once fully available), it won't look as good but it'll work to some extent. Honestly, if it troubles you too much, I'd just subscribe or send an anonymous donation to NovelAI, since the damage is already done. You might as well compensate them in some way and everyone wins.  
If your concerns are more on the monetization and copyright side, you'll have to ask a lawyer, but the entire thing looks grim if you ask me, I wouldn't plan any commercial escapade around this.  
Personally, for me this is all in good fun.

#### AnyLoRA

AnyLoRA is a new checkpoint designed to train from.  
Honestly, I've tried it a few times and the results tend to come out worse, but they are still recognizable and not "broken". There are **some cases where it does come fine**, so I recommend trying both and pick the one that looks the best in the most checkpoints you try ([you are trying your models with more than one checkpoint, aren't you?](https://rentry.org/59xed3#test-your-model-with-multiple-checkpoints)).  
I personally hold animefinal-full (NAI) as the gold standard for anything 2D, be it anime or cartoon, at least for now (SDXL might change this dynamic).  
Seems AnyLoRA isn't part of many mixes as well, what makes me question its inherent value. If I had to put a language analogy, it'd be like writing an essay in a regional English dialect.

#### The furries keep asking

I keep getting asked about this and was forced to have to experiment, but, yes, in most situations NAI (animefinal-full) will be enough to learn a furry character.

- No, it won't give your character anime eyes **unless you had too few steps** (or the character has animesque eyes to begin with).
- Slightly increasing **resolution** may help with finer details like scales, spikes and whatnot.
- **Pokemon** and similar cartoony animals will work perfectly just with NAI. There are lots of examples already.
- You are making your model **more compatible** with other concepts by using NAI as base.

![Example](https://i.imgur.com/IdmJi0a.png "Example")  
This LoRA was trained with Prodigy, 1200 steps, 90 images, 512 resolution, booru tagged, from NAI (see my settings above, copy my base Prodigy args in the Prodigy section). It was not inpainted (adetailer didn't kick in) or edited in any way besides halving the size to paste here. You can see it has a "sort of humanoid" body plan, so it'll work just fine. It's able to get a decent variety of poses and even properly proportioned clothes, and despite this example having an empty background (I didn't specify any), it can do them fine. Can throw this into AOM3 and generate the character with its characteristic style.

Now, you probably want to use stuff like fluffyrock if you want to:

- Have more realistic-er features and better posing for more unusual body plans (backwards knees or multiple arms)
- Physically accurate nuts and bolts and the combination of such parts for purposes of titilation (the things I have to write...)
- Use author style tags? (this is a thing with furries and AI, but I never quite got the appeal)
- You will only generate images with fluffyrock ignoring all other popular mixes, concept LoRAs and such
- You strictly want e612 tagging and their effects

I personally think using more exotic base models leads to a fragmentation of the ecosystem, so to speak, so I'll advise against it unless it's "the only way©" to get what you want.  
**I admit I haven't tried to generate images of furries bumping uglies (the things i have to write...) so your mileage may vary there.**

## LEARNING RATES

[Grid of Unet/TE strengths 0.1,0.25,0.5,1 and 2](https://i.imgur.com/OFanVlM.jpeg), [Grid of Unet/TE strengths 1.0,1.2,1.4,1.5,1.6,1.8](https://i.imgur.com/dktVoXT.jpg)  
Display of effects of learning rate. This displays this model has just enough Unet training but can use a bit more TE training, Unet 1.0 - TE 1.5 looks accurate but not chibi. That means next training will go better with 1.5 LE rate.

If you can't stand the scientific "e-notation" numbers, Kohya's script admits real numbers as well. Therefore "1e-4" becomes "0.0001" and "5e-5" becomes "0.00005". It's up to taste.

It is recommended to use adaptive optimizers like DAdaptation (DAdaptAdam/DAdaptLion) or Prodigy, AdaFactor (with proper args) will also go adaptive. Those eliminate the guessing work of tweaking the learning rates and make it very difficult to burn the Unet, allowing to train more epochs without risks or tweaks.

In case you cannot use adaptive optimizers, there are two ways to control learning rate.

|Option|Values|Effect|
|---|---|---|
|--learning_rate|0.005-0.0001|Master knob for LR. Sets the values for the other two.|
|--unet_lr|0.0001-0.005|Sets the Unet's LR. Most sensitive part of the model, don't set it too high.|
|--text_encoder_lr|0.00001-0.00005|Sets the text encoder's LR. It's the language processing of the model. Better set much lower than Unet's.|

What does this mean?  
If you don't care, just set `--learning_rate` to set the other two.  
Otherwise, set them individually, since it's redundant to specify `--learning_rate` if you set the other two. I just set it the same as the Unet LR.

Read below to see what each training component does.

### Text encoder learning rate

The text encoder controls how the AI interprets text prompts when generating, and associates things to "neurons" when training.

The documentation for the Kohya scripts suggest using `5e-5` for it. If none is specified, it'll use the value of `--learning_rate`.  
Testing models with exact same training set and only changing this option, on the same seed, it seems to separate details better.

- Lowering LE learning rate seems to have benefits in separating objects. If you get unwanted objects in your generations, you may want to lower it.
- If you have difficulty causing things to appear without weighting the prompt a lot, **you lowered it too much**.

The TE is what links the tags or tokens to the data in the Unet. Of course, more definition of things means more control in your prompt.  
The Unet itself can however learn how to put things together even without tag guidance, but training the TE well will allow you more granularity of features. In other words, more prompt control.

### Unet learning rate

The Unet serves as a rough equivalent of visual memory. It also seems to have some information about how elements it learns relates to each other and their position in a structure.  
The Unet is very easy to overcook, so if things look wrong, it's likely to be over or undercooked. The margin for it coming right is narrow, but the "good zone" varies from set to set, it's hard to determine.  
Check out the troubleshooting section for advice if your generations look funky.

The standard value is `1e-4`. Normally you don't want to touch Unet values unless you know what you are doing or:

- If your model seems overfit, it might have trained the Unet too aggressively, you can solve this with less learning rate or less steps, or decreasing alpha or using other dampeners.
- If your model outputs pure blobs of visual noise (not "slightly blobby", I mean literally incomprehensible masses of nothing in particular) you set it way too high. Divide it by at least 8, you probably missed a zero or something.
- If your models seems too weak, cannot replicate fine details or so, it might be too low or require more steps.

The Unet is, arguably, the most intricate part of the whole process. It contains the _planning_ of the images as well as information about color and texture.  
Think of it as some sort progressive detailing thing. First you get a planet, inside the planet there are continents, the countries, then states or provinces, then cities, then streets and so on. It starts with something that can be described as a "blurry silhouette" (think the things you see during at the start of previews when generating) and it starts adding more and more detail as it goes "forward". For a person it'd be a general base of a pose and then it starts "zooming in" until it becomes pixels. This is why lower resolutions make some details wobbly, it has more room to work with the more pixels you ask for. That's why hires. fix or inpainting faces makes them better.

Note that this is a "visual" simplification, as the entire thing is a soup of math with probability croutons and doesn't contain images in the strict sense of the word.

The Unet is composed of multiple blocks, which associate to the level of detail in ways. IN blocks determine the planning, and OUT blocks the fine detail like texture.

So, burning the Unet means it'll have issues knowing where to place things or how to detail them. Like, "_probability of eyes, `0.9`? Sure eyes here! and here! and here too!_" , or all the values get so high that it'll try to place **everything, everywhere** and that's when you end up with results that can only be described as digital chunky salsa.

### Optimizers

Optimizers are pieces of digital sorcery that overview the learning process.

|Optimizer|Required args|Notes|VRAM|
|---|---|---|---|
|AdamW8bit|None|Default. So far, the most well tested.|LOW|
|AdamW|None|Default, but 32 bits. Will use double the VRAM but it's more precise on paper, just slightly better in practice.|MID|
|DAdaptAdam|`--optimizer_args "decouple=True" "weight_decay=0.01" "betas=0.9,0.999"` learning rates between 1.0 and 0.1. `Constant` scheduler is a good default. Best results with alpha 1?|Adjust learning rate on the fly (adaptive). **Requires arguments to work, high quality**. High VRAM usage. (6.0GB Minimum, usable in 6GB cards if nothing else is using VRAM)|HIGH|
|SGDNesterov8bit||Works, low VRAM usage (equivalent to AdamW8bit). Extremely slow learning, 2000 steps nowhere near enough. Not really more "optimized" since it'll require much more time. Needs more testing.|LOW|
|SGDNesterov||Same issues as SGDNesterov8bit, but at higher precision like AdamW.|MID|
|AdaFactor|`--optimizer_args "relative_step=True" "scale_parameter=True" "warmup_init=True"` for adaptive (default)|Overrides scheduler. Results similar to Nesterov, but it's adaptive and its VRAM usage is very low, could be useful to experiment further. Seems much better than DAdaptation.|LOW!|
|Lion|None|Not bad but can give out very strange results. Bit heavier due to being higher precision.|MID-HIGH|
|Lion8bit|None?|New 8-bit variant of Lion. Might make it more viable for low-VRAM setups.|TBD|
|Prodigy|`--optimizer_args "decouple=True" "weight_decay=0.01" "d_coef=2" "use_bias_correction=True" "safeguard_warmup=True"`, d_coef might need adjustment for different types of LoRA|Direct upgrade to `DAdaptation`, viable for SDXL and LyCORIS as well as regular LoRA. Good results.|HIGH|

Optimizers give the training their own set of rules and can simplify guesswork or use less resources, or more resources but for a better result.  
While they cannot possibly turn a bad training set into something usable, they can help, well, optimize the process. Some do a better job than others, so it's worth trying a few.  
Right now, the gold standard are _adaptive_ optimizers, as those will automatically adjust learning rates based on loss, every _backpropagation_ (when the training commits changes to the math soup that is the model), balancing the learning rates.  
While they are technically more intricate, just setting the right optimizer args in the table will suffice and then you only need to worry about your images and tags.  
Right now, DAdaptAdam, DAdaptLion and Prodigy are the recommended optimizers, because of removing all the guesswork and avoiding burning things.  
Prodigy is reported to work in SDXL, so it's good to familiarize oneself with it.

#### Lion

`Lion` gave me very strange results, like a model with a white-haired character giving a rainbow-colored mess for its hair, even when every other optimizer gets that right. But some people swear by it, so maybe there's more to it. It does _add its own unique flavor to models_, but I cannot quite explain why yet.  
Seems to learn fairly fast and can come in handy for some cases. It's worth trying to see how it comes out.

#### AdaFactor

`AdaFactor` on the other hand did output results that weren't broken, but the training seemed really weak and might require a bit more time.  
Makes me wonder if it might be **more suitable for style or concept learning** due to their smaller impact on the output, but I haven't tested it yet.  
I hear reports of it being rather slow per step.  
TODO: Try it further.

#### DAdaptation ⭐

DAdaptation needs specific arguments to work. Scheduler must be set to `constant` and it requires `--optimizer_args "decouple=True" "weight_decay=0.01" "betas=0.9,0.999"`.

DAdaptation seems to have difficulty taking the Unet/TE learning rates separately. Seems **it's best to leave both at 1.0**, despite talk of having them at unet=1.0 and te=0.5, and let it sort things out.

**202306**: DAdaptation needs to be installed separately now. `pip install -U dadaptation` with **the virtual env active** will sort it out.

DAdaptation has been renamed to DAdaptAdam for use. Keep it in mind.

DAdaptation is an _adaptive_ optimizer, it will adapt training values on the fly, saving you the need to control it yourself. It will generally give very good results for minimum effort, as long as the training set is not faulty (but that's true for everything in training). At this moment in time, I consider it the **best available optimizer**.

Big caveat, though. DAdaptation is pretty heavy. **It uses 6.1GB of VRAM at batch size 1 (512x512), so 6GB VRAM users cannot use it**, unfortunately. AdaFactor could be an alternative in that case.

Due to the non-determinism of the optimizer, it's difficult to reliably gauge Alpha effects, take this with a grain of salt.

I tried training DAdaptation with various Alpha settings. Seems Alpha 1 gives the best results. Alpha 64 (with rank 128) was fine too.  
Alpha 0 (= Net Dim) gave pretty bad results in comparison. Until I have more accurate numbers, **I would recommend keeping Alpha between 1 and half of net dim/rank**. (So if net dim is 128, from 1-64. If net dim is 32, from 1-16).

Other options:

- Noise offset up to ~0.1 seems to not disturb things.
- Flip augmentation is also fine, but the same issues with asymmetric character designs apply.

#### Prodigy

Prodigy needs to be installed separately now. `pip install -U prodigyopt` with **the virtual env active** will get it. **Not necessary with kohya-ss, it'll do it itself**

Use the following optimizer args for it to work: `--optimizer_args "decouple=True" "weight_decay=0.01" "d_coef=2" "use_bias_correction=True" "safeguard_warmup=False" "betas=0.9,0.999"`

Prodigy seems to be a direct upgrade to DAdaptation and shares a lot of superficial attributes. Seems to be done by the same team so it can be considered its successor.

Like DAdaptation, it's _adaptive_ and adjusts learning as it goes. Seems the adjusting is more regular (**use more epochs than repeats**!) and accurate.  
Prodigy also can be used for **SDXL LoRA training and LyCORIS training**, and I read that it has good success rate at it.

I have only tested it a bit, but the results, with the same exact parameters and training set as a successful DAdaptAdam LoRA, came out noticeably even _better_. The particular test used a difficult subject to learn, which makes it more notorious in my eyes. I was already a big fan of DAdaptation, so a direct upgrade is a big deal!

All attributes and caveats of DAdaptation are present in Prodigy as well. VRAM usage and speed are about the same, and setup is very similar, only having to make a few changes to the optimizer args (see second warning in this section or table above.)  
For regular LoRA training, if you use my settings for DAdaptation, the same number of steps and epochs will be fine for Prodigy. Just change the optimizer type, the optimizer_args and you are good to go.

#### d

`d` is the value Prodigy uses as dynamic learning rate. When looking at tensorflow you'll see it represented as a `lr/d*lr` chart.

#### d_coef

Ranges: 0.5-10 (Recommended 2)  
The dynamic learning rate coefficient. It will multiply the value of `d`, the dynamic learning rate used by Prodigy. This is the simplest way to scale up the learning rate if determined to be too low or using **lower rank**. You can also increase the values of Unet/TE Learning Rate to 2 or so, but this seems to be more stable than that.  
The **recommended values are between 0.5 and 2**, but in at very low ranks (LyCORIS-LoKR, LyCORIS-(IA)^3, LoRA-LierLa rank <= 8) you may raise up to 10. Above that it will become too much and it's reported to be no good, which seems to align with my own experiments.  
For LyCORIS-(IA)^3, it's recommended to up to 8-10, since it requires a mammoth learning rate.

#### Schedulers

Prodigy will work fine with a `constant` scheduler. Since it's using the value of `d`, it'll raise or lower it accordingly. Other safeguards such as `scale_weight_norms` will prevent any potential burning ups.  
Prodigy seems to work fine with `constant_with_warmup` scheduler, but requires more steps. At about 10(%) warmup, it may require an extra epoch or two to compensate. If using warmup, it's recommended to enable `safeguard_warmup=True`.  
Then `cosine` and `cosine with restarts` will also adapt the learning rates accordingly, but I feel it's rarely necessary.

#### Min. SNR Gamma

The effects of min_snr_gamma seem a bit more interesting when using Prodigy, it seems to become a sort of multiplicative scale for the dynamic learning rate.  
Lower values will have lower loss (and therefore learn more aggressively), while higher values have higher loss (less resemblance to training set).  
What does this mean? **min_snr_gamma <= 5 makes it more suitable for character learning**. Based on the [Character Difficulty](https://rentry.org/59xed3) chart, it'll help out with characters on the higher (C-E) categories, as those require more aggressive training and may help you cram a more complicated character in a LyCORIS-LoKR or use ranks <=16 in a LoRA-LierLa. A value of 1 seemed quite strong.  
On the other hand, **min_snr_gamma >= 5 will dampen learning** and thus allow for that low-temperature baking **that benefits styles and concepts**.

### Scheduler

To be completed.

As of right now, `cosine_with_restarts` seems to be the most effective of all the schedulers. We can consider it a default.  
The scheduler causes alterations to the learning rate with a given pattern. For example `cosine` will make the learning rates oscillate up and down.  
However, there might be edge cases where an alternate scheduler is preferred. For example, if using `DAdaptation` as optimizer, you want to set it to `constant`.

|Scheduler|Effect|
|---|---|
|constant|Learning rates do not change.|
|constant_with_warmup|Like constant, but starts at zero and increases linearly during warmup_steps until reaching the given values.|
|linear|Drops constantly until it's zero at the end.|
|cosine|Learning rates go up and down following a cosine wave form.|
|cosine_with_restarts|Like cosine, but starts from full LR at given intervals.|
|polynomial|Like linear, but with a fancier curve.|

Constant is not recommended unless you are using `AdaFactor`, `DAdaptation` or `Prodigy`, it'll generally overtrain unless set at very low learning rates.  
Constant with warmup is about the same, but it gets a % value of warmup steps where it does from zero to the desired learning rates. Slightly smoother results, but again, only recommended for adaptive optimizers.  
Linear starts strong, can be used to overtrain a bit at the start then smooth the results until palatable.  
Cosine, configured with a decay value equal to, or slightly higher than, the total training steps, is similar to linear but is more gradual, and generally trains a bit more than Linear.  
Cosine with restarts will also decay over a configured time, but then go back to full force and decay again. Training is more aggressive than cosine, since learning rate peaks at more points in training, but it'll also smooth down.  
Polynomial...I still need to try it. It's similar to cosine but the curve tends to go inwards, therefore learning less aggressively.

**TODO: Make a graph!!**

---

## TYPES OF TRAINING

SELECT YOUR STYLE.  
We got Finetunes, dreambooth and keyworded. Trickster and Royal Guard may be coming someday.

### "Finetune style" (Default)

Like finetuning a model, it uses _caption files_, small .txt files matching the name of each of your images. Those captions instruct the training to look for something, and trains both the Unet and the text encoder.  
Captions are composed of either a bunch of _prose_ describing the image ("Laetitia walking on a flower field") or a collection of _tags_ ("Laetitia, 1girl, solo, flower field").  
If you find the captioning process a hassle, or **you want to train an artist style** without bothering, scroll down to the "Keyword Dreambooth" section.

#### Multiple concept support

![Laetitia in a crude Hitachi Seaside Park (It's a place in Japan)](https://i.imgur.com/Z2YvuAZ.png "Laetitia in a crude Hitachi Seaside Park (It's a place in Japan)")Training multiple concepts in a single LORA, despite their more focused usage, is still possible. The image example uses the character of [Laetitia](https://lobotomycorp.fandom.com/wiki/Laetitia) in [Hitachi Seaside Park](https://en.wikipedia.org/wiki/Hitachi_Seaside_Park#/media/File:Baby_blue-eyes,Nemophila,Hitachinaka-city,Japan.jpg), both baked into the same model.  
You can train backgrounds, more than one character, items related to that character...anything goes, but it needs tagging and some logical balance, some common sense applies:

- Don't put more backgrounds than characters as it tends to give you empty backgrounds.
- If training more than one character, make sure the amount of total images for each character are roughly the same or one will take over.  
    I was able to replicate the "feel" of some good backgrounds with just one or two images (x10 repeats/epoch).

### "Dreambooth style"

The name strikes me as odd, I always thought the basic form of dreambooth was "keyword activation AND regularization" with the finetuned hybrids coming out later.

Do NOT train styles dreambooth style. It seems to heavily discard style, use it for _characters_.

Training your LORA **with regularization images** is described in the documentation as "dreambooth style" setup.  
This method changes the rules and resembles dreambooth training results a lot more. By using it, you'll _forfeit most of the style_ of your character but the AI will still somehow figure out the details. You will need to **double the amount of steps** for it to work.  
In exchange, there are a number of benefits:

- Seem to separate details from style a lot better.
- Seem to soak "active" style much better (either from the model in use when generating or style addons).
- Is very able to turn stuff like chibi characters into something more normal consistently.  
    Read the [REGULARIZATION IMAGES](https://rentry.org/59xed3#regularization-images) section for more information on how to set them up.

#### When to use "finetune" or "dreambooth style" training

From my experiments seems you want dreambooth style when your _training image set is bad or has a style or quirks you don't exactly want passed into image gen_ (like training a character on scribbles or chibis or such), and regular LORA finetuning when you do want the style and quirks of the training images to have more presence.  
If you are very constrained with your training images it seems to always be worth it.

### "Keyword style"

Okay I finally settled into a descriptive enough name. This otherwise unnamed variation doesn't require tagging and uses a "sks" type of **activation word** (or "class name"), although it's not always necessary, making it suitable for styles, as it'll alter the Unet regardless.  
This variant **does not require regularization images**, making it fairly simple to use, but keep reading for caveats.

To set it up, do not tag your images (or remove any .txt) files with tags, and set your folder names like `<repetitions>_<activation word>`. When the scripts don't find any tag files, the folder name will be used.  
The activation word can be anything you wish (even with spaces), but short, rarely tokens such as "sks" will be _slightly more efficient_.

Once trained, you can use the activation word in your prompt, but keep in mind that **the Unet will be changed by the training** therefore visual style will always carry to some extent, _even when the activation word is not used_.

For models trained this way you will need **better prompts**, since there's no guidance from the Text Encoder, expect to use higher heights and more negatives to remove rogue elements. At times the TE will not be able to recognize some unusual features because of this.

Despite the caveats, **this is a perfectly valid method for characters, styles and concepts**, and it requires skipping a lot of tedious work with tagging. It is also capable of handling more unusual subjects like robots or pokemon, that would be difficult to properly tag in a sensible way. But it's very random whether it'll stay on model or become a humanoid version of it.

**20230701**: The quality of this type of training is also boosted by adaptive optimizers, making it very simple to get a style or character trained without tweaking the settings!

### Resuming training

`--network_weights=<PATH TO EXISTING LORA>` lets you continue training from there.  
This can be done with any model, as long as you know the **rank** to set it to the same value. There's an option to guess in kohya_ss, but I'd rather check manually.  
Once the rank matches, the rest is up to you. You could just give an undercooked model some more time to finish up, do a pass with lower or decreasing learning rates to polish it, change the training set, use some old model you downloaded as a base`*`, etc. There are multiple ways to experiment.  
Of course, the result will be a new model and the original will be kept intact.

- If you have a model that is almost there or undercooked you can just add a few more epochs to finish it up.

**If using adaptive optimizers** the first ~50-200 steps will be warming up at low learning rates, so take that time into consideration.

- Resuming training can be a good idea if using Colabs so you can train it in stages and always keep some progress.
- If you enabled saving snapshots during training, and find out one of the snapshots is better, you can use that as a base instead of the final product, and change some settings to see if it improves further.
- A couple hundred steps at a very low learning rate can be good to "round" some of the weights, which can potentially improve details or slightly reduce overfitting a bit, but it doesn't always work. (A model can be way too far gone to fix).
- You can change the dataset in the middle to, for example, train first with very general images and then the highest quality ones. Or any sort of combination in that fashion.
- You can also stage various training phases at different learning rates or settings. If you know what you are doing you can combine multiple techniques to optimize a working training set.

`*`: If you publish a model trained from another model by another person, obviously be considerate and give credit if possible. Even if you did more actual work. Some humility goes a long way and saves you from potential drama.

### LyCORIS (LoHA/LoCon/Etc)

Using LyCORIS models requires, at the time of writing, a separate extension in sd-webui. Install [LyCORIS](https://github.com/KohakuBlueleaf/LyCORIS) by **KohakuBlueleaf** to use them. Keep in mind they have to be put in their own LyCORIS folder. There's an older LoCon extension, but **It's been replaced by the LyCORIS** extension, so remove it to avoid conflicts.

I'll leave the warning for users of webui that haven't updated, but since it's now integrated with sd-webui, you **won't need an extension** to use LyCORIS anymore and they just go in the same folder as your regular LoRAs. Sweet.

LyCORIS needs to be added to the Kohya scripts as a separate package. Use `pip install -U lycoris_lora` with **the virtual env activated** to sort it out. You might also need `pip install -U open_clip_torch` if it fails at launch.

LyCORIS is a group of optimizations and experimental methods for training. It is composed of a number of different ways to train and characterized by lower rank requirements and smaller sizes.

|Name|Acronym|Args|Observations|Caveats|
|---|---|---|---|---|
|Conventional LoRA|LoCon|locon|||
|LoRA with Hadamard Product Representation|LoHa|loha||Excessive VRAM use and training time. Not suitable for 6GB cards, 8GB ones may struggle and can't train at higher rank.|
|LoRA with Kronecker Product|LoKR|lokr|Very TINY output files (2.5MB rank 64).|Can't handle complex characters without lots of adjustments, finicky, dampened.|
|(IA)^3|?|ia3|Requires massive learning rates to work (8-10x the usual).|Not portable well across models, train on model intended to use with.|
|Dynamic Search-free LoRA|DyLoRA|dylora|Finds rank on its own.|Very slow, ridiculously high dampening.|
||||||

You should in theory **require less steps (therefore less time) to properly train a model** but in my experience it seems to be requiring a lot more steps on average. Keep in mind my settings usually only take 100 images and 1000-1400 steps for a LoRA-LierLa, where a character LyCORIS may require at least twice as much time despite being advertised as better for characters. Learns very weakly.

#### Pros

- Cram a lot of training data in a tiny file, making them good for building libraries of stuff without using a ton of disk space.
- Works well for styles and concepts.
- Good for training elements like weapons or accessories, and backgrounds.
- You train _every_ block of the Unet (LoRA-LierLa, the standard flavor, gives 16 blocks)
- Now that it's fully integrated in sd-webui, they can use used interchangeably in the same folder.
- Better at handling huge datasets.

#### Cons

- Quality of the output is not inherently **better**. A well-trained LoRA and a well-trained Lyco are about the same level of quality.
- LoHA is really slow and uses a lot of VRAM to train. (AI)^3 is experimental. DyLoRA is nice for resizing and stuff, but doesn't offer real quality advantages and uses way too many steps. Optimal settings may require 10GB of VRAM or more, definitely not for 6GB and 8GB might not fit either.
- Takes more time per iteration, even more training steps. Takes longer the lower the rank is.
- Seriously dampened learning that makes `Prodigy` look like `Nesterov`.
- Ideal settings can make BIGGER files than using regular LoRA-LierLa.
- It's definitely worse for characters despite claims to be good for them. Can only handle anime waifus and simple things well.

Sadly, **since characters are my main focus, I cannot recommend moving to LyCORIS for them**. It's much slower and uses more resources than a regular LoRA-LierLa that you can cheat your way around with `Prodigy` and rank 64 in 800-1400 steps, under 30 minutes of compute time. They are suitable, however, for characters that work at lower ranks, but being slower and using more VRAM negates most of the advantages.

Having more Unet blocks _should_ make the result better, but I can hardly see a difference in practice.

#### LyCORIS-LoCon

LyCORIS-LoCon is the oldest and considered good for styles. If used for characters it'll also carry style more aggressively than other options. This makes the resulting model a bit more rigid. It's is however the oldest of the methods in LyCORIS and not likely to be improved/optimized later.

#### LyCORIS-LoHA

LyCORIS-LoHA is usable for characters, but it becomes less effective the more complex the character is, as it cannot pack as much rank without it going bananas, burning up the components and possibly causing NaN errors at inference time.  
The lower ranks make it slower and may require higher learning rates. Higher ranks require more than 8GB of VRAM, so I cannot test them properly.

#### LyCORIS-LoKR

LyCORIS-LoKR is suitable for simpler characters and outputs really tiny (2.5MB) files. If according to this table your character is within A-C, it can be good to use a LoKR to get the smallest possible file. However, it's described in the LyCORIS repo to be tied to the model it was trained from, making it less portable across models and will lose effect with mixes.  
Since the "expressive power" is low, it's not suitable for complex characters that would work in a LoRA-LierLa at 64 rank or higher, even at rank 64 and conv_dim 64 it's still a very slow learner and takes more real clock time, and if you go too aggressively to use less steps it has risk of overfitting in a not-quite-there odd way.  
You can alter the _LoKR Factor_ setting to scale the size of the network accordingly, and at 2 it'll have equivalent learning capabilities to a LoRA-LierLa, but that creates **files bigger than a regular LoRA-LierLa** (LoKR ends up 2MB bigger). Which I feel defeats the purpose since quality is not really improved.  
**Very finicky with learn rates.**

#### LyCORIS-(IA)^3

LyCORIS-(IA)^3 requires massive learning rates, it's recommended to use a `cosine` or `linear` schedule or an adaptive optimizer (`Prodigy` with high `d_coef` (8-10), for example) and set it so it overtrains the first few steps and smooths out the weights for the rest of the run. However, like LoKR, it's also highly tied to the model it's trained from, and is explicity indicated in the LyCORIS repository that it doesn't transfer well to other models.  
Works for its niche, but it's too limited.

#### Conclusion (character-oriented)

Some call LyCORIS a meme format and after a whole weekend of experiments I'm inclined to agree.  
While it's possible to get pretty good LoCons and some LoHas or LoKRs, the extra time or resource usage lowers its attractiveness.  
**Use them for styles and concepts, that's where it shines.**  
Unless your character is very simple and you want very small file sizes, or you have lots of images to work with, it usually requires more time and resources to get right compared to an equivalent LoRA-LierLa, and at times the result ends up being a bigger file, which negates some of the theoretical advantages.  
Generally speaking I cannot recommend it unless you know what you are doing to adapt to its idiosyncracies.

### SDXL

If caching TE, _caption dropout rate_, _shuffle caption_, _token warmup step_ and _caption tag dropout rate_ cannot be used (yet?).

- Training using bf16 is recommended, but fp16 can also be used. ("full fp16 training" can make `Prodigy` mess the value of `d`, though, so don't use it)
- Most existing knowledge seems to apply directly, just at higher resolutions/memory use.
    - Keep in mind checkpoints and mixings are still in their infancy and might not give results as good as SD1.5 even if trained right.
    - Otherwise, other than possibly needing some more steps, training is very similar to SD1.5 in most regards, apparently.
- Every dim/rank "unit" contains more information. Seems to be roughly 3-4x times more effective, so a XL rank 16 may fit a similar amount of learning as a 1.5 rank 64, but doesn't seem to be an exact translation. Play around with values like 16, 24 or 32 to fit a character that worked well at 64 in SD1.5.
- There seem to be some limitations about training the text encoder. At the moment training will not start if learning rate for TE is not equal to zero.
- Training with 8GB is possible, but my system with 8GB of VRAM and 32GB of RAM is left with few resources in the meantime.
- Training times are about four times longer than SD1.x, give or take (depends on your video card model).
- Prodigy works well. I hear AdaFactor and AdamW do the job well too. (I need more AdaFactor testing)
- Training on SDXL 1.0 and using an anime model to generate gave better results than generating from the same anime model and I cannot explain why.

#### Be careful

Note that anime and realistic finetunes of SDXL are still in its infancy. You may have trained the subject well and it might have a funky face because the models aren't quite as flexible as SD1.5 mixes.

### Weighted training

There is a feature allowing you to train specific sections of the Unet.

#### The Unet and its blocks

The Unet of a model is composed of three sections (IN, MID, OUT) divided in multiple _blocks_. Each block is used, in order, from IN00 to IN11, M00 and then OUT00 to OUT11.

|Type|Blocks|Effect|
|---|---|---|
|IN|IN00, IN01, IN02, IN03, IN04, IN05, IN06, IN07, IN08, IN09, IN10, IN11|Composition, silhouette, body planning, posture|
|MID|M00|Middle ground, more effects to determine|
|OUT|OUT00, OUT01, OUT02, OUT03, OUT04, OUT05, OUT06, OUT07, OUT08, OUT09, OUT10, OUT11|Color, shadows, texture, details|

Seems some of the layers also affect specific parts of the output. For example layers **OUT04+OUT05+OUT06** seem to have bigger influence on _eyes and face_ than on bodies, for example.

#### LoRA blocks

LoRAs have a smaller amount of blocks, which are "sandwiched" with the checkpoint's Unet in memory.

|Type|Blocks|
|---|---|
|IN|IN01, IN02, IN04, IN05, IN07, IN08|
|MID|M00|
|OUT|OUT03, OUT04, OUT05, OUT06, OUT07, OUT08, OUT09, OUT10, OUT11|
|#### LyCORIS blocks||
|LyCORIS, on the other hand, has the same amount of blocks as a checkpoint and is mixed in memory instead of "sandwiched".||
|#### Why it matters||
|Knowing this, **style LoRAs can probably benefit heavily from training the OUT layers** more than the IN blocks, and **concepts can benefit from training IN blocks more than OUT blocks** (although depends on the concept, "posture only" ones can probably take this literally).||

Similarly, this can be used to obtain "special effects" of sorts. Training a character only in the OUT blocks will "skin" a regular human figure into that character, discarding the body plan but keeping a large amount of details and colors.  
You could for example train a model, OUT only, with images of robots, and then generate images of armored knights. Instant power armors!

This can also un-chibify characters or make a something like a pokemon more humanoid, but some experimentation is needed before committing, read below.

#### Testing weights before training

I recommend experimenting with the [sd-webui-lora-block-weight](https://github.com/hako-mikan/sd-webui-lora-block-weight) by Hako-mikan.  
You need to have trained a model first, with all blocks.  
This extension allows to dynamically change the weights of LoRAs for a generation. If you trained a concept and find it gives better result with less weight on the OUT blocks, you probably want to train it with the same weights so it doesn't change style dramatically, allowing it to be more mixable.  
I recommend creating a few _Presets_ for easier testing.  

|   |   |
|---|---|
|[1](https://rentry.org/59xed3#L-5-1)<br>[2](https://rentry.org/59xed3#L-5-2)|OUTX:X,X,X,X,X,X,X,X,1,1,1,1,1,1,1,1,1<br>INX :1,1,1,1,1,1,1,1,X,X,X,X,X,X,X,X,X|

I named them "backwards" because they are used to test the OUT or IN blocks **without the other blocks**, so change name at your discretion!

To use them, load your lora like

- On webui 1.5.0 or superior: `<lora:mylora:1:1:lwb=OUTX:x=0.5>` or `<lora:mylora:1:1:lwb=INX:x=0.5>`
- On previous versions: `<lora:mylora:1:OUTX:0.5>`, etc.  
    This is to accomodate the new ability to set the text encoder's weight.  
    For reference, the values go as follows:  
    `<lora:mylora:A:B:lwb=C¹:x=C²>` where A is global strength, if B is not present. If B is present, A is Unet strength and B is TE strength.  
    C¹(lwb) is the Preset you want to use.  
    C²(x) is the strength given to blocks marked as `X`, this allows you to test variations quickly.  
    You can, of course, make your own presets testing more specific blocks.

For example, if you are training a style, and find out the sweet spot is with IN blocks at 0.2 and OUT blocks at 1.0, that's the same weights you'll use to train with.

##### LyCORIS

The list for LyCORIS is similar but longer.  

|   |   |
|---|---|
|[1](https://rentry.org/59xed3#L-6-1)<br>[2](https://rentry.org/59xed3#L-6-2)|LOUTX: X,X,X,X,X,X,X,X,X,X,X,X ,X, 1,1,1,1,1,1,1,1,1,1,1,1<br>LINX : 1,1,1,1,1,1,1,1,1,1,1,1, 1, X,X,X,X,X,X,X,X,X,X,X,X|

Same principles apply otherwise.

#### Setting up

I'll post the exact methods to train specific blocks soon.

---

## PREPARING IMAGES

Valid formats and extensions are `png`, `jpg`/`jpeg`,`webp` and `bmp`. They must be lowercase in Linux or they will be ignored.

If you got incorrect images there (GIF, etc), the script will ignore them and continue. This **can cause your training to go for more steps or whole epochs than intended and may cause the model to come out weird**. When the script starts make sure the number of images and steps matches what you want.

Organize your images as follows:  

|   |   |
|---|---|
|[1](https://rentry.org/59xed3#L-7-1)<br>[2](https://rentry.org/59xed3#L-7-2)<br>[3](https://rentry.org/59xed3#L-7-3)<br>[4](https://rentry.org/59xed3#L-7-4)<br>[5](https://rentry.org/59xed3#L-7-5)<br>[6](https://rentry.org/59xed3#L-7-6)<br>[7](https://rentry.org/59xed3#L-7-7)<br>[8](https://rentry.org/59xed3#L-7-8)|Your training set folder (point the Kohya script for this folder)<br>+ X_Concept1<br>    + image.jpg    + image.txt<br>+ Y_Concept2<br>    + image.png    + image.txt<br>+ reg (leave empty)|

### Selecting images

You want images where your subject is clearly represented.  
Avoid images where:

- The character is not represented accurately. (wrong hair color/style, wrong details...)
- The character is being partially covered by something else.
- The style or pose are strange or low quality.
- There are faces or hands of other characters near the borders of the image. It'll somehow bias the output model to put stuff at the edges just with one or two! Edit random people out.
- Blurry images (low resolution captures, screenshots or photos)

Images with these flaws will _confuse the model_ and it'll make similar failures. **Avoid them unless you have no other options!**

You do want images where:

- The art is accurate to the character's design.
- Close-ups of the head. If you have large images it's never a bad idea to pick one with a good face and try to fit it in the training resolution (512x512 by default).
- Close-ups of the eyes if the design is unusual.  
    You may also want closeups of certain details. If you **notice the AI is not giving a specific part enough definition, then a full-resolution image of that part might help**. This could be useful for intricate decorations, accessories, unusual eye designs and so on. Will make them less scribbly.

You also want some variety, but _try to preserve character accuracy_.

Most problems with a model's results are usually caused by improper tagging or too much/little baking, images don't tend to cause as many issues by themselves, and are easier to spot. It's obvious when a certain image is causing issues because something similar to it pops out in generations and it's basically poisoning the Unet with suckiness.  
You will only be able to notice them **after** you trained, it's impossible to predict how the AI processes them otherwise.

### The short version

If you aren't super picky about details, just grab 30-100 images of decent quality and go wild. **That'll usually work.**  
If you don't have that luxury, refer to the [Rare character/OC HOWTO](https://rentry.org/59xed3#rare-characteroc-howto) below, and good luck.  
If you just want to generate a character without changing standard clothes, hair or accessories, that's all you need.  
If you want more out of the model, read the long version.

### The long version

If you want the model to be flexible with clothes, backgrounds and whatever details, you will need to strategize and pick images more carefully.  
Like before, the **advice is to train first and fix issues later, as you might get lucky with a lazy set.**

#### Consistency of individual elements

Depending on your standards, some images have more value than others when teaching the AI.

For example, imagine you train Superman, with his iconic logo over his chest. If you train with just images of Superman in his costume, the AI will attempt to draw the logo on pretty much everything you prompt for, even a business suit. You also need to tag accordingly so the AI can tell the logo is part of the costume and not part of Superman (but that's the most complex part, refer to the tagging section for details).

#### Teaching individual elements

For teaching the AI an _individual element_, you want images where that element is clear, and images where the element is not present, so you can use prompts to control it, or to avoid it appearing all the time.  
The Unet seems to learn by "difference", so simply editing an accessory or other element out of an image, and then feeding both "on" and "off" images will help separating it. You can afford some sloppiness.

### Image size/aspect ratio

By default the scripts will "bucket" images. That means putting them in different containers (the buckets) based on their resolution and aspect ratio. This is highly convenient. However, it seems there still needs to be some care involved.  
**If your images are bucketed too randomly, that seems to cause issues and lower quality of the model.**  
It seems to do better when most images fall in a single bucket or they are in a balanced spread (buckets have around the same number of images).  
Regardless of bucketing, you usually want images that are the exact same resolution you are training with, those will always work better.  
I seem to have _somewhat_ better results when I increase the minimum a bit (320) and decrease the maximum a bit (768). Maybe because that means a smaller amount of buckets to spread images into.

### REGULARIZATION IMAGES

Using them is what achieves "dreambooth style" training, read above for an explanation.  
Setting them up is similar to how you set up your training images, just place your regularization images with the same format as the training images.  

|   |   |
|---|---|
|[1](https://rentry.org/59xed3#L-8-1)<br> [2](https://rentry.org/59xed3#L-8-2)<br> [3](https://rentry.org/59xed3#L-8-3)<br> [4](https://rentry.org/59xed3#L-8-4)<br> [5](https://rentry.org/59xed3#L-8-5)<br> [6](https://rentry.org/59xed3#L-8-6)<br> [7](https://rentry.org/59xed3#L-8-7)<br> [8](https://rentry.org/59xed3#L-8-8)<br> [9](https://rentry.org/59xed3#L-8-9)<br>[10](https://rentry.org/59xed3#L-8-10)|Your training set folder (point the Kohya script for this folder as normal)<br>+ X_Concept1<br>    + image.jpg    + image.txt<br>+ Y_Concept2<br>    + image.png    + image.txt<br>+ reg (the script will ignore this folder normally, point your reg_dir to this folder)<br>    + Z_Concept1        + image.jpg|

#### Easy route

You don't need to match the number of repetitions in the regularization image folder, but the names need to match. Use the multiplier as necessary to boost the number of reg images. Usually, you want **as many regularization images as regular training images, repeats included**, but you can play around with the amounts.  
The reg images **do not need captions**, but I hear it can help. Untested at the moment.  
Use stuff of the same "class" as your character. Since you'll be training only characters with reg images, pick something that resembles your character _but not quite_. I find AI outputs of a prompt _equivalent to the one you would use with the LORA enabled_ (if your character has pink hair and is a girl, prompt for girls with pink hair, even if they don't resemble the character much, you want similar but not "close" results, apparently).  
I've tried using images of the character being trained as well and it still worked.

##### Easy explanation:

This is highly abstracted and not exactly how it works, but if you are going this route, it'll work.  
Think of the Unet as an old TV or CRT screen.  
When you train the Unet you are putting an image on the screen and "leaving it for a while". Eventually, some "pixels" on the screen will get burned.  
By applying regularization, you are kind of flushing the image so it doesn't burn up too much, like a screensaver.  
A small amount of attributes from the reg images can go into the Unet, which might be enough to boost diversity of poses and other minor details.

#### Hard route

Same setup as before but with some significant differences.  
Turns out the regularization can be optimized with some extra steps. After someone tipped me about the actual effects of regularization, and I read the documents myself, turns out there's a method to it.  
You will want to **generate an AI reg image for every training image** you have. The names will have to match. So **every training image will have a matching regularization image**.  
To generate the images, you need to use:

- Generating images from the same model you are going to train (animefinal-full-pruned.ckpt if NAI, etc).
- Same prompt as the caption for the training image.
- DDIM sampler, resolution equal to your training resolution (not the same as the training image!), seed equal to your training seed (420 if you didn't touch it in the scripts below).  
    Then rename the image so it matches the filename of the matching training image.  
    While I notice a decent quality level, and somehow a bit more retaining of style, I can't say it blows the easy method out of the water.

##### Hard explanation:

Apparently, and roughly, regularization images are reduced to latents and then trained on how to produce them back, using DDIM as sampler.  
The theory seems to be that it then tries to match the tags, seed and latents so it has a more direct clue of what is it training, as opposed to trying to "look" into the whole thing. _This does not mean the reg is being used as a mask or anything, latents aren't exactly images, they are just represented as such so the eldritch knowledge doesn't fry our meaty brain._  
Therefore the reg images need to match the tags and seed, as it seems to have an easier time correlating both that way.  
Unfortunately, while the results were very good from testing it "by the books", it's not _much_ better than doing it with random images.  
The reason for why it works regardless is unknown.

#### Random images

You can use a collection of random images as well. I've had it work a few times.  
Just throw a bunch of nice images with decent style or features in there, a little bit of the collective style of the reg images will carry over to the model,

### TAGGING YOUR IMAGES (FINETUNING ONLY, IMPORTANT!!!!)

The AI is more tolerant of a few low quality images than of a few bad tags.

Install this webui extension: [https://github.com/toshiaki1729/stable-diffusion-webui-dataset-tag-editor](https://github.com/toshiaki1729/stable-diffusion-webui-dataset-tag-editor)  
It's a tool to batch edit/add/remove/interrogate tags for image sets, it'll help a lot with interrogating and simple batch (multiple) addition or deletion of tags.

The first step is using an interrogator like Deepdanbooru or WD1.4 Tagger. That will give you a bunch of tags to work with.  
If using the above extension, do something like this.  
![](https://i.imgur.com/Q6gngTv.png)

The first time **before clicking Load** make sure to set an interrogator (wd-v1-4-swinv2-tagger-v2 works fine for me), and "Use Interrogator Caption" to "If Empty" to get your starting tag base.

SET IT TO "NO" AFTERWARDS. Consider it the gun safety trigger. If you leave it in anything but "No" or "if Empty" (once .txt files exist) it'll do it over and overwrite your changes!

Tagging is surprisingly important and too much or too little (or too randomly spread) can ruin your model or make it too rigid.  
Training **works by instructing the AI to "find" the tagged elements in the given image** even if it doesn't exactly know what is what.  
Your job is precisely to help it figure it out (unless it already knows from existing training).

#### When to tag characters/styles

Your character/style/concept activation tag should be the very first tag in the tag list, and present in _every_ tag file. If you add a file later and forget to put it there, it'll make things unreliable.

Characters and styles don't _need_ to be strictly tagged, but you are adding extra glue to correlate the character with the associated tags, like an activation word.  
When generating images, this activation word can be weighted in a prompt (like `(character:1.2)`) and can help consistency if other tags are affecting the accuracy, specially if multiple characters or versions of the character are being trained.  
If the checkpoint you are training from has prior knowledge of a character, style or concept, you'll make use of this training as well (this also works both ways, as you may want to avoid that prior training and use a different tag, or you may want to override the prior training with your own).  
So, short version: **tag characters and tag concepts well**. Styles are a looser thing, so you don't strictly need to tag them, but I think it's a good idea to do so.

#### Tags and details

Make sure you can provide examples with certain tags "on" and "off", like if your subject character has a hat, provide a pic with hat (and tag it as having a hat) and one without (without the tag). If you are having a severe lack of images, head to the "Rare character HOWTO" section.  
When generating images with the output LoRA, you'll be able to prompt for the hat, or put the hat in negatives as convenient.  
A tag existing will bias the model to have a higher chance of putting that something into the final image (see why that can be troublesome here: [False positives/autotagging](https://rentry.org/59xed3#false-positivesautotagging)) but that can also be used as an advantage if you _want_ to draw attention to that something.

Tagging works like trying to explain a thing to a person who is very gullible. Tag a bunch of apples as oranges and it'll start generating oranges when asking for apples. You also might want to specify certain details. _If you have a character in a cape, it'll always consider the cape part of the character unless you tell it the character is wearing a cape._  
Let's put it this way. The AI learns the whole character as a _whole collection of things_ unless you specify its components or the components are well-known to the **checkpoint** you use.

Tagging elements like wings, tails, unusual bits of clothing or decorations can also help making them less of a mess, **specially if you provide examples of the character without them** (just edit the images if needed). There will always be some trouble with stuff **behind** a character, but the more (properly tagged) images you can show, the easier time the text encoder will have linking to those elements.  
Tagging those stray elements will also help with stuff like shirt logos that keep appearing with different clothes, as long as you can show it "on" and "off".

##### What to tag

- Tag things you want the AI to be aware of. It can infer some things on its own, but _don't count on it if it's unusual._ The AI can't quite separate certain elements from a character because it has no idea what it is. You need to teach it with on-off samples so it can get it. So tag those.
- You'll also want to tag obvious stuff, the color and type of hair, the color and type of clothes, and whatever elements the AI struggles with when you test the model.
- What you tag also seems to have some influence at generation time. For example if a character has visible eyelashes in the training images, and you tag "eyelashes", you'll obtain visible eyelashes much more consistently without the need of explicitly prompting for it. Not doing it will make it random and might require prompting explicitly.
- Poses are to be tagged as well. From what other people has shown me, not tagging _any_ pose seems to lead to samey poses when generating.
- Anything you feel important to note or you want to be more likely to appear in generations.
- Remember awareness of a tag means it can also be **used for negatives**. So tagging things you want to **remove** that way works, too.

##### What not to tag

- You don't usually need to indicate stuff like a human having a face or hands unless they don't. The Unet seems to be able to figure out the relationship between _some_ elements.
- It's also not strictly necessary to tag a style/artist.
- Tagging things like "simple background" can influence the model into generating images with simple backgrounds. This doesn't disable the ability to generate backgrounds (simple background in prompt negatives can fix that) but might be undesirable. Similar to the eyelashes example above, existing tags might have some influence when generating.
- You may want to avoid tagging certain things, so the AI doesn't fixate on them, at your convenience.

##### False positives/autotagging

EL DIABLO. This is bad and you want them gone. False positives seem to confuse the AI and consistency drops considerably.

Automated tagging (Deepdanbooru, WD1.4 tagger...) make a lot of false positives or fails to see details, gets incorrect hair colors due to lighting or palette...so make sure to remove incorrect tags, and add the ones that are missing. A single "brown hair" in a blonde character, due to a darker palette, will make the generations randomly show brown hair in broad daylight.  
Make sure it doesn't goof like confusing a sparkle for a star, a lamp for a moon, and obvious goofs like that.  
Let's put in in a simple, alarmist sentence: **Bad tags contaminate the model**.

##### Consolidating tags

Interrogators will usually return a group of tags when an element is detected. Like "boots, red footwear, red boots" when given an image of Laetitia.  
You usually want to consolidate those into a single one. "Red boots" is the most directly descriptive there, so I choose that one.

##### Tag debugging

When testing your model, if you feel an element is too insistent, too hard to remove, or appears everywhere, that's because you tagged wrong. Clean up and try again focusing on the tags related to that annoying element, that's the only way I found to get them out.

---

## OTHER TRAINING PARAMETERS

### CLIP skip

If you are analyzing a model too hard you may find the 11th layer is zeroed with CLIP skip 2. This is normal, as you skip training it, it's zeroed out.

The value for `--clip_skip` must be the same as the one you use to generate images with the model you train from.  
So if you train on NAI, that uses CLIP skip 2, set it to `--clip_skip=2`.  
If you use a realistic model and some furry models that uses CLIP skip 1, set it to `--clip_skip=1`.

I heard recommendations about always training at CLIP skip 1, I'm investigating whether it is a good idea or not.

### Number of steps/epochs

Your training steps is divided by your batch size. You are doing X steps at once, so if you have batch 2, it'll do two steps at once. Therefore, if you got 1000 steps and batch size 2, it'll show as 500 steps. Keep this in mind!

While more repeats are somehow better than more epochs, it's useful to have a few actual epochs in order to generate progress snapshots. If you burned a model, the snapshots might be fine at a previous epoch.

Total number of steps is your `(number of images x number of repeats) x number of epochs` unless you are using regularization images which is, `((number of images x number of repeats)+(number of reg images x number of repeats)) x epochs`, or basically double the steps.  
You want at least ~1000 total steps for training to stick. ~800 at the bare minimum (depends on whether the concept has prior training or not). For training from absolute scratch (a non-humanoid or obscure character) you'll want at least ~1500.

The perfect number is hard to say, as it depends on training set size.

- You want more steps if you lower the learning rate.
- If, during use of the model, you can raise LORA strength above 1.0 and it still works fine or better, you can train it more without ill effects.

### Learn dampening

Certain options act as _learning dampeners_, meaning they reduce the learning rate or its impact.

|Option|MIN|MAX|Base Default|Learn dampening|VRAM use|Generation effect|
|---|---|---|---|---|---|---|
|resolution|512|768|512|↑↑↑ every +64|↑↑|Increases quality of finer details.|
|noise_offset|0.0|1.0|OFF|↑↑↑ every +0.1||Increases dynamic range (brighter brights, darker darks). May "deep fry" if set too high.|
|network_dim|1|768|64(original spec:4)|↑ every -16|↑|Increases network size (can cram more into it)|
|alpha|1|net dim|net dim|↑↑ every -16||Dampens learning to prevent precision errors.|
|min_snr_gamma|1|20|5|↑ every +1||Smooths average loss, making learning more stable.|
|scale_weight_norms|0|10|1|To determine conclusively||Reportedly increases compatibility when generating with more LoRAs, discards style slightly|

Numbers aren't absolute because there are no hard numbers to math. Every arrow represents a noticeable small decrease.

This is interesting for a good reason. _The more steps you can fit into the training without burning up the Unet or TE, the better_. So at times you may want to dampen learning so you can train more. This, of course, means more training time, but seems that the results make much better use of the images in addition to their effects. You can also compensate the learn dampening with more learning rate, but that might not work as well.  
The simplest one to use is Alpha, as it has no other effects.

I don't recommend intentionaly dampening the training a lot, since you will hit diminishing returns quickly, unless you are training styles or concepts.

### Net dim (network dimensions)/Rank

Network Dimensions can also be referred to as "rank". If you read about rank 128, that'd be net dim 128.

The current maximum value seems to be 768, after that it's known to cause issues.

Lower ranks and alpha requiring **higher learning rate** to achieve equivalent detail. **Adaptive optimizers** should take care of this for you (just add an extra epoch or two instead) but **if you are still using manual learning rates do keep it in mind**.

The network dimensions, or rank, indicates how many parameters of the Unet/TE to train. The default is 4, but 64 is a very good value for most characters or styles.  
The ninja scrolls indicate the higher the value the higher the "expressive power" of the model, but has a drawback of higher file size. Seems to be about `value x 1.3MB (x 2 if full precision)`. A hypothetical model with the current safe maximum size, 768, will be roughly 1GB. Double that if saving the model at float precision.

For characters, a size of 64 tends to suffice. You can go lower the more "generic" the character is. If it's an anime girl whose main defining characteristics are facial details, hairstyle and clothes, a size of 32 or even 16 will be fine. More unique, intricate or unusual characters will be better at 64, 92 or 128. With **current methods, 92 seems to be where diminishing returns start kicking in**, and **128 is already a bit of a waste**. I find 64 can handle pokemon and cartoony characters just fine nowadays.

Styles can however use bigger sizes, with a bit of a correlation between **number of images** and the final value. With few images, 64 or 92 can do the job. With 10000+ images, try 128. Don't bother going as far as 256 unless you are putting image sets in the millions in there. It is however possible to get away with training a style with very few images and a small rank, so try to err on the side of lower values if guessing or indecisive.

Concepts can however afford to be a bit lower. Simple clothing, poses and backgrounds that aren't very elaborate can work with values as low as 8.

### Network Alpha

Alpha needs to be equal or lower than rank.

Network alpha is basically a learning brake, or dampener. It is always _relative to the value of net dim_.  
This is used to scale weights (the model's actual data) when saving them by multiplying them by (`alpha/net dim`) and was introduced as a way to prevent rounding errors from zeroing some of the weights.

- Setting it to 0, or the same value as net dim, prevents the dampening from happening.
- The default value is 1, which dampens learning considerably, so more steps or **higher learning rates** are necessary to compensate.
- The maximum value **is the same value as net dim**. Higher values are allowed but when I tried it to see what happened, the output was pretty **burned up**.  
    Observe what the numbers become when given a net dim of 128:  
    
    |   |   |
    |---|---|
    |[1](https://rentry.org/59xed3#L-9-1)<br>[2](https://rentry.org/59xed3#L-9-2)<br>[3](https://rentry.org/59xed3#L-9-3)<br>[4](https://rentry.org/59xed3#L-9-4)<br>[5](https://rentry.org/59xed3#L-9-5)|Alpha 0 = Alpha 128 = 128/128 = x1<br>Alpha 1 = 1/128 = x0.0078125<br>Alpha 64 = 64/128 = x0.5<br>Alpha 128 = 128/128 = x1<br>Alpha 256 = 256/128 = x2|
    

### Noise offset

Setting it too high might cause "deep-frying" effects similar to high (11+) CFG scale.

Noise offset works by adding a random value to the latents at learning time. This increases the dynamic range of images at the cost of slower learning.  
This feature is **entirely optional** and should only be used if you want the effect or want to use it as a learn dampener.

The effects are similar to increasing the CFG scale at generation time, but a bit more subtle. Raising it too high might "deep fry" the outputs, so be careful. Just a bit doesn't hurt if you want slightly bolder colors.  
A value of 0.1 is recommended. Just do 1-2 more epochs to counter the learn dampening.  
Effects **vary from training set to training set**, some seem more prone to deep-frying when the value is high than others. Regularized models usually come out better.  
After trying it for a while I can't really recommend it for general use, but it **can be useful if your inputs have dull colors**, or **in some situations where the outputs looks better with higher CFG scale**, so you can bake it in instead of raising it in webui.

- I've been using a value of 0.06 lately, just to add a little bit.
- If you know what you are doing, your training set is solid and you want more contrast, you can raise it safely.

### Resolution

Exact effects to determine.  
You can specify resolution as a single number (eg "512") or as an `width x height` value (eg "512x758").  
Seems to increase detail quality and composition at the cost of more training time/VRAM, but it also seemed to cause secondary effects.  
Training with it too high might decrease quality of lower resolution images, but small increments seem fine.

- 512 is a fine default.
- So far, 576 (576x576) has been consistently improving my bakes at the cost of training speed and VRAM usage.

### Augmentations

The augmentations are basically simple image effects applied during training.  
The effects can range from subtle to "enough of a boost to save a bad model", but they make training slower.  
The available options are as follows:

`--cache_latents` will not work when augmentations other than `flip_aug` are enabled.

|Augmentation|Values|Effects|Disables cache latents?|
|---|---|---|---|
|flip_aug|None|Randomly flips images horizontally. Useful anytime, **unless your character is heavily asymmetrical**. Like that guy from Street Fighter III.|NO|
|color_aug|None|Does random hue shifts. Can enhance color ranges and separate similarly-colored elements a bit better.|YES|
|crop_aug|None|Slices large images into parts instead of scaling them. Needs testing.|YES|
|face_crop_aug_range|"min,max" (e.g."2.0,4.0")|Tries to zoom into faces. Effects hard to notice?|YES|

### Min. SNR Gamma

This is a new feature to smooth the random peaks in training loss, leading to "smoother" learning. Can help reduce Unet/TE issues.  
Recommended value is `--min_snr_gamma=5`, 1 will have a stronger effect and 20 will barely have any effect. 20 is considered the maximum value, but it's recommended to be in the 1-10 range.  
It does not involve any speed loss or VRAM increase, so it doesn't hurt to use it. It's a pretty simple and straighforward optimization.  
Using SNR Gamma can cause some issues with DAdaptation and possibly AdaFactor, but I only encountered one noticeable quality drop, so it should be fine to use all the time. It has a more straightforward interaction with Prodigy, described here.  
More Min.SNR Gamma will introduce a tiny bit of dampening as well, increased for higher values.

### Scale Weight Norms

This is a feature that scales down values that are considered too large for a weight, preventing odd peaks that could potentially damage the Unet in the usual ways. This essentially protects the Unet and TE from burning up hard, dampens learning and discards training set style to a degree.  
The **recommended value is 1**, and you can go higher up for less effect (up to 10), and lower for higher effect.  
It is **described as making the output model more compatible with other models, like combining two or more LoRAs together**, even if some style is lost.

I found it helped make characters a bit easier to work with when changing clothes or poses at a value of 1.

### Seed

The random seed is what determines a repeatable sequence of random numbers. Just like when generating images, the seed has influence over the model.

It's entirely possible to find a random seed that isn't good for the subject, although it is rare. Adaptive optimizers should make this even rarer.  
If you have tried everything and your model is still not great, changing the seed might help.

Most random number generators are _pseudorandom_, meaning they output generally random numbers, but in a sequence. This is very useful because it can allow a programmer to reduce a lot of data into a single seed so the sequence of numbers can be repeated to generate a map, a level or a generated image. If a seed is not being asked for, it's usually taken from the computer's clock or randomized through other means.

I've used a fixed training seed from the start without issues, but I have seen two separate instances of bad seeds when helping someone else, where changing the seed suddenly fixed the problem. So while it's a very unlikely culprit, keep it in mind if nothing else seems to work.

### Loss

While loss is hardly a setting, it's a thing that bears mentioning.  
"Loss" is used to refer to how similar a image is to the images it was trained from. Too little loss and you got something very similar to the training images, while more loss means it's lost track of things and is just doing whatever. So more loss = less similar to the training set.  
Loss is usually in ranges of 0.15 and 0.05.  
To examine loss charts, you have to enable a log folder and use Tensorflow to see them in a handy graph form. You can do this with both the Kohya scripts and Kohya_ss.

---

## TESTING AND DEBUGGING MODELS

### Why testing?

Due to the random nature of AI imaging, first impressions might be misleading. Your model might output 3 great images by sheer chance, you call it good, and then you find out it has issues. Same if the first few images are bad.  
So make sure to test your models and try a lot of different prompts, mixes and other addons to see how the model actually performs. XY plots or a few batches of like 5 images can help expediting the process.  
![XY plot testing various epochs](https://i.imgur.com/pT2tFyU.jpeg "XY plot testing various epochs")

Try a multitude of scenarios, poses, clothes and expressions. I just keep a list of prompts I copypaste when testing.

Furthermore, the AI shows amusing or revolting quirks over time that aren't obvious at first glance, usually due to some stray or missing tag. Signs of overfitting may not be obvious at first too.

In other words you want some solid numbers. **Don't take first impressions literally**, since this is highly random. Change some tags around, change negatives. I've gotten models that _seemed_ bad at first glance but turned out to be pretty good once I adjusted my prompts a bit.

### Strength (at generation time)

Your LORA **should work fine at 1.0 strength** when using it to generate images.

- If you have to lower it to not ruin images, it's overfit or poorly trained.
    - A caveat to this is that there exist some cases where a very faithful model works well at 1.0 but you need extra flexibility or a more human body planning, so lowering it to ~0.8 can do the job.
    - DAdaptAdam and Prodigy make it much easier for models to just work at 1.0 because of the automatically corrected learning rates.
- If you have to raise it, that means you still have room available for more training or higher training rate, whether you want or not depends on how good it is _now_.
    - This of course excludes the new breed of "control slider" LoRAs appearing in CivitAI and such. As those use the strength as an effect multiplier.
- If you **have** to raise it or otherwise it's hardly noticeable, you **need** more training or higher training rate.

### Test your model with multiple checkpoints

While this sounds like an obvious one, now that many trainers are making their models public, you can see some models that work great in CivitAI previews but perform really poorly in your setup. **I am not calling anyone out, so lower the pitchforks!**  
The problem here is usually that the trainer just tested the model with the same checkpoint they trained with, saw it worked fine and uploaded. I'll admit this is not a terrible approach if training for yourself, but when uploading publicly it's a good idea to test with the most popular models. The amount of mixing in the model can require raising the strength or weighting the activation tag to get a good result.

If you feel this doesn't give great results, you can just call it a day, but make sure to put a notice like "this model works best in XXX checkpoint" for clarity.

At times it is just how it is, as training from other checkpoints or altering training parameters to work with a popular mix can ruin the result for your intended checkpoint.

### Overfitting

![An overfitted image](https://i.imgur.com/Quo0GXb.png "An overfitted image")

A model becomes "overfit" when it tries to reproduce the training images too aggressively or the results are plain weird.  
This is usually caused by the unet "burning up". A burned up Unet basically has probabilities for things set too high or too low due to math indigestion.

Overfitting usually happens when you train for too long or with too high of a learning rate. So here's what to do to get a view of the various epochs:

- First, make sure to save a snapshot every epoch.
- Generate a XY plot with a search and replace. Set your prompt to have a keyword such as "LORA", then have the XY plot search and replace that term for your LORA's activation token at strength 1.0 (so step 1 finds "LORA" and replaces it for "<lora:last:1.0>" or "<lora:last-0000001:1.0>", tailor it to your model's file names). Then run that plot and see how the model progresses every step. The natural progression should be from "no effect" (first one, using "LORA" which means nothing to the AI) to an increasing likeness of a character or style.
    - At this point you might find that epoch 7/10, for example, is perfectly fine and ready to go. Nothing else to do, just keep the winner.
- If it's always overfit, even at the start, review your training rate or use an adaptive optimizer like `DAdaptAdam`, `DAdaptLion` or `Prodigy`, as those adjust it on the fly.
- You may have net dim too high or alpha higher than net dim (alpha should never be higher than rank!).
- If it overfits even then, and are training on something that isn't NAI or base SD, try training from those instead. Some mixes aren't really fit for training.
- If nothing else works, you might have too many images or images that are dragging the thing down, or your rank is too low to properly math all your images.

#### If you have the additional-networks extension

Since sd-webui 1.5 this is not necessary anymore, as you can specify the strengths separately. `<lora:mylora:A:B>` such as `<lora:mylora:1.0:0.5>` will set Unet to 1.0 and TE at 0.5.

The webui extension allows modifying Unet and text encoder strength separately. This allows you to play with the values and try to see which component is over/underbaked. The changes usually reflect the adjustment necessary to training.  
If, for example, your model works fine at 0.5 strength for Unet and 1.0 strength for TE, that means you just need to reduce the Unet learning rate by half.  
If it works fine at 1.0 Unet strength and 2.0 TE strength, then leave Unet as it is, and double the TE learning rate.  
It saves a lot of guesswork if you are setting training rates manually.

### Debugging tagging

![Megane is love, megane is life.](https://i.imgur.com/nO0T0uF.jpg "Megane is love, megane is life.")  
In this case I didn't have enough examples of the character (One possible generic skin for the Medic class, or "megane Medi-ko" from Etrian Odyssey IV) with different clothes so it's biased to filling space for a bag that might or might not be asked for, and a specific design with a sailor neck and visible straps around the waist.  
The bag can be solved by _properly tagging all images with a visible bag, something I failed to do in this case_. I went with "messenger bag" since it was the type that came up the most often when autotagging, but only applied it to a few images.  
You may see stuff like shirt logos or specific accessories being too hard to get rid of. In this case, the coat elements issue is harder to get rid of and usually requires more images to teach it how to separate element from character and a tag to solidify that knowledge (preferably an existing one).  
You may want to do manual edits in a few images to remove the element and reduce the _probability_ of it existing when asking for something else at generation time.  
The **differences are subtle compared to TE issues**, but the more you train the more sense it makes. You'll also notice that kind of thing because _it's really persistent_ unlike TE errors that come and go. Usually requires a full change of clothes (like putting a character only wearing dresses in a hoodie or armor, or direct nudity) to remove via prompting or very strong weights for alternate clothes of accessories.

---

## Rare character/OC HOWTO

![BE PRAYING](https://i.imgur.com/JXs0gfA.png "BE PRAYING")**EFFORT ALERT. DON'T GIVE UP**_WORK IN PROGRESS (sciencing needs time and a lot of trial and error, please wait patiently)_  
![Laetitia, from Lobotomy Corp/Library of Ruina. ©Project Moon](https://i.imgur.com/TY1XZ0k.png "Laetitia, from Lobotomy Corp/Library of Ruina. ©Project Moon")I'm particularly specializing on rare characters, I'll update this section with advice on how to get by if you only have a few crappy images of your favorite character.  
I have seen a curious phenomenon of people wanting to turn specific AI outputs into a more fleshed out character and the entire thing _fascinates_ me at a fundamental level, so I'll try to expand this advice to help out with that as well.

Prepare some form of image editor (I recommend [Krita](https://rentry.org/59xed3), but Photoshop, GIMP, [Paint.NET](http://paint.net/) or any other program you are comfortable with, if any. If you aren't acquainted with any of them, download Krita (it's free and I really like using it for actual art) and get acquainted with a couple tools.

### Image preparation

- You will need at least 10 to 25 images depending on their quality and variety. There have been successful attempts with less images, but it's up to luck. 100 images is the gold standard, but I understand you are working under constraints, here.
    - If you just have one or two images, you will [definitely need to work together with the AI](https://rentry.org/59xed3).
- Have a bit of critical eye, if you can choose, choose images that look better or at least look better to _you_.
    - If you can't choose, use regularization to reduce the impact of the image's style.
    - Ask a pair of friendly eyes if necessary.
- Human artists aren't always accurate and goof like the AI, and those goofs carry to the AI. You want many **views and styles of the same thing**, not variations of it. In other words, artist mistakes like wrong hairstyle, eye colors, mistaken clothing elements or so are better avoided. If you got nothing else, **edit them for accuracy**.
    - At times this happens even within canon art. In those cases, pick your favorite variation and try to reinforce it the same way.
    - img2img/inpaint until it works is an option, but it can take from one to infinite tries. Help it out manually if needed.
- You want at least a couple views and different costumes, or if the costume has multiple layers, pictures with some layers removed will allow you to toggle, as long as you tag them accordingly.
    - Again, this is not always possible. It's not uncommon for a character to be always drawn in the same clothes or pose, specially if really obscure. You will have to edit them or ask someone to help (that someone [can be the AI](https://rentry.org/59xed3)).
- 3D models are viable, but unless you want to generate renders, use regularization to soften the style. You can also img2img your renders to alter style.
- BE PRAYING

### Image editing

#### Quick Krita starter pack

While a full tutorial is out of the scope of this rentry, I advise finding a basic tutorial video and maybe setting up the plugin to send images back and forth from Krita to sd-webui (but good old copy/paste works too).  
After doing stuff for a while, I find these tools to be rather useful.  
![The elite four](https://i.imgur.com/pqSUZbX.png "The elite four")  
These four tools, all placed in the Digital section of Brush Presets, are your bread and butter editing tools.

- Distort Move will _displace_ stuff under the cursor in the direction of your stroke. This can be used to fix short limbs, make hair longer or shorter and generally morph an image. Be careful, as it's blurry, so the bigger the resolution of the image the better. Use img2img/inpaint to fix the results.
- Adjust Color will change the colors of the area under the cursor to the selected main color. Use this to fix hair/eye/clothing colors. It might require multiple passes to get the desired outcome.
- Blender Blur will, well, blur the area under the cursor. If can be useful to iron out your own edits, make smaller mistakes less noticeable or to clean out JPEG artifacts.
- Basic-1 is a basic solid color brush, useful to paint over things.

I've personally verified these tools can be used well for editing stuff without the use of a tablet, which I assume most of you don't have. I've been doing it mouse-only just to make sure the advice didn't require fine skills.

If your skills aren't great, make sure to make edits in small steps so they are easy to undo with the undo key (ctrl+z) and you don't have to start over from scratch. Use layers at your discretion, but if you are copy-pasting make sure to _select all_ and _copy merged_ so you don't copy only the current layer (also if you draw off the edges it may go over size, so select all and copy merged all the time so you ensure it's always the same size).

Remember, the AI can help turn your edits into "well integrated" changes.

### Using the AI to help you out

**Inpaint and img2img are your friends**. You can use img2img (denoise ~0.7) to drastically alter official art, giving the AI variance in styles or poses in return. Use as high a resolution as you can muster, and inpaint (_only masked_ option) faces and fine details so they are more coherent.  
As for inpaint, you can use it to for example change clothes and then inpaint (again _only masked_ and at higher resolutions) for coherence.  
Note that with "change clothes" I mean you can draw some somewhat coherent blobs of color on top, or erase things, paste something from other image on top, stock art, another AI generation... **Anything goes** if it does the job.  
Similarly, you can use the same principle to remove elements. For example if your LoRA keeps producing elements like bags, straps or bits of armor and they bleed into different clothing, then make a copy of an image and remove the element and use inpaint to try to fill the blanks. Similarly if a character has some shirt logo or accessory like a pendant, you also want to make another copy and remove it.

Likewise, you can photoshop your way into turning **an AI generation into your character** by editing the hair color, style and clothes until the resemblance is good. This is a last resort, but if it's **accurate** it'll work.

Don't be afraid of making some **sort of frankenstein image out of multiple bits** (a collage) and then having the AI make it coherent.

ControlNet is another valid option to help you out. It may help you colorize grayscale images, turn a quick sketch into something more elaborate or turn other AI outputs into different images with different styles or so. And, if you are using sketches and have managed to obtain enough colored images, throw the sketch in too, it'll give more "silhouettes" for the Unet to work with (and will probably be discarded by the common "monochrome" in negative prompts).

### Using raw AI outputs as inputs

Watch your CFG Scale when generating AI images for learning. Make it lower than your usual when generating normal images, if CFG scale is too high, the higher contrast and more saturated colors will bleed into your LoRA, so keep it fairly mild (CFG Scales of 5-7). Unless, of course, you want the saturated colors for style, in that case go wild. Think that when generating, it'll add more on top.

Stable Diffusion does **not** add an invisible watermark to prevent loopback training. Ignore hearsay stating the contrary.

AI outputs are perfectly valid as AI inputs. However, you must be _really picky_ about them. **They can influence the results heavily to look like a specific model, like the OrangeMixes**.  
Ideally, you want the AI images to be the same size as your training resolution.

Standard SD goofs can easily carry over your outputs unless regularized or balanced by many quality pictures (_if you are reading this, chances are you don't have that luxury, though_), so make sure it's as proper as possible, ask for a second opinion from a friend or something if you doubt (seeing many generations of the same thing can dull your senses enough to miss obvious errors).

Hands are generally a lost cause but try to at the very least have the correct amount of fingers. Inpaint until it works if necessary. If you have art skills, fix them yourself to ensure it'll go right.

### The GACHAMAX Temporary LoRA approach (last resort)

If your constraints are massive (like one image) you can "bruteforce" the process, so to speak.  
This is relatively time consuming and has a bit of a luck factor involved.

- 1. Train a simple, quick model (10 epochs, should take like 5 minutes) with just the one image and try to generate the best possible likeness in a similar style with whatever comes out, inpaint or img2img until it works, or edit it. It should be easier than doing it from scratch.
- 2. Train another quick model with the new image.
- 3. Some coherence will start to come up, so you'll have an easier time than the first and you may be able to raise it to 4 proper images in less time.
- 4. At this point you can probably change models or add some style LoRAs to add variety in styles and try to get 6 images or so.
- 5. Train another quick model, will now take a little bit longer but should still be really fast at 10 epochs.
- 6. Now try to see if any image is sticking out, purge it if necessary and replace with the best you can get.
- 7. Try to get as many good images as you can and repeat the process until it's solid and flexible.

This is a very luck based approach and may still require edits to save time, but it will _eventually_ work.

### General advice

Elbow grease is necessary to get a really good model out of an obscure character. Depending on how complex the character is, you might need at least 5 tries to get _good_ results (by my standards of accuracy and flexibility, of course. If your second try or even the first is good enough for you, then just wrap up and call it done, you already won).

If using purely AI generated images, try not to stick to a single checkpoint so you have more style flexibility.

### For readers with art skills

If you have some art skills, you can train your own characters and style.  
Similarly, if you train an existing character, you can customize a model further than what it's possible with public images and fanarts. You can supply extra angles, poses, clothes, expressions and proportions to increase the range of the model. While every trained model is different because of curation and standards, supplying your own artwork can make it much more unique thanks to that.

I've had training respond pretty positively to my own images and even lazy sketches, and I'm hardly the best at art.  
When I have more free time to experiment with this, I'll expand this section further.

---

## SAMPLE POWERSHELL SCRIPT (WINDOWS)

**START COPYING BELOW HERE, SAVE TO A TEXT FILE, EDIT PATHS AND OPTIONS AS NEEDED**  

```
# Config:
$ckpt = "X:\SD\voldy\models\Stable-diffusion\animefull-final-pruned.ckpt"; #Full path to model you want to train FROM, or base model.
$image_dir = "X:\SD\training\my_concepts_folder"; #Data set folder
$output = "X:\SD\voldy\models\lora"; #Output folder for your baked LORAs.
$reg_dir = "X:\SD\training\reg"; #Only use these for dreambooth style training. Point to an empty folder otherwise.

$train_batch_size           = 1        #Amount of images to process at once. I have 8GB of VRAM so I left it at 1, it just worked. Raise if you got more VRAM.
$learning_rate              = 0.0001   #Unet learning rate.
$text_encoder_learning_rate = 0.00005  #Text Encoder learning rate. This is the recommended value.
$num_epochs                 = 8        #Total number of epochs (amount of times the entire set is repeated)
$save_every_n_epochs        = 1        #Save checkpoints every X epochs.
$resolution                 = 512      #Resolution to work at. Higher requires more training for the unet and more VRAM.
$network_dim                = 128      #AKA Rank. Higher for more resemblance to the training images and bigger file size. 96-192 for characters. 160 was good for me.
$network_alpha              = 128      #Must be equal or lower than network dim. Dampens learning the lower it is, but avoids rounding issues.
$noise_offset               = 0.0      #Increases dynamic range of outputs. Every 0.1 dampens learning quite a bit, do more steps or higher training rates to compensate.
$clip_skip                  = 2        #Set it to 2 if you train from NAI.
$optimizer                  = "AdamW8bit" # Valid values: "AdamW", "AdamW8bit", "Lion", "SGDNesterov", "SDGNesterov8bit", "DAdaptation", "AdaFactor"
# Default AdamW8bit (old --use_8bit_adam). DAdaptation requires setting learning rates to values between 0.1 and 1.0 as it tweaks them during training.
$scheduler                  = "cosine_with_restarts"

# End of config

$learning_rate              = $learning_rate * $train_batch_size # Seems to work better for the Unet.

.\venv\Scripts\activate #Activate python venv before starting.

accelerate launch --num_cpu_threads_per_process 8 train_network.py `
    --network_module="networks.lora" `
    --pretrained_model_name_or_path=$ckpt --train_data_dir=$image_dir --reg_data_dir=$reg_dir --output_dir=$output `
    --caption_extension=".txt" --shuffle_caption --keep_tokens=1`
    --prior_loss_weight=1 `
    --resolution="$resolution" `
    --enable_bucket --min_bucket_reso=320 --max_bucket_reso=960 `
    --train_batch_size="$train_batch_size" `
    --learning_rate="$learning_rate" --unet_lr="$learning_rate" --text_encoder_lr=$text_encoder_learning_rate `
    --max_train_epochs=$num_epochs `
    --mixed_precision="fp16" --save_precision="fp16" `
    --optimizer_type="$optimizer" --xformers `
    --save_every_n_epochs="$save_every_n_epochs" `
    --save_model_as=safetensors `
    --clip_skip="$clip_skip" `
    --seed=420 `
        --flip_aug `
    --network_dim="$network_dim" --network_alpha="$network_alpha" `
    --max_token_length=225 `
    --cache_latents `
    --lr_scheduler="$scheduler" `
        --noise_offset="$noise_offset"
```

## SAMPLE BASH SCRIPT (LINUX)

**START COPYING BELOW HERE, SAVE TO A TEXT FILE, GIVE IT EXECUTABLE PERMISSIONS, ETC**

```
#!/usr/bin/env bash
#Set these paths as required:
WEBUI_DIR="/mnt/DATA/AI/stable-diffusion-webui/" # SD-webui folder
MODEL_DIR="/mnt/DATA/AI/stable-diffusion-models/Stable-diffusion/" # Model folder
TRAIN_DIR="/mnt/DATA/AI/sd-scripts" # Kohya scripts folder

function training_Kohya_lora {
    cd "$TRAIN_DIR" || {
        echo "Folder not found or not accessible."; exit 1
    }

    local training_set="penny" #Set this to the base folder for a character.
    local ckpt="$MODEL_DIR/animefinal-full-pruned.ckpt" # Base model(checkpoint) to finetune
    local image_dir="$TRAIN_DIR/SETS/$training_set/"
    local reg_dir="$TRAIN_DIR/SETS/$training_set/reg/" #Regulation image folder. Optional, you can point it to an empty folder if you don't want them.
    local output="/mnt/DATA/AI/stable-diffusion-models/LORA/" #Folder to save outputs. WARNING: Will overwrite existing files.

    local learning_rate="0.0001" #Learning rate. Remember this is supposed to be a magnitude larger than a dreambooth equivalent. Worked well for me at this rate.
    local text_encoder_lr="0.00005" #Learning rate for TEXT ENCODER. This is the value suggested in the ninja scrolls. Seems to work better for details.
    local train_batch_size="2" #Amount of images to process at once. I have 8GB of VRAM so I left it at 1, it just worked. Raise if you got more VRAM.
    local num_epochs="6" #Total number of epochs (amount of times the entire set is repeated)
    local save_every_x_epochs="2" #Save checkpoints every X epochs.
    local network_dim="160" #Higher for more resemblance to the training images and bigger file size. 96-192 for characters.
    local scheduler="cosine_with_restarts"

    . venv/bin/activate #Activate your venv before starting.

    accelerate launch --num_cpu_threads_per_process 8 train_network.py  --network_module="networks.lora"    --pretrained_model_name_or_path="$ckpt" --train_data_dir="$image_dir" --reg_data_dir="$reg_dir" --output_dir="$output"  --output_name="${training_set}_last_e${num_epochs}_n${network_dim}" --caption_extension=".txt" --shuffle_caption    --prior_loss_weight=1   --network_alpha="$network_dim"  --resolution=512    --enable_bucket --min_bucket_reso=320 --max_bucket_reso=768 --train_batch_size="$train_batch_size"  --gradient_accumulation_steps=1 --learning_rate="$learning_rate" --unet_lr="$learning_rate" --text_encoder_lr="$text_encoder_lr"    --max_train_epochs="$num_epochs"    --mixed_precision="fp16" --save_precision="fp16"    --use_8bit_adam --xformers  --save_every_n_epochs="$save_every_x_epochs"    --save_model_as=safetensors --clip_skip=2   --seed=420  --flip_aug --color_aug --face_crop_aug_range="2.0,4.0"  --network_dim="$network_dim"    --max_token_length=150  --lr_scheduler="$scheduler" --training_comment="LORA:$training_set"
}

training_Kohya_lora "$@"
```


Pub: 05 Jan 2023 21:20 UTC  
Edit: 18 Aug 2023 11:52 UTC  
Views: 340387  

---