---
layout: post
title: "How to Diagnose a Motherboard Without Schematics"
categories: posts
---

## Introduction

Schematics are an immensely helpful resource when trying to find one or more faulty components on a motherboard. Unfortunately, schematics are not publicly available for many boards. This means that if you want to get good at fixing motherboards, doing so without the use of schematics is an essential skill. This page is my attempt at a comprehensive guide for doing just that. For the moment, this is a work in progress which I will be updating periodically.

## Preface

Diagnosing a motherboard takes time and patience. It's important that before you begin this process, you are certain that there is a fault on the motherboard. I will assume for brevity sake that you have already gone through the process of isolating the issue or are reading this out of curiosity. In this guide, we will be focused on a typical no power situation. This means no fan spin or any other sign of life when pressing the power button.

### Spot the Obvious

Always start with a [visual inspection](visual-inspection.html) of the board. This can save you time by identifying obvious issues which narrows down the problem space. In some cases you may find that the damage is too extensive for a repair to be economical. As you gain more experience, you'll get faster at inspecting the board and be able to identify key issues early in the troubleshooting process.

### Start at the Source

Assuming the visual inspection did not provide you with any clues, it's time to put on your detective hat and bring out the [multimeter](/misc/2024/06/22/recommended-tools.html) probes. Ensure the charger is plugged into the board, then perform a voltage measurement on the pins of the DC jack. One of the pins should be reading around 18-20 V - if not then you could be dealing with a faulty DC jack. In order for the device to function, voltage has to be delivered to all the different chips and components on the board. You can think of a motherboard as a collection of sub-systems that work together to power and control all the different parts of your computer. These sub-systems each require different levels of voltage. For example, the backlight circuit might require 40 V to light up the screen of a laptop whereas the CPU could be fried if more than 1 V was sent to it. All of these different voltage levels and the role they play are classified as "power rails". In any case, the voltage levels we see in these different sub-systems all derived from the "main power rail" which is code for the voltage that comes directly from the charger.
