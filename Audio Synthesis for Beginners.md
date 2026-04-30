---
title: Audio Synthesis for Beginners
tags:
  - music
  - vst
maturity: seed
plantedDate: 2026-04-30
tendedDate: 2026-04-30
---
# Introduction
I have been interested in audio synthesis for a while, and I understand a bit of the high level stuff, so I thought it would be fun to delve into building my own VST. There are a few major different types of audio synthesis (making sounds) so I want to create a basic, educational VST to introduce people to a few of them.

The only issue is, I need to learn how to make a VST, and I need to learn the key differences between all the types! So this will be my discovery, and learnings as I go. If you want the VST, that will be at the end (if it ever gets finished/released - *spoiler not yet unless I forgot to update this bit*).

For context, I'm not coming at this from nowhere, I own a couple of basic synths, including my first synth, the ARGON8X (digital polyphonic wavetable) and my latest addition, the adorable, Moog Mother 32 (subtractive analogue - see below). I love them both, but want to learn a bit more about what makes them tick!

![[Pasted image 20260430173822.png|500]]

# What is Audio Synthesis
Audio synthesis is what I'm using as the umbrella term for any method of making and shaping sound. That includes additive synths, FM synths, and many more which I'm sure I'll learn as I go. It importantly *doesn't* include sampling/recording sounds to play them back.

The 2 above I'm more closely aware of, but there are various other synthesis techniques (to name a few) include:
- Additive
- Subtractive
- Wavetable
- FM (Frequency Modulation) Synthesis
- Granular

I'm going to attempt to explain each of these as I go, and include as much as possible in my theoretical VST attempt! Let's start at the beginning...

## Subtractive Synthesis
Subtractive synthesis is possibly the easiest to grasp, and is the one you may be most familiar with. It was pioneered by Moog in the 1960s/1970s.

You start with a simple wave and, you guessed it, start to subtract from that audio signal until you get the sound that you want. There are a few key parts therefore to make a complete subtractive synthesizer.

### The Oscillator
The oscillator is the starting point, and the wave that we will be adjusting as we pass through the synthesizer. It's important to start with something considered here, as since we're *subtracting* as we go, we need to make sure we have all the frequencies from the start. This oscillator can be anything though; sin, saw, triangle, square or anything else. Traditionally these were the easy waves to produce electronically, but in modern synthesizer the oscillator can be anything as complex as you'd like.

### The Filter
Once we have a sound to work with, its time to start subtracting bits from it. The most fundamental part of a subtractive synth is arguably the filter. This affects the shape of the sound and decides which frequencies make it to the final sound. The most common type of filter you will encounter is a 'low-pass' filter, as well as sometimes a 'high-pass' filter. These are exact opposites of each other, with the low pass letting *low frequencies pass*, whereas the high pass, only keeps the high frequencies. We will focus on a low pass as the primary use case.


![[Pasted image 20260430175650.png|550]]