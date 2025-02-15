#


### make_bitflipping_env
[source](https://github.com/RLE-Foundation/rllte/blob/main/rllte/env/bitflipping/__init__.py/#L244)
```python
.make_bitflipping_env(
   env_id: str = 'BitFlippingEnv-v0', num_envs: int = 1, device: str = 'cpu', seed: int = 0,
   parallel: bool = True, n_bits: int = 15, continuous: bool = False,
   max_steps: Optional[int] = 15, discrete_obs_space: bool = False,
   image_obs_space: bool = False, channel_first: bool = True
)
```

---
Create bit flipping environment.


**Args**

* **env_id** (str) : Name of environment.
* **num_envs** (int) : Number of environments.
* **device** (str) : Device to convert the data.
* **seed** (int) : Random seed.
* **parallel** (bool) : `True` for creating asynchronous environments, and `False`
    for creating synchronous environments.
* **n_bits** (int) : Number of bits to flip
* **continuous** (bool) : Whether to use the continuous actions version or not,
    by default, it uses the discrete one.
* **max_steps** (int) :  Max number of steps, by default, equal to n_bits.
* **discrete_obs_space** (bool) : Whether to use the discrete observation
    version or not, by default, it uses the ``MultiBinary`` one.
* **image_obs_space** (bool) : Use image as input instead of the ``MultiBinary`` one.
* **channel_first** (bool) : Whether to use channel-first or last image.


**Returns**

The vectorized environments.
