# git

git은 버전관리시스템(VCS)이다.
  
-

### VCS란?

파일의 변경이력을 기록하여 관리를 용이하게 해준다.

### VCS의 이점

- 변경 내용 공유 가능
- 과거 상태로 복구 용이
- 여러 분기(branch)를 통해 병렬 관리 가능

### git을 쓰는 이유?

- 변경 내용을 추적하여 이전 상태로 복원이 가능하다.
- 빠른 속도
- 누구나 읽어갈 수 있도록 공개 가능
- 오프라인 상태에서도 작업 가능
- 복잡한 *Branch* 관리에 적합
- 병렬 개발 및 버전 관리가 용이해 생산성 증가
- *local repository*와 *remote repository*의 분리    
  -> 소스코드 분산관리   
  -> *local* 혹은 *remote repository* 중 하나가 심각한 피해를 입더라도 분산된 코드로 전체 코드 복원 가능
- 다양한 서비스 업체 및 보조 툴이 존재

### 주요 용어

- **Working Directory** : 실제 작업하고 있는 공간   
: *git*은 *working directory*의 변경사항을 지속적으로 체크하고 반영하는 동기화 작업을 한다.
- **Staging Area(Index)** – 변경이력의 임시 저장 공간   
: *working directory*에서 `add` 명령어을 통해 변경내용을 스테이지에 저장된다. 이 공간에 올려져 있는 파일만 *local repository*에 추가할 수 있다. 커밋 히스토리는 절대 수정이 되지 않기 때문에 다시 한 번 체크하기 위해 스테이지가 존재한다.
- **Local Repository** – 작업중인 컴퓨터의 변경이력 저장 공간   
: 오프라인 작업 시 이 공간까지 접근이 가능하며 매우 빠르다. *remote repository*에 손실이 발생하더라도 빠른 복구가 가능하다.
- **Remote Repository** – 외부 서버에 있는 저장 공간   
: 인터넷을 이용하여 접근 가능하다. 여러 사용자로부터 관리되는 각 *local repository*의 접점

### 주요 명령어

- `Add` – 작업 내용 중 일부 혹은 전체를 stage area로 저장하는 작업
- `commit` – stage area의 작업 내용을 local repository에 저장하는 작업   
: 각각의 commit은 의미 있는 변경 단위이고, 변경에 대한 설명을 commit message로 남긴다. 
- `push` – local repository의 내용을 remote repository로 보내는 작업 
- `pull` – remote repository로부터 working directory로 변경 내용을 가져오는 것
- `branch` – 새로운 commit을 쌓을 수 있는 가지를 만드는 것, 혹은 그 가지   
: branch 중 개발의 주축이 되는 branch를 master Branch라 하며, 모든 branch는 master branch에서 분기되어 최종적으로 다시 master branch에 병합(merge)되어 개발이 진행된다.
- `merge` – 하나의 branch를 다른 branch와 합치는 과정
- gitignore - commit에 포함하지 않을 파일 관리

