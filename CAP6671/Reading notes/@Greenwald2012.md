---
title: Bidding under uncertainty: Theory and experiments
authors: Amy Greenwald, Justin Boyan
year: 2004
note: week04
pdffile:: [[greenwald04bidding.pdf]]
---

Referenced in [[Lecture 18 Final Exam Review#Trading Agent Competition]]
Discussed in [Sukthankar CAP 6671 on 2/1/2023 (Wed) (panopto.com)](https://ucf.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id=98c32ed3-2ba8-4378-be4d-af8100e249eb) at 44:48

# Combinatorial Valuations
Challenge: The value of something is not independent of others. This can be affected in two specific ways:

- Complements: "The whole is greater than the sum of its parts." 
	- Some packages **complement** each other:
		- Ex: Having hotel on all nights 1 through 3 is better than having to go to a new hotel each day.
	- formally: $value(X\overline{Y})+value(\overline{Y}X)\leq value(XY)$
	- Example: Having a tripod and flash without a camera is useless
- Substitutes: Multiple copies of a similar thing is not as valuable:
	- Some packages can be **substituted**:
		- ex: Having an expensive hotel on night 1 AND a cheap hotel on night 1 makes us unhappy because we can't stay in both places on the same night.
	- formally: $value(X\overline{Y})+value(\overline{Y}X)\geq value(XY)$
	- Example: Given that we already have camera $X$, we gain very little additional value from also having camera $Y$, and vice versa. It's better to have one or the other, rather than both. So, camera $X$ can be *substituted* for camera $Y$.

## Marginal Utility (MU)
Combinatorial valuation leads us to use a MU mechanism to determine whether it's worth bidding on a new object.
- Definition: **Marginal Utility** is the difference between the utility of owning the set plus the new object minus the cost of the new object and minus the utility of owning the set without the new object.
- Formally: marginal utility of $x\notin X\cup Y$ is: $$\mu(x,X,Y,\vec{p})=\alpha (X\cup \{x\},Y,\vec{p})-\alpha(X,Y,\vec{p})$$
- Example: MU(flash) is greater when we already have a camera: $$MU(flash) \ll MU(camera+flash)$$





