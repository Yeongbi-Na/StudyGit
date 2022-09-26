## Git 실습

![image](https://user-images.githubusercontent.com/61492320/192205795-335f6160-ce77-4a0e-acf8-9c57254638a9.png)



#### 1. 기본 세팅 </br>
```git config --global user.name
git config --global user.name "Yeongbi"
git config --global core.autocrlf true
```

``` git init
rm -rf .git
git status
``` 
</br>



## working dir >> staging area
&nbsp; &nbsp; &nbsp;<img src="https://user-images.githubusercontent.com/61492320/192209027-cce0eb49-e005-415f-8f03-2fc5806015e6.png"  width="500" height="250"/> &nbsp;&nbsp; <img src="https://user-images.githubusercontent.com/61492320/192209399-709a984a-8ded-4d8b-84ef-d9fea668f445.png"  width="400" height="250"/>


#### 1. txt 파일 생성 </br>
``` echo hell world! > a.txt
echo hell world! > b.txt
echo hell world! > c.txt
git status
``` 

![image](https://user-images.githubusercontent.com/61492320/192195096-7ac7ac58-d410-4b15-8e1b-93f0365931cd.png)

</br>

#### 2. git add </br>
- staging area에 a.txt add
``` 
git add a.txt
git status
``` 
![image](https://user-images.githubusercontent.com/61492320/192195224-63ce63df-b395-4bf9-bfa4-a2f3476cb01f.png)
</br>

- staging area에 b.txt, c.txt add
``` 
git add b.txt
git add c.txt
git status
``` 
![image](https://user-images.githubusercontent.com/61492320/192195288-5810e11d-62f9-4a71-a817-9c2963a21ba5.png)
</br>

- a.txt 수정했을 때 git 상태
``` 
echo ybyb >> a.txt
git status
``` 
![image](https://user-images.githubusercontent.com/61492320/192195882-3f5dd1d3-84fa-4d1b-81f7-ab3a0ff6f647.png)

</br>

- 수정된 a.txt를 add
``` 
git add a.txt
git status
``` 
![image](https://user-images.githubusercontent.com/61492320/192195947-4c00e930-965f-4202-ae21-41c4ccd36396.png)

</br>

- 파일들을(in local) 삭제했을 때 git 상태
``` git rm --cached *
git status
``` 

![image](https://user-images.githubusercontent.com/61492320/192196046-f26ddcfe-8d56-465e-9549-e6d5d0c7848b.png)

</br>

- 기타 명령어
``` 
git rm --cached * 모두 삭제
``` 

- git add . 와 git add * 차이
git add . :  .gitignore파일에 있는 파일명들은 제외하고 stage에 올리는 것
git add * : .gitignore파일에 있는 파일들도 stage로 올리는 것


</br>

``` 
git add *# 해당 경로에 있는 파일들 모두가 staging area로 add 
``` 

</br>

#### 2. gitignore
.gitignore파일: Git 버전 관리에서 제외할 목록을 지정하는 파일/ gitignor라는 파일 만들어서 무시할 파일들을 넣어줌, log css 등 특정 파일들, 특정 경로 지정해서 추가 가능

- .gitignore 에 추가하기

``` 
#파일 생성
echo styling > style.css
echo log > log.log
echo log > log2log

# .gitignore에 추가
echo *.log > .gitignore # 모든 .log파일을 gitignore에 추가
echo /git/*.css >> .gitignore # /git 경로에 있는 .css파일을 gitignore에 추가
``` 


- .gitignore 확인

```
start .gitignore
``` 
![image](https://user-images.githubusercontent.com/61492320/192202564-4ae65be9-ffc0-49fc-ac37-4844f1cecd57.png)

</br>

### 3. git status

``` 
git status -h #help 옵션
``` 


``` 
git status -s #간단하게 보기
#A: staged file
#AM: staged file이 working dir에서 수정된 상태
``` 

![image](https://user-images.githubusercontent.com/61492320/192203755-5a042816-11de-456e-812e-74460ba9cd5a.png)

</br>

### 4. git diff
diff: staged file과 working dir 파일간 차이 보기 / 어디가 수정됐는지, 어떤 파일이 수정됐는지</br>
terminal 말고 

```
git diff 
<출력 결과>
삭제된 것은 -- 
추가된 것은 ++
``` 

![image](https://user-images.githubusercontent.com/61492320/192204410-a33f64ff-42d9-4e41-bea1-dc7b85dd638e.png)



``` 
git diff --staged 
# status 와 같이 -h 옵션으로 원하는 diff만 보는 명령어 확인해서 사용가능

``` 
![image](https://user-images.githubusercontent.com/61492320/192204334-21e8dd0b-2a57-44e0-afdc-9e8381726eca.png)

</br>

- vscode를 통한 diff 확인
``` 
# 1. config 파일 수정하기
git config --global -e # git config 파일 수정하기 위해
config 파일에 아래와 같이 추가
``` 
![image](https://user-images.githubusercontent.com/61492320/192205513-c0280ff4-9ea6-406a-9535-4f086df5daf0.png)


``` 
git difftool
``` 
![image](https://user-images.githubusercontent.com/61492320/192205436-1b9df909-55e2-46f6-b3ca-399f9d06b602.png)



### 기타 
``` 
cat a.txt #파일 내 텍스트 출력해줌
``` 


** 질문할것
- .gitignore 추가할 때 >> 로 하면 되는 거 맞는쥐 메모장에 텍스트 추가한 것처럼










![image](https://user-images.githubusercontent.com/61492320/192209108-885b7075-93d6-4693-ae66-0ba71dfba725.png)

![image](https://user-images.githubusercontent.com/61492320/192209178-f9931da2-0685-49ed-bab7-c5bae3a0cb66.png)



![image](https://user-images.githubusercontent.com/61492320/192208919-ffd91b81-a07d-40af-8c35-d51e4814e6c6.png)


![image](https://user-images.githubusercontent.com/61492320/192209235-c1bba5bc-b057-4179-9b2a-973e1cd457ed.png)


참고 사이트 
- https://jud00.tistory.com/entry/Git-gitignore-%ED%8C%8C%EC%9D%BC%EC%9D%80-%EB%AD%98%EA%B9%8C-%EA%B7%B8%EB%A6%AC%EA%B3%A0-%EC%96%B8%EC%A0%9C-%EC%82%AC%EC%9A%A9%ED%95%A0%EA%B9%8C
- https://www.youtube.com/watch?v=Z9dvM7qgN9s
- https://inpa.tistory.com/entry/GIT-%E2%9A%A1%EF%B8%8F-git-add-%F0%9F%86%9A-git-add-%EC%B0%A8%EC%9D%B4%EC%A0%90
