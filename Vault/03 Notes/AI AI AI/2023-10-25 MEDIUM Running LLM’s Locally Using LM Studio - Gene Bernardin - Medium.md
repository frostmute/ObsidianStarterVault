---
url: "https://medium.com/@genebernardin/running-llms-locally-using-lm-studio-38070f286413"
title: "Running LLM’s Locally Using LM Studio - Gene Bernardin - Medium"
author:
  - "Gene Bernardin"
description: "Have you ever considered running an LLM locally on your computer? There are a few reasons you might want to consider it: 2. Model Access: running models locally, you can try some of the open source…"
tags:
  - "clippings"
  - "medium"
published: 2023-10-25
created: 2025-02-20T14:09:51-06:00
---
# Running LLM’s Locally Using LM Studio - Gene Bernardin - Medium
By Gene Bernardin
Published: 2023-10-25

![](https://miro.medium.com/v2/resize:fit:875/1*1t6Hp_HgKYpuOzxW7M8Qug.png)


Have you ever considered running an LLM locally on your computer? There are a few reasons you might want to consider it:

1\. Off-line: no internet connection required.

2\. Model Access: running models locally, you can try some of the open source models you have heard so much about (Llama 2, Vicuna, Mistral, OpenOrca, and on and on…).

3\. Privacy: when you run a model locally, no information is transferred to the cloud. Although privacy concerns have perhaps been overstated when using cloud based models like GPT-4, Bard and Claud 2, running a model locally avoids any issues whatsoever.

4\. Experimentation: if you see the value of generative AI, then you have to have an appreciation for the potential of open-source models that have been trained using different/varying strategies… and knowing what else is available.

5\. Cost: open-source models are free and some of them can be used commercially without limitations.

Now, it is true that GPT-4 is generally considered the best generative AI Chatbot, but open-source models are getting better all the time and may be just fine for many of your use cases. In the open-source category, there are many interesting contenders. There also is a lot more specialization, which makes for an interesting argument that a smaller LLM which is highly trained on a specific domain, could be more useful in those specific areas.

There has been some speculation that GPT-4 is not actually a single large LLM but rather a “Mixture of Experts” (MoE); smaller, specialized LLM’s working together. Now, OpenAI has been quiet on the “secret sauce” that is GPT-4, but it would stand to be a logical consideration, if not now, certainly for the future. Highly trained domain specific LLM’s working together as agents to provide the best possible competency across a wide range of generalization, may be the best strategy. These smaller domain specific LLM’s would be easier to update and improve (compared to updating and improving a single large LLM) and additional domain specific LLM’s could be added as needed or desired to further increase competency; provided the coordination exists to select the best LLM to respond to domain specific queries.

So… to circle back… small open-source LLM’s have their use cases for today and certainly tomorrow.

The hurdle for many has been that running a local LLM, has required a bit of computer savvy as typically it required running them inside a command prompt, or using a bit more complicated WebUI tool like Oobabooga. Enter LM Studio.

LM Studio is an open-source, free, desktop software tool that makes installing and using open-source LLM models extremely easy. Here’s how to use it:

1\. Go to “lmstudio.ai”:

2\. Download and install the version for your operating system:

![](https://miro.medium.com/v2/resize:fit:875/1*73HUG8Z9ImncCJyEqVUSCA.png)

LM Studio webpage

3\. Open LM Studio using the newly created desktop icon:

4\. Select an LLM to install. (1) You can do this by either selecting one of the community suggested models listed in the main window, or (2) by using the search bar for any model available at HuggingFace (just look up a keyword and all associated models will be listed). Note that there are currently 371,692 models listed at HuggingFace.co:

![](https://miro.medium.com/v2/resize:fit:875/1*kefDplrR81O1oXFn7kF9AQ.png)

selecting LLMs

5\. Whether you elect to download from the community suggested models, or search for one on your own, you can see the size of the install/download file. So be sure you are okay with the size of the download.

![](https://miro.medium.com/v2/resize:fit:875/1*s1Jx5NS-cRQli7t5sT8_Bw.png)

specific model information

**UPDATE: You will note that at the top of the left half of the screen over the release date column, is “compatibility guess”. LM Studio has checked your system and is presenting those models which it feels you will be able to run on your computer. To see All Models, click on “compatibility guess” (#1). Clicking on a model on the left, will present the available versions on the right and display those models which should work given your computer’s specs (#2). See image below:**

![](https://miro.medium.com/v2/resize:fit:875/1*wGZPoKBeieiY_dNqaMwsLw.png)

Compatibility and Should Work indicators

Note that depending on the capabilities/speed of your computer, larger models will be more accurate but slower. You will also find that most of these models are quantized.

A little explanation about quantization. Quantization refers to using lower precision numbers like 8-bit integers rather than 32-bit floating point values to represent the weights and activations in the model. This reduces memory usage and speeds up inference on your computer’s hardware. Quantization can reduce model accuracy slightly compared to a full precision version, but provides up to 4x memory savings and faster inference. Think of it like how MP-3’s are compressed music files or .jpgs are compressed image files. Although these are of less quality, you often won’t see a significant difference. In the case of LLM’s, the “Q” number you see in the listing of the LLM, represents the amount of quantization. Lower is more and higher is less quantization.

Also, in the model listing, you will see references to GGML and GGUF. Don’t worry about it. These are two quantization strategies; “Mixed Logits” vs “Uniformly Quantized Fully Connected”. GGML provides a more flexible mixed-precision quantization framework while GGUF is specifically optimized for uniformly quantizing all layers of Transformer models. GGML may enable higher compression rates but GGUF offers simpler deployment.

Yeah… I don’t understand either. “Mileage may very”… pick one and don’t be put off by the technical stuff.

6\. Once the model has finished its download, (1) select the model from the drop-down menu at the top of the window; (2) select the chat bubble in the left side column; (3) open up the following sections on the right, “Context Overflow Policy” and “Chat Appearance”.

![](https://miro.medium.com/v2/resize:fit:875/1*I8zEteuvavMP2NseazTnuw.png)

ready the model

7\. Make sure “Maintain a rolling window and truncate past messages” is selected under “Content Overflow Policy” and “Plaintext” is selected under “Chat Appearance”.

![](https://miro.medium.com/v2/resize:fit:875/1*Vgf2jMnBk-f70Wr603i5kg.png)

8\. Now close those two areas and open up “Model Configuration” and then open “Prompt Format” and scroll down to “Pre-prompt / System prompt” and select the “>” symbol to open that. Here you can enter the system “role”. Meaning, you can set up how you want the bot to act and what “skills” or other specific qualities should be provided in its answers. You can modify what is there to suit your needs. If you have a ChatGPT Plus account, this is the same as “Custom instructions”.

![](https://miro.medium.com/v2/resize:fit:875/1*ivsHBDL61HQGBBtdhIzLMw.png)

![](https://miro.medium.com/v2/resize:fit:875/1*Lxt4PKxVaIXSFq0Q68KlmQ.png)

adding system role / custom instructions

9\. Continue to scroll down in this column until you come to “Hardware Settings”. Open this area if you wish to offload some processing to your GPU. The default is to allow your computer’s CPU to do all the work, but if you have a GPU installed, you will see it listed here. If you find the processing of your queries is annoyingly slow, offloading to your GPU will greatly assist with this. Play around with how many layers you want it to handle (start with 10–20). This really depends on the model and your GPU. Leaving it all to be handled by the CPU is fine but the model might run a bit slow (again… depending on the model and its size). You also have the option to increase the number of CPU threads the LLM uses. The default is 4 but you can increase the number, or just leave it where it is if you don’t feel comfortable experimenting and don’t know how many threads your CPU has to play with.

![](https://miro.medium.com/v2/resize:fit:875/1*hdompSU_UoLOwwmQJ9au2A.png)

optional hardware settings

10\. After these changes, you are now ready to use your local LLM. Simply enter your query in the “USER” field and the LLM will respond as “AI”.

![](https://miro.medium.com/v2/resize:fit:875/1*indXZpC6tCN7GbO8SJQK9A.png)

chat dialogue

HAVE FUN!