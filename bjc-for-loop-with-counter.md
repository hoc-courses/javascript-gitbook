# bjc for loop with counter



[**1.3.6 Looping with a Counter**](https://bjc.edc.org/bjc-r/cur/programming/1-introduction/3-drawing/6-the-for-block.html?topic=nyc_bjc%2F1-intro-loops.topic&course=bjc4nyc.html&novideo&noassignment)

**Computer scientists describe this program structure as looping, repetition, or iteration.** [**Sequencing, selection**](http://bjc.edc.org/bjc-r/cur/programming/1-introduction/2-gossip-and-greet/4-learning-names.html?topic=nyc_bjc%2F1-intro-loops.topic&course=bjc4nyc.html&novideo&noassignment#AP)**, and iteration are building blocks of algorithms.**

**The forever block generates an infinite loop that goes on forever. An infinite loop can sometimes be the result of a bug, but in some interactive programs, you want the program to keep running until stopped by the user.**

**You've seen these ways to repeat a set of commands:**

* ![the forever block](https://lh5.googleusercontent.com/Gjq5gj3XKcg-21oZU6a6sPNmcDThmaF1tres-i6EIlPJPdCjxqx0H4D_o6NWux2QPgSGpkUWyQtS_DQJosmupiFKoNEe9DyKIH20FvnfGGY_ohpbqXFtl0o5WRtUNoO2_HJuJcs) **repeats the same commands forever. \(You used it to** [**make Alonzo keep moving**](http://bjc.edc.org/bjc-r/cur/programming/1-introduction/1-building-an-app/6-keeping-score.html?topic=nyc_bjc%2F1-intro-loops.topic&course=bjc4nyc.html&novideo&noassignment)**.\)**
* ![the repeat block](https://lh5.googleusercontent.com/wfsZVmxMoGSnbL1Kzyr6fhtYKXVck28_mln02MioKzmztkpJ1lc0ziq8Aa4n3bJdzyTCxG4fF2xZn9NS4zpQK-lVja_nvKcw_YD9nx9qVhqNAXe773IBnNiQkGyD56mqVF3Phic) **repeats them a specific number of times. \(You used it to** [**draw shapes**](http://bjc.edc.org/bjc-r/cur/programming/1-introduction/3-drawing/1-exploring-motion.html?topic=nyc_bjc%2F1-intro-loops.topic&course=bjc4nyc.html&novideo&noassignment)**.\)**

**On this page, you will use for loops to repeat and count the repetitions so you can use that counter to draw shapes with repeated patterns...**

![spiral](https://lh3.googleusercontent.com/7ykP3wzjKv1QgjGFnRwfRnKPFSjItEWty1SJ5h0kG7zHDlYqZGmfLK7Tf0FJ9mHcByMtSRewWRBYaWqjKrLPIJjGnv8UsSxcYFb4Kjd_KCP63Anq9rc6_a-RLf_tjvG2C7wH1Iw) ****![nested squares](https://lh4.googleusercontent.com/RRLYrZTHwma-qpP1yZRSAU0QCntQfRaav_CjArlAUllaXT9hIvfQcOwY6f4qw39mX0g2Z_kcU62syWbTPwtZfLD7iJgAiv0UCLgR4PnE5XtFcQVVYs5ApX0Gmx13eBwhPWajt1g)

**You can use** ![for](https://lh4.googleusercontent.com/2IEd_Tdl0o620KE2KrTJaCraFs4FciMzB81tovoqoUwvGljmsnfFpKnfaOLCNDbhjDC7bYVzVO-lzwGvRUjpTcH1apustdHCMVQjT9pUj8TBFTIGBs4ROmH28I2r0jiGiYivVoU) **to name a variable \(here,** ![i](https://lh5.googleusercontent.com/9bfOyy0CCbdHrxPXH6xDmEdyRIScEejlSL9BOBjMH8WO8dbryFPWRBPo3ph5XcZ3AeuBNxLs3Vhw21GZhrRNXfBk-sJNpX6yh90gbQ7OHz6ogrReNA_W95eQ0hA8qs73dHtOUvs)**\) that counts each repetition, and you can use that counter variable in the repeating script. For example, the for block lets you simplify long scripts like:** 

**Each time the for block runs the script inside, it changes the value of the variable by 1, counting from the first input number to the second.**

![say \(1\) for \(2\) secs, say \(2\) for \(2\) secs, say \(3\) for \(2\) secs... say \(10\) for \(2\) secs](https://lh6.googleusercontent.com/2q8TPh1fQTzUrFFyMwruEnvj4gnZrn53QFn5fOLKzR3N1tXk8H3rD5FnF66sbP7ADa8bBj29Y7J7GwLvDai9xltdgGr5HXj4X3i24_4gJL1wwbM-NcGhFEWFkp6aBneZvYcK7FA)       **to** ![for \(i\) \(1\) to \(10\) \[say \(Hello!\) for \(2\) secs](https://lh5.googleusercontent.com/86762j4y4M0tjrwxoyiaOKzFeJRg56yeWTkz7DVKs5-_aduLDVSoAX9CsqbgBl-Ho57eban1ArQDiGb4FuO9TP_40YDSARM48K-jkY3W4NztJ2Dc7ey0wabdhe41ydxhlDA4Q3A)

![Import Tools](https://lh6.googleusercontent.com/sfycM8NubNIKdgPR5rDesIUNuhHGylzL45MoJjHLkN8nTWevl8pwYTDkwNZbqK_jSLmo4gxcaTwgz5uLkoeZIiJqUKrlOSUTnSG0_Nn2qcE_KuGnF5d-xvh_vYW08_QxxJ8O6UM)

**In the current version of Snap, the for block isn't installed automatically. You'll need to import tools once into each new Snap project where you need for and some other important tools.** 

![select &apos;Import tools&apos; from the Snap! file menu](https://lh4.googleusercontent.com/g8Rro9NAw0QQLngSYuS2Ssph3_mYRuM4_z2PlFg33WdlgMbm7DxvpG_JRmxmX0er5ict7hISqz3nOb5HMXyaWVBEtYb4hiWjI91neDCfRv8iyu95-Q39YMpDFLoOaqhOugBbyRM)

1. **Click on the File** ![File menu icon](https://lh4.googleusercontent.com/GXnGOwnF3nsQZySA1wQxa78MIk37oSQgUX-qXnauVO_uwplksuT8V4k1gmi9QV1UdpgkXVBtf7Z8a_5fbywJcVv9DfqHai4S_gasa7qi-5xPgy1XF1VuZyUCiI83RIYoAD5n4KA) **menu at the top of the Snap window and select "Import Tools."**
2. **The for block gives you a default variable, i \(for index\). You can change the name of this variable by clicking it. Once changed, drag it out and use it just like any variable.**
3. **Build this script that makes the sprite say the numbers 1 through 10.** 
4. ![for \(i\) = \(1\) to \(10\) \[say \(i\) for \(2\) secs\]](https://lh4.googleusercontent.com/mruQniQiDDpMybfwoD6vRkGQewdHA3Vk1p8fnP0iWrqGkEF5i3pQ2vCUrk7s5U7FvAYV2vPUjdAvffbE5P4CQJ6pP15jV695w4frLl6SgIc3HEianYoP5o_mNZiSvK1mo1FQEzQ)
   1. **Then modify it so that the sprite says 0, 2, 4, 6, 8, ... up through 30.**
   2. **Discuss your solutions with another pair.**
5. **Experiment with spirals.**
   1. **Build this script and try it out:**
   2. **This design got the nickname "squiral" because it's a square spiral.**
   3. ![squiral script](https://lh4.googleusercontent.com/6vroDSq0BbaXRi9AffT4XDGA54Si15rObk8lQQCniGWyP2pMSxDsOKIEm7zV1Ot-_KCvS5vzGHkbOODOuN0V0FFsOcdBCpsisb0TtaHDXpDaRd94aX8g_Fg0IIHAKml1UWFYk_A)
   4. 5. ![Talk with Your Partner](https://lh3.googleusercontent.com/KDRGfWslcfESaKatCSGK4fsGrijNQpTBSm2vXYaBtL32PGzb05vw37qpFa6qhVZt29-2FDt8Mj2zASPaedpofKYomZs23gopwmLbebn8mYBoZ8SXBoJK46px4S4eRJAEfkyhID4) **Make sure you can explain why the squiral spirals outward.**
   6. **Try switching the order of the 100 and the 1 in the for block in the squiral script. What is the result?**
   7. **Try changing the turning angle in the squiral script to other numbers such as 92, 126, etc.**
   8. **Change the inputs to turn and move to get as close as you can get to a smooth spiral:**
   9. ![spiral](https://lh5.googleusercontent.com/4fkryvrVddkPXreUvsmswT44EwjpvZhvDjVCz6ydQxpbHCCcMSHV2_h_AQxCk4KlPpEWf2eHm3e_Ze61T05Q0HBTGqMwQrtyHGncVGYhUOcYADhU9e4lg9Bv1B5FNOPvB6fIohc)
6. **"U1L3-Squiral"**![Save your work as U1L3-Squiral](https://lh3.googleusercontent.com/dL-UmcdU4OZQyaWCi5TThWg2rrgLGUnz8ZJc75xp9Rgyt4IWu8cDNR1ZU3VBC62Ouq_oktxAoctB91n1G4ojzmIQ7hQm64uQHChrIN9tImzU_Ic-gCSwje5xhQ_ktriVXSwmPiM)
7. **Open your U1L3-Pinwheel project, and build a nest squares block that uses for and your polygon block to draw nested squares. Give it an input so that it will draw whatever number of squares you specify, with each square larger than the previous:** 
8. ![nested squares](https://lh3.googleusercontent.com/bMqu5SBxDd3qUbb6Qmc-DzI5EX_Z8nz_qfjMwX9crcGIgJn0zCiShfzq-mYQ9yHCxXDaYIw7iZKmKYbgSfMaW47U8kwUWH9u5sctDpD4lBpNJ0ubvNLu8gDrZxpjkk9Mck_9VsU)
9. **Build nest polygons that accepts the number of polygons and the number of sides for the polygons.**
10. **Build a script that draws 12 regular polygons, each with one more side than the previous one, as shown below.**
11. ![polygons: triangle through decagon](https://lh3.googleusercontent.com/cK58UJ7KW4tYoR8Ze29SX_zLGC9qMovrwlM-AC-JlWZ6VstZzWEA8oyPpyMWLe4j-0Jv1USy3A6G81Ouz6_EM8ic_xp1NFMkz6szimA9b7DEjrxELG3d1SfH4o5ISFRceoSGB_M)
12. **Predict what this script will do before you try it:**
13. ![for tens = 0 to 9, for ones = 0 to 9, say \(join tens ones\) for 0.3 secs](https://lh5.googleusercontent.com/obOhdWRhiByFBVUveDY4K9dDP0cYqzpREeTmU2WHtX0ofmL9OAY3HsjmFYbpr9bQD5YcdakLMDOvBNw5RYjfD3Fu9fnULdD0vDsfR23lO_VNR9tPXhDfUkfxa9miFCSeaBnLZoM)

**Build a script that counts down by 10 from 100 to 0 \(that is, 100, 90, 80, etc.\).**

**Find a way to use for to nest squares this way. Build your block with two inputs that let you specify how many squares the design will contain and how much bigger each square will be than the previous one.**

![Tough Stuff](https://lh5.googleusercontent.com/-u_wsv3O2J4GgXwSQJHuZhnur0G9Eon0ASH0m70clLB7gj5GU0ecv04Lo6N9HKA1mMPPBI1EN5M9DojJCXFvd3vy74v2d4UAemDI4YUPiY3LoADKVXN1O_YoYU7m5lqSedniHFk)![concentric squares](https://lh3.googleusercontent.com/79sywPkJ1FsS2VwZaPyXnQ5XkhQbBpfvR1_FlX_H--41fN6Lu8lwIKmXGXxQc6gNJerOe0K1qewxdg_ydIKjZnfWMVY6_XPd0maqK9W9OeZBzNgb7hbIibEQ_iS0-Iijx8wBR9M)

**Below are two animations that use the pinwheel code with inputs. Find out how to create your own artistic animations.**

![Array of pinwheels animation](https://lh5.googleusercontent.com/GaihcnSWpANldEFVYq4pK465ROYamuIpQA20L5JQyhCQfYMYAfl43nZAt0gwKv6R6DCEz94WP94DInLFugdVo2rjiltcS2a60cwGuBh9Q_E5S_gJfcLzc_PISFk2I9EZHrEQiFw) ****![Pinwheel wreath animation](https://lh6.googleusercontent.com/4RTx1g746TpgRVVng2_PKJY58SWxP3m1VP_8FPCMD-eW0Ixt-nzckZSctd0chrZ3zB3biadepiRcTGE38aOcKLAoPHyuugTsjpPFGsyxR0BG1Tbc5onAxa8UqKKpuOireWXgDWw)

**The following code may give you ideas about how to create animations. Make sure to remove all wait 0.5 secs blocks from your pinwheelcode so they don't slow it down. The warp block allows the drawing of the pinwheel all at once.**

![Code for creating animation](https://lh3.googleusercontent.com/Apw3SDPkpeWPZOI3D9wKkUAsiVlZ3PALud1Xy_sXvRY7Ltz6T5cKQNG0hma-dx2pROJaHZgOgWqlxiOAC_I_XX5Fewrsvy7okf0M28tZ8vAhyCyZVoXz2HVqICfLuFL5-wcuUOo)

![Tough Stuff](https://lh4.googleusercontent.com/w2OweARb6EcUrh-fPJTD-0Qht7pJZ80iHgf9Q0ANpcrsINW2FI1RsUpstdtGWcQ_Ic-fGmSJLiLE66nrslPU6m0cL6AOJbKKd2GIvLqnqKjH2u1UEKDtghgeZ7SxNofW0gFhbOs) ****![Tough Stuff](https://lh6.googleusercontent.com/CZbAKk5xqJNbhRI4rudYFwg798R7eiZoxogRQrbGIT1aofVuol5DprPrLBmpNif68VZ9wuRTxuBil0ZQg7uV62ZiwRTqNqTgss444e2WXKwazzqPPQu5UHv4sSbfW4lTs6nSo-o) ****![Tough Stuff](https://lh4.googleusercontent.com/cCcWzqS8DSIhQtRTXU-TzVFOVz7jH1_gW_8wepFdE15F2I1DV4n4dfocK1rcLDnoNXNdNx_jMk_BC7bhmgA8KDyPmOI6ZN-gQA66x4r_c-RCsAHqF75tTd82lnTczOGi7PtRiHo) **This block is like the squiral, but instead of changing the input to move, it changes the input to turn:**

![inspi \(num\) \(size\) \(angle\) : for \(i\) = 1 to \(num\) \[move \(size\) steps; turn \(i\) \* \(angle\) degrees\]](https://lh3.googleusercontent.com/aAqGdjYN2TxNVKqITck_SnRqceyysn1OBnU4I9XtT_vGUd1-Dffu_fR-WssXvY_wE2ow8s2Dj4rGqAVpYvsljHhAT4YkHZvkrnQjek-ePD6kj_Ie-pEqrSDTR96l6H1mjNwuEA0)

1. **Try sketching what it will draw with an angle of 2.**
2. **Then build it, and try each of these tests:**
3. **You can stop each test with the stop button \(**![stop button](https://lh5.googleusercontent.com/OXn_hEP0kRhghH7vyEvuqn1jXSV4XWRUywe8Aty1dacoFlJehPSkHIJOa_IEhkmU53QTDhbg31QL5nzHSTwiM1gZU87MqHam5Y_SMEBTMznjtWD95e8LS55nFDkpkt11yDvJNd8)**\) when you're sure nothing new will happen, but don't decide that too quickly!**
4. ![inspi with \(1000,10,80\), \(1000,5,1\), \(1000,5,7\), \(1000,5,13\), \(1000,10,77\)](https://lh5.googleusercontent.com/VJH4SEGF3L40a8HGoCP8xO7mBSNKpBjZa32t_G15zOF2EHnmduOltC7Nc9LhBy1MrtjUJKcIFM_fCnRR7iZgagFnj6HsvPU63n5oUtz55JSEHPov8EXzu0tvj3oB9HXSMpKUGTU)
5. **What's going on? Can you work out a theory to predict anything about the shape it draws for a particular angle input?** [**\(Don't click unless you really, really need a super big hint.\)**](http://bjc.edc.org/bjc-r/cur/programming/1-introduction/3-drawing/6-the-for-block.html?topic=nyc_bjc%2F1-intro-loops.topic&course=bjc4nyc.html&novideo&noassignment#hint-1)

