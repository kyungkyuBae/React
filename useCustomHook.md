# CustomHook
## CustomHook 를 사용해야하는 이유
로직을 재사용할 때 CustomHook을 만들어두면 코드 재사용을 할 수 있다.

---
## CustomHook 사용법


        function useNaming(){
                //원하는 기능 구현
        return // 원하는 반환 값들
        }


1. 네이밍을 할 때에는 CustomHook도 react의 Hook이기 때문에 use를 붙여서 네이밍 하는것이 가이드라인이다.  

2. 함수 내부에서 원하는 로직들을 처리하고 반환하고 싶은값들을 반환하면 된다.
