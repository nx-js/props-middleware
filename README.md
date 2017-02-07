# The props middleware

The `props` allows you to inject data into reusable components.

- name: props
- middleware dependencies: [attributes](https://github.com/nx-js/attributes-middleware)
- all middleware dependencies: [observe](https://github.com/nx-js/observe-middleware), [attributes](https://github.com/nx-js/attributes-middleware)
- processes: element nodes
- throws on: text nodes
- use as: component middleware
- [docs](http://nx-framework.com/docs/middlewares/props)

## Installation

`npm install @nx-js/props-middleware`

## Usage

```js
const component = require('@nx-js/core')
const observe = require('@nx-js/observe-middleware')
const attributes = require('@nx-js/attributes-middleware')
const props = require('@nx-js/props-middleware')

component()
  .use(observe)
  .use(attributes)
  .use(props('name', 'age', 'items'))
  .register('props-comp')
```

```html
<props-comp name="Bob" age="12" @items="myItems">Hello World!</props-comp>
```
