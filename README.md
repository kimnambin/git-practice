vs코드 깃허브 업로드 하는 법

git add . 

git commit -m ""

git push origin main

==================================================
git init // 해당 폴더 (로컬 저장소)의 git 초기화 (필수)
git remote add origin https://github.com/{nickname}/testRepo.git 
git branch -M main 

git add . 
git commit -m "first commit"
git push -u origin main // 해당 명령어 입력한 후엔 git push만 해도 올라감

git pull origin main

==========================================

깃허브 클론하는 법

git bash 들어가서

git clone 주소


새로운 브랜치 만들고 커밋하기

git branch (브랜치 확인)
git checkout -b new-branch-name

-------------------------------------------------
머지 하는 법

git merge "브랜치이름"
ex) main 브랜치에 sub 브랜치를 머지하는 경우엔 -> git merge sub
