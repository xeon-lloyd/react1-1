# 전동환 202030129  

<br>


## 3월 27일 강의 내용  
### JSX
JavaScript XML  
javascript에 xml을(태그)를 추가한 확장문법 - 가독성 좋아짐  
내부적으로 XML/HTML 코드를 자바스크립트로 변환 *(createElement 함수로)*  
javascript 코드를 사용하고 싶다면 {} 안에서 사용 *(변수명 출력에 자주 사용)*
  

### 컴포넌트 만들기
#### class형 *(React.Component 상속)*
```jsx
class Hello extends React.Component {
    render(){
        return <div>Hello {this.props.toWhat}</div>
    }
}

export default Hello
```

#### function 형
```jsx
export default function Book(props){
    return (
        <div>
            <h1>{`이 책의 이름은 ${props.name}입니다.`}</h1>
            <h1>{`이 책은 총 ${props.numOfPage}페이지로 이뤄져 있습니다.`}</h1>
        </div>
    )
}
```

#### prop 전달
```jsx
<Hello toWhat="world" />
```


### 엘리먼트
리액트 앱의 가장 작은 빌딩 블록들  
Virtual DOM 형태를 취함

||DOM|Virtual DOM|
|---|---|---|
|업데이트 속도|느리다|빠르다|
|element<br>업데이트 방식|DOM 전체를 업데이트|변화 부분을 가상 DOM으로 만든 후<br>DOM과 비교하여 다른 부분만 업데이트|
|메모리|낭비가 심함|효율적|

#### 엘리먼트의 불변성
한 번 생성된 엘리먼트의 children이나 속성은 바꿀 수 없음  
-> 만약 내용이 바뀐다면  
 컴포넌트를 통해서 새로운 엘리먼트 생성 후 이전 엘리먼트와 교체하는 방법  


### root DOM node
```<div id="root"></div>``` html 코드 필수  
이 div 태그안에 리액트 엘리먼트가 렌더링됨  
  
```jsx
const element = <h1>안녕, 리액트!</h1>
ReactDOM.render(element, document.getElementById('root'))
```
엘리먼트를 렌더링하려면 위 코드가 필요 *(```render()``` 함수 이용)*


### 주의사항
element를 정의할때는 무조건 최종적으로 1개의 태그만 리턴되게 하야함
```jsx
const elemet = (
    <div>
        <h1>안녕, 리액트</h1>
        <h2>다른 태그</h2>
    </div>
)
```
*여기서 div를 묶어서 2개의 태그를 내보내는 것 처럼


<br>

## 3월 20일 강의 내용  
### 리액트(React)
복잡한 사이트를 쉽고 빠르게 만들고, 관리하기 위해 만들어진 것  
SPA(Single Page Application)를 쉽고 빠르게 만들 수 있도록 함  

#### 장점
**1. 렌더링이 빠름**  
Virtual DOM을 사용. *(기존 DOM 조작의 비효율적, 느려서 고안됨)*  
|DOM|Virtual DOM|
|---|---|
|동기식|비동기식|
|변화된 부분이 있으면 전체 refresh|바뀐 부분만 변경|

**2. 컴포넌트 기반 구조**  
리액트의 모든 페이지는 컴포넌트로 구성  
컴포넌트는 다른 여러개의 넘포넌트로 구성가능  
&nbsp;&nbsp; → **재사용성**이 높아 생산성이 높음 *(유지보수 용의)*  
※ 재사용이 가능하려면 모듈의 의존성이 없어야함  

**3. 기타맨**  
 - 든든한 지원군: 메타에서 오픈소스로 꾸준히 관리
 - 활발한 지식공유 & 커뮤니티(사용자가 많음)
 - 모바일 앱 개발 가능 (크로스 플랫폼)

#### 단점
1. **방대한 학습량**: 러닝커브가 높음
2. **높은 상태 관리 복잡도**: state, component life ctyle...

<br>

### 프로젝트
#### 리액트 앱 만들기
```bash
npx create-react-app my-app
```

#### 실행하기
```bash
npm start
```

#### 기타
컴포넌트 이름(파일이름)은 대문자로 시작  


<br>

## 3월 13일 강의 내용  
### GitHub 사용법  
```bash
git config --global user.email "흠흐밍@밍.흠"
git config --global user.name "흠흐밍"
```
--global떼면 폴더마다 설정가능  
값 안주면 설정된 값 확인  


### html 톺아보기  
**SPA(single page application)**  
 - 무한 스크롤 *(유튜브, 인스타 등: 필요할때 컨텐츠 로드)*
 - 웹 애플리케이션 *(크로스플랫폼 가능)*

