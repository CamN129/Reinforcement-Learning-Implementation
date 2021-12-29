## About
After watching most of [David Silver's lectures](https://www.youtube.com/watch?v=2pWv7GOvuf0) on reinforcement learning and reading through [OpenAI's Spinning Up](https://spinningup.openai.com/en/latest/user/introduction.html), I decided to begin attempting to implement some of the fundamental reinforcement learning algorithms.

## VPG 
[Vanilla policy gradient](https://spinningup.openai.com/en/latest/algorithms/vpg.html) uses a stochastic policy and learns in an on policy way (explores by sampling actions according to up to date policy). I followed the layout spinning up gave, but replacing advantage value simply with episode returns as done [here](https://www.notion.so/Vanilla-Policy-Gradients-b93451bb5507454c9d7de6a96ac629c1#a4aaed6159b5483e9d1e03f655e3fdce).

https://user-images.githubusercontent.com/64811449/147689323-5d1c0808-e263-47c4-b62e-8ee9b72a1a23.mp4
In this environment, the agent is rewarded for balancing the pole on the cart. The choice of action is discrete and can be either move left or right.

## PPO (Clip)
[Proximal Policy Optimization](https://spinningup.openai.com/en/latest/algorithms/ppo.html) similarly uses a stochastic policy and learns in an on policy way. This time we use the actor critic method to update our policy. The actor determines what action we take, while the critic evaluates the actor's action and computes the value. PPO updates the policy so that the new policy is only "this" much different than the previous policy, "this" being determined by the clip hyperparameter.

https://user-images.githubusercontent.com/64811449/147690283-9aaa582b-dd06-47d9-805f-91d5ef8acfcb.mp4
In this environment, the agent is rewarded for balancing the pendulum. The choice of action is continuous, it is one number, positive or negative, that determines how hard to swing the arm and in what direction.
