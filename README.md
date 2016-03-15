# deadbeef

The most important part of much important work is coming up with clever hex-encoded constants to put into your code, protocols, and exploits.
This module attempts to address a shocking lack of diversity constant of these constants and hopes to ignite a renaissance in hex constants around the world.

## Install

To install:

```bash
pip install deadbeef
```

## Usage

To use:

```python
import deadbeef

# gets a cool hex constant (string) of length 8
print "0x" + deadbeef.get_string(8)

# gets a cool int of length *4* that hex()es to a string of length 8 (plus '0x')
print hex(deadbeef.get_int(8))

# get some even hexspeak
print deadbeef.get_int(postfilter=lambda w: int(w, 16) % 2 == 0)

# get some hexspeak that has at least 7 different letters pre-conversion
print deadbeef.get_int(prefilter=lambda w: len(set(w)) >= 7)
```

## Replacements

deadbeef makes the following replacements to hexify strings:

| From | To |
|------|----|
|    g | 9  |
|    i | 1  |
|    j | f  |
|    o | 0  |
|    s | 5  |
|    t | 7  |
|    z | 2  |
|    l | 1  |
|    q | 9  |
|    h | 6  |

Custom replacements can be provided by instantiating your own `DEADBEEF` object and using it instead of the module-wide functions.

## See also

After writing this, it occurred to me that it might already be out there. Check out:

- https://en.wikipedia.org/wiki/Hexspeak
- https://reminiscential.wordpress.com/2008/09/03/hexspeak-and-generator/
- http://nedbatchelder.com/text/hexwords.html
