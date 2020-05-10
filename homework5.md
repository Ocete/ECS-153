# Homework 5: Machine Learning and Security
**José Antonio Álvarez Ocete**

## Main concepts presented

During the first lecture we discussed and went deep on most of Mickens lecture [[1]](#footnote1) about skepticism and uses of ML for security nowadays. The first thing we noticed in this matter is how **security applied ML is not a classic ML problem** for the following reasons:

- In a classic ML problem we have a certain amount of data to train our model. Here, the data keep coming and flowing. And opponents can react to our decisions and models, so we should be able to adapt to those.

- The ML model shouldn't make final decisions. We can't permanently block a transaction or access because our ML algorithm dictates so, we should over other mechanisms on top of it to make sure that action is malicious.

- Measuring impact and how good your model is in these problems is way more difficult, we have to rely on different metrics than usual.

In order to illustrate these points we went through an example: detecting malicious login attempts in Lyft. In this problem we are constantly obtaining new data (new login attempts) and our model should be able to learn from those along the way. Additionally, we realize that blocking a login attempt just because our ML model dictates so leaves little room for mistakes. However, adding an additional system afterward that confirms your identity through a different system, like putting in your email or taking a picture of yourself, to let you in. Finally, in order to look at the impact of your decisions you can look at multiple factors: Successful logins overtime upon deploying the new system, looking at how many users put it their email correctly and how many decided not even try to, or looking at reviews in the store.

After that we talked about **Deep fakes**, using ML to create fake representations of real images (or even videos), such as credit cards and facial pictures. We dived into *Fugazi*, a model that combines ML and traditional vision algorithms in certain areas to create fake credit cards with amazing results.

In the second lecture we talked about **Adversarial Examples**: creating ML input that fools the ML model. The approach taken in the lecture we previously watched [[2]](#footnote2) was the **White Box** threat model, assuming that the attacker can see the weights and hyperparameters of the neural network.

After explaining this type of attack we discussed some attempts to counter it that the research community has developed over time. None of them really worked except adding some of the adversarial examples to your training set. However, the attackers will them create new pictures that bypass this new model, then you could retrain your model... And iterate on it.

Finally, we have a small discussion about the **Black Box** threat model, where we would train a model in a similar way as the model we want to attack was trained. Then, we train a second model following the white box techniques to fool the model we just trained and we perfectly now. Finally, the model we just trained should be able to fool our aim model.

## Future Work

The first idea I wanted to discuss is the question left between lectures: **When is ML is appropriate for security?** As an also Math bachelor myself I would like to work on ML and AI at some point. In this regard, these lectures made me think of where it is appropriate to use ML and what other guidelines we should consider. Adding extra layers to our algorithm to make sure of the model's answers is a really good way to prevent fatal mistakes.

In the same way, we could consider using more readable models like, for instance, decision trees. If we trained this kind of model to dictate if someone is guilty of a certain crime, we could see in a really narrowed structure information from other similar cases. For example, we could reach a node in a decision tree that upon answering certain questions the algorithm thinks that the accused is guilty with a 95% confidence, and we can track how the algorithm reached that conclusion. That doesn't mean we should just follow what it dictates, but something like this could be really useful.

On the other hand, I wanted to discuss how **our inability to detect deep fakes in general has a profound implication on society**. This could be used to provide really convincing fake evidence in a trial or even change history in the long term. It is important that we fight and conduct research against these measures to make sure we aren't overwhelmed but these behaviors in the future.

## References

<a name="footnote1">[1]</a>: [Q: Why Do Keynote Speakers Keep Suggesting That Improving Security Is Possible? A: Because Keynote Speakers Make Bad Life Decisions and Are Poor Role Models](https://www.usenix.org/conference/usenixsecurity18/presentation/mickens). James Mickens, Harvard University.

<a name="footnote2">[2]</a>: [Towards evaluating the robustness of neural networks](https://www.youtube.com/watch?v=yIXNL88JBWQ). N Carlini, D Wagner 2017 IEEE Symposium on Security and Privacy (SP), 39-57.
