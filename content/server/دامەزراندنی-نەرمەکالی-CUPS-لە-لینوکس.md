---
layout: post
title: دامەزراندنی نەرمەکالی CUPS لە لینوکس
tags: [ڕاژە]
date : "2017-03-14 05:35:45"
---

##### پێشەکی

CUPS کورتکراوەی Common UNIX Printing System کە لە سیستەمەکانی هاوشێوەی یونیکس(ماک ، لینوکس و BSD) بۆ پرینتکردن سوودی لێوەردەگرن.زۆرتری دابەشکراوەکانی گنو/لینوکس بە شێوازی پێشگریمان ئەم نەرمەکالایان بۆ چاپکردنی دۆکیومینتەکان لەسەرە .بەڵام کاتێک کار لە سەر سێرڤێر دەکەن یان لە شوێنێک کە ئەم نەرمەکالا لە سەر دابەشکراوەکەتان نەبێت، دەتوانن بە خوێندنەوەی ئەم بابەتە ئەم نەرمەکالا دامەزرێنن.

##### دامەزراندن

بۆ دامەزراندن CUPS سەرەتا دەبێت دڵنیا بن کە پەیوەندیتان هەیە بە ئینتەرنێتەوە ئینجا لە دابەشکراوەی ئوبونتو ئەم فەرمانە بنووسن :

```shell
sudo apt-get install cups $
```

پاش دامەزراندنی CUPS، ئێستا دەبێت نەرمەکالاکە وەگرخەین و بەرێوەی ببەین  و لەترمیناڵ ئەم فەرمانە دەنووسین :

```shell
sudo /etc/init.d/cups start $
```

بۆ Restart کردنی نەرمەکالا دەبێت لەم فەرمانە سوود بگرین:

```shell
sudo /etc/init.d/cups restart $
```

بۆ ئەوە کە بزانین نەرمەکالاکە بە باشی ئیش دەکات دەبێت ئەم فەرمانە بنووسین :

```shell
sudo /etc/init.d/cups status $
```

بۆ وێستاننی نەرمەکالا دەبێت لەم فەرمانە سوود بگرین :

```shell
sudo /etc/init.d/cups stop $
```

کاتێک گەرەکتانە نەرمەکالا لە کاتی بووت بوونی سیستەمەکەتان بێتە سەر لەم فەرمانە سوود بگرن :

```shell
sudo update-rc.d cups enable $
```

کاتێک گەرەکتانە کە لە کاتی بووت کردنی سیستەمەکەتان، چاپکەر نەکەوێتە کار دەبێت ئەم فەرمانە بنووسن لە ترمیناڵ‌:

```shell
 sudo update-rc.d cups disable $
```

زۆر یەک لە دابەشکراوەکانی گنو/لینوکس بە شێوازی گرافیکی و پێشگریمان وێنۆ چکەیێک(Icon) لە بەشی رێکخستنەکانی سیستەم هەیە کە توانایی بەرێوەبردنی پرینتێر/پرینتیرەکانیان بۆ دابینکراوە. بۆ ئەم مەبەستە دەتوانن
بڕۆنە بەشی System Settings  ئینجا لە سەر دوکمەی Printer کرتە بکەن. بۆ وێنە لە گنو/لینوکسی ئێلێمێنتری بەم شێوازەیە :

![](/server/images/03.jpg)