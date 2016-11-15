# Programming Zone
歡迎來到 Amos, Victor 神的領域

先隨便丟一下

關於"size_t" C++ 規格書上的說明與提示
The type size_t is an implementation-deﬁned unsigned integer type that is large enough to contain the size in bytes of any object.

Note: It is recommended that implementations choose types for ptrdiff_t and size_t whose integer conversion ranks (4.13) are no greater than that of signed long int unless a larger size is necessary to contain all the possible values. —end note

什麼是integer conversion rank
http://www.enseignement.polytechnique.fr/informatique/INF478/docs/Cpp/en/c/language/integer_conversion_rank.html

進階說明
兩個算術類型的變數做算術運算，比如a + b，如果兩邊變數操作的類型不同，編譯器會自動做類型轉換，使兩邊類型相同之後再做運算，這稱為Usual Arithmetic Conversion。轉換規則如下：

1．如果有一邊的類型是long double，則把另一邊也轉成long double。

2．如果有一邊的類型是double，則把另一邊也轉成double。

3．如果有一邊的類型是float，則把另一邊也轉成float。

4．兩邊都是整數型，首先按第14.3.1節講過的規則對a和b做Integer Promotion，如果類型仍不相同，則需要繼續轉換。我們規定char、short、int、long、long long的轉換級別（Integer Conversion Rank）一個比一個高，同一類型的有符號和無符號數具有相同的Rank。轉換規則如下：

如果兩邊都是有符號數，或者都是無符號數，那麼較低Rank的類型轉換成較高Rank的類型。例如unsigned int和unsigned long做算術運算時都轉成unsigned long。

如果一邊是無符號數另一邊是有符號數，無符號數的Rank不低於有符號數的Rank，則把有符號數轉成另一邊的無符號類型。例如unsigned long和int做算術運算時都轉成unsigned long，unsigned long和long做算術運算時也都轉成unsigned long。

剩下的情況是：一邊有符號另一邊無符號，並且無符號數的Rank低於有符號數的Rank。這時又分為兩種情況，如果有符號數類型能夠覆蓋無符號數類型的取值範圍，則把無符號數轉成另一邊的有符號類型。例如在遵循LP64的平台上unsigned int和long做算術運算時都轉成long。

否則，也就是這個有符號數類型不足以覆蓋這個無符號數類型的取值範圍，則把兩邊都轉成有符號數的Rank對應的無符號類型。例如在遵循ILP32的平台上unsigned int和long做算術運算時都轉成unsigned long。


## Kate 老師
您的 Kate 老師已上線...

## Sharing Links (好文值得一看)
  * [merge branch 的新選擇： rebase](https://ihower.tw/blog/archives/3843)
