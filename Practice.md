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


- staging area에 a.txt add
``` 
git add a.txt
git status
``` 
![image](https://user-images.githubusercontent.com/61492320/192195224-63ce63df-b395-4bf9-bfa4-a2f3476cb01f.png)


- staging area에 b.txt, c.txt add
``` 
git add b.txt
git add c.txt
git status
``` 
![image](https://user-images.githubusercontent.com/61492320/192195288-5810e11d-62f9-4a71-a817-9c2963a21ba5.png)


- a.txt 했을 때 git 상태
``` 
echo ybyb >> a.txt
git status
``` 
![image](https://user-images.githubusercontent.com/61492320/192195882-3f5dd1d3-84fa-4d1b-81f7-ab3a0ff6f647.png)


- 수정된 a.txt add
``` 
git add a.txt
git status
``` 
![image](https://user-images.githubusercontent.com/61492320/192195947-4c00e930-965f-4202-ae21-41c4ccd36396.png)

- 로컬의 파일 삭제했을 때 git 상태
``` git rm --cached *
git status
``` 

![image](https://user-images.githubusercontent.com/61492320/192196046-f26ddcfe-8d56-465e-9549-e6d5d0c7848b.png)


