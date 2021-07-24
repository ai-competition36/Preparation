# 참고자료
목차
1. 리눅스 기본 명령어
2. 소스 코드 관리를 위한 GIT 사용법
3. 기타

---

# 1. 리눅스 기본 명령어
## 이미지 파일 열기 
> eog 파일이름

## 파일 복사
cp {옵션} {복사할경로} {붙여넣을경로}
> cp -r /home/ai_competition/1.competition_trainset/ ./
> cp -r /home/ai_competition/2.testset/ ./
> cp -r /home/ai_competition/3.backsub_images_100/ ./

## 파일 삭제 
단일파일 : > rm {파일명}
하위디렉토리까지 삭제 : > rm -rf {폴더명}

## 주피터 노트북 사용 
> conda activate env_ywj
> jupyter notebook --ip=0.0.0.0 --no-browser
> 147.46.121.38:8888로 접속
> 패스워드 1234

## GPU 사용 
> cm.gpu q=cm_s_vgpu

## 서버 -> 로컬 
> scp -rf ai_competition36@147.46.121.38:/home/ai_competition36/* ./path/to/save

---

# 2. 소스 코드 관리를 위한 GIT 사용법
## 초기 설정
```
git config --global user.name {이름}
git config --global user.email {이메일}
git init
touch .gitignore
git add .
git commit -m "first commit"
# first commit까지 해야 초기 설정 완료
```
## init
로컬 디렉토리를 git저장소로 만든다. .git파일 생성
```
git init
```
## add
로컬 디렉토리의 변경사항을 Stage에 올린다.
```
git add {파일이름}
# 또는
git add --all
git add .
```
## commit
stage에 있는 변경사항을 커밋한다.
```
git commit -m 'commit message'
# commit log 확인 방법
git log
```
## push
origin은 원격저장소를 나타낸다.
```
git add origin {원격저장소이름} https://github.com/유저네임/레파지토리네임.git
git push origin master
```
## fetch
리모트 서버의 최신 이력을 로컬로 가져옴
```
git fetch
# 리모트 서버의 변경사항을 확인할 수 있다.
```
## pull
리모트 서버의 최신 이력을 로컬로 가져와 병합
```
git pull origin master
# 리모트 서버의 master브랜치를 로컬로 병합
```
## branch
```
git branch develop
# develop이라는 이름의 branch를 만들어 준다.
git branch
# 현재 있는 branch 표시
```
### checkout
내가 사용할 브랜치를 지정
```
git checkout <branch>
```
### merge
브랜치를 병합
```
git checkout master
# master branch로 이동한 다음
git merge develop
# develop branch를 master branch로 병합
```
### merge시 발생하는 이슈에 대한 해결방법
https://backlog.com/git-tutorial/kr/stepup/stepup2_7.html
## commit 간 이동(버전 관리)
```
git log
# 커밋 히스토리를 조회할 수 있다.
git reset {commit hash값}
git reset HEAD~1 # 하나 뒤에 있는 commit으로 돌아간다
git reset --hard #  사이에 있는 commit들을 모두 지우고 뒤로 돌아간다
git reset --soft #  사이에 있는 commit들이 모두 합쳐진 채로 staged 영역에 남는다
git reset --mixed # (default) 사이에 있는 commit들이 모두 합쳐진 채로 unstaged 영역에 남는다
```

---

# 기타
## Object detection mAP 측정 방법
https://keyog.tistory.com/44?category=879585

## darknet github(yolov3 사용법)
https://github.com/AlexeyAB/darknet