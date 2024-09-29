# Git 기본 가이드

이 문서는 Git에서 사용하는 주요 개념과 워크플로우인 `pull`, `push`, `commit`, `branch`, `merge`에 대해 설명합니다.

## 1. Pull

### 정의:
`pull`은 원격 저장소의 변경 사항을 로컬 저장소로 가져와 병합하는 작업입니다.

### 상세 설명:
- `git pull`은 `git fetch`(원격 저장소에서 변경 사항 가져오기)와 `git merge`(가져온 변경 사항을 병합)를 함께 수행하는 명령어입니다.
- 이 명령어를 통해 팀원이 작업한 최신 내용을 내 로컬 저장소로 가져올 수 있습니다.

### 사용 상황:
- 팀원이 업데이트한 내용을 로컬 저장소에 적용할 때 사용합니다.

---

## 2. Push

### 정의:
`push`는 로컬 저장소에서 작업한 내용을 원격 저장소에 업로드하는 작업입니다.

### 상세 설명:
- 로컬에서 커밋한 작업을 원격 저장소로 올려 다른 팀원들과 공유할 수 있습니다.
- **주의**: 충돌을 방지하기 위해, `push`를 하기 전에 `pull`을 먼저 수행하여 최신 상태를 반영하는 것이 일반적입니다.

### 사용 상황:
- 내가 작업한 내용을 원격 저장소에 올려 팀원들과 공유할 때 사용합니다.

---

## 3. Commit

### 정의:
`commit`은 로컬 저장소에 변경 사항을 기록하는 작업입니다.

### 상세 설명:
- 커밋은 코드 변경 내역을 기록하고, 이를 하나의 버전으로 저장합니다.
- 커밋 메시지를 통해 변경된 내용을 설명할 수 있습니다.
- 커밋은 로컬에서만 이루어지며, 이를 원격 저장소에 반영하려면 `push`를 해야 합니다.

### 사용 상황:
- 코드 수정이나 작업이 완료되면, 이를 기록하기 위해 `commit`을 사용합니다.

---

## 4. Branch

### 정의:
`branch`는 독립적인 작업 공간으로, Git에서는 서로 다른 기능이나 버전 개발을 동시에 진행하기 위해 브랜치를 사용합니다.

### 상세 설명:
- 기본 브랜치는 `main` 또는 `master`로, 프로젝트의 최종 버전이 저장됩니다.
- 새로운 기능을 개발하거나 버그를 수정할 때는 별도의 브랜치를 만들어 작업하고, 완료 후 `main` 브랜치에 병합합니다.

### 사용 상황:
- 기능 개발, 버그 수정, 또는 독립적인 실험을 할 때 브랜치를 사용합니다.

---

## 5. Merge

### 정의:
`merge`는 하나의 브랜치에서 작업한 내용을 다른 브랜치에 통합하는 작업입니다.

### 상세 설명:
- 주로 기능 개발이 완료된 브랜치를 `main` 브랜치에 병합할 때 사용됩니다.
- 병합 과정에서 충돌이 발생할 수 있으며, 이를 수동으로 해결한 후 다시 병합을 시도할 수 있습니다.

### 사용 상황:
- 브랜치에서 작업한 내용을 `main` 브랜치에 합치거나, 여러 브랜치의 작업을 하나로 통합할 때 사용합니다.

  ---
  
<br> <!-- 추가적인 간격을 위한 줄 바꿈 -->
<br> <!-- 추가적인 간격을 위한 줄 바꿈 -->
<br> <!-- 추가적인 간격을 위한 줄 바꿈 -->
<br> <!-- 추가적인 간격을 위한 줄 바꿈 -->

## 이미지를 통한 직관적 설명


![result.png](https://github.com/yeonhochi/use_github/blob/main/result.png)

---

- ### vs code 즉, 로컬 저장소에서 다음과 같이 작업을 진행하고 있을 때


![1.png](https://github.com/yeonhochi/use_github/blob/main/1.png)
<br> <!-- 추가적인 간격을 위한 줄 바꿈 -->
<br> <!-- 추가적인 간격을 위한 줄 바꿈 -->
<br> <!-- 추가적인 간격을 위한 줄 바꿈 -->

---


- ### Local 경로에 저장한 소스 코드가 SourceTree에도 반영된 것을 확인 할 수 있습니다.
- ### Local 저장소에 변경 사항을 기록하는 작업인 `commit` 을 진행합니다.


![2.png](https://github.com/yeonhochi/use_github/blob/main/2.png)

---
<br> <!-- 추가적인 간격을 위한 줄 바꿈 -->
<br> <!-- 추가적인 간격을 위한 줄 바꿈 -->
<br> <!-- 추가적인 간격을 위한 줄 바꿈 -->


- ### `pull`은 원격 저장소의 변경 사항을 로컬 저장소로 가져와 병합하는 작업으로 `push`를 진행하기 전 반드시 진행해주어야 합니다.




![5.png](https://github.com/yeonhochi/use_github/blob/main/5.png)

---


<br> <!-- 추가적인 간격을 위한 줄 바꿈 -->
<br> <!-- 추가적인 간격을 위한 줄 바꿈 -->
<br> <!-- 추가적인 간격을 위한 줄 바꿈 -->




- ### `commit`과`pull`을 완료하고, `push`를 하면 수정된 내용들이 설정한 Git repository에 다음과 같이 반영되는 것을 확인 할 수 있습니다.




![6.png](https://github.com/yeonhochi/use_github/blob/main/6.png)
<br><br>




![7.png](https://github.com/yeonhochi/use_github/blob/main/7.png)


