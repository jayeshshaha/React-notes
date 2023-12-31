
1)

function App() {
  return (
    <>
     <h1 style={{color:'red',backgroundColor:'blue'}}>Hello</h1>
    </>
  );
}

export default App;

2)

function App() {
  const stylying = {
    color: 'red',
    backgroundColor: 'blue',
    padding: '10px'
  }
  return (
    <>
     <h1 style={stylying}>Hello</h1>
    </>
  );
}

export default App;

3)

import './index.css'

4)
BootStrap
import 'bootstrap/dist/css/bootstrap.min.css'; // this in index.js file 

5)
TailWind CSS
