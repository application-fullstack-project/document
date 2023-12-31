# 윈도우에서 NestJS 서버 개발환경 설정하기

Windows 10 환경에서 NestJS 개발환경을 설정해 보겠습니다. 해당 문서의 작성일은 2023년 9월이므로, 변경된 내용이 존재할수 있습니다.

여기에 소개되는 프로그램들은 모두 Windows를 위한 프로그램이 아닌 리눅스를 위한 프로그램입니다. 처음에는 WSl이라는 윈도우에서 리눅스를 가상으로 실행할 수 있게 안내하려고 했으나, 난이도가 높아질 것 같아 Windows에서 바로 설치하는 방법을 소개하겠습니다.

혹시나 해서 설치 중간에 오류가 났을 시 확률이 높은 문제를 정리해 보았습니다.

- 사용자 이름이 한글인 경우 : 사용자 이름을 영문으로 바꾸는 것을 권장합니다.
- 프로그램 설치 후 정상작동이 안되는 경우 : 재부팅을 해보시고, 그래도 안되면 프로그램을 삭제하고 다시 설치해 보시기 바랍니다.


1. Node.js 설치하기
공식 홈페이지에서 설치하겠습니다. 설치는 아래의 링크에서 다운로드 받아 설치하면 됩니다. 이 때 좌측의 LTS 버전을 설치하시면 됩니다. LTS 버전은 오랫동안 지원하고 가장 안정적인 버전입니다.

https://nodejs.org/ko

<!-- ![Node.js 다운 화면](image/1.png) -->
<img src="image/1.png" width="500px">

설치 과정은 어렵지 않고, 권장사항대로 설치 하시면 되겠습니다. 혹시 모르니 설치 과정의 사진들을 첨부하겠습니다.

<!-- ![Node.js 설치 화면](image/2.png)
![Node.js 설치 화면](image/3.png)
![Node.js 설치 화면](image/4.png)
![Node.js 설치 화면](image/5.png)
![Node.js 설치 화면](image/6.png)
![Node.js 설치 화면](image/7.png)
![Node.js 설치 화면](image/8.png) -->
<img src="image/2.png" width="500px">
<img src="image/3.png" width="500px">
<img src="image/4.png" width="500px">
<img src="image/5.png" width="500px">
<img src="image/6.png" width="500px">
<img src="image/7.png" width="500px">
<img src="image/8.png" width="500px">

설치가 완료되면, powershell 창에서 node -v 명령어를 입력해 버전을 확인해 보겠습니다. 정상적으로 버전이 뜬다면, 설치가 잘 된 것입니다. powershell는 윈도우키 + R을 눌러서 실행창을 띄우고 powershell를 입력하면 실행할 수 있습니다.

<!-- ![Node.js 설치 확인](image/9.png) -->
<img src="image/9.png" width="500px">

Mac에서는 nvm을 설치하고 node를 실행하지만, Windows에서는 바로 Node를 설치하는 것이 빠른 개발환경 구축에 도움이 되어서 이러한 방법으로 소개했습니다.

1. vscode 설치하기

vscode를 설치해 보겠습니다. 아래의 공식 홈페이지에서 자신의 컴퓨터에 맞는 설치파일(Windows)을 받아서 실행합니다.

https://code.visualstudio.com/download

<!-- ![vscode 설치 홈페이지](image/10.png) -->
<img src="image/10.png" width="500px">

vscode 또한 권장 사항에 맞게 설치하시면 됩니다. 

<!-- ![vscode 설치 화면](image/11.png)
![vscode 설치 화면](image/12.png)
![vscode 설치 화면](image/13.png)
![vscode 설치 화면](image/14.png)
![vscode 설치 화면](image/15.png) -->
<img src="image/11.png" width="500px">
<img src="image/12.png" width="500px">
<img src="image/13.png" width="500px">
<img src="image/14.png" width="500px">
<img src="image/15.png" width="500px">

3. NestJS 프로젝트 설치 및 생성하기

원하는 폴더에 프로젝트를 생성합니다. 아무 폴더나 상관없지만 보통은 C:\Users\사용자이름 폴더에서 프로젝트를 생성합니다.

 C:\Users\사용자이름 폴더에서 Shift + 마우스 오른쪽 버튼을 누르면 아래와 같은 메뉴가 나옵니다. 여기서 '여기에 Powershell 창 열기'를 클릭하면 powershell 창이 열립니다.
<!-- ![NestJS 프로젝트 생성](image/51.png) -->
<img src="image/51.png" width="500px">

여기서 아래의 명령어를 순서대로 입력하면 nestjs 프로젝트가 생성됩니다.

```powershell
npm i -g @nestjs/cli
nest new project-name
```

이제 vscode를 열고 위에서 만든 폴더를 open하면 개발환경이 완성됩니다.

4. Git 설치하기

공식 홈페이지에서 다운받은 후 설치하시면 됩니다. 본인의 컴퓨터에 맞는 Git을 설치하시면 됩니다. 대부분의 컴퓨는 64비트이므로 64비트-Setup을 받아서 설치하시면 되겠습니다.

https://git-scm.com/download/win

Git 또한 권장사항으로 설치하면 되겠습니다.

<!-- ![Git 설치 화면](image/16.png)
![Git 설치 화면](image/17.png)
![Git 설치 화면](image/18.png)
![Git 설치 화면](image/19.png)
![Git 설치 화면](image/20.png)
![Git 설치 화면](image/21.png)
![Git 설치 화면](image/22.png)
![Git 설치 화면](image/23.png)
![Git 설치 화면](image/24.png)
![Git 설치 화면](image/25.png)
![Git 설치 화면](image/26.png)
![Git 설치 화면](image/27.png)
![Git 설치 화면](image/28.png)
![Git 설치 화면](image/29.png)
![Git 설치 화면](image/30.png) -->
<img src="image/16.png" width="500px">
<img src="image/17.png" width="500px">
<img src="image/18.png" width="500px">
<img src="image/19.png" width="500px">
<img src="image/20.png" width="500px">
<img src="image/21.png" width="500px">
<img src="image/22.png" width="500px">
<img src="image/23.png" width="500px">
<img src="image/24.png" width="500px">
<img src="image/25.png" width="500px">
<img src="image/26.png" width="500px">
<img src="image/27.png" width="500px">
<img src="image/28.png" width="500px">
<img src="image/29.png" width="500px">
<img src="image/30.png" width="500px">

5. Postgres 설치하기

PC에 Database를 설치합니다. Windows 전용으로 Postgres를 제공하는 EDB를 설치하겠습니다. 아래의 홈페이지에서 14.9 버전을 설치하시면 됩니다. Windows x86-64 버전을 설치하시면 됩니다. 설치 마지막에 StackBuilder에서 확장 프로그램을 설치하라는 문구가 나오는데, 여기서는 설치하지 않겠습니다.

중간에 password와 port를 설정하는 부분이 나오는데, 여기는 책에 나온대로 설정하시면 되겠습니다.

<!-- ![Postgres 설치 화면](image/31.png)
![Postgres 설치 화면](image/32.png)
![Postgres 설치 화면](image/33.png)
![Postgres 설치 화면](image/34.png)
![Postgres 설치 화면](image/35.png)
![Postgres 설치 화면](image/36.png)
![Postgres 설치 화면](image/37.png)
![Postgres 설치 화면](image/38.png)
![Postgres 설치 화면](image/39.png)
![Postgres 설치 화면](image/40.png) -->
<img src="image/31.png" width="500px">
<img src="image/32.png" width="500px">
<img src="image/33.png" width="500px">
<img src="image/34.png" width="500px">
<img src="image/35.png" width="500px">
<img src="image/36.png" width="500px">
<img src="image/37.png" width="500px">
<img src="image/38.png" width="500px">
<img src="image/39.png" width="500px">
<img src="image/40.png" width="500px">

EDB는 일반적인 프로그램처럼 실행되지 않고 서비스로 실행이 됩니다. 실행중인 프로세스를 확인하기 위해서는 작업관리자에서 프로세스 탭을 확인하시면 되겠습니다.

<!-- ![Postgres 실행 확인](image/41.png) -->
<img src="image/41.png" width="500px">

이렇게 실행된 Postgres는 부팅시 자동으로 실행됩니다. 자동 실행을 제어하고 싶을 때는 서비스에서 Postgres 서비스를 중지할 수 있습니다.

<!-- ![Postgres 실행 확인](image/42.png)
![Postgres 실행 확인](image/43.png) -->
<img src="image/42.png" width="500px">
<img src="image/43.png" width="500px">

6. DB 클라이언트 설치
DB 프로그램을 설치했으니, DB의 내용을 확인할 클라이언트를 설치해야 합니다. 여기서는 DBeaver community를 설치할 것이며, 이것 또한 공식 홈페이지에서 다운받으시면 되겠습니다.

https://dbeaver.io/download/

<!-- ![DBeaver 홈페이지](image/43.png) -->
<img src="image/43.png" width="500px">

이것 또한 권장사항에 맞게 설치하시면 됩니다.

<!-- ![DBeaver 홈페이지](image/44.png)
![DBeaver 홈페이지](image/45.png)
![DBeaver 홈페이지](image/46.png)
![DBeaver 홈페이지](image/47.png)
![DBeaver 홈페이지](image/48.png)
![DBeaver 홈페이지](image/49.png)
![DBeaver 홈페이지](image/50.png) -->
<img src="image/44.png" width="500px">
<img src="image/45.png" width="500px">
<img src="image/46.png" width="500px">
<img src="image/47.png" width="500px">
<img src="image/48.png" width="500px">
<img src="image/49.png" width="500px">
<img src="image/50.png" width="500px">

7. DBeaver 연결하기

책에 나온대로 연결하시면 되겠습니다.