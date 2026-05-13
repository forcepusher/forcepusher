Projects done with the help of AI (Average Intelligence) tools have "Sloppy" in their name, while others never used it.  
  
Don't get me wrong, AI is a great tool to get stuff done fast, but it's dum as hell and have to be carefully guided.  
Some people [compare it to a parrot](https://www.youtube.com/watch?v=p22QeLNHvlc) with a gigantic brain. But it's still just a parrot facerolling on the keyboard.  
Current Transformers LLM architecture is basically T9 text prediction from old phones, and models are dictionaries.  
Repeatedly tap on your phone's text predictions - this is the current state of AI. We need "Conception-Text" models.  
Though autocomplete was always a good tool anyway. Now with proper expectations you're ready to start building.  
  
Oh, BTW. Stop using cloud AI services, start with your own local LMStudio/ComfyUI machine. Save monies.  
You need 16+ GB VRAM on Nvidia card (preferably 24-32GB), 32+ GB RAM (pref 64-128GB), any half-decent CPU.  
3 weeks of pure suffering and you're ready for a true/actual AI future, it'll pay off in less than a year.  
Our videocards now can not only run games, but write somewhat useful code. That's pretty cool right?  
  
And if part of your job or pipeline can actually be replaced by a parrot - maybe it should be replaced.  
Think of writing and updating tests. If you're blank-staring at the wall right now, you get it.  

---
  
### Cookbook (essential models I've found for programming so far):
**Wasserman** 32k - unsloth/gemma-4-31b-it@iq4_nl (for 24GB GPU, very heavy and reliable, use temperature 1.0)  
**Drunk Wasserman** 96k - unsloth/gemma-4-31b-it@q2_k_xl (for 24GB GPU, same as above for bigger context window)  
**Pentester** 64k - xortron.criminalcomputing.2026.27b.next@q5_k_m (Qwen3.5 for 24GB GPU, use temperature 0.6)  
**Crackhead** 232k/48k - google/gemma-4-26b-a4b@q4_k_m (for 16GB GPU + 32GB RAM, starter option, temp 0.7)  
  
On 16GB VRAM card you will have 48k context window while computing 8 layers on CPU, and it's still a Crackhead model. It's basically for testing before buying hardware for fat models.  
  
Models less than 26B are absolutely useless, don't hold your hopes high.  
Put `Be short and terse. Subject, next step.` in a rule or system prompt, or use my [portable caveman](https://github.com/forcepusher/smol-caveman) prompt.  
Quantize your vision .mmproj files to Q8_0 so you don't have to blind the model completely.  
Don't use uncensored/abliterated crap, every single bit of KL divergence makes a huge difference.  
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
