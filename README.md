#context tutorial

start...

##1.First context folder banailm .. 

##2. j context folder banailm tar vtr 2 ta file banalm 

##3. 1st file er name  Contextmain.js and 2nd contextState.js

##4.Contextmain.js r vtr kaj

        import {createContext} from 'react';

        const ContextMain = createContext()

        export default ContextMain;


##5.ContextState.js r kaj :

        import ContextMain from "../contextmain/ContextMain"


        const ContextState = (props) => {
            return (
                <ContextMain.Provider value="nayeem">

                    {props.children}
                    
                </ContextMain.Provider>
            );
        };

        export default ContextState;



##6.app.js r vtr j routing kora sekhne ContextState.js import krlm .

##7.jader vtr context value pass krte chai tdr <ContextState> deye rep
 kore dete hbe...

 example :
        
        
      <ContextState>
          <Route path="/user">
            <Users />

          </Route>
          <Route path="/">
            <Home />
          </Route>
     </ContextState>


##8. <User /> ei khne context use krte chai ..

##9.thle 2 ta jnis import krte hbe ...useContext and amra j ContextMain file create krchi....

    a. import {useContext} from 'react';
    b. import ContextMain from "../../components3/context/contextmain/ContextMain"


##10 .let a = useContext(ContextMain) akta veriable create kore useContext r vtr ContextMain deye dete hbe...

##11.now console.log(a) 

finish...
