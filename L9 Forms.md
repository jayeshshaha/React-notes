import { useState } from "react";

function App() {
  const[username,setUsername] = useState("");

  function handleChange(event){
     setUsername(event.target.value);
  }
  function handleSubmit(event){
     event.preventDefault(); // not to reload page
     alert(`You typed : ${username}`);
     setUsername("");
  }

  return (
    <>
      <h1>Form Demo</h1>
      <form onSubmit={handleSubmit}>
        <input type="text" value={username} onChange={handleChange}/>
        <button>Submit</button>
      </form>
    </>
  );
}

export default App;
