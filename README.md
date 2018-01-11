#Lorca.js
Lorca is a NLP library for Spanish written in javascript.

##Installation
###Client-side

Download lorca.js from this repository and inclue it in your html. Start using it right away.

###Server-side
Not suported yet, but soon.

##Text tokenization

```javascript
var doc = lorca('En verano hace calor. En invierno hace frío');

doc.get();
// En verano hace calor. En invierno hace frío.

doc.sentences().get();
// [ 'En verano hace calor.', ' En invierno hace frío.' ]

doc.words().get();
// [ 'en', 'verano', 'hace', 'calor', 'en', 'invierno', 'hace', 'frío' ]

doc.syllables().get();
// [ 'En ', 've', 'ra', 'no', ' ha', 'ce ', 'ca', 'lor.', ' En', ' in', 'vier', 'no', ' ha', 'ce ','frí', 'o.' ]

doc.sentences().words().get();
// [ [ 'en', 'verano', 'hace', 'calor' ],
//   [ 'en', 'invierno', 'hace', 'frío' ] ]

doc.sentences().words().syllables().get();
/*
 [ [ [ 'en' ],
     [ 've', 'ra', 'no' ],
     [ 'ha', 'ce' ],
     [ 'ca', 'lor' ] ],
   [ [ 'en' ],
     [ 'in', 'vier', 'no' ],
     [ 'ha', 'ce' ],
     [ 'frí', 'o' ] ] ]
*/

doc.sentences().syllables().get();
// [ [ 'En ', 've', 'ra', 'no', ' ha', 'ce ', 'ca', 'lor.' ],
//   [ ' En', ' in', 'vier', 'no', ' ha', 'ce ', 'frí', 'o.' ] ]

doc.words().syllables().get();
/*
[ [ 'en' ],
  [ 've', 'ra', 'no' ],
  [ 'ha', 'ce' ],
  [ 'ca', 'lor' ],
  [ 'en' ],
  [ 'in', 'vier', 'no' ],
  [ 'ha', 'ce' ],
  [ 'frí', 'o' ] ]
*/
```



