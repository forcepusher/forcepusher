Projects in my repos done with the help of "AI" (Average Intelligence) tools have "Sloppy" in their name.  
  
"AI" is a great to get stuff done fast, but it's dum as hell and have to be very carefully guided.  
Some people [compare it to a parrot](https://www.youtube.com/watch?v=p22QeLNHvlc) with a gigantic memory facerolling on the keyboard.  
  
LLM is not even a neural network, it's an autocomplete dictionary for T9 text predictions just like in old phones.  
Repeatedly tap on your phone's text predictions - this is the current state of "AI".  
Now with proper expectations you're ready to start building.  
  
Oh, BTW. Stop using cloud services, start with your own local LMStudio/ComfyUI machine. Save monies.  
You need 16+ GB VRAM on Nvidia card (preferably 24-32GB), 32+ GB RAM (pref 64 or 128GB), any half-decent CPU.  
3 weeks of pure suffering and you're ready for a true AI future, it'll pay off in less than a year.  
Our videocards now can not only run games, but write somewhat useful code. That's pretty cool right?  
  
And if part of your job or pipeline can actually be replaced by a parrot, maybe it should be replaced.  
Think of writing and updating tests. If you're blank-staring at the wall right now, you get it.  
Don't let LLMs think for you or build an architecture - it's all harmful random garbage.  
  
---
  
### Cookbook (essential models I've found for programming so far):
24GB GPU + 64 or 128GB RAM:  
**Wasserman** 56k - unsloth/gemma-4-31b-it@iq4_xs (heavy and reliable, temperature 0.3, top k 64)  
**Pentester** 64k - xortron.criminalcomputing.2026.27b.next@q5_k_m (qwen3.5 finetune, temperature 0.3, top k 40)  
**Crackhead** 64k - unsloth/gemma-4-26b-a4b-it@q5_k_s (schizo and fast as hell, temperature 0.3, top k 64)  
  
16GB GPU + 32GB RAM:  
**Local Pentester** 40k - xortron.criminalcomputing.2026.27b.next@iq3_xs (full GPU compute, temperature 0.3, top k 40)  
**Local Crackhead** 48k - unsloth/gemma-4-26b-a4b-it@iq4_nl (compute 2 layers on CPU, temperature 0.3, top k 64)  
  
If you can get anything done on 16GB GPU models, you should probably invest in RTX 3090 or go straight to 5090.  
  
Use "<|channel>" as your thought start string for Gemma 4, not "<|channel>thought" to avoid bugs.  
I use low temperature to prevent tool use typos/screwups, it's a very common problem.  
All models should use 8k output token limit, except gemma-4-26b-a4b that actually needs 16k for schizo reasoning.  
Put `Responses MUST be terse and short.` in a rule or use my [portable caveman](https://github.com/forcepusher/smol-caveman) prompt.  
Quantize your vision .mmproj files to Q8_0 so you don't have to blind the model completely.  
Don't use uncensored/abliterated crap, every bit of KL divergence makes a huge difference.  
Never use Q8_0 KV Cache, it kills the tool calls because it introduces typos and lobotomizes the model.  
When short on memory, always disable Unified KV Cache and set Max Concurrent Prediction to 1.  
Use OpenAI-compatible API to connect to LM Studio. Best open-source agentic IDE atm seems to be https://zed.dev/  
Here are [jinja templates](https://github.com/forcepusher/jinja-templates-lmstudio-zed) for LM Studio and Zed. Very tedious to get right.  
  
---
  
### More Unity packages:  
- [com.bananaparty.touchinput](https://github.com/forcepusher/com.bananaparty.touchinput)  
- [com.bananaparty.websocketclient](https://github.com/forcepusher/com.bananaparty.websocketclient)  
  
### ComfyUI nodes:  
- [ComfyUI-Enhancement-Utils](https://github.com/forcepusher/ComfyUI-Enhancement-Utils) - PC resource monitor and execution follower  
- [ComfyUI-SloppyAudio](https://github.com/forcepusher/ComfyUI-SloppyAudio) - Audio editing tools based on SoX and BS-RoFormer  
  
### Other instruments:  
- [smol-caveman](https://github.com/forcepusher/smol-caveman) - Portable Caveman prompt designed for local LLMs. Read less slop and get much better results. 
- [ComfyUI-SloppyInstall.bat](https://gist.github.com/forcepusher/4bc79cce87f3cbda21872ea6ee1936cf) - Simplified pip install -r "requirements.txt" for custom nodes in portable ComfyUI.  
- [SloppyServer.bat](https://gist.github.com/forcepusher/4c4cf4a8d9e390e4f224f4f31c348672) - Single file local/Wi-Fi server for debugging multithreaded mobile Unity WebGL builds and other apps  

### Technical articles (No AI tool ever touched this holy grail):  
- [How to OOP (Russian)](https://github.com/forcepusher/Obsidian/blob/master/Arch/com.bananaparty.arch.docs.ru.md)  
- [How to OOP (English auto-translate)](https://github-com.translate.goog/forcepusher/Obsidian/blob/master/Arch/com.bananaparty.arch.docs.ru.md?_x_tr_sl=ru&_x_tr_tl=en&_x_tr_hl=en&_x_tr_pto=wapp)
