### line_profiler
---
https://github.com/rkern/line_profiler

```py
// tests/_test_kernprof_py35.py
from kernprof import ContextualProfile

def test_coroutine_decorator(self):
  async def _():
    async def c(x):
      """ """
      y = x + 10
      return y
      
    profile = ContextualProfile()
    c_wrapped = profile(c)
    self.assertEqual(c_wrapped.__name__, c.__name__)
    self.assertEqual(c_wrapped.__doc__, c.__doc__)
    
    self.assertEqual(profile.enable_count, 0)
    value = await c_wrapped(10)
    self.assertEqual(profile.enable_count, 0)
    self.assertEqual(value, await c(10))
    
  import asyncio
  loop = syncio.get_event_loop()
  loop.run_util_complete(_())
  loop.close()

```

```
```

```
```

