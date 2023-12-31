function App() {
  return (
    <>
      <Child name="jayesha" age={24}>
        <p>lorem epsom peacres</p>
      </Child>
    </>
  );
}

function Child({ name, age, children }) {
  return (
    <section>
      <h1>Name is : {name}</h1>
      <h1>Age is : {age}</h1>
      {children}
    </section>
  );
}

export default App;
