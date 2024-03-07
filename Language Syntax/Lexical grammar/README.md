# Lexical grammar(词汇语法)

**lexical grammar**

​		**definition** :  The lexical grammar lays down the rules governing how a character sequence is divided up

into subsequences of characters, each part of which represents an individual token.

从上可以知道，词汇语法告诉编译器怎么样去把一个字符序列分成一个个token.

***



### 1. Lexical elements(词汇元素)

Lexical elements: include **token** and **preprocessing-token**.

#### 1_1. **token** 

​		**definition**:  A token is the smallest independent unit of meaning in a program, as defined by the compiler. 

There are five different types of tokens: 

>1. keywords. (关键字)
>2. identifier. (标识符)
>3. constant. (常量)
>4. string-literal. (字符串)
>5. punctuator. (标点符号)

##### 1_01. keywords: 

​		**definition**:  Reserved words that have special meaning in the programming language.

##### <img src="https://raw.githubusercontent.com/jayFTX/c17_library/master/img/Snipaste_2024-03-07_12-49-20.png" alt="keywords" style="zoom:50%;" />

+++



##### 1_02. identifier:  

​		**definition**: Names given to various program elements such as variables, functions, classes, etc. They typically 

consist of letters, digits, and underscores, with certain rules and conventions regarding their usage.

​    	**Syntax**(语法):

**Firstly** :   names:

​							expressions expressions ...   

​							expressions expressions 

​							expressions

***Consequently***，names = [expressions expressions ...]

​										  = [expressions expressions ]

​										  = [expressions]

*Note*: 表达式里的被空白隔开的标识是代表可连接的意思。

其中每个表达式 还能被 表达式(标识所定义的) 替换。

<img src="https://raw.githubusercontent.com/jayFTX/c17_library/master/img/identifier_.png" alt="identifier" style="zoom:50%;" align="left" />

<img src="https://raw.githubusercontent.com/jayFTX/c17_library/master/img/digit.png" alt="digit" style="zoom:50%;" align="left"/>

(6.4.2.1）第一张图片指定了 identifier 是可以等价于3个表达式其中之一，所以上述第一张图片可以理解为这样: 

​			identifier  = [identifier-non-digit],

​							  = [identifier  identifier-non-digit], 

​							  = [identifier  digit]



<img src="https://raw.githubusercontent.com/jayFTX/c17_library/master/img/Universial%20character%20names.png" alt="universal character names" style="zoom:57%;" align="left"/>

用以上规则可得:      1. universal-character-name = \u hexadecimal-digit hexadecimal-digit hexadecimal-digit hexadecimal-digit

​                                  that is,  universal-character-name = \u 后接 4个十六进制数。

​								  2.  universal-character-name = \U 后接8个十六进制数。 

相信你已经懂得怎么理解图片中的语法规则了!

***综上， 标识符构成规则: 不能以数字开头，但是可以用下划线，字母和universal-character-name开头,并且在后面能跟 任意个下划线，字母，数字和universal-character-name等***。

+++



##### 1_03. constant:





