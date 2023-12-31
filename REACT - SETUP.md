-------------------------------------------------------------------------------------
<!-- * Public folder - index.html -->
-------------------------------------------------------------------------------------

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <link rel="icon" href="%PUBLIC_URL%/favicon.ico" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <meta name="theme-color" content="#000000" />
  
  
    <title>React App</title>
  </head>
  <body>
    <noscript>You need to enable JavaScript to run this app.</noscript>
    <div id="root"></div>
   
  </body>
</html>

-------------------------------------------------------------------------------------
<!-- * Src folder - App.js  -->
-------------------------------------------------------------------------------------


function App() {
  return <></>;
}

export default App;

-------------------------------------------------------------------------------------
<!-- * Src folder - index.js  -->
-------------------------------------------------------------------------------------


import React from "react";
import ReactDOM from "react-dom/client";
import App from "./App";

const root = ReactDOM.createRoot(document.getElementById("root"));
root.render(<App />);


-------------------------------------------------------------------------------------
 <!-- * Emmet Setting -->
-------------------------------------------------------------------------------------

Settings search - emmet
under this =>n Emmet: Include Languages 
put key = javascript
put value = javascriptreact


or

 "emmet.includeLanguages": {
        "javascript": "javascriptreact"
      },