import ComponentC from "./ComponentC";

// 1) Import (createContext)
import { createContext } from "react";
// 2) Creating instance of (createContext)
export const Data = createContext();

function App() {
  const name = "Jayesh";

  return (
    // 3)Wrap our componenet into proivder component
    <>
      <Data.Provider value={name}>
        <ComponentC />
      </Data.Provider>
    </>
  );
}

export default App;

----------------------------------------

import { Data } from "./App";
<!-- ! So in short if i say what i  have learnt that Data.Consumer expects a callbackfnc because in Data.Provider  we have the passed the value -->
const ComponentC = () => {
  return (
    <>
      <Data.Consumer>
        {(name) => {
          return <h1>My name is: {name}</h1>;
        }}
      </Data.Consumer>
    </>
  );
};

export default ComponentC;


----------------------------------------
## 2nd example 

----------------------------------------

import ComponentC from "./ComponentC";

// 1) Import (createContext)
import { createContext } from "react";
// 2) Creating instance of (createContext)
export const Data = createContext();
export const Data1 = createContext();

function App() {
  const name = "Jayesh";
  const age =23;

  return (
    // 3)Wrap our componenet into proivder component
    <>
      <Data.Provider value={name}>
       <Data1.Provider value={age}>
        <ComponentC />
        </Data1.Provider>
      </Data.Provider>
    </>
  );
}

export default App;

----------------------------------------
import { Data,Data1 } from "./App";

const ComponentC = () => {
    return (
      <>
        <Data.Consumer>
          {(name) => {
            return (
              <>
                <h1>My name is: {name}</h1>
                <Data1.Consumer>
                  {(age) => {
                    return <h1>My age is {age}</h1>;
                  }}
                </Data1.Consumer>
              </>
            );
          }}
        </Data.Consumer>
      </>
    );
  };
  

export default ComponentC;
