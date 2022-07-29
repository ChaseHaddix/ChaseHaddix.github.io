---
title: 'What is EEG?'
date: 2021-09-10
permalink: /posts/2021/09/blog-post-3/
tags:
  - EEG

---

You may have seen those headcaps with dozens of wires coming from them on TV or in a hospital. But what's going on? 

Electroencephalography (EEG)
------

What is it?
======

  EEG is a way to measure the very tiny changes in the electric field surround your brain. Electrodes, or small pieces of conductive material such as metal, are placed on the scalp and these changes are picked up and carried down wires to be processed. To accept this, you first must understand why there is an electric field associated with your brain. Physiological processes (especially in your brain) involve the movement of ions from cell to cell. The best example of this is a neuron firing. Every time an action potential races down a neuron, a tiny electric field surrounds that neuron. For an incredibly thorough review of this topic, I suggest the popular book ["Electric Fields of the Brain" by Nunez & Srinivasan](https://brainmaster.com/software/pubs/brain/Nunez%202ed.pdf)

![Neuron Graphic!](/images/NeuronFiringGraphic.jpg)

  Now, one little neuron can't be detected all the way at the scalp. But what if a bunch fire at the same time? A real-world analogy: Imagine you are late to a concert or sporting event. As you walk up to the stadium, it doesn't sound very loud. But then you hear the roar of applause. Did you just miss something good? One person clapping may not be detectable, but if hundreds or thousands clap at the same time you certainly notice. 

  In the brain, the primary generators of EEG are known as pyramidal neurons. These neurons (when firing in unison) are detectable with EEG for a couple of reasons. First, they are located in the cortex, the outer layer of the brain. So the relatively weak electric fields don't have to travel far to reach the electrode on the scalp. Second, they are oriented perpendicular to the brain's surface. This maximizes the summation of their firings. If they were oriented randomly, their contributions may cancel each other out. These types of cells, with a pyramidal cell body owing to its name, were popularized by neuroscience pioneer Santiago Ramon y Cajal. Below is his drawing of one from 1904. Nearly two decades later, in 1924, Hans Berger invented EEG. 

![RamonyCajal!](/images/RamonYCajal.jpg)

How does it work?
======
  The units of EEG measurement are in Volts. As with any voltage measurement, the potential difference is between a recording electrode and a reference electrode. Importantly, EEG is measured between two electrodes. Often times, the reference electrode is either on the forehead (thick skull) or ear lobe (far from brain). EEG leads feed into an amplifier, where the tiny voltages, usually on the nano-volt scale, are amplified before being converted from an analog signal (continuous) into a digital signal (discrete). Sample rates for EEG vary depending on application. The higher the rate, the closer you are to the analog/original signal. But at some costs, including a large amount of data to save. Typically, each EEG electrode/channel is saved at 125 to 1000 Hz, or samples per second. 
  
  Since an electrode is only able to pick up activity over a small part of the brain, dozens or even hundreds of electrodes are needed to tell the whole story about what is going on in the brain, or at least the cortical outer layer. 


Let's Recap 
======

  * Among the oldest brain imaging techniques 
      * Nearly 100 years old!
  * EEG is non-invasive
      * Doesn't hurt
      * Doesn't require surgery
  * Considered inexpensive (after you buy all the equipment)
  * Able to detect activity across the whole brain
  * Poor quality signal
      * Susceptible to artifacts like muscle and head motion
  * Great temporal resolution
      * Can sample hundreds or thousands of times per second
  * Poor spatial resolution
      * Each EEG channel reflects activity of thousands or millions of neurons
  * Researchers describe EEG according to rhythms or waves
      * Alpha rhythm is the most common, prominent when you close your eyes
    
