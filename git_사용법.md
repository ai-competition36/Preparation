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
```
git add origin {원격저장소이름} https://github.com/유저네임/레파지토리네임.git
git push origin master
```
