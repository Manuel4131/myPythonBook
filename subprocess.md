Reference

[Subprocess in python](https://docs.python.org/2/library/subprocess.html)

#Antoher example
```bash
./scriptName cat 'white content'
```

When you need to parse the string to the script, be aware
that the file name or argument options may contain white spaces or some chars needed to be escaped. In that condition, you need to add quotes to wrap them. Otherwise, the argument will be separated into several arguments. 

```python
#!/usr/bin/python

import subprocess;
import shlex;
import sys;

inputString= raw_input("Input command: ")
print "The input command is: " + inputString
cmdline=shlex.split(inputString);
print  cmdline
subprocess.Popen(cmdline);
```



