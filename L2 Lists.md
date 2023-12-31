const items = [{
  name: "jayesh",
  age: 24,
  id:1
},
{
  name: "alex",
  age: 25,
  id:2
},
{
  name: "dex",
  age: 26,
  id:3
}];

function App() {
  return (
    <>
      {items.map(item => (
        <li key={item.id}>Name : {item.name} & Age : {item.age}</li>
      ))}
    </>
  );
}

export default App;
