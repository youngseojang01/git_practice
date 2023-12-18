### 깃의 사용 이유(버전관리, 백업, 협업)
----
버전 관리: 소프트웨어 개발 진행 시에는 중간중간 버전 저장이 꼭 필요함
- 새로 추가한 기능이 최종적으로 쓰이지 않을 수도 있고, 예상치 못한 버그가 발생하여 새롭게 시도한 파트를 다 날리게 될 수도 있음
- 작업 규모가 커졌을 대 단순히 여러 개의 파일로 버전을 남겨놓으면 관리가 힘든 경우가 많음
- 깃에서는 누가, 언제, 무엇을 고쳣는지가 다 기록에 남으며 이를 손쉽게 확인가능하고, 메인 작업 저장소를 예전 버전으로 손쉽게 되돌릴 수 있음

-----
### 깃 커밋 하는법
1. 깃 저장소 생성 (로컬 저장소)
```
git init
```
2. f1.txt를 git에 커밋 (커밋을 통해 스테이지에서 저장소로 이동)
```
git add f1.txt
git commit -m "create f1.txt"
```

### 깃 브랜치 생성 및 전환
1. 깃 브랜치 생성 (기본 브랜치는 master)
```
git branch issue1
```
2. 깃 브랜치 전환
```
git checkout issue1
```

### 깃 브랜치 병합 및 삭제
1. 현재 브랜치 확인
```
git branch
```
2. 브랜치 병합 (master에 issue1을 병합)
```
git checkout master
git merge issue1
```
3. 브랜치 삭제
```
git branch -d issue1
```

### 깃허브 원격 저장소 연결, 푸시 및 풀
1. 원격 저장소 연결
```
git remote add origin https://github.com/git_practice.git
```
2. 원격 저장소 확인 (기본 저장소는 origin)
```
git remote -v
```
3. 원격 저장소에 최초로 push (원격 origin과 로컬 master 브랜치의 연결)
```
git push -u origin master
```
4. 원격 저장소에 최초 push 이후의 push
```
git push
```
5. 원격 저장소에 대한 pull (origin 저장소의 내용을 master 브랜치로 로드)
```
git pull origin master
```
