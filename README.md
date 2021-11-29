# opensource_vimgolf

## 1. Add quotes to ansible playbook

#### 실행
```shell
$ vimgolf put 5f0f5fbe280fbf000c233304
```
  ##### 최고점 : 8
  
  ###### <초기 실행>
  
  GWi"<End>"<Esc>ZZ
  ##### 최고점 : 9

  #### 명령어  
  * G : 파일 끝 줄로 이동
  
  * W : 다음 공백 뒤로 이동
  
  * i : 문자 입력
  
  * " : "(큰따옴표) 입력
  
  * <End> : 문장 끝으로 이동
    
  * " : "(큰따옴표) 입력
    
  * <Esc> : 입력 종료
    
  * ZZ : 저장 후 종료(= :wq)

  
## 2. simple replacements

#### 실행
```shell
$ vimgolf put 603ba26a01b4d00009c10a49
```
  ##### 최고점 : 19
  
  ##### <초기실행>
  
  :%s/sublime\|emacs/vim/g<CR>ZZ
  ##### 최고점 : 27
  
  #### 명령어
  * :%s : 모든 범위 문자에서 바꿀 내용 입력 후 검색 및 치환
  
  * /sublime\|emacs : 모든 범위에서 검색할 문자
  
  * /vim : 바꿀 문자
  
  * /g : 여러 패턴이 나오면 모두 변경
  
  * <CR> : 엔터
  
  * ZZ : 저장 후 종료
  
  

## 3. Satisfy the go linter

실행
```shell
$ vimgolf put 5f1063aa8361810006e73210
```
최고점 : 20

## 4. Plotting some variables in python

실행
```shell
$ vimgolf put 9v0060da5177000000000209
```
최고점 : 34

## 5. Python dataclasses

실행
```shell
$ vimgolf put 6013804df3308e0009368f1c
```
최고점 : 19
