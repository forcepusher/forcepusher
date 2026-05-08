Projects done with the help of AI (Average Intelligence) tools have "Sloppy" in their name, while others never used it.  
Don't get me wrong, AI is a great tool to get stuff done fast, but it's dum as hell and have to be carefully guided.  
Some people [compare it to a parrot](https://www.youtube.com/watch?v=p22QeLNHvlc) with a gigantic brain. It's still just a parrot though.  
  
Current Transformers LLM architecture is basically T9 text prediction from old phones, and models are dictionaries.  
Repeatedly tap on your phone's text predictions - this is the current state of AI. We need "Conception-Text" models.  
But autocomplete was always a good tool anyway. Now with proper expectations you're ready to start building.  
  
Oh, BTW. Stop using cloud AI services, start with your own local LMStudio/ComfyUI machine. Save monies.  
You need 16+ GB VRAM on Nvidia card (preferably 24GB), 48+ GB RAM (pref 64GB), and any half-decent CPU.  
3 weeks of pure suffering and you're ready for a true/actual AI future, it'll pay off in less than a year.  
Our videocards now can not only run games, but write somewhat useful code. That's pretty cool right?  
  
And if part of your job or pipeline can actually be replaced by a parrot - maybe it should be replaced.  
Think of writing and updating tests. Lovely part of our job, ain't it?  

---
  
Useful models I've found so far that have any idea what they're doing and not dying while working:  
gemma-4-31b@q4_k_m (for 24GB GPU, a bit schizo but very reliable, also heavy - needs Q8_0 KV Cache)  
gemma-4-26b-a4b@q6_k (for 16GB GPU to run partially on CPU, cheapest starter option)  
  
Models less than 26B are completely useless, don't hold your hopes high.  
Mixture Of Experts (A4B, A3B) are useless too unless you're running them partially on CPU, have to use at least Q6_K.  
  
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
