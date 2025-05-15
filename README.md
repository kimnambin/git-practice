# Git 관련 명령어

### 로컬 프로젝트를 원격 저장소에 연결 후 푸시

1. git init

2. git remote add origin https://github.com/{깃허브아디}/{레포주소}

3. git branch -M main
4. git add .

5. git commit -m "first commit"

6. git push -u origin main<br>
   ⚠️'-u' 옵션을 붙이면 다음 푸시부터는 `git push`만 해도 올라감

---

### 커밋 규칙

| 타입(Type) | 설명(Description)                                     |
| ---------- | ----------------------------------------------------- |
| `feat`     | 새로운 기능에 대한 커밋                               |
| `fix`      | 버그 수정에 대한 커밋                                 |
| `build`    | 빌드 관련 파일 수정 / 모듈 설치 또는 삭제에 대한 커밋 |
| `chore`    | 그 외 자잘한 수정에 대한 커밋                         |
| `ci`       | CI 관련 설정 수정에 대한 커밋                         |
| `docs`     | 문서 수정에 대한 커밋                                 |
| `style`    | 코드 스타일 혹은 포맷 등에 관한 커밋                  |
| `refactor` | 코드 리팩토링에 대한 커밋                             |
| `test`     | 테스트 코드 수정에 대한 커밋                          |
| `perf`     | 성능 개선에 대한 커밋                                 |

---

### 레포 삭제하기

    git remote remove origin

---

### 새로운 파일 추가 x + 커밋만 할 때

    1. git commit -am "커밋 내용"
    2. git push

---

## 브랜치 관리

- 브랜치 목록보기

  git branch

- 브랜치 생성하고 이동

  git checkout -b 브랜치명

- 브랜치 이동

  git switch 브랜치명

---

## 원격 저장소관련

- 원격 저장소의 변경 사항을 가져와 병합

  git pull origin 브랜치명

  ⚠️git pull origin main --allow-unrelated-histories

  서로 관련이 없는 두 Git 히스토리를 병합할 수 있게 허용하는 옵션

- 원격 저장소의 변경 사항을 가져오지만 병합하지는 않음

git fetch origin

- github 브랜치 내용-> git에 가져오기

  git checkout -t origin/(브랜치)

- 병합

  git merge 브랜치명

> main 브랜치에 sub 브랜치를 머지하는 경우) git merge sub

---

### clone

    git clone 깃허브주소

---

### gitignore가 제대로 작동되지 않을 때

    1. git rm -r --cached .
    2. git add .
    3. git commit -m "커밋내용"
