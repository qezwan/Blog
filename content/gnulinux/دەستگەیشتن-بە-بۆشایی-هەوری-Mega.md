---
layout: post
title: دەستگەیشتن بە بۆشایی هەوری Mega
tags: [گنو/لینوکس]
date : "2018-08-25 05:20:45"
socialshare: true
---

##### پێشەکی :

مێگا بۆشایێکی هەورییە کە ڕیتان پێدەدا فایلەکانتان لە سەر کۆمپیوتر،تەلەفۆنی هۆشمەند،ڕاژە و …هتد،لە نێویا پاشکەوت بکەن.قەبارەی پاشکەوتکردن [هەم بە پارەیە](https://mega.nz/pro) هەم بە لاشە(ئێوە بۆ دێسکتۆپ ۲۰ گیگتان پێ دەبخشرێت). ئەڵبەت ئێوە دەتوانن لە گوگڵ درایڤ،وان درایڤی مایکرۆسۆفت،درۆپ بۆکس و…هتد سوود بگرن، بەڵام پێشنیاری ئێمە مێگایە .

![](/gnulinux/images/00007-1.png)



ەشوێن ئەوەن کە چۆن بە ئاسانی پەڕەکانتان پاشکەوت بکەنە نێو بۆشایی هەوری مێگا،باش وایە کە ئەم بابەتە بخوێنن.هەوڵدەدەین فێرکاریێک لە سەر لکاندنی درایڤ(بۆشایی هەوری)ـەکەتان لە مێگا ،لەگەڵ سیستەمی کارپێکردنی گنو/لینوکسەکەتان، پێ فێر بکەین.لێرە چەند شێواز بەکار دەبەین.
هاوکاتگه‌ری(Sync) مێگا بۆ ڕاژەخوازی ڕوومێزی(Desktop Client)
بە دڵنیایەوە مێگا بە تەواوی پاڵپشتی لە ڕاژەخوازی ڕوومێزی گنو/لینوکس دەکا.بە[ سەردانی ئەم پەڕە ](https://mega.nz/sync)و هەڵبژاردنی گنو/لینوکسی دامەزراوە لە سەر کۆمپیەترەکەتان دەتوانن نەرمەکالای هاوکاتگەری مێگا لە سەر کۆمپیوترەکەتان دامەزرێنن.ئەڵبەت هەواڵێکی خۆشیش ئەوەیە کە بۆ دوو جۆری ئەندازیاری کۆمپیوتریش واتە ۳۲بیت و ۶۴بیت وشێندراوە.لە زۆربەی دابەشکراوەکان گنو/لینوکس پاڵپشتی دەکا وەکوUbuntu, Linux Mint, ElementaryOS, Debian, Fedora SUSE, تەنانەت Arch Linux.

###### ئوبونتو

دامەزراندنی ڕاژەخوازی هاوکاتەگەری Mega زۆر سادەیە لە سەر ئوبونتو.[سەرەتا بچنە پەڕەی داگرتنی](https://mega.nz/sync)، ئینجا گنو/لینوکسی ئوبونتو بە پێی وشانی سیستەمەکەتان هەڵبژێرن جا فایلی دێبەکەی(deb.) داگرن.من بۆ ئێلێمێنتری لوکی ۶۴گیگ دامەزراند.
![](/gnulinux/images/00007-2.png)
بۆ وشانی کۆنەی ئوبونتوو، لە ۱۲.۰۴ تا دوایین وشانی واتە ۱۸.۰۴ پاڵپشتی دەکا، ئەمەش خاڵێکی بەهێزە.پاش داگرتنی پەڕەکەی دوو کرتەی لەسەر بکەن تاکوو ناوەندی نەرمەکالای ئوبونتو دەکرێتەوە و دایمەزرێنن.گەر کێشەیێک بوو لەمە دەتوانن بە شێوازی دەستی دایمەزرێنن بەم جۆرە لە ڕێگای ترمیناڵ:

```shell
cd ~/Downloads

sudo dpkg -i megasync-*.deb
sudo apt install -f
```

###### دێبیان :

دامەزراندنی ڕاژەخوازی هاوکاتەگەری Mega ، لە دێبیان زۆر سادەو بە باشی دەچیتە پێشەوە.مێگا لە وشانی ۷، ۸ و ۹ پاڵپشتی دەکا.ئەو پەڕەکە داتناگرتوە، دوو کرتەی لەسەر بکەن تا بەرنامەی Gdebi بکرێتەوە بۆ هاوئاهەنگی و دامەزراندن.
گەر ناتوانن یان کێشەیێک هەیە ئەوە بەم فەرمانە لە ترمیناڵ دایمەزرێنن :

```shell
cd ~/Downloads

sudo dpkg -i megasync-*.deb

sudo apt-get install -f
```

###### ئاچ(Arch) لینوکس

بە فەرمی پاڵپشتی لە مێگا دەکا بەڵام بە جیاتی ئەوە ئاماژە بە AUR بکا بە درووستکردنی پاکەتی دامەزراندن بەکارهێنەر ڕێنمایی دەکا.بەکارهێنەرانی ئاچ دەتوانن پاکەتی Pacman دابگرن و دایمەزرێنن.بەڵام لەبیرتان بێتەوە بەو شێوە کە ئاچ لینوکس دیزاین کراوە ،هەر کات کە گەرەکتان بێ Mega Sync بەرز بکەنەوە دەبێ وشانێکی نوێ مێگای لە ماڵپەڕی فەرمی دابگرن.
بچن بۆ [پەڕەی فەرمی داگرتنی مێگا](https://mega.nz/sync) ئینجا ئاچ دابگرن.ئینجا بە فەرمانی `CD `بچنە نێو بوخچە یان مەسیری` Downloads/~ `بەم شێوازە :

```shell
cd ~/Downloads
```

ئێستا ئێوە لە نێو بوخچەی Downloads دان، دەبێ بە یارمەتی پاکەتی pacman دایمەزرێنن:

```shell
sudo pacman -U megasync-x86_64.pkg.tar.xz
```

بەنابە زاتی Arch Linux ، دەبێ تەواو پەڕەکانی پێداویستی بۆ مێگا دامەزرێ.بۆ ئاسایش، دوواینی بەڕۆژ بوونەوەوەی مێگا ئەنجام بدەن و دەبێ دڵنیا بن کە بەرنامە لە باشترین حاڵەت جێبەجێدەکرێت :

```shell
sudo pacman -Syyuu
```

پاش بەڕۆژ بوونەوە مێگا ئامادەیە ببۆ ئیش پێکردن.

###### فێدۆرا

مێگا بە پاکەتی RPM بۆ زۆربەی دابەشکراوەکانی فێدۆرا بوونی هەیە. لە دوو وشانی کۆنەو نوێ واتە لە وشانی ۱۹ تا ۲۰ . سەرەتا بڕۆن بۆ [پەڕەی داگرتنی مێگا](https://mega.nz/sync) ئینجا وشانی داخوازی خۆتان بە پێی سیستەمی کارگێڕیەکەتان داگرن.کاتێک پاکەتی میگاتان داگرت بەم فەرمانە بکەن ؛

```shell
cd ~/Downloads

sudo dnf install -y megasync-Fedora_28.x86_64.rpm
```

ئاگات لە ژمارەو وشانی پاکەتی مێگا بێی .شایەت ئەوەی جەنابت جیاواز بێ لەمە.

###### ئۆپێن سووسە(OpenSUSE) :

بە سادەیی[ بچن بۆ پەڕەی داگرتن](https://mega.nz/sync) لە ماڵپەڕی مێگا،وشانی ئۆپن سووسە بە پێی کۆمپیوترەکەتان هەڵبژێرن.بچنە نێو بوخچە یان مەسیری` Downloads/~ `بەم شێوازە :

```shell
cd ~/Downloads
```

##### بە یارمەتی Zypper دایمەزرێنن :

 

```shell
sudo zypper install megasync-openSUSE_*.rpm
```

##### ڕێکخستنی مێگا :

پاش داگرتنی مێگا و دامەزراندنی لە گنو/لینوکسەکەت. دەبێ کرتەی لە سەر فایلی دامەزراندن بکەن تا میگا لە پەنجێرەیێک دەکرێتەوە.زانیاری هەژمارەکەتانی تێدا بنووسن، ئێستا بە شێوازی خۆماڵی نەرمەکالای مێگا هاوکاتەگەری (Sync) ئەنجام دەدا.
لە ڕێگای هێڵێ فەرمان لە ترمیناڵ بەم جۆرە چالاک دەبێ :

```shell
cd ~/MEGA
```

 ![](/gnulinux/images/00007-3.png)