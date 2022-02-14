# Torch-Warmup
Easiest way to use learning rate warmup method on PyTorch

# INSTALLATION

Install [pytorch-ignite](https://pytorch.org/ignite/index.html)
```
pip install pytorch-ignite
```

# In-script workflow

```python
from ignite.handlers.param_scheduler import create_lr_scheduler_with_warmup 
```
