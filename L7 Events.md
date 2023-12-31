const Button = ()=>{
  function handleClick(){
    console.log('Clicked');
    alert('You clicked me')
  }
   return <button onClick={handleClick}>Click</button>
}

function App() {

  return (
    <>
    <Button/>
    <h1>Sample</h1>
    </>
 );
}

export default App;


------------------------------------------

const Button = ()=>{
  function handleClick(a,b){
    console.log(a+b);
  }
   return <button onClick={()=>handleClick(2,2)}>Click</button>
}

function App() {

  return (
    <>
    <Button/>
    </>
 );
}

export default App;

------------------------------------------
const Copy = () => {
  function copyHandler() {
    alert("Stop stealing my content");
  }
  return (
    <>
      <p onCopy={copyHandler}>ansfm amksfnjkajkbsfa anfsjnajfbas aksnjknfa </p>
    </>
  );
};
function App() {
  return (
    <>
      <Copy />
      <h1>sada</h1>
    </>
  );
}

export default App;

------------------------------------------

const Move = () => {
  function moveHandler() {
    alert("Stop stealing my content");
  }
  return (
    <>
      <p onMouseMove={moveHandler}>ansfm amksfnjkajkbsfa anfsjnajfbas aksnjknfa </p>
    </>
  );
};
function App() {
  return (
    <>
      <Move />
      <h1>sada</h1>
    </>
  );
}

export default App;

