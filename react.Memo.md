# react.memo
## react.memo 를 사용해야하는 이유
* 하위컴포넌트의 불필요한 re-rendering을 막고싶다면 react.memo를 사용해보자
---
## useMemo 사용법


        import {memo} from 'react'


1. 우선 memo를 import 시켜준다.

        memo(Component);

2. 컴포넌트를 memo로 감싸준다.

---

- 랜더링이 될 상황에 놓였을 때 prop check 를 통해서 prop의 값이 변하지 않았다면, 이전값을 재사용하게 된다.
