# ObservableObject

It's a simple Javascript object that implement the Subject part in a Observer-Subject relationship in ECMA6.

## How to use

Example:

```javascript 
class Game {
    constructor () {
        this.stateObject = {
            value1: true,
            value2: false
        }

        const state = new ObservableObject(this.stateObject, (property, value) => {
            console.log('property', property)
            console.log('value', value)
        })

        state.value1 = false
        console.log('later', state.value1)
    }
}
```