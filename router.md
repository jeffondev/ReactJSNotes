# Router
## install

```
npm i react-router-dom
```  

<br/>

## 프로젝트에 라우터 적용
* index.js에 `<App />`을 `<BrowserRouter>`로 감쌈
```js
import { BrowserRouter } from 'react-router-dom';

ReactDOM.render(
  <BrowserRouter>
    <App />
  </BrowserRouter>, 
  document.getElementById('root')
);
```

* import 해서 사용
```js
import { Routes, Route, Link, useNavigate, Outlet, Redirect, Navigate} from 'react-router-dom';
```

<br/>

## 사용법
1. Route 컴포넌트로 특정 경로에 컴포넌트 보여주기
```js
<Routes>
  <Route path="/" element={<Seeds />} />
</Routes>
```

2. Link 컴포넌트를 사용해 페이지 이동버튼 보여주기
```js
<Link to="/">홈으로 이동</Link>
```

3. Navigate 컴포넌트로 페이지 이동
```js
<Navigate to={"/seeds"}/>
```

4. 아이디 경로ㅗ로롤
```js
<Route path='/seeds/:id?' element={
            
  <Seeds seed={seed} />
} />
```

5.  Route와 Navigate 컴포넌트 함께 쓰기
```js
<Route path='/' element={<Navigate to={"/seeds"}/>}/>
///어떤 주소든 /seeds로 이동,표시
```