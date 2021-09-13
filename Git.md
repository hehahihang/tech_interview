### Git

1. Git의 3가지 영역
➡️Working Directory, Staging Area, Git Directory(Repository) 3가지 작업영역으로 파일들을 관리합니다.  
* Working Directory
  - Git이 추적중이 파일들이 위치하는 영역
  - git init을 통해서 git이 관리하도록 지정된 디렉토리
  - 작업한 파일(생성,수정)들이 저장되는 곳   
* Staging Area
  - commit 할 준비가 된 파일들이 위치하는 영역
  - 작업한(수정된) 파일들 중 버전으로 만들고자 (commit 하고자)하는 파일을 저장합니다.
  - 기술용어로 git에서 "Index"로 불리기도 함  
* Git Directory(Repository)
  - 커밋되어 버전을 관리하는 파일들이 위치하는 영역
  - Git이 프로젝트의 메타데이터와 데이터베이스를 저장하는 곳
  - 프로젝트의 버전 정보를 관리하기 위해 필요한 모든 파일이 저장되어 있다.  

2. Git의 3가지 상태
➡️Git은 파일의 변경사항을 버전별로 관리하기 위해 **Modified, Staged, Committed** 3가지 상태로 관리를 합니다.  
* Modified
  - 수정한 파일을 로컬 데이터베이스에 commit 하지 않은 상태를 의미한다.
  - Working Directory 영역에 있는 파일들 중 수정을한 파일들의 상태를 의미합니다.
* Staged
  - 수정한 파일들 중 commit 할 것이라고 표시한 상태를 의미합니다.
  - Staging Area에 있는 파일들의 상태입니다.
* Committed
  - Staged 상태의 파일들이 로컬 데이터베이스에 안전하게 저장되었다는 것을 의미합니다.
  - commit된 대상 파일은 Working Directory 영역으로 돌아가게 되고 대상 파일의 버전을 관리하는 파일들은 Repositry에 저장된 상태
  - Committed 상태 대상 파일을 수정하게 되면 Modified 상태가 됩니다.
