---
layout: post
title: هەڵبژاردنی بنکەدراوەی MySQL
tags: [mysql]
date : "2018-08-09 05:35:45"
---

### پێشەکی

تا ئێستا ئێمە بە دروستکردن،سڕینەوەی بنکە دراوە لە MYSQL ئاشنا بووین. ئێستا گەر چەندین بنکەدراوە لە MYSQL دروست بکەین دەبێ بۆ سڕینەوە یان دەستکاریان سەرەتا بنکەدراوە هەڵبژێرین.MYSQL فەرمان و نەخشەی پێویست بۆ هەڵبژاردنی هەر یەک لە بنکەدراوەکان، بۆ دەستکاری هەیە.ئەڵبەت هەر بنکەدراوە ناوێکی هەیە کە بۆ دەستپێگەیشتن سوودی لێدەگرین.

### هەڵبژاردنی بنکەدراوەی MYSQL بە هێڵی فەرمان

کاتیک کە لە گەڵ ڕاژەیMYSQL پەیوەندی دەگرین، پێویستە کە بنکەدراوەییک هەڵبژێرین. بە هێڵی فەرمان بە ئاسانی پاش فەرمانی <mysql ئەم ئیشە جێبەجێ دەبێ. بۆ هەڵبژاردنی بنکەدراوە لە فەرمانی **use** دەگرین.
**نمونە:**
ئەمە وێنەیێکی سادە بۆ هەڵبژاردنی بنکە دراوەیێک بەناوی kurdish ــە.

```sql
[root@host]# mysql -u root -p
Enter password:******
mysql> use KURDISH;
Database changed
mysql>
```

لە فەرمانەکەی سەرەوە بنکەدراوەی KURDISH بژاردە کراوە. خاڵ
تەواوی ناوەکانی بنکەدراوە، خشتەکان، ناوی فیلدەکان هەستیار بە گەورەیی و بچکۆلەیی پیتەکانن.بۆیە ئێوە دەبێ لەکاتی ئیش بە فەرمانەکان SQL ، لە ناوی گونجاو سوود بگرن.



### هەڵبژاردنی بنکەدراوەی MYSQL بە یارمەتی زمانی PHP

زمانی PHP نەخشەیێکی هەیە بە ناوی mysql_select_db بۆ هەڵبژاردنی بنکە دراوەیێک.
کاتێک بە سەرکەوتووانە بنکەدراوەی هەڵبژارد TRUE و بە پێچەوانە FALSE دەگەرێنێتەوە.

```sql
bool mysql_select_db( db_name, connection );
```



| ڕیز  |  پارەمەتر  |                            شڕۆڤە                             |
| :--: | :--------: | :----------------------------------------------------------: |
|  ١   |  db_name   |         پێویستە :ناوی بنکەدراوەی MYSQL هەڵدەبژێرێت.          |
|  ٢   | connection | دڵخوازە : گەر دابین نەکرابێت ،دوایین پەیوەندی کراوەی mysql_connect دەخاتە بەردەست. |

**نمونە**
ئەم وێنە چۆنیەتی هەڵبژاردنی بنکەدراوەیێک نیشان دەدا:

```sql
<html>
   <head>
      <title>Selecting MySQL Database</title>
   </head>
    
   <body>
      <?php
         $dbhost = 'localhost:3036';
         $dbuser = 'qezwan';
         $dbpass = 'qezwan123';
         $conn = mysql_connect($dbhost, $dbuser, $dbpass);
          
         if(! $conn ) {
            die('Could not connect: ' . mysql_error());
         }
         echo 'Connected successfully';
         mysql_select_db( 'KURDISH ' );
          
         mysql_close($conn);
      ?>
   </body>
</html>
```

**کورتەی باس :**
ئێوە گەر لە سیستمەی بەرێوەبردنی MYSQL سوود بگرن بۆ پاشکەوت و بەرێوەبردنی دراوەکان، پێش دێت کە زۆرتر لە دانەیێک بنکەدراوەتان هەیە.هەر بۆیە ئیشکردن لە سەر بنکە دراوەکان دەبێ سەرەتا هەڵیبژێرن، کە لەم وانە خوێندمان.