# React Multi Select Component

React Multi Select Component

![Animated GIF demo](react-multi-select.gif)

[Storybook Demo](https://khan.github.io/react-multi-select/)

## Installation:
`npm install --save @khanacademy/react-multi-select`
`yarn add @khanacademy/react-multi-select`

## Usage:
See the examples in `/src/stories/index.js` for how to use the component, but here is a minimum required setups:

```
import React from 'react';
import MultiSelect from "@khanacademy/react-multi-select";

const options = [
  {label: "One", value: 1},
  {label: "Two", value: 2},
  {label: "Three", value: 3},
];

class Consumer extends React.Component {
  state = {
    selected: [],
  }

  render() {
    const {selected} = this.state;

    return <MultiSelect
      options={options}
      selected={selected}
      onSelectedChanged={selected => this.setState({selected})}
    />
  }
}
```


## i18n:
You can override the strings to be whatever you want, including translations for your languages.

```
<StatefulMultiSelect
    overrideStrings={{
        selectSomeItems: "Select Some items...",
        allItemsAreSelected: "All Items are Selected",
        selectAll: "Select All",
        search: "Search",
    }}
/>
```
# Developer Notes
## To Run Example:
`npm run storybook`

## To Create/Update Distribution (dist) Folder:
## For Widows 
1. Update the `prepublish` path in package.json file to absolute path of `.scripts/prepublish.sh` file. Example `C:/Users/Admin/**/**/react-multi-select/.scripts/prepublish.sh`
2. Then run the command `npm run prepublish` in terminal to regenerate dist folder.

## For MAC
1. Update the `prepublish` path in package.json file to `. ./.scripts/prepublish.sh`.
2. Run the command `npm run prepublish` in terminal to regenerate dist folder.