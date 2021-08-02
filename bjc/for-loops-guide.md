# For Loops Guide

Yolanda Shen

Supplements the list portion of Lists and Scoping

Corresponds with Lists Lab 

#### This guide assumes you: <a id="h.1nkupu69y0kx"></a>

* Are familiar with what a list is
* Have reviewed or watched Lecture 4

### Goals <a id="h.o4l6ixk5iyu4"></a>

* Understand differences and similarities between for-loops
* Know when to use which for-loop

### Outline <a id="h.gafh5nl3narq"></a>

1. Motivating Example \(how to read errors\)
2. For Loop Overview: for i vs for each item
3. How the For Loops Relate
4. Summary

## 1. For Loop Overview <a id="h.6ox5i6f1fe8k"></a>

These are the two most widely used for-loops in iteration:

![](https://lh5.googleusercontent.com/mGRt64PXfD14HBTsF9J_j1YPw8fQnPSG88ao4Jl8947oWXwYW9ax1szTuz_S31-gyXMy6BR4hQqGc35xOaSu0ycvlzAWl2sGOYeCmXL7Cw1iX9FhhOxf4xTXhK70GjwHSQ)                        ![](https://lh6.googleusercontent.com/Nc_XRApc5L_MvxBCvywpT_y-9RJ7e3fAeAbFzzN-uuKphvd18GZzPaSRFCBouJjfYwV-DeX8bo_cbizxJeKBt6p227Dzeb4ii6qwuFe19DlUb2FHFxYGGXqY-NgRHF9ZYg)

### for i Loop <a id="h.ia9wzh537bgg"></a>

Let’s say we have the following script:

![](https://lh3.googleusercontent.com/C5wXgiwHoRnBBkrkIMbnr3FP7qVxRep6OggT8tWCmQ8UdBtT9uAxmDYsxL_FeRFHhGB_thetNZRfkuKYa-SeDjxtEx1nilyG_eMa1fbeSvX-bMUjXfJVp3Qsip3RRbHy3A)

Here, i iterates over the numbers in the range 1-10, inclusive. In other words,

On the first loop, i = 1 and the sprite would say “1” for two seconds;

Second loop: i = 2 and the sprite says “2”;

...so on until the tenth loop.

### for each item Loop <a id="h.89h03s4iwa9v"></a>

![](https://lh4.googleusercontent.com/f_5XSqV-IiUIk29jigUkzDW1SAM5_tRbqAYkBQdblwNe9IU0xfDoC-J-rY5Ujcgwz4ZPbfBpF0MPy1BZbGte5N1wuR3PCNNI38KcguOYQ_mI7ZUQmIXFXhsGXLRC65DymA)

Here, item iterates over the items in the list. On the first loop, item = a so the sprite would say a, and this would continue until we reach the end of the list.

Q: Now what if we wanted to ‘say’ the positions \(aka index\) of a list like ![](https://lh3.googleusercontent.com/Xj2R1xQ1xOYJNKe8nq5RCnaIEDseyA1Uo1SXXwhS08biEKUjMP2BWeYwY-v9OQKIPqGXwIqXsmGfc4cyfKvD2i5yyL6WnsDTaZE-H90dct_VQM1KcyX8Sdp01PQHc_Kprg)? Which for-loop would we use?

A: We’d want to use the for i  loop, even though we are dealing with a list, because it keeps track of the numerical placements \(1, 2, 3\). On the other hand, for each item does not keep track of the index, so you don’t know where you are in the list.

### for each item has “blinders” <a id="h.dchlglmjcj7z"></a>

Another way of thinking about for each item is to envision that it has blinders. Let's take a look at the image below.

… ![](https://lh4.googleusercontent.com/6U3j9YCW74ydB6G2qo3LVzLOF1NsOP4vYZzcBpF3oOd0GtZXbWozEsH2K1V_dwOprLdma5LaIV4IKs3oHeUVyW8NnblT5MwaiuOPvXcXfU0_l_R6iQtnKoArQYRylQnxzg) …

for each item may be able to point at the actual contents of the list, but since it has blinders on, it can’t ‘look around’ to figure out its index. The only way for us to know where in the list we are is to use for i .

![](https://lh5.googleusercontent.com/IN4NPfV_HTFCtfY4L-91-d6izMGIQCqdLIPu43Z5vuQIrySlVC4JIxnjjaWBC1D68v1iqDZXaPBi7V72oRQwTiODQRUoVIysiY3dq9Uq4Jraq43fcMIedYqGfuRQYgPGrw)

## 2. How For Loops Relate <a id="h.fu5uck47oke0"></a>

### Making Our Own for each item Loop <a id="h.6q1cjgh9rm5"></a>

![](https://lh4.googleusercontent.com/Xscpz9TiVTS_kIv5k3BHpMMwiR4btcdhIC5GEPF_h9POogGeI-TUCmu6e2XQBlQ4Sz_BrOD13KrEmGRaZEbrH46jWs1OPchwgGkP-OxCwogmSMGsWIvKPERFVJM_pIjTsw)

Say we didn’t have a for each item loop and wanted to make our own. Let’s consider what we might put in the ? in order to achieve the same behavior.

A: 

![](https://lh3.googleusercontent.com/sVlb4xAPe4wO5BSwn_11OHK-VkmXynxhtE1hz8L6OoNNB5D2F85vApAqaMVYLwEa_UYJnnZyEQsssVcp5Ijmel-5qMcKavbQtk-OBTxCuh43fQdnCsaBAjmcGobljDTqlQ)

Yay! We’re allowed to do this because once we know the position of an item in the list,

Snap! has a handy block that allows us to immediately access the item.

![](https://lh5.googleusercontent.com/L5AO5kq9YiD8i5jTot1b9ZDDIekklq4yjNsefCNyYNpTnuweWX5AoxKEGfA2UG80O9g4BWhcTZdkoyjyjroMK45Iwk6mpzLr3Wi13XpsEkXEUEYfQu3TLSITaB2eKvdahA)

### Making Our Own for i Loop <a id="h.p7yexarwwzqd"></a>

Let’s try the other way around now.

![](https://lh4.googleusercontent.com/7eJDT1IbPFJIswXBGNmnm68cHb7siJ0TdPj_UpqgL0XCkQnsCx9OppN4vn_0jk45xEHO2V03o5Oa9J_bArxlfLrADHDr5OISvvNdDNFBcB78Q_xsk6tpyZFm7Ym1QKTcJg)

A:

![](https://lh5.googleusercontent.com/CwTjUNrl_ugUIvrLIl0waI-Wn-oYF8mq4HLCI2oUjbmDrtrVsReNWLsVGeh554pMYlNSuUhz0IuoBgZktUNUNmoTd8CMtcLXmtqHvOuS3PdzMSFcZhIihrHfNKEzuolBxA)

Unfortunately, this block can be a little buggy. Here is why:

If we know item = a , and  list = ![](https://lh6.googleusercontent.com/RsStBLJauML5B5mMi2GWtyWxwGn3nT_yjd367A2f2_C1pBtWkRrTDLJFY193maHQYbMKa8Nw-a-GSiGTUAO8Nesfq98vwLXs7-0zWU1EvWdzdPDmIvTDPCGRKUhG4z2Eew) , there is no way even we humans could know which “a” is being referred to! The ![](https://lh4.googleusercontent.com/ggGkXZLPUe2WM5WYskcYuzSzy_V4sVDlLmVrX3BuZ-8D8UktD5jShzdz8xCQI0EyydwChXkuJ7h8BiIPp51hkIlakL_hDLFbNSl8b9pc2HWeRrLlVuk_4TmT8IGSoKC-hw) picks the first index available. With the given list of all ‘a’s, the block will report 1.

\*Note: There are a few somewhat complex ways to go from for each item → for i, but using for i + ![](https://lh6.googleusercontent.com/qoApqOha1JVkMs5vsK3TRVSoY8lOWQ6k4Z6fCVpf_5Tbdm0FuQu2xI-P09zhf_CwMF00Ff0aZqudrj690h3vB2ng9qN8twqRmkjYkUAU0T39Dix0GK5E9fiG_t_rPNaoGQ)is simpler and accomplishes the same thing.

## 3. Summary <a id="h.fh0ntzskfqz4"></a>

### For Loops <a id="h.65b6ptfjryee"></a>

![](https://lh5.googleusercontent.com/abPYyARFfMt7T8-CZte5LHj2fdsN_3-r2wpmX-yjG2COaT2SIZii_a9Xk_29zeYdAl2qVZR0EY-ev9xHOd9zU60i9RvxP1ywiyNhizM9V6tKL2028DzfMYAkPQ8yPVEQ6g)

### for i ⇄ for each item <a id="h.2t6lhhx1d7j0"></a>

![](https://lh6.googleusercontent.com/4MmazW-V2iFCAmtplg-TjmLCmLEUa_Fs2kEenRBXC5TsGI8cCC_3EI21x00YzNqebOZQ4Hi1Zh-aD-6KtFXfi0-h09U3E74zaZmvuPLYBYQ26jSwM6c0lY_PM4Qvmw9d2w)

In terms of how the for loops are related, you can easily convert from for i → for each item.

This is useful because you have simultaneous access to the index and the item when using for i and ![](https://lh6.googleusercontent.com/qoApqOha1JVkMs5vsK3TRVSoY8lOWQ6k4Z6fCVpf_5Tbdm0FuQu2xI-P09zhf_CwMF00Ff0aZqudrj690h3vB2ng9qN8twqRmkjYkUAU0T39Dix0GK5E9fiG_t_rPNaoGQ).

You can also convert for each item → for i  with the ![](https://lh6.googleusercontent.com/2pGr4bTUF83OymebzWEIPWnPIORa6guGYkoAQp1ugtZsOhsCHK7gL0vpQw8flZXjUhbFTYGGwchThD48iNEH9PjSONaH-66Z7DzA76kp9JHUxz1IN1E9YGu1ijGozqnKFQ) block, with a limitation.

\*Note: There are a few somewhat complex ways to go from for each item → for i, but using

for i + ![](https://lh6.googleusercontent.com/qoApqOha1JVkMs5vsK3TRVSoY8lOWQ6k4Z6fCVpf_5Tbdm0FuQu2xI-P09zhf_CwMF00Ff0aZqudrj690h3vB2ng9qN8twqRmkjYkUAU0T39Dix0GK5E9fiG_t_rPNaoGQ) is simpler and accomplishes the same thing.

