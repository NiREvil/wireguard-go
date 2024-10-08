## $\color{orange} \Large \text{WARP-PLUS}$
$\color{silver} \large \text{Many thanks to Usef Ghobadi and dear Mark Pashmfouroush}$

$\color{gray} \large \text{Warp-Plus is an open-source implementation of Cloudflare's Warp, enhanced with Psiphon integration}$
$\color{gray} \large \text{for circumventing censorship. This project aims to provide a robust and cross-platform VPN solution}$
$\color{gray} \large \text{that can use psiphon on top of warp and warp-in-warp for changing the user virtual nat location.}$


$\color{orange} \Large \text{Features}$
```POV-Ray SDL
- Warp Integration: Leverages Cloudflare's Warp to provide a fast and secure VPN service.
- Psiphon Chaining: Integrates with Psiphon for censorship circumvention, allowing seamless access to the
  internet in restrictive environments.
- Warp in Warp Chaining: Chaining two instances of warp together to bypass location restrictions.
- SOCKS5 Proxy Support: Includes a SOCKS5 proxy for secure and private browsing.
```

![rainbow](https://github.com/NiREvil/vless/assets/126243832/1aca7f5d-6495-44b7-aced-072bae52f256)  

## جدول مطالب
- [نصب و اجرا](#نصب-و-اجرا)
  - [نکات مورد نیاز](#نکات-مورد-نیاز)
  - [توضیحات تکمیلی](#توضیحات-تکمیلی)
- [رنج آیپی و پورت های وارپ](#رنج-آیپی-و-پورت-های-وارپ)
- [ویدئوهای آموزش](#ویدئوهای-آموزش)
- [راهنمای کلی دستورات](#راهنمای-کلی-دستورات)
- [کد اختصاری کشورها](#کد-اختصاری-کشورها)
- [بخش دانلود ترماکس](#بخش-دانلود-ترماکس)


 ![rainbow](https://github.com/NiREvil/vless/assets/126243832/1aca7f5d-6495-44b7-aced-072bae52f256)  



<details>
<summary> v1.2.4 تغییرات در نسخه </summary>

```CSS
- actions: support build for mips-softfloat devices
- Changed install script link 
- deps: update psiphon-tunnel-core
- psiphon add countries, clean up code, fix connection timeouts
- use noql-net/certpool RootCAs
- Fix android DNS issues by using Go's built-in DNS resolver
- improve wireguard code
```

</details>  



<details>
<summary> v1.2.3 تغییرات در نسخه </summary>

```CSS
warp: fix duplicate device bug by @markpash
Automatic warp reserved field by default, add win32, include wintun.dll and other cleanups by @markpash
```

</details>  

![rainbow](https://github.com/NiREvil/vless/assets/126243832/1aca7f5d-6495-44b7-aced-072bae52f256)  

<p align="center">
  <br><img src="https://raw.githubusercontent.com/NiREvil/workers-cloudflare/main/Other/pics/warp-plus2.jpg" width="960px">

![rainbow](https://github.com/NiREvil/vless/assets/126243832/1aca7f5d-6495-44b7-aced-072bae52f256)  

## نصب و اجرا 
  
$\color{orange} \Large \text{Getting Started with Termux}$

```POV-Ray SDL
bash <(curl -fsSL https://raw.githubusercontent.com/NiREvil/wireguard-go/master/termux.sh)
```

---
  
## نکات مورد نیاز  

**عدم اتصال:** اگه حس کردید کانکت نمیشه یا خطا میده دستور 
```POV-Ray SDL
rm -rf .cache/warp-plus
```  

رو اجرا کنید تا فایل‌های کش‌ پاک حذف بشن و مجددا دستور warp رو اجرا کنید.  


**اجرای مجدد:** بعد از نصب برای اجرای مجدد فقط کافیه که `warp` یا `usef` یا `warp-plus`رو وارد کنید. همش یکیه هیچ فرقی نداره.  


**عدم نصب:** اگر با 1 نصب نشد و خطا گرفتید اول یکبار گزینه 3 رو بزنید تا وارپ پلاس `Uninstall` بشه سپس عدد 2 رو انتخاب کنید یعنی Arm (عموما برای گوشی‌های قدیمی و پردازنده ضعیف این گزینه جواب میده). 


  
    
**نمایش راهنما:** برای نمایش راهنما دستور `warp -h` رو اجرا کنید.  

  
    
**اجرا روی لوکال‌هاست:** دریافت ترافیک وارپ پلاس بر روی آی‌پی و پورت `127.0.0.1:8086` روی پروتکل `SOCKS` یا کپی و وارد کردن این کانفیگ در نکوباکس و ...
```POV-Ray SDL
socks://Og==@127.0.0.1:8086#TERMUX+USEF
``` 

  
    
    
**توقف اجرای اسکریپت:** برای متوقف کردن وارپ در حال اجرا از کلیدهای ترکیبی `Ctrl + C` استفاده کنید و همچنین برای بستن نشست فعال و خارج شدن از ترماکس پس از متوقف کردن آن؛ از کلیدهای `Ctrl + D` استفاده کنید.  

  
    
    
**باز راه‌اندازی:** برای اجرای دوباره دستور قبلی در ترماکس از جهت‌نمای رو به بالا ` ↑ ` استفاده کنید. 

  
  
    
**تبدیل اکانت وارپ ب وارپ پلاس:** در روش تبدیل اکانت WARP به WARP plus (گزینه 6) مقدار ID نمایش داده شده کپی و سپس آنرا وارد می‌کنید. پس از اجرای WARP دو اکانت برای شما ساخته شده که پس از انتخاب گزینه 6 خودکار مقدار ID هر دو اکانت را پیدا می‌کند و شما باید هر بار یکی را انتخاب کنید و یا میتوانید با انتخاب manual مقدار ID دیگری را وارد کنید (مثلا برای خود برنامه‌ی 1.1.1.1 یا جای دیگه) با این کار هر 20 ثانیه 1GB به اکانت شما اضافه شده و اکانت شما از حالت معمولی به پلاس تغییر می‌کند.  

  
    
    
و همچنین می‌تونید برای تبدیل شدن وارپ به وارپ پلاس خیلی راحت‌تر مستقیما از [ربات‌های تلگرام](https://t.me/F_NiREvil/5271) کلید لایسنس دریافت و در دستور زبر جایگذاری

```POV-Ray SDL
warp -k yourlicensekey
```

سپس آنرا اجرا کنید.  

  
	
   
	 
**تغییر لوکیشن وارپ:** برای تغییر لوکیشن از طریق سایفون از منو یا به شکل دستی باید اقدام کرد، برای مثال برای دریافت آی‌پی USA در خروجی از دستور زیر استفاده کنید:  

```POV-Ray SDL
warp --cfon --country US
```
  
	
یا برای مثال برای Estonia از دستور  زیر استفاده کنید: 

```POV-Ray SDL
warp --cfon --country EE
```

  
	
**اسکن آی‌پی:** برای اسکن آی‌پی تمیز وارپ از دستور  

```POV-Ray SDL
warp --scan
```

استفاده کنید.  

  
	
 
**پروکسی چین:** برای زنجیر کردن دو کانفیگ وارپ (proxy chain) باهم و تغییر آی‌پی خروجی به آی‌پی غیر ایران (عموما آلمان) از دستور  

```POV-Ray SDL
warp --gool
```

استفاده کنید.  


![rainbow](https://github.com/NiREvil/vless/assets/126243832/1aca7f5d-6495-44b7-aced-072bae52f256)  

## توضیحات تکمیلی

**و اما بذار بهت بگم که** خب دستورات دیگه‌ای هم وجود دارن‌ مثلا:

  
	
**وارپ با آی‌پی سفارشی ورژن 4 یا 6:** از قبل می‌تونستیم انتخاب کنیم که وارپ عادی ما با آی‌پی ورژن 4 ران بشه یا با ورژن 6 مثلا من چون می‌دیدم واسه مخابرات خودش ipv6 انتخاب میکنه میومدم با این دستور اجرا می‌کردم `warp -4` کانکت میشد راحت، یا مثلا اگه سرویس‌دهنده اینترنت شما از IPv6 پشتیبانی میکنه می‌تونی دستور رو اینطوری اجرا کنی: `warp -6`  

  
	
   
	 
**پروکسی‌چین,سایفون با آی‌پی سفارشی:** حالا از نسخه v1.2.1 به بعد این امکان رو فراهم کردن که برای بخش gool هم بشه اینطوری عمل کرد، یعنی می‌تونیم تو دستور گول و سایفون هم بگیم با کدوم ورژن آی‌پی اجرا بشه.  
مثلا برای اجرای gool می‌تونیم اینجوری عمل کنیم:  

- برای اجرا با آی‌پی ورژن 4 اینو وارد می‌کنیم:

```POV-Ray SDL
warp --gool -4
```

  
	
 و برای اجرا با آی‌پی ورژن 6 این رو:

```POV-Ray SDL
warp --gool -6
```

  
	
 و برای اجرای سایفون با ورژن آی‌پی دلخواه:


```POV-Ray SDL
warp --cfon --country US -4
```

و یا ورژن 6

```POV-Ray SDL
warp --cfon --country US -6
```



> اون US برای مثال بود می‌تونی هر لوکیشنی قرار بدی به جای اون. انتهای این صفحه لیست کامل لوکیشن‌ها قرار دارن
  >
>  خلاصه اینکه یا انتخاب ورژن آی‌پی رو بسپر به وارپ‌پلاس یا که خودت هندل کن.

> [!CAUTION]
> ولـی ولــــــی ممکنه انتخاب آی‌پی رو بسپاری دست خودش 

و بیاد حتی ipv4 که مورد نطرت هست رو انتخاب کنه ولی از یه رنج شخمی، فرضا یکی دوماه پیش برای مخابرات هیشکدوم از آی‌پی ها از رنج 162 کار نمیکردن، فقط 188 اوکی بود، فک کن میومد از رنج 162 انتخاب میکرد ...!!!


> [!TIP]
> مثلا این آی‌پی‌ها الان با مخابرات و ایرانسل خوبن:
> 
> `188.114.96.118:864`
> 
> `162.159.192.187:934`
> 
> `162.159.192.12:942`
> 
> `ipw.nscl.ir:955`
>
> کلا رنج 188 و 162 خوراک مخابرات و ایرانسله با تموم پورت‌های موجود.
>
> اینم با همراه اول خوب بودش:
>
>  `🖕`

  
  
**تغییر آی‌پی:** اگه تو نکوباکس، هیدیفای، ویتوری یا هرجایی کانفیگ وایرگاردی وجود داره که با نت شما عالی کار می‌کنه آی‌پی و پورت همون رو بردار و بیا داخل ترماکس و با دستور  

```robots.txt
warp -e IP:PORT
```

بده بهش تا ممبعد وقتی استارت کردی وارپ رو از همین آی‌پی و پورت ک تو پروفایلت ذخیره شده استفاده کنه. 



### بحث شیرین و مفصل اندپوینت اسکنرها
> کلیک کن این پایین تا باز بشه این تاپیک


<details>
<summary> اسکنرها و تغییر آی‌پی وارپ </summary>      


#### اسکنر ییمان  

اولینشون اسکنر پیمان هستش که آموزش مربوط به اون قبلا در [این پست](https://t.me/F_NiREvil/6305) به طور کامل قرار داده شده. [این تلگراف](https://telegra.ph/%D9%86%D8%AD%D9%88%D9%87-%D8%A7%D8%B3%DA%A9%D9%86-%DA%A9%D8%B1%D8%AF%D9%86-%D8%A7%D9%86%D8%AF%D9%BE%D9%88%DB%8C%D9%86%D8%AA-%D9%85%D9%86%D8%A7%D8%B3%D8%A8-%D8%A8%D8%B1%D8%A7%DB%8C-%D9%88%D8%A7%D8%B1%D9%BE-05-30-2) هم قشنگه برا توضیحش  

```POV-Ray SDL
bash <(curl -fsSL https://raw.githubusercontent.com/Ptechgithub/warp/main/endip/install.sh)
```


  
بعد از دریافت کانفیگ از طریق گزینه چهار (wire-g) میتونیم با دستور زیر کانفیگمون رو تبدیل به پلاس بکنیم
  
```POV-Ray SDL
wire-g -l license
```
از یکی از [این ربات‌ها](https://t.me/F_NiREvil/5271) بگیرید لایسنس رو.

---

#### اسکنر فسبیل شده خودمون  

اینم اسکنر خودمون ک فسیل شده فراموشش کنید کلا

```POV-Ray SDL
bash <(curl -fsSL https://raw.githubusercontent.com/NiREvil/warp/main/endip/install.sh)
```
---  

#### اسکنر حسین محسنی
  
لینک مخزن اسکنر ویندوزی آی‌پی کلادفلر و وارپ از حسین محسنی از بچه های خوب روزگار

```POV-Ray SDL
http://github.com/hossein-mohseni/EP-Scanner
```
---  

#### اسکنر عرشیا  

و اما به به، این اسکنر عرشیاس نیم وجبه کلا این بچه خیلی باحاله کاراش، مثلا همین اسکنر از شیر مرغ داره تا جون آدمیزاد، اصن نگم برات، ببین آی‌پی وارپ اسکن میکنه با آی‌پی کلادفلر و تو خروجی اونو بر حسب استفاده در bpb یا پنل وحید فرید مرتب میکنه، کانفیگ وارپ میسازه حتی نوع سینگ‌باکس حتی برای کلاینت مهسا و هیدیفای و ویتوری و کلا یه چیز دیگه است.  
توضیحات مورد نیاز رو از [مخزن گیت‌هاب](https://github.com/arshiacomplus/WarpScanner) خودشون بخونید.


```CSS
bash <(curl -fsSL https://raw.githubusercontent.com/arshiacomplus/WarpScanner/main/install.sh)
```

---

  #### اپ اسکنر چینی
این اپلیکیشنم اسکنره هم آی‌پی کلادفلر داره هم وارپ، توسعه داده شده توسط 2dust توسعه دهنده کلاینت v2rayNG.

[Related post link](https://t.me/F_NiREvil/6389?single)

---  

#### اسکنر آیفون و آی‌پد
  
اینم نحوه اجرای اسکنر داخل IOS هستش، من دستورات رو نوشتم شما میتونی اسکریپت داخل دستور پنجم رو تغییر بدی و از هرکدوم که خواستی استفاده کنی.  


[Related post link](https://t.me/F_NiREvil/5792)  

---  

#### اسکنر azavaxhu

اینم اسکنره وارپ هستش ولی خروجی یه لینک میده بهت که توش چندتا کانفیگ وارپ ساخته با اون تعداد آی‌پی که خودت موقع شروع انتخاب کرده بودی، لینک که بهت میده واسه سرویس bash upload هستش، وی‌پی‌ان خاموش میتونید اد کنید تو هیدیفای.  

```POV-Ray SDL
curl -sSL https://raw.githubusercontent.com/azavaxhuman/Quick_Warp_on_Warp/main/install.sh -o install.sh && chmod +x install.sh && bash install.sh
```

---  

  #### اسکنر ناشناس
  
اینم یادم نیست چی بود فک کنم پرایوت کی و آدرس و reserved می‌ساخت زمون شاه که reserved مد نبود اصلا   

```POV-Ray SDL
curl -sL "https://api.zeroteam.top/warp?format=sing-box" | grep -Eo --color=never '"2606:4700:[0-9a-f:]+/128"|"private_key":"[0-9a-zA-Z\/+]+="|"reserved":\[[0-9]+(,[0-9]+){2}\]'
 ```

</details>  
    
  

## رنج آی‌پی و پورت‌های وارپ

> [!TIP]
> شاید ب کارت بیاد رنج آی‌پی و پورت‌های وارپ کلادفلر:

**Cloudflare warp IP ranges**

```CSS
162.159.192.0/24
162.159.193.0/24 
162.159.195.0/24
188.114.96.0/24
188.114.97.0/24
188.114.98.0/24
188.114.99.0/24
```

**Ports**

```CSS
500-854-859-864-878-880-890-891-894-903-908-928-934-939-942-943-945-946,955-968-987-988-1002-1010-1014-1018-1070-1074-1180-1387-1701-1843-2371-2408-2506-3138-3476-3581-3854-4177-4198-4233-4500-5279-5956-7103-7152-7156-7281-7559-8319-8742-8854-8886
```

![rainbow](https://github.com/NiREvil/vless/assets/126243832/1aca7f5d-6495-44b7-aced-072bae52f256)


## ویدئوهای آموزش  

**$\color{lightblue} \large \text{Part 1:}$**
>
>  **with Single Command install**

```CSS
bash <(curl -fsSL https://raw.githubusercontent.com/NiREvil/wireguard-go/master/termux.sh)
```

https://github.com/NiREvil/wireguard-go/assets/126243832/458edbef-1053-4605-9afd-fdf88ef2398c


![rainbow](https://github.com/NiREvil/vless/assets/126243832/1aca7f5d-6495-44b7-aced-072bae52f256)

**$\color{lightblue} \large \text{Part 2:}$**
> **Run Warp ON Warp (gool) with: `warp --gool`**

https://github.com/NiREvil/wireguard-go/assets/126243832/07aa5d18-c4b1-43fb-9814-b23ac730afa9



![rainbow](https://github.com/NiREvil/vless/assets/126243832/1aca7f5d-6495-44b7-aced-072bae52f256)

**$\color{lightblue} \large \text{Part 3:}$**
> **Run psiphon with: `warp --cfon --country US`**

https://github.com/NiREvil/wireguard-go/assets/126243832/5054de35-e798-4603-ba7b-5c0accc0da07

![rainbow](https://github.com/NiREvil/vless/assets/126243832/1aca7f5d-6495-44b7-aced-072bae52f256)

**$\color{lightblue} \large \text{Part 4:}$**
> **Using `Warp-plus in Windows`**
> **Note:
>   Just be aware that because the video is from a few months ago; when entering commands,
>  we used a single -, but now in the recent update we use two -- in Warp commands**

[![YouTube Video](https://img.youtube.com/vi/Me2PJTOgnaQ/0.jpg)](https://www.youtube.com/watch?v=Me2PJTOgnaQ)

![rainbow](https://github.com/NiREvil/vless/assets/126243832/1aca7f5d-6495-44b7-aced-072bae52f256)


## راهنمای کلی دستورات   
$\color{orange} \Large \text{Usage}$

```POV-Ray SDL
NAME
  warp-plus

FLAGS
  -4                       only use IPv4 for random warp endpoint
  -6                       only use IPv6 for random warp endpoint
  -v, --verbose            enable verbose logging
  -b, --bind STRING        socks bind address (default: 127.0.0.1:8086)
  -e, --endpoint STRING    warp endpoint
  -k, --key STRING         warp key
      --dns STRING         DNS address (default: 1.1.1.1)
      --gool               enable gool mode (warp in warp)
      --cfon               enable psiphon mode (must provide country as well)
      --country STRING     psiphon country code (valid values - (default: AT)
      --scan               enable warp scanning
      --rtt DURATION       scanner rtt limit (default: 1s)
      --cache-dir STRING   directory to store generated profiles
      --tun-experimental   enable tun interface (experimental)
      --fwmark UINT        set linux firewall mark for tun mode (default: 4981)
      --wgconf STRING      path to a normal wireguard config
  -c, --config STRING      path to config file
      --version            displays version number
```
![rainbow](https://github.com/NiREvil/vless/assets/126243832/1aca7f5d-6495-44b7-aced-072bae52f256)


## کد اختصاری کشورها  
$\color{orange} \Large \text{Country Codes for Psiphon}$

- Austria (AT)
- Australia (AU)
- Belgium (BE)
- Bulgaria (BG)
- Canada (CA)
- Switzerland (CH)
- Czech Republic (CZ)
- Germany (DE)
- Denmark (DK)
- Estonia (EE)
- Spain (ES)
- Finland (FI)
- France (FR)
- United Kingdom (GB)
- Hungary (HU)
- Croatia (HR)
- Ireland (IE)
- India (IN)
- Italy (IT)
- Japan (JP)
- Latvia (LV)
- Netherlands (NL)
- Norway (NO)
- Poland (PL)
- Portugal (PT)
- Romania (RO)
- Serbia (RS)
- Sweden (SE)
- Singapore (SG)
- Slovakia (SK)
- United States (US)

![rainbow](https://github.com/NiREvil/vless/assets/126243832/1aca7f5d-6495-44b7-aced-072bae52f256)

## بخش دانلود ترماکس  
$\color{silver} \Large \text{Termux download BOX}$

| Source | Download Link |
|:--------:| -------------:|
| F-Droid | [Get it Now](https://f-droid.org/en/packages/com.termux) |
| GitHub :octocat:| [Get it Now](https://github.com/termux/termux-app/releases) |
| Google Play | [Get it Now](https://play.google.com/store/apps/details?id=com.termux) |
| How to fix the installation error of Termux packages on Android 5 & 6 | [Fix Errors](https://t.me/F_NiREvil/5040) |

> I recommend installing GitHub for sure, as the Google Play version has many bugs and the F-Droid version is not compatible with most devices. The best choice is the GitHub repository of the app.

![rainbow](https://github.com/NiREvil/vless/assets/126243832/1aca7f5d-6495-44b7-aced-072bae52f256)

$\color{silver} \large \text{Prerequisites}$
- Download the latest version from the [releases](https://github.com/bepass-org/warp-plus/releases)
- Basic understanding of VPN and proxy configurations


## $\color{silver} \large \text{Acknowledgements}$
- $\color{gray} \normalsize \text{Cloudflare Warp}$
- $\color{gray} \normalsize \text{Cloudflare Warp}$
- $\color{gray} \normalsize \text{Psiphon}$
- $\color{gray} \normalsize \text{All contributors and supporters of this project.}$


$\color{silver} \large \text{That's it. If you have any questions, feel free to ask in the comments.}$  





$\color{gold} \large \text{Be curious 🤍🪐}$   


  [![Telegram Badge](https://img.shields.io/badge/Telegram-Profile-informational?style=flat&logo=telegram&logoColor=white&color=1CA2F1)](https://t.me/F_NiREvil)
