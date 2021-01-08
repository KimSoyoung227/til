# node.js Express framework?

- express란? 
웹 서버 필요한 뼈대를 구축해놓은 프레임워크
cf) Koa, Hapi 등

- 디렉터리 구조

express

    ㄴpackage.json

    ㄴpulic
        ㄴcss 

        ㄴstyle.css

    ㄴrouter
        ㄴmain.js

    ㄴserver.js

    ㄴviews
        ㄴabout.html 

        ㄴindex.html


- 설치방법

npm install express

- 파일 분류
 * package.json : 프로그램 이름, 버전, 모듈 등 노드 프로그램의 정보를 입력

 * bin/www : 서버 구동을 위한 파일. express 서버 설정 코드가 작성된 app.js를 가져와 http 객체와 연동하는 소스

 * app.js : bin/www에서 사용하며 express 설정 파일이 담겨있는 핵심코드.
  
 * /routes : 라우팅을 위한 폴더

 * /public : 정적파일을 위한 폴더

 * /views : 템플릿 파일 
