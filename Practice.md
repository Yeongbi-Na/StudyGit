## Git 실습
#### 1. 기본 세팅 </br>
```git config --global user.name
git config --global user.name "Yeongbi"
git config --global core.autocrlf true
```

``` git init
rm -rf .git
git status
``` 


#### 2. git add </br>
- txt 파일 생성

``` echo hell world! > a.txt
echo hell world! > b.txt
echo hell world! > c.txt
git status
``` 

![image](https://user-images.githubusercontent.com/61492320/192195096-7ac7ac58-d410-4b15-8e1b-93f0365931cd.png)

</br>

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
.gitignore파일: Git 버전 관리에서 제외할 목록을 지정하는 파일/ gitignor라는 파일 만들어서 무시할 파일들을 넣어줌

</br>


git add * # 해당 경로에 있는 파일들 모두가 staging area로 add

#### 2. gitignore


참고 사이트 
- https://jud00.tistory.com/entry/Git-gitignore-%ED%8C%8C%EC%9D%BC%EC%9D%80-%EB%AD%98%EA%B9%8C-%EA%B7%B8%EB%A6%AC%EA%B3%A0-%EC%96%B8%EC%A0%9C-%EC%82%AC%EC%9A%A9%ED%95%A0%EA%B9%8C
- https://www.youtube.com/watch?v=Z9dvM7qgN9s
