# useImmer
## useimmer 를 사용해야하는 이유
* 간단한 상태관리가 아니라면, useState 보다 useImmer를 사용하여 
보다 간단하게 불변성을 유지하면서 상태를 업데이트 할 수 있다.
---
## useImmer 사용법

    const [<상태 객체>, <상태객체 업데이트함수>] = useImmer(상태객체 초기값)

* 상태객체는 이 변수의 값이 변할때마다 화면에 반영되게 하고 싶은 변수이다.

* 상태객체업데이트함수는 상태객체를 값을 변화하여 업데이트를 시켜줄 로직을 담고 있는 함수이다. (상태객체의 변수명을 person 이라고 하였다면 상태객체 업데이트함수명은 주로 update를 붙여 updatePerson 으로 주로 작명함)

* 상태객체 초기값은 처음 화면에 출력되었을때 상태객체의 값이다.
