# Git & Github 실습을 위한 임시 프로젝트 
### 2025-02-18
### 작업자: BEOMJOON KIM


## 14. stash에 작업 내용을 임시 저장
	stash : 임시 기억 클립보드 (HEAD가 가리키는 어떤 브랜치도 이용 가능)

	새 작업 브랜치 생성
	> git branch new_work
	> git checkout new_work
	-- 새로운 작업을 한다.

	작업 브랜치에서 stash로 저장
	> git stash (작업 하던 내용이 stash에 저장되고 마스터로 전환)

	stash에 임시 저장된 내용 반영하기
	> git stash pop (적용 후 임시 저장소에서 제거)
	> git stash apply (적용)
