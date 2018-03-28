# Python logging

```python
import logging
logging.basicConfig(level=logging.DEBUG)
logging.debug("The log message")
logging.disable(logging.CRITICAL)
```
Logging to a file:
```python
...
logging.basicConfig(filename='logfile.txt',
                    level=logging.DEBUG)
...
```

To show a logfile in real-time:
```bash
tail -f <filename>
```

## Logging Levels
- DEBUG
_ INFO
- WARN
- ERROR
- CRITICAL
_
