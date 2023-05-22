# useCallback
## useCallback 를 사용해야하는 이유
* 우선 react에서 re-rendering 이 발생하는 조건에는,  
        - 내부 상태 변경시  
        - prop 값 변경시  
        - 부모컴포넌트가 re-rendering 될 때  
이렇게 re-rendering 될때 useMemo를 사용한다면 불필요한 연산을 줄이고 최적화하여 re-rendering을 할 수 있다.(성능향상)
---
## useMemo 사용법


        useCallback(fn, [])


1. useCallback은 처음 랜더링 될때 fn를 반환해주고, [] dependencies 값이 변경될때만 값이 재할당된다.

* <span style="color:red">따로 메모리를 할당해서 저장해놓기 때문에 필요없는 값까지 광범위한 메모리를 저장하게 되는 무분별한 사용은 오히려 성능을 감소시키기때문에 적절한 사용이 필요하다  </span>
