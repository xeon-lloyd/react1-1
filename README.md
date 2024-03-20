# 전동환 202030129  

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

