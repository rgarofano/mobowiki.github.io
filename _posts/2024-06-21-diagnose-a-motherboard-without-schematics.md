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

Assuming the visual inspection did not provide you with any clues, it's time to put on your detective hat and bring out the multimeter probes. Ensure the charger is plugged into the board, then perform a voltage measurement on the pins of the DC jack. One of the pins should be reading ~19 V - if not then you are dealing with a faulty DC jack. In order for the device to function, voltage has to be delivered to all the different chips and components on the board. Different parts of the board require different levels of voltage. Therefore, the ~19 V on the charger is source for everything, it needs to be distributed all over the board and stepped down along the way. For now, the best course of action is to try and follow the charger voltage for as long as we can.
