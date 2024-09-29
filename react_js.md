## Reactjs-popup-npm

<details><summary>You need to install the reactjs-popup (using npm)</summary>npm install reactjs-popup --save</details>

<details><summary>or install using yarn</summary>yarn add reactjs-popup</details>


```javascript
import React from 'react';
import Popup from 'reactjs-popup';
import 'reactjs-popup/dist/index.css';

export default () => (
  <Popup trigger={<button> Trigger</button>} position="right center">
    <div>Popup content here !!</div>
  </Popup> 1 
);


## React-toastify-npm

<details><summary>You need to install the react-toastify (using npm)</summary>npm install --save react-toastify</details>

<details><summary>or install using yarn</summary>yarn add react-toastify</details>


```javascript
import React from 'react';

  import { ToastContainer, toast } from 'react-toastify';
  import 'react-toastify/dist/ReactToastify.css';
  
  function App(){
    const notify = () => toast("Wow so easy!");

    return (
      <div>
        <button onClick={notify}>Notify!</button>
        <ToastContainer />
      </div>
    );
  }
