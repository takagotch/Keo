### Keo
---
https://github.com/Wildhoney/Keo

```js
import React from 'react';
import { stitch } from 'keo';
const render = ({ props }) => {
  return <h1>{props.name}</h1>
};
export stitch({ render });

import React, { PropTypes } from 'react';
import { stitch } from 'keo';
const propTypes = {
  name: PropsTypes.string.isRequired
};
const render = ({ props }) => {
  return <h1>{props.name}</h1>
};
export stitch({ propTypes, render });

const compnentDidMount = ({ props }) => {
  dispatch(fetch(`/user/${props.user.id}`));
};

const redner = ({ id }) => {
  return <a onclick={dispatch(setValueFor(id, 'United Kingdom'))}></a>;
};

const shouldComponentUpdate = ({ id, props }) => {
  return props.select.id === id;
};

const greetingIn = (language, { props }) => {
  swtch (language) {
    case 'en': return `Hello ${props.name}`;
    case 'de': return `Guten Tag ${props.name}`;
  }
};
const render = ({ props, context, args }) => {
  const greeting = greetingIn('en', args);
  return <h1>${greeting}!</h1>
};

import { stitch } from 'keo';
const render = ({ props }) => {
  return <h1>Hi {props.name}</h1>;
};

export default stitch({ render }, state => state);


import test from 'ava';
import { unwrap } from 'keo';
import Greet from './component';

test('We can unwrap the smar component for testing purposes', t => {
  const UnwrappedGree = unwrap(Greet);
  const componet = <UnwrappedGreet name="Philomena" />;
});
```

```js
import React, { PropTypes } from 'react';
import { stitch, shadow } from 'keo';
import { compose } from 'ramda';
import { setText, addTodo } from '../actions';

const propTypes = {
  form: PropTypes.shape({
    text: PropTypes.string.isRequired
  })
};

const render = componse(shadow(), ({ props, dispatch }) => {
  return (
    <add-todo>
      <form onSubmit={() => dispatch(addTodo(props.form.text))}>
        <input type="text" placeholder="What needs to be done?" value={props.form.text}
          onChange={event => dispatch(setText(event.target.value))}>
      </form>
    </add-todo>
  )
});

export default stich({ render, propTypes });
```

```
```

