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
```


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
```



## Yup-npm

<details><summary>You need to install the formik yup (using npm)</summary>npm install formik yup</details>

```javascript
import { object, string, number, date, InferType } from 'yup';

let userSchema = object({
  name: string().required(),
  age: number().required().positive().integer(),
  email: string().email(),
  website: string().url().nullable(),
  createdOn: date().default(() => new Date()),
});

// parse and assert validity
const user = await userSchema.validate(await fetchUser());

type User = InferType<typeof userSchema>;
/* {
  name: string;
  age: number;
  email?: string | undefined
  website?: string | null | undefined
  createdOn: Date
}*/
```


## React Countup

<details><summary>or install using yarn</summary>yarn add react-countup</details>

<details><summary>or install using npm</summary>npm install react-countup</details>


#### Usage

```javascript
import CountUp from 'react-countup';
```

#### Simple example

```javascript
<CountUp end={100} />
```
