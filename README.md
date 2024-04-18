# React Router Project Starter
Before running install the node modules package

**App.js**
In app.js Routes are created to navigate through to different part of the website using Routes method without causing a reload of pages.
The parent route set by default is Home and its children routes are
1) Login
2) Signup
3) Dashboard

Note the dashboard can be only navigated if the user is logged in which is determined by a hook defined isLoggedIn which keeps track of the user login's. Initially its value is set to false.

**PrivateRoute**
If you try to maually go to '/dashboard' with URL you will be navigated to login page because Dashboard component is defined inside component name PrivateRoute.
PrivateRoute checks whether the user isLoggedIn and only if he is, then he can be allowed to dashboard content.

**Navbar.js**
Navbar consist of image which when clicked takes you to login page,which defined with help of <Link>
Three more links are created 
1)Home
2)About
3)Contact
Currently, all of them traverse to the same link as of now i didnt put any content
There are 4 buttons in Navbar
1)SignUp 2)LogIn 3)LogOut 4)Dashboard
If the user is not logged in then then 1 and 2 buttons are only displayed otherwise 3 and 4 are diplayed whose functionality is design using concept of useState 

**SignupForn.js, LoginForm.js and Template.js**
The only difference between these two components was diffrent format of forms in them so to make it reusable, I designed a common Template component which uses the tenary operator to decide whether SignUp or LoginForm should be displayed.

**Home.js, Login.js, Signup.js and Dashboard.js**
In these components I have the actual parameters value that need to be displayed on page that is passed to Template.js


