## Numeric Data Type
* ### Four integer type
  8 represents 8 bit i.e 1 and 0
    * int : 4 bytes : 2^(4*8)/2 possibilities : Range -2,14,74,83,648 to 2,14,74,83,647
    * short : 2 bytes : 2^(2*8)/2 possibilities : Range -32,768 to 32,785
    * long : 8 bytes : 2^(8*8)/2 possibilities : Ranges -92,23,37,20,36,85,47,75,808 to 92,23,37,20,36,85,47,75,807
    * byte : 1 bytes : 2^(1*8)/2 possibilities : Range -128 to 127

When we write down the number it called as number **Literal**
* Number ends with "L" it is a long number **40000L**
* When Number starts with 0x its hexadecimal **0xCAFE**
* When it starts with "0b" it is a binary number **0b1111_0101_0010_0000**

* ### Two Floating Points in JAVA
* float : 4 bytes : Approximately +/- 3.402822347E+38F(6-7 significant decimal digits)
* double : 8 bytes :Approximately +/- 1.79769313486231570E+308 (15 significant decimal digit)

**Float Literals**
* 0.5F
* Only use float if a library requires it
* Special value **Double.POSITIVE_INFINITY, Double.NEGATIVE_INFINITY, Double.NaN**

* ### The  **Char** Type 
* originally used to describe Unicode character 
* Nowadays:"Code Units" in the UTF-16 encoding
* Every Unicode character one or two char value
   * A has "Code point" U+0041 and it is encoded as single char value (hex 0041 or decimal 65)
   * ### 𝕆 
      has "code point" U+1D546 and is encoded by two units hex value D*35 DD46
* Avoid char unless you know that you won't run into Unicode character >= U+10000
* Character literals enclosed in single quotes: 'A', '\n', '\u2122'

* ### The **boolean** Type
* There  are two boolean values true , false
* No conversion in between int and boolean i.e true to 0 and false to 1 and vice versa

** All together Java has **8** Primitive Data Types
* int,long,shot,byte
* flot,double
* char
* boolean

## Variables
* Every variable must declare with a type, which comes before name of the Variable :
   ```
  int vacaionDaya;
  ```
* Initialization is Optional : 
  ```
  int days=365;
  ```
* Decleration can appear anywhere in block
   ```
   We can declar variable anywhere but it is suggested to Declare as close as possible to first use
   i.e. near to its use
  ```
* Can assign new value using "=" oprator
  ```
  days=12;
  ```
* Constant Declaration with **final** 
  ```
  final int days=14;
  ```
  **final makes variable constant,final means once it is initialized, that's the final time you have chance to change it**

## Mathematical Operation and Function

* Arithmetic : +,-,*,/
* Integer division and modulus: / and %(with integer operands ):
   * 15/2 is 7
   * 15%2 is 1
   * 15.0/2 is 7.5
* Math.sqrt(x) is square root of X
* Math.pow(a,b) is a^b
* Math.floorMod(a,b) is lik a%b with better behaviour for negative value
  Math.floorMode(-15,2) = 1
* Trigonometry and log functions:
   * Math.sin, Math.log......

**Starting from **Java 9** there is one convenient called **jshell**, and it gets executed directly, without the need of having to write **main()** and don't need to compile it.
this interactive shell very useful for to explore small expects of java**

## Hands on
  ```
  Open terminal and type "jshell"
 
 c:/user> jshell
  |  Welcome to JShell -- Version 20.0.2
  |  For an introduction type: /help intro

  jshell> 16/2
  $1 ==> 8

  jshell> 15/2
  $2 ==> 7

  jshell> 15%2
  $3 ==> 1

  jshell> 17.0/2
  $4 ==> 8.5

  jshell> Math.floorMod(-15,2)
  $7 ==> 1

  jshell> -15%2
  $8 ==> -1

  jshell> Math.sqrt(8)
  $5 ==> 2.8284271247461903

  jshell> Math.sqrt(4)
  $6 ==> 2.0


  ```
 
## Type Conversion
                         
  char
  
  &darr;

  int &larr; short &larr;  byte

  &darr;
  
  float &rarr; double

** ---- line represent data loss can be happened at the time of conversion**
  ```mermaid 
     graph LR 
     A[byte :1] -->B[short :2]
     B -->C[int :4]
     G[char :1]-->C
     C -->D[long :8]
     C -.->E[float :4]
     E -->F[double :8]
     D -.->E
     D -.->F
     
     
  ```
   
