# Play it Yourself sequencer

Sequencer for a Yamaha Disklavier for usage with the node.js app "Play it Yourself".

I'm running [PatchBox OS](https://blokas.io/patchbox-os/), which comes pre-installed with Pure Data and all that jazz.

Also good to have is `tmux`.

## Starting Pd on a Rasbperry pi with SSH

Although the patch can be run with the GUI, the way this has been presented is with the patch running on a Rasberry Pi. Due to having to SSH into the Pi, I have had to run Pd without the GUI. You then have to specify what MIDI Out port you're gonna use, like this:

```
$ ssh <user-name>$<ip-for-raspberry-pi>
$ tmux
$ pd -nogui -midioutdev "1" mastersequencer.pd
```

Where the 1 after `-midioutdev` is the index of MIDI Out ports you're gonna use.

Then you can simply type `C-b d` in the tmux/ssh session to detach from tmux, and safely log off from the pi without it stopping the PD patch.
