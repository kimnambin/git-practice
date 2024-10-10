# 깃 관련 명령어

## 로컬 프로젝트를 원격 저장소에 연결 후 푸시하는 방법(처음 올릴 때)

1. git init

2. git remote add origin https://github.com/{깃허브아디}/{레포주소}

3. git branch -M main
4. git add .

5. git commit -m "first commit"

6. git push -u origin main<br>
   ⚠️'-u' 옵션을 붙이면 다음 푸시부터는 `git push`만 해도 올라감

레포 삭제하기

    git remote remove origin

새로운 파일이 추가되지 않았을 경우 커밋하기

    1. git commit -am "커밋 내용"
    2. git push

---

## 브랜치 관리

브랜치 확인하기

     git branch

브랜치 생성하고 이동

     git checkout -b 브랜치명

브랜치 이동

    git switch 브랜치명

---

## 원격 저장소관련

### git pull origin 브랜치명

원격 저장소의 변경 사항을 가져와 병합

⚠️git pull origin main --allow-unrelated-histories<br>
서로 관련이 없는 두 Git 히스토리를 병합할 수 있게 허용하는 옵션

### git fetch origin

원격 저장소의 변경 사항을 가져오지만 병합하지는 않음

### git merge 브랜치명

현재 브랜치에 지정한 브랜치의 변경 사항을 병합

> main 브랜치에 sub 브랜치를 머지하는 경우)

main 브랜치인 상태에서 git merge sub 명령어 실행

---

### 기타

#### 클론

    git clone 깃허브주소

#### gitignore가 제대로 작동되지 않을 때

    1. git rm -r --cached .
    2. git add .
    3. git commit -m "커밋내용"
