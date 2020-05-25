# Homework 6: Identity
**José Antonio Álvarez Ocete**

## Main concepts presented

We started this last technical lecture by talking about **phishing**, giving some quick notes about this week video [[1]](#footnote1). In particular, we talked about **lateral phishing**, which comes from someone familiar from the attacked perspective, or someone within the same company. Since the idea of phishing is to sell a story, it's more likely that we fall for it when it comes from someone we know.

We continued by discussing different situations where **digital identity** is interesting in the 21st century. Although these questions might look almost identical and could be answered simply by showing that the person sitting in front of the computer is who they say they are, they answer different problems from a security perspective. The questions are the following:

- **Who is this human in the real world?** This is important, for example, for online signatures.

- **Is this the same human we saw previously?** For some social networks we don't really need to know who is the person accessing the account, but yeah make sure they own the account.

- **Is this a script or a human?** In order to block automated attacks, from phishing to like farms and fake news.

- **Does this human own the payment method they’re using?** For online payment.

Finally, we talked extensively about **login and signup**, how they are exploited by attackers and what measures can be taken. We also discussed **the importance of false positives and how to avoid them**, referring to past lectures for this topic. Since one of the main solutions are user challenges, we talked about the different principles of them and some examples that showed how they can be based on the product in particular.

## Future Work

This is one of the security research areas that will *always* have future work to do, and that is for a very simple reason: Fraud can't be stopped completely. It can be mitigated, but it is a constant fight between attackers finding new ways to crack the system and security teams finding a balance between stopping them and don't pushing away real users.

One of the most important things here, at least for my point of view, are the fake news. Ways to manipulate people by just using social media and their phones. It's an influence that is already taken place and we can't really see, and it will be really dangerous in the near future.

Coming back to the paper itself, the researchers leave a couple of notes on where to further progress within their work. The first one is time-based, how the attacks are spread over time and if they occur at certain moments, while the second one is job position based, how these attacks first enter the corporations, how they spread (upwards or just in every direction?) or other factors that could help figure out the attackers' particular intentions, if any.

## References

<a name="footnote1">[1]</a>: [Detecting and Characterizing Lateral Phishing at Scale](https://www.youtube.com/watch?v=EZSlT7AWBzo&feature=youtu.be). Grant Ho, UC Berkeley and Barracuda Networks; Asaf Cidon, Barracuda Networks and Columbia University; Lior Gavish and Marco Schweighauser, Barracuda Networks; Vern Paxson, UC Berkeley and ICSI; Stefan Savage and Geoffrey M. Voelker, UC San Diego; David Wagner, UC Berkeley, Usenix Security 2019.
