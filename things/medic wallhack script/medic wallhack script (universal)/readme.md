add 

```
// Teammate 'Wallhack' Script - Press to show all teammates for a few seconds (helpful if you're lost)
hud_medicautocallers 1
alias autocall_default "hud_medicautocallersthreshold 50" // Change "50" to whatever health percentage you want teammates to auto-callout on normally
alias autocall_all     "hud_medicautocallersthreshold 150"
alias +radar "autocall_all"
alias -radar "autocall_default"
autocall_default
bind key +radar // Change "key" to whatever key you want this script bound to
```

to your autoexec, and look at the comments so you can replace things as needed.