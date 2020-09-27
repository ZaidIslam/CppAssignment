# Bug 1

1. **The incorrect original code or code snippit that you wrote:**

``` cpp
case 1;
    cout << "Pi times radius squared\n";
  break;


```

2. **What bug does the original code have?**

After case 1; <-- I put ";" instead of ":". 

3. **What misunderstanding of C++ concepts lead you to this incorrect code?**

I understand the concepts but just made a mistake.

4. **How to correct the bug?**

Replace the semicolon ";" with a colon ":".

5. **The corresponding bug-free code or code snippet is:**

``` cpp
case 1:
    cout << "Pi times radius squared\n";
  break;
```

6. **What is the take-away message from this bug?**

That when stating cases for a switch, you need to put a colon.

---

# Bug 2

1. **The incorrect original code or code snippit that you wrote:**

``` cpp
  if (select == 0)
     {
      cout << "Please enter the amount of USD dollars: " << endl;
      cin >> amount;
      conversion = (amount * usd);
      cout << "They can be converted to "<< conversion << " CAD" << endl;
      } 
      
   else (select == 1) 
     {
      cout << "Please enter the amount of CAD dollars: " << endl;
      cin >> amount;
      conversion = (amount / usd);
      cout << "They can be converted to "<< conversion << " USD" << endl;
      }
         
   else 
     {
       cout <<"illegal entry" << endl;
       }

```

2. **What bug does the original code have?**

After the if statement there is an else statement "else (select == 1).
Instead there should be an else if statement.

3. **What misunderstanding of C++ concepts lead you to this incorrect code?**

I thought else and else if statement are the same thing.

4. **How to correct the bug?**

Turn that first else statement to else if statement.

5. **The corresponding bug-free code or code snippet is:**

``` cpp
  if (select == 0)
     {
      cout << "Please enter the amount of USD dollars: " << endl;
      cin >> amount;
      conversion = (amount * usd);
      cout << "They can be converted to "<< conversion << " CAD" << endl;
      } 
      
   else if (select == 1) 
     {
      cout << "Please enter the amount of CAD dollars: " << endl;
      cin >> amount;
      conversion = (amount / usd);
      cout << "They can be converted to "<< conversion << " USD" << endl;
      }
         
   else 
     {
       cout <<"illegal entry" << endl;
       }
```

6. **What is the take-away message from this bug?**

That when there are multiple else statements, you need to use else if. Else is only used when its the last statement in the if statement.  


# Bug 3

1. **The incorrect original code or code snippit that you wrote:**

``` cpp

 float cad{1.0}, usd{1.32};
 float conversion{};
 int select{}, amount{};
 
```

2. **What bug does the original code have?**

There aren't any bugs in this code but I can clean it up and put all the float variables into one statement.

3. **What misunderstanding of C++ concepts lead you to this incorrect code?**

I thought if I initialized a variable I won't be able to put other variables with no value in the same statement.

4. **How to correct the bug?**

Put all the float values in the same statement and use commas to seperate them.

5. **The corresponding bug-free code or code snippet is:**

``` cpp
 float cad{1.0}, usd{1.32}, conversion{};
   int select{}, amount{};
```

6. **What is the take-away message from this bug?**

A variable with {1.32} value and a variable with {} are equivalent since they are both initialized.
