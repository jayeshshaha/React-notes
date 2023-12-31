import ComponentA from "./ComponentA";

function App() {
  const name = "Jayesh";

  return (
    <>
      <ComponentA name={name} />
    </>
  );
}

export default App;
---------------------------------------
import ComponentB from "./ComponentB";

const ComponentA = ({ name }) => {
  console.log(name);
  return (
    <>
      <ComponentB name={name} />
    </>
  );
};

export default ComponentA;

---------------------------------------
import ComponentC from "./ComponentC";

const ComponentB = ({ name }) => {
  return (
    <>
      <ComponentC name={name} />
    </>
  );
};

export default ComponentB;

---------------------------------------
const ComponentC = ({ name }) => {
  return <div>this data is getting from ComponentA {name}</div>;
};

export default ComponentC;

