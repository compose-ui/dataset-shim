dataset-shim
============

Shims the dataset property for DOM nodes. This was copied from [brettz9's gist](https://gist.github.com/brettz9/4093766).

Usage:

```html
<!DOCTYPE html>
 
<script src="html5-dataset.js"></script>
 
<h3 id="hd" data-ab-cd="zzz">Test!</h3>
 
<script>
var h = document.getElementById('hd');
 
for (var i in h) {
    if (i === 'dataset') {alert('iterated an Element object');}
}
for (var i in Element.prototype) {
    if (i === 'dataset') {alert('iterated the Element prototype');}
}
 
 
try {
    alert(h.dataset.abCd)
}catch(e) {alert(e);}
 
h.dataset.abCd = 'abc';
alert(h.dataset.abCd)
    
</script>
```
