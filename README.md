# useContext(React Hook) 사용해보기
userContext훅 사용하기 위한 준비
```jsx
import React, {useState, useContext} from "react";
```
```jsx
const ColorContext = React.createContext(null);
```  
<br/>
ColorContext.Provider을 통해 value 값 전달
<br/><br/>

```       jsx
<ColorContext.Provider
         value={{
             isDark,
             setIsDark
         }}>
      <Page/>
 </ColorContext.Provider>
  ```
 
<br/>
Provider을 통한 value값 사용  <br/>


```jsx
const {isDark, setIsDark} = useContext(ColorContext);
    const toggleColor = () => {
       setIsDark(!isDark);
 }
```
