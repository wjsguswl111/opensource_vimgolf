# opensource_vimgolf

## 1. Add quotes to ansible playbook

#### 실행
```shell
$ vimgolf put 5f0f5fbe280fbf000c233304
```
  ##### 최고점 : 8
  
  ###### <초기 실행>
  ```shell
  GWi"<End>"<Esc>ZZ
  ```
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
  
  
  ###### <최종 실행>
  ```shell
  GWi"<End><C-@>ZZ
  ```
  ##### 최고점 : 8
  
  ##### 명령어
  * G : 파일 끝 줄로 이동
  
  * W : 다음 공백 뒤로 이동
  
  * i : 문자 입력
  
  * " : "(큰따옴표) 입력
  
  * End : 문장 끝으로 이동
  
  * C-@ : 매크로 실행, 이전에 삽입된 텍스트를 삽입하고 삽입을 중지
  
  * ZZ : 저장 후 종료
  
  #### 실행 

  
## 2. simple replacements

#### 실행
```shell
$ vimgolf put 603ba26a01b4d00009c10a49
```
  ##### 최고점 : 19
  
  ##### <초기 실행>
  ```shell
  :%s/sublime\|emacs/vim/g<CR>ZZ
  ```
  ##### 최고점 : 27
  
  #### 명령어
  * :%s : 모든 범위 문자에서 바꿀 내용 입력 후 검색 및 치환
  
  * /sublime\|emacs : 모든 범위에서 검색할 문자
  
  * /vim : 바꿀 문자
  
  * /g : 여러 패턴이 나오면 모두 변경
  
  * CR : 엔터
  
  * ZZ : 저장 후 종료
  
  
  ###### <최종 실행>
  ```shell
  w*:s//vim/g<CR>}}B*g&ZZ
  ```
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


###### <최종 실행>
```shell
4GqaO// <C-N> TODO<Esc>6Gq@aZZ
```
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

###### <최종 실행>
```shell
:%s/y1/abs(y1)/g<CR>:3s/1/2/g<CR>:4s/1/3/g<CR>:5s/1/4/g<CR>3G/k<CR>sb<Esc>nsr<Esc>nsg<Esc>ZZ
```
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

  ###### <최종 실행>
```shell
GBastu<C-P>,n<C-N>,a<C-N>,sc<C-N><Esc>ZZ
```
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
