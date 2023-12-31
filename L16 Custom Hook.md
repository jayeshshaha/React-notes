import { useState, useEffect } from "react";

function App() {
  const [data, setData] = useState(null);
  useEffect(() => {
    fetch("https://jsonplaceholder.typicode.com/todos")
      .then((r) => r.json())
      .then((d) => setData(d));
  });
  return(
  <>
    {data &&
      data.map((item) => {
        return <p key={Math.random()}>{item.title}</p>;
      })}
  </>
  )
}

export default App;
-------------------------------------------

import { useState,useEffect } from "react";

const useFetch = (url) =>{
    const [data, setData] = useState(null);
    useEffect(()=>{
       fetch(url)
       .then(r => r.json())
       .then((d)=>setData(d))
    },[url])
    return [data];
}

export default useFetch;


--------------------------------------------

## exporting the custom hook in this main component
import useFetch from "./useFetch";

function App() {
  const [data] = useFetch("https://jsonplaceholder.typicode.com/todos");
 
  return(
  <>
    {data &&
      data.map((item) => {
        return <p key={Math.random()}>{item.title}</p>;
      })}
  </>
  )
}

export default App;
