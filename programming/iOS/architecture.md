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


What is UIViewController?
User Interface design updating views with model data responding to user input - UIView Subclass
Saving restoring state
DataSources and Delegates - Separate classes
Animation - UIView Subclass
Networking
Navigation


Navigation
Control the flow in your app
Handle the flow in your app
Handle ipad/iphone variants
Handle A/B testing
UIViewController?

A -> Coordinator(Protocol) -> B

Coordinator - Sub-Coordinators


protocol Coordinator {
    var children: [Coordinator] { get set }
    var nav: UINavigationController { get set }
    func start()
}

func userTapper() {
    coordinator.buy(widget)
}

A -> buy
B -> buy
C -> buy

Benefits:
No hardcoded flow
SOLID - S
one flow


## Advanced Coordinators

1. using child coordinators
2. Navigating backwards
3. Passing data between controllers
4. Coordinated tab bar controller
5. Handling Segues
6. Protocol and Closures
