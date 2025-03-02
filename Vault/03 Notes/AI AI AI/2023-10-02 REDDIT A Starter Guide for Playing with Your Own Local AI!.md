---
created: 2025-02-20T14:11:58-06:00
url: https://www.reddit.com/r/LocalLLaMA/comments/16y95hk/a_starter_guide_for_playing_with_your_own_local_ai/?rdt=44764
tags:
  - source/reddit
title: A Starter Guide for Playing with Your Own Local AI!
published: 2023-10-02T16:31:14-05:00
subreddit: r/LocalLLaMA
---

#webclip/unread

> Posted in **r/LocalLLaMA** by *LearningSomeCode* at 2023-10-02T16:31:14-05:00 (⬆️ 845)


# A Starter Guide for Playing with Your Own Local AI!

So I've noticed a lot of the same questions pop up when it comes to running LLMs locally, because much of the information out there is a bit spread out or technically complex. My goal is to create a stripped down guide of "Here's what you need to get started", without going too deep into the why or how. That stuff is important to know, but it's better learned after you've actually got everything running.

***This is not meant to be exhaustive or comprehensive; this is literally just to try to help to take you from "I know nothing about this stuff" to "Yay I have an AI on my computer!"***

I'll be breaking this into sections, so feel free to jump to the section you care the most about. There's lots of words here, but maybe all those words don't pertain to you.

**Don't be overwhelmed; just hop around between the sections.** My recommendation installation steps are up top, with general info and questions about LLMs and AI in general starting halfway down.

**Table of contents**

- **Installation**

- ***I have an Nvidia Graphics Card on Windows or Linux!***
- ***I have an AMD Graphics card on Windows or Linux!***
- ***I have a Mac!***
- ***I have an older machine!***
- **General Info**

- ***I have no idea what an LLM is!***
- ***I have no idea what a Fine-Tune is!***
- ***I have no idea what "context" is!***
- ***I have no idea where to get LLMs!***
- ***I have no idea what size LLMs to get!***
- ***I have no idea what quant to get!***
- ***I have no idea what "K" quants are!***
- ***I have no idea what GGML/GGUF/GPTQ/exl2 is!***
- ***I have no idea what settings to use when loading the model!***
- ***I have no idea what flavor model to get!***
- ***I have no idea what normal speeds should look like!***
- ***I have no idea why my model is acting dumb!***

# Installation Recommendations

> ***I have an NVidia Graphics Card on Windows or Linux!***

If you're on Windows, the fastest route to success is probably **Koboldcpp**. It's literally just an executable. It doesn't have a lot of bells and whistles, but it gets the job done great. The app also acts as an API if you were hoping to run this with a secondary tool like SillyTavern.

[https://github.com/LostRuins/koboldcpp/wiki#quick-start](https://github.com/LostRuins/koboldcpp/wiki#quick-start)

Now, if you want something with more features built in or you're on Linux, I recommend **Oobabooga**! It can also act as an API for things like SillyTavern.

[https://github.com/oobabooga/text-generation-webui#one-click-installers](https://github.com/oobabooga/text-generation-webui#one-click-installers)

If you have git, you know what to do. If you don't- scroll up and click the green "Code" dropdown and select "Download Zip"

There used to be more steps involved, but I no longer see the requirements for those, so I think the 1 click installer does everything now. How lucky!

For Linux Users: [Please see the comment below](https://www.reddit.com/r/LocalLLaMA/comments/16y95hk/comment/k37b0kh/?utm_source=share&utm_medium=web2x&context=3) suggesting running Oobabooga in a docker container!

> ***I have an AMD Graphics card on Windows or Linux!***

For Windows- use **koboldcpp**. It has the best windows support for AMD at the moment, and it can act as an API for things like SillyTavern if you were wanting to do that.

[https://github.com/LostRuins/koboldcpp/wiki#quick-start](https://github.com/LostRuins/koboldcpp/wiki#quick-start)

and here is more info on the AMD bits. Make sure to read both before proceeding

[https://github.com/YellowRoseCx/koboldcpp-rocm/releases](https://github.com/YellowRoseCx/koboldcpp-rocm/releases)

If you're on Linux, you can probably do the above, but **Oobabooga** also supports AMD for you (I think...) and it can act as an API for things like SillyTavern as well.

[https://github.com/oobabooga/text-generation-webui/blob/main/docs/One-Click-Installers.md#using-an-amd-gpu-in-linux](https://github.com/oobabooga/text-generation-webui/blob/main/docs/One-Click-Installers.md#using-an-amd-gpu-in-linux)

If you have git, you know what to do. If you don't- scroll up and click the green "Code" dropdown and select "Download Zip"

For Linux Users: [Please see the comment below](https://www.reddit.com/r/LocalLLaMA/comments/16y95hk/comment/k37b0kh/?utm_source=share&utm_medium=web2x&context=3) suggesting running Oobabooga in a docker container!

> ***I have a Mac!***

Macs are great for inference, but note that y'all have some special instructions.

First- if you're on an M1 Max or Ultra, or an M2 Max or Ultra, you're in good shape.

Anything else that is not one of the above processors is going to be a little slow... maybe very slow. The original M1s, the intel processors, all of them don't do quite as well. But hey... maybe it's worth a shot?

Second- Macs are special in how they do their VRAM. Normally, on a graphics card you'd have somewhere between 4 to 24GB of VRAM on a special dedicated card in your computer. Macs, however, have specially made really fast RAM baked in that also acts as VRAM. The OS will assign up to 75% of this total RAM as VRAM.

So, for example, the 16GB M2 Macbook Pro will have about 10GB of available VRAM. The 128GB Mac Studio has 98GB of VRAM available. This means you can run MASSIVE models [with relatively decent speeds.](https://www.reddit.com/r/LocalLLaMA/comments/16oww9j/running_ggufs_on_m1_ultra_part_2/)

For you, the quickest route to success if you just want to toy around with some models is **GPT4All,** but it is pretty limited. However, it was my first program and what helped me get into this stuff.

It's a simple 1 click installer; super simple. It can act as an API, but isn't recognized by a lot of programs. So if you want something like SillyTavern, you would do better with something else.

(**NOTE:** It CAN act as an API, and it uses the OpenAPI schema. If you're a developer, you can likely tweak whatever program you want to run against GPT4All to recognize it. Anything that can connect to openAI can connect to GPT4All as well).

Also note that it only runs GGML files; they are older. But it does Metal inference (Mac's GPU offloading) out of the box. A lot of folks think of GPT4All as being CPU only, but I believe that's only true on Windows/Linux. Either way, it's a small program and easy to try if you just want to toy around with this stuff a little.

[https://gpt4all.io/index.html](https://gpt4all.io/index.html)

Alternatively, **Oobabooga** works for you as well, and it can act as an API for things like SillyTavern!

[https://github.com/oobabooga/text-generation-webui#installation](https://github.com/oobabooga/text-generation-webui#installation)

If you have git, you know what to do. If you don't- scroll up and click the green "Code" dropdown and select "Download Zip".

There used to be more to this, but the instructions seem to have vanished, so I think the 1 click installer does it all for you now!

There's another easy option as well, but I've never used it. However, a friend set it up quickly and it seemed painless. **LM Studios.**

[https://lmstudio.ai/](https://lmstudio.ai/)

Some folks have posted about it here, so maybe try that too and see how it goes.

> ***I have an older machine!***

I see folks come on here sometimes with pretty old machines, where they may have 2GB of VRAM or less, a much older cpu, etc. Those are a case by case basis of trial and error.

In your shoes, I'd start small. **GPT4All** is a CPU based program on Windows and supports Metal on Mac. It's simple, it has small models. I'd probably start there to see what works, using the smallest models they recommend.

After that, I'd look at something like **KoboldCPP**

[https://github.com/LostRuins/koboldcpp/wiki#quick-start](https://github.com/LostRuins/koboldcpp/wiki#quick-start)

Kobold is lightweight, tends to be pretty performant.

I would start with a 7b gguf model, even as low down as a 3\_K\_S. I'm not saying that's all you can run, but you want a baseline for what performance looks like. Then I'd start adding size.

It's ok to not run at full GPU layers (see above). If there are 35 in the model (it'll usually tell you in the command prompt window), you can do 30. You will take a bigger performance hit having 100% of the layers in your GPU if you don't have enough VRAM to cover the model. You will get better performance doing maybe 30 out of 35 layers in that scenario, where 5 go to the CPU.

At the end of the day, it's about seeing what works. There's lots of posts talking about how well a 3080, 3090, etc will work, but not many for some Dell G3 laptop from 2017, so you're going to have test around and bit and see what works.

# General Info

> ***I have no idea what an LLM is!***

An LLM is the "brains" behind an AI. This is what does all the thinking and is something that we can run locally; like our own personal ChatGPT on our computers. Llama 2 is a free LLM base that was given to us by Meta; it's the successor to their previous version Llama. The vast majority of models you see online are a "Fine-Tune", or a modified version, of Llama or Llama 2.

Llama 2 is generally considered smarter and can handle more context than Llama, so just grab those.

If you want to try any before you start grabbing, please [check out a comment below](https://www.reddit.com/r/LocalLLaMA/comments/16y95hk/comment/k3k3mdy/) where some free locations to test them out have been linked!

> ***I have no idea what a Fine-Tune is!***

It's where people take a model and add more data to it to make it better at something (or worse if they mess it up lol). That something could be conversation, it could be math, it could be coding, it could be roleplaying, it could be translating, etc. People tend to name their Fine-Tunes so you can recognize them. Vicuna, Wizard, Nous-Hermes, etc are all specific Fine-Tunes with specific tasks.

If you see a model named Wizard-Vicuna, it means someone took both Wizard and Vicuna and smooshed em together to make a hybrid model. You'll see this a lot. Google the name of each flavor to get an idea of what they are good at!

> ***I have no idea what "context" is!***

"Context" is what tells the LLM what to say to you. The AI models don't remember anything themselves; every time you send a message, you have to send everything that you want it to know to give you a response back. If you set up a character for yourself in whatever program you're using that says "My name is LearningSomeCode. I'm kinda dumb but I talk good", then that needs to be sent EVERY SINGLE TIME you send a message, because if you ever send a message without that, it forgets who you are and won't act on that. In a way, [you can think of LLMs as being stateless](https://www.reddit.com/r/Oobabooga/comments/16qa4cj/comment/k1vy8rr/?context=3).

99% of the time, that's all handled by the program you're using, so you don't have to worry about any of that. But what you DO have to worry about is that there's a limit! Llama models could handle 2048 context, which was about 1500 words. Llama 2 models handle 4096. So the more that you can handle, the more chat history, character info, instructions, etc you can send.

> ***I have no idea where to get LLMs!***

[Huggingface.co](https://huggingface.co/). Click "models" up top. Search there.

> ***I have no idea what size LLMs to get!***

It all comes down to your computer. **Models come in sizes**, which we refer to as "b" sizes. 3b, 7b, 13b, 20b, 30b, 33b, 34b, 65b, 70b. Those are the numbers you'll see the most.

**The b stands for "billions of parameters",** and the bigger it is the smarter your model is. A 70b feels almost like you're talking to a person, where a 3b struggles to maintain a good conversation for long.

Don't let that fool you though; some of my favorites are 13b. They are surprisingly good.

A full sizes model is 2 bytes per "b". That means a **3b's real size is** **6GB**. But thanks to quantizing, you can get a "compressed" version of that file for FAR less.

> ***I have no idea what quant to get!***

"Quantized" models come in q2, q3, q4, q5, q6 and q8. The smaller the number, the smaller and dumber the model. This means a 34b q3 is only 17GB! That's a far cry from the full size of 68GB.

Rule of thumb: You are generally better off running a small q of a bigger model than a big q of a smaller model.

34b q3 is going to, in general, be smarter and better than a 13b q8.

[https://www.reddit.com/media?url=https%3A%2F%2Fpreview.redd.it%2Fr9gd7dn2ksgb1.png%3Fwidth%3D792%26format%3Dpng%26auto%3Dwebp%26s%3Db9dce2e22724665754cc94a22442f2795f594345](https://www.reddit.com/media?url=https%3A%2F%2Fpreview.redd.it%2Fr9gd7dn2ksgb1.png%3Fwidth%3D792%26format%3Dpng%26auto%3Dwebp%26s%3Db9dce2e22724665754cc94a22442f2795f594345)

In the above picture, higher is worse. The higher up you are on that chart, the more "perplexity" the model has; aka, the model acts dumber. As you can see in that picture, the best 13b doesn't come close to the worst 30b.

It's basically a big game of "what can I fit in my video RAM?" The size you're looking for is the biggest "b" you can get and the biggest "q" you can get that fits within your Video Card's VRAM.

Here's an example: [https://huggingface.co/TheBloke/Llama-2-7b-Chat-GGUF](https://huggingface.co/TheBloke/Llama-2-7b-Chat-GGUF)

This is a 7b. If you scroll down, you can see that TheBloke offers a very helpful chart of what size each is. So even though this is a 7b model, the q3\_K\_L is "compressed" down to a 3.6GB file! Despite that, though, "Max RAM required" column still says 6.10GB, so don't be fooled! A 4GB card might still struggle with that.

> ***I have no idea what "K" quants are!***

Additionally, along with the "q"s, you might also see things like "K\_M" or "K\_S". Those are "K" quants, and S stands for "small", the M for "medium" and the L for "Large".

So a q4\_K\_S is smaller than a q4\_K\_L, and both of those are smaller than a q6.

> ***I have no idea what GGML/GGUF/GPTQ/exl2 is!***

Think of them as file types.

- GGML runs on a combination of graphics card and cpu. These are outdated and only older applications run them now
- GGUF is the newer version of GGML. An upgrade! They run on a combination of graphics card and cpu. It's my favorite type! These run in Llamacpp. Also, if you're on a mac, you probably want to run these.
- GPTQ runs purely on your video card. It's fast! But you better have enough VRAM. These run in AutoGPTQ or ExLlama.
- exl2 also runs on video card, and it's mega fast. Not many of them though... These run in ExLlama2!

There are other file types as well, but I see them mentioned less.

I usually recommend folks choose GGUF to start with.

> ***I have no idea what settings to use when loading the model!***

- Set the **context** or **ctx** to whatever the max is for your model; it will likely be either 2048 or 4096 (check the readme for the model on huggingface to find out).

- Don't mess with rope settings; that's fancy stuff for another day. That includes alpha, rope compress, rope freq base, rope scale base. If you see that stuff, just leave it alone for now. You'll know when you need it.
- If you're using GGUF, it should be automatically set the rope stuff for you depending on the program you use, like Oobabooga!
- Set your **Threads** to the number of CPU cores you have. Look up your computer's processor to find out!

- On mac, it might be worth taking the number of cores you have and subtracting 4. They do "Efficiency Cores" and I think there is usually 4 of them; they aren't good for speed for this. So if you have a 20 core CPU, I'd probably put 16 threads.
- For **GPU layers** or **n-gpu-layers** or **ngl** (if using GGML or GGUF)-

- If you're on mac, any number that isn't 0 is fine; even 1 is fine. It's really just on or off for Mac users. 0 is off, 1+ is on.
- If you're on Windows or Linux, do like 50 layers and then look at the Command Prompt when you load the model and it'll tell you how many layers there. If you can fit the entire model in your GPU VRAM, then put the number of layers it says the model has or higher (it'll just default to the max layers if you g higher). If you can't fit the entire model into your VRAM, start reducing layers until the thing runs right.
- **EDIT-** In a comment below I added a bit more info in answer to someone else. Maybe this will help a bit. [https://www.reddit.com/r/LocalLLaMA/comments/16y95hk/comment/k3ebnpv/](https://www.reddit.com/r/LocalLLaMA/comments/16y95hk/comment/k3ebnpv/?utm_source=share&utm_medium=web2x&context=3)
- If you're on Koboldcpp, don't get hung up on BLAS threads for now. Just leave that blank. I don't know what that does either lol. Once you're up and running, you can go look that up.
- You should be fine ignoring the other checkboxes and fields for now. These all have great uses and value, but you can learn them as you go.

> ***I have no idea what flavor model to get!***

Google is your friend lol. I always google "reddit best 7b llm for \_\_\_\_\_" (replacing \_\_\_\_ with chat, general purpose, coding, math, etc. Trust me, folks love talking about this stuff so you'll find tons of recommendations).

Some of them are aptly named, like "CodeLlama" is self explanatory. "WizardMath". But then others like "Orca Mini" (great for general purpose), MAmmoTH (supposedly really good for math), etc are not.

> ***I have no idea what normal speeds should look like!***

For most of the programs, it should show an output on a command prompt or elsewhere with the Tokens Per Second that you are achieving (T/s). If you hardware is weak, it's not beyond reason that you might be seeing 1-2 tokens per second. If you have great hardware like a 3090, 4090, or a Mac Studio M1/M2 Ultra, then you should be seeing speeds on 13b models of at least 15-20 T/s.

If you have great hardware and small models are running at 1-2 T/s, then it's time to hit Google! Something is definitely wrong.

> ***I have no idea why my model is acting dumb!***

There are a few things that could cause this.

- You fiddled with the rope settings or changed the context size. Bad user! Go undo that until you know what they do.
- Your presets are set weird. Things like "Temperature", "Top\_K", etc. Explaining these is pretty involved, but most programs should have presets. If they do, look for things like "Deterministic" or "Divine Intellect" and try them. Those are good presets, but not for everything; I just use those to get a baseline. Check around online for more info on what presets are best for what tasks.
- Your context is too low; ie you aren't sending a lot of info to the model yet. I know this sounds really weird, but models have this funky thing where if you only send them 500 tokens or less in your prompt, they're straight up stupid. But then they slowly get better over time. [Check out this graph](https://www.reddit.com/media?url=https%3A%2F%2Fpreview.redd.it%2F2qdj7itsb39b1.png%3Fwidth%3D662%26format%3Dpng%26auto%3Dwebp%26v%3Denabled%26s%3Df9b2f044f59fbad5ad51fefacda0b61f724f12f1), where you can see that at the first couple hundred tokens the "perplexity" (which is bad. lower is better) is WAY high, then it balances out, it goes WAY high again if you go over the limit.

Anyhow, hope this gets you started! There's a lot more info out there, but perhaps with this you can at least get your feet off the ground.


## More Info

"Hey I want to try some of these models right now where can I go?"

https://huggingface.co/chat/ -> requires login, access to some of the best models, at the fastest speeds. Currently, mine shows access to 4 models. The major hub of internet modeling.

https://lite.koboldai.net/ I'm too lazy to count, looks like 15 models are currently available, they models are hosted by generous users sharing their gpu. Speed can range from instant to quite a while. Explore, this whole project is awesome.

Chat.petals.dev has 6 models to choose from with overlap with hugging face, this is a distributed network, where a model is turned into blocks and spread across helpers. This network aims for 5 tokens a second and sometimes is does and sometimes it doesn't. This is my go to option because it doesn't require a login and has access to Falcon180 and llama2-70b, without wait times.

## Even More Info

Can you explain base models vs. instruct vs chat?

How about a short discussion about llama vs. Mistral vs StableLM?



Upvote
7

Downvote

Reply
reply

Award

Share
Share

u/LearningSomeCode avatar
LearningSomeCode
OP
•
1y ago
Of course!

Llama 2 is the base model that Meta put out. They trained it themselves and released it open source for us to use. Mistral is a similar situation- a base model that was put out by a French company the other week. These base models do work on their own, as in you can load them up and talk to them, but base models are often not that impressive in terms of responses, things they do, etc.

There is a concept called "fine-tuning" where users can "train" those base models with more data. They train it with everything from more conversational dialog to programming knowledge to RPG knowledge, etc. The "flavors" I mentioned above. This makes the models much more usable, and tend to be what the rest of us are using in our day to day stuff.

The chat version of Llama-2 is just a fine-tune of the Llama-2 base done by Meta themselves as opposed to regular users; so a fine tune by the same folks who put the base out. The goal of the chat fine tune was just to make the base model easier to talk to.

https://huggingface.co/meta-llama/Llama-2-7b-chat-hf

Our fine-tuned LLMs, called Llama-2-Chat, are optimized for dialogue use cases.


I actually don't see a Llama-2 instruct, but there is an instruct fine tune of CodeLlama, the 34b coding model

https://huggingface.co/codellama/CodeLlama-34b-Instruct-hf

Same thing here- base model of CodeLlama is good at actually doing the coding, while instruct is actually good at following instructions. So for example base codellama can complete a code snippet really well, while codellama-instruct understands you better when you tell it to write that code from scratch.

---

Thanks for the guide! So I'm trying to use LM Studio. It's the first thing I downloaded and it seems more user-friendly than oobabooga, and I have some questions. I'm using GGUF 13B/30B models.

For GPU layers or n-gpu-layers or ngl (if using GGML or GGUF)-

I'm on Windows with a 3090 and lots of RAM. In LM Studio, there's a setting for n_gpu_layers that defaults to 0, but I'm not seeing a place where it tells me how many layers total there are.

Layers are determined by model and quantization method, right? So it's going to be different for every model I download?

Any way for me to find this layer info in LM Studio, or on huggingface, or somewhere else?

Set your Threads to the number of CPU cores you have. Look up your computer's processor to find out!

So we go with the number of performance cores only? I have an Intel i7-12700K, with 12 cores, 8 of which are performance cores, and 4 are efficiency cores. The product page also says it has 20 total threads. So I would go with 8, but not 12 or 20?

Set the context or ctx to whatever the max is for your model; it will likely be either 2048 or 4096 (check the readme for the model on huggingface to find out).

I'm actually not seeing this on the huggingface page for any of the several models I've downloaded. Any reliable way to find this data point?

---

Layers are determined by model and quantization method, right? So it's going to be different for every model I download?

Just model size, not quant. For example, by loading up a llama 2 13b 5_K_M into Oobabooga I can see that it has 43 layers.

llm_load_tensors: offloaded 43/43 layers to GPU

llm_load_tensors: VRAM used: 11895 MB

If I load up a 13b q8, it still has 43 layers.

llm_load_tensors: offloaded 43/43 layers to GPU

llm_load_tensors: VRAM used: 16224 MB

Since I have 24GB of VRAM on my 4090, I know that I can offload all 43 layers and have lots of room for either model.

However, a 34b 3_K_L has 51 layers, and that's getting close to my limit because windows is weird and slows down a lot if I go over 20GB lol

llm_load_tensors: offloaded 51/51 layers to GPU

llm_load_tensors: VRAM used: 19913 MB

I did google a little to see if anyone had given a list of how many layers each model has, but alas I couldn't find one. And I don't know LM Studio well enough to know where to find that info, I'm afraid. I'll try to write that out one day. I can tell you that for Llama2 models (30b is not llama2 I'm afraid) it is:

7b: 35 layers

13b: 43 layers

34b: 51 layers

70b: 83 layers


If you set your layers above the max, it'll just stop at the max. So if I load a 13b with 100 layers, it'll be 43/43.

Alternatively, if I try to load a 70b at 83 layers, it'll do it but be HORRIBLY slow. So instead I try to load the 70b with 55 layers, which brings me close to about that 20GB mark my computer is happy with. That's still slow, but less slow lol.

So we go with the number of performance cores only? I have an Intel i7-12700K, with 12 cores, 8 of which are performance cores, and 4 are efficiency cores. The product page also says it has 20 total threads. So I would go with 8, but not 12 or 20?

Personally I'd set it at 12. The performance core note was for Mac; I've never heard of anyone mention that the efficiency cores in intel are a problem. With that said, if you ever get a way to see your tokens per second that would be easy to toy with. You could try 12, run a query, reload with 8, try a query. One of those two will be a bit faster, depending on the right answer.

Ignore the number of threads they say, though; as best as I can tell, that's not the right answer. Every CPU I tried to set to the number of threads instead of cores, the results weren't great.

---

I'm actually not seeing this on the huggingface page for any of the several models I've downloaded. Any reliable way to find this data point?

If you download from TheBloke, he'll generally have it hidden in 1 of 2 spots:

He lists the original models at the top. If you can see whether the original model is listed as Llama 2 or not, you're set. If they just say "Llama" its 2048. If they say "Llama 2" it's 4096.

He often lists, somewhere, the command prompt command to load this in llamacpp or something else. That command almost always has an -ctx or -nctx or something argument with 2048 or 4096.

If both of those fail, look for the model name and find the original author to see if they list it as Llama or Llama 2