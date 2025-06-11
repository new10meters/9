App.js

import React from 'react'; 
import { BrowserRouter as Router, Route, Routes } from 'react-router-dom'; 
import Navbar from './components/Navbar'; 
import Home from './components/Home'; 
import About from './components/About'; 
import Contact from './components/Contact'; 
function App( ){ 
return ( 
<Router> 
<div> 
<Navbar /> 
<div className="content"> 
<Routes> 
<Route path="/" element={<Home />} /> 
<Route path="/about" element={<About />} /> 
<Route path="/contact" element={<Contact />} /> 
</Routes> 
</div> 
</div> 
</Router> 
); 
}; 
export default App; 
 
 
About.js 
 
import React from'react'; 
function About { 
 return ( 
  <div> 
   <h1>About Us</h1> 
   <p>Learn more about us on this page.</p> 
  </div> 
 ); 
}; 
export default About; 

 
Contact.js 
 
import React from'react'; 
function Contact { 
 return ( 
  <div> 
   <h1>Contact Us</h1> 
   <p>Get in touch with us here!</p> 
  </div> 
 ); 
}; 
export default Contact; 

 
Home.js 
 
import React from'react'; 
function Home { 
 return ( 
  <div> 
   <h1>Welcome to the Home Page!</h1> 
   <p>This is the home page of our simple React application.</p> 
  </div> 
 ); 
}; 
export default Home; 

 
Navbar.js 
 
import React from'react'; 
import { NavLink } from'react-router-dom'; 
function Navbar { 
 return ( 
  <nav> 
   <ul> 
    <li> 
     <NavLinkto="/" exactactiveClassName="active"> 
      Home 
     </NavLink> 
    </li> 
    <li> 
     <NavLinkto="/about" activeClassName="active"> 
      About 
     </NavLink> 
    </li> 
    <li> 
     <NavLinkto="/contact" activeClassName="active"> 
      Contact 
     </NavLink> 
    </li> 
   </ul> 
  </nav> 
 ); 
}; 
export default  Navbar; 
 
 
App.css 
body { 
font-family: Arial, sans-serif; 
background-color: #f4f4f4; 
margin: 0; 
padding: 0; 
} 
 
div { 
max-width: 960px; 
margin: 0auto; 
padding: 20px; 
} 
 
h2 { 
color: #333; 
margin-bottom: 20px; 
} 
 
nav { 
background-color: #333; 
padding: 10px; 
border-radius: 5px; 
margin-bottom: 20px; 
} 
ul { 
list-style: none; 
display: flex; 
gap: 15px; 
justify-content: center; 
margin: 0; 
padding: 0; 
} 
a { 
text-decoration: none; 
color: white; 
padding: 8px16px; 
border-radius: 4px; 
} 
a:hover { 
background-color: #444; 
} 
a.active { 
background-color: #1e90ff; 
font-weight: bold; 
} 
