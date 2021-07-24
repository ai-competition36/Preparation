# init
로컬 디렉토리를 git저장소로 만든다. .git파일 생성
```
git init
```
# add
로컬 디렉토리의 변경사항을 Stage에 올린다.
```
git add {파일이름}
# 또는
git add --all
```
# commit
stage에 있는 변경사항을 커밋한다.
```
git commit -m 'commit message'
# commit log 확인 방법
git log
```
# push
origin은 원격저장소를 나타낸다.
```
git add origin {원격저장소이름} https://github.com/유저네임/레파지토리네임.git
git push origin master
```
# fetch
리모트 서버의 최신 이력을 로컬로 가져옴
```
git fetch
# 리모트 서버의 변경사항을 확인할 수 있다.
```
# pull
리모트 서버의 최신 이력을 로컬로 가져와 병합
```
git pull origin master
# 리모트 서버의 master브랜치를 로컬로 병합
```
# branch
```
git branch develop
# develop이라는 이름의 branch를 만들어 준다.
git branch
# 현재 있는 branch 표시
```
## checkout
내가 사용할 브랜치를 지정
```
git checkout <branch>
```
## merge
브랜치를 병합
```
git checkout master
# master branch로 이동한 다음
git merge develop
# develop branch를 master branch로 병합
```
## merge시 발생하는 이슈에 대한 해결방법
https://backlog.com/git-tutorial/kr/stepup/stepup2_7.html