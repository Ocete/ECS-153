# Homework 4: Malicious Computer Systems
**José Antonio Álvarez Ocete**

## Introduction

For this particular homework it was pretty difficult for me to separate the *Main Concepts* section from the *Future Work* section. Not because I couldn't distinguish objectives concepts from my own ideas but because it makes more sense to read my homework as a whole speech instead of two independent sections. I hope this change of format is not inconvenient.

## Main concepts presented and Future Work

In this lecture (4/27), we started discussing how security breaches in computer security are celebrated within the research community. Coming back to the very last lecture (5/1), we discussed the security and ethics of ML and how even if we can do something, that doesn't mean we *should* do it.

That raises an important question for me here. A clear example is the car hacking paper seen at the beginning of the course [[1]](#myfootnote1). It showed multiple ways to completely compromise a car. They also explained that they had reached out to several software and automobile companies and that they were listening and willing to make changes in their security. However, if they are willing to do such a thing, wouldn't it be better to wait until those security measures have been implemented before publicly revealing a security breach as such?

I think the openness of the research community about the kind of outbreaks helps immensely to both developers and researchers but, at the same time, I believe they sometimes do things too quickly, just like publishing, and that might be dangerous. If I recall correctly, the exact same thing happened with the Meltdown vulnerability a few years ago. When the bug was publicly published, companies were already working on it -- and obviously some malicious software had already exploited it. However, couldn't they have waited until it had been patched before releasing it to the press?

We continued the lecture by discussing how attackers and defenders want to be in the lowest possible layer in the system. The lower you are, the more you can control and convert, although the implementation gets more and more difficult. We tackled this with an example of an attacker and a defender both fighting over a system and we showed how the attacker would use the uppermost layer and a high-level language to implement the attack itself while covering it from a lower layer with less flexible tools.

This was followed by a brief explanation of the research done in the paper. How the challenges that Sam and the team faced redirected their work in a new line, software attacks with a minimal hardware tampering.

This is the second topic I wanted to discuss: how huge adversities can push developers and researchers to think outside the box and find creative and outstanding solutions, as we can see in Sam's work. I can think of at least to clear examples of this within the videogame industry: The first one is the classic Doom and how they faked 3D using actually 2D in a really clever way changing the industry as a whole afterward. The second one is how the speed of the enemy changes in Space Invaders as more of them get killed. At first, this was purely due to the speed of the CPU: The fewer enemies it had to render, the quickest it could render them and the faster they moved. They ended up implementing this issue as a feature, adapting what at first seemed like hardware adversity to make it part of the game's very core. I see huge similarities between these developments and the way Sam and his team developed their paper.

But developers and researchers are not the only ones that upon facing adversities have to rethink of they work: malicious attackers do it too. This brings us to the next point on our lecture: adversarial thinking and how to counter it.

We ended the lecture by discussing in detail two types of attacks:
-  A way of bypass the page protection software by ignoring the *priv* bit upon reading a certain chain of characters.
- The shadow mode mechanism: Injecting code into the cache using the NIC. Upon reading a certain chain of bytes, the malicious debug code will trigger letting us execute the code on the cache. Once this malicious debug code is installed in the hardware we could do this as many times as we wanted by just sending a package to the computer.

These are both attacks that used minimum hardware changes to compromise the whole system, being able to run *any* code the attacker wants.

## Bibliography

<a name="myfootnote1">[1]</a>: [Comprehensive Experimental Analyses of Automotive Attack Surfaces](https://www.usenix.org/legacy/events/sec11/tech/full_papers/Checkoway.pdf). Stephen Checkoway, Damon McCoy, Brian Kantor, Danny Anderson, Hovav Shacham, and Stefan Savage, University of California, San Diego; Karl Koscher, Alexei Czeskis, Franziska Roesner, and Tadayoshi Kohno, University of Washington (Optional paper)
