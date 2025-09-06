# Ex.No: 10  Logic Programming –  Simple queries from facts and rules
### DATE: 06-09-2025                                                                           
### REGISTER NUMBER : 212223060066
### AIM: 
To write a prolog program to find the answer of query. 
###  Algorithm:
 Step 1: Start the program <br> 
 Step 2: Convert the sentence into First order Logic  <br> 
 Step 3:  Convert the sentence into Horn clause form  <br> 
 Step 4: Add rules and predicates in a program   <br> 
 Step 5:  Pass the query to program. <br> 
 Step 6: Prolog interpreter shows the output and return answer. <br> 
 Step 8:  Stop the program.
### Program:
### Task 1:
Construct the FOL representation for the following sentences <br> 
1.	John likes all kinds of food.  <br> 
2.	Apples are food.  <br> 
3.	Chicken is a food.  <br> 
4.	Sue eats everything Bill eats. <br> 
5.	 Bill eats peanuts  <br> 
   Convert into clause form and Prove that John like Apple by using Prolog. <br> 
### Program:
```
likes(john, X):-food(X).
food(apple).
food(chicken).
eats(sue,X):-eats(bill,X).
eats(bill,peanuts).
```

### Output:
<img width="945" height="308" alt="Screenshot 2025-09-06 140359" src="https://github.com/user-attachments/assets/472e8c40-bd7e-4d9e-874f-a5e564786bac" />


### Task 2:
Consider the following facts and represent them in predicate form: <br>              
1.	Steve likes easy courses. <br> 
2.	Science courses are hard. <br> 
3. All the courses in Have fun department are easy <br> 
4. BK301 is Have fun department course.<br> 
Convert the facts in predicate form to clauses and then prove by resolution: “Steve likes BK301 course”<br> 

### Program:
```
likes(steve,X):-easycourse(X).
hard(science).
easycourse(X):-dept(havefun,X).
dept(havefun,bk301).
```

### Output:
<img width="946" height="308" alt="Screenshot 2025-09-06 140428" src="https://github.com/user-attachments/assets/9312c716-61f3-425f-a06f-b22dd6c6775c" />


### Task 3:
Consider the statement <br> 
“This is a crime for an American to sell weapons to hostile nations. The Nano , enemy of America has some missiles and its missiles were sold it by Colonal West who is an American” <br> 
Convert to Clause form and prove west is criminal by using Prolog.<br> 
### Program:
```
crime(X):-american(X),weapon(Y),sells(X,Y,Z),hostile(X,Z).
sells(west,Y,nano):-owns(nano,Y),missile(Y).
weapon(Y):-missile(Y).
hostile(B,A):-enemy(A,B).
enemy(nano,west).
owns(nano,m1).
missile(m1).
american(west).
```


### Output:
<img width="932" height="309" alt="Screenshot 2025-09-06 142725" src="https://github.com/user-attachments/assets/8525221c-cbdd-47d6-a2d0-82951ecdf171" />


### Result:
Thus the prolog programs were executed successfully and the answer of query was found.
