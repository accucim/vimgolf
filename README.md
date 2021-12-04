# vimgolf

# 1) Add quotes to ansible playbook
![vimgolf_01](https://user-images.githubusercontent.com/93031435/144705536-96fb2c6b-86d0-4558-9d1c-55aece57faa7.gif)

## `G W i " <End> " <Esc> ZZ`

+ `G`: 맨 마지막으로 이동

+ `W`: 공백으로 이동

+ `i`: 입력모드로 전환

+ `esc`: 명령모드로 전환

+ `ZZ`: 저장


# 2) simple replacements
![vimgolf_02](https://user-images.githubusercontent.com/93031435/144705541-c69fc914-b072-4ecf-a0f6-3f7922cc8a03.gif)

`W ce vim <Esc> :%s/emacs/vim/g <CR> ZZ`

`W`: 공백으로 이동
`ce`: 단어를 삭제하고 입력모드로 전환
`:%s/str1/str2/g`: 모든(한 줄에 여러 개 있는) str1을 str2로 치환

# 3) Satisfy the go linter
![vimgolf_03](https://user-images.githubusercontent.com/93031435/144705545-e992e9f6-046c-41ab-a1ed-6c0a92b62066.gif)

`3j yy P i // <Esc> W W C TODO <Esc> yy <Down> p W ce D<C-N> <Esc> ZZ`

`j`: 명령모드에서 아래로 이동
`yy`: 줄 복사
`P`: 현재 줄 위에 복사한 것을 붙여넣기
`W`: 공백으로 이동
`C`: 현재 커서 위치부터 문장 끝까지 삭제
`p`: 현재 줄 아래 복사한 것을 붙여넣기
`ce`: 단어를 삭제하고 입력모드로 전환
`ctrl + N`: 자동완성


# 4) Plotting some variables in python
![vimgolf_04](https://user-images.githubusercontent.com/93031435/144705547-a17340e7-a08a-4563-a8d9-60dd2ed88237.gif)

`:%s/y1/abs(y1) <CR> <C-A> <C-A> <C-A> <Up> . . <Up> . f1 . <Down> . . <Down> . . . fk r g <Up> r r <Up> r b f1 <C-A> <Down> . . <Down> . . .  ZZ`

`:%s/str1/str2`: 모든 str1을 str2로 치환
`ctrl + a`: 커서 다음에 위치한 숫자를 찾아내 1증가
`.`: 바로 전에 수행한 명령을 반복 수행시키는 명령어
`f+str`: str 앞으로 이동
`r`: 한 문자 치환


# 5) Python dataclasses
![vimgolf_05](https://user-images.githubusercontent.com/93031435/144705550-19867558-66e6-4e7a-8e74-df771c9d99ad.gif)

`/" <CR> a s <C-N> <Down> <CR> ,n<C-N> ,a<C-N> ,sc<C-N> <Esc> ZZ`

`/str`: 현재 커서에서 파일 끝 쪽으로 str 찾기
`a`: 현재 커서 위치 뒤에 텍스트 추가
`ctrl+N`: 자동완성
