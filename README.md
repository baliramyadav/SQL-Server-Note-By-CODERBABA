# SQL Server Note By CODERBABA
 Don't miss out on this essential guide to mastering SQL Server data types! 

SQL Server Data Types 📊
________________________________________
Index:
1.	Char & Varchar 🔤
2.	Nchar, Nvarchar & Unicode Data Types 🔠
3.	Tinyint, Smallint, Int & Bigint 🔢
4.	Decimal/Numeric Data Type ➗
5.	Money & SmallMoney 💵
6.	Float & Real Data Types 🌊
7.	Date Data Type 📅
8.	Time Data Type ⏰
9.	DateTime2 Data Type ⏳
10.	DateTimeOffset ⏰⏳
11.	DateTime & SmallDateTime 📅⏰
12.	Date Formats 📜
13.	DateTime2 Vs DateTime ⏳🆚📅
14.	Bit & Boolean 🅱️
15.	Binary & VarBinary 🔢🔄


#watch full video tutorial
![010101](https://github.com/baliramyadav/SQL-Server-Note-By-CODERBABA/assets/80908177/3a607291-0f40-4d89-83e0-aa6d65693ab0)

Why 90% of Developers Are Wrong About CHAR, VARCHAR and NVARCHAR in SQL Server
https://youtu.be/gwtideAuxSc



SQL Server Data Types 📊________________________________________

SQL Server data types define the type of data that a column in a table can hold. Let's dive into the categories and details of SQL Server data types:________________________________________

1. String Data Types 📝
•	Char & Varchar 🔤

•	Char: Fixed-length string data type. Store a-z, A-Z (letters), numbers & special characters.

•	Example: char(5) will store 'SQL ' for 'SQL' (padded with spaces).

•	Varchar: Variable-length string data type.

•	Example: varchar(5) will store 'SQL' for 'SQL'. (No padded spaces)

•	Example: varchar will store 1 character as default value

•	Text & NText 📜

•	Text: Variable-length non-Unicode data with a maximum length of 2^31-1 (2,147,483,647) characters.

•	NText: Variable-length Unicode data with a maximum length of 2^30-1 (1,073,741,823) characters.

________________________________________

2. Unicode String Data Types 🌐
3. 
•	NChar & NVarchar 🔤

•	NChar: Fixed-length Unicode data.

•	Example: nchar(5) will store 'SQL ' for 'SQL'.

•	NVarchar: Variable-length Unicode data.

•	Example: nvarchar(5) will store 'SQL' for 'SQL'.


________________________________________


3. Exact Numeric Data Types 🔢
4. 
•	Tinyint, Smallint, Int & Bigint 🕰️

•	Tinyint: 1-byte integer data (0 to 255).

•	Smallint: 2-byte integer data (-32,768 to 32,767).

•	Int: 4-byte integer data (-2^31 to 2^31-1).

•	Bigint: 8-byte integer data (-2^63 to 2^63-1).

•	Decimal/Numeric 📈

•	Fixed precision and scale numeric data.

•	Example: decimal(5,2) can hold values like 123.45.

•	Money & SmallMoney 💵

•	Money: Monetary data from -922,337,203,685,477.5808 to 922,337,203,685,477.5807.

•	SmallMoney: Monetary data from -214,748.3648 to 214,748.3647.


________________________________________

4. Approximate Numeric Data Types 🎯
5. 
•	Float & Real 🌊

•	Float: Floating-point number with 7-digit precision.

•	Example: float can hold values like 123.456789.

•	Real: Floating-point number with 15-digit precision.

________________________________________
5. Date/Time Data Types 📅
   
•	Date 📆

•	Date only (no time).

•	Example: '2022-04-01'

•	Time ⏰

•	Time only (no date).

•	Example: '14:30:00'

•	DateTime2 🕰️

•	Date and time with fractional seconds.

•	Example: '2022-04-01 14:30:00.1234567'

•	DateTimeOffset 🕰️

•	Date, time, and time zone offset.

•	Example: '2022-04-01 14:30:00.1234567 +05:30'

•	DateTime & SmallDateTime 🕰️

•	Date and time.

•	Example: '2022-04-01 14:30:00'

________________________________________
6. Binary Strings 📊


•	Binary & VarBinary 📊

•	Binary: Fixed-length binary data.

•	VarBinary: Variable-length binary data.

________________________________________
7. Other Data Types 📦
   
•	Bit & Boolean 🔘

•	Bit: Can hold 0, 1, or NULL.

•	Boolean: Synonymous with Bit.

Key Points 📍

•	SQL Server supports various data types categorized based on the kind of data they can hold.

String Data Types 📜

String data types are used to store sequences of characters, which can include letters, numbers, symbols, and special characters. SQL Server provides two main categories of string data types: fixed-length and variable-length.
 

Fixed-Length String Data Types 📏

1.	CHAR & NCHAR 🔤
   
•	Description:

Char and Nchar are fixed-length string data types.

•	Size:

You need to specify a fixed size when defining the column.

•	Example:
char(5) will always store 5 characters. If you insert 'SQL', it will be stored as 'SQL ' (padded with spaces).
•	Usage:

Suitable for storing codes, ID numbers, and fixed-length strings.

Variable-Length String Data Types 📐

2.	VARCHAR & NVARCHAR 🔠
   
•	Description:
Varchar and Nvarchar are variable-length string data types.

•	Size:
You can store strings up to a maximum defined length.

varchar= 8000 byte,    nvarchar= 4000

•	Example:
varchar(5) will store up to 5 characters. If you insert 'SQL', it will be stored as 'SQL' (without padding spaces).
•	Usage:

Ideal for storing names, addresses, and variable-length data.
Notes: In Varchar ASCII values can only represent 256 characters. Like Capital A-Z, small a-z, numbers from 0-9.
where as in Nvarchar we can write ASCII values & special characters. Unicode value can represent more than 256 ASCII characters. Like Capital A-z, Small a-z, number from 0-9 and special character like Chinese, Korean or Japanese characters.

Differential Between Fixed-Length and Variable-Length 📊

•	Storage:      
•	Fixed-Length (CHAR): Allocates a fixed amount of storage.

•	Variable-Length (VARCHAR): Allocates storage as per the data length.

•	Padding:
•	Fixed-Length (CHAR): Pads with spaces to reach the defined length.

•	Variable-Length (VARCHAR): Does not pad with spaces.

•	Storage Efficiency:
•	Fixed-Length (CHAR): Less storage efficient for varying length data due to padding.

•	Variable-Length (VARCHAR): More storage efficient for varying length data.
Usage Tips 💡

•	Char/Nchar: Best for storing data with a consistent and fixed length.
•	Varchar/Nvarchar: Best for storing data with varying lengths, optimizing storage space.



What is Char Data Type? 🔤

The CHAR data type in SQL Server is a fixed-length character data type. It allows you to store characters, numbers, and special characters in strings up to 8000 bytes in size. CHAR data types are best used for storing data that is of a consistent length.

Best Use Cases ✅
•	State codes in the United States (e.g., CA for California).

•	Gender codes (e.g., M for Male, F for Female).

•	Phone numbers.

•	Postal codes.

these columns are store fixed length char values

Limitation ❌
Using a CHAR column is not ideal for storing data where the length varies significantly, such as:
•	Addresses.
•	Memo fields.
Padding in Char 🚀
Even though CHAR is a fixed-length data type, it can still store values shorter than its defined length. When you insert a string shorter than the column's length:
•	Padding Occurs: Spaces are automatically added to the right to match the defined length.
Example:
•	CHAR(10) defined.
•	Insert 'SQL' into the column.
•	Stored value: 'SQL ' (padded with spaces).
Space Efficiency 📊
Each CHAR column uses a consistent amount of disk space or memory because it is always fully populated with spaces when needed.
Challenges with Trailing Spaces ⚠️
The trailing spaces can pose challenges, especially when:
•	Searching: You might miss records due to trailing spaces.
•	Comparing: Comparisons can yield unexpected results due to added spaces.
Example:
If you search for 'SQL' in a CHAR(10) column and the stored value is 'SQL ', the search might not yield the expected result.
________________________________________
Conclusion 📌
While the CHAR data type is excellent for storing consistent-length data efficiently, its automatic padding with spaces can introduce complexities. Always consider the nature and variability of your data before choosing between CHAR and VARCHAR.









VARCHAR: The Variable-Length Character Data Type 📝
VARCHAR is a versatile data type in SQL Server that is used to store variable-length character strings. Unlike CHAR, which is a fixed-length data type, VARCHAR only consumes the necessary space required to store the data, without adding any extra spaces.
Characteristics of VARCHAR 📊
•	Storage Capacity 📏:
•	VARCHAR columns can store strings up to 8,000 bytes in size.
•	Flexibility 🔄:
•	It can store a mix of characters, numbers, and special characters, similar to the CHAR column.
•	Storage Efficiency 💾:
•	It only occupies the space required by the stored string, eliminating the need for padding with extra spaces.
Performance Consideration ⚙️
•	Calculation Overhead 📈:
•	Due to the variable-length nature of VARCHAR, the length of the data needs to be calculated and stored along with the actual data. This extra calculation can make VARCHAR slightly less performant compared to CHAR columns.
•	Disk Space Savings 💿:
•	The storage efficiency of VARCHAR often results in significant disk space savings. The reduced disk space usage can sometimes offset the performance cost associated with its variable-length nature.
Example 📝
•	Using CHAR
 
•	If you insert '101' as EmpID and 'John' as EmpName, they will be stored as '101 ' and 'John ' (padded with spaces).
•	Using VARCHAR
 
•	If you insert '101' as EmpID and ‘CoderBaba’ as EmpName, they will be stored as '101' and ‘CoderBaba’ (without padding spaces).
Best Practices ✅
•	Use VARCHAR when the length of the data varies significantly, as it offers better storage efficiency.
•	VARCHAR is suitable for storing textual data like names, addresses, and descriptions.
Interview Insight 🎙️
•	Question: How does VARCHAR differ from CHAR in terms of storage and performance?
Answer:
•	VARCHAR is a variable-length data type, whereas CHAR is fixed-length.
•	VARCHAR consumes only the required space, eliminating the need for padding with extra spaces.
•	CHAR is more storage efficient for fixed-length data but can be less performant when compared to VARCHAR for variable-length data due to the overhead of calculating the data length.

VARCHAR(MAX) in SQL Server 📝________________________________________
Overview 📌 The VARCHAR(MAX) data type is an extension of the VARCHAR data type, supporting variable-length character data. While it has similarities to VARCHAR, VARCHAR(MAX) is designed to handle larger string values, supporting character strings up to 2 GB (2,147,483,647 bytes) in size.________________________________________
Key Features 🔍
•	Variable Length: Just like VARCHAR, VARCHAR(MAX) stores variable-length character data.
•	Size Limit: It supports character strings up to 2 GB in length, making it suitable for storing large text data.________________________________________
Why Choose VARCHAR(MAX)? 🤔
While you might be tempted to use VARCHAR(MAX) all the time due to its large size, there are specific reasons and limitations to consider:
1.	Indexing Limitations ❌
•	VARCHAR(MAX) columns cannot be used as key columns in indexes.
Example:
 

2.	Length Restriction 📏
•	You cannot restrict the length of the VARCHAR(MAX) column like you can with standard VARCHAR.
3.	Storage Considerations 📦
•	Large string values in VARCHAR(MAX) columns utilize LOB_DATA allocation units, which are slower than IN_ROW_DATA storage allocation units.
•	LOB_DATA storage doesn’t support page and row compression.
________________________________________
Eliminating Truncation Errors ✂️
Using VARCHAR(MAX) can indeed help eliminate truncation errors, but there's a catch:
•	It can prevent truncation up to 2,147,483,647 bytes.
Example:
 
However, trying to store a string longer than this limit will result in an error.
________________________________________
Conclusion 📌
While VARCHAR(MAX) provides the flexibility to store large text data, it's essential to be aware of its limitations and choose the appropriate data type based on your specific requirements.
Remember, always optimize your database design to ensure efficient storage and performance! 🚀








Unicode String Data Types in SQL Server 🌐
Unicode encoding is a character encoding standard that is used to represent text in many modern software applications, databases, and communication protocols. Unicode provides a unique number for every character, regardless of the platform, program, or language. This ensures that text is displayed and processed consistently across different systems and languages.
In SQL Server, Unicode encoding is commonly used to store data in Unicode character sets, such as NCHAR, NVARCHAR, and NTEXT.
Data Types in SQL Server for Unicode:
•	NCHAR: Fixed-length Unicode string.
•	NVARCHAR: Variable-length Unicode string.
•	NTEXT: Variable-length Unicode text.

📝 What are NCHAR, NVARCHAR, and NTEXT?
NCHAR: Stands for "NATIONAL CHARACTER".
NVARCHAR: Stands for "NATIONAL CHARACTER VARYING".
NTEXT: ISO synonym for "NATIONAL TEXT".
Example:
1. Storing Unicode Data:
Let's say you want to store a Unicode string "हिन्दी" (which means "Hindi" in English) in a table.
 


Inserting Unicode data into the table:
 
2. Retrieving Unicode Data:
 
Output:
 
Benefits of Unicode Encoding:
1.	Multilingual Support: Unicode supports characters from multiple languages, making it easier to store and retrieve data in different languages.
2.	Consistency: Unicode ensures consistent representation of text across different platforms and systems.
3.	Compatibility: Unicode encoding is widely supported by modern software applications and databases, making it easier to share and exchange data.
The idea was to use:
•	VARCHAR for ASCII characters
•	NVARCHAR for non-ASCII characters
📊 Key Difference:
•	VARCHAR: Stored as regular 8-bit data (1 byte per character).
•	NVARCHAR: Stored as 2 bytes per character.

📝 Example:
Let's consider storing the word "Hello":
•	VARCHAR: Takes up 5 bytes (H + e + l + l + o).
•	NVARCHAR: Takes up 10 bytes (2 bytes per character).
📝 Capacity:
•	NVARCHAR can hold up to 4000 characters but takes double the space compared to VARCHAR.

SQL Server Int Data Types: tinyint, smallint, int & bigint 📊
SQL Server integer data types are used to store whole numbers, both positive and negative. They do not support fractions. SQL Server provides four types of integer data types, each with different ranges and sizes: tinyint, smallint, int, and bigint.
 


Types and Their Ranges 📏
•	tinyint:
•	Range: 0 to 255
•	Size: 1 byte
•	smallint:
•	Range: -32,768 to 32,767
•	Size: 2 bytes
•	int:
•	Range: -2,147,483,648 to 2,147,483,647
•	Size: 4 bytes
•	bigint:
•	Range: -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807
•	Size: 8 bytes
Creating an Integer Column 📝
 
Inserting Data 📥
 
Reading the Values 📖
 
Choosing the Right Integer Data Type 🎯
Always select the smallest data type that meets the requirements of the column to optimize storage and performance.
•	For storing ages: tinyint is sufficient as it can store up to 255.
•	For larger numbers, but not exceeding 32,768: Use smallint.
•	For general use cases: int is recommended.
•	Use bigint only when expecting values greater than the max value of int (i.e., 2,147,483,647). Keep in mind that bigint consumes double the space compared to int.

What are Decimal & Numeric Data Types? 💡
The Decimal and Numeric data types in SQL Server represent numbers that contain both an integer part and a fractional part, separated by a decimal point. These data types accommodate both negative and positive numbers.
🔁 Note: In SQL Server, both Decimal and Numeric data types are identical; you can use them interchangeably.

Defining a Decimal Number 🔢
Use the following syntax to define a Decimal number:
 
•	p (Precision):
•	Defines the maximum number of digits you can store, including both the integer and fractional parts.
•	Example: The number 123.45 has a precision of 5 because it has 5 digits.
•	The minimum precision is 1, and the maximum is 38. The default precision is 18.
•	s (Scale):
•	Defines the number of decimal digits you can store.
•	Example: DECIMAL(5,2) will store the number up to 2 decimal places.
•	If you attempt to insert a number with more decimal places than the column allows, SQL Server will round it.
•	If the number lacks a decimal position (like an integer), SQL Server will implicitly add .00 to the number.
________________________________________
Maximum Limit & Range 📏
•	The precision and scale determine the maximum limit for storing values in the decimal data type.
•	The maximum number of digits to the right of the decimal point (the integer part) is equal to the precision minus scale (p-s).
•	Example: In a Decimal(5,2) column, the integer portion can contain only 3 digits (5-2).
•	Hence, in Decimal(5,2), you can store numbers from -999.00 to 999.99.
•	For Decimal(38,2), the range is -999999999999999999999999999999999999.00 to 999999999999999999999999999999999999.99.
•	If you need to store numbers larger than this range, you should use the float data type.
________________________________________
Size in Bytes 💾
•	The storage size of a decimal number on the disk depends on the precision used.
•	Precisions from 1 to 9 require 5 bytes of disk space.
•	Example: Decimal(3,2), Decimal(5,2), and Decimal(9,2) all use 5 bytes of disk space, although Decimal(9,2) can store more numbers.
________________________________________
Creating a Decimal Column 🛠️
Here's how to create a table with decimal columns:
 
Inserting Decimal Values ➕
To insert a new value using the insert statement:
 
🔍 Result:
 
If you attempt to insert a value exceeding the column limit, SQL Server throws an "Arithmetic overflow error."
 
🔥 Error:
Arithmetic overflow error converting numeric to data type numeric. The statement has been terminated.

However, if you have more digits in the fractional part, SQL Server will round them off:
 
 

Money & SmallMoney Data Types in SQL Server 💰
________________________________________
Money Data Type 💵
•	Description:
The money data type in SQL Server is designed to store monetary or currency values. It has a fixed precision with 4 digits after the decimal point.
•	Range:
•	Minimum: -922,337,203,685,477.5808
•	Maximum: +922,337,203,685,477.5807
•	Storage:
•	Size: 8 bytes
Example:
•	1234.00 is stored as 12340000
•	5555.5555 is stored as 55555555
•	Decimal Representation:
Even though money is stored without decimals, the decimal point and digits are added when you query and view the data.
________________________________________
SmallMoney Data Type 💵
•	Description:
The smallmoney data type is similar to money but consumes less storage.
•	Range:
•	Minimum: -214,748.3648
•	Maximum: +214,748.3647
•	Storage:
•	Size: 4 bytes
Example:
•	1234.5678 is stored as 12345678
________________________________________
Differential Between Money & Decimal 📊
•	Storage:
•	Money: Fixed-size storage.
•	Decimal: Variable-size storage based on precision.
•	Internal Representation:
•	Money: Stored as integer (BigInt).
•	Decimal: Stored with the specified number of decimal places.
Example with Money:
 
Result:
 
Example with Decimal:
 
Result:
 
•	Precision:
•	Money: Fixed 4 fraction digits; loses precision in mathematical operations.
•	Decimal: Can maintain precision up to 38 digits.
•	Performance:
•	Integer Operations: Money operations are faster as they are treated as integers.
•	Storage Efficiency: Money requires less storage compared to decimals. Smallmoney requires 4 bytes, while the equivalent decimal(10,4) needs at least 9 bytes. Money takes 8 bytes, while decimal(19,4) needs 9 bytes.
________________________________________
Creating and Using Money Data Type 📋
Creating Table with Money Data type:
 
Inserting & Retrieving Values:
 
Result:
 

What are Float & Real Data Types in SQL Server? 🤔
Floating-Point Numbers: Floating-point numbers don't have a fixed decimal point; it can appear anywhere in the number, thus termed as "Floating Point" numbers. The behavior of float and real adheres to the IEEE Standard for Floating-Point Arithmetic.
Scientific Notation: These numbers are stored using the scientific notation in binary format. For instance, 650,000,000 can be represented as 6.5 ✕ 10^8, where:
•	6.5 is Significand
•	10 is the base
•	8 is the exponent
 
Float & Real in SQL Server 🖥️
•	Float: Double Precision 64-bit format, using 8 bytes of storage.
•	Real: Single Precision 32-bit format, using 4 bytes of storage.
Binary Representation:
•	Float (64-bit): 1 bit for sign, 11 bits for exponent, and 52 bits for the fraction.
•	Real (32-bit): 1 bit for sign, 8 bits for exponent, and 23 bits for the fraction.
 
Creating Float & Real Columns 📝
The syntax for creating a float column is float(n), where n is between 1 to 53. The default value of n is 53.
•	float(1) to float(23) creates a Single Precision 32-bit column (mapped to real).
•	float(24) to float(53) creates a Double Precision 64-bit column.

 
Output:
 
 
Example:
•	decimal(9,2) uses 5 bytes but can store from -9999999.99 to 9999999.99.
•	int uses 4 bytes but can't store fractions.
•	real (32-bit) can store from -3.4E38 to 3.4E38.
________________________________________
Loss of Precision 🚫
Due to limited storage, floating-point numbers might lose precision.
Example:
 
This happens because 0.1 is stored approximately as 0.100000001490116119384765625 (in 32-bit single precision).
________________________________________
Which One to Use? 🤔
•	Decimal: If the number stays below the maximum precision provided by the decimal (which is 38), it's preferred.
•	Float/Real: Use when handling large numbers.
•	Real: If storage is a primary concern (only 4 bytes), and a slight loss in accuracy is acceptable.
Recommendations:
•	Avoid using float for equality checks (= & <>), rounding of numbers, etc.
•	Especially avoid in financial applications where high accuracy is crucial.
________________________________________
🔍 Key Takeaway:
Choose the appropriate data type based on the precision and storage requirements of your data. Always be cautious of the potential loss of precision when using floating-point numbers, especially in critical applications.



What is the Date Data Type in SQL Server? 🤔
The Date data type in SQL Server is used to store date values. Unlike DateTime or DateTime2, the Date data type stores only the date without any time or time zone information.

How Does SQL Server Store Date? 📚
SQL Server internally represents dates as integers:
•	The base date is 1900-01-01.
•	Each day after the base date is represented by an integer value, with 1 being 1900-01-02, 2 being 1900-01-03, and so on.
Examples:
•	Convert the integer 0 to date:
 
•	Result: 1900-01-01 00:00:00.000
•	Convert the current date to an integer:
 
•	Result: 44177
•	Convert an integer back to a date:
 
•	Result: 2020-12-14 00:00:00.000
________________________________________
Using the Date Data Type 🛠️
•	Creation of Date Column:
 
Inserting Date Values:

 
Displaying Date: By default, SQL Server displays dates in the format YYYY-MM-DD. Custom formatting can be achieved using the FORMAT function.
 
Storage Size & Range 📏
•	Min Date: 0001-01-01
•	Max Date: 9999-12-31
•	Storage: 3 Bytes
•	Default Value: 1900-01-01
•	Default String Literal Format: YYYY-MM-DD
________________________________________
Date Format Considerations 📌
•	Universal Format: Always use YYYYMMDD when inserting dates to avoid ambiguity.
 
Other accepted formats:
 
Language Settings: SQL Server uses the @@LANGUAGE setting to determine date formats. To check the current language:
 
Use sp_helplanguage to find the dateformat value:
 
•	Based on the format (dmy, mdy, ymd), insert dates accordingly.
•	Using DATEFORMAT: Temporarily set the date format for the current session:
 
Two-Digit Year Considerations 📅
•	For two-digit years:
•	Cut-off Year: 2049
•	Time Span: 1950 to 2049
 
•	Customizing the Cut-off Year: Use the two digit year cutoff option to adjust the cut-off year.
________________________________________
Summary 📝: 
The Date data type in SQL Server provides a clean and efficient way to store and manipulate date values without the overhead of time and time zone information. Always remember to use the universal YYYYMMDD format when inserting dates to maintain consistency and prevent ambiguity.
What is Time Data Type in SQL Server?
Time is a SQL Server data type used to store time of the day without a time zone, using a 24-hour format. It exclusively holds the time, excluding the date.
How SQL Server Stores Time? 🕰️
Internally, SQL Server represents time as an integer. This integer signifies the number of clock ticks after midnight. Each tick is equivalent to 1⁄10000000 of a second. The smallest unit of time it can store is 0.0000001 second. If a time less than this is input, it gets rounded off. Time is displayed in the format:
 
Syntax:
 
Here, n denotes the number of digits for the fractional part of the seconds, ranging from 0 to 7. By default, n is 7.
Storage Size Based on Precision 📊
Data Type	Precision & Scale	Storage Size (bytes)	Example
time	*Default (time(7))	16,7	09:31:35.6170000
time(0)	8,0	3	09:31:36
time(1)	10,1	3	09:31:35.6
time(2)	11,2	3	09:31:35.62
time(3)	12,3	4	09:31:35.617
time(4)	13,4	4	09:31:35.6170
time(5)	14,5	5	09:31:35.61700
time(6)	15,6	5	09:31:35.617000
time(7)	16,7	5	09:31:35.6170000
Default Time Format ⏲️
SQL Server displays time in the 24-hour format:
 
Where:
•	hh represents the hour (00 to 23)
•	mm represents the minute (00 to 59)
•	ss represents the second (00 to 59)
•	nnnnnnn is the fractional part of the seconds. The number of digits is determined by the column definition time(n). Note: It does not use milliseconds.
________________________________________
Creating Time Columns in a Table 📄
 
Inserting Values 📝
INSERT INTO testTime (colTime, col0, col1, col2, col3, col4, col5, col6, col7) 
VALUES (CURRENT_TIMESTAMP, CURRENT_TIMESTAMP, CURRENT_TIMESTAMP, CURRENT_TIMESTAMP, CURRENT_TIMESTAMP, CURRENT_TIMESTAMP, CURRENT_TIMESTAMP, CURRENT_TIMESTAMP, CURRENT_TIMESTAMP);

 
Time Formats for Insertion 🔄
You can insert time in various formats:
•	hh:mm[:ss][.fractional seconds][AM][PM]
Examples: '09:30:30', '09:31:57.999', '09:31:57.9002640'
•	hh:mm[:ss][:fractional seconds][AM][PM]
Examples: '15:10:20:60', '09:31:57











DateTime2 in SQL Server 📅⏰
________________________________________
Description: DateTime2 is a data type in SQL Server used to store both date and time information. It offers enhanced precision compared to the traditional DateTime and SmallDateTime types.
________________________________________
Key Features:
•	Precision:
DateTime2 can store fractional seconds with up to 7 decimal places, equivalent to 1⁄10000000 of a second.
•	Time Format:
The time is represented based on a 24-hour clock.
•	Range:
DateTime2 has a broader range than DateTime and SmallDateTime, supporting a wider span of dates from January 1, 0001, to December 31, 9999.
•	SQL Compliance:
DateTime2 is compliant with the SQL standard, making it more consistent across different database systems.
Example: Let's consider an example to understand DateTime2 better:
 
In this example:
•	The EventDateTime column stores a specific date and time.
•	The (3) specifies the precision of the DateTime2 data type, which means it will store up to 3 decimal places for the fractional seconds.
Advantages Over DateTime & SmallDateTime:
•	Better Precision: DateTime2 offers higher precision with up to 7 decimal places.
•	Flexibility: It provides a wider range and more flexibility in date and time operations.
•	Recommendation: Microsoft recommends using DateTime2 over DateTime and SmallDateTime due to its enhanced features and compliance with SQL standards.
How Date & Time is Stored 🕰️
SQL Server stores both date and time as integers:
•	Date: Stored as the number of days elapsed since a base date, which is 1900-01-01.
•	Time: Stored as the number of clock ticks after midnight. Each tick is 1/10000000 of a second. The smallest unit stored is 0.0000001 second.
Precision & Storage 📏
Data type	Storage Size (bytes)	Example
DateTime2	8	2020-12-23 15:40:45.2756145
DateTime2(0)	6	2020-12-23 15:40:45
DateTime2(1)	6	2020-12-23 15:40:45.3
DateTime2(2)	6	2020-12-23 15:40:45.28
DateTime2(3)	7	2020-12-23 15:40:45.276
DateTime2(4)	7	2020-12-23 15:40:45.2756
DateTime2(5)	8	2020-12-23 15:40:45.27561
DateTime2(6)	8	2020-12-23 15:40:45.275615
DateTime2(7)	8	2020-12-23 15:40:45.2756145
Range & Properties:
•	Syntax: datetime2 [ (fractional seconds precision) ]
•	Usage: DECLARE @MyDatetime2 datetime2(7)
•	Date range: 0001-01-01 through 9999-12-31
•	Time range: 00:00:00 through 23:59:59.9999999
•	Time zone offset: No
•	Default value: 1900-01-01 00:00:00
Creating DateTime2 Column:

 

Inserting Date & Time 📝

INSERT INTO TestTable (colDefault, col0, col1, col2, col3, col4, col5, col6, col7) VALUES 
('2020-12-23 15:40:45.2756145','2020-12-23 15:40:45.2756145','2020-12-23 15:40:45.2756145', '2020-12-23 15:40:45.2756145','2020-12-23 15:40:45.2756145','2020-12-23 15:40:45.2756145', '2020-12-23 15:40:45.2756145','2020-12-23 15:40:45.2756145','2020-12-23 15:40:45.2756145')		

 
Displaying the Date & Time 📊
Dates are stored as numbers and are independent of any formats.
SQL Server displays dates by default in YYYY-MM-DD hh:mm:ss[.nnnnnn]. Refer to the SQL Server date formats for a list of various date formats and conversion methods.
Safe Insertion Format: Always use the format YYYY-MM-DD hh:mm:ss[.nnnnnnn] to insert dates. This format is universal and prevents interpretation issues.
Example:
 
Language Settings & DATEFORMAT 🌍
Language settings influence the date formats you can use for inserting date values.
Check Current Language:
SELECT @@language;
Check Date Format:
EXEC sp_helplanguage; 
The format might be dmy, mdy, or ymd.
Using DATEFORMAT: You can set the date format to dmy, mdy, or ymd, but remember it works only for the current session.
Example:
 
Two-digit Year & Separators 🔢
Always use four-digit years to avoid misinterpretation by SQL Server.
Example:
 
Output:
 
What is DateTimeOffset in SQL Server? 🤔
The DateTimeOffset data type in SQL Server combines date, time, and time zone offset information. While it's similar to both DateTime and DateTime2, it uniquely stores the time zone offset, unlike DateTime and DateTime2.
What is Time Zone Offset? 🌍⏳
A Time Zone represents a geographical region with the same standard time. The Time Zone Offset signifies the difference between local time and Coordinated Universal Time (UTC).
Syntax 📝
 
n: Number of digits for the fractional part of the seconds (0 to 7, default is 7).
Examples of DateTimeOffset Precision 🕰️
Data Type	Precision & Scale	Storage Size (bytes)	Example
datetimeoffset	34,7	10	2020-12-20 17:20:12.5636531 +05:30
datetimeoffset(0)	26,0	8	2020-12-20 17:20:13 +05:30
datetimeoffset(1)	28,1	8	2020-12-20 17:20:12.6 +05:30
datetimeoffset(2)	29,2	8	2020-12-20 17:20:12.56 +05:30
datetimeoffset(3)	30,3	9	2020-12-20 17:20:12.564 +05:30
datetimeoffset(4)	31,4	9	2020-12-20 17:20:12.5637 +05:30
datetimeoffset(5)	32,5	10	2020-12-20 17:20:12.56365 +05:30
datetimeoffset(6)	33,6	10	2020-12-20 17:20:12.563653 +05:30
datetimeoffset(7)	34,7	10	2020-12-20 17:20:12.5636531 +05:30
________________________________________
Default Format 📅⏰
SQL Server uses the 24-hour format:
 
•	yyyy: Year
•	MM: Month
•	dd: Day
•	hh: Hour (00-23)
•	mm: Minute (00-59)
•	ss: Second (00-59)
•	nnnnnnn: Fractional part of the seconds (based on n, no milliseconds)
•	[{+|-}hh:mm]: Time zone offset
Time Zone Offset Details 🌐⏰
•	hh: Two digits (-14 to +14)
•	mm: Two digits (00-59)
•	+/-: Specifies addition or subtraction from UTC
•	Valid range: -14:00 to +14:00
Range & Default Values 📆
•	Date Range: 0001-01-01 to 9999-12-31
•	Time Range: 00:00:00 to 23:59:59.99999
•	Time Zone Offset Range: -14:00 through +14:00
•	Default Value: 1900-01-01 00:00:00 00:00
Creating a DateTimeOffset Column 📊
Here's how to create a table with 8 DateTimeOffset columns, each having a different fractional seconds precision:
 
Inserting Values 📝
Use SYSDATETIMEOFFSET() to insert the current datetime with the time offset into the table:
 
 
Which to Use: DateTime2 or DateTimeOffset? 🤔
•	DateTime2: Best for single time zone applications.
•	DateTimeOffset: Suitable for applications spanning multiple time zones. It stores the local time along with the time zone offset, making it more versatile.








SQL Server DateTime & SmallDateTime Data Types ⏰
________________________________________
DateTime in SQL Server 📅⏰
•	Description:
The DateTime data type in SQL Server is used to store both date and time together, based on a 24-hour clock. It represents the number of clock ticks after midnight, with each tick being 1⁄300 of a second.
•	Format:
Displayed in the format: hh:mm:ss[.nnn]
•	Usage:
 	
 
SmallDateTime in SQL Server ⏳
•	Description:
The SmallDateTime data type also stores both date and time but with precision limited to minutes, excluding seconds.
•	Rounding Behavior:
If seconds are inserted:
•	Values up to 29.998 seconds are rounded down to the nearest minute.
•	Values from 29.999 seconds and above are rounded up to the nearest minute.
•	Usage:
 
 
 
DateTime & SmallDateTime Examples 📋
•	Creating DateTime & SmallDateTime Columns:
 
Inserting Values:
Insert into Table1 (Column1, Column2) Values ('2020-12-21 12:40:53', '2020-12-21 12:40:53' )
 
Local Variables:
 
Default Date & Time: If you don't provide a time, it defaults to 00:00:00.
 
If no date is provided, it defaults to 1900-01-01.
 
Range Limitations 📏
Both these data types have limitations:
•	DateTime: Minimum: 1753-01-01
•	SmallDateTime: Minimum: 1900-01-01
 




















SQL Server Date Formats 📅
📌The FORMAT function in SQL Server allows us to display dates in various formats. SQL Server internally stores dates and times as integers. However, the way dates and times are displayed varies from culture to culture. For instance, while some prefer the format DD/MM/YYYY, others might opt for YYYY/MM/DD. Hence, it's crucial to format dates and times according to the user's preference before presenting it to them.
________________________________________
Usage and Syntax 🛠️
The FORMAT function was introduced in SQL Server 2012 and is used as follows:
FORMAT(value, format [, culture]) 
•	value: A valid date expression to format.
•	format: The format string.
•	culture: The culture to use for formatting.
For versions prior to SQL Server 2012, the CONVERT function should be used.
________________________________________
Format Strings 📝
There are two types of format strings available:
1.	Standard Format String
2.	Custom Format String
________________________________________
Custom Format Strings 🎨
Custom format strings allow us to format the date and time using format specifiers. These can be combined in various ways to get the desired output.
Example:
 
Day, Month, and Year Formats 🗓️
Here are the format specifiers to format the day, month, and year:
•	Day Formats:
•	d: Day of the month (1 through 31).
•	dd: Day of the month (01 through 31). Single-digit day is formatted with a leading zero.
•	ddd: Abbreviated name of the day of the week (e.g., Fri).
•	dddd: Full name of the day of the week (e.g., Friday).
Example:
 
Month Formats 📆
Month uses M as the format specifier. Remember, m stands for minutes.
Example:
 


Year Formats 📅
Example:
 

SQL Server Date Formats 📅
________________________________________
Introduction 📌
The FORMAT function in SQL Server allows us to display dates in various formats. SQL Server internally stores dates and times as integers. However, the way dates and times are displayed varies from culture to culture. For instance, while some prefer the format DD/MM/YYYY, others might opt for YYYY/MM/DD. Hence, it's crucial to format dates and times according to the user's preference before presenting it to them.
________________________________________
Usage and Syntax 🛠️
The FORMAT function was introduced in SQL Server 2012 and is used as follows:
sqlCopy code
FORMAT(value, format [, culture]) 
•	value: A valid date expression to format.
•	format: The format string.
•	culture: The culture to use for formatting.
For versions prior to SQL Server 2012, the CONVERT function should be used.
________________________________________
Format Strings 📝
There are two types of format strings available:
1.	Standard Format String
2.	Custom Format String
________________________________________
Custom Format Strings 🎨
Custom format strings allow us to format the date and time using format specifiers. These can be combined in various ways to get the desired output.
Example:
sqlCopy code
DECLARE @dt DATETIME SET @dt = '2006-01-01 15:08:07' -- DD/MM/YYYY SELECT FORMAT(@dt, 'dd/MM/yyyy') -- Output: 01/01/2006 -- YYYY/MM/DD SELECT FORMAT(@dt, 'yyyy/MM/dd') -- Output: 2006/01/01 
________________________________________
Day, Month, and Year Formats 🗓️
Here are the format specifiers to format the day, month, and year:
•	Day Formats:
•	d: Day of the month (1 through 31).
•	dd: Day of the month (01 through 31). Single-digit day is formatted with a leading zero.
•	ddd: Abbreviated name of the day of the week (e.g., Fri).
•	dddd: Full name of the day of the week (e.g., Friday).
Example:
sqlCopy code
DECLARE @dt DATETIME SET @dt = '2020-5-6 12:28 PM' SELECT FORMAT(@dt, 'd/MM/yyyy') -- Output: 6/05/2020 SELECT FORMAT(@dt, 'dd/MM/yyyy') -- Output: 06/05/2020 SELECT FORMAT(@dt, 'ddd/MM/yyyy') -- Output: Wed/05/2020 SELECT FORMAT(@dt, 'dddd/MM/yyyy') -- Output: Wednesday/05/2020 SELECT FORMAT(@dt, 'ddddd/MM/yyyy') -- Output: Wednesday/05/2020 
________________________________________
Month Formats 📆
Month uses M as the format specifier. Remember, m stands for minutes.
Example:
sqlCopy code
DECLARE @dt DATETIME SET @dt = '2020-01-6 12:28 PM' SELECT FORMAT(@dt, 'dd/M/yyyy') -- Output: 06/1/2020 SELECT FORMAT(@dt, 'dd/MM/yyyy') -- Output: 06/01/2020 SELECT FORMAT(@dt, 'dd/MMM/yyyy') -- Output: 06/Jan/2020 SELECT FORMAT(@dt, 'dd/MMMM/yyyy') -- Output: 06/January/2020 
________________________________________
Year Formats 📅
Example:
sqlCopy code
DECLARE @dt DATETIME SET @dt = '2006-01-01' SELECT FORMAT(@dt, 'dd/MM/y') -- Output: 01/01/6 SELECT FORMAT(@dt, 'dd/MM/yy') -- Output: 01/01/06 SELECT FORMAT(@dt, 'dd/MM/yyy') -- Output: 01/01/2006 SELECT FORMAT(@dt, 'dd/MM/yyyy') -- Output: 01/01/2006 SELECT FORMAT(@dt, 'dd/MM/yyyyy') -- Output: 01/01/02006 
________________________________________
Time Format Strings ⏰
Here are the format specifiers to format the time:
•	h: Hour as a number from 1 through 12.
•	hh: Hour as a number from 01 through 12.
•	H: Hour as a number from 1 through 24.
•	HH: Hour as a number from 01 through 23.
•	m: Minute as a number from 0 through 59.
•	mm: Minute as a number from 00 through 59.
•	s: Second as a number from 0 through 59.
•	ss: Second as a number from 00 through 59.
•	t: Represents the first character of the AM/PM.
•	tt: Represents both characters of the AM/PM.
•	z: Represents the signed offset time from the UTC.
•	zz: Represents the signed offset time from the UTC.
•	zzz: Represents the signed offset time from the UTC.
Examples:
 
 
Other Format Strings 🎛️
Additional format specifiers include:
•	f to fffffff: Represents tenths of a second.
•	F to FFFFFFF: Represents tenths of a second. Nothing is displayed if the digit is zero.
•	:: Represents the time separator.
•	/: Represents the date separator.
•	"string": Literal string delimiter.
•	%: Defines the following character as a custom format specifier.
•	\: The escape character.
•	Any other character: The character is copied to the result string unchanged.
Standard Date & Time Formats 📅⏰
Standard date and time format strings use a single character as the format specifier. For example, the d format specifier displays the date in the short date pattern.
Example:
DECLARE @dt DATETIME
SET @dt = '2006-01-01 15:08:07'

SELECT FORMAT(@dt, 'd')
-- Output: 1/1/2006

SELECT FORMAT(@dt, 'D')
-- Output: Sunday, January 1, 2006

SELECT FORMAT(@dt, 'f')
-- Output: Sunday, January 1, 2006 3:08 PM

SELECT FORMAT(@dt, 'F')
-- Output: Sunday, January 1, 2006 3:08:07 PM

SELECT FORMAT(@dt, 'g')
-- Output: 1/1/2006 3:08 PM

SELECT FORMAT(@dt, 'G')
-- Output: 1/1/2006 3:08:07 PM

SELECT FORMAT(@dt, 'M')
-- Output: January 1

SELECT FORMAT(@dt, 'm')
-- Output: January 1

SELECT FORMAT(@dt, 'O')
-- Output: 2006-01-01T15:08:07.0000000

SELECT FORMAT(@dt, 'o')
-- Output: 2006-01-01T15:08:07.0000000

SELECT FORMAT(@dt, 'R')
-- Output: Sun, 01 Jan 2006 15:08:07 GMT

SELECT FORMAT(@dt, 'r')
-- Output: Sun, 01 Jan 2006 15:08:07 GMT

SELECT FORMAT(@dt, 's')
-- Output: 2006-01-01T15:08:07

SELECT FORMAT(@dt, 't')
-- Output: 3:08 PM

SELECT FORMAT(@dt, 'T')
-- Output: 3:08:07 PM

SELECT FORMAT(@dt, 'u')
-- Output: 2006-01-01 15:08:07Z

SELECT FORMAT(@dt, 'Y')
-- Output: January 2006

SELECT FORMAT(@dt, 'y')
-- Output: January 2006
Changing the Language 🌐
You can change the language used for formatting in two ways:
1.	Use the culture parameter in the FORMAT function.
2.	Use the SET LANGUAGE TSQL command.
Example:
 
List of Supported Languages 🌐
To find out the list of supported languages, use the following query:
SELECT * FROM sys.syslanguages










DateTime2 Vs DateTime 📅⏰
Introduction 📝
Both DateTime and DateTime2 are data types in SQL Server designed to store date and time values. Introduced in SQL 2008, DateTime2 offers improved precision and flexibility compared to the traditional DateTime. Let's dive into the differences between these two popular data types.
________________________________________
Syntax 🖋️
•	DateTime2:
datetime2(n)
Where n is the fractional seconds precision.
Example:
DECLARE @MyDatetime2 datetime2(3) 
•	DateTime:
datetime
Example:
DECLARE @MyDatetime datetime 
________________________________________
ANSI SQL Compliance 🌐
•	DateTime2:
Compliant with SQL Standards and ISO 8601.
•	DateTime:
Not ANSI SQL Compliant.
Format 📜
•	DateTime2:
YYYY-MM-DD hh:mm:ss.nnnnnnn
•	DateTime:
YYYY-MM-DD hh:mm:ss.nnn
Date Range 📅
•	DateTime2:
0001-01-01 to 9999-12-31
•	DateTime:
1753-01-01 to 9999-01-01
________________________________________
Time Range ⏰
•	DateTime2:
00:00:00 through 23:59:59.9999999
•	DateTime:
00:00:00 through 23:59:59.997
________________________________________
Accuracy & Precision 🎯
•	DateTime2:
Up to .0000001 seconds (100 nanoseconds).
•	DateTime:
Rounded to increments of .000, .003, or .007 seconds.
________________________________________
User-Defined Precision 📐
•	DateTime2:
Allows user-defined fractional seconds precision.
•	DateTime:
Fixed precision.
________________________________________
Storage 💾
•	DateTime2:
•	n <= 2: 6 Bytes
•	n = 3 or n = 4: 7 Bytes
•	n >= 5: 8 Bytes
Example:
 
•	Result: 0x078029676967F8410B
•	DateTime:
Fixed 8 Bytes for all values.
Example:
 
•	Result: 0x0000AC9D00CB50D4
________________________________________
Implicit Conversion 🔄
SQL Server performs implicit data type conversions during expression evaluation. However, there are notable differences between DateTime and DateTime2.
Example:
 
Storage Mechanism 🧠
Both data types use integers to store date and time:
•	Date Integer: Days since the base date.
DateTime: Base date is 1900-01-01.
DateTime2: Base date is 0001-01-01.
•	Time Integer: Clock ticks since midnight.
DateTime: Each tick is 1/10000000 of a second.
DateTime2: Each tick is 1/300 of a second.
________________________________________
Additional Points 📌
•	Precision:
•	DateTime2: 1/10000000 of a second.
•	DateTime: 1/300 of a second.
•	User Specified Precision:
•	DateTime2: You can specify fractional seconds precision. DateTime2(3) is equivalent to DateTime.
•	ISO Compliance:
•	DateTime2: Adheres to SQL Standards and ISO 8601.







Bit & Boolean Data Types in SQL Server 📊
________________________________________
Bit Data Type 🧮
•	Description:
The SQL Server bit data type is a 1-bit numeric data type, which is commonly used as a Boolean data type in SQL Server. It can store three values: 0, 1, or NULL. In the context of Boolean, 0 is considered as false and 1 as true.
•	Storage Optimization 💾:
•	A single bit column requires only 1 bit of storage.
•	However, in SQL Server, a byte consists of 8 bits.
•	To optimize storage, SQL Server combines multiple bit columns into a single byte.
•	If there are 8 or fewer bit columns in a table, they are combined into 1 byte.
•	If there are 9 to 16 bit columns, they are combined into 2 bytes.

Boolean Data Type ✅❌
•	Description:
SQL Server does not have a separate Boolean data type. Instead, the bit data type is used to represent Boolean values.
•	1 is treated as true
•	0 is treated as false


Examples and Queries 📝
•	Creating a Table with Bit/Boolean Column 🛠
 
•	Inserting Values into a Bit/Boolean Column ➕

  
 
Converting String Values to Bit 🔀
 
•	Note:
•	The string values 'TRUE' and 'FALSE' are converted to 1 and 0 respectively.
•	Any other string value conversion results in an error.
•	Converting Bit Column to Integer ➗
 
Key Points 📍
1.	bit data type is a numerical type in SQL Server.
2.	The bit data type is used to represent Boolean values where 1 is true and 0 is false.
3.	SQL Server optimizes the storage of bit columns by merging them into bytes.
4.	When inserting values, SQL Server allows direct insertion of integers 0 and 1 for bit columns.
5.	Conversion of string values like 'TRUE' and 'FALSE' to bit results in 1 and 0 respectively.
6.	Converting a bit column to an integer allows mathematical operations on it after type conversion.









SQL Server Binary and VarBinary Data Types 📊
________________________________________
Overview 📌
Binary and Varbinary data types in SQL Server are used to store raw binary data. These data types are suitable for storing contents of image files (like BMP, TIFF, GIF, or JPEG), word documents, and other binary data.
________________________________________
Binary Data Types 📜
________________________________________
1. Binary (Binary) 🔒
•	Description:
Binary is a fixed-width data type.
•	Syntax:
binary(n)
Here, n defines the size in bytes (1 to 8000 bytes). And not number of characters
•	Storage:
The Binary data type always uses n bytes of storage, regardless of the actual data size.
•	Example:
 
•	In this example, the column will occupy 10 bytes of storage.
________________________________________
2. Varbinary (Varbinary) 📦
•	Description:
Varbinary is a variable-width data type.
•	Syntax:
varbinary(n)
Here, n defines the maximum size in bytes.
•	Storage:
Varbinary data type uses the actual length of the data entered + 2 bytes as the storage.
•	Example:
 
3. Varbinary(Max) (Varbinary(Max)) 📦
•	Description:
Varbinary(max) is used when the length of the binary data is expected to exceed 8000 bytes.
•	Example:
 
🚫 Important Note 🚫
The ntext, text, and image data types will be deprecated in future versions of SQL Server. It is recommended to use nvarchar(max), varchar(max), and varbinary(max) instead.
________________________________________
Examples of Binary Data Type 📝
________________________________________
Creating Tables with Binary Columns:
 
 
Inserting Values into Binary Columns:
 
Using Binary Local Variables:
 
Converting to and from Binary 🔄
________________________________________
Binary to String:
Conversion from binary to string is implicit.
 


String to Binary:
Implicit conversion from string to binary is not allowed. Use the CAST or CONVERT function.

DECLARE @bin VARBINARY(MAX) = CAST('Hello World' AS VARBINARY(MAX)) 
________________________________________
🛠 Conversion Examples:
String to Binary:
 
Binary to String:
 
Which Binary Type to Choose? 🤔
Choose the appropriate binary data type based on your data needs:
•	binary: For consistent column data entries sizes.
•	varbinary: For varying column data entries sizes.
•	varbinary(max): When column data entries exceed 8,000 bytes.
________________________________________
🔥 Tip for Interviews:
Always be cautious about silent padding & truncation when converting data from one type to binary and vice versa.





📣 Stay Updated!
For more insightful content, tutorials, and tips on SQL and database management, subscribe to my YouTube channel @coderbaba. Your support helps in creating more valuable content for the community! 🙌👨‍💻
 
