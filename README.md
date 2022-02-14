# Torch-Warmup
Easiest way to use learning rate warmup method on PyTorch, **as far as I know**.

# INSTALLATION

Install [pytorch-ignite](https://pytorch.org/ignite/index.html)
```
pip install pytorch-ignite
```

# Example

```python
from ignite.handlers.param_scheduler import create_lr_scheduler_with_warmup

...
lr_scheduler = ...
lr_scheduler_warmup = create_lr_scheduler_with_warmup(lr_scheduler,
                                               warmup_start_value=warmup_initial_lr,
                                               warmup_duration=warmup_iteration,
                                               warmup_end_value=initial_lr)
...

while not converged do: #pseudocode 
  lr_scheduler(None)
  ...
  optimizer.step()
  ...
end while
```

Please see the [warmup.ipynb](./warmup.ipynb) file for more information.
