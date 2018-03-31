# Python logging

```python
import logging
logging.basicConfig(level=logging.DEBUG)
logging.debug("The log message")
logging.disable(logging.CRITICAL)
```
Logging to a file:
```python
logging.basicConfig(filename='binthelist.log', filemode='w',
                    format='%(message)s',
                    level=logging.DEBUG)
```

To show a logfile in real-time:
```bash
tail -f <filename>
```

## Logging Levels
- DEBUG
- INFO
- WARN
- ERROR
- CRITICAL
