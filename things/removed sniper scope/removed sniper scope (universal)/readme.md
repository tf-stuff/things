<b>if you use a hud, do NOT download the file above, and do the steps below.<br>
if you *dont* use a hud, add the last command (`alias remove_scope...`) and download the file above and put it into custom.<br></b>
first, go into your huds scripts folder to find its hudanimations. then copy and paste the text below somewhere in it

```
event ScopeRemoval
{
    Animate HudScope Position "9999 9999" Linear 0.0 0.0
}
```

then, search the file for the "damagedplayer" event, and replace it with this:

```
event DamagedPlayer
{
	RunEvent ScopeRemoval 0.0
}
```

then go to your autoexec and paste in this:

```
alias remove_scope "sv_cheats 1; testhudanim scoperemoval"
remove_scope
```
