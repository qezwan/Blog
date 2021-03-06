---
layout: post
title: دامەزراندنی ڕاژەیێکی بچووک بە CentOS 7.3
tags: [ڕاژە]
date : "2017-02-24 05:35:45"
---

##### پێشەکی:

لەم فێرکارییە بە دامەزراندنی ڕاژەیێک بە کەمترین ئیمکانات ، ئاشنا دەبین. دابەشکراوەیێک کە ئەم ڕاژەمان لەسەری رێکخستووە CentOS 7.3ـە.ئەم فێرکارییە هەنگاوێکە بۆ قۆناغەکانی داهاتوو لە دامەزراندنی راژە یان سێرڤێرێکی تەواو کە SAMBA, LAMP وە LEMP لەسەر دامەزراوە.

##### پێداویستی :

بۆ دامەزراندنی ڕاژەی CentOS 7.3 نیازمان بە فایلی ئەم سیستەمی کارپێکردنەوە .بۆ ئەم مەبەستە پێشنیار دەکەین کە سوود لە فایلی ISO بگرن.کاتێک کە ئەم فایلەتان داگرت دەتوانن لەسەر فلاش یان DVD بیسووتینن بەو مەرجە کە توانایی بووتی بێت. سەرەتا فایلیISO دادەگرین لەم بەستەرە .

ئێمە لێرە لە سەر ماشینێکی خەیاڵی قۆناغەکانی دامەزراندن ئەنجام دەدەین ،هیچ جیاوازی لەگەڵ کۆمپیوترێکی ڕاستەقینە بۆ دامەزراندنی ئەم سێرڤێرەنییە.

**خاڵ :**

وشانی سێرڤێر لەم فێرکارییە CentOS 7.3ـیە، هەروا من لەم ئای پی ئادرێسە 192.168.1.100 وە ناوی ڕاژەی server1.example.com ،بۆ ئەم فێرکارییە سوود دەگرم.ئێوە دەتوانن بە حەزی خۆتان و بەڕجاوگرتنی ستانداردەکان ئەم ناوانە بگۆڕن.

##### دامەزراندن

فایلی CentOS 7.3 کە لەسەر DVD یان فلاش سووتانتانە بووتی(Boot) بکەن. ئینجا ڕەستەی Install CentOS 7 هەڵبژێرن(وەک وێنەی خوارەوە).

![](/server/images/02-1.png)

پاش هەڵبژاردن دوکمەی ENTER لێبدەن.

![](/server/images/02-2.png)

ئێستا زمانی ئینگلیزی هەڵبژێرن یان هەر زمانێک کە پێتان خۆشە ،لێرە پێشنیار زمانی ئینگلیزی وەڵاتی ئەمریکایە واتەEnglish United States . ئینجا لەسەر دوکمەی Continue کرتە بکە.

![](/server/images/02-3.png)

ئازیزان پەڕەیێک وەک وێنەی خوارەوە دەردەکەوێت کە دەبێت ریکخستنەکانی خۆماڵی وەک DATE & TIME وە KEYBOARD دیاربکەین.

![](/server/images/02-4.png)

من لەسەردێری LOCALIZATION(بەخۆماڵیکردن) سەرەتا کات و بەروار رێکدەخەم.بۆ ئەم مەبەستە لەسەر DATE & TIME کرتەیێک دەکەم و کاتی شوێنەکەم هەڵدەبژێرم.

![](/server/images/02-5.png)

من لێرە Europe وەک مەنتەقە و شاریش Berlin بەڵدەبژێرم (کات بەم شوێنە خۆی بۆ سێرڤێرەکەم رێکدەخات).ئینجا لەسەر دوکمەی Done کرتە دەکەم.

پاش ریکخستنی کات/برواری شوینی سیرڤێر، ئێمە دەبێت زمانی تەختەکلیلەکەمان(KEYBOARD) هەڵبژێرین

![](/server/images/02-6.png)

لێرە زمانی ئینگیزی بە شێوازی پێشگریمان هەر هەڵمانژارد بەڵام دەبێ زمانی کوردیشی پێ زیاد بکەین بۆ ئەم کارە لەسەر وێنۆچکەی + کرتە دەکەین .

![](/server/images/02-7.png)

لێرە لیستێک لەو تەختەکلیلانە کە بوونیان هەیە بۆ نووسین بە زمانە جیاوازەکان دەردەکەون کە منGerman هەڵدەبژێرم. ئینجا لەسەر دوکمەی Add کرتە دەکەم.

![](/server/images/02-8.png)

لەم پەنجێرە کارێکی دیکەمان دەمێنێت کە دەبێت لە بەشی LAYOUT SWITCHING OPTIONS لەسەر دوکمەی Optionsکرتەیێک بکەین بۆ ئەوە شێوازی گۆڕینی تەختەکلیل دیاری بکەین.

![](/server/images/02-9.png)

هەڵبەژاردە یان کورتەکلیلی زۆرمان هەس بۆ گۆڕینی زمانی تەختەکلیلەکان بەڵام من Alt+Ctrl هەڵدەبژێرم و ئینجا لەسەر دوکمەی Done کرتە دەکەم.

![](/server/images/02-10.png)

ئێستا لەسەر دۆکمەیDone کرتە دەکەم تا دەچمە پەڕەی سەرەتایی.

![](/server/images/02-11.png)

ئیستا بەشی LANGUAGE SUPPORT ماوە کە زمانێکی دیکەی پێ زیاد بکەم.کوردە حەیاتەکە بەداخەوە هەر هیچی لێبەرنایێت تەنانەت وۆردپرێس و درۆپاڵی پاش 15 ساڵ هێشتا بە ناقسی کردوە بە کوردی جا چ بگەیێ بەم سیستەمی کارپێکردنە.بەهەر حاڵ گەر پێت خۆشە سێرڤێرەکەت بە زمانێکی دیکە بێت ئەوە باشە لەم بەشە وەک تەختە کلیلەکەت زمانێکی دیکەی بۆ هەڵبژێریت با سیستەمەکەت بێتە سەر ئەو زمانە.

![](/server/images/02-12.png)

بە شێوازی پێسگریان زمانی ئینگلیزی هەڵبژێردراوە بەڵام من زمانی Deutsch German پێ زیاد دەکم بەم جۆرە:

![](/server/images/02-13.png)

ئێستا لە پەڕەی کانفیگ بچنە بەشی SOFTWARE > INSTALLATION SOURCE 

![](/server/images/02-14.png)

لەم بەشەسەرچاوەی دامەزراندنەکە دیار دەکەن.واتە بە شێوازی پێشگریمان “Auto-detected installation media” هەڵبژێردراوە ،گەر ەنابەت سەرچاوەییک دیکەت هەیە وەک ڕایەڵە یان تۆڕ ئەتوانی ئەم ڕەستە “On the network” هەڵبژێریت و گەر پێویستیبە پراکسی بوو بۆی رێکبخە لە بەشیProxy Setup . هەر با پێشگریمان بمێنێت ئینجا لەسەر دوکمەی Done کرتە بکە.

![](/server/images/02-15.png)

لە بەشی SOFTWARE SELECTION بە شێوازی پێشگریمان لەسەر Minimal Installسازکراوە.

![](/server/images/02-16.png)

لێرە ئێوە دەتوانن پاکەتی خزمەتگوزاری فرەتر لەسەر ئەم سێرڤەرە زیاد بکەن بەڵام چونکە ئێمە بە شێوازی ڕاژەی بچووک خەریکین دامەزراندن دەکەین ئەم خزمەتگوزارییانە لەبەردەست نییە خۆمان دەتوانین لە دوایی دامەزراندن زیادی بکەین.بەڵام بە شێوازی داگرتنی فایل بە تواوی لە ستونی ڕاست خزمەتگوزاریەکانی دیکە بۆ هەڵبژاردن دەردەکەون.بس ئێمە لەم دامەزراندنە پێویستمان بە (Minimal Install(Basic Functionality هەیە و لەسەر دوکمەی Done کرتە بکە.

![](/server/images/02-17.png)

دەچینە پەڕەی سەرەتا وە ئێمە دەچینی بەشی SYSTEM و INSTALLATION DESTINATION هەڵدەبژێرین.

![](/server/images/02-18.png)

لێرە دەتوانیت هاردەکەت پارتیشێن بکەی کە من پێم باشە هەروا بمێنێتەوە.ئەمە شتیکی سەلیقەییە.لەسەر دوکمەی Done کرتە بکە.

![](/server/images/02-19.png)

ئێستا دەبێت لە بەشی NETWORK & HOSTNAME ڕایەڵەکەمان کانفیگ بکەین.

![](/server/images/02-20.png)

ناوی هاستەکەی من server1.example.com و بە شێوازی ئێتێرنێت(ethernet) سوود لە پەیوەندی تۆڕ دەگرم بۆ رێکخستنی لەسەر دوکمەی Configure کرتە دەکەم.

![](/server/images/02-21.png)

لە سەرخشتی IPv4 ریکخستنەکان ئەنجام دەدەم گەر لە IPv6 سوود دەبینن دەتوانن لەو سەرخشتە دەستکاری بکەن.

![](/server/images/02-22.png)

لە سەر خشتی IPv4 ئێوە Manual هەڵبژێرن.

![](/server/images/02-23.png)

پاشان دەبێ زانیاریەکانی IP, Netmask وە Gateway پێبدەن. من لە IPبە 192.168.1.100 وە Netmaskبە 255.255.255.0، Gateway بە 192.168.1.1 ریکدەخەم. هەروا DNS serversـیش بەم ئادرەسەیە 8.8.8.8 8.8.4.4 ئینجا پاش تەواو بوون لەسەر دوکمەی Save کرتە بکەن.

![](/server/images/02-24.png)

**خاڵ :** گەر لە IPv6 سوود نابینن دەبێ لەو سەرخشتە لەبەشی Methode هەڵبژاردەی ignoreهەڵبژێرن.هەروا گەر لە IPv6 سوود دەگرن دەبێ بۆ IPv4ئەم کارە بکەن.

![](/server/images/02-25.png)

ئێستا وەک وێنەی خوارەوە جۆری پەیوەندیەکەت ON بکە واتە چالاکی بکە. ئینجا لەسەر دوکمەی Done کرتە بکە.

![](/server/images/02-26.png)

ئێستا لە پەڕەی سەرەتاوە لەسەر دوکمەی Begin Installation کرتە بکە.

![](/server/images/02-27.png)

ئێستا ئێوە شریتێکی شین دەبینن کەلە خوارەوە کە خەریکە پرۆسەی دامەزراندن نیشاندەدا.لێرە ئێمە دووکار دەبێ بکەین.یەکەم بۆ بەڕێوەبەری گشتی(ROOT) وشەی نهێنی دابین بکەین و ناوی بەکارهێنەرێکیش(USER CREATION ) تۆمار بکەین.سەرەتا بەڕێوبەری گشتی واتە ڕووت :

![](/server/images/02-28.png)

وشەی نهێنیێکی بەهێز هەڵبژێرەو لە سەر دوکمەی Done کرتە بکە.

![](/server/images/02-29.png)

ئێستا بەکارهێنەرێکی نوێ تۆمار دەکەین واتە USER CREATION:

![](/server/images/02-30.png)

من بەکارهێنەرێک کە بەڕێوەبەر نیە تۆمار دەکەم, ناوی تەواوی من “Howtoforge” وە ناوی بەکارهێنەرەکەم “howtoforge”, ئێستا وشەیێکی نهینی بەهێزیشی بۆ دابین دەکەم و لە سەر دوکمەی Done کرتە دەکم. تاکوو دامەزراندن قۆناغەکانی تەواو بێت.

![](/server/images/02-31.png)

پاش تەواو بوونی دامەزراندن داوای ریستارتت لێدەکات.

![](/server/images/02-32.png)

پاش ریستارت بوونەوە داوای ناوی بەکارهێنەر و وشەی نهێنیت لێدەکات.

![](/server/images/02-33.png)

یەکەم بار بۆ چوونەژوورەوە :

کاتێک بە عینوانی بەکارهێنەری root دەچنە ژوور دەبێت چەند کار بە باشی ئەنجام بدەن.

![](/server/images/02-34.png)

یەکەمیان دەبێ سیستەمەکەمان بەڕۆژ بکەینەوە بەم فەرمانە:

```shell
yum update
```

گەر پەیامێکی نیشان دا پیتی “y” لێبدە بۆ بەردەوام بوونی پرۆسەی بەڕۆژبوون واتە update .

ئەم فەرمانەش بۆ دامەزراندنی دوو دەستکاریکەری دەقە، واتە nano وە vim

```shell
yum install nano vim
```

پەیکەربەستنی ڕایەڵە :
لە CentOS 7.3 minimal فەرمانی ifconfig بە شێوەی پێشگریمان ئیجرا نابێت دەبێ خۆمان دایمەزرێنین بەم جۆرە :

```shell
yum install net-tools
```

گەر گەرەکتە رێکخستەنەکانی ڕایەڵە ببینیت یان دەستیان تێوەردەی بەم مەسیرە بڕۆ بەم فەرمانە :

```shell
nano /etc/sysconfig/network-scripts/ifcfg-ens33
```

ئێستا ئەو شتە دەبینن کە لە قۆناغی دامەزراندنی IPـیەکان پێشتر رێکخرا، بەم جۆرە :

```shell
TYPE="Ethernet"
BOOTPROTO="none"
DEFROUTE="yes"
IPV4_FAILURE_FATAL="no"
IPV6INIT="no"
IPV6_AUTOCONF="yes"
IPV6_DEFROUTE="yes"
IPV6_PEERDNS="yes"
IPV6_PEERROUTES="yes"
IPV6_FAILURE_FATAL="no"
IPV6_ADDR_GEN_MODE="stable-privacy"
NAME="ens33"
UUID="233f2c1b-877c-4b28-b17d-1eb091ded288"
DEVICE="ens33"
ONBOOT="yes"
IPADDR="192.168.1.100"
PREFIX="24"
GATEWAY="192.168.1.1"
DNS1="8.8.8.8"
```

گەر لە خزمەتگوزاری DHCP سوود دەگریت بەم جۆرە کردار بکە:

```shell
TYPE="Ethernet"
BOOTPROTO="dhcp"
DEFROUTE="yes"
IPV4_FAILURE_FATAL="no"
IPV6INIT="yes"
IPV6_AUTOCONF="yes"
IPV6_DEFROUTE="yes"
IPV6_FAILURE_FATAL="no"
NAME="ens33"
UUID="233f2c1b-877c-4b28-b17d-1eb091ded288"
DEVICE="ens33"
ONBOOT="yes"
HWADDR="00:50:56:15:23:79"
PEERDNS="yes"
PEERROUTES="yes"
IPV6_PEERDNS="yes"
IPV6_PEERROUTES="yes"
IPV6_PRIVACY="no"
```

گەر پێویست بوو دەستکاری بکە !

ڕێکخستنی /etc/hosts :

```shell
nano /etc/hosts
```

بەم شێوازە زانیاریکەتان بگۆڕە :

```shell
127.0.0.1   localhost localhost.localdomain localhost4 localhost4.localdomain4
192.168.1.100   server1.example.com     server1

::1         localhost localhost.localdomain localhost6 localhost6.localdomain6
```

پیرۆز بێت دامەزراندنی ڕاژەکەتان لە دابەشکراوەی گنو/لینوکسیCentOS 7.3 تەواو بوو . ?









سەرچاوە :[howtoforge](https://www.howtoforge.com/tutorial/centos-7-3-server/) 