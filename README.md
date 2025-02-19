# Git & Github 실습을 위한 임시 프로젝트 
### 2025-02-18
### 작업자: BEOMJOON KIM

## 이것은 로컬에서 변경한 내용

## 13. 브랜치 병합(merge)
	작업한 브랜치를 특정 브랜치와 병합(merge)한다.

	(Fast-Forward  병합 - 앞으로 빨리 가기)
	병합전에 마스터 브랜치로 전환한다.
	> git checkout master (또는 main)

	마스터 브랜치로 전환 후 작업 브랜치와 병합한다.
	> git merge 작업브랜치 (master브랜치가 작업브랜치로 옮겨지면서 병합 됨)

	병합한 후에는 작업했던 브랜치는 삭제 해 준다. 
	> git branch -D 작업브랜치

	Fast-Forward 병합이 아닌 일반 병합은 새로은 커밋을 생성한다.

	
## 병합 시 유의 사항
	1) 병합은 브랜치 레벨에서만 병합이 가능하다.
	2) 현재 브랜치에 없는 커밋만 병합 가능
	3) 변경 대상 브랜치로 전환 후 병합

(주의) 병합할 두 브랜치가 동일 파일의 동일한 곳을 수정 했다면 충돌이 발생해서 병합이 거부된다. 이럴 때는 병합을 먼저 해결하고 커밋을 재 수정 해야 한다

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
