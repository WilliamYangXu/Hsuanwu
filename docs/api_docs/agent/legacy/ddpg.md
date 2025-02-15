#


## DDPG
[source](https://github.com/RLE-Foundation/rllte/blob/main/rllte/agent/legacy/ddpg.py/#L40)
```python 
DDPG(
   env: gym.Env, eval_env: Optional[gym.Env] = None, tag: str = 'default', seed: int = 1,
   device: str = 'cpu', pretraining: bool = False, num_init_steps: int = 2000,
   feature_dim: int = 50, batch_size: int = 256, lr: float = 0.0001, eps: float = 1e-08,
   hidden_dim: int = 1024, critic_target_tau: float = 0.01, update_every_steps: int = 2,
   discount: float = 0.99, init_fn: str = 'orthogonal'
)
```


---
Deep Deterministic Policy Gradient (DDPG) agent.


**Args**

* **env** (gym.Env) : A Gym-like environment for training.
* **eval_env** (gym.Env) : A Gym-like environment for evaluation.
* **tag** (str) : An experiment tag.
* **seed** (int) : Random seed for reproduction.
* **device** (str) : Device (cpu, cuda, ...) on which the code should be run.
* **pretraining** (bool) : Turn on the pre-training mode.
* **num_init_steps** (int) : Number of initial exploration steps.
* **feature_dim** (int) : Number of features extracted by the encoder.
* **batch_size** (int) : Number of samples per batch to load.
* **lr** (float) : The learning rate.
* **eps** (float) : Term added to the denominator to improve numerical stability.
* **hidden_dim** (int) : The size of the hidden layers.
* **critic_target_tau**  : The critic Q-function soft-update rate.
* **update_every_steps** (int) : The agent update frequency.
* **discount** (float) : Discount factor.
* **init_fn** (str) : Parameters initialization method.



**Returns**

DDPG agent instance.


**Methods:**


### .update
[source](https://github.com/RLE-Foundation/rllte/blob/main/rllte/agent/legacy/ddpg.py/#L135)
```python
.update()
```

---
Update the agent and return training metrics such as actor loss, critic_loss, etc.

### .update_critic
[source](https://github.com/RLE-Foundation/rllte/blob/main/rllte/agent/legacy/ddpg.py/#L177)
```python
.update_critic(
   obs: th.Tensor, actions: th.Tensor, rewards: th.Tensor, terminateds: th.Tensor,
   truncateds: th.Tensor, next_obs: th.Tensor
)
```

---
Update the critic network.


**Args**

* **obs** (th.Tensor) : Observations.
* **actions** (th.Tensor) : Actions.
* **rewards** (th.Tensor) : Rewards.
* **terminateds** (th.Tensor) : Terminateds.
* **truncateds** (th.Tensor) : Truncateds.
* **next_obs** (th.Tensor) : Next observations.


**Returns**

Critic loss.

### .update_actor
[source](https://github.com/RLE-Foundation/rllte/blob/main/rllte/agent/legacy/ddpg.py/#L224)
```python
.update_actor(
   obs: th.Tensor
)
```

---
Update the actor network.


**Args**

* **obs** (th.Tensor) : Observations.


**Returns**

Actor loss metrics.
