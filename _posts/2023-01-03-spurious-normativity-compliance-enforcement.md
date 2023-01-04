---
layout: post
title: "Spurious normativity enhances learning of compliance and enforcement behavior in artificial agents"
author: Raphael Koster, Dylan Hadfield-Menell, Richard Everett, Joel Leibo, et al.
date: 2022-01-12
categories: [research, social]
tags: multi-agent-rl
---

[https://www.pnas.org/doi/10.1073/pnas.2106028118](https://www.pnas.org/doi/10.1073/pnas.2106028118)

https://github.com/deepmind/spurious_normativity

> How do societies learn and maintain social norms? 
>
> Here we use multiagent reinforcement learning to investigate the learning dynamics of enforcement and compliance behaviors. 
>
> Artificial agents populate a foraging environment and need to learn to avoid a poisonous berry. Agents learn to avoid eating poisonous berries better when doing so is taboo, meaning the behavior is punished by other agents. The taboo helps overcome a credit assignment problem in discovering delayed health effects. 
>
> Critically, introducing an additional taboo, which results in punishment for eating a harmless berry, further improves overall returns. **This “silly rule” counterintuitively has a positive effect because it gives agents more practice in learning rule enforcement.** 
>
> By probing what individual agents have learned, we demonstrate that normative behavior relies on a sequence of learned skills. Learning rule compliance builds upon prior learning of rule enforcement by other agents. 
>
> Our results highlight the benefit of employing a multiagent reinforcement learning computational model focused on learning to implement complex actions.

> In particular, the model creates rich learning dynamics for individual agents as well as groups that could not otherwise be approached.
>
> 1. **Complex action sequences**: Punishing other agents’ behavior, observing a rule violation or complying with a rule are complex sequences of subactions that can look different each time they are performed or observed.
> 2. **Skills build on each other**: As agents have to learn to implement complex behaviors, we can expect a temporal dependency and sequentiality among these behaviors. For example, for agents to learn to avoid a taboo, agents will first need to learn how to effectively apply punishing, in order to motivate rule compliance.
> 3. **Opportunity cost**: As agents are driven by maximizing total reward, whether or not an agent engages in social punishing depends on the opportunity cost of the action sequence, the agent’s skill in implementing it, and the reward gained by punishing the other agent’s transgression. This means there is an intrinsic economy to behavior that is bounded by what agents have learned.
> 4. **Generalization**: Since the social dynamics are learned in neural networks, they afford the opportunity for, or even necessitate, a degree of generalization. In particular, as punishment is identical for the consequences of transgressing against an important or silly rule, there is an opportunity for generalization of the enforcement behavior learned for both rules.
> 5. **Endogenous errors**: As social punishing of silly or important rules is implemented in the same way, a confusion between the two can arise. Similarly, punishing might be misdirected at agents that did not break a social taboo. These costly false-positive incidents provide an intrinsic counterweight to the development of an indiscriminate social punishing dynamic. Importantly, unlike other frameworks, deep RL does not require us to model mistakes in behavior as random noise (e.g., refs. [33](https://www.pnas.org/doi/10.1073/pnas.2106028118#core-r33) and [47](https://www.pnas.org/doi/10.1073/pnas.2106028118#core-r47)). Instead, mistakes in RL are emergent from the learning dynamics and the inherent difficulty of implementing an effective behavior policy.
