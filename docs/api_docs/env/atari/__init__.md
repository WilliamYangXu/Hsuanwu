#


### make_atari_env
[source](https://github.com/RLE-Foundation/rllte/blob/main/rllte/env/atari/__init__.py/#L85)
```python
.make_atari_env(
   env_id: str = 'Alien-v5', num_envs: int = 8, device: str = 'cpu', seed: int = 1,
   frame_stack: int = 4, parallel: bool = True
)
```

---
Create Atari environments.


**Args**

* **env_id** (str) : Name of environment.
* **num_envs** (int) : Number of environments.
* **device** (str) : Device to convert the data.
* **seed** (int) : Random seed.
* **frame_stack** (int) : Number of stacked frames.
* **parallel** (bool) : `True` for creating asynchronous environments, and `False`
    for creating synchronous environments.


**Returns**

The vectorized environments.

----


### make_envpool_atari_env
[source](https://github.com/RLE-Foundation/rllte/blob/main/rllte/env/atari/__init__.py/#L46)
```python
.make_envpool_atari_env(
   env_id: str = 'Alien-v5', num_envs: int = 8, device: str = 'cpu', seed: int = 1,
   parallel: bool = True
)
```

---
Create Atari environments with `envpool`.


**Args**

* **env_id** (str) : Name of environment.
* **num_envs** (int) : Number of environments.
* **device** (str) : Device to convert the data.
* **seed** (int) : Random seed.
* **parallel** (bool) : `True` for creating asynchronous environments, and `False`
    for creating synchronous environments.


**Returns**

The vectorized environments.
