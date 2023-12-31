function App() {
  return (
    <>
      <Child name="jayesh"
      age = {23} />
    </>
  );
}

function Child(props) {
  return (
    <section>
      <h1>Name is : {props.name}</h1>
      <h1>Age is : {props.age}</h1>
    </section>
  );
}

export default App;

------------------------------------------------------------------------------------
function App() {
  return (
    <>
      <Child name="jayesha"
      age = {23} />
    </>
  );
}

function Child(props) {
 const { name , age} = props;
  return (
    <section>
      <h1>Name is : {name}</h1>
      <h1>Age is : {age}</h1>
    </section>
  );
}

export default App;

------------------------------------------------------------------------------------

function App() {
  return (
    <>
      <Child name="jayesha"
      age = {24} />
    </>
  );
}

function Child({name,age}) {
  return (
    <section>
      <h1>Name is : {name}</h1>
      <h1>Age is : {age}</h1>
    </section>
  );
}

export default App;



