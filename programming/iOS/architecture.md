# Architecture

## Better MVC

https://davedelong.com/blog/2017/11/06/a-better-mvc-part-1-the-problems/
https://www.youtube.com/watch?v=YWVzCd5FYbs&feature=emb_title


**Problem:**
1. violate encapsulation principles, which ends up leading to spaghetti code
2. Massive View Controller

**Solution:**

1. view controller should manage either sequence or UI, but not both.
2. 1 View Controller ≠ 1 screen of content
3. UICellViewController

**Related:**<BR>
https://www.youtube.com/watch?v=PdkWjdKOqfo<BR>
http://aplus.rs/2017/much-ado-about-ios-app-architecture/
https://www.dotconferences.com/2018/01/ben-scheirman-buckets-of-code

## Coordinator Pattern

https://www.hackingwithswift.com/articles/71/how-to-use-the-coordinator-pattern-in-ios-apps
