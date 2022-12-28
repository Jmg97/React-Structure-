
**CRA, Redux Tookit, style components를 베이스로 설계**

```
PROJECT
├── .vscode/
├── node_modules/
├── package.json
├── package-lock.json
├── .eslintrc
├── .prettierrc
├── .gitignore
├── README.md
│
├── public/                        
│   ├── images/                   // 이미지 파일 폴더
│   └── data/                     // Mock 데이터 폴더
│
└── src/
	├── index.js
	├── utils.js                         // 유틸함수 정의
	├── constants.js                     // 상수데이터 정의
 	├── Router.js                 
    ├── components/                      // 공통 컴포넌트 폴더
    │   └── ComponentName/               // 공통 컴포넌트 별 폴더
    │       ├── ComponentName.jsx
    │       └── ComponentName.style.jsx  // 컴포넌트 style 정의
    │
    ├── pages/                           // 라우트에 의한 분류 페이지 폴더 	
    │   └── PageComponentName/
    │       ├── PageComponentName.jsx
    │       └── PageComponentName.style.jsx	
    │ 
    ├── styles/               	         // styled-component 스타일 폴더
    │   ├── GlobalStyle.jsx
    │   └── theme.js
    │
    ├── redux/                           // redux 폴더
    │   ├── store.js                     // redux store
    │   ├── actions/                     // 액션 정의 폴더
    │   └── reducers/                    // 리듀서 정의 폴더
    │ 
    └── hooks/                           // custom hook 폴더
```

- 컴포넌트의 이름은 PascalCase로 작성하고 그 이외는 camelCase로 작성한다.
- 공통으로 사용되는 컴포넌트 설계 시 src/components 경로에 Nav, Button 등 폴더로 관리한다. 
- 공통 컴포넌트는 충분한 소통을 통해 필요한 Props를 고려하여 작성한다.
- pages에서는 라우트에 의한 페이지별 컴포넌트를 작성한다. 각 페이지에서 개별로 필요한 컴포넌트는 각 페이지 폴더 안에 작성한다.

- styles 폴더는 styled-components의 전역 스타일, reset css, theme을 작성한다.

- 각 컴포넌트 스타일은 동일 경로에 스타일만 따로 정의하는 파일(ComponentName.style.jsx)을 생성하여 컴포넌트 파일에서 임포트 해서 사용한다. 스타일 파일을 분리함으로써 코드의 가독성이 올라간다.

- 자주 사용되는 로직이나 상수 데이터의 경우도 따로 constants, util, hooks에 작성하여 임포트하여 작성한다.


