# Play it Yourself sequencer

Sequencer for a Yamaha Disklavier for usage with the node.js app "Play it Yourself".

## Starting Pd on a Rasbperry pi

Although the patch can be run with the GUI, the way this has been presented is with the patch running on a Rasberry Pi. Due to having to SSH into the Pi, I have had to run Pd without the GUI. You then have to specify what MIDI Out port you're gonna use, like this:

```
$ pd -nogui -midioutdev "1" mastersequencer.pd
```

Where the 1 after `-midioutdev` is the index of MIDI Out ports you're gonna use.
