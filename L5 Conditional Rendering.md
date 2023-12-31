
1)
Since we are using jsx we need to use return and to render that particular component return before  it

const ValidPassword = () => <h1>Valid Password</h1>
const InvalidPassword = () => <h1>Valid Password</h1>

const Password = ({isValid})=>{
 if(isValid){
   return <ValidPassword/>
 }
 else{
   return <InvalidPassword/>
 }
}


function App() {
 return <>
 <Password isValid = {true} />
 </>;
}


export default App;

2)

const Cart = ()=>{
 const items = ['Wire','PowerBuds','Hoodies']


 return <>
   <h1>Card</h1>
 {items.length > 0 && <h1>You have {items.length} in your cart</h1>}
   <ul>
     <h4>Products</h4>
     {items.map(item=>(
       <li key={item}>{item}</li>
     ))}
   </ul>
 </>
}

function App() {
 return <>
  <Cart/>
 </>;
}
export default App;

3)

const ValidPassword = () => <h1>Valid Password</h1>;
const InvalidPassword = () => <h1>Invalid Password</h1>;


const Password = ({ isValid }) => {
 return isValid ? <ValidPassword /> : <InvalidPassword />;
};


function App() {
 return (
   <>
     <Password isValid={false} />
   </>
 );
}

