---
title: Audio Synthesis for Beginners
tags:
  - music
  - vst
maturity: seed
plantedDate: 2026-04-30
tendedDate: 2026-04-30
---
I have been interested in audio synthesis for a while, and I understand a bit of the high level stuff, so I thought it would be fun to delve into building my own VST. There are a few major different types of audio synthesis (making sounds) so I want to create a basic, educational VST to introduce people to a few of them.

The only issue is, I need to learn how to make a VST, and I need to learn the key differences between all the types! So this will be my discovery, and learnings as I go. If you want the VST, that will be at the end (if it ever gets finished/released - spoiler not yet unless I forgot to update this bit).
# What is Audio Synthesis
Audio synthesis is what I'm using as the umbrella term for any method of making sound. That includes additive synths, FM synths, and many more which I'm sure I'll learn as I go. It importantly *doesn't* include sampling/recording sounds to play them back.

The 2 above I'm more closely aware of, but there are various other synthesis techniques (to name a few) include:
- Additive
- Subtractive
- Wavetable
- FM (Frequency Modulation) Synthesis
- Granular

I'm going to attempt to explain each of these as I go, and include as much as possible in my theoretical VST attempt! Let's start at the beginning...

## Subtractive Synthesis
