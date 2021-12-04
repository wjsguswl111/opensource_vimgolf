# opensource_vimgolf

## 1. Add quotes to ansible playbook

#### 실행
```shell
$ vimgolf put 5f0f5fbe280fbf000c233304
```
##### 최고점 : 8
  
###### <초기실행>
```shell
GWi"<End>"<Esc>ZZ
```
![1번 초기실행](https://user-images.githubusercontent.com/76931115/144583275-3e4bab40-cad6-48e6-beed-b85edfebab92.jpg)
##### 최고점 : 9

#### 명령어  
* G : 파일 끝 줄로 이동
* W : 다음 공백 뒤로 이동
* i : 문자 입력
* " : "(큰따옴표) 입력
* End : 문장 끝으로 이동
* Esc : 입력 종료
* ZZ : 저장 후 종료(= :wq)
  
#### 실행 영상
![1번 초기실행](https://user-images.githubusercontent.com/76931115/144709092-5f74d948-95b9-4907-82ca-139ec667bc65.gif)

###### <최종실행>
```shell
GWi"<End><C-@>ZZ
```
![1번 최종실행](https://user-images.githubusercontent.com/76931115/144583362-c9b6a02c-b35c-4b4f-97bb-ac6e3576fe92.jpg)
##### 최고점 : 8 

##### 명령어
* G : 파일 끝 줄로 이동
* W : 다음 공백 뒤로 이동
* i : 문자 입력
* " : "(큰따옴표) 입력
* End : 문장 끝으로 이동
* C-@ : 매크로 실행, 이전에 삽입된 텍스트를 삽입하고 삽입을 중지
* ZZ : 저장 후 종료
  
#### 실행 영상
![1번 최종실행](https://user-images.githubusercontent.com/76931115/144709107-294a4e04-4a5d-4a43-8dd6-3a2e674de4c2.gif)



## 2. simple replacements

#### 실행
```shell
$ vimgolf put 603ba26a01b4d00009c10a49
```
##### 최고점 : 19
  
##### <초기실행>
```shell
:%s/sublime\|emacs/vim/g<CR>ZZ
```
![2번 초기실행](https://user-images.githubusercontent.com/76931115/144583454-e33609e8-ee34-4180-9b7e-d788e08942dc.jpg)
##### 최고점 : 27
  
#### 명령어
* :%s : 모든 범위 문자에서 바꿀 내용 입력 후 검색 및 치환
* /sublime\|emacs : 모든 범위에서 검색할 문자
* /vim : 바꿀 문자
* /g : 여러 패턴이 나오면 모두 변경
* CR : 엔터
* ZZ : 저장 후 종료

#### 실행 영상
![2번 초기실행](https://user-images.githubusercontent.com/76931115/144709119-aa05fa19-6bfb-4e1f-8b0a-b983da37cbca.gif)
 
###### <최종실행1>
```shell
w*:s//vim/g<CR>}}B*g&ZZ
```
![2번 최종실행1](https://user-images.githubusercontent.com/76931115/144583480-3c3a0206-f629-42ab-8e16-8083b25a1d70.jpg)
##### 최고점 : 20
  
#### 명령어
* w : 다음 단어로 이동
* '*' : 단어 모두 선택
* :s//vim/g : 단어 모두 vim으로 변경
* CR : 엔터
* } : 다음 문단으로 이동
* B : 이전 단어로 이동
* g : 확장 명령
* & : :s 반복
* ZZ : 저장 후 종료
  
#### 실행 영상
![2번 최종실행1](https://user-images.githubusercontent.com/76931115/144709132-a26a12f8-b626-4f4c-aa25-f7a069b0e76d.gif)

###### <최종실행2>
```shell
w*:s//vim/g<CR>G7W*g&ZZ
```
![2번 최종실행2](https://user-images.githubusercontent.com/76931115/144583517-f2d4dcae-cc48-4664-b95d-6803df3435db.jpg)
##### 최고점 : 20
  
#### 명령어
* w : 다음 단어로 이동
* '*' : 단어 모두 선택
* :s//vim/g : 단어 모두 vim으로 변경
* CR : 엔터
* G : 문장 맨 마지막 줄 앞으로 이동
* 7W : 7번째 단어 다음으로 이
* B : 이전 단어로 이동
* g : 확장 명령
* & : :s 반복
* ZZ : 저장 후 종료
  
#### 실행 영상
![2번 최종실행2](https://user-images.githubusercontent.com/76931115/144709142-774b31f7-fa30-4a7b-a289-ee4bb76f6697.gif)



## 3. Satisfy the go linter

#### 실행
```shell
$ vimgolf put 5f1063aa8361810006e73210
```
##### 최고점 : 20
  
##### <초기실행>
```shell
G-O// <C-N> TODO<Esc>-O// <C-N> TODO<Esc>ZZ
```
![3번 초기실행](https://user-images.githubusercontent.com/76931115/144583562-accb3097-4582-4187-8a08-f8775b6d447b.jpg)
##### 최고점 : 27
  
#### 명령어
* G : 문장 맨 끝으로 이동
* '-' : 이전 줄로 이동
* O : 행 위에 문자 삽입
* //  : // 입력
* C-N : 자동채우기
*  TODO :  TODO 입력
* Esc : 입력 모드 종료
* ZZ : 저장 후 종료

#### 실행 영상
![3번 초기실행](https://user-images.githubusercontent.com/76931115/144709147-8b209585-67be-4513-a864-1b1ec91cd827.gif)

###### <최종실행>
```shell
4GqaO// <C-N> TODO<Esc>6Gq@aZZ
```
![3번 최종실행](https://user-images.githubusercontent.com/76931115/144583603-34cb26a2-eb16-4ea5-a05f-861f82587990.jpg)
##### 최고점 : 22

#### 명령어
* 4G : 4번째 줄로 이동
* qa : 레지스터에 작업을 기록
* O : 행위에 삽입
* //  : // 내용 삽입
* C-N : 자동 채우기
*  TODO :  TODO 내용 삽입
*  Esc : 입력 종료
*  6G : 6번째 줄로 이동
*  q@a : 기록된 매크로 재생
*  ZZ : 저장 후 
  
#### 실행영상
![3번 최종실행](https://user-images.githubusercontent.com/76931115/144709156-ac07523f-c964-418b-a23a-b2a29586d465.gif)



## 4. Plotting some variables in python

#### 실행
```shell
$ vimgolf put 9v0060da5177000000000209
```
##### 최고점 : 34
  
##### <초기실행>
```shell
:%s/y1/abs(y1)/g<CR>3G/x<CR><C-A>n<C-A><C-A>n<C-A><C-A><C-A>3G/y<CR><C-A>n<C-A><C-A>n<C-A><C-A><C-A>3G/#<CR><C-A>n<C-A><C-A>n<C-A><C-A><C-A>3G/k<CR>sb<Esc>nsr<Esc>nsg<Esc>ZZ
```
![4번 초기실행](https://user-images.githubusercontent.com/76931115/144583658-f8d188cf-cc39-461b-a7f8-f6b4194898a3.jpg)
##### 최고점 : 74
  
#### 명령어
* :%s : 모든 범위 문자에서 바꿀 내용 입력 후 검색 및 치환
* /y1/abs(y1)/g : y1을 abs(y1)로 변경
* CR : 엔터
* 3G : 3번째 줄 맨 앞으로 이동
* /x : x를 검색
* C-A : 숫자를 1씩 증가
* n : 다음 찾기
* /y : y를 검색
* /# : #를 검색
* /k : k를 검색
* s : 해당 문자 삭제 후 삽입
* b, r, g : 삭제 후 삽입한 문자
* Esc : 입력모드 종료
* ZZ : 저장 후 종료 

#### 실행 영상
![4번 초기실행](https://user-images.githubusercontent.com/76931115/144709162-4a659665-aa26-4821-a39d-a5fa6ddae739.gif)

###### <최종실행>
```shell
:%s/y1/abs(y1)/g<CR>:3s/1/2/g<CR>:4s/1/3/g<CR>:5s/1/4/g<CR>3G/k<CR>sb<Esc>nsr<Esc>nsg<Esc>ZZ
```
![4번 최종실행](https://user-images.githubusercontent.com/76931115/144583694-6d21e286-88ed-464d-b918-bb0a9236c896.jpg)
##### 최고점 : 65

#### 명령어
* :%s/y1/abs(y1)/g : 파일의 y1을 모두 abs(y1)으로 변경
* CR : 엔터
* :3s/1/2/g : 3번째 줄의 1을 2로 변경
* :4s/1/3/g : 4번째 줄의 1을 3으로 변경
* :5s/1/4/g : 5번째 줄의 1을 4로 변경
* 3G/k : 3번째 줄의 k로 이동
* s : 다음 내용 삭제후 삽입
* Esc : 입력 종료
* n : 다음 검색으로 이동
* b, r, g : b, r, g 입력
* ZZ : 저장 후 종료

#### 실행 영상
![4번 최종실행](https://user-images.githubusercontent.com/76931115/144709172-c53b5adf-24c0-49d3-b191-b5ff3a7ca1b5.gif)



## 5. Python dataclasses

#### 실행
```shell
$ vimgolf put 6013804df3308e0009368f1c
```
##### 최고점 : 19
  
##### <초기실행>
```shell
/"<CR>as<C-N><Down><CR>,n<C-N>,a<C-N>,s<C-P><Up><CR><Esc>ZZ
```
![5번 초기실행](https://user-images.githubusercontent.com/76931115/144583733-72f9a628-0f70-4333-a385-1b5b54563f45.jpg)
##### 최고점 : 22
  
#### 명령어
* /" : "(큰따옴표) 검색
* CR : 엔터
* a : 덧붙이기 입력
* sC-N, nC-N, aC-N : s, n, a로 시작하는 단어 자동채우기
* Down : 아래 방향키
* , : ,(콤마) 삽입
* sC-P : s로 시작하는 단어 자동채우기(아래서부터 선택)
* Up : 위 방향키
* Esc : 입력 종료
* ZZ : 저장 후 종료

#### 실행 영상
![5번 초기실행](https://user-images.githubusercontent.com/76931115/144709177-3e170294-db88-40ed-a1c3-8d7c603ae34e.gif)

###### <최종실행>
```shell
GBastu<C-P>,n<C-N>,a<C-N>,sc<C-N><Esc>ZZ
```
![5번 최종실행](https://user-images.githubusercontent.com/76931115/144583772-fae1a2d9-8d88-4b01-ace2-693977bfe005.jpg)
##### 최고점 : 20

#### 명령어
* G : 마지막 문장으로 이동
* B : 앞 단어로 이동
* a : 덧붙이기 입력
* stuC-P : stu로 시작하는 단어 자동완성(아래서부터)
* nC-N : n으로 시작하는 단어 자동완성(위에서부터)
* aC-N : a로 시작하는 단어 자동완성
* scC-N : sc로 시작하는 단어 자동완성
* Esc : 입력 종료
* ZZ : 저장 후 종료

#### 실행 영상
![5번 최종실행](https://user-images.githubusercontent.com/76931115/144709186-9e469c82-01f6-472b-8220-7b2822a4cf48.gif)
