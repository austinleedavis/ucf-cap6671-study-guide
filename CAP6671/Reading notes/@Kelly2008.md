---
title: Offline planning with hierarchical task networks in video games
authors: John-Paul Kelly, Adi Botea, Sven Koenig
year: 2008
note: week02
pdffile:: [[AIIDE08-010.pdf]]
---

Discussed in [Sukthankar CAP 6671 on 1/25/2023](https://ucf.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id=2d65ec97-5a87-452a-acf9-af8100e2498d) at 38:58
Will be on the [[Lecture 18 Final Exam Review#Planning]]
Original file is available at [[AIIDE08-010.pdf]]

# Abstract  

Artificial intelligence (AI) technology can have a dramatic impact on the quality of video games. AI planning techniques are useful in a wide range of game components, including modules that control the behavior of fully autonomous units. However, planning is computationally expensive, and the CPU and memory resources available to game AI modules at runtime are scarce. Offline planning can be a good strategy to avoid runtime performance bottlenecks. In this work, we apply hierarchical task network (HTN) planning to video games. We describe a system that computes plans offline and then represents them as game scripts. This can be seen as a form of generating game scripts automatically, replacing the traditional approach of composing them by hand. We apply our ideas to the commercial game THE ELDER SCROLLS IV: OBLIVION, with encouraging results. Our system generates scripts automatically at a level of complexity that would require a great human effort to achieve

# Summary

Introduces #HTN 
System generates NPC scripts at a level of complexity that would require "great human effort to achieve." 
Whereas SCRIPTEASE focuses on Software engineering (the closest thing to this work) makes no attempt at automating the planninng side of scripting. 
Evals: **linear growth in # NPCs and duration**


# Gita's take
Instead of letting the human planner chain together actions, the programmer is going to write (partially filled out) **recipes** for how certain tasks should be achieved. *Example*: To get to UCF each day, you don't have to think about it, unless there's an unforeseen circumstance.
