# Claim boundary

The repository supports the following bounded conclusions:

- final task correctness and valid recovery can diverge when persistent state remains invalid;
- matched frozen failure states support controlled comparison of recovery scopes;
- local replay is the strongest fixed strategy in the reported bounded experiment under the frozen cost definition;
- the current evidence does not justify a learned recovery controller.

The repository does not support claims that:

- local replay is universally optimal;
- learned recovery is generally unnecessary;
- the selected InterCode tasks estimate real-world failure prevalence;
- residual invalid artifacts necessarily cause downstream harm;
- the diagnostic ablations are independent experimental replications.
