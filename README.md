# Harmonic Entropy Exploration in Python

***What is harmonic entropy?***

It's well documented on the Xenharmonic wiki.

There is a certain tolerance for frequency difference -- if two frequencies are close enough, then to human ears they should be equivalent.
Maybe we could define this as: at least close enough so that their "beat" frequency is no faster than 1 Hz.  Probably need to investigate / play around with this idea further.


### Idea for optimal harmonic control based on entropy


1) Define a multi-valued time series of fundamental frequencies (a.k.a. "sine wave music").
  Each frequency corresponds to an oscillator to which we later add a certain overtone series.
2) Choose a set of discrete intervals over which to do the harmonic analysis and optimization.
  *Aside* It may be possible to do a continuous-time optimization -- i.e. continuous optimal control.
4) Apply perturbations to each fundamental's harmonic series -- i.e. perturb the oscillator shape
  
  ***PROBLEM***
  Adjusting the overtones in the harmonic series -- even a tiny amount -- really sound pretty awful.

4) For each interval (for which the fundamentals may have different harmonic relationships) apply
  a set of optimization criteria to adjust the oscillator shapes so that the overtone series'
  *This is the hard part.*  There are many optimization goals that could be implemented here.
  Here are some ideas:
  
  - penalize non-decaying overtone series
  - penalize distance from original perturbed values
  - penalize harmonic entropy


