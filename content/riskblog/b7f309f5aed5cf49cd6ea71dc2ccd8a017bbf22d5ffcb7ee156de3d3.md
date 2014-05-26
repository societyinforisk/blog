Title: AES on the iPhone isn’t broken by Default
Date: 2011-12-14 17:25:29
Category: Riskblog
Tags: Aggregated_Blogs
Slug: aes-on-the-iphone-isn't-broken-by-default-jay-jacobs-2011-12-14-17:25:29
Author: Jay Jacobs

>[AES on the iPhone isn’t broken by Default](http://beechplane.wordpress.com/2011/12/14/aes-on-the-iphone-isnt-broken-by-default/) originally posted at [Behavioral Security » Risk](http://beechplane.wordpress.com) and syndicated at [SIRA](http://societyinforisk.org)
***
I wanted to title this “CBC mode in the AES implementation on the iPhone isn’t as effective as it could be” but that was a bit too long.  Bob Rudis forwarded this post, “[AES on the iPhone is broken by Default](http://log.nadim.cc/?p=58)” to me via twitter this morning and I wanted to write up something quick on it because I responded “premise is faulty in that write up” and this ain’t gonna fit in 140 characters.  Here is the premise I’m talking about:

> In order for CBC mode to perform securely, the IV must remain impossible for the attacker to derive or predict.

This isn’t correct.  In order for CBC mode to be ***effective*** the initialization vector (IV) should be unique (i.e. random), preferably per individual use.  To correct the statement: **In order for AES to perform securely, the key must remain impossible for the attacker to derive or predict.**   There is nothing in the post that makes the claim that the key is exposed or somehow able to be derived or predicted. 

Here’s the thing about IV’s: they are not secret.  If there is a requirement to keep an IV secret, the cryptosystem is either designed wrong or has some funky restrictions and I’ll be honest, I’ve seen both.  In fact, the IV is so *not secret*, the IV can be passed in the clear (unprotected) along with the encrypted message and it does not weaken the implementation.  Along those lines, there are critical cryptosystems in use that don’t use IV’s.   For example, some financial systems leverage ECB mode which doesn’t use an IV (and has it’s own problems).   Even a bad implementation of CBC is better than ECB.  Keep that in mind because apparently ECB is good enough for much of the worlds lifeblood.

So what’s the real damage here?  As I said in order for CBC to be effective, the IV should not be reused.  If it is reused (as it appears to be on the implementation in the iPhone Nadim wrote about), we get a case where an attacker may start to pull out patterns from the first block.  Which means if the first block contains repeatable patterns across multiple messages, it may be possible to detect that repetition and infer some type of meaning.  For example, if the message started out with the name of the sender, a pattern could emerge (across multiple encrypted messages using the same key and IV) in the first block that may enable some inference as to the sender on that particular message.

Overall, I think the claim of “AES is broken on the iPhone” is a bit overblown, but it’s up to the interpretation of “broken”.  If I were to rate this finding on a risk scale from “meh” to “sky is falling”, off the cuff I’d say it was more towards “meh”.  I’d appreciate this fixed from apple at some point… that is, if they get around to it and can squeeze it in so it doesn’t affect when I can get an iPhone 5…  I’d totally apply that patch.  But I certainly wouldn’t chuck my phone in the river over this.

[![img](/images/blank.png)](#) ![img](/images/blank.png)


