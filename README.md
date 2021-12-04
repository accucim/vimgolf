# vimgolf

# 1) Add quotes to ansible playbook
![vimgolf_01](https://user-images.githubusercontent.com/93031435/144705536-96fb2c6b-86d0-4558-9d1c-55aece57faa7.gif)

+ ### keystroke: 9

### `G W i " <End> " <Esc> ZZ`

+ ### `G`: 맨 마지막으로 이동

+ ### `W`: 공백으로 이동

+ ### `i`: 입력모드로 전환

+ ### `esc`: 명령모드로 전환

+ ### `ZZ`: 저장

## 설명
`G`로 맨 마지막으로 이동한다. 그 다음 첫 번째 공백으로 이동한다.
입력 모드로 전환 후 `"`를 적절한 위치에 입력한다. 그 후 저장하고 나온다.

---

# 2) simple replacements
![vimgolf_02](https://user-images.githubusercontent.com/93031435/144705541-c69fc914-b072-4ecf-a0f6-3f7922cc8a03.gif)

+ ### keystroke: 25

### `W ce vim <Esc> :%s/emacs/vim/g <CR> ZZ`

+ ### `W`: 공백으로 이동

+ ### `ce`: 단어를 삭제하고 입력모드로 전환

+ ### `:%s/str1/str2/g`: 모든(한 줄에 여러 개 있는) str1을 str2로 치환

## 설명
첫 번째 공백으로 이동 한 후 sublime 단어를 삭제하고 vim을 입력한다.

그 후 emacs를 vim으로 모두 바꿔준다. 저장 후 나온다.

---

# 3) Satisfy the go linter
![vimgolf_03](https://user-images.githubusercontent.com/93031435/144705545-e992e9f6-046c-41ab-a1ed-6c0a92b62066.gif)

+ ### keystroke: 30

### `3j yy P i // <Esc> W W C TODO <Esc> yy <Down> p W ce D<C-N> <Esc> ZZ`

+ ### `j`: 명령모드에서 아래로 이동

+ ### `yy`: 줄 복사

+ ### `P`: 현재 줄 위에 복사한 것을 붙여넣기

+ ### `W`: 공백으로 이동

+ ### `C`: 현재 커서 위치부터 문장 끝까지 삭제

+ ### `p`: 현재 줄 아래 복사한 것을 붙여넣기

+ ### `ce`: 단어를 삭제하고 입력모드로 전환

+ ### `ctrl + N`: 자동완성

## 설명
3줄 아래로 이동한다. `Version string` 문장을 복사한다. 복사한 문장을 현재 줄 위에 붙여넣는다.

입력모드에서 `//`를 입력하고 두 번째 공백 앞으로 이동한다. `C`로 문장 삭제 후 TODO를 입력한다.

`// Version TODO` 문장을 복사한 후 붙여넣는다. 공백으로 이동 후 `Version` 단어를 삭제하고,

Debug를 자동완성으로 써준다. 저장 후 나온다.

---

# 4) Plotting some variables in python
![vimgolf_04](https://user-images.githubusercontent.com/93031435/144705547-a17340e7-a08a-4563-a8d9-60dd2ed88237.gif)

+ ### keystroke: 55

### `:%s/y1/abs(y1) <CR> <C-A> <C-A> <C-A> <Up> . . <Up> . f1 . <Down> . . <Down> . . . fk r g <Up> r r <Up> r b f1 <C-A> <Down> . . <Down> . . .  ZZ`

+ ### `:%s/str1/str2`: 모든 str1을 str2로 치환

+ ### `ctrl + a`: 커서 다음에 위치한 숫자를 찾아내 1증가

+ ### `.`: 바로 전에 수행한 명령을 반복 수행시키는 명령어

+ ### `f + str`: str 앞으로 이동

+ ### `r`: 한 문자 치환

## 설명
모든 `y1`을 `abs(y1)`으로 치환한다. `ctrl + a`로 숫자를 4로 증가시켜준다.

위로 올라가면서 전에 했던 명령(숫자 증가)을 계속 수행한다. `f1`으로 1을 찾아 이동한다.

밑으로 내려가면서 전에 했던 명령을 수행한다. `fk`로 `k`앞으로 이동한다.

`r`을 이용해 위로 올라가면서 한 문자를 바꿔준다.

또 1을 찾아 숫자를 증가시켜준다. 저장 후 나온다.

---

# 5) Python dataclasses
![vimgolf_05](https://user-images.githubusercontent.com/93031435/144705550-19867558-66e6-4e7a-8e74-df771c9d99ad.gif)

+ ### keystroke: 21

### `/" <CR> a s <C-N> <Down> <CR> ,n<C-N> ,a<C-N> ,sc<C-N> <Esc> ZZ`

+ ### `/str`: 현재 커서에서 파일 끝 쪽으로 str 찾기

+ ### `a`: 현재 커서 위치 뒤에 텍스트 추가

+ ### `ctrl + N`: 자동완성

## 설명
`/"`로 `"`을 찾아 이동한다. 현재 커서 뒤에 적절한 단어를 입력 한 후 자동완성으로 완성시켜준다.

저장 후 나온다.
