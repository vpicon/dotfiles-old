# Personal Configuration Files
This repository contains the personal configuration files for my PC 
environments.

## 1. Vim
Basically, some quality of life, tabs as spaces and using some plugins with 
[vim-plug](https://github.com/junegunn/vim-plug).

TODO: Future check and move to use neovim.

## 2. tmux
Configuration for lower status bar, change colorings to match Gruvbox color, 
and map the hotkey to Ctrl+A.

## 3. Extra Fixes
### 3.1 Slow Mouse Cursor on Ubuntu
Solution as by [this page](http://carlocapocasa.com/crushing-the-kworker-uprising-or-how-to-fix-your-linux-lenovo-ideapad-y560p/).
The problem is with ACPI GPE's interrupt values. Check them by running the command:

```bash
$ grep enabled /sys/firmware/acpi/interrupts/* 
```

The resulting GPE with a clear high number (than others, for example 200) is 
the problem. To disable it, just type

```bash
echo "disable" > /sys/firmware/acpi/interrupts/gpeXX (XX is the number of your gpe)
```

TODO: Then add a crontab entry to fix it at reboot time. 

## 4. Win
Maybe one does take bad decisions in life which leads him to use windows. 
Just contains key mappings (CapsLock to Ctrl).
