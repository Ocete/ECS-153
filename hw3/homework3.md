# Homework 3: trusted computing base
**José Antonio Álvarez Ocete**

## Main concepts presented

The most important concept of these few lectures and maybe the whole course is the **trusted computing base** (TCB). As defined by [Wikipedia](https://en.wikipedia.org/wiki/Trusted_computing_base):

`
The TCB of a computer system is the set of all hardware, firmware, and/or software components that are critical to its security, in the sense that bugs or vulnerabilities occurring inside the TCB might jeopardize the security properties of the entire system. By contrast, parts of a computer system outside the TCB must not be able to misbehave in a way that would leak any more privileges than are granted to them in accordance with the security policy.
`

I. e., it's the part of the system that we trust to be secure. In this week's videos, we look at works that assume that the whole system except for a little tiny piece is compromised, reducing their TCB to the minimum possible.

Back to this first lecture, we also discussed how running an app through a browser is way more secure than downloading it and installing it in your computer due to the permissions you are giving to it. We also talked about two important concepts: **interfaces** and **policies**.

Examples of interfaces:
- Processes within an operating system
- Client / server
- Web apps within a web browser

In order to explain policies, we used an example of trying to make a connection to *Facebook*. We described the narrowed and only way to connect to *Facebook* and how this improved its security, adding on top of that the sanity checks Facebook will have.

During the second lecture, we focussed on **hardware wallets**, explained how they work and had a discussion about if we would buy one given that all our money was kept in cryptocurrencies. We were explained how **Meltdown** worked and discussed how this could be applied to steal a private key within a hardware wallet.

From here we jumped to **Notary**, explaining how it *really* resets the whole system between apps so no methods like *Meltdown* can be applied. Finally, we talked about **formal methods**, and how they are used to prove things for software, such that how the reset in *Notary* would work for any previous state.

In the third lecture, we focussed on browsers and how they have been the target of attacks since the web evolved so much. We studied different types of vulnerabilities:

- Web apps vulnerabilities
- Browser vulnerabilities
- OS & lib vulnerabilities

And how the deeper you go, the more control you have over the system and the more damage you can achieve. This week's paper, **Fidelius** focussed on the last two types of vulnerabilities. The researchers assumed the whole system was compromised, reducing their TCB to the last minimum, a hardware enclave used to process and store the most vital information that your browser processes.

We also talked a lit more about **hardware enclaves**, how they work and how they might not be the most reliable thing to use, as it has been proven before that they have plenty of side channels vulnerabilities.

## Future Work

For the first video, the researchers commented on how their chip has quite simple and that their ideas of a complete reset between processes could be applied to more complex ones. In fact, this is something that hardware wallets creators could do on their own, implement this idea to their own wallets since they know the hardware better than anyone.

Following this idea, I have been thinking about how this could be applied to more complex systems: phones and computers. Computers nowadays use plenty of CPUs at the same time and multiple processes running on them, first concurrently, and second switching between different processes really fast. As an idea, CPUs could be completely reset between processes, just like *Notary* does. It is not so simple, of course. The current state of a running process is saved somewhere in memory, clearing the CPU and not protecting this saved state correctly is essentially meaningless. We would assume here that our TCB is the OS, but not the different apps, and the threat model processes trying to obtain information from the previous process running in the same CPU.

For the second video, it was mentioned how relying on users to look at switches has been proven to not be secure at all. I believe the next step on the *Fidelius* line of work would be to know when the browser is working with sensible data, such as logins, and tell the user if *Fidelius* is not active in a more explicit way. Making this way to rely on the browser might be a bad idea since we are assuming the browser has been compromised. In fact, we are also assuming that the OS is compromised but we could implement different ways to tell the user, and just some of them rely on the OS (let's say, a sound created by the hardware enclave and a pop-up from the OS).
