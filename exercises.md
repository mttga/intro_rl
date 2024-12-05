# Introduction to RL Lab

### Let's Go Hands-On!

**Your goal is to get hands-on experience by experimenting with RL yourself.** Choose one or more exercises from the list below (depending on the time available). The exercises are arranged by difficulty, so it’s recommended to start with the earlier ones. The last few exercises are more challenging and may not be possible to complete today. Consider them as long-term tasks.

---

### Exercises:

1. **Epsilon-Greedy Policy Evaluation (simple):**  
   Q-Learning and DQN use an epsilon-greedy exploration policy during training. As a result, the exact greedy performance of the algorithm is not known during training. Modify the algorithm so that every N episodes, you can print an estimate of the greedy algorithm's performance.

2. **Handling Randomness in RL (simple):**  
   RL can be unstable and heavily influenced by random factors during training. For reliable performance evaluation:  
   - Learn how to control randomization [here](https://stackoverflow.com/questions/47331235/how-should-openai-environments-gyms-use-env-seed0).  
   - Perform multiple runs of DQN and Reinforce with Acrobot, using different random initializations.  
   - Produce plots comparing the mean return (across seeds) and standard error for the two algorithms. The final plots should resemble [this example](https://spinningup.openai.com/en/latest/spinningup/bench.html).

3. **Leveraging GPUs (simple):**  
   DQN and Reinforce use neural networks, but the provided implementations run only on CPUs. Modify them to train on GPUs.

4. **Hyperparameter Ablations (simple):**  
   Investigate the effects of modifying the hyperparameters of an RL algorithm of your choice. Generate ablation plots to show how the performance changes.

5. **CartPole Environment (simple):**  
   Apply Q-Learning, DQN, or Reinforce to the [CartPole environment](https://www.gymlibrary.dev/environments/classic_control/cart_pole/).  
   - Goal: Balance a pendulum by applying forces to the left or right of a cart.  
   - Success Criterion: Achieve an average episode return of 500.  
   - You may need to adjust hyperparameters (e.g., learning rate) to solve this task.

6. **LunarLander Environment (medium):**  
   Apply Q-Learning, DQN, or Reinforce to the [LunarLander environment](https://www.gymlibrary.dev/environments/box2d/lunar_lander/).  
   - Goal: Land a space rocket inside a designated zone on the moon.  
   - Success Criterion: Achieve an average episode return of 200.  
   - You may need to adjust hyperparameters (e.g., learning rate) to solve this task.

7. **DQN Without Target Networks (medium):**  
   Modify DQN to remove target networks (i.e., compute the target using the current network without freezing it during training).  
   - Test the algorithm’s stability in at least two environments.  
   - Perform multiple runs with different seeds, save the results, and compare performance using plots similar to those in Exercise 2.

8. **Dueling Architectures (medium):**  
   Modify DQN to incorporate a dueling architecture ([paper](https://arxiv.org/abs/1511.06581), [blog](https://towardsdatascience.com/dueling-deep-q-networks-81ffab672751)).  
   - Apply it to at least one environment and compare its performance with standard DQN.

9. **SARSA Algorithm (medium):**  
   Learn about the SARSA algorithm from the course slides or resources like [this](https://towardsdatascience.com/introduction-to-reinforcement-learning-temporal-difference-sarsa-q-learning-e8f22669c366) or [this](https://medium.com/practical-coders-chronicles/learning-with-cliffwalking-sarsa-algorithm-in-3-easy-steps-95ca57735a8f).  
   - Explore why Q-Learning is off-policy while SARSA is on-policy.  
   - Modify the provided Q-Learning implementation to use SARSA and apply it to at least one environment.

10. **Advantage Actor-Critic (A2C) (medium):**  
    Apply Advantage Actor-Critic to the [CartPole](https://www.gymlibrary.dev/environments/classic_control/cart_pole/) or [LunarLander](https://www.gymlibrary.dev/environments/box2d/lunar_lander/) environments.  
    - Understand the algorithm well before implementation. [This blog](https://huggingface.co/blog/deep-rl-a2c) is a simple introduction. 
    - Modify the current implementation to handle discrete actions.

11. **Target Networks for Actor-Critic (advanced):**  
    Can target networks be used to stabilize the actor-critic model? Modify the actor-critic algorithm to use target networks for training the critic and test it on at least one environment.

12. **Using $Q(s, a)$ Instead of Advantages (advanced):**  
    In Actor-Critic, replace the use of advantages $A(s, a)$ with $Q(s, a)$ for bias correction. Investigate how $Q(s, a)$ can be learned with a critic.

13. **Double DQN (advanced):**  
    Modify DQN to implement Double DQN ([paper](https://arxiv.org/abs/1509.06461), [blog](https://towardsdatascience.com/double-deep-q-networks-905dd8325412)).  
    - Apply it to one or more environments and compare its performance with standard DQN.

14. **Replay Buffers in Actor-Critic (very advenced):**  
    Investigate using replay buffers for training the critic in the Actor-Critic model.  
    - Discuss potential challenges.  
    - Hint: This approach leads to algorithms like [DDPG](https://spinningup.openai.com/en/latest/algorithms/ddpg.html).  
    - Attempt to implement it.