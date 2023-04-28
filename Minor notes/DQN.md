This topic was on the [[Lecture 18 Final Exam Review#Deep Learning Review]] 
Presented in [Sukthankar CAP 6671 on 2/22/2023 (Wed) (panopto.com)](https://ucf.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id=847daea8-caf4-4b11-8e8a-af8100e24a8a) at 15:57
Related reading (texbook): [[deeprl.pdf]]


# Deep RL (in general)
![[Pasted image 20230428110440.png]]
Various ways model can operate:
- predicting $V_\pi(s)$ the value of a state
- Predicting $Q_\pi(s,a)$, the Q function that takes both state and action into account
- Predicting $A_\pi(s,a)$, the *benefit* of $a\to s$, rather than the *value* of being in $s$ 

![[Pasted image 20230428110720.png]]
This is what makes deep-RL expensive: We have to generate lots and lots of examples

![[Pasted image 20230428110825.png]]



# Deep Q network
Idea: Replace the Q-table with a neural network and learn the parameters, but this presents several problems which researchers have tried to overcome.

First, there are strong correlations between samples because successor states tend to be very close to each other. This makes it difficult to learn because the updates to the NN's weights $\mathbf{W}$ all tend to have the same gradient, i.e., their updated in the same direction. The NN thus over corrects its weights, causing it to forget things it learned in the past. 

Researchers tried to overcome the strong correlation problem using **experience replay**, where replays are be saved in a **replay buffer** so they could be fed to the NN in batches. Experience replay destroys the correlation between samples, but the batch update to the target value had to be adjusted to the following, where $\mathbf{W}_{old}$ is held constant until the update is applied: 
$$\ell=\left(r+\gamma \max_{a'}Q(s',a',\mathbf{W}_{old})-Q(s,a,\mathbf{W})\right)$$
The second issue is **the problem of the moving target**. Unlike supervised learning, the target value changes every time we update $\mathbf{W}$ since our target policy is parameterized by $\mathbf{W}$. Specifically, the value of $\max_{a'}Q(s'a',\mathbf{W}_{old})$ (not necessarily the argmax, but the max value) changes each time we update $\mathbf{W}$. 

We *could* overcome the second problem by increasing our batch size (the fully-fitted Q-iteration algorithm), but this slows learning because we're updating much less frequently. So, we must strike a good compromise somewhere in between 1 gradient step and $N\gg1$ gradient steps.
![[Pasted image 20230428113607.png]]








