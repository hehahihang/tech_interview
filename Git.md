## Git  

### Git의 3가지 영역  
➡️**Working Directory, Staging Area, Git Directory(Repository)** 3가지 작업영역으로 파일들을 관리합니다.  

![99B3CE3D5B5AC35427](https://user-images.githubusercontent.com/57223501/133052358-f72ddf17-d4d6-442d-91f9-78d95c050f16.png)

* Working Directory
  - Git이 추적중이 파일들이 위치하는 영역
  - git init을 통해서 git이 관리하도록 지정된 디렉토리
  - 작업한 파일(생성,수정)들이 저장되는 곳   
* Staging Area
  - commit 할 준비가 된 파일들이 위치하는 영역
  - 작업한(수정된) 파일들 중 버전으로 만들고자 (commit 하고자)하는 파일을 저장합니다.
  - Working Directory에서 Git add 명령을 실행하면 파일들은 Staging Area로 이동, 소스코드 상태정보 확인 가능
  - 기술용어로 git에서 "Index"로 불리기도 함  
* Git Directory(Repository)
  - 커밋되어 버전을 관리하는 파일들이 위치하는 영역
  - Git이 프로젝트의 메타데이터와 데이터베이스를 저장하는 곳
  - 프로젝트의 버전 정보를 관리하기 위해 필요한 모든 파일이 저장되어 있다.  

### Git의 3가지 상태 (Git 라이프 사이클) 

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

### Git Life Cycle 관점 4가지 상태  

![2447383557690E1003](https://user-images.githubusercontent.com/57223501/133186548-4058a015-70d0-4a5c-96fb-e59ae64b9074.png)

➡️Working Directory에 있는 파일들은 크게 **Untracked와 Tracked로 상태가 분류된다**  
- Tracked 는 세부적으로 Unmodified, Modified ,Staged로 분리된다
- 따라서, Life Cycle 관점에서 본 파일들은 **Tracked, Unmodified, Modified, Staged 4가지 상태로 분류 **  

- Untracked : Working directory에 존재는 하지만 git이 관리하지 않는 파일들의 상태
  - WD에 새롭게 만들어진 파일들이 해당 됌
  - 새로운 파일을 만든 후 **git status**를 통해 Untrackted 상태 확인 가능  

- Staged : commit을 하기 전의 파일 상태를 의미
  - Staging 영역에 있는 파일의 상태입니다.
  - Untracked 상태 or commit으로 상태가 버전이 수정된 이후 git add 명령어를 수행하면 파일들은 Staged 상태가 됌  

- Unmodified : 수정하지 않은 파일 상태를 의미
  - 한 번 이상 commit한 파일들 중 수정을 하지 않은 파일 or 다른 repository의 파일을 clone했을때 파일의 상태  

- Modified : 수정을 한 파일의 상태를 의미
   - Unmodified 상태릐 파일을 수정하면 Modified 상태가 된다.
   - "changes not staged for commit" 은 Tracked 상태이지만 아직 Staged 상태는 아닌 파일을 의미함
