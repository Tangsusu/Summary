#### 说明：记录SQL学习过程中的难点以及注意点，格式：以四级标题指明类别，
#### SQL UPDATE
执行没有WHERE字句的UPDATE要慎重，再慎重。
#### SQL DELETE
可以在不删除表的情况下，删除表中所有的行。可以保持表的结构、属性、索引不变。`DELETE FROM table_name / DELETE * FROM table_name`
#### SQL 通配符

- %和_都用LIKE，REGEXP或NOT REGEXP运算符来操作正则表达式（有疑问）<br>
正则表达式<br>
.匹配除\n之外的任意单个字符<br>
^匹配字符串开始的位置<br>
$匹配字符串结束的位置<br>
OR匹配多个串`SELECT * FROM products WHERE pro_id REGEXP '1000|2000'`<br>
- 特殊例子：`SELECT * FROM Websites WHERE name REGEXP '^[^A-H]'`<br>
#### SQL别名
特殊例子：`SELECT name,CONCAT(url,',',alexa,',',country) AS site_info FROM Websites;`
#### SQL INNER JOIN
把两张表中有相同字段数据的记录组合起来
#### SQL LEFT JOIN
LEFT JOIN 关键字从左表（table1）返回所有的行，即使右表（table2）中没有匹配。如果右表中没有匹配，则结果为NULL。

