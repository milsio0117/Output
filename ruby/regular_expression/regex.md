## 正規表現
|書き方 |	内容 |
|:---|:---|
|.|	任意の1文字（改行はなし）|
|*	|直前の文字を0回以上の繰り返し|
|+	|直前の文字を1回以上の繰り返し|
|*?	|直前の文字を0回以上の繰り返し、より短くマッチ|
|+?	|直前の文字を1回以上の繰り返し、より短くマッチ|
|?	|直前の文字を0回か1回の繰り返し|
|??|	直前の文字を0〜1回の繰り返し、より短くマッチ|
|-（ハイフン）|	範囲の表現|
|[]（ブランケットで囲む）|	[]内のいずれかの1文字にマッチ|
|^|	いずれかの1文字にマッチしない（否定）[のすぐあとに記述|
|^|行頭にマッチ（≒先頭。nで改行されたあとの先頭も含めるので１つとは限らない）|
|$|行末にマッチ（同上）|
|\A|	先頭にマッチ（改行後は含まれず１つのみ）|
|\Z|	末尾にマッチ、改行文字なら改行の直前|
|\z|末尾にマッチ、改行でも常に末尾にマッチ|
|\s	|空白文字[\t\r\n\f]にマッチ|
|\S	|空白文字[\t\r\n\f]以外にマッチ|
|\w	|英数字[0-9A-Za-z_]にマッチ|
|\W	|英数字[0-9A-Za-z_]以外にマッチ|
|[0-9]	|すべての数字にマッチ|
[^0-9]	|すべての数字以外にマッチ|
|\d	|10進数(0-9)|
|\D	|10進数(0-9)以外(つまり数字以外何でも)|
|\h	|16進数(0-9A-Fa-f)|
|\H	|16進数以外|
|\b	|スペースなどによる単語の区切り|
|\G|	直前にマッチした箇所の直後にマッチ|
|\t	|タブ文字|
|\n|	改行|
|{n} |直前の文字をn回の繰り返し|
|{n}?	|直前の文字をn回の繰り返し、より短くマッチ|
|{n,}	|直前の文字をn回以上の繰り返し|
|{n,}?	|直前の文字をn回以上の繰り返し、より短くマッチ|
|{n,m}	|直前の文字をn〜m回の繰り返し|
|{n,m}?|直前の文字をn〜m回の繰り返し、より短くマッチ|
|a ｜ b	|aもしくはbにマッチ|
|() |グループ化 |
|\n|()でグループ化したもののn番目|
|?=... | match(/(ABC)(?=DEF)/, "ABCDEF")　DEFが存在すればABCにマッチ|
|?!...| DEFが存在しない場合にABCにマッチ|
|?<=... |match(/(?<=ABC)(DEF)/, "ABCDEF") DEF の前に ABC が存在する場合のみ DEF にマッチ |
|?<!... | DEF の前に ABC が存在しない場合のみ DEF にマッチ|
<br>
* /\d+/ :数字が1個以上並んでいる場合の文字列
