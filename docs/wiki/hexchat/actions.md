# Actions
HexChat supports different JSON Actions which are listed here.  
The page will help you understanding the overall syntax of how to apply actions to a chat Section.

## Hover
The `hover` field tells HexChat to apply the provided `value` as a hover action based on the provided type.

### `text`
The `text` type will make HexChat set the provided values as a Hover text (tooltip). You can utilize color codes inside the Hover text for further customisation.

Syntax:  
```yaml
formats:
  tooltip:
    text: 'This text has a tooltip!'
    #
    # Adding the hover
    #
    hover:
      type: 'text'
      #
      # When 'text' is used as type does value become a String list.
      #
      value:
      - '&7This is a hover text!'
```

### `achievement`
The `achievement` type will display a specific achievement, when you hover over the text.  
The provided value has to be a [valid Achievement ID](https://minecraft.gamepedia.com/Advancement#List_of_advancements) (e.g. `minecraft:story/mine_stone`).

Syntax:  
```yaml
format:
  advancement:
    text: 'This text has an advancement!'
    #
    # Adding the hover
    #
    hover:
      type: 'achievement'
      #
      # When 'achievement' is used as type does value become a String.
      #
      value: 'minecraft:shiny_gear' # "Cover Me With Diamonds!" achievement
```

----
## Click
The `click` field allows you to set an action for when the player clicks on the text.

### `execute`
The `execute` type will run a provided command as the player that clicks the text.

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
    Any version older than 1.15 will default to [`suggest`](#suggest)

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
