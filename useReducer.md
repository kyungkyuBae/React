# useReducer
## useReducer 를 사용해야하는 이유
* useState 보다 관리할 상태가 여러가지라면 useReducer를 사용하면 
코드가 깔끔하고 한눈에 알아보기 쉽다.
* 로직을 따로 빼내어 재사용성이올라간다.
---
## useReducer 사용법

    const [<상태 객체>, <dispatch 함수>] = useReducer(<reducer 함수>, <초기 상태>, <초기 함수>)

* 상태객체는 이 변수의 값이 변할때마다 화면에 반영되게 하고 싶은 변수이다
* dispatch는 상태객체를 변하게하려면 이 함수를 호출해야 한다
* reducer 함수는 dispatch로 호출했을 때 로직에 따라 상태객체를 변하게 하는 함수이다
* 초기상태는 처음 화면에 출력되었을때 상태객체의 값이다.
