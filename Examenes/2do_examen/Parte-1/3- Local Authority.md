### Descripción
Can you get the flag? Go to this [website](http://saturn.picoctf.net:49386/) and see what you can discover.

### Solución

Al inspeccionar elemento dentro del archivo secure.js
```js
function checkPassword(username, password)
{
  if( username === 'admin' && password === 'strongPassword098765' )
  {
    return true;
  }
  else
  {
    return false;
  }
}
```

picoCTF{j5_15_7r4n5p4r3n7_b0c2c9cb}