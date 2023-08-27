# ContextAPITempelate

import React, {
  createContext,
  useContext,
  useEffect,
  useReducer,
  useState,
} from "react";

export const Appcontext = createContext();
//Custom Hook
export const useGlobalContext = () => useContext(Appcontext);
export const ContextProvider = (props) => {
  const [load, setLoad] = useState("Faheem ");
  return (
    <Appcontext.Provider value={{ load }}>
        {props.children}
    </Appcontext.Provider>
  );
};


// const {load}= useGlobalContext();  in app.js 
