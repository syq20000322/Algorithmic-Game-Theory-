## Setting 

#### • Participants 

-  A set of leaders L = {l, … , n} 
-  A set of followers F = {f, … , n}

####  • Preferences

 • Each leader has strict preferences over all followers

 • Each follower has strict preferences over all leaders 

#### • Objective 

• To find a **one-to-one stable** matching

- (one-to-one) Matching: each leader is paired with at most one follower and vice versa 
- Stable: no pair (l, f) wants to deviate 

• A **matching is stabl**e if 

 	• There is no leader-follower pair, each of whom would prefer to match with each other rather than their assigned partner.

 • Such a pair is called a **blocking pair**

![blocking pair](http://m.qpic.cn/psc?/V51UtlER36fYng45Fb5k3ktWYR4BINB0/ruAMsa53pVQWN7FLK88i5ukQ3dejNCWGHm2DL8SJNDswhLEOvIj4gf1RlQelPZpmyJuzxUUKum*6b0I1KfO62d.6BTA9fkRUe37rzkZBEqE!/b&bo=yATTAQAAAAADBzw!&rf=viewer_4)

**Theorem (Gale-Shapley algorithm)**

A stable matching always exists, and can be found in polynomial time



```c
Deferred-acceptance-leader-oriented (leaders, followers, preferences)
 Assign all leaders and followers to be free; //initial state
 While (some leader l is free and hasn’t proposed to every follower)
     f = first follower on l's list to whom l hasn't yet proposed;
	// next: l proposes to f
 	If (f is free)
 		assign l and f to be engaged; //tentatively matched
 	else if (f prefers l to her fiancé l') { //f is engaged
 		set l and f to be engaged;
 		set l' to be free;
 	else f rejects l; //and l remains free
 output the n engaged pairs, who form a stable matching;
```

Example

![stable matching](http://m.qpic.cn/psc?/V51UtlER36fYng45Fb5k3ktWYR4BINB0/ruAMsa53pVQWN7FLK88i5jBFtKYo5Vy02zdMzIR1zeWhRe0aD*OvGthplDSWzN9KCJ6a66mXxgvzNs81zbWIYFclZMJyR*uh4dVw0lVnxqA!/mnull&bo=5wMQAgAAAAADB9Q!&rf=photolist&t=5)
