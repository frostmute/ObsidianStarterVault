---
created: 2025-02-08T03:09:51 (UTC -06:00)
tags: []
source: https://archive.md/sud91#selection-523.0-977.138
banner: https://archive.md/sud91/a5dd24b25d20e8c250d19dc557fb1901c7ad986f/scr.png

---

# /prog/ - How to get a solid foundation in compsci mathematics

> ## Excerpt
> 8chan /prog/ - Programming - How to get a solid foundation in compsci mathematics

***

[![](https://archive.md/sud91/cd6e8682c61c2fcabae5cd218dd5207405cb6df2.jpg)](https://archive.md/o/sud91/https://media.8ch.net/prog/src/1439697368517.jpg)

\[–\]

This guide assumes you forgot everything from highschool. No you don't have to learn any of this in order to program you can just start hacking around every .c file in your kernel.org git source clone and see what happens. Why would you want to learn math? Because it will change your thinking. You won't be easily fooled by bullshit, you will have tools to sort through obvious logical fallacies. You will be able to optimize programs and create your own algorithms. You will be able to estimate. Above all, you will be able to solve problems using computation which is what computer science is all about. And least of all, you will get paid more than anybody else without this knowledge so if your goal is shekels then read on. Note: DO THE EXERCISES. You won't learn otherwise. Books instead of video lectures were chosen because they've lasted 30+ years some of them in relevancy in the field, also lectures disappear all the time like when MIT nuked all one prof's Physics OCW lectures because he tried to pickup a student, setting a precedent that at anytime this information can disappear. Read a book nigga.

Math Preliminary

**Basic Mathematics by Serge Lang**

Buy/Pirate this book (he's dead). It's highschool math, from the perspective of a Mathematician. You will learn up Pre-Calculus and be prepared for rigorous proofs later.

**An Introduction to Mathematical Reasoning" by Peter J Eccels**

This changes you from rote drilling and being a human calculator in highschool to learning what math actually is, and what proofs do. Excellent, excellent book.

**How to Solve It by G. Polya**

How to do proofs, written in 1940s and still for sale in every Chapters/B&N bookstore to this day because it's the best proof helper that exists.

Welcome to Proofs

**Calculus" by Spivak**

Actually, you are learning ANALYSIS, in addition to calculus. Torrent the 3rd edition w/the answer book. This is a fucking hard assed book, you may be better off reading "Advanced Calculus" which is actually easier, as the intro points out that Spivak's exercises are difficult as shit: [http://www.math.harvard.edu/~shlomo/docs/Advanced\_Calculus.pdf](https://archive.md/o/sud91/www.math.harvard.edu/~shlomo/docs/Advanced_Calculus.pdf)

**Discrete Math Intro**

**Linear Algebra by Friedberg, Insel and Spence**

Get the latest version (piracy). It's proof centric, this will come in handy later when you need to understand some Linear applications and don't know how something works so can revert back to your training in LA in proofs. LA is heavily, heavily used in all game programming. Also in cryptography and numerous other CompSci fields.

PART 2

Algorithms

NP-hard problems

**Concrete Math by Knuth et all (CONtinuous and disCRETE math)**

This is chapter 2 of The Art of Computer Programming (TAOCP) "Mathematical Preliminaries" in a format that isn't as terse. Complete this and you can do any of the TAOCP books, and solve any problem using discrete mathematics in computer science.

Bezerker level, how the fuck did they do that tier

**Calculus on Manifolds** by Spivak. This notation is used by Gerald Sussman (of SICP fame) in all his texts. It's a great fleshing out of multi variable calculus, but you absolutely have to do the exercises, it's a small book but difficult.

You write out math equations in scheme. You will get that "aha" moment like when you read SICP but for Math. If you just read the first chapter/intro you will be able to convert math equations into functions whenever you come across them. If you read the whole book you will:

\* write a lagrangian as a normal Scheme function

\* symbolically take derivatives of that to get equations of motion

\* print those equations with LaTeX.

\* compile those equations to native code and numerically integrate and plot the motion of the system

It's like magic the first time you see it. You can now write highly advanced physics into game player movements.

Master of the Universe tier

**The Art of Computer Programming** any volume. I would start with 4.1a Combinatorial Algorithms. 4.1b is out on Knuth's homepage and it contains all new math that isn't even on Wikipedia yet. The exercises are in the book for a reason, it's not just reference it's to help you understand the material so try some of them.

**Functional Differential Geometry** by Sussman. [http://groups.csail.mit.edu/mac/users/gjs/6946/calculus-indexed.pdf](https://archive.md/o/sud91/https://groups.csail.mit.edu/mac/users/gjs/6946/calculus-indexed.pdf) SICP is the gold tier for Computer Science, SICM is gold tier for Physics, and Functional Differential Geometry is gold tier for applied mathematics. This again converts equations into scheme functions. Treating data as a distribution in high-dimensional space is at the core of machine learning, and differentiating across those dimensions is typically how learning is done. There's a whole area called Information Geometry which treats the parameter spaces of statistical models as Riemannian manifolds under the Fisher information metric you'll learn in machine learning courses.

In SICM the same authors mention that a computational approach to calculus revealed errors in their own understanding of classical mechanics equations (such as Lagrange's equations), and they introduced new notation to address the problem. Functional Differential Geometry picks up that idea and runs with it, debugging general relativity and quantum mechanics.

Conclusion

This list is about learning base theory, so you can branch off and learn anything you want yourself like a formal course in Statistics [http://www.stat.cmu.edu/~larry/all-of-statistics/](https://archive.md/o/sud91/www.stat.cmu.edu/~larry/all-of-statistics/) or go into number theory for cryptography. With this foundation there is literally no course or advanced field of Compsci you can't take.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  08/16/15 (Sun) 04:10:46 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233036)[3036](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3036)

I like your suggestions.

For linear algebra I would suggest Shilov, it's a fantastic book, and published very cheaply by Dover books. Of course with all these recommendations, it is never a bad idea to read from a few different authors, some will suit you better than others.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  08/16/15 (Sun) 04:14:26 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233037)[3037](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3037)

[![](https://archive.md/sud91/e65a07e3bf5ae383b4a5dd2827c9ed0a6ab6ef9e.jpg)](https://archive.md/o/sud91/https://media.8ch.net/prog/src/1439698466301.jpg)

For probability I highly recommend this one.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  08/16/15 (Sun) 04:19:28 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233038)[3038](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3038)

\>"Advanced Calculus" which is actually easier,

I seem to remember that being the other way around.

Another alternative for calculus/Analysis is the two volume treatise by Zorich.

Of all the analysis books I could find, that one stood out to me as the clear winner, based on the breadth of coverage, and the well explained yet slick proof style.

Your millage may very.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  08/16/15 (Sun) 04:22:48 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233039)[3039](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3039)

[![](https://archive.md/sud91/0e4ea7fbbb9dde52251875bcbbfed69d43c3b8c5.jpg)](https://archive.md/o/sud91/https://media.8ch.net/prog/src/1439698968419.jpg)

Ahh, no graph theory yet. So I'll make another recommendation.

If you don't like that, the authoritative text is Diestel. Might be more difficult as a first book for a self learner.

  

Jesus Christ OP, how long would it take to read all this stuff?

(Saved the thread for future reference.)

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  08/16/15 (Sun) 04:29:36 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233041)[3041](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3041)

I'm not OP, but I added the books after his nice list.

I think 3-4 years is a good target. You'll want to read most if not all of the linear algebra and analysis texts, but as you specialize to more advanced topics, you'll just cover things that interest you.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  08/16/15 (Sun) 04:30:00 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233042)[3042](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3042)

Fuck, I posted the wrong "Advanced Calculus" book, I meant to post this so-called Honors Calculus pdf who's intro talks about how good Spivak is for self learning, and how difficult some of the problems are [http://math.uga.edu/~pete/2400full.pdf](https://archive.md/o/sud91/math.uga.edu/~pete/2400full.pdf)

Anybody else with suggestions for theory in CompSci books feel free to dump in this thread

  

I did these books after work, and during an 8 month stretch where I was living off cryptocoin arbitrage, so complete my work by 8am and had nothing to do all day. (I'd still be doing it if it wasn't for blockades put up by governments for getting money into exchanges/irc trading partners).

I spent 2-6hrs per day on each book. It took me a month to do Basic Math, as I was only doing it 2hrs per day. A week to read the other 2 prelim books, about 3 months to do Spivak's Calculus because holy shit it was hard (for me, at the time), about a month each for Discrete Math/Linear Algebra which I did at the same time as Spivak's book, so one day read/do Spivak for about 4-6hrs then do the other book(s) next day.

CLRS took me a while because I did the full MOOC online for it, I think 2-3 months. I wish I had just read the book. While doing it I started reading Concrete Math and used stackexchange to chase down things I didn't know that came up, that took me a good 4 months as it was probably the hardest book I've ever done.

Calculus on Manifolds took a month, it's small but dense and very good. I went back and reread parts of it so many times doing SICM that I can't remember how many times I've done it so let's say 2 months. SICM took awhile, because I had no physics education so had to go and research everything I came across I didn't understand. I think 4 months it took doing p/t. I'm still reading The Art of Computer Programming, I did most of 4A but then went to Vol 1 and started from beginning. I don't read the entire chapters, I skim to get a good reference then try some of the exercises or convert his pseudo-code into Typed Racket for the things I do for money these days. Building a trading engine vol 4 is gold for that.

Functional Differential Geometry I did in less than one month because I was doing it 9hrs a day, it was totally crazy fascinating (just like SICM) and I had a good solid understanding of his notation which is similar to Spivak's Calculus on Manifolds so breezed through it. Right now I'm just reading TAOCP and The Art of Software Security Assessment which is not math related but an awesome read.

Tl;DR it took me about 1.5 years to do this, but I went through some of these books at the same time and some days spent 20 mins on them and others spent 9 hrs.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  08/16/15 (Sun) 04:45:44 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233045)[3045](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3045)

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  08/16/15 (Sun) 04:48:55 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233047)[3047](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3047)

This is an amazing thread. What has prompted you to be such a fucking fantastic gentleman, OP?

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  08/16/15 (Sun) 04:49:57 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233048)[3048](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3048)

[![](https://archive.md/sud91/7b7ad87b24b9ee971b955072c48d24ea5fbfcfc4.jpg)](https://archive.md/o/sud91/https://media.8ch.net/prog/src/1439700598026.jpg)

Cool shit OP, mad respect.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  08/16/15 (Sun) 23:18:01 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233055)[3055](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3055)

There's also this gargantuan reference book, which covers almost everything in Applied Math [http://www.derivations.org/](https://archive.md/o/sud91/www.derivations.org/) written by a Debian developer.

It gives you to the point definitions of anything you may come across in computer science/engineering courses you forgot, like how Logarithms work. There's no exercises, so you won't get an full understanding of the material but good enough for "brute force learning" which means you start doing any advanced compsci course you wish then go look up any references they assume you already know, like summation or vector calculus.

  

What do you think about Introduction to Algorithms? I got that book with the hope to learn more about math however I can't force myself to read through it. Any advice on that? How does that compare to the other books?

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  08/19/15 (Wed) 05:02:38 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233070)[3070](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3070)[\>>3075](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233075)

Not the person you asked, but I think it is essential reading for any computer scientist. There's another book which gets recommended a lot

\> Robert Sedgewick - Algorithms.

I haven't read it, but I did really like ItoA. You're going to need to cover that material at some point, although it's more foundational than practical.

  

The things is that I don't understand a lot of stuff. I downloaded the Basic Math in order to clear a lot of the things I am missing and then I am going to pick up on ItoA.

I feel shame not paying attention in math class. So much wasted time.

P.S.

Finding the Basic Math by Serge Lang wasn't easy so when I found it I decided that I'll seed it for a while on kickass in case someone else wants the knowledge.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  08/19/15 (Wed) 20:04:13 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233076)[3076](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3076)

\>I feel shame not paying attention in math class. So much wasted time.

Don't. There's very little chance that you had a great teacher anyways. If the will is there, you'll repair any gaps in your knowledge.

I was once in the same boat as you, but now I've read pretty much all of the books OP listed. Math classes in school are horrible for generating motivation, so it seems little more than busy work. Besides, as a high school student there are other priorities, like getting the attention of the hot girl in the class.

Stick with it.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  08/19/15 (Wed) 20:07:08 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233077)[3077](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3077)

I've heard some good things about this book too, but I cannot attest its level of difficulty

It's Knuth though, so I'm sure it is top quality.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  08/19/15 (Wed) 21:30:28 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233081)[3081](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3081)[\>>3082](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233082)

Just type the name of the book (excluding "by" when including the author's name) and you'll find many books that aren't on torrent websites. Follow one of the mirrored links and you're pretty much set.

Btw, thanks for the guide op, I appreciate this so much.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  08/19/15 (Wed) 21:40:13 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233082)[3082](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3082)

Thanks a lot dude. I am in the process of getting my shit sorted out.

  

[![](https://archive.md/sud91/cca8f7947086f179e4ec18f89c33c20b2eb9971f.jpg)](https://archive.md/o/sud91/https://media.8ch.net/prog/src/1440079578657.jpg)

Currently going through basic math and calculus by Serge Lang. ( looking back at anything I get confused over).

Also Introduction to Functional programming with Lambda calculus.

I've also got SICP coming in the mail.

Its kinda depressing when I think about it. Having to go to college soon when I already know what I want to study and can do it on my own. B-but no I need to go into debt and have a piece of paper so I can join all the other "programmers" out of college who really don't know shit. (source: my friends)

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  08/20/15 (Thu) 20:27:27 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233086)[3086](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3086)[\>>3116](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233116)

You could do a double major in math/comsci.

Or a masters in either one of those subjects. That separates you from the average blub programmer.

  

I'm reading Basic Mathematics right now, and there's an exercise like this:

**Justify each step, using commutativity and associativity in proving the following identities.**

I don't know what is meant by "identity" here, but I get the idea of what I'm supposed to do. Trouble is I've no idea what I'm actually supposed to write down. Could someone give me an example please?

Here's the first one for example's sake:

(a + b) + (c + d) = (a + d) + (b + c)

Also, could someone tell me how to use the $$ tags? I couldn't get them to work.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  08/21/15 (Fri) 00:58:33 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233092)[3092](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3092)[\>>3097](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233097)

It's mainly moving stuff around. Since addition is the only operation in the expression, you can manipulate what's being added first :

(a + b) + (c + d) = (a + d) + (b + c)

\= (a + c) + (b + d)

\= (a + b + c) + d

\= a + (b + c + d)

\= (a + b + c + d)

\= (a + b) + (c + d)

I might be wrong but that's what I did.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  08/21/15 (Fri) 02:44:47 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233094)[3094](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3094)

\>I don't know what is meant by "identity"

An identity is any kind of transform which leaves the operand unchanged. It's a fancy way of saying both sides are equal. You could also say, "equalities".

That example you are showing is demonstrating two identities of addition which must hold in a field.

commutativity: a + b == b + a

associativity: (a + b) + c == a + (b + c)

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  08/21/15 (Fri) 06:15:31 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233097)[3097](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3097)[\>>3106](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233106)

An identity is basically an equation, except you can use it anywhere.

To prove an identity, you need to show that both sides of the equation are the same. You usually do this using expansion, simplification, and even other identities.

See below for a proof.

You've got the right idea, but that's not a proof since you're using the thing you're trying to prove to prove it. You'd get marked wrong in an exam (unless you're like me and you bitch to your professor for half marks. Needless to say I won't make that mistake again)

What you'd want is something more like:

Proposition: (a + b) + (c + d) = (a + d) + (b + c)

Proog:

Take the LHS

(a + b) + (c + d)

\= a + (b + c) + d (associative laws)

\= a + d + (b + c) (commutative laws)

\= (a + d) + (b + c) (associative laws)

Which equals RHS.

Therefore, (a + b) + (c + d) = (a + d) + (b + c) holds.

qed

I should probably also specify which mathematical objects a, b, c, and d are.

ie:

let a, b, c, d be particular but arbitrary real numbers.

\[…\]

Therefore, (a + b) + (c + d) = (a + d) + (b + c) holds for numbers a, b, c, d in the reals.

  

[\>>3090](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233090) here, is it okay to ask for more help in this thread? I was an idiot when I was younger, and I didn't pay attention in maths class. I'm trying to catch up now, but I no longer have teachers who I can ask for help.

For now I'll just ask.

The third exercise asks me to prove the identity (a - b) + (c - d) = (a + c) + ( - b - d). Here's how I did it:

Proposition: (a - b) + (c - d) = (a + c) + ( - b - d)

Proof:

Take the LHS

(a - b) + (c - d)

\= (a + (- b)) + (c + (- d))

\= a + ((- b) + c) + (-d) (by associativity)

\= a + (c + (- b)) 0 (-d) (by commutativity)

\= (a + c) + (-b - d) (by associativity

Which equals the RHS, and therefore the proposition holds.

QED

I have two questions. First, is this correct? Two, am I supposed to note what I did in each step, as I did with the last three steps, but not with the first?

Also, one of the later exercises says to "Show that - (a + b + c) = - a + ( - 6) + ( - c)." What's the difference between this and the earlier exercises where you're asked to justify steps?

What does it mean to say that variables are particular but arbitrary?

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  08/22/15 (Sat) 06:59:08 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233107)[3107](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3107)

\>What does it mean to say that variables are particular but arbitrary?

Basically just a way of saying "It works for any number". You can pick any numbers within the constraints I gave you (in my case, they have to be real numbers), and it will work for any of those.

Take the following with a grain of salt: I'm still learning myself

I'm fairly sure it's dependent on how unrestrictive the constraints are - in particular if those constraints don't refer to another variable.

You wouldn't say:

Let a and b be particular but arbitrary integers, such that a = 2b.

Though, you might say

Let b be a particular but arbitrary integer, and a be an integer satisfying a = 2b

I couldn't tell you why they word it like that, but that's how my textbooks and my professors tend to do it, so I just immitate it.

  

Can you explain your learning process?

How did you manage to completely read 6 math books that have more 500+ pages in them in less than 2 years and understand all the material :/.

  

All the while running cryptocurrency trading algos that he wrote from scratch.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  08/24/15 (Mon) 10:52:01 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233116)[3116](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3116)

\>double major in math/comsci

This is what I'm doing. I'm hoping it will give me better opportunities to do work in academic/research oriented areas, as opposed to enterprise stuff.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  08/24/15 (Mon) 19:41:31 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233119)[3119](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3119)[\>>3123](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233123)

[![](https://archive.md/sud91/c9e4522e506ad354d9f3fa98478a5f8558691b00.jpg)](https://archive.md/o/sud91/https://media.8ch.net/prog/src/1440445291681.jpg)

I'm on page 40 in Basic Math and I feel like an idiot.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  08/25/15 (Tue) 11:42:09 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233123)[3123](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3123)

Be sure to practice questions. Don't just read or you won't learn half of it. Also, it often helps to get it explained in different words - khanacademy is pretty good for that. He explains it and then goes through a couple examples.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  08/25/15 (Tue) 23:28:54 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233128)[3128](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3128)[\>>3133](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233133)

\>I have two questions. First, is this correct? Two, am I supposed to note what I did in each step, as I did with the last three steps, but not with the first?

\>Also, one of the later exercises says to "Show that - (a + b + c) = - a + ( - 6) + ( - c)." What's the difference between this and the earlier exercises where you're asked to justify steps?

Could someone please help me with these?

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  08/26/15 (Wed) 18:58:46 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233129)[3129](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3129)

Maths books .pdfs:

Of varying skills levels. Share any you have there.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  08/26/15 (Wed) 20:51:05 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233130)[3130](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3130)[\>>3132](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233132)

Found one of the books mentioned in OPs post on /freedu/, Basic Mathematics by Serge Lang. I'm posting it in this thread so you guys can check it out. If you find any other books mentioned in this thread, make sure to post 'em and share 'em around.

Big thanks to the Anon on /freedu/ for finding this.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  08/26/15 (Wed) 20:56:41 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233132)[3132](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3132)[\>>4356](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234356)

Unfortunately the PDF will not upload here, so I've uploaded the book to the following link:

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  08/27/15 (Thu) 03:19:37 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233133)[3133](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3133)

The first step seems to just be a definition. In other words a - b is short hand for a + (-b), or at least that's how the book seems to do things considering one of it's examples.

Maybe you don't have to keep everything on the same side and can add the minus of the LHS to the right one. He does that in some of his earlier examples, and it would make sense since -(a + b + c) doesn't seem as easy to use as (a + b + c).

Or you could use No.4 or No.5.

I want to say you can't really do it with just associativity and commutativity since -(a + b) only makes sense based on (a + b). They proved -(a + b) = -a - b by adding (a + b) to both sides and getting everything to zero, which I'm pretty sure uses more than associativity and commutativity (axioms involving zero)…I think.

It's funny how adding numbers can be so hard, while taking derivatives is easy as fuck.

Math's weird

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  08/29/15 (Sat) 12:20:32 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233156)[3156](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3156)

[![](https://archive.md/sud91/989b45d75d3bd7ba3e3a57c72b634950fcc83554.jpg)](https://archive.md/o/sud91/https://media.8ch.net/prog/src/1440850832646.jpg)

This thread is gold and deserves to be stickied.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  08/30/15 (Sun) 19:03:33 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233168)[3168](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3168)[\>>3169](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233169)

[![](https://archive.md/sud91/8036bce2adc34b09f8cae811442f6041ffae19f1.jpg)](https://archive.md/o/sud91/https://media.8ch.net/prog/src/1440961414131.jpg)

My day was done pretty quick. The trading algos were not incredibly difficult, simple arbitrage. I would trade say $5,000 on one site one day then sell it on another, pocket typically $200-400 depending on spread that day. Sometimes this took 10m and other times a few hours trying to sell a large amount. Either way I had a lot, lot of time to read and do exercises. I didn't look at reddit, HN, chans or any news RSS time sinks I just worked.

I flew through most of the books except the exceptionally dense books, like Knuth's Concrete Math that was a hard read. TAOCP is an exceptionally hard read too in terms of density of information. I also read some other pdf's not included here like an abstract algebra honors book from a Florida university I found.

I did the exercises in stages, for example I would do chapter 1 X amount of exercises, so 5 out of 20 exercises. Then read chapter 2. Then go back do a few exercises in chapter 1 I missed, such as 5 more exercises. Then repeat this for every chapter I read.

The result is you maintain a solid understanding of the material all the way through the book so don't forget anything since you constantly review basic concepts, and I could burn through the material that way, and didn't need to spend additional time reviewing by re-reading chapters.

tl;dr this gets easier as you go. In the beginning everything is very foreign and dense, hard to work through. Half way through you develop solid "mathematical maturity" so it's no longer a slog and can casually read and write proofs on a commuter train or sitting in a starbucks.

Nick Bostrom, who wrote Superintelligence (an excellent book on dystopic AI) said he listens to university lectures at double speed while working out using VLC to prevent them having "mickey mouse voices". Our day is full of wasted time, once you start taking advantage of all the time you waste this will be no problem to accomplish, probably faster than me as I wasted lot's of time.

Bill Gates read TAOCP just 20 minutes a day but he stuck to that daily schedule to finish it. Small improvements accumulate into large improvements rapidly because daily action provides "compounding interest." Pic of this post is an excellent Soviet era mathematician survey book of the entire field of mathematics providing you with clear explanations at a high level if you're having problems with a subject. I also used The Princeton Companion to Mathematics to quickly review something if it wasn't making sense to me in the textbook I was reading.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  08/30/15 (Sun) 19:06:21 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233169)[3169](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3169)

Forgot to add, you do not need to read the whole text if you don't want to. You can look up courses on MIT Open Courseware (such as, Linear Algebra) and just read their lecture notes and do their assigned reading out of the book for bare minimum effort to learn a subject good enough to be adequate at rolling your own algorithms or understanding math concepts. There's no need to do every single chapter unless you're interested in it like I was

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  08/30/15 (Sun) 20:33:46 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233172)[3172](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3172)

The answers are in the back of the book for some questions. An identity is a relation that means that whatever the number or value may be, the answer stays the same. You can also start with Lial's Basic College Mathematics, it's a little more clearer than Lang's book as he assumes you know identities. I'll attempt to attach it to this post if not this (spammy, use ublock origin/adblock) link has it [http://www.uploadable.ch/file/uBDeWscyUnRV/d3mlr.Basic.College.Mathematics.9th.edition.pdf](https://archive.md/o/sud91/www.uploadable.ch/file/uBDeWscyUnRV/d3mlr.Basic.College.Mathematics.9th.edition.pdf)

Lial's book covers even earlier stuff, like fractions which I had forgotten. Associative laws will come into play when you do Linear Algebra later and learn Rings.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  09/07/15 (Mon) 09:21:32 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233212)[3212](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3212)

[![](https://archive.md/sud91/b03e227cf594451078bd70221adf79ea694002ee.jpg)](https://archive.md/o/sud91/https://media.8ch.net/prog/src/1441617692585.jpg)

Some really great material around here, thanks OP.

I'll personally recommend, added to all that, Introduction to the Theory of Computation by Michael Sipser, it's a really pricy book so pirate it (I've had the chance to found mine on a yard sale).

It is really dense and high-level, so it is in the berzerk tier of the topic, and cover a lot, lot of material, from finites automatas to context-free grammars, necessary to be a great programmer.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  09/12/15 (Sat) 16:52:31 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233248)[3248](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3248)

[![](https://archive.md/sud91/af612b59746efa6e1833db81eae686780f19ab96.jpg)](https://archive.md/o/sud91/https://media.8ch.net/prog/src/1442076751686.jpg)

Thanks for stickying this thread mods.

Also OP, thanks a lot for posting Serge Lang's book it has actually been extremely helpful.

  

My question is. When it's too late? I'm 25 years old, almost 26. Also I have to go to work (7-8) hours a day. I'm no lifer (not bitter about that) so this can(?) be an advantage. Do you think I can make it? My main interest are algorithms. I would skip that hard mathematical stuff like those differential things. I have some rusty knowledge of high school math (I can easily solve equations, quadratic theorem, I know about sets and operations with it, equality and ordering relations, basic vector calculus, also I can integrate and derivate… but not in 'proofs' way, I just have more practical, rote knowledge. Thanks for answer, anybody.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  09/25/15 (Fri) 03:18:09 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233277)[3277](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3277)

its not too late m8 but you do need to understand how to do some basic logic and proof to understand certain algorithms involving trees and asympotic analysis, etc

I dont know you or how self-motivated you are so I cant say whether or not you can make it but start learning and programming in your off time and youll figure that out. It never hurts to try.

also muh dubs

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  10/01/15 (Thu) 07:46:59 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233306)[3306](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3306)

What scheme implementation is better for SICM and Functional Differential Geometry?

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  10/01/15 (Thu) 08:56:09 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233307)[3307](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3307)

Programming mathematics yet no type theory, nor cat theory?

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  10/04/15 (Sun) 00:41:34 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233324)[3324](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3324)

It's not too late, but you need to be willing to put the work in. What's there to lose?

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  10/05/15 (Mon) 13:19:20 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233330)[3330](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3330)[\>>3346](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233346)

Cross posting since this board better fits.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  10/06/15 (Tue) 02:00:54 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233343)[3343](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3343)

[![](https://archive.md/sud91/8a2662eb50224a5ac38247a6ebef11e7a855f79a.jpg)](https://archive.md/o/sud91/https://media.8ch.net/prog/src/1444096854768.jpg)

Going through SICP and I forgot how into math, whoops :^)

Thanks for the resources.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  10/06/15 (Tue) 18:29:41 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233346)[3346](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3346)

\>Is SICP wrong here? Isn't A(0,0) supposed to be 1 and not 0

How so?

(A 0 0) means that (= y 0) holds and thus the function returns 0. Or am I missing something?

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  10/09/15 (Fri) 04:22:31 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233366)[3366](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3366)[\>>4256](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234256)

[![](https://archive.md/sud91/dc57c5e3064109284ba5f8df6b15ccc659cccf3a.jpg)](https://archive.md/o/sud91/https://media.8ch.net/prog/src/1444364551293.jpg)

I can provide some advice on learning mathematics

\>"I failed maths in high school, what do I do?"

High school maths education is basically a joke, and everyone who uses advanced maths regularly can agree that this is true. You have unmotivated teachers who have never done advanced mathematics teaching you to rote learn and memorize things for the sole purpose of getting good grades in an exam. That's not how you learn maths. If you didn't do well at maths in high school then it's okay, anyone who isn't a complete dumbass can learn maths properly as long as they put enough time and effort into it.

\>Don't be discouraged if you don't understand something

This stuff takes effort to learn, and you need to have the mindset that you are willing to try and understand things that you don't understand at first. If you come across a mathematical concept or a problem that you have difficulty understanding or doing it, don't tell yourself "I'm stupid, I can't understand this, I should just give up". Think about it for a while and try to understand it, and eventually you will understand it.

When you're struggling with something, this is when your mind really starts to expand. It's just like lifting weights, you can't get stronger if you lift pussy weights that are easy for you to lift, you need to lift heavy shit that's challenging for you and keep lifting heavier and heavier over time, and your body will adapt by making you stronger and you'll make sick gainz. Similarly with any kind of intellectual pursuit, you aren't going to get smarter by doing things that are easy, you need to struggle with concepts or problems, that's the only way you'll get smarter and improve your creative problem solving skills.

\>Focus on proofs and/or problem solving, not computation

Doing proofs will make sure you really understand the mathematical concepts, rather than just doing a blind calculation without understanding what you're doing. You can also do problems that aren't proof-based, but they still require you to figure out an outside-the-box solution instead of following a memorized procedure. You can always use a computer to do computational mathematics (buy or pirate software like Mathematica), doing it without a computer isn't going to help you.

\>It's better to do a few hard problems rather than doing a lot of easy problems

Find good problems that are challenging for you to do, and spend time doing them. If you have a good textbook, it should be filled with challenging problems, or do a google search to find hard problems. You can also do past Putnam exams. The Putnam Competition is an undergraduate mathematics competition known for being ridiculously difficult. Even some of the world's leading mathematicians can sit the exam and be unable to solve a single problem. The thing that makes these exams useful for getting better at maths is that they typically don't require that much background knowlege of maths, a lot of problems don't even require you to know calculus, but these problems will still be very challenging and will build your creative problem solving skills like a motherfucker. Here's a link to an archive of these exams: [http://kskedlaya.org/putnam-archive/](https://archive.md/o/sud91/kskedlaya.org/putnam-archive/)

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  10/12/15 (Mon) 16:20:46 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233421)[3421](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3421)

I majored in MIS and got a nice 70k after graduation. But it was only because of previous internship experience. Take some internships along with your courseware and you'll do fine. Save up form the paid internships and you will get both experience and money saved up to pay of your school loans.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  10/15/15 (Thu) 01:49:01 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233427)[3427](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3427)[\>>3438](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233438)

[![](https://archive.md/sud91/45a79ed8b539c770ec291e1b2ae12a219fe36099.jpg)](https://archive.md/o/sud91/https://media.8ch.net/prog/src/1444873742014.jpg)

What is depressing to me is that I am about to graduate in CS and the school I went to taught no math and basically any theory. Oh, and it didn't teach practical stuff that well either.

I really want to not work for a year and just study these books and stuff. They look awesome.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  10/17/15 (Sat) 02:21:41 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233438)[3438](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3438)

On what school did you go ?

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  10/18/15 (Sun) 01:28:24 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233440)[3440](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3440)[\>>3452](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233452)

If someone know where to torrent Linear Algebra by Friedberg, Insel and Spence ; it's nowhere and that shit expensive

  
  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  10/20/15 (Tue) 18:02:09 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233453)[3453](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3453)[\>>3474](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233474)

Thanks you so much but the quality is bad, where do you think I can have something better ? I have troubles reading

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  10/26/15 (Mon) 01:52:10 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233474)[3474](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3474)[\>>3482](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233482)

Does anyone know of a good introduction to vector algebra? I'm trying to learn the basics.

Use this search engine

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  10/27/15 (Tue) 13:29:03 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233480)[3480](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3480)

Try Algorithms Unlocked. It's by one of the authors of CLRS, but a bit easier.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  10/27/15 (Tue) 13:31:42 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233481)[3481](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3481)

I know OP prefers books but this was pretty good, you can download the videos if you want:

  
  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  11/06/15 (Fri) 22:10:28 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233543)[3543](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3543)

I just checked the book you said you had trouble reading. It's a djvu file, and it's actually better quality than most pdf scans. You need a djvu reader, try sumatrapdf on windows.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu") tfw u dont knw where to get fucking ebooks from Anonymous  11/13/15 (Fri) 00:13:39 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233572)[3572](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3572)[\>>3640](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233640) [\>>3642](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233642)

can anyone post fucking torrent or other links to download these books?

  

I must disagree strongly with giving Basic Mathematics by Lang as first book for those who start.

While it is a great book, it is not a book for beginners and/or those who are not gifted.

When I started it was useless since I didn't have a gift for math nor I had the proper preparation and ability to manage it.

A great book to start instead is Algebra & Trigonometry by Sullivan, since:

\>you only need to be able to do the basic operations and know like what is a triangle and a square

\>it has been made to teach normal, ungifted people

\>it has a lot of exercises made to learn and practice with solutions in the back

\>it has extensive and detailed coverage of almost all math needed for pre-calculus

\>you can pirate it

After I did that book I was able to understand and learn something from Lang. Despite the name, it is not a book for beginners.

I noticed that many of this guides online on programming/math always advise people to get the "best book", where "best" is the "best" for people who already know/are gifted and not best as in best for normal people and beginners.

  

What do you think of Stewart's 'Precalculus'? I recently started it and I intend on completing the whole book so I can patch up my shitty high school math knowledge

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  11/19/15 (Thu) 18:26:03 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233604)[3604](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3604)

I guess it is similar to Sullivan's Algebra & Trig (or Sullivan's Precalculus, which is pretty similar to A&T with just some differences in chapters).

I've done the whole Algebra & Trig, it worked for me: I didn't find any mistakes in the book's answer key (very important for self-study), that's why I advised that book.

I had to go online from time to time to understand some concepts better, but that's that.

Of course, there are probably other books that are just as valid.

The important thing I think is to have book that is made for normal people going to college, that covers almost all the arguments, and has a lot of exercises and grunt work.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  11/22/15 (Sun) 00:24:31 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233619)[3619](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3619)

\>I must disagree strongly with giving Basic Mathematics by Lang as first book for those who start.

This.

I hate to be the one to discourage but the presented study material is way, WAY beyond the mental capacities of any average person. You seriously need to be principally gifted in mathematics to be able to work through something like concrete math or the Spivak textbook.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  11/26/15 (Thu) 04:17:50 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233637)[3637](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3637)[\>>3643](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233643)

which version do you reccomend? I'm planning on buying a used copy soon

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  11/26/15 (Thu) 21:58:30 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233640)[3640](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3640)[\>>4208](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234208)

ok FBI over TOR:

books.google.com

  
  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  11/27/15 (Fri) 18:56:05 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233643)[3643](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3643)

I used the 9th edition.

Usually this kind of books don't have many differences between editions, but sometimes they skip putting the answers in the book between editions, so make sure the book you get has the answers to odd-numbered exercises.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  12/03/15 (Thu) 13:31:52 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233673)[3673](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3673)

Thank you immensely for all this advice and the good books.

Just a question: you linked youtube classes along with the Discrete Math book but apparently while the book is from Michiel Smid's and based on his second-year

course COMP 2804 (Discrete Structures II), the Youchoob lectures are from his colleague John Howat COMP 1805 (Discrete Structures I).

Since I have no formal education on the subject I'll just start with the lectures and related material on Howat's website, but I assume you linked Michiel's book because it is his more adv topics that should be studied?

  

Khan Academy, up to Algebra II (1d-3m)

Stewart's Calculus, 1ch-2ch/d odd & 7/d review

How to Prove It

Spivak's Calculus

Calculus On Manifolds (3m-4m)

Strang's Linear Algebra and Its Applications

Apostol's Calculus, vols. 1-2

Foote's Abstract Algebra

Lay's Linear Algebra and Its Applications

Baby Rudin (2m-4m)

Papa Rudin (6m-1y)

\[2y\]

  
  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  12/26/15 (Sat) 07:39:29 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233765)[3765](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3765)

\>been browsing /g/ weekly for years

\>no /g/ on front page

\>search for "tech"

\>before hitting link, realize I don't actually want to see threads about hardware

\>search "computer science", no results

\>search programming

\>/programming/

\>right before clicking, notice total posts and pph counters

\>/prog/ highest in all stats

\>sticky on front page is a thread about the topic I've been most concerned with for the last few months: ACTUAL COMPUTER SCIENCE

Definitely going to keep coming back here

\>do a search for perl

\>3 hits

This board. You guys. I needed you

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  12/26/15 (Sat) 07:40:32 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233766)[3766](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3766)

\>Why would you want to learn math? Because it will change your thinking.

Literally what I've been thinking for the last half a year or longer

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  01/04/16 (Mon) 23:55:12 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233808)[3808](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3808)

[\[pop\]](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23)YouTube embed. Click thumbnail to play.  
[![](https://archive.md/sud91/3d9344f0222885553abc3f308087a5e57e838dcd.jpg)](https://archive.md/o/sud91/https://www.youtube.com/watch?v=1973FK47m40)

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  01/04/16 (Mon) 23:56:03 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233809)[3809](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3809)

\>Baby Rudin (2m-4m)

\>Papa Rudin (6m-1y)

  
  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  01/06/16 (Wed) 09:29:53 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233819)[3819](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3819)

I didn't mean to post that.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  01/06/16 (Wed) 21:12:38 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233823)[3823](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3823)[\>>3858](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233858)

I have the same problem as you, I don't even understand the first few pages with the proofs. I'm downloading Sullivan rn as you recommended.

I'll post results if you guys want.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  01/20/16 (Wed) 22:20:49 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233858)[3858](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3858)

would love too, I'm college right now at year and half for getting my BS thus i feel pretty ignorant on maths and plus in my curricular agenda, i dont get any progamming subject and im applying for electronic and telecoms carrer, i do understand some of the basis when it comes to electronic,electrical and telecoms but i do really want to program, i have this goal in my head since highschool, i don't want to be hax0r or anything i just want to be able to code, understand it, and develope shit… so I'm going to start with this guide too and see where it leads at the end hope the treath is still alive, also i want to learn on i2p stuff since I have some basis on the network field, can someone just help me out on pointing the right direction on where should i just start on i2p

thanks in advanced.

English it ain't my native tongue so i hope i made myself clear, and thank you OP for the guide!

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  02/09/16 (Tue) 06:49:39 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233921)[3921](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3921)[\>>3960](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233960)

[![](https://archive.md/sud91/47d4261295a6ec6b88da67d616fd14d49890d3ce.jpg)](https://archive.md/o/sud91/https://media.8ch.net/prog/src/1455000579755.jpg)

OP, you talk about trading algo on crypto markets. Is there any other ways of making legit money online like this? I can only think of selling 0 days at the moment.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  02/17/16 (Wed) 05:44:05 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233960)[3960](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q3960)

Cryptocoin trading is still sort of profitable, even if mining isn't that efficient anymore. The 2013 bubble burst seriously proved the doubts of Bitcoin's critics.

I would advise browsing some forums and reading up on economics, if you're new to the field that is. Other than reselling clearance stuff/auctioning off your weebshit there aren't many other (legal) get-rich-quick schemes.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  04/16/16 (Sat) 11:23:07 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234123)[4123](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4123)

[![](https://archive.md/sud91/64382a546384b572caab27cc52e3ff6c8a2d1cfe.jpg)](https://archive.md/o/sud91/https://media.8ch.net/prog/src/1460805787164.jpg)

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  04/17/16 (Sun) 21:35:32 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234131)[4131](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4131)

Thank you for this godly thread, OP.

18 y/o NEET here. Everyone at the GED test center just said "you should go to community college!!!!11one" Hahaha, **no**.

I dropped out of HS 'cause I sure as hell wasn't getting anywhere. Even if I _did_ make it to the best public uni in my state (extremely unlikely), my loaded grandparents would have to dig into their savings just to put me through 4 more years of hell.

Fuck that. I'll become a wizard on my own time, my own terms.

Besides, I'm a weeb and need plenty of time to study Nipponese. :^)

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  04/22/16 (Fri) 12:06:31 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234139)[4139](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4139)

I'd just like to say thanks a lot OP.

I'm a junior offering Computer Eng. and all the maths I have ever done, I've done mechanically and not because I had some level of understanding of what was going on in the background. I plan on going through the books to hopefully remedy this.

Just out of curiousity, what are you up to these days?

  

Holy shit, I feel like a fucking retard.

I'm stuck on exercise 1 of simple mathematics.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  05/17/16 (Tue) 06:10:15 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234207)[4207](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4207)

Took me a few hours, but I made it to the chapter about divisions.

Nice book OP

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  05/17/16 (Tue) 06:26:01 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234208)[4208](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4208)[\>>4209](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234209)

I dont get you 2 getting hostile, anon raised a fair point

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  05/17/16 (Tue) 06:33:45 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234209)[4209](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4209)

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  05/19/16 (Thu) 04:04:21 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234211)[4211](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4211)

On Basic Mathematics, can anyone explain me this:

Question:

```
d) Show that if n is a positive integer at most equal to m, then(:)+(„-O'C”: O'8.
```

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  05/19/16 (Thu) 04:05:23 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234212)[4212](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4212)

welp uhn, exercise 7, letter D, pages 55-56.

Answer is on page 453

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  05/21/16 (Sat) 05:53:07 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234221)[4221](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4221)[\>>4223](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234223)

I get you, bro. I was never taught any proper mathematics, I just memorized what to do when I saw something , pressed the buttons on the calculator and prayed to God I passed.

How was your math education?

Anyone else going through these books?

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  05/21/16 (Sat) 23:01:58 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234223)[4223](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4223)

\>I get you, bro. I was never taught any proper mathematics, I just memorized what to do when I saw something , pressed the buttons on the calculator and prayed to God I passed.

I used to love math up until highschool, where I stopped understanding shit and everything became "hurr just memorize X, Y and Z and you'll get into a good college".

I started hating math at around that time, it didn't help that I have social anxiety and thus asking anything to the professor was highly difficult at first, and then became fucking impossible later.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  06/02/16 (Thu) 20:33:16 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234256)[4256](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4256)

\>High school maths education is basically a joke, and everyone who uses advanced maths regularly can agree that this is true. You have unmotivated teachers who have never done advanced mathematics teaching you to rote learn and memorize things for the sole purpose of getting good grades in an exam. That's not how you learn maths. If you didn't do well at maths in high school then it's okay, anyone who isn't a complete dumbass can learn maths properly as long as they put enough time and effort into it.

To be fair this is how children learn best by being drilled. Thats why the strategy changes after high school. I had phds teaching me math in college who would give you hand written packets of problems in order to force you to think. And theyll say no fuck that just drill kids.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  07/05/16 (Tue) 01:14:24 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234317)[4317](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4317)

I want to learn about category theory and hypergraphs. What are the best/simplest resources for a beginner?

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  07/29/16 (Fri) 12:51:37 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234343)[4343](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4343)[\>>4344](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234344)

Thanks for one of the best threads out there.

I'm working through Lang's Basic Mathematics, I feel like I have a much firmer grasp on the basics now, but there was one linear equation that absolutely stumped me, even when I come back to it a chapter later.

Would anyone far more skilled than I mind going through the steps of intuition you took to solve this?

```
 (1/2)x - (2/3)y + z = 1x - (1/3)y + z = 02x - (1/3)y + (2/5)z = 1
```

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  07/30/16 (Sat) 12:03:22 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234344)[4344](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4344)

I belive the second equation is x - (1/5)y + z = 0

Anyway, what I did when solving these was:

\- for all equations: put every term under the same denominator; you DON'T need to put ALL of the equations under the SAME term!

\- now you can get rid of the denominators by multiplying both sides of the equalities by that same amount

\- now solve like any other systems of equations, i.e., try to get some term to have the same quoefficient as the corresponding term for some other equation, e.g. for x == 2x, you have to multiply by 2, however, don't forget you have to multiply the WHOLE equation by 2 to maintain equality, not just what you feel like…

Proceeding like this should lead you to the answer. If you are having trouble, try to work out things in small steps, say, start with 1 equation with 1 unknown, then 2 equations on 2 unknowns, and so forth, or something like that.

Don't sweat it, those last few exercises on S.Lang's chapter on 'Systems of Equations' are not demanding at all, but require that you go through some long computations, which can be boring and tiresome, so take your time, and if you can't solve it today, give it another try tomorrow, but don't stop reading the rest of the book just because of that exercise!

This was more of an hint than my 'steps of intuition to solve' the problem I guess, but that should do the trick if you were able to do every other exercise on that chapter.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  07/30/16 (Sat) 20:06:01 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234345)[4345](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4345)

OP you are fantastic. I just fished myself out of a massive anxiety slump because of your advice. I've started jogging, doing weights and more importantly, reading again because of your advice. You are a Legend

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  08/10/16 (Wed) 13:19:02 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234356)[4356](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4356)[\>>4435](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234435)

Thank you so much for uploading this. It's a bitch to find.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  09/22/16 (Thu) 15:22:20 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234427)[4427](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4427)[\>>4428](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234428)

"Assume that every positive integer can be written in one of the forms 3k, 3k+1, 3k+2 for some integer k. Show that if the square of a positive integer is divisible by 3, then so is the integer."

Also, how to prove this corollary "Let a be a positive integer. If a^2 is even, then a is even. If a^2 is odd, then a is odd"?

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  09/24/16 (Sat) 07:22:13 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234428)[4428](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4428)

For the first out, write out the square of 3k, 3k+1 and 3k+2 and see if they match the defintion of "divisible by x".

For the second one, write out the numbers according to the defintions of even and odd, and then square them.

I'm assuming even and odd are defined as "numbers which can be written as 2k (+ 1)", but if it isn't match it according to that definition.

There isn't much of a trick here. It's just paying close attention to the definitions and writing out what that means.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  09/30/16 (Fri) 14:27:39 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234435)[4435](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4435)

Here's a magnet link to the same book, in case it goes down

magnet:?xt=urn:btih:3aa376ce46367b879316e8f0a4bc03857da4997a&dn=Serge%20Lang%20(1971).%20Basic%20Mathematics.%20Reading%2c%20Mass.%2c%20Addison-Wesley.pdf&tr=udp%3a%2f%2ftracker.openbittorrent.com%3a80%2fannounce

checksums match

  

Page 79, basic math:

Let E be an abbreviation for even, and let I be an abbreviation for odd.

We know that:

E + E = E

E + I = I + E = I

I + I = E,

EE = E

II = I

IE = El = E .

a) Show that addition for E and I is associative and commutative.

So…

2n + 2m + 1 = (2m + 2n ) + 1

(2m + 2n) + 1 = 2k + 1

(k = mn)

As far as I know, the commutative property is unnecessary here. So does Lang want me to use it anyway, or am I misunderstanding the question?

Show that j E plays the role of a zero element for addition. What is

the additive inverse of E l What is the additive inverse of J?

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  12/05/16 (Mon) 04:49:16 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234488)[4488](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4488)

Perfect library resource site for anyone looking for these books. (Has torrent and direct downloads)

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  01/06/17 (Fri) 10:48:54 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234534)[4534](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4534)

[![](https://archive.md/sud91/a69f8a3fdf4f110f4df071b6f9bae20c3f50d6a7.jpg)](https://archive.md/o/sud91/https://media.8ch.net/file_store/aa694d383434fc01e1ea1c956d4833eae595ced83398b52cba3bda85c9d0acfc.jpg)

At least you didn't do law/finance

Kill me.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  01/06/17 (Fri) 15:58:31 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234535)[4535](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4535)[\>>4536](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234536)

\>459

\>Page 79, basic math:

\>Let E be an abbreviation for even, and let I be an abbreviation for odd.

\>We know that:

\>E + E = E

\>E + I = I + E = I

\>I + I = E,

\>EE = E

\>II = I

\>IE = El = E .

\>a) Show that addition for E and I is associative and commutative.

I'm currently on this exercise myself, but I've tried to show the properties without using the 2k and 2k+1 forms for even and odd, but instead work from the set of basic identities he writes that 'we know'. Not sure which approach is intended.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  01/06/17 (Fri) 17:38:11 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234536)[4536](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4536)[\>>4540](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234540)

I don't think you should use the 2k+1 and 2k forms, since then you're basically abusing the fact that the addition and multiplication of the integers is already associative and commutative.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  01/07/17 (Sat) 13:46:34 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234540)[4540](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4540)[\>>4545](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234545)

That's what was a little dissonant about using the 2k\[+1\] forms for me too!

My method of showing was to brute force show that associativity and commutativity holds for short strings of terms, and then argue that since it holds for the short strings, it must hold for longer strings because the longer strings contain shorter strings. (PROPERTY holds for any two terms, then it must hold for any longer string of terms because you can always use PROPERTY on two neighbours (because two neighbours is string of two terms), and thus get the desired change in expression one step at a time).

I'm at once fairly sure there must be a more elegant way to show the properties, but the way I did didn't feel like a total kludge either :)

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  01/08/17 (Sun) 17:04:53 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234544)[4544](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4544)[\>>4573](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234573)

Fuck, I dont know who I want to be anymore. Few months ago I have decided to be an computer scientist and started to read SICP, some math books, bought Arduino. And about a week ago I realised that I really want is to make games, I started to learn how to draw, play around in GameMaker. And now I have no idea in which way to proceed, cs or gamedev.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  01/08/17 (Sun) 17:50:28 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234545)[4545](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4545)

\>then argue that since it holds for the short strings, it must hold for longer strings

If you mean that you've proven that a+b=b+a implies a+b+c+d+e+f=a+f+c+b+d+e=… and so on, then I think that was redundant. To prove that some operation is commutative, you literally only have to show that a+b=b+a for all a, b in your set, since that is the definition of a commutative operation. Of course, it implies a+b+c+d+e+f=a+f+c+b+d+e=…, but that is irrelevant.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  01/13/17 (Fri) 15:32:19 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234548)[4548](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4548)[\>>4552](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234552)

Okay, doing the exercises for Basic Math takes a shitload of paper and space.

Would it be okay to do the exercises on something like notepad, or would doing the exercises on paper be better?

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  01/18/17 (Wed) 15:29:56 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234552)[4552](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4552)

You can write your exercises however you'd like, but you'll probably need to use scratch paper at some point.

If you're up to it though, you could try doing the math in your head.

Maybe get a small whiteboard? Or you could use a tablet.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  02/10/17 (Fri) 05:54:08 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234573)[4573](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4573)

You can transfer your prog skills into gamedev easier than the other way around.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  03/06/17 (Mon) 14:48:47 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234607)[4607](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4607)

this is pretty good and there are even videos of the lectures.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  03/10/17 (Fri) 07:37:38 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234610)[4610](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4610)[\>>4613](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234613)

holy shit, what a find with SICM. Why the fuck isn't that in the /sci/ wiki?

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  03/10/17 (Fri) 07:38:04 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234611)[4611](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4611)[\>>4613](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234613)

oh, and does anyone know if a video lecture series exist for SICM too?

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  03/10/17 (Fri) 07:40:07 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234612)[4612](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4612)[\>>4613](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234613)

op your killin it with the dank sussman scheme books, i'm hard as a fuckn rock right now shit sounds so dope

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  03/10/17 (Fri) 08:23:37 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234613)[4613](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4613)[\>>4641](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234641)

Samefag here, requesting OP ,>>3034, shed some light on how I can make that much money while putting in so little time each day. I've always wanted to get into cryptos. Would you be willing to host a similar thread on /biz/?

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  03/11/17 (Sat) 19:11:33 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234617)[4617](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4617)[\>>4618](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234618)

the link for functional differential geometry by sussman no longer works, can someone link to a seed / download?

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  03/11/17 (Sat) 19:14:49 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234618)[4618](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4618)

  

[![](https://archive.md/sud91/f8cb39e9497828192d46f013f68ff2d69029711c.jpg)](https://archive.md/o/sud91/https://media.8ch.net/file_store/cdb603ad0b544e31ece78e839a84c609483a25d182c2303e0ad4c2a902b24803.jpg)

So I originally wrote this kek. I apologize for this cringey post I think I was liquored (and had far less math experience).

In those many years I have developed a much better curriculum if anybody is interested that eliminates all noise and is pure signal. I also tailored it for somebody who knows absolutely nothing about Math since I started with half-highschool knowledge.

This is shit I wish I knew 2 years ago I would've saved a bunch of time instead of trying to figure out Spivak's manifolds book which is entirely difficult btw and would've been better if I had spent time building up abstractions in algebraic structures instead.

These days I am a researcher at a medical university because there was nobody local to hire for parallel algorithms research so they hired me.

Tip for anybody doing this, the books look difficult and long, but once you reach a certain level of mathematical maturity you can easily just skip whole chapters on review and just concentrate on the actual new information which often is just 2-3 chapters. That's how researchers can plow through so many books like a guy I work with who read several Category Theory books and papers in just a week. He really only read half a book because he had arrived at a level where he could confidently intuit mathematics having built all the necessary rigorous foundations.

  

I abandoned bitcoin a while ago due to numerous issues too long to get into here now I'm all about Zcash [https://z.cash/](https://archive.md/o/sud91/https://z.cash/) primarily because of the team of crypto experts who put it together.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  04/19/17 (Wed) 20:29:12 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234651)[4651](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4651)[\>>4652](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234652)

Personally, I like your layout a lot more I really dislike having to sign up for so much stuff through the link I provided, yours seems like a nice cut and dry approach that puts the readers nose straight to the books. I'd be very interested to hear your opinion on how they might compare though. Right now I'm almost ready to starting diving into analysis, but my CS and programming side of things is very weak.

\>I am a researcher at a medical university because there was nobody local to hire

Really interesting bit here. Good for you anon, an inspiration.

\>z.cash

Do you make money off it like you did in the other post you described? I have free time, but use it mainly to study, not make money. I'd love something that allows me to make money remotely while not having to put in many hours.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  04/19/17 (Wed) 20:33:24 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234652)[4652](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4652)

Just to expand on my background a little bit, I've gone through half a Discrete Structures book as well, so after I finish these (currently in Vector Calc and second half of Discrete Structures) I was going to start a Linear Algebra and the Intro to Algorithms book, and finally actually get through SICP. I've got to work on my programming skills…

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  04/23/17 (Sun) 00:45:23 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234657)[4657](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4657)[\>>4658](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234658)

why did you take SICM u nigger

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  04/23/17 (Sun) 05:30:48 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234658)[4658](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4658)[\>>4659](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234659)

AND you took out Sussman's Functional Differential Geometry? Together with SICP these were your coolest books, why remove them from in an attempt to "improve" curriculum?

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  04/23/17 (Sun) 05:31:34 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234659)[4659](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4659)

fiy I'm copying your curricular , adding those two books, and renaming it my own unless you beat me to it

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  04/27/17 (Thu) 18:09:06 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234664)[4664](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4664)[\>>4665](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234665)

If you ever do get around to responding, leaving an email or some contact info would be stellar, I've got a few questions regarding the functionalcs curriculum.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  04/27/17 (Thu) 18:09:20 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234665)[4665](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4665)

Questions and torrent request, that is

  

[![](https://archive.md/sud91/c1e2d8a8102abfba8097dad4a914bc4b22b0fee6.jpg)](https://archive.md/o/sud91/https://media.8ch.net/file_store/3aff9644e2dddfad21f197563a58881e0ee00a85cbcb7cd7e672e2c0a4e608de.jpg)

Wait a feckin minute…I had the screencap of the OP in my "stuff to do before I die" folder, and now you're saying this version is bullshit and made a new one?

I'm confused, shall I diss CLRS, Concrete Math, the Sussman books and co?

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  04/29/17 (Sat) 18:05:54 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234667)[4667](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4667)[\>>4668](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234668)

Not OP, but I wouldn't ditch CLRS, Concrete Math, or the Sussman books.

The other link seems more organized and structured, but reading more books will only help. I imagine CLRS, Concrete Math, and the Sussman books cover similar content to books in the functionalcs link, at some point or another, at which point you could simply skim over whichever one it is you're reading. So, you're likely safe to go about it either way (meaning read CLRS and such first, then go through functionalcs, or vice versa).

More important than sweating the small stuff is making progress, so I wouldn't sweat it until you're there :^) Then you could always post asking for recommendation on this book\_A vs book\_B, so you know what you're in for, and how much overlap you can expect.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  05/02/17 (Tue) 17:11:43 ID: c71b16  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234668)[4668](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4668)[\>>4669](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234669)

Also, Satanon, Concrete Math is referenced for it's exercises and SICP from Sussman is used extensively.

  

Are we in this together? Maybe making a new thread/board would help in gathering new possible students?

  
  

Samefag here, just bored and expanding a bit

There's a lot of overlap in the material (like the whole intro series for functionalcs link is included in the OSS Uni link), which is kinda nice imo. Plus second link has mostly MOOCs, very little reading and lots of visuals, which are nice for brainlets like myself to break up the monotony of reading though a book and it feels good completing the weeks work in a MOOC. But on the other side, the books in functionalcs provide lots of rigor, which is of course nice too.

And personally, I found the link OP provided to be much more structured and has a better curriculum overall than the OP in this thread, and OP anon said this himself, so I'm mostly ignoring the original post in this thread, but do plan on reading through some of the gems like TAOCP (including Concrete Math), CLRS, all the Sussman and Spivak books as time allows and when appropriate, as they are all universally well regarded books. Oddly, the functionalCS has less renowned books in it, but reading the descriptions I believe in them and their place in the curriculum.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  05/09/17 (Tue) 22:59:16 ID: f21e73  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234673)[4673](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4673)

Also, just for the sake of sharing resources, I doubt I'll ever get through the books in this thread, the books in OPs recent link AND the github link, but for extra material there's always these:

  

Hey anon, here is samefag of [\>>4669](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234669) again!

Well those were my conclusions too, more or less. I'll follow the structure of both links (OPr's functionalCS and OSS CS) and pick the parts that fit my needs better wherever ther's an overlap. FunctionalCS inspires me especially since this "constructive type theory" where math proofs and computer programs are almost the same entity literally turns me on af.

So, this should take you about 2 years of working 3 hours per day, no breaks (the "Seinfeld productivity trick" is the only thing I've ever achieved anything).

Plus I'd like to read at least parts of CLRS, Concrete Mathematics, and SICM. SICP as you said is referenced in the link so I'm only gonna use as much as it is required for that course.

Is this doable? I don't know, but the blob of lack of motivation that seems to follow me everywhere disappears in a sec everytime I see this post, its links/books and similar ones, so maybe it is.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  05/12/17 (Fri) 14:14:22 ID: 2e7b85  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234678)[4678](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4678)[\>>4679](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234679)

Sorry for the messy writing style, kinda sleep deprived atm

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  05/13/17 (Sat) 01:11:15 ID: f21e73  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234679)[4679](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4679)[\>>4694](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234694)

\>2 years of working 3 hours per day

IMO we can get it done sooner without sacrificing depth, some of the courses in OSS uni I was gonna plow right through, or at least I hope to.

And yes, it seems completely doable to me, for what its worth. Also, my motivation sucks dick too. But it's better to rely on discipline than motivation, so I would focus on cultivating that. I just set up my "daily minimums" for the Seinfeld method, and I hope to grow them over time. I think relying on spurs of motivation can end up hurting in the long run, since realistically, this stuff is going to be monotonous, boring and uncomfortably hard - so I think being very disciplined is much more fundamental to success than being motivated.

But at any rate, the writing style in the functionalcs link is very motivating to me to :^) I would love to know that the knowledge of all these books is carried in my brain, and (hopefully) applied in the work I do.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  05/14/17 (Sun) 03:40:52 ID: f21e73  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234681)[4681](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4681)[\>>4682](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234682)

\>z.cash

Ok, seriously OP, make a thread on /biz/ detailing how what I need to know to be successful here.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  05/14/17 (Sun) 16:41:56 ID: f21e73  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234682)[4682](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4682)

Just to reiterate about the zcash thing, I hear a lot of people saying it's a scam, since the founders can just create more coins whenever they want, and things along that line. But 4 years ago I had wished I had the guts to dump some money into bitcoin, so I think I'm going to start mining zcash and see how it goes (never mined before, so also doing it as a learning experience).

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  05/17/17 (Wed) 18:59:54 ID: cb0914  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234683)[4683](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4683)[\>>4684](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234684)

You say that you are working as a researcher at a university does that mean you have a degree? I like the sound of research but don't want to experience the cancer of undergraduate studies so I am wondering if it's possible to become a researcher without credentials.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  05/19/17 (Fri) 16:56:46 ID: f21e73  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234684)[4684](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4684)

OP is kill, but I don't think he went had a degree. At least,that's what I like to think.

What sort of undergraduate study cancer are you talking about? Fulfilling prerequisites?

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  05/21/17 (Sun) 16:22:24 ID: 91d625  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234685)[4685](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4685)[\>>4686](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234686)

Do i need to know the multiplication table out of my head to do this stuff?

Or should i learn that first??

Never learned the multiplication table properly…

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  05/21/17 (Sun) 22:14:47 ID: f21e73  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234686)[4686](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4686)

Do you mean like answers to random multiplication questions? As in just memorizing 12 x 5? 4x3? etc, etc..? If so, no. You'll get much better at it as you move along, but it's absolutely never necessary in the corporate and professional world to be quick with mental arithmetic.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  05/26/17 (Fri) 01:25:20 ID: f21e73  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234693)[4693](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4693)

/r/ing op share cryptocurrency algorithms you wrote and talk a bit about zcash, there's shitloads of doubt about it out there

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  05/28/17 (Sun) 20:14:14 ID: 5f5567  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234694)[4694](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4694)[\>>4695](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234695)

Hey studentanon, still the same guy of a couple weeks ago here.

Are you making any progress yet? Bc I've not started yet, except watching a few videos, since I'm currently doing my masters thesis for the actual uni, which will hopefully be over this summer.

Anyway I had a look at the whole thing and there's really more than I need if one considers both the oss uni and the functionalcs links. Also, deciding what I want to know and where do I want to get that info from is gonna take me a little concentrated effort, I need to like make a mental map or something of the whole personalized curriculum. But again, not now, most probably in 2 months. I am very much looking forward to it!

  

\>>Are you making any progress yet?

Hey I was just going to call you a faggot for not replying. I've started, but only vaguely. These are the resources I'm using:

Each has their own pros and cons. I think functionalcs is by far the most rigorous and solid, with it's 'downside' actually being its rigor IMO, as some of the equivelant OSS Uni material is very digestiable and quicker paced than digesting a book. The OSS course, as said has the pro of being digestible, and I find that MOOCs can be refreshing, however it lacks 'rigor' at times, imo. And lastly the teachyourselfcs link is brief, which is great because it's realistic, and keeps me on track to realize what's really necassary (as you said, like a mental map).

I'm not planning on using every link from every course though, that would be an insane amount of both time and overlap (initally at least, perhaps over the years for review I might exhaust them all). However, using them in tandem is kinda nice, as an example: I started the Linear Algebra MOOC because I wanted a gentle introduction before jumping into the functionlCS book. It also keeps me in check since I can kind of find the "median path", the one with maximum overlap, as those must be the most essential topics to learn.

So, the reason I'm telling you this is that for functionalCS I've only read "The Little Schemer", which is only briefly mentioned in the "alternative intro", along with the little MLer. AMAZING books though for a beginner, you don't even need a computer just a notebook to start understanding recursion. I also went through Learning How to Learn, and exhausted all the other extra links in functionalCS (some great stuff in there, as you mentioned like the Sienfield method).I'm going to finish Harvards CS50 course (about halfway right now), then start the HtDP series as the official intro, I began the first just to get a taste.

Sorry for the blog post, but I think that's sort of what this thread is turning into if we continue :^)

What's your thesis on? Genuinely curious.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  05/28/17 (Sun) 23:34:24 ID: f21e73  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234696)[4696](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4696)[\>>4701](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234701)

I should've expaned more on the comparison between OSS Uni and FunctionalCS. Rigor is absolutely essential, the more of you have the better you will become and I think functionalcs is fantastic because it's so rigorous. BUT, the updside to a lack of rigor is that it's EASY to do, especially since you don't even have to read shit, and I find I tend to get more done overall if I follow the path of least resistance. As an example, I wouldn't have started linear algebra if the mooc didn't seem so piss easy.

Also, functionalcs gets mad points for all the books that include programming alongside the material, that's DOPE AF.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  05/30/17 (Tue) 19:37:02 ID: a87129  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234700)[4700](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4700)

I'm just starting and If any of you fellas want to join me in studying I'm at this mumble server:

addr: bunkerchan.xyz

port: 64738

nick is ivegotasthma

order of studying:

  

Hey! That teachyourselfcs link precisely looks like the stuff I was hoping to find, or was eventually going to painfully have to assemble myself. It's gonna be the main compass to keep me broadly on track, as I progress. Great find!

Actually, a certain level of rigor gives me literal wood lol, as I can be quite sensitive to information overload but on the other hand I am able and love to think as "deep" as possible, exerting all my mental energy to understanding a concept well, that is.

As it says in the introduction to The Little Schemer: "If you do not fully understand one chapter, you will understand the next one even less." THIS is the kind of stuff I crave for!

Btw I'm tackling those two "The Little-" books as we speak, and I'm like wtf! Pure food for the mind.

I watched the first lecture of Learning How to Learn and thought was common sense bull mixed with documentary tier brain science, but I should probably give it a second chance…

The first two lectures of CS50 make me think I already know the stuff taught in the course, but watching it anyway can't hurt, I mean the classes are like a TV show (the guy is literally one of the best public speakers I have ever seen, so much for the stereotypical computer scientist lol) and sometimes it is nice to see things you gave for granted being explained with a different metaphor or through examples you didn't think about before.

I should say I already know Linear Algebra and Calculus pretty well, since I studied experimental Physics, even though I'm slowly shifting towards Material Science with my masters - I'm doing experiments with soft solids these days. I'm no Einstein, believe me, but I did attend uni at a good place, where I got to know quite a few whizes including people who do wicked shit like quantum information or write highly efficient code for parallelized computing. Maybe I'm wrong, but I have got the impression those really good guys doing theory are just faster thinkers and there's not much you can do about such a thing, but nevertheless I myself took a class in Computational Physics (mostly the mathematical and empirical theory of it) and found it fucking fascinating. Hence the desire to know more. But as far as the training in algorithms and languages goes, I'm as ignorant as the layman.

Now I think I'm winning the blogpost challenge since I also included irrelevant personal info!

  

Man right on anon! Rigor gives me wood too lol. But finding ezpz stuff is nice when shit hits the fan and I'm totally lost.

And I love the little schemer, it's taught in such a great way. Good for you!

\>LH2L

Yeah, it was 'mostly' common sense bull, but having a complete and thorough reminder of it was really nice. I can post my pdf of the notes I took if you'd like. I just powered through it one evening after putting it off for so long.

\>CS50

Yeah, I felt the same way.. UNTIL I tried the assignments. I would just kinda skim over the notes and think"ok I'm probably at like week 6 with my current knowledge and skill level", but then week 0 assignments would fuck me up. I didn't know the speaker was so great though I guess I'll have to start watching those.

\>Lin Alg

Oh right on, I'm finishing calc up at local community college now, don't know a lick of linear algebra though. I've always wanted to know whats it like to meet these "whizzes" I always hear about. I tend to think (having no experience around these people) that's more a matter of "mathematical maturity" but applied to many different concepts.. But again what do I know, that's just my hopeful optimistic brainlet take on it.

What's your thesis on though?

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  05/31/17 (Wed) 02:48:47 ID: f21e73  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234703)[4703](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4703)

Oh, I wanted to ask: does reading the little MLer and the little schemer concurrently have any drawbacks? I was doing them in sequence, so I'm just curious if I might be able to take a peek at MLer.

  

\>I can post my pdf of the notes I took if you'd like.

Pleeease!

\>mathematical maturity

Ok, re-reading myself I think I sounded a bit pessimistic: some of the top guys I met are indeed just ultrafast minds, like this guy I met that was doing his thesis on Quantum Information in Thermodynamics, a guy who still found the time to do super intense workouts 7 days a week among other things. But many of them just seemed to be super well organized and determined to reach their goals through daily "deliberate practice". And yes, that slowly but surely gets you to mathematical maturity and can make one familiar even with huge complicated subjects.

Btw, my thesis is in 2-d Soft Condensed Matter. In principle, solids are often just regular arrays of atoms stacked together: one clever way to study some of their properties is to build models resembling those regular arrays but involving bigger units in place of the atoms, so-called colloidal crystals, and look at those instead. Mechanical properties and structural features can thus be investigated, by using a variety of probes. I still have to make my mind over what I like best, building experimental setups, doing the actual measurements, maybe doing computer simulations once I'll have read more about that? More fuel to my quest into the wonders of Compsci!

I'm pretty sure a good googling could lead anyone who's reading this to my group's homepage, so much for the anonymous imageboard thing lol.

  

\>Pleeease!

Ok, so, brace yourself: I recently switched OS's and a lot of my files became corrupt on my flash drive and my LH2L notes were one of those unfortunate ones. If anything doesn't make sense feel free to ask (probably a lot of confusing bits). I've deciphered and reconstructed it the best I could, but these weren't notes that were intended to be released to the public at any rate, so:

Week 1: Pomodoro technique, focus vs diffused modes of thinking, the importance of frequency over binge sessions, increase working memory, sleep & excersize .

Week 2: Essentials of Chunking. Chunks can be analgous to zipping a file on a computer - compressing the ideas into a consice understanding. Uniting scattreed bits of information through meaning. Merging of chunks allows efficient understanding and application of creativity. Example of playing guitar and chunks of chord sequences and combining with other chunks. Example of tongue twisters (hard for non-native, easy for those who have a native, chunk by chunk understadning. Connection between steps when following step-by-steps solutions - rather than focusin on why it worked.

Week 3: Procrastination and Memory How to chunk - it varies from subject/activity to subject/activity. Focus (not distracted), understanding of concept (diffuse), "Aha!" vs expertise - closing the book and seeing if I can solve it myself. Context (application through related and unrelated problems) - know how to use the tool through practice. Bottom up and top down learning. Big picture: walking through a chapter before hand, small: details. SKipping ahead is ok! It can help cement a previous lack of understanding. Illusion of competence: Re-reading sucks compared to recalling after reading/practice. Glancing at soltuions, thinking it's easy and that you know it SUCKS. Highlighting / underlining SUCKS, but synthesizing your own notes in your words is tip-top. Try not to repeat mistakes, but implement self test. Become independent of enviromental cues (study in different spots) Seeing the bigger picutre: Dopamine in learning. Emotions are intertwined with cognition and thus learning. Be happy to learn! Build a library of chunks: Chunk trasnfer to from one disicpline to another (piano to sc2) - diffuse. Sequential thinking through focused vs Holistic (intuition). Overleanirng: don't spend too much time practicing what you've mastered - stay away from too easy too often. Eistellung: falling into a rut of problem solving, a roadblock. Be open to new approaches. Know which chunks to use, bounce between difference problems (interleaving - like on an exam, pick out why some problems call for one technique over an other) - don't limit this to one subject, interleave between many subjects. This is where there is a benefit to studying many different fields. Avoidance of stress.

Week 4: Renaissance Learning and Unlocking Potential: Building a foundation takes a long time - procrastination kills this. Habit is ZOMBIE MODE unless cultivated for PATRICIAN MODE. 1. Cue (texts, feelings) 2. Routine (from cue) 3. The Reward (why the habit continues) 4. Belief (belief in urself!). Don't focus on the product (finishing homework), focus on the process (putting forth best effort for short period) - surfer anology. This can be compared to pomodoro. Look to change reaction to cues, and change of habit will follow. Recognize these: location, time, how I feel, reactions (other people, things that have happened). Often, you can be unaware that you've entered a procrastination phase. The reward can be synthesized. Juggling life and learning: outline of task at least the evening before. Make list to free up available RAM. Delay distraction until task is completed, back up plans for when procrastination strikes. Images play a role in memory, the more triggers the better. Repitition. Flashcards (or equivelant). As information becomes solidified through intelreaving, increase space between recall. Consilidation, reaction, reconsilidation. Create groups - personal tricks to memorize: all cows eat grass. Visualizing items in a familiar setting..? Creative applications of learning gimmicks. visual and spacial technniques - use these! The more playful the better. Remeber numbers by associating them with events..?

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  06/02/17 (Fri) 18:33:05 ID: f21e73  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234706)[4706](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4706)

\>super well organized and determined to reach their goals through daily "deliberate practice"

Well that's good to hear, lol. I've always heard these rumors of intellectual goliaths roaming around campus and my inner competitiveness has always been a bit skeptical. Not to imply that all people are of equal intellect, but I've always attributed more of that to hard work, like you say, rather than innate ability (it helps soothe my brainlet mind to think hard work will actually pay off I suppose).

\>2-d soft condensed matter

That's cool anon, good on you. I've only completed physics with calculus (the intro series at most unis), so I have no idea about any of that stuff but it sounds cool! I've always wanted to go into some sort of maths/physics computation at some point, seems comfy and transferable to lots of other fields (finance, biology, etc).

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  06/10/17 (Sat) 10:47:06 ID: 5f5567  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234707)[4707](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4707)[\>>4711](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234711)

[![](https://archive.md/sud91/6b3436e17d9cd818f693df3c9486c8876aded372.jpg)](https://archive.md/o/sud91/https://media.8ch.net/file_store/2755a21be3fe8f8d1e2bdebea4fe29bcc3c5ac313995223ec83359f9ea503aa6.jpg)

Hey, thanks for the notes. I had a look at most of the course because some parts actually captured my attention, it wasn't bad after all. (I think you have made week 3 into week 4, and split week 2 into 2 and 3 in your notes, not that it matters too much…)

So, I'm at the end of the C intro part in the video lectures of CS50, I plan on having a look at the related assignments maybe and then switch to the "Introduction to CS and Programming using Python" as the OSS link suggests to do as CS50 moves away from C.

So, I'm coming to the conclusion that for me the only really effective learning is through hard, focused studying, and a book in a quiet room is probably the best way to attain this. Plus, of course, practice, which can be pen and paper as in Physics - but for CS is mostly doing the programming exercises, reading and editing other people's code, and generally speaking coding your nights away.

So, I'll try to avoid lectures as the main source of knowledge, only watching the ones that introduce concept I don't have the time to read about, or concepts I wasn't able to grasp otherwise.

In this I totally agree with Scott Young:

Also, I still have the writing and an exam due this summer, so I'll be mostly postponing stuff to then.

There's one big elephant in the room I haven't discussed so far. Ok, we both want to learn CS because it's cool, useful and all, but I originally came to this thread an year ago or so because I wanted to build my mathematical baggage beyond Calculus and Linear Algebra: so, after I have learned algorithms, I definitely want to dive into some of those Calculus on Manifolds or maybe Functional Differential Geometry. Deep down, I would still totally like to hide away with a stash of mathematics books even more than I want to code. One thing at a time tho.

Pic related is how I feel about all this.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  06/10/17 (Sat) 10:50:59 ID: 5f5567  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234708)[4708](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4708)

\>So, I'll try to avoid lectures as the main source of knowledge

What I meant by all this is: assignments are the real gold of online course ware

\>Pic related is how I feel about all this.

Just in case: that's supposed to be a dawn - the beginning of a new day

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  06/12/17 (Mon) 18:16:52 ID: f21e73  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234711)[4711](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4711)[\>>4712](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234712)

\>lectures (mostly) suck

I completely agree with your idea about just getting your hands dirty doing exercises to learn, as quickly and as much as possible and resorting to lectures when confused. Absolutely, 100% agree. Sometimes I'll even only briefly skim the chapter and refer back to it when stuck (in math). Things don't click or become ingrained into my brain until I myself put the parts together and connect the dots (I do like example heavy lectures though because of this, as an example Professor Leonard is my vice in calculus).

\>writing and exam due

I've been postponing everything the past two weeks as I'm finishing finals up right now (Discrete Math II and Vector Calc) and moving ASAP, but this summer won't have any schoolwork to do so plan on plowing through a lot of this beginning at the end of this week. I got distracted and spent too much time reading working on this stuff instead of doing my schoolwork lol.

\>mathematical baggage

This is why the thread appealed to me to, it's a nice meeting point between the appeal of very rigorous math and an application of it with CS. I think the Functional Diff Geo book sounds super cool but I've some prereqs to knock out before I can take that on.

\>pic related

And I feel the same, it's very refreshing to be interested in this and not have deadlines hanging over my head, lame lectures and useless group projects like at my college. Being able to pursue it at my own pace (faster or slower) is also fantastic. Also, I've really grown to hate James Stewart's presentation style (finally finished Calculus: Concepts and Contexts). The books in these online self education things are so much better it seems (not at teaching calculus necessarily, but just in general - as an example, the little Schemer was different than anything I've ever read yet so effective, and How to Prove it reads almost like a novel and is far more efficient in teaching the material, IMHO, than trudging the Stewart's book).

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  06/12/17 (Mon) 22:39:54 ID: 5f5567  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234712)[4712](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4712)[\>>4713](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234713)

That's great anon, also it feels great to share our experiences about this journey. It'd be even cooler if we could gather more people

Hey, I didn't ask so far: what is it that you're enrolled in at your local university? CS bachelor or something else entirely?

I started attending class again after almost a semester of lab work today, for a one-week workshop/course and - it sucks, at least a bit. Most of the time I was just thinking how it would be nicer to dive into the books, skip the things I already know and maybe slow down on the stuff I want a deeper understanding of. Fortunately I do have my free time for that.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  06/13/17 (Tue) 03:16:05 ID: f21e73  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234713)[4713](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4713)[\>>4715](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234715)

\>more people

I may have recruited two friends that will begin around June 20th, hopefully. Maybe we can outreach to more people via HN or reddit It'd be great if we had an active board here on 8ch. I agree though, I got a little competitive motivation when I read you were ahead of me in cs50 and The Little Schemer, lol, so that's helpful.

\>CS Bachelor or..?

I'm lackadaisically going for a math major, currently looking to transfer to Uni this fall or next (still wanna finish the physics series and some CS classes from community college to save $$$). But I'm unhurried because outside of school I have (non-academic) work that has some promising horizons (for a humble poorfag), and I don't mind taking my time as it allows for a lighter load and more time for meandering into projects like this :^) Honestly, I'm not even sure if completing uni is worth since programmers don't necessarily need degrees. One of the things keeping me motivated in school is the allure of PhD life though. I like what I'm learning so I think getting paid to do so would be pretty comfy. How do you like? Do you get a lot of free time on top of it? How often are you required o be in building? I imagine in varies a lot depending on your specialization.

\>classes suck

I agree! I so much more enjoy being able to select my own textbook, go fast or slow and wander into tangents while learning. I lose all enthusiasm when the books are already chosen, the pace is set along with the order of consumption, and I can't stand having to attend lectures, do group projects, etc etc.. I hope to see autodidacts get more respect in industry and academia some day.

  

Hey, same ol' anon from a different home here.

\>I may have recruited two friends

That's what I'm talking bout! Anyway, when we'll make a board/subreddit/whatever US TWO ought to be the bosses of that place no doubt!

\>going for a math major, currently looking to transfer to Uni this fall or next

That's fantastic! I would say a Bachelor is really enough if you're not living in a country with high unemployment rate. I admit kind of grew tired of my masters programme at times - even if all around it was a great experience and I learned cool stuff, visited labs, had hands-on practice, even published a scientific/engineering paper already etc… Speaking of a PhD, I don't really know. Here in Europoorland the PhD is a 3/4 year programme you are only allowed to apply for if you already earned your Master's, which is somewhere between 1 and 2+ years. I know the situation in Burgerland is totes different but my personal opinion right now is that I an "industry" job would feel more like "real work" anyway - but maybe it's just that I can't make my mind on what I want to do in life at the moment. Except, of course, hiding away and learnin CS/reading Math books :^)

\> How do you like? Do you get a lot of free time on top of it? How often are you required o be in building? I imagine in varies a lot depending on your specialization.

It definitely does depend! The PhD candidates I am doing my Msc thesis alonside with seem generally not too stressed, they do work hard and sometimes late in the afternoon or even in the weekend, but I have the feeling they only do it because they want to get the results and publish (and they do!). Also, the atmosphere is especially nice because they are all good people and because the Uni is top so money in not too much of a problem for our research. But go just a few labs away, and you'll see miserable people with no free time at all that get bullied by the professor into showing up every sunday, or some other wicked shit. Do they get more done, more publications and respect in the field? Maybe. But, as a bright friend of mine who became Full Professor at 30-something often says: luck plays a major role, not just significant but major! Of course you have to get some shit done for luck to catch you.

This is why in looking for a job I am becoming increasingly focused also on other, so to say collateral, aspects such as paycheck, human environment, quality of life, because I noticed so many things that turned my once idyllic notion of the scientific community into what is just another part of the job market, where in the end people and the relations between them is really what makes a difference. Case in point: looks like many professors are just machines for writing grant applications for funding. Do I really want to climb the ladder of Academia, for the love of Science, just to get to that in the end?

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu") The Art of Problem solving Volume 2 chiupuk  06/16/17 (Fri) 15:22:59 ID: 2c6976  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234716)[4716](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4716)[\>>4717](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234717)

Hello everyone, I am searching for "The art of problem solving Volume 2: And beyond"

does anyone have it, please, share it, sharing is caring ;)

Ty in advance

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  06/16/17 (Fri) 17:07:25 ID: df8576  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234717)[4717](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4717)

Sup dear tripfriend. Ever heard of Library Genesis?

  

Hey anon, me again.

I am a complete NEET for the next 3-4 weeks, so I'd like to get a lot of headway into this.

I'm beginning to think the most productive medium for our endeavors might be discord. I've never really used it, but as I understand it's a very popular IRC client that keeps conversation history, so we could very easily log into our little chat and post a question, but that will only be useful if we grow in numbers.

\>Bachelor is enough

I hope so :-) I'm not sure what math classes I want to take either, with pure, applied and stats. But I'm figuring that out as I go. I don't know what I want to do either, but there's certainly a shitty romanticism I attach to contributing to your field with publishing papers.

\>The PhD candidates I am doing my Msc thesis alongside with seem generally not too stressed

That's good to hear! I would hope, if I ever go that route, that I would still have time for leisurely unhurried walks and lazy mornings. Reading further, I can see it seems dependent on who you're working under though, which only makes sense.

\>Quality of life

As I get older I begin to narrow down my career path more and more to being based exactly on that. More than anything, I want to set my own schedule, and I hope CS can get me closer to that option (working remote seems relatively common in CS, compared to other STEM majors). I can very easily see myself facing the same conflicts of watching your idealistic view of the scientific community turn into realizing it's just another part of the job market, so thanks for sharing that bit. More and more I consider keeping my academic ambitions just as a hobby, while placing real focus on finding a career I'll simply derive more joy from.

ANYWAY, I'm gonna be blazing through The Little series this week. Where were you planning on going after that? I have been enjoying cs50 and plan to complete that, but don't know my next step quite after that, I would really like to move onto How to Design Programs personally (which is listed in each of three sites we're going off of), though OSS UNI recommends taking another intro course (which strikes me as time wasted) and TeachYourSelfCS recommends How to Design Programs only if the SICP book is too challenging. I don't know, but I'm interested in how your progressing and which direction you might be going! I'm going to set up a discord when I get around to it, it'd be great if we could have a "sticky" post in it as well.

  

an update: rather than discord, I've been recommended keybase and it seems exactly what I was looking for. Lmk if you like the sound of that!

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  06/26/17 (Mon) 21:03:44 ID: f21e73  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234723)[4723](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4723)[\>>4731](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234731)

sorry for spam posting, but how's your math physics anon?

just askign because I'll be going through real analysis towards the latter half of summer, I've never taken linear algebra so I was going to cover that than work through baby Rudin and Analysis I-III by Terrance Tao

  
  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  06/30/17 (Fri) 20:49:11 ID: 5f5567  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234731)[4731](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4731)[\>>4732](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234732)

\>I'm gonna be blazing through The Little series this week. Where were you planning on going after that?

To my writing, or else I'm kinda fucked :^)

But yeah I'm really eager to build my basics of CS asap because I want to know more about Machine Learning and related fields.

how's your math physics anon?

I am proficient in Linear Algebra and I know Calculus pretty well (but there's much of the less basic stuff that I'd like to have a deeper look at - e.g. a consistent theory of Differential Equations which my curriculum was sadly lacking). I studied some Complex Analysis (turns out Calculus done using complex numbers is a totally different kind of beast) and Functional Analysis too, both vastly irrelevant if you're not going to dive in the realm of Theoretical Physics eventually.

\>rather than discord, I've been recommended keybase

FIne then, I'd really like to have a platform where we can freely discuss the real stuff without the drunken turkposting of this guy [\>>4726](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234726)

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  07/01/17 (Sat) 02:58:58 ID: d0ea0a  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234732)[4732](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4732)[\>>4739](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234739)

\>To my writing

Ah ok, and after that? Last I heard you had completed both the Little Schemer and MLer, and had dabbled a bit in cs50. I mean it's not like we have to take the same courses, but I'd be interested in what you're doing and why.

\>Complex Analysis

Ok, you're quite a bit ahead of me in that department! I'm tackling the Linear Algebra book recommend in functionalcs along with building up my (horrible) proof skills with How to Prove It by Velleman.

\>keybase

I still have to set mine up, do you run a GNU/Linux distro anon? I switched to NixOS recently so I've been mainly tinkering and trying to set up various development enviroments, and that's been a bit of a bottleneck. But at any rate, we can still post here for quite some time, and since we're still only at a meesly number of 2, I don't think it's much of an issue :-)

  

I might be able to handle the science part but I've always been bad at math. I remember as far back as either kindergarten or first grade, my class was in a computer lab doing basic math problems in these four or five games, which included basic addition and subtraction involving carrying. No matter what game it was, I was always one of the last few people to finish, if not _the_ last. I also failed algebra 1 in 9th grade and had to go in for tutoring nearly every morning for a whole year for whatever came after geometry (algebra II, maybe). Also, I've tried to teach myself a few different things before and have never been able to do any of them on my own because I get frustrated easily and have a shit self-esteem; I've always had to have someone else teach me how to do really anything. OP seems to either be very intelligent or just has a natural knack for learning technical stuff, or more than likely, both.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  07/02/17 (Sun) 04:45:56 ID: d0ea0a  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234734)[4734](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4734)[\>>4735](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234735)

hey anon, the math you'll actually have to know is never going to be like in grade school where it's mental arithmetic - even algebraic simplifies / solvers are out there for that kind of stuff.

I don't know, but what's the worst that can happen, right? Getting frustrated happens less with time, I'd give a shot anon.

I think you'd enjoy Harvards' cs50, especially the scratch intro. It's a drag and drop introduction to programming a little game.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  07/02/17 (Sun) 16:50:54 ID: d56dce  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234735)[4735](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4735)[\>>4736](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234736)

Yeah, maybe you're right. Guess it wouldn't hurt to just give it a try.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  07/03/17 (Mon) 02:28:45 ID: d56dce  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234736)[4736](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4736)[\>>4737](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234737)

Same anon here. I decided to give the books a try and am maybe two hours into it. I'm on the very first exercise in the _Basic Mathematics_ book and to put it bluntly, I don't know what the fuck I'm doing, which means I probably won't be able to do any of the other exercises throughout the book either, let alone the rest of the books which are probably hundreds, if not _thousands_ of times harder than this one. I've read and reread everything up until page 29 (the page I'm currently on) and I still don't understand how I'm supposed to solve these problems without knowing the definitions of "associativity" and "commutativity" other than some brief examples that don't help me very much. I can skip ahead and look at the answers section at the very end but that would kind of defeat the purpose of doing the exercises to help me learn. I don't remember a single goddamn thing from high school. Much as I hated that place, at least my teachers explained to me what certain terms meant and how they worked, even if it was in a somewhat shitty way. It seems like this book just assumes that you know what everything means and can figure out how to put it together with wordy yet short explanations. Am I doing something wrong or am I just a stupid asshole?

\-P.S.- I'm not asking for answers or explanations to the exercises and problems, I just want to know where to go from here if I can't even get 30 pages in to the very first book. I'm already tempted to simply quit altogether because I feel extremely discouraged right now.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  07/03/17 (Mon) 03:18:36 ID: d0ea0a  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234737)[4737](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4737)[\>>4738](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234738)

Hey anon, that's awesome you're giving it a shot!

I think it's analogous to learning to play guitar. It fucking sucks at first, you're fingers sting, you suck and the noises you make are obnoxious, nothing is clicking and it's super frustrating and embarrassing - so most people quit after a week. You might hear excuses like "my fingers are too short/fat/long/skinny" - I used these myself at one point. But, if you hold out for just another week and bear with it, you start to get calloused, things hurt a little less, and you start sounding pretty smooth. By week 3-4, you can play a couple of your favorite songs and things aren't so bad anymore. It's easy to pick up new songs, and all that frustration was all kinda silly in hindsight. People play 1000000x better than me with their feet for christ sake.

Similarly with learning mathematics. The math that made my blood boil the most was the exact math you're working on, but you will become calloused and smooth through experience if you just stick it out through that beginner phase when everything feels hopeless and you can't stop telling yourself your doomed to suck. Just know the hardest part is the first couple of weeks, and if you need any help with problems, I'd love to explain - no matter how "dumb" you think they are or make you sound. After you've developed your base, I firmly believe it only gets easier (except for, perhaps, proofs, but that's a different story ;) ). My point is that it gets thousands of times easier, not harder. If you read OP here [\>>3044](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%233044) he mentions how hard things were at first, but he begins flying through material that's higher level and would seem "more difficult" - through experience, he's achieved a higher level of 'mathematical maturity', and is able to inhale the text like it's nothing (maybe not, but that's what it seems like).

If you get stuck, look around for help, reread the chapter, etc etc. I've heard Khan Academy is great for k-12+ math, have you tried watching their videos? Textbooks can be hard to learn from when you don't have many learning skills. Also, on that same note, I think you'd benefit a lot from the Learning How To Learn MOOC available on Coursera - it's all about efficient and thoroughness in learning, and is a great tool before embarking on a journey like this (plus, you could finish it in an evening).

  

I mean, I thought about looking up the definitions online or examples of what problems involving associativity/commutativity look like, but I didn't do that and instead tried to rely solely on what was in the book in hopes that I could figure it out myself, which like I said, didn't really work. I guess I'm just annoyed that even for a title like _Basic Mathematics_, I need to read other books and/or do other things _before_ I can actually understand what's in it. But I guess if that's what I have to, then that's what I have to do. Thanks a lot for the suggestions and positive words, anon. I signed up for that Coursera class and will see if that helps me any.

  

\>Last I heard you had completed both the Little Schemer and MLer

I didn't do The Little MLer tho, I am more interested in Scheme/Lisp than ML for what it will allow me to do (e.g. read Sussman's books!)

<Complex Analysis

This may sound like an advanced version of Analysis, if you're not familiar with Complex numbers. But it's a whole different kind of branch instead. As I said, while you might need to know and use Complex numbers, for most of Computer Science related things you definitely don't need the theorems of Complex Analysis in your life.

I also have to admit some stuff is starting to fade away in my (Real) Analysis/Calculus and Linear Algebra and could really enjoy a few hard ass problem solving sessions in the weeks after I'm done with the lab. I can envision myself late into the evening hours, grinning from ear to ear, sipping some ice tea while I teach myself about multivariable functions.

Btw, I will most probably use the first 9 chapters of Adams's Calculus book because I like the enormous amount of exercises including some neat real-world stuff, and then jump to something else for the higher dimensions Analysis (AKA Vector Calculus).

I have no idea what to use to become strong again in Linear Algebra, my lecturer was amazing but the book she chose was pretty weak. I'd like something concise, possibly a classic that I can read from cover to cover while solving selected problems the way OP suggested. How is this "Baby" Rudin?

\>do you run a GNU/Linux distro anon?

I do. Switched eons ago to Linux Mint because it's like the slightly less normie/gay version of Ubuntu, but still far from the complexity of Debian. I encountered errors while trying to install Keybase tho, I might have a better look at it during the week.

  

<Baby Rudin

I fucked up with all those nicknames. I think I meant Valenza or whatever is that you're using. Also if you had a look at Lang's book suggested somewhere in the thread.

Let me also say to this guy

anon DON'T GIVE UP UNTIL IT FUCKING BLEEDS! And IMHO if the MOOCs feel like you're not experiencing any pain, then you might reconsider the use of them…

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  07/03/17 (Mon) 21:26:06 ID: d0ea0a  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234741)[4741](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4741)[\>>4743](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234743)

\>How is Valenza?

I am only on the first chapter, but I really, really enjoy it so far. It's exactly the type of problems I'd like to be able to handle, written in a nice way and comes off as erotically rigorous. My previous math experience has mainly been "computing the calculus" through Stewart, which sucks balls in my opinion as it doesn't prepare for you for rigorous classes. So all that being said, Valenza is hard as fuck for my pea brain, but I'd love to be good at a book like that at confidently understand and approach the questions. /blog

Oh ok, well I actually decided I like The Little Schemer → The Seasoned Schemer → The Little MLer. A lot of the course material in functionalcs uses ML, so I thought it'd be nice to get an ezpz intro to it - but I totally agree with the Sussman goals. After all, the guide is only just that; a guide.

\>Linux Mint

Anon, allow me to let you in on a little Scheme secret: GuixSD ;) I would totally run it if I had the patience to configure it for nonfree drivers (I imagine someone has already done it, but I'm up to my ears with other system config stuff, so it's on the backburner). But anyway, it's a scheme programmers wet dream!

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  07/03/17 (Mon) 21:31:32 ID: d0ea0a  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234742)[4742](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4742)[\>>4752](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234752)

I'm always having to reference other material, you shouldn't be ashamed of that. Use all the tools you have anon.As you know, the goal isn't to complete the book in isolation, it's to master the materia - and the internet, other books, etc are all wonderful supplements for that.

But I see where your coming from. Often, I close my laptop and work from my ereader, because I want to be able to do just what you mentioned, but let that be something to comfortably aim for, not something to force yourself into.

Additionally, there's so much programming that involves nearly zero math anon, you might like The Little Schemer, you can do it without a computer using only a paper and pencil.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  07/04/17 (Tue) 19:57:38 ID: 5f5567  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234743)[4743](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4743)[\>>4781](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234781)

\>GuixSD

<"GuixSD will use a scheme init system and GNU dmd, also in scheme, which means you \[…\] can completely abstract your systems as just data to be manipulated in a program"

Well it might be a bit early for me but…Whoa!

I'm starting to believe that if I'm ahead of you in Maths, on the other hand you are probably quite ahead on me as computer savyness. Good!

I'm actually very happy to help with any concepts you might encounter, I remember Linear Algebra looked foreign and a bit boring

in the limitation of what was and wasn't allowed by its rules (e.g. a line or plane passing through the origin is a vector space, a line or plane that doesn't have the origin in it, is not! - etc) and the lecturer was instrumental in making me understand the things. So, especially when we'll set up a more convenient way to communicate, just ask for any doubt and if I'm able to answer it will also do good to my own cause - I want to dig that stuff out of the depths of the brain once and for all!

I might read the Little MLer, dunno about the Seasoned Schemer…OP the Almighty says in the functionalcs guide that the "Little" books are just good in order to get an introduction to the concepts of functional programming. Well, let's see how it goes. At the moment I have other stuff to think about all day, so I kind of took a break from video lectures (not entirely my thing anyway - but could be of use at times as I said b4) and am only picking the books I will want to do later on.

Also, partially unrelated to CS, I have just finished reading two books I started ages ago, both in a genre halfway between the "productivity tips" and "neuropsychology for the masses": one is called Focus by renowned psychologist Daniel Goleman, and the other is The Power Of Habit by Charles Duhigg and I was keking hard bc guess what! Most of the concepts from the Learning How To Learn class are discussed in the books, I'm sure they are in the references of the MOOC somewhere.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  07/15/17 (Sat) 19:45:23 ID: d321dc  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234752)[4752](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4752)[\>>4781](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234781)

Thanks for the suggestion, I'll be sure to keep it in mind! I'm currently doing the "Learning How to Learn" course hosted on Coursera but will try to give one of those MOOC's a spin at some point after I'm done with this one (maybe in between the OP-recommended math books, as I still have to go through all of those too).

You're right, I guess it was a little ridiculous of me to assume I could do it all on my own without any external help/references. Ok, I downloaded a PDF of that book. Thanks for the recommendation, it seems rather helpful.

Thank you both for the encouragement, it's very much appreciated from this end :)

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  07/23/17 (Sun) 21:48:07 ID: a9037e  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234756)[4756](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4756)[\>>4782](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234782)

This is a surprisingly civil, and productive, thread.

Comparing the former with /g/, and the latter with HN and Peassit.

Cheers for this.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  08/14/17 (Mon) 16:20:55 ID: 02f86f  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234775)[4775](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4775)

\>Try and get into TU/e or other university graduate program, this is possible even if you don't have a bachelors degree

OP, there are discussions on /r/cscareerquestions about how impossible it is for someone without a CS bachelors get into a Masters program and perform well, let alone be fully funded, so how can you get into a good grad one without even having a degree first?

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  08/17/17 (Thu) 01:51:06 ID: a7a7fc  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234781)[4781](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4781)[\>>4783](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234783)

Hey buddy how have you been doing? And you, [\>>4752](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234752), newfriend?

As for me, working full time has put the breaks on and had me drop a couple gears, but I think I'm finding a cozy, slow and meandering cruise to be nice (slow and steady wins the race after all! Ha). I've been doing much more math than programming lately though, as it's a bit easier to bust out a couple math problems/chapters on a portable ereader than it is to program on the fly (largely due to my laptop having no battery). But it has to get done at any rate, according to lord OP at least :-)

I never did finish cs50/HtDP, but being back here has bumped that up a bit in the priority list. How's your CS journey of ultimate comfiness been?

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  08/17/17 (Thu) 01:52:29 ID: a7a7fc  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234782)[4782](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4782)[\>>4785](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234785)

\>Peassit

I've been thinkning about what this could be for about 5 minutes but have no clue.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  08/17/17 (Thu) 13:00:34 ID: 6457bf  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234783)[4783](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4783)

Hey, nice to hear from you again!

I also had a busy life in the last month or so, but now that some of those big rocks which kept me busy are gone, I wan to get back on track soon!

We should definitely find a better way to keep in contact, as we said…

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  08/18/17 (Fri) 04:34:38 ID: 1877d0  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234785)[4785](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4785)[\>>4786](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234786)

I remember writing it and thinking it would be to obscure.

My reposted jokes bring all the gold to the yard, and they're like it's upvoted more than yours, damn right, it's upvoted more than yours.

  
  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  08/18/17 (Fri) 12:13:46 ID: 1877d0  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234787)[4787](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4787)

  
  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  09/17/17 (Sun) 02:45:33 ID: d53808  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234815)[4815](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4815)[\>>4820](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234820)

readin' Concepts, Techniques and Models of Computer Programming

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  09/20/17 (Wed) 03:27:51 ID: 3708c6  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234820)[4820](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4820)[\>>4821](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234821)

Where have I seen this before?

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  09/20/17 (Wed) 03:34:27 ID: 3708c6  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234821)[4821](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4821)

That's where I recognize it from at least.

  

This is absolutely amazing, but I'm kind of lost. I not really confident in my knowledge about middle/high school math. What should I read if I'm going to pursue a CS degree?

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  10/07/17 (Sat) 19:36:23 ID: f4cf22  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234827)[4827](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4827)[\>>4832](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234832)

If you're pursuing a CS degree, get comfortable with middle/high school math (aka 'college' algebra, precalc, etc). For that I'd have Axler's "Precalculus", Courant's "What is Mathematics?", Stillwell's "Numbers and Geometry or Lang's Basic Math at hand for reference, or simply youtube/khan academy if you prefer videos. Don't begin here though, just reference these when you get stuck.

Now, where I'd really begin beyond simply having reference material is with Discrete Math (or a combinatorics text). If you're going to be a cs student, OP recommends Van Drunen's "Discrete Mathematics and Functional Programming" ([https://functionalcs.github.io/curriculum/#org07d9d58](https://archive.md/o/sud91/https://functionalcs.github.io/curriculum/%23org07d9d58)), but I found both Epp's "Discrete Math with Applications and Lovasz "Discrete Mathematics: Elementary and Beyond" to be nice, and the latter was especially digestible and enjoyable to work through.

Another important branch of math in CS is linear algebra, and I'm trying to digest that right now. In the link I provided for the discrete math text, there's also Linear Algebra recommendations and resources. There are lighter introductions to linear algebra though, as in Marvin Marcus's and Gilbert Strangs works.

And lastly, an overall understanding of caclulus is pretty important, and there's plenty of text available on that (a few of which are mentioned again in that same link).

Good luck and enjoy, anon :-) You can begin with either calculus, discrete math or linear algebra, none of these depend on knowledge from the others. But the most common sequence is calculus first, as it often referenced in linear algebra and discrete math. Calculus will also make you confident in your middle/high school math abilities, because it puts them to the real test.

  

What if my middle/school skills is not that great?

  

Still applies, but in that caseI'd focus more on Khan Academy, as that probably suites your learning style most (with the visual and verbal presentations and examples). But don't be afraid of peeking around the textbooks, as that's how you'll want to be learning eventually imo. All of those books in the first paragraph still apply as recommendations if you're at the middle school level (AFAIK).

Stick to doing lots of excersizes, don't ever just think you get it and move on. Drill drill drill!

Also, I'd highly recommend the "Learning How to Learn" course on Coursera. It's intended to span four weeks, but that's bullshit and you can do it in four hours if you watch the vids on x2 speed, take solid notes and immediately apply what you've learned to the course itself (so meta, I know).

Honestly, at a middle school level, I'd start with some trigonometry and learn algebra as you go (if you need to factor something, go review factoring, etc). Don't try to learn from the bottom up again or you'll waste months. Just spot check yourself as you go into deeper concepts. Good luck though buddy and I'm here if you have any questions!

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  10/15/17 (Sun) 17:09:42 ID: 495df3  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234834)[4834](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4834)[\>>4835](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234835)

Or, if you'd rather, you could start with Calculus/Analysis, Linear Algebra and/or Discrete Math and review what you don't understand as you go, but this would likely, and quickly, lead to a review of trigonometry anyway.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  10/15/17 (Sun) 18:25:48 ID: aa3976  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234835)[4835](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4835)[\>>4836](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234836)

I've already finished learning how to learn along time ago and I also read a lot of books about learning and mastery.

So here is my plan on how I would tackle those things:

\- Calculus: I'll read Calculus: Early Transcendentals by James Stewart (although I'm not really sure what version I should read, or if I need to read the whole book.)

\- Discrete maths: Discrete Mathematics: Elementary and Beyond by Lovaz

\- Linear Algebra: Introduction to Linear Algebra by Gilbert Strang

and for reference I'll be using Axler's pre-calculus and Khan Academy.

Do you know which version of Stewart's Calculus Early Transcendentals should I read and should I read the whole book?

Also should I learn the material in the following order(Calculus -> DM -> LA) or can I learn in a different order?

And lastly I would love to thank you all wonderful people, this was absolutely amazing and insightful. Reddit and stack-exchange couldn't offer an advice on such level. I really honored and I would love to get in contact with some of you.

  

\>Calculus: Early Transcendentals

I would just get the most recent version from libgen.io, personally. Some of those look wonderful even in pdf format. As far as reading the whole thing, I would. But don't be afraid to depart to other texts and such. You don't have to do every exercise, but the entire text is a good starting ground for both calculus and developing your mathematical maturity. Stewart gets a lot of crap on /sci/ and such because of his accessible style (and capitalistic marketing, but that's a different story), however I found his writing to be great for a rather underdeveloped student like myself when I read his similar book titled Calculus: Concepts and Context. Also, "Professor Leonard" has some great lectures on YouTube for this subject, as does 3B1B.

\>Discrete Mathematics: Elementary and Beyond

I'm about halfway through this one right now and really like it! It's a very fun read, which is a nice departure from the usual cut and dry presentation style, so good luck :-)

\>Linear Algebra: Introduction to Linear Algebra

I've only read the first couple chapters, but this book certainly gets a lot of positive praise as an introductory book, and of course the Open Course Ware material is a big benefit. Don't be afraid to poke around at a couple other books though if the material isn't clicking. After trying to slug my way through several LA books I've found one that's working for me, so perhaps you may do the same. And again there's the 3B1B lectures for this too.

\>(Calculus -> DM -> LA)

It can go in any order, depending on the texts you choose (i.e a linear algebra book might use calculus in the examples, or vice versa). I think the most common progression is calculus first, and after that it's dependent on the students choosing. I found Discrete Math to be fun and motivational though, for what it's worth.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  10/16/17 (Mon) 17:26:23 ID: aa3976  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234840)[4840](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4840)

Great, well then I'll be studying calculus, wish me luck.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  10/17/17 (Tue) 20:55:02 ID: aa3976  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234841)[4841](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4841)[\>>4842](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234842)

Do you have any suggestions on how I should study the textbook? Because I spend a lot of time taking notes which feels ineffective or am I mistaken?

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  10/17/17 (Tue) 22:51:06 ID: ce8f15  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234842)[4842](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4842)[\>>4844](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234844)

Personally I kind of dropped taking notes in favor of spending that time on exercises. Sometimes I'll even begin with the exercises, then refer to the text afterward (I find the text becomes readily digestible if I begin reading with intent to solve a problem). This is highly individual I'm sure, but I suggest you give it a shot. After all, I want the knowledge in my head, not on paper and I hated all the time I was spending simply rewording the authors work rather than actively learning.

Just my $0.02! And good luck anon :-) Post away if you have any troubles or need further recommendations.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  10/18/17 (Wed) 19:54:32 ID: e18cc3  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234844)[4844](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4844)[\>>4852](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234852)

Oh, also, interleaving (spaced repetitions of coming back to problems from completed sections to review) is critical and I find working through examples as they're presented as if they were an actual problem is useful too. Just another 2 cent deposit :3

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  10/23/17 (Mon) 18:34:02 ID: 2993c0  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234850)[4850](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4850)[\>>4856](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234856)

\>> 4836

Well I guess not everybody is meant to understand and learn math. Which CS areas that aren't math heavy?

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  10/24/17 (Tue) 20:30:56 ID: 2993c0  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234852)[4852](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4852)[\>>4856](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234856)

Just an update. After trying to pass the diagnostic exams at the beginning of Stewart's calculus early transcendentals, and failing miserably in everything except algebra. I'm going to try and read Axler's pre-calculus as fast as I can and then give calculus another shot.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  10/26/17 (Thu) 16:58:13 ID: 53f51f  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234856)[4856](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4856)[\>>4857](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234857)

There's plenty (see webdev), but why do you think you're not meant to learn/understand math?

Hey good for you, algebra is the hardest part. If you can do that you'll sail through the rest. I really need to dedicate some to algebraic drills as well, so good luck to us both :^)

Calculus is really the ezpz part though, the algebra and trig is what's hard.

  

\>>4852(here)

I live in a third world country, and the education system was really crap. I didn't know about the unit circle until recently, so that's way I'm studying pre calculus. I feel really angry that my teachers left out a huge part of mathematics just because they thought it wasn't necessary or because they didn't understand it at all.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  10/27/17 (Fri) 00:15:44 ID: b10bc8  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234858)[4858](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4858)[\>>4863](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234863)

fwiw I didn't learn any trig during my time in public education and sucked at algebra. But good on you anon, that's awesome you're building yourself up.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  10/28/17 (Sat) 22:45:24 ID: 2993c0  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234863)[4863](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4863)

It makes furious that those bastards get paid by our oen taxes to teach us things that we can learn online for almost nothing, and they manage to do it incompetently and incompletely.

  
  

A better book, imo, is Allendoefer and Oakley's "Principles of Mathematics", it has an identica; audience to Lang's text, but rather than

1: logic, sets and proofs

2: Number Fields (basic algebraic properties, real and complex numbers)

3: Integers (induction, divisibility, factorization, rings, matrices)

4: Groups

5: Equations and Inequalities

6: Functions

7: Exponential and Logarithmic functions

8: Trigonometric functions

9: Analytic Geometry

10: Limits

11: Calculus

12: Probability

13: Boolean Algebra

Though Lang's book is cool and a classic, I definately think the above deserves mention due to it's breadth, depth and organization of content.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  11/11/17 (Sat) 19:54:01 ID: 16e7b8  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234880)[4880](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4880)

\>but rather than

(meant to say but rather what Lang list in it's table of content, this contains: …)

  
  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  11/16/17 (Thu) 23:33:31 ID: 83cbd7  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234887)[4887](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4887)

the pdfs are shit quality tho :/

  

This is sort of a thread-related question since it involves BTC, but how much economical and/or programming knowledge would I need to invest in either Bitcoin or just stocks in general, as well as mining BTC (which I know nothing about)? Also, for someone who currently has less than $2,000 in total to their name, is it possible to do reasonably well with investing in either of the aforementioned things? I'm not expecting like a seven- or even six-figure range, but I don't want to live with my parents forever and there's really nowhere I can work that would pay me anything above what a high school or college student would earn. Not that I'm above being a wagie or anything considering I've had three part-time jobs and one almost full-time in the past, but from what it seems, I would have to work my ass off and save up my money for several more years until I could even think about moving out of my parents' place, which would leave me almost no time whatsoever to learn anything new without burning myself out since I'd probably be working full-time. I'm thinking about taking a class or two this spring semester at my community college and was initially going to take programming/computer-related classes, but I feel like even though I'm abysmal at math, I'd still have an easier time figuring that shit out along with the programming myself at home than the economics stuff… unless anyone here feels differently based on insight or first-hand experience.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  12/08/17 (Fri) 03:29:24 ID: 2cc583  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234893)[4893](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4893)

Well, I ended up signing up for an intro economics course with my local community college and will be taking it online in late January of next year. I just hope it was the right decision, especially considering I'm partially paying for it.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  12/20/17 (Wed) 22:31:04 ID: a328e8  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234908)[4908](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4908)[\>>4938](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234938)

OP, do you keep the exercises that you did, organized or do you just throw them in a binder? I have a stack of sheets of paper in a corner in my room, but I just keep them there gathering dust in case I need to re-read. I haven't felt the need to go back though, but if I follow the method of looking at the exercises first and then the theory, then I might have to keep my exercises in a neat order if I ever need to go back, since I don't have notes(or as many).

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  01/16/18 (Tue) 19:10:42 ID: 51b849  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234921)[4921](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4921)[\>>4936](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234936)

Hey OP or whoever wrote this

\>>LH2L

\>Yeah, it was 'mostly' common sense bull, but having a complete and thorough reminder of it was really nice. I can post my pdf of the notes I took if you'd like. I just powered through it one evening after putting it off for so long.

Please do. I've done LH2L about a year ago, I have some anki cards about it, but it would be nice to refresh the knowledge and the habits.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  02/07/18 (Wed) 19:06:36 ID: bcea5d  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234936)[4936](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4936)

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  02/07/18 (Wed) 19:09:49 ID: bcea5d  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234937)[4937](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4937)

You don't \*need\* any econ or programming knowledge to invest in bitcoin. More knowledge can't hurt though, and I'd take a hard look at alternative coins too. You won't be mining BTC, but you can mine alts with a GPU.

\>$2,000 total

Yes, it is. I turned $100 into $6,000 recently by buying RaiBlocks at $0.7. Don't count on this though, and you just have to patient, dilligent and quick to act before the market wises up.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  02/07/18 (Wed) 19:11:38 ID: bcea5d  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234938)[4938](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4938)

I'm not OP, but I find value in keeping the exercises. But ultimately, you want the information to be easily accessable in your head, not via searching through papers. So I weigh spaced recall and interleaving as far more important.

I keep boiled down notes and reminders in .tex files too.

  

\>Basic Mathematics by Serge Lang

Its got no solutions, being a math retard I am just suppose to assume I am correct with every exercise?

You had me so hopeful OP but now I am doubting you

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  02/20/18 (Tue) 18:54:32 ID: cb52f2  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234962)[4962](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4962)[\>>4963](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234963)

Seems I am just a normal retard and not just a math retard solutions (though not complete solutions) are at the back of the book and not at the end of each chapter

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  02/21/18 (Wed) 03:34:45 ID: bcea5d  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234963)[4963](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4963)

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  02/26/18 (Mon) 00:31:06 ID: 51b849  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234966)[4966](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4966)[\>>5055](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%235055)

What is the fucking point of learning algebraic abstractions? I understand why real analysis (and complex and multivar analysis) is useful, I guess I kinda understand why linear algebra is useful. Probability theory is obviously the top useful thing. So, why would one need more algebra?

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  03/01/18 (Thu) 20:01:39 ID: f6d826  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%234985)[4985](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q4985)[\>>5043](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%235043)

Just in case: First of all, thanks for taking the time to put this together. It's been really helpful for me so far.

I was wondering if you could create a Graduate Research Elective in Formal Methods? It fits with the theme of the curriculum well, and I believe it's particularly difficult for those of us outside of academia to find quality resources for. At least, I've really struggled to get my head around it - moreso the math/logic/theory than the tools.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  04/10/18 (Tue) 00:11:55 ID: bcea5d  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%235043)[5043](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q5043)

he hasn't posted in ages, but out of curiousity how far along are you and where did you begin?

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  04/17/18 (Tue) 11:30:18 ID: 436096  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%235055)[5055](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q5055)

When you're modeling a system, certain objects might end up forming algebraic structures. Recognizing those structures will tell you properties about it that might not be obvious. Also, Algebra is being used in a lot of CS fields. To give some examples, a lot of people into Haskell and functional programming often talk a lot about category theory. People who study graphs might use Algebraic Combinatorics. Elliptic Dual Curve Cryptography requires a good understanding of algebraic geometry and groups to really understand what's going on. As you get more and more into mathematics, algebraic structures really begin to appear everywhere. Even simple operations such as modulos can be viewed algebraically.

As a math a major I really should be able to give you a better answer, but this is all I have for now. Hopefully I'll have a better answer later (or someone else can answer)

Here's a link as well you should read:

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  05/06/18 (Sun) 09:26:05 ID: 5ad553  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%235076)[5076](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q5076)

This book is a fucking nigger.

No enrtry level explanations for retards such as myself, only for people who are already smart.

Fuck this book.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  05/08/18 (Tue) 00:20:39 ID: c4351a  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%235079)[5079](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q5079)[\>>5082](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%235082)

Where'd you go, anon? I have an idea for a neat collaboration project we could work on. The idea was based directly off of this conversation and the struggles we had in setting something up.

  

Hey anon, glad to hear from you again! Also funny coincidence that I hadn't checked this page in months and today I find your message…

I'm here, I graduated, and I am reading a lot in my free time - I bought quite a bunch of the books mentioned in this thread, thanks to a temporary job I took as an engineer recently.

What's the best way we could go on with this conversation without the risk of losing touch?

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  05/09/18 (Wed) 06:59:17 ID: f80029  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%235082)[5082](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q5082)[\>>5087](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%235087)

This was obviously meant as a reply to

  

Well, I kind of think it's a shit idea now. But at any rate, the plan was to implement something that would hypothetically make the process of both finding people to work through resrouces with and actually working through material with others much easier.

I tried discussing it in more length here:

Basically using Matrix chat protocol with GitTea and KeyBase for file hosting, and then finding or creating some forum organized by topic heirarchies, from general topics to specific resources (example: math → calculus → Spivak), making it easy to find advice and communities at all levels. At any given moment, there are thousands of people working through any given canonical resources, and if they could be united in a de facto, standard, go-to platform it'd make learning by oneself be a much more enjoyable experience.

Ultimately though, perhaps the autodidact path is doomed to be a lonely one. People are inconsistent, have real lives going on outside of studying in their free time, etc etc.. Resources already exist like StackExchange, IRC and subs like /r/GetStudying (but it's pretty gay imho, nothing like the en masse platform I envisioned. But by using a combination of them, you can in essence accompish the same thing, I guess. That, and there are a few shitty looking platforms that already exist and do essentially the same thing, but in a less freetard approved way, afaict.

And congrats on graduating and landing a job, I was suprised to see a response here at all, especially so quickly. I've just been trying to think of a neat way to test my skills outside of a cookie cutter cirriculum/course/book, and I think taking on something creative and innovative would really grind my lackluster skills and result in a higher level of programming maturity. This was just a problem I've encountered a lot, so when I thought of a potential solution I got pretty excited at the thought.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  05/12/18 (Sat) 19:19:51 ID: 9116d0  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%235088)[5088](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q5088)

\>subs like /r/GetStudying (but it's pretty gay imho, nothing like the en masse platform I envisioned

\*)

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  05/15/18 (Tue) 19:53:30 ID: 9a7338  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%235089)[5089](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q5089)

Hey! I am more and more convinced that there is no such thing as a shit idea, because execution is what really matters. Lots of successful products, lots of famous apps came from ideas that were already implemented, but badly - or not good enough.

Personally, I liked your post on 4/sci/ and I think your idea has got potential. The only major drawback is that people are lazy, they don't follow through their plans, not many are really committed to their goals, and thus a study related app that really works can only be aimed at that niche of people that are already trying to do something.

Maybe we can really do something about it.

But in the meantime, what are you trying to study (except Spivak, I guess) and would you like to finally start attacking some book together?

  

OP here, I'm back, even if this is the 'heathen' board with Jim hiding out in the phils. No idea the current state of hot wheels. Update what I'm doing. this: [https://functionalcs.github.io/curriculum/](https://archive.md/o/sud91/https://functionalcs.github.io/curriculum/)

I'm killing bounty's for gitcoin, working for a sleazy finance corp on the down low, and also conducting my life in a non-brainlet way just trying to use probability to estimate my success in really stupid things I come up with. I reworked the math section, you will understand exactly what is happening.

Ignore all my previous advice, I was a brainlet on maximum cruise control just lucking out. I'll see you guys in the underverse, because we're all banned now thanks to clowns going full retard. It's just memes, never forget the fallen memes.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  04/12/19 (Fri) 00:22:17 ID: 852e17  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%235303)[5303](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q5303)[\>>5304](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%235304)

\>gitcoin bounties

what does this look like? can you talk about your workflow for this?

if you find time, a post on some worthwhile hustles like that would be cool (despite it working directly against your self-interest..). I have a lot of spare time and could use some cash or whatever, I'll drop an email if you want

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  04/12/19 (Fri) 00:34:58 ID: 852e17  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%235304)[5304](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q5304)

oh, and can you expand on

\>just trying to use probability to estimate my success

it sounds entertaining yet pragmatic

  

Newfag here.

Can this help me rebuild my forgotten math background from 0? Third world education more or less didn't care as long as you passed.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  04/13/19 (Sat) 21:01:03 ID: 3ae53a  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%235308)[5308](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q5308)[\>>5310](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%235310)

Yes - there is a section in the guide that specifically addresses this concern. Specifically:

Start now, go fast, and don't look back.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  04/15/19 (Mon) 09:42:40 ID: c500fa  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%235310)[5310](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q5310)

This is me.

Thank you, that will help me alot.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  05/04/19 (Sat) 09:11:28 ID: fa6885  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%235332)[5332](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q5332)

Lmao didn't knew the author of functionalcs posts here too. Anyways I'm currently going through the Common Lisp alternate route and Discrete Mathematics with Functional Programming. So far so good.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  06/20/19 (Thu) 02:37:51 ID: 8f2ae9  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%235384)[5384](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q5384)[\>>5422](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%235422)

Always try to get an intuitive understanding( don't be afraid of using images to get the point across). Don't fall for the memorizing formulas trap like I did for most of my pre-University education

When I stopped believing that math was supposed to be hard, I started finding ways to understand it. Now, I ace most classes and I spend my spare time learning about automata

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  07/04/19 (Thu) 12:57:48 ID: beb48d  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%235395)[5395](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q5395)[\>>5414](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%235414)

One of the best threads I've seen in my entire life.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  07/08/19 (Mon) 18:15:33 ID: d60d13  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%235397)[5397](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q5397)

  

I hope so because I'm the OP, and it's cringe to see my old self preserved years ago shitposting on cruise control in the dungeons of the internet (how do I sage myself), usually after being all night at a concert/bar and wasted off my ass . Back then I was listening to Burzum - Fallen nonstop after drinking where you're alone in those early hours hacking away doing something stupid at 4am, and there was a paradox in the lyrics I chased down which got me interested again in academia. During this period I was working a really awful working class labour job with tons of overtime, essentially back breaking labour. Then I started to do the texts that everybody said were 'impossible' to do. But I did not do these resources correctly, I basically just read them, did a few exercises, thought I knew the material, went into full naive scientist mode and then ran into a brick wall later doing more advanced material, I had to go back and re-do everything. So that is what [https://functionalcs.github.io/curriculum/](https://archive.md/o/sud91/https://functionalcs.github.io/curriculum/) is, it is a redo where I realized I did a half assed job the first time.

Anybody reading this in (current year), I'm going to redo the math section, and throw out most of this, primarily shilling Apostol as the best way to build your math skills but I'll include my own notes, I wrote a small book for every resource which again, I take for granted that it helped me learn these topics.

The university job I had I didn't have a degree at the time, and you don't need one either. All univeristies hire for research programmers and local students don't take these jobs because they don't pay enough and they are off chasing that startup gold or trying to intern for FAANG (Facebook, Amazon, Apple, Netflix, Google). So you can weasel your way in, especially if you know specific skills like say, the 15-210 parallel algorithms text which was directly responsible for me being hired. Once you get in, you now learn directly from PhDs, on a daily (or in my case weekend) basis. Then you will see how somebody at that level operates in real time, showing up and telling you how they spent 4 hours that morning digesting some incredibly difficult paper or spent a week learning an impossibly dense text. It was when I met these researchers I realized my work output was insufficient and I needed to redo everything all over again, starting with Apostol.

Anyway tl;dr eventually I'm going to re-do the math section into it's own site, targeted to a pleb like myself when this was written who had the worst math background, and I'll include detailed walkthrough notes so you don't need to do precalc. That's sort of what JK did with [https://pimbook.org/](https://archive.md/o/sud91/https://pimbook.org/) but even that is too advanced for my former self and assumes too much.

I also live in a totally different world than when I wrote this. If you've ever seen that terribad movie Deadpool, there's a grimey alley scene where it's pissing rain outside a strip club. That was shot the night I wrote this thread IIRC. I lived 3 floors up facing that alley in what can only be described as an industrial shithole in one of the worst neighborhoods in the world. They came back to reshoot something with fake rain and there were spotlights shining in my window annoying me and I couldn't study, so I wrote this thread. tl;dr education is the key for getting out of a personal hell. Good luck and hopefully one day this thread will die

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  07/21/19 (Sun) 08:14:11 ID: f5eaa4  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%235422)[5422](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q5422)[\>>5460](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%235460)

This. As long as you understand what mathematical relationships mean, then you can understand why the mathematical relationships work. To be able to do this requires a solid background understanding in fundamental mathematical ideas. Go back to the basics and understand "why" rather than memorizing "what".

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  07/27/19 (Sat) 03:54:34 ID: 534dc8  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%235447)[5447](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q5447)

Yeah, no. This thread shall not be left to die, this has helped/ is helping/ will help others so it's too important now to just go away. I am currently at coordinates from Dover.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  07/27/19 (Sat) 05:21:00 ID: 9c4285  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%235448)[5448](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q5448)

Too late bro. I save this thread every time I visit the board

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  08/03/19 (Sat) 23:22:49 ID: d52371  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%235460)[5460](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q5460)[\>>5463](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%235463)

The way I learned math was just understanding the 'abstractions'.

Most of the real/complex plane are algorithms that produce an output, then they are attached to real line like they're just a number, like say, Pi, but they're not, they are a seperate computation that you have to understand before you get their abstract attachment to the real or complex line/plane. After you understand this (by writing your own examples), it sort of makes sense and you can begin to understand manipulating these algorithms as just 'objects'. You also realize why proofs of these things are so hard, because you're not just writing a proof for it's abstraction you're digging deep into the internals of whatever it represents and trying to prove that complex thing. Hopefully this makes sense.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  08/03/19 (Sat) 23:48:25 ID: 267e80  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%235463)[5463](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q5463)[\>>5465](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%235465)

\>Most of the real/complex plane are algorithms that produce an output, then they are attached to real line like they're just a number, like say, Pi, but they're not, they are a seperate computation that you have to understand before you get their abstract attachment to the real or complex line/plane.

This makes no sense. There are real numbers you can't compute, such as Chaitin's constants, but I'm not even sure you're talking about that.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  08/04/19 (Sun) 00:05:21 ID: d52371  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%235464)[5464](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q5464)

I'm also writing an entire solution guide to starting at math from zero and working up. I don't know how long it will take, and also it's probably a bad idea to provide a solution guide, because I think the way I learned was because I didn't have a solution guide, so I needed to communicate my proofs to people on stack exchange and ask them if my logic was trash or not. Proofs really can't have a final answer, because anybody can write another proof like Ramanujan and his weird proofs of number theory he sent to Hardy back in the day that were legit but totally different than from what they were doing. Given an exercise to write a proof, every single one of us will come up with a different answer, and most of those will be correct. This is the problem with this level of math, you honestly need some kind of mentor to help you with the logic because your naive logic might actually be correct. If you look at the answer, you will be discouraged thinking "wow I don't know this at all, look at this answer it's totally different from how I approached it" but you still may be right! You could also be completely wrong despite being convince you aren't. This is the difficulty of self learning math and hopefully I'll try to help with this by mimicking what I did to learn this material, inspiring some other anon to do the same.

I'm also writing a walkthrough for MIT's crash course in web programming, here: [http://webdevelopment.mit.edu/2018/lectures](https://archive.md/o/sud91/webdevelopment.mit.edu/2018/lectures) and here: [http://weblab.mit.edu/schedule/](https://archive.md/o/sud91/weblab.mit.edu/schedule/) because I enjoy the art of the hustle, making money competitively on those terrible freelancer sites and from starting from zero. I also encourage any anon here to learn OCaml, and watch Jane Street's incremental dom lecture on YouTube. A webdev framework in OCaml, no javascript knowledge needed. React uses 'indirection' to create their virtualDOM and provide you with a functional interface, but you can skip all this and go straight to incr\_dom and just write directly in OCaml and produce some pretty incredible things. If you're interested see [https://www.janestreet.com/tech-talks/intro-to-incr-dom/](https://archive.md/o/sud91/https://www.janestreet.com/tech-talks/intro-to-incr-dom/) and just think about a virtualDOM (a tree structure) and how you can use 'indirection' to shadow it and then perform some of the miracles the girl displays in the talk. Good luck anons

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  08/04/19 (Sun) 00:34:33 ID: d52371  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%235465)[5465](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q5465)

Ryan O'Donnel covers this in the complexity theory lectures as Chaitlin was also at CMU. This is also in the Oregon Summer School Programming lectures when they talk about Per Martin-Löf papers and is one of the reasons for higher computational type theory because some things are uncomputable which is why they abandoned HoTT. Chaitlin also has a set of excellent lectures on YouTube if you're interested.

  

[▶](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23 "Post menu")Anonymous  08/04/19 (Sun) 19:15:52 ID: a5c02f  [No.](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%235468)[5468](https://archive.md/o/sud91/https://8ch.net/prog/res/3034.html%23q5468)

tfw stuck on the preliminaries for over a year because they keep changing and have to start over
