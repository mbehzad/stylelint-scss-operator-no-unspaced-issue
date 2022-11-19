# Minimal Reproducing Repo for scss/operator-no-unspaced false positive for `*` when used as selector

SCSS code: 
```scss
.element {
    @supports selector(:has(*)) {
        opacity: 0;    
    }
}
```
stylelintrc config: 
```json
{
  "plugins": [
    "stylelint-scss"
  ],
  "rules": {
    "scss/operator-no-unspaced": true
  }
}
```
Error:
```
2:26  ✖  Expected single space before "*"  scss/operator-no-unspaced
2:26  ✖  Expected single space after "*"   scss/operator-no-unspaced
```

Run `npm test` to see the stlyint error.
