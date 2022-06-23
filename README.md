# CONFIGURATIONS

## 1. Vim
TODO

## 2. tmux
TODO

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
