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

#### 실행
```shell
$ vimgolf put 5f1063aa8361810006e73210
```
  ##### 최고점 : 20
  
  ##### <초기실행>
  
  G-O// <C-N> TODO<Esc>-O// <C-N> TODO<Esc>ZZ
  ##### 최고점 : 27
  
  #### 명령어
  * G : 문장 맨 끝으로 이동
  
  * - : 이전 줄로 이동
  
  * O : 행 위에 문자 삽입
  
  * //  : // 입력
  
  * <C-N> : 자동채우기
  
  *  TODO :  TODO 입력
  
  * <Esc> : 입력 모드 종료
  
  * ZZ : 저장 후 종료
  

## 4. Plotting some variables in python

#### 실행
```shell
$ vimgolf put 9v0060da5177000000000209
```
  ##### 최고점 : 34
  
  ##### <초기실행>
  
  :%s/y1/abs(y1)/g<CR>3G/x<CR><C-A>n<C-A><C-A>n<C-A><C-A><C-A>3G/y<CR><C-A>n<C-A><C-A>n<C-A><C-A><C-A>3G/#<CR><C-A>n<C-A><C-A>n<C-A><C-A><C-A>3G/k<CR>sb<Esc>nsr<Esc>nsg<Esc>ZZ
  ##### 최고점 : 74
  
  #### 명령어
  * :%s : 모든 범위 문자에서 바꿀 내용 입력 후 검색 및 치환
  
  * /y1/abs(y1)/g : y1을 abs(y1)로 변경
  
  * <CR> : 엔터
  
  * 3G : 3번째 줄 맨 앞으로 이동
  
  * /x : x를 검색
  
  * <C-A> : 숫자를 1씩 증가
  
  * n : 다음 찾기
  
  * /y : y를 검색
  
  * /# : #를 검색
  
  * /k : k를 검색
  
  * s : 해당 문자 삭제 후 삽입
  
  * b, r, g : 삭제 후 삽입한 문자
  
  * <Esc> : 입력모드 종료
  
  * ZZ : 저장 후 종료 

## 5. Python dataclasses

#### 실행
```shell
$ vimgolf put 6013804df3308e0009368f1c
```
  ##### 최고점 : 19
  
  ##### <초기실행>
  
  /"<CR>as<C-N><Down><CR>,n<C-N>,a<C-N>,s<C-P><Up><CR><Esc>ZZ
  ##### 최고점 : 22
  
  #### 명령어
  * /" : "(큰따옴표) 검색
  
  * <CR> : 엔터
  
  * a : 덧붙이기 입력
  
  * s<C-N>, n<C-N>, a<C-N> : s, n, a로 시작하는 단어 자동채우기
  
  * <Down> : 아래 방향키
  
  * , : ,(콤마) 삽입
  
  * s<C-P> : s로 시작하는 단어 자동채우기(아래서부터 선택)
  
  * <Up> : 위 방향키
  
  * <Esc> : 입력 종료
  
  * ZZ : 저장 후 종료
  
