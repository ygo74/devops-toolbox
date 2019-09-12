# Environment Development configuration
## Visual studio code



### extensions :
- Trailing Spaces : Only to see spaces on the files  
```json
{ "trailing-spaces.trimOnSave": true }
```  

### settings :
- Trailing Spaces : disable for markdown files
```json
    "files.trimTrailingWhitespace": true,
    "[markdown]": {
        "files.trimTrailingWhitespace": false
    }
```  
- scrollback buffer :
```json
    "terminal.integrated.scrollback": 100000
```
