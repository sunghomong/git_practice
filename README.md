# 실무간 깃 허브를 능숙하게 다루기 위한 연습

## 깃헙 브랜치 3개로 협업해보기

- repo 생성
- git init

```bash
PS C:\git_practice> echo "# git_practice" >> README.md
PS C:\git_practice> git init
Initialized empty Git repository in C:/git_practice/.git/
PS C:\git_practice> git add README.md
PS C:\git_practice> git commit -m "first commit"
[master (root-commit) 0333c8c] first commit
1 file changed, 0 insertions(+), 0 deletions(-)
create mode 100644 README.md
PS C:\git_practice> git branch -M main
PS C:\git_practice> git remote add origin https://github.com/sunghomong/git_practice.git
PS C:\git_practice> git push -u origin main
```

- develop 브랜치 생성

```bash
git branch develop
git branch # 확인용
git push --set-upstream origin develop
```

- 페이지에서 develop 생겼는지 확인
- default branch develop으로 변경
- 이슈 생성 해보기
- fetch & pull

```bash
git fetch
git pull origin develop
```

- 작업 브랜치 생성후 그 브랜치로 이동

```bash
git branch Feat/컴포넌트 
git branch # 확인용
git switch Feat/컴포넌트
```

- 예제 텍스트 생성 및 작성

```bash
touch 성호.txt
```

- 작업한 브랜치로 push

```bash
git add .
git commit -m"컴포넌트 작업 완료~" 
git push --set-upstream origin Feat/컴포넌트 # 본인 원격 브랜치명
```

- compare & pull request
- 코드 리뷰 후 merge
- merge 후 원격에서 해당 브랜치 삭제
- 로컬에서도 switch 후 해당 브랜치 삭제
- 브랜치 삭제 후 develop에서 git fetch & pull
- 똑같이 한번 더 연습

- merge 할때 해당 이슈 번호 넣고 merge가 성공적이면 closed로 이슈가 성공적으로 완료된걸 표시 가능 
```txt
closes #4 
```

- git pull 할때는 develop에서, git push 할때는 작업 브랜치에서!!!

