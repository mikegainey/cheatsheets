# Python doctest

```python
import doctest    # at the top of the file
...
doctest.testmod() # at the bottom of the file
```
from the command line:
```python
python3 -m doctest myprogram.py
```
another way:
```python
if __name__ == '__main__':
    import doctest
    doctest.testmod()
```
