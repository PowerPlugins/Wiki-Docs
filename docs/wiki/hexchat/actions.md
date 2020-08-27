# Actions
HexChat supports different JSON Actions which are listed here.  
The page will help you understanding the overall syntax of how to apply actions to a chat Section.

## Hover
The `hover` option tells HexChat to add the provided List as a Hover message to the text.

Syntax:  
```yaml
formats:
  tooltip:
    text: 'This text has a tooltip!'
    #
    # Adding the hover
    #
    hover:
    - '&7This is a hover text!'
```

----
## Click
The `click` field allows you to set an action for when the player clicks on the text.

### `execute`
The `execute` type will run a provided command as the player that clicks the text.  
You can alternatively also provide `command` as type.

Syntax:  
```yaml
formats:
  runCommand:
    text: 'Click to get a Diamond!'
    #
    # Adding the click action
    #
    click:
      type: 'execute'
      value: '/give %player% diamond'
```

### `suggest`
The `suggest` type will put the provided command/text into the player's chat bar.

Syntax:  
```yaml
formats:
  suggestCommand:
    text: 'Click to send a message to %player%'
    #
    # Adding the click action
    #
    click:
      type: 'suggest'
      value: '/msg %player% '
```

### `copy`
The `copy` type will allow you to set a text, which will then be copied into the players clipboard once they click on the text.

!!! info "Important"
    This type only works on 1.15 and newer.

Syntax:  
```yaml
formats:
  copyText:
    text: 'Click to copy something.'
    #
    # Adding the click action
    #
    click:
      type: 'copy'
      value: 'Something'
```

### `url`
The `url` type will allow you to set a URL, that would get opened once the player clicks the text.

Syntax:  
```yaml
formats:
  openUrl:
    text: 'Click to open a URL.'
    #
    # Adding the click action
    #
    click:
      type: 'url'
      value: 'https://github.com/Andre601/HexChat'
```
