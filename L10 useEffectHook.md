import { useEffect, useState } from "react";

function App() {
  const [value, setValue] = useState(0);

  // 1.Reder for the (first time) all of the code will be executed under useEffect
  // 2.Anytime we do (side effect)
  // 3. Dependancy
  // if condition shuld never be used outside useEffect

  useEffect(() => {
    // if(value>0){
    console.log("hello world");
    document.title = `Increment(${value})`;
    // }
  },[value]);
  return (
    <>
      <h1>{value}</h1>
      <button
        onClick={() => {
          setValue(value + 1);
        }}
      >
        Click Me
      </button>
    </>
  );
}

export default App;


## 2nd example fetch

import { useEffect, useState } from "react";

function App() {
  const [data, setData] = useState([]);

  // 1.Reder for the (first time) all of the code will be executed under useEffect
  // 2.Anytime we do (side effect)
  // if condition shuld never be used outside useEffect

  useEffect(() => {
    async function getData() {
      const response = await fetch(
        "https://jsonplaceholder.typicode.com/posts"
      );
      const data = await response.json();

      if (data && data.length > 0) setData(data);
    }
    getData();
  }, []);
  return (
    <>
      <ul>
        {data.map((item) => (
          <li key={Math.random()}>{item.title}</li>
        ))}
      </ul>
    </>
  );
}

export default App;