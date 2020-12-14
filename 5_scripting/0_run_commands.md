#### run() - simplification over Popen()
```python
from subprocess import run
from subprocess import DEVNULL
res = run(('echo',
    '-n',
    'hello'), stdout=DEVNULL)
print(res.returncode)  # 0
```

#### run() with shell=True
    (sh -c '...' analog)
```python
from subprocess import run
res = run('ls -la .', shell=True)
print(res.returncode)  # 0
```

#### check_output()
```python
from subprocess import check_output
res = check_output(('ls',
    '-la',
    '/tmp/.'))
print(res.decode('utf-8'))
```
    output:

    total 40
    drwxrwxrwt  8 root  wheel    256 Aug 29 21:06 .as_integer_ratio
    drwxr-xr-x  6 root  wheel    192 Mar  3 17:00 ..
    drwx------  3 gena  wheel     96 Aug 24 14:31 tmux-501
    ...
    
#### Popen(), read line by line
```python
import subprocess
with subprocess.Popen(['ping','google.com'], stdout=subprocess.PIPE) as proc:
  while True:
    line = proc.stdout.readline()
    if not line:
      break
    print(f'output line: {line.rstrip()}')
```

#### Popen and wait for the result
```python
import subprocess
with subprocess.Popen(['ls','-la'], stdout=subprocess.PIPE) as proc:
  print(f'output: {proc.stdout.read().decode("utf-8")}')
```

