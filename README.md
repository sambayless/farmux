# farmux
Utility for launching jobs on remote machines, in fresh tmux sessions. Optionally copies the command binary to the host (if a full path is specified).

Usage: 
```
$farm user@host my_command arg1 arg2 ...
```
For example, 

```
$farm user@host echo "Hello Farm"
```

A default host can be configured, in which case usage is as simple as:
```
$farm echo "Hello Farm" ...
```
If ```my_command``` is an executable specified with a relative or absolute path (eg, ```farm ./my_command arg1 arg2```), then the binary will be copied to a temporary location on the remote machine before the command is executed. So long as the architectures/environments of the two machines match, this allows for locally compiled commands to be rapidly tested on the remote machine.

