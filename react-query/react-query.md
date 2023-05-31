
# react-query
* 서버의 값을 가져오거나 값을 캐싱,업데이트,에러 등 비동기를 좀 더 쉽게 할 수 있게 도와주는 라이브러리이다.
## react-query 를 사용 하는 이유
* 값을 캐싱할 수 있다.
* 데이터가 오래 되었다고 판단되면(개발자가 지정) 다시 서버로부터 값을 받아온다.
* 데이터를 받아오지 못했을 경우, 다시 받아올 수 있다.



---
## react-query 사용법

react 환경이 구축된 곳에서 터미널에서 react-query를 세팅합니다

       npx create-react-app my-app
        cd my-app
        yarn install react-query
        yarn install && yarn start
        

react-query를 사용할 컴포넌트 상위에서 new QueryClinet() 를 선언하고,
사용할 컴포넌트들을 QueryClientProvider로 묶어주고 prop으로 선언한 QueryClient를 전달한다.

        const queryClient = new QueryClient();

                ReactDOM.render(
        <React.StrictMode>
        <QueryClientProvider client={queryClient}>
        {/* devtools */}
        <ReactQueryDevtools initialIsOpen={true} />
        <App />
        </QueryClientProvider>
        </React.StrictMode>,
        document.getElementById("root")
        );


데이터를 받아오고 싶은 컴포넌트 내부에서 useQuery api를 사용하여 데이터를 받아오고 사용법은 다음과 같습니다.

useQuery의 첫번째 인자는 key 값을 쓰고 이 key값으로 리액트 쿼리내부에 데이터를 접근할 수 있습니다.  
두번째 인자로는 비동기 함수가 들어갑니다.
세번째 인자로는 useQuery의 옵션값이 들어갑니다.
return되는 값은 비동기 함수가 성공했는지,실패했는지,데이터 값을 저장하는 객체가 반환됩니다.

        const {isLoading,isError,data} = useQuery(['key'],fetchApi,{option})



    
