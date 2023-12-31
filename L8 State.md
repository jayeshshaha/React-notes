
import { useState } from "react";

const Counter = () => {
  const [count, setCount] = useState(0);
  function increment() {
    setCount(count + 1);
  }
  function decrement() {
    setCount(count - 1);
  }
  return (
    <>
      <h1>{count}</h1>
      <button onClick={increment}>+</button>
      <button onClick={decrement}>-</button>
    </>
  );
};
function App() {
  return (
    <>
      <Counter />
    </>
  );
}

export default App;

## Updating String values in State
import { useState } from "react";

const Counter = () => {
  const [username, setUsername] = useState('Unknown');
  function changeName() {
     setUsername('lex');
  }
  
  return (
    <>
      <h1>{username}</h1>
      <button onClick={changeName}>Change Name</button>
    </>
  );
};
function App() {
  return (
    <>
      <Counter />
    </>
  );
}

export default App;

## Updating Arrays values in State
import { useState } from "react";
function App() {
  const [friends, setFriends] = useState(["alex", "dex"]);

  function addOne() {
    setFriends([...friends, "polxw"]);
  }
  function removeOne() {
    setFriends(friends.filter((f) => f !== "alex"));
  }
  function updateOne() {
    setFriends(friends.map((f) => (f === "alex" ? "alex smith" : f)));
  }

  return (
    <>
      {friends.map((f) => (
        <li key={Math.random()}>{f}</li>
      ))}

      <button onClick={addOne}>Add One</button>
      <button onClick={removeOne}>Remove One</button>
      <button onClick={updateOne}>Update One</button>
    </>
  );
}

export default App;

## Updating Object values in State
import { useState } from "react";
function App() {
  const[movie,setMovies] = useState({
    title:'Dhoom',
    ratings:7
  })
  function handleClick(){
    // const copyMovie ={
    //   ...movie,
    //   ratings:5,
    // }
    // setMovies(copyMovie);
    setMovies({...movie,ratings:10})
  }
  return <>
  <h1>{movie.title}</h1>
   <h1>{movie.ratings}</h1>
   <button onClick ={handleClick}>Change rating</button>
  </>
}

export default App;

## Updating Array Of Objects values in State
import { useState } from "react";
function App() {
  const [movies, setMovies] = useState([
    { id: 1, title: "Spiderman", ratings: 3 },
    { id: 2, title: "Superman", ratings: 5 },
  ]);

  function handleClick() {
    setMovies(
      movies.map((m) => (m.id === 1 ? { ...movies, title: "Hamburg" } : m))
    );
  }

  return (
    <>
      {movies.map((movie) => (
        <li>{movie.title}</li>
      ))}
      <button onClick={handleClick}>Change Name</button>
    </>
  );
}

export default App;
