##reactjs-popup-npm

<details><summary>This is a comment</summary>npm install reactjs-popup --save</details>

<details><summary>This is a comment</summary>yarn add reactjs-popup</details>


```javascript
import React from 'react';
import Popup from 'reactjs-popup';
import 'reactjs-popup/dist/index.css';

export default () => (
  <Popup trigger={<button> Trigger</button>} position="right center">
    <div>Popup content here !!</div>
  </Popup> 1 
);
