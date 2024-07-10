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