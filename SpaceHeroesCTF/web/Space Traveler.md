## Description:
explore space with us

Inspect the site with Devtool , i saw obfuscated JS code:
```javascript
<script>
var _0xb645=["\x47\x75\x65\x73\x73\x20\x54\x68\x65\x20\x46\x6C\x61\x67","\x73\x68\x63\x74\x66\x7B\x66\x6C\x61\x67\x7D","\x59\x6F\x75\x20\x67\x75\x65\x73\x73\x65\x64\x20\x72\x69\x67\x68\x74\x2E","\x73\x68\x63\x74\x66\x7B\x65\x69\x67\x68\x74\x79\x5F\x73\x65\x76\x65\x6E\x5F\x74\x68\x6F\x75\x73\x61\x6E\x64\x5F\x6D\x69\x6C\x6C\x69\x6F\x6E\x5F\x73\x75\x6E\x73\x7D","\x59\x6F\x75\x20\x67\x75\x65\x73\x73\x65\x64\x20\x77\x72\x6F\x6E\x67\x2E","\x69\x6E\x6E\x65\x72\x48\x54\x4D\x4C","\x64\x65\x6D\x6F","\x67\x65\x74\x45\x6C\x65\x6D\x65\x6E\x74\x42\x79\x49\x64"];function myFunction(){let _0xb729x2;let _0xb729x3=prompt(_0xb645[0],_0xb645[1]);switch(_0xb729x3){case _0xb645[3]:_0xb729x2= _0xb645[2];break;default:_0xb729x2= _0xb645[4]};document[_0xb645[7]](_0xb645[6])[_0xb645[5]]= _0xb729x2}
</script>
```
After deobfuscated with JSNice , i got this:
```javascript
var _0xb645 = ["Guess The Flag", "shctf{flag}", "You guessed right.", "shctf{eighty_seven_thousand_million_suns}", "You guessed wrong.", "innerHTML", "demo", "getElementById"];
/**
 * @return {undefined}
 */
function myFunction() {
  let _0xb729x2;
  let _0xb729x3 = prompt(_0xb645[0], _0xb645[1]);
  switch(_0xb729x3) {
    case _0xb645[3]:
      _0xb729x2 = _0xb645[2];
      break;
    default:
      _0xb729x2 = _0xb645[4];
  }
  document[_0xb645[7]](_0xb645[6])[_0xb645[5]] = _0xb729x2;
}
;
```
I thought i might detected the flag instantly in **_0xb645** variable . Attempted to submit successfully.
>Flag: shctf{eighty_seven_thousand_million_suns}

