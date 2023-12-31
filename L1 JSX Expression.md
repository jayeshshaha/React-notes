function App() {
  const name = "jayesh";
  const mul = (a, b) => {
    return a * b;
  };
  const specialclass = "simple-class";
  return (
    <>
      <h1>{name}</h1>
      <h1>{2 + 2}</h1>
      <p>2 * 2 = {mul(2, 4)}</p>
      <p className={specialclass}>This is a simple class</p>
    </>
  );
}