---
title: Massive cross-platform simulations of online social networks
authors: Goran Murić, Alexey Tregubov, Jim Blythe, Andrés Abeliuk, Divya Choudhary, Kristina Lerman, Emilio Ferrara
year: 2020
note: week11
pdffile:: [[muric2020.pdf]]
---




Given a large quantity of data on GitHub, Redit, Twitter, try to predict what woudl happen in the future.
There were 7 teams competing. This paper was from Univ. S. Calif. Starting at programmers interacting with each other on GitHub.

Given 26 months of data, predict 2 months in the future. 

![[Pasted image 20230419182048.png]]
![[Pasted image 20230419182102.png]]
Goal was to measure difference between Sim Count vs Truth Count (i.e., number of stars/watches/retweets/etc)

![[Pasted image 20230419182146.png]]
These agents were programmed in Netlogo, and combined using evolutionary model discovery
![[Pasted image 20230419182223.png]]
USC modeled information cascades
![[Pasted image 20230419182253.png]]
UCF's team recognized that you can cluster user (archetypical users) Aim to build a simpler model tuned on the data.
![[Pasted image 20230419182346.png]]
UCF used k-means clustering, low-pass filter on users 1w/ low activity and filtered bots

![[Pasted image 20230419182434.png]]
Goal was to perform **stable clustering** across different months.

UCF: The archetypes were then programmed in Netlogo. 

Ivon garabay, Industrial Engineer
Steve IST