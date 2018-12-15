# Clean Code

#### DRY, YAGNI
#### D-Dirty C-Clean   
### Naming:
###### 1) naming matters - better variable names
```
D:Int t = 0
C:Int total = 0
```      
###### 2) classes   
Single responsibility - be specific - nouns not verbs - avoid generic suffixes   
```
D: MyFunction
C: User, Account
```   
###### 3) methods
```
D: get, pending
C: getRegisteredUsers, isValidSubmission
```
###### 4) Warning signs   
And, or , if (too much work)   

###### 5)checkPassword shouldn’t log users out   
Validate submission shouldn’t save   
getUser shouldn’t save their session      

###### 6)Abbreviations   
Don’t use them, use long descriptive names   
```
D:RegUse
C:RegisteredUser
```   
###### 7) Booleans   
```
D: open, login if(login) {}
C: isOpen, loggedIn if(loggedIn) {}
```
###### 8)Symmetry   
D: on/disable, slow/max
C: on/off, min/max

### Conditionals
###### 1) comparisons
```
D:If(loggedIn == true) {}
C: if(loggedIn)
```

###### 2) assignments  
```
D: bool goingForChiptole;
if(cashInWallet > 6.0){
goingForChiptole = true
} else{
goingForChiptole = false
}
C:  bool goingForChiptole =  cashInWallet > 6.0;
```

###### 3) positive conditionals
```
D: if (!isNotLoggedIn)
C: if( loggedIn)
```

###### 4) Ternary Elegance
```
D: usual if else
C: int registrationFee = isSpeaker ? 0 : 50;
```

###### 5) Stringly Typed
```
D: if (employeeType == “manager”)
C: if (employee.Type == EmployeeType.Manager)
```

###### 6) Magic numbers
```
D: if( age > 21)
C: if( age > legalDrinkingAge) if (status == Status.Active)
```

###### 7) Complex conditionals
```
D: if(age > 56 && retired == true)
C: bool eligibleForPension =  age > 56 && retired == true | if (eligibleForPension)
```

###### 8) Use Polymorphism vs If/Switch   
###### 9) Be Declarative   



### Functions
###### 1) Avoid pyramid of doom   
###### 2) Return early
```
D: If (){
	if(){
	}
}
return something;

C: if() return false
    if() return false
    ```
###### 3) Fail fast   
Same as above but throw an exception (guard in swift)
###### 4) Convey Intents   
```
D: If ( s == true || a == false)
C: if(ValidRequest(s,a))
```
###### 5) Do one thing   
###### 6) MayFly variable   
Initialise variable just in time where its required , do one thing

###### 7) Parameters   
Strive for 0-2 parameters
```
D:
private void saveUser(User user, bool emailUser){
 // save user
	if(emailUser){
		//email user
	}
}
C:
private void saveUser(User user){
	// save user
}

Private void emailUser(User user){
	// email user
}
```
Rarely < 20 line, Hardly > 100 lines no more than 3 parameters - clean code

###### 8) Exceptions   
Unrecoverable - Null Reference, FNF, Access denied   
Recoverable - Retry , Wait and try   
Ignorable - Logging click   

### Classes:
###### 1) High cohesion
```
D:
Vehicle
Edit vehicle options
Schedule maintenance
Select financing
C:
Vehicle
Edit vehicle options
VehicleMaintenance
Schedule maintenance
VehicleFinance
Select financing
```

### Comments
1) Let code do the talking   
2) leave metadata to git   
3) don’t leave commented code   
4) add TODO if necessary   

### Stay Clean:
1) Don’t refactor everything - Legacy code is well tested code   
2) Code review & Pair programming   
3) Leave the code better than you found it, then your code is always clean   


References   
https://github.com/JuanCrg90/Clean-Code-Notes
https://github.com/jbarroso/clean-code
https://github.com/abiodunjames/Awesome-Clean-Code-Resources
