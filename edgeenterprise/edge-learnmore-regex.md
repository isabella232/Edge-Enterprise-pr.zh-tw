---
title: 規則運算式 2 語法
ms.author: comanea
author: AndreaLBarr
manager: seanlyn
ms.date: 08/12/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: 規則運算式 2 語法
ms.openlocfilehash: 78f21846c142d67470cd421a34baafa9d0021bd0
ms.sourcegitcommit: 8968f3107291935ed9adc84bba348d5f187eadae
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/12/2021
ms.locfileid: "11979321"
---
# <a name="regular-expression-2-re2h-syntax"></a>規則運算式 2 (re2.h) 語法

規則運算式是描述字元字串集的標記法。 如果字串位於規則運算式所描述的集中，我們通常表示規則運算式與字串相符。

最簡單的規則運算式是單一常值字元。 除`\*+?()|`以外的元字元，字元與其本身相符。 若要比對元字元，請用反杠來逸出它： `\+` 比對文字加號字元。

可以變更或串連兩個規則運算式，以形成新規則運算式：如果 *e<sub>1</sub>* 符合 _s_ 和*e<sub>2</sub>* 符合 _t_，則*<sub>1</sub>*  | *e<sub>2</sub> *符合 _s_ 或 _t_，以及*e<sub>1</sub>* *e<sub>2</sub>* 符合__ st。

元字元_`\`_、_+_，以及 _？_ 是重複運算子：*e<sub>1</sub>* _`\`_ 與零個或多個 (可能不同的) 字串順序相符，其中每個字串都符合 *e<sub>1</sub>*；*e<sub>1</sub>* _+_ 符合一或多個；*e<sub>1</sub>* _？_ 符合零或一。

運算子的優先順序 (從最弱到最强的繫結)，首先是替代，然後是串連，最後是重複運算子。 顯式括弧可以用於強制不同的意義，就像在算術運算式中一樣。 一些範例 _：ab|cd_相當於 (_ab) | (cd) ;__`ab\`_ 等於 _`a(b\)`_ 。

到目前為止描述的語法是大多數傳統的 Unix _egrep_ 規則運算式語法。 這個子集足以描述所有的常規語言：不嚴格地說，規則語言是一組字串，這些字串只需使用固定的記憶體量就可以在一次通過文字時進行匹配。 較新的規則運算式設備 (特別是 Perl 和那些複製它的設備) 新增了許多新的運算子和逸出序列，這使得規則運算式更簡潔，有時更神秘，但通常不是更强大。

此頁面列出了 RE2 接受的規則運算式語法。

它也列出了一些 PCRE、PERL 和 VIM 接受的語法。

## <a name="syntax-tables"></a>語法資料表

| 各種單字元運算式 | 範例 |
| --- | --- |
| 任何字元，可能包括新行字元 (s=true) | . |
| 字元類別 | [xyz] |
| 反字元類別 | [^xyz] |
| Perl 字元類別 ([連結](#user-content-perl)) | \d |
| 反 Perl 字元類別 | \D |
| ASCII 字元類別 ([連結](#user-content-ascii)) | [[:alpha:]] |
| 反 ASCII 字元類別 | [[:^alpha:]] |
| Unicode 字元類別 (單字母名稱) | \pN |
| Unicode 字元類別 | \p{Greek} |
| 反 Unicode 字元類 (單字母名稱) | \PN |
| 反 Unicode 字元類別 | \P{Greek} |

|&nbsp;| 複合 |
| --- | --- |
| xy | x 後接 y |
| x\|y | x 或 y (偏好 x) |

|&nbsp;| 重複 |
| --- | --- |
| x\* | 零或多個 x，偏好更多 |
| x+ | 一個或多個 x，偏好更多 |
| x? | 零或一個 x，偏好更多 |
| x{n,m} | n 或 n+1 或 ... 或 m x，偏好更多 |
| x{n,} | n 或更多 x，偏好更多 |
| x{n} | 完全符合 n x |
| x\*? | 零或多個 x，偏好更少 |
| x+? | 一個或多個 x，偏好更少 |
| x?? | 零或一個 x，偏好零 |
| x{n,m}? | n 或 n+1 或 ... 或 m x，偏好更少 |
| x{n,}? | n 或更多 x，偏好更少 |
| x{n}? | 完全符合 n x |
| x{} | (≡ x\*) (不支援) VIM |
| x{-} | (≡ x\*?) (不支援) VIM |
| x{-n} | (≡ x{n}?) (不支援) VIM |
| x= | (≡ x?) (不支援) VIM |

實作限制：計算表單 x {n,m}，x {n,} 和 x {n} 拒絕創建最小或最大重複計數超過 1000 的表單。 無限重複不受此限制。

|&nbsp;| 所有格重複 |
| --- | --- |
| x\*+ | 零個或多個 x、所有格 (不支援) |
| x++ | 一或多個 x、所有格 (不支援) |
| x?+ | 零個或一個 x、所有格 (不支援) |
| x{n,m}+ | n 或 ... 或 m x，所有格 (不支持) |
| x{n,}+ | n 或多個 x，所有格 (不支援) |
| x{n}+ | 完全符合 n x，所有格 (不支持) |

|&nbsp;| 分組 |
| --- | --- |
| (re) | 編號擷取群組 (子符合) |
| (?P&lt;名稱&gt;re) | 具名&amp;編號擷取群組 (子符合) |
| (?&lt;名稱&gt;re) | 具名 &amp; 編號擷取群組 (子符合) (不支援) |
| (?&#39;name&#39;re) | 具名 &amp; 編號擷取群組 (子符合) (不支援) |
| (?:re) | 非擷取群組 |
| (?flags) | 在目前的群組內設定旗標；非擷取 |
| (?flags:re) | 在 re 期間設定旗標；非擷取 |
| (?#text) | 注釋 (不支援) |
| (?\|x\|y\|z) | 分支編號重設 (不支援) |
| (?&gt;re) | re 的所有格匹配 (不支持) |
| re@&gt; | re 的所有格匹配 (不支援) VIM |
| %(re) | 非擷取群組 (不支援) VIM |

|&nbsp;| Flags |
| --- | --- |
| i | 不區分大小寫 (預設為 false) |
| m | 多行模式：除了開始/結束文字 (預設為 false) 以外，還能有 ^ 和 $ 符合開始/結束行。 |
| s | let . 符合 \n (預設為 false) |
| U | ungreedy：交換 x\* 和 x\*?、x+ 和 x+? 等的意義 (預設為 false) |

旗標語法為 xyz (set) 或 -xyz (clear) 或 xy-z (設定為 xy、clear z)。

|&nbsp;| 空字串 |
| --- | --- |
| ^ | 文字或行的開頭 (m=true) |
| $ | 文字 (例如 \z 非 \Z) 或行的結尾 (m=true) |
| \A | 文字的開頭 |
| \b | 在 ASCII 字的邊界 (一邊是\w，另一邊是 \W, \A, or \z) |
| \B | 不在 ASCII 字的邊界 |
| \g | 搜尋的次文字的開頭處 (不支援) PCRE |
| \G | 最近符合的結尾處 (不支援) PERL |
| \Z | 在文字結尾處，或文字結尾處的新行字元之前 (不支援) |
| \z | 在文字結尾處 |
| (?=re) | 在文字與 re 相符之前 (不支援) |
| (?!re) | 在文字不符合 re 之前 (不支援) |
| (?&lt;=re) | 在文字與 re 相符之后 (不支援) |
| (?&lt;!re) | 在文字與 re 不相符之后 (不支援) |
| re&amp; | 在文字與 re 相符之前 (不支援) VIM |
| re@= | 在文字與 re 相符之前 (不支援) VIM |
| re@! | 在文字不符合 re 之前 (不支援) VIM |
| re@&lt;= | 在文字與 re 相符之后 (不支援) VIM |
| re@&lt;! | 在文字與 re 不相符之后 (不支援) VIM |
| \zs | 開始匹配組 (= \K) (不支援) VIM |
| \ze | 結束匹配組 (不支援) VIM |
| \%^ | 檔案開頭 (不支援) VIM |
| \%$ | 檔案結尾 (不支持) VIM |
| \%V | 在螢幕上 (不支援) VIM |
| \%# | 游標位置 (不支援) VIM |
| \%&#39;m | 標記 m 位置 (不支援) VIM |
| \%23l | 在行 23 中 (不支援) VIM |
| \%23c | 在欄 23 中 (不支援) VIM  |
| \%23v | 在虛擬欄 23 中 (不支援) VIM |

|&nbsp;| 逸出序列 |
| --- | --- |
| \a | bell (≡ \007) |
| \f | 表單摘要 (≡ \014) |
| \t | 水平索引標籤 (≡ \011) |
| \n | 新行字元 (≡ \012) |
| \r | 滑動架傳回 (≡ \015) |
| \v | 垂直定位字元 (≡ \013) |
| \* | 常值 \*，適用于任何標點字元 \* |
| \123 | 八進位字元代碼 (最多三個數字) |
| \x7F | 十六進位字元碼 (正好兩個數字) |
| \x{10FFFF} | 十六進位字元代碼 |
| \C | 即使在 UTF-8 模式中也與單一位元組相符 |
| \Q...\E | 常值文字 ... 即使 ... 有標點符號 |
| \1 | 反向參考 (不支援) |
| \b | 退格鍵 (不支援) (使用 \ 010) |
| \cK | 控制 char ^K (不支援) (使用 \001 等) |
| \e | 逸出 (不支援) (使用 \033) |
| \g1 | 反向參考 (不支援) |
| \g{1} | 反向參考 (不支援) |
| \g{+1} | 反向參考 (不支援) |
| \g{-1} | 反向參考 (不支援) |
| \g{name} | 具名反向參考 (不支援) |
| \g&lt;名稱&gt; | 副程式撥號 (不支援) |
| \g&#39;name&#39; | 副程式撥號 (不支援) |
| \k&lt;名稱&gt; | 具名反向參考 (不支援) |
| \k&#39;name&#39; | 具名反向參考 (不支援) |
| \lX | 小寫 X (不支援) |
| \ux | 大寫 x (不支持) |
| \L...\E | 小寫文字 ... (不支援) |
| \K | 重設 $0 的開頭 (不支援) |
| \N{name} | 具名 Unicode 字元 (不支援) |
| \R | 分行符號 (不支援) |
| \U...\E | 大寫文字 ... (不支援) |
| \X | 擴充 Unicode 序列 (不支援) |
| \%d123 | 十進位字元 123 (不支援) VIM |
| \%xFF | 十六進位字元 FF (不支援) VIM |
| \%o123 | 八進位字元 123 (不支援) VIM |
| \%u1234 | Unicode 字元 0x1234 (不支援) VIM |
| \%U12345678 | Unicode 字元 0x12345678 (不支援) VIM |

|&nbsp;| 字元類別元素 |
| --- | --- |
| x | 單一字元 |
| A-Z | 字元範圍 (全人) |
| \d | Perl 字元類別 |
| [:foo:] | ASCII 字元類別 foo |
| \p{Foo} | Unicode 字元類別 Foo |
| \pF | Unicode 字元類別 F (單字母名稱) |

|&nbsp;| 具名字元類作為字元類元素 |
| --- | --- |
| [\d] | 數位 (≡ \d) |
| [^\d] | 非數位 (≡ \D) |
| [\D] | 非數位 (≡ \D) |
| [^\D] | 否非數位 (≡ \d) |
| [[:name:]] | 字元類別中的具名 ASCII 類別 (≡ [:name:]) |
| [^[:name:]] | 在反字元類中的具名 ASCII 類別 (≡ [:^name:]) |
| [\p{Name}] | 字元類別中的具名 Unicode 屬性 (≡ \p{Name}) |
| [^\p{Name}] | 反字元類別中的具名 Unicode 屬性 (≡ \p{Name}) |

| <a name="user-content-perl"></a> | Perl 字元類 (全為 ASCII) |
| --- | --- |
| \d | 位數 (≡ [0-9]) |
| \D | 非位數 (≡ [^0-9]) |
| \s | 空格 (≡ [\t\n\f\r]) |
| \S | 非空格 (≡ [^\t\n\f\r]) |
| \w | 文字字元 (≡ [0-9A-Za-z\_]) |
| \W | 非文字字元 (≡ [^0-9A-Za-z\_]) |
| \h | 水平空間 (不支援) |
| \H | 非水平空間 (不支援) |
| \v | 垂直空間 (不支援) |
| \V | 非垂直空間 (不支援) |

|<a name="user-content-ascii"></a>  | ASCII 字元類別 |
| --- | --- |
| [[:alnum:]] | 英數字元 (≡ [0-9A-Za-z]) |
| [[:alpha:]] | 字母 (≡ [A-Za-z]) |
| [[:ascii:]] | ASCII (≡ [\x00-\x7F]) |
| [[:blank:]] | 空白(≡ [\t]) |
| [[:cntrl:]] | 控制項 (≡ [\x00-\x1F\x7F]) |
| [[:d igit：]] | 位數 (≡ [0-9]) |
| [[:graph:]] | 圖形化 (≡ `[!-~]` ≡ `[A-Za-z0-9!&quot;#$%&amp;&#39;()\*+,\-./:;&lt;=&gt;?@[\\\]^_`\` `{\|}~]`) |
| [[:lower:]] | 小寫 (≡ [a-z]) |
| [[:print:]] | 可列印 (≡ [-~] ≡ [[:graph:]]) |
| [[:punct:]] | 標點符號 (≡ [!-/:-@[-`{-~]) |
| [[:space:]] | 空格 (≡ [\t\n\v\f\r]) |
| [[:upper:]] | 大寫 (≡ [A-Z]) |
| [[:word:]] | 文字字元 (≡ [0-9A-Za-z\_]) |
| [[:xdigit:]] | 十六進位數位 (≡ [0-9A-Fa-f]) |

|&nbsp;| Unicode 字元類名 --一般類別 |
| --- | --- |
| C | 其他 |
| 副本 | control |
| Cf | format |
| Cn | 未指派的代碼點 (不支援) |
| Co | 私密用法 |
| Cs | 替代 |
| L | 字母 |
| LC | 大小寫字母 (不支援) |
| L&amp; | 大小寫字母 (不支援) |
| Ll | 小寫字母 |
| Lm | 修飾詞字母 |
| Lo | 其他字母 |
| Lt | 大寫字母 |
| Lu | 大寫字母 |
| M | 標記 |
| Mc | 間距標記 |
| Me | 封閉標記 |
| Mn | 非間距標記 |
| N | 數字 |
| Nd | 十進位數 |
| Nl | 字母數字 |
| 否 | 其他數字 |
| P | 標點符號 |
| Pc | 連接器標點符號 |
| Pd | 虛線標點符號 |
| Pe | 關閉標點符號 |
| Pf | 末位標點符號 |
| Pi | 首位標點 |
| Po | 其他標點符號 |
| Ps | 開放標點符號 |
| S | symbol |
| Sc | 貨幣符號 |
| Sk | 修飾詞符號 |
| Sm | 數學符號 |
| So | 其他符號 |
| Z | 分隔符號 |
| Zl | 行分隔符號 |
| Zp | 段落分隔符號 |
| Zs | 空格分隔符號 |

| Unicode 字元類名 -- 指令碼 |
| --- |
| Adlam 文 |
| 阿洪姆語 |
| Anatolian\_Hieroglyphs |
| 阿拉伯文 |
| 亞美尼亞文 |
| 阿維斯塔文 |
| 峇里文 |
| 巴姆文 |
| Bassa\_Vah |
| 巴塔克文 |
| 孟加拉文 |
| 拜克舒基文 |
| 注音符號 |
| 婆羅米文 |
| 點字 |
| 布吉斯文 |
| 布錫語 |
| Canadian\_Aboriginal |
| 卡里亞文 |
| Caucasian\_Albanian |
| 查克馬文 |
| Cham |
| 卻洛奇文 |
| 花剌子模語 |
| 通用 |
| 科普特語 |
| 楔形文字 |
| 賽普勒斯 |
| 西里爾文 |
| 德瑟列特文 |
| 梵文字母 |
| Dives\_Akuru |
| Dogra 文 |
| 杜普雷速记 |
| Egyptian\_Hieroglyphs |
| 艾巴申語 |
| 埃利邁文 |
| 衣索比亞文 |
| 喬治亞文 |
| 格來哥利蒂克文 |
| 歌德 |
| 古蘭塔文 |
| 希臘文 |
| 古吉拉特文 |
| Gunjala\_Gondi |
| 果魯穆奇文字 |
| 漢語 |
| 諺文 |
| Hanifi\_Rohingya |
| 漢奴勞族文 |
| 哈特拉文 |
| 希伯來文 |
| 平假名 |
| Imperial\_Aramaic |
| 已繼承 |
| Inscriptional\_Pahlavi |
| Inscriptional\_Parthian |
| 爪哇文 |
| 凱提體文 |
| 坎那達文 |
| 片假名 |
| Kayah\_Li |
| 佉盧文 |
| Khitan\_Small\_Script |
| 高棉文 |
| 郝吉文 |
| 信德文 |
| 寮文 |
| 拉丁文 |
| 雷布查文 |
| 林布文 |
| Linear\_A |
| Linear\_B |
| 栗粟文 |
| 呂西亞文 |
| 利底亞文 |
| 馬哈加尼文 |
| 瑪加沙文 |
| 馬來亞拉姆文 |
| 曼底克文 |
| 摩尼文 |
| Marchen 文 |
| Masaram\_Gondi |
| 梅德法伊德林文 |
| Meetei\_Mayek |
| Mende\_Kikakui |
| Meroitic\_Cursive |
| Meroitic\_Hieroglyphs |
| 苗文 |
| Modi 文 |
| 蒙古文 |
| 姆諾文 |
| Multani 文 |
| 緬甸 |
| 納巴泰文 |
| 南迪城文 |
| New\_Tai\_Lue |
| Newa 文 |
| 西非書面文字 |
| 女書 |
| Nyiakeng\_Puachue\_Hmong |
| 歐甘字母 |
| Ol\_Chiki |
| Old\_Hungarian |
| Old\_Italic |
| Old\_North\_Arabian |
| Old\_Permic |
| Old\_Persian |
| Old\_Sogdian |
| Old\_South\_Arabian |
| Old\_Turkic |
| 奧里亞語 |
| 奧賽治文 |
| 奧斯曼亞文 |
| Pahawh\_Hmong |
| 帕爾邁拉文 |
| Pau\_Cin\_Hau |
| Phags\_Pa |
| 腓尼基文 |
| Psalter\_Pahlavi |
| 拉讓文 |
| 盧恩文 |
| 撒馬利亞文 |
| 紹拉斯徹文 |
| 沙拉達文 |
| 蕭伯納文 |
| 悉曇文 |
| 手語書寫 |
| 僧伽羅文 |
| 粟特文 |
| Sora\_Sompeng |
| 索永布文 |
| 巽丹文 |
| Syloti\_Nagri |
| 敘利亞文 |
| 他加祿語 |
| 塔班瓦語 |
| Tai\_Le |
| Tai\_Tham |
| Tai\_Viet |
| 塔卡里文 |
| 坦米爾文 |
| 西夏語 |
| 特拉古文 |
| 塔安那文 |
| 泰文 |
| 藏文 |
| 提弗納文 |
| 底羅仆多文 |
| 烏加里特語 |
| 范文 |
| Wancho 語 |
| Warang\_Citi |
| 亞茲迪文 |
| 彝文 |
| Zanabazar\_Square |

|&nbsp;| Vim 字元類別 |
| --- | --- |
| \i | 識別碼字元 FF (不支援) VIM |
| \I | \i 排除數字 (不支援) VIM |
| \k | 關鍵字字元 FF (不支援) VIM |
| \K | \k 排除數字 (不支援) VIM |
| \f | 檔案名字元 (不支援) VIM |
| \F | \f 排除數字 (不支援) VIM |
| \p | 可列印字元 (不支援) VIM |
| \P | \p 排除數字 (不支援) VIM |
| \s | 空格字元 (≡ [\t]) (NOT SUPPORTED) VIM |
| \S | 非空格字元 (≡ [^ \t]) (NOT SUPPORTED) VIM |
| \d | 数位 (≡ [0-9]) VIM |
| \D | 非 \d VIM |
| \x | 十六進位數位 (≡ [0-9A-Fa-f]) (NOT SUPPORTED) VIM |
| \X | 非 \x (不支援) VIM |
| \o | 八進位數位 (≡ [0-7]) (不支援) VIM |
| \O | 非 \o (不支援) VIM |
| \w | 文字字元 VIM |
| \W | 非 \w VIM |
| \h | 文字字元標題 FF (不支援) VIM |
| \H | 非 \h (不支援) VIM |
| \a | 字母 \o (不支援) VIM |
| \A | 非 \a (不支援) VIM |
| \l | 小寫 (不支援) |
| \L | 非小寫 (不支援) VIM |
| \u | 大寫 (不支援) |
| \U | 非大寫 (不支援) VIM |
| \_x | \x 和分行符號，適用于任何 x (不支援) VIM |
| \c | 忽略大小寫 (不支援) VIM |
| \C | 符合大小寫 (不支援) VIM |
| \m | 魔術 (不支援) VIM |
| \M | 非魔術 (不支援) VIM |
| \v | 超魔術 (不支援) VIM |
| \V | 超非魔術 (不支援) VIM |
| \Z | 忽略 Unicode 結合字元中的差異 (不支援) VIM |

| &nbsp; | 魔術 |
| --- | --- |
| (?{code}) | 任意 Perl 代碼 (不支援) PERL |
| (??{code}) | 已延遲任意 Perl 代碼 (不支援) PERL |
| (?n) | 對 regexp 擷取群組 n 的遞迴撥號 (不支援) |
| (?+n) | 遞迴呼叫相關群組 +n (不支援) |
| (?-n) | 遞迴呼叫相關群組 -n (不支援) |
| (?C) | PCRE 圖說文字 (不支援) PCRE |
| (?R) | 對整個 regexp 的遞迴撥號 (≡ (?0)) (不支援) |
| (?&amp;name) | 遞迴呼叫具名群組 (不支援) |
| (?P=name) | 具名反向參考 (不支援) |
| (?P&gt;name) | 遞迴呼叫具名群組 (不支援) |
| (?(cond)true|false) | 條件式分支 (不支援) |
| (?(cond)true) | 條件式分支 (不支援) |
| (\*ACCEPT) | 讓 regexps 更像 Prolog (不支援) |
| (\*COMMIT) | (不支援) |
| (\*F) | (不支援) |
| (\*FAIL) | (不支援) |
| (\*MARK) | (不支援) |
| (\*PRUNE) | (不支援) |
| (\*SKIP) | (不支援) |
| (\*THEN) | (不支援) |
| (\*ANY) | 設定分行符號慣例 (不支援) |
| (\*ANYCRLF) | (不支援) |
| (\*CR) | (不支援) |
| (\*CRLF) | (不支援) |
| (\*LF) | (不支援) |
| (\*BSR\_ANYCRLF) | 設定 \R 慣例 (不支援) PCRE |
| (\*BSR\_UNICODE) | (不支援) PCRE |

## <a name="content-license"></a>內容授權

> [!NOTE]
> 本頁的某些部分是根據 Chromium.org 創造和分享的作品加以修改，並根據[創用 CC 姓名標示 4.0 國際版本授權條款](http://creativecommons.org/licenses/by/4.0/)中所述條款加以使用。 原始頁面可在[此處](https://github.com/google/re2/wiki/Syntax)找到。
  
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />本作品根據<a rel="license" href="http://creativecommons.org/licenses/by/4.0/">創用 CC 姓名標示 4.0 國際版本授權條款</a>獲得授權。

## <a name="see-also"></a>請參閱

- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)