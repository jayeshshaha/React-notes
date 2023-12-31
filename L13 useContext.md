
###### things are are same here but different in ComponentC

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

-----------------------------------------------
import { Data,Data1 } from "./App";
import { useContext } from "react";

const ComponentC = () => {
    const name = useContext(Data);
    const age = useContext(Data1);
    return (
      <>
       <h1> My name is {name} & I'm {age} years old</h1>
      </>
    );
  };
  

export default ComponentC;

