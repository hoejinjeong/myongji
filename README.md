1. 설정과 초기화
   전역 사용자명 / 이메일 구성하기
   git config --global user.name "Your name"
   git config --global user.email "Your email address"
   
   저장소별 사용자명 / 이메일 구성하기 (해당저장소 디렉터리로 이동후)
   git config user.name "Your name"
   git config user.email "your email address"
   
   참고로 user 설정이 되어 있지 않으면 Github에 있는 repository에 변경사항을 푸시 한다고 해도 commit 집계도 안되고 해당 커밋의 작성자 프로필 아이콘도 ? 로 표시되기 때문에 웬만하면 name과 email 주소를 설정하길 추천한다.
   
   전역 설정 정보 조회
   git config --global --list
   
   저장소별 설정 정보 조회
   git config --list
   
   Git의 출력결과 색상 활성화하기
   git config --global color.ui "auto"
   
   새로운 저장소 초기화 하기
   mkdir /path/newDir
   cd /path/newDir
   git init
   
   저장소 복제하기
   git clone <저장소url>
   
   새로운 원격 저장소 추가하기
   git remote add <원격 저장소> <저장소url>
           . . .
           
2. 기본적인 사용법
   아래 명령어에서 []는 선택적인 매개변수를 의미한다.
   
   새로운 파일을 추가하거나 존재하는 파일 스테이징하고 커밋하기
   git add <파일>
   git commit -m"<메시지>"
   
   파일의 일부를 스테이징하기
   git add -p[<파일>[<파일>[기타 파일들...]]]
   
   add 명령에서 Git 대화 모드를 사용하여 파일 추가하기
   git add -i
   
   수정되고 추적되는 파일의 변경사항 스테이징하기
   git add -u[<경로>[<경로>]]
   
   수정되고 추적되는 모든 파일의 변경사항 커밋하기
   git commit -m "<메시지>"-a
   
   작업 트리의 변경 사항 돌려놓기
   git checkout HEAD <파일> [<파일>]
   
   커밋되지 않고 스테이징된 변경 사항 재설정하기
   git reset HEAD <파일> [<파일>]
   
