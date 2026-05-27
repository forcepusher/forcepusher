Projects done with the help of Average Intelligence tools have "Sloppy" in their name. Others never touched.  
  
Of course "AI" is a great to get stuff done fast, but it's quite dumb and have to be very carefully guided.  
Some people [compare it to a parrot](https://www.youtube.com/watch?v=p22QeLNHvlc) facerolling on the keyboard.  
  
LLM is not even a neural network, it's an autocomplete dictionary for T9 text predictions just like in old phones.  
Repeatedly tap on your phone's text predictions - this is the current state of "AI".  
Now with proper expectations you're ready to start building.  
  
Oh, BTW. If you don't want to feed money to cloud services - start with your own local LMStudio/ComfyUI machine.  
All you need is 16GB VRAM GPU and 32GB RAM to start, CPU doesn't matter. It's really that cheap.  
Setup takes 3 weeks of pure suffering and you're ready for a true AI future, it'll pay off in less than a year.  
Our videocards now can not only run games, but write somewhat useful code. That's pretty cool right?  
  
And if part of your job or pipeline can actually be replaced by a parrot, maybe it should be replaced.  
Think of writing and updating tests. If you're blank-staring at the wall right now, you get it.  
Don't let LLMs think for you or build an architecture - it's all harmful random garbage.  
  
---
  
### Cookbook (reliable agentic models I've found for programming so far):
24GB GPU VRAM + 64GB RAM (comfortable):  
[**Robot**](https://huggingface.co/unsloth/Qwen3.6-27B-GGUF/tree/main) 80k (x4 parallel) - unsloth/qwen3.6-27b@q5_k_xl (Q8_0 KV Cache, temp 0.6, top k 20, min p 0)  
[**Wasserman**](https://huggingface.co/unsloth/gemma-4-31B-it-GGUF/tree/main) 48k (x2 parallel) - unsloth/gemma-4-31b-it@iq4_xs (temperature 0.3, top k 64, min p 0.05)  
[**Pentester**](https://huggingface.co/mradermacher/XORTRON.CriminalComputing.2026.27B.Instruct.NEXT-GGUF/tree/main) 64k (x2 parallel) - xortron.criminalcomputing.2026.27b.next@q5_k_m (temp 0.6, top k 20, min p 0)  
  
16GB GPU VRAM + 32GB RAM (starter):  
[**Local Robot**](https://huggingface.co/unsloth/Qwen3.6-27B-GGUF/tree/main) 40k - unsloth/qwen3.6-27b@q5_k_xl (Q8_0 KV Cache, temperature 0.6, top k 20, min p 0)  
[**Local Pentester**](https://huggingface.co/mradermacher/XORTRON.CriminalComputing.2026.27B.Instruct.NEXT-i1-GGUF/tree/main) 32k - xortron.criminalcomputing.2026.27b.next@iq3_xs (1 layer on CPU, temp 0.6, top k 20, min p 0)  
  
Global settings: Repetition Penalty disabled, Top P Sampling 0.95.  
This is [how the settings work](https://www.youtube.com/watch?v=_3DWwb96exY) (yeah I know, exactly the way we like it).  
  
If you can get anything done on 16GB GPU VRAM models, you should invest in RTX 3090 or a multi-GPU setup.  
Every 8GB extra VRAM is an astronomic leap in quality. 16GB models are not even close to 24GB models.  
  
Use OpenAI-compatible API to connect to LM Studio. The https://zed.dev/ seems to be best open-source agentic IDE.  
Here are [jinja templates](https://github.com/forcepusher/jinja-templates-lmstudio-zed) for LM Studio and Zed. Very tedious to get right.  
Put `Responses MUST be terse and short.` in a rule or system prompt, or use my [portable caveman](https://github.com/forcepusher/smol-caveman) prompt.  
Vision consumes a lot. Use Q8_0 or BF16 .mmproj files so you don't have to blind the model completely.  
  
I use low temperature of 0.3 to prevent tool use typos/screwups, but top k 40 to mitigate reasoning quality hit.  
To avoid Gemma 4 thinking bugs, use "<|channel>" as your reasoning start string, not "<|channel>thought".  
All models should use 8k output token limit to prevent occasional very long useless loops when it fails a tool call.  
Avoid Q8_0 KV Cache. On most models It kills the tool calls because it introduces typos, and lobotomize reasoning.  
Always disable Unified KV Cache and set Max Concurrent Prediction to 1, unless model is intended to work in parallel.  
  
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
