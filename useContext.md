# useContext
## useContext 를 사용해야하는 이유
* 하위 컴포넌트로 상태값을 전달하고 싶다면,
props로 전달하는게 일반적이지만 제일 하위에 있는 컴포넌트로 상태값을 전달하고 싶다면?
<br/> 이 경우 props로 계속해서 전달한다면 prop Drilling을 해줘야한다
<br/> 거쳐야하는 컴포넌트의 수가 많거나 전달해야하는 props이 많다면 useContext를 사용하자. 
---
## useContext 사용법
1. 우선 createContext() 함수를 사용하여 context를 만들어준다.

        const DarkModeContext = createContext()

2. 상위 컴포넌트에서 context.provider를 이용하여 전달하고자하는 하위 컴포넌트들을 감싸주고 전달할 값을 value 안에 넣어준다

        <DarkModeContext.Provider value = {{isDark,setIsDark}}>
            <div>
            </div>
        </DarkModeContext.Provider>

3.사용하고자 하는 하위 컴포넌트에서, useContext를 사용하여 상태값을 받아온다.

        const {isDark,setIsDark} = useContext(DarkModeContext) 
