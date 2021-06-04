# Prework review

Hi Nicole 🙋🏻‍♀️!! I am writing to give you some feedback on your prework! 🚀

### 1. Snail-and-Well
Let's go with the first challenge! 

- *Find the solution to the challenge using the variables defined above.*

    In this exercise you did't consider the distance that the snail slides every night, so... 

    ```python
    while snail_position <= well_height: #if the the snail position is less than the well_height
        days += 1 # sum a day in the counter
        snail_position += daily_distance # sum the distance it reaches
        if snail_position <= well_height: # if the snail is in the well, then we have to subtract what falls during the night
            snail_position -= nightly_distance
    ```
- Really nice great that you will be interested in doing the bonus
  ```python
  while snail_position <= well_height:
    snail_position += advance_cm[days]
    if snail_position <= well_height:
        snail_position -= nightly_distance
    days += 1 # be care here, in this code you are adding days regardless of the nightly displacemnts, because the days sum are is out of the loop. 
    
    print("It would take {} days.".format(days))
  ```
### 2. Duel-of-Sorcerers

Let's go with th battle!

The first part of this challenge is perfect. Only as a detail:
- In python it is a convention that when we do a `for` or a `if` or a `while` or a `function`... (anything that is accompanied by a colon) the code that follows is put on the following line. So, you code should be like this
  ```python
  for a,b in zip(gandalf,saruman):
    if a>b: 
        gandalf_wins +=1
    else: 
        saruman_wins +=1
  ```
    In the bonus part, I have seen that you have had some problems in the exercise 4 *The battle starts! Using the variables you've created above, code the execution of spell clashes. Remember that a sorcerer wins if he succeeds in winning 3 spell clashes in a row* Firstly, good job using `zip` method, it is really usefull when we want to iterate through two list. I'm trying to explain the best solution to this exercise, but if you any doubt tell me and we can see the solution more detailed.

    ```python
    for g,s in zip(gandalf_power,saruman_power):
        #using this for we will iterate trought the two list and we can compare the iterable elements
        if g > s:
            #now we compare each element of the list. As the sorcerers has to win three times in a row, when gandalf wins what we do is reset saruman's win counter, and vice versa.
                gandalf_wins += 1
                saruman_wins = 0 #reset the saruman counter to 0
                if gandalf_wins == 3:
                    print(f'Gandalf has won {gandalf_wins} clashes in a row, he is the winner of the battle!\n')
                    break
                
        # and the same code with saruman    
        elif g < s:
                saruman_wins += 1
                gandalf_wins = 0
                if saruman_wins == 3:
                    print(f'Saruman has won {saruman_wins} clashes in a row, he is the winner of the battle!\n')
                    break
                
        else:
            print('There has been a tie\n')
    ```
    In any case, if you have any question tell meeeeee
Finally, suuuper that you used `statistics` to calculate the mean and stdev! Fantastic 🔥

### 3. Bus

Perfect this challenge Nicoleeee 👏🏽👏🏽

### 4. Robin-Hood

 - As a detail, when we create a variable or iterate using a for loop it is important that we don't use `key words` as `list`, `set`, `key`, `tuple`... If you want to create a variable with the name "list" you could use a low bar (or choose another name). In your case, you use the key-word `tuple` in a for loop
  
  ```python
  for tuple in points:
    if ((tuple[0]) > 0) & ((tuple[1]) > 0): 
        Q_1 += 1
   ...

    # I recommend you to change tuple to another word
            
  ```

### 5. Temperature-Processor

Good job Nicoleeeeee!!! 


### 6. Rock–Paper–Scissors

Let's go with the last exercise! Overall, you have done really good job in this challenge. I give you some tips related to this exercise that i hope that help you!

- In the exercise 8 *Define a function that checks who won a round.* 
  The code it is perfect, but we could optimize our code using the `or` and `and` operators and reduce the number of lines. It is good practice to try to avoid repeating lines of code that are too similar. One possible solution in this case could be: 

  ```python
    if player_gesture == cpu_gesture: 
        print(0)
    elif (player_gesture == 'r' and cpu_gesture == 's') or (player_gesture == 's' and cpu_gesture == 'p') or (player_gesture == 'p' and cpu_gesture == 'r'):
        print(1)
    else: 
        print(2)
  ```

 - The bonus exercise was similar to rock, paper, scissors, the only thing we should do is add two more possible options.

- Finally, in this exercise we needed to used functions, what are the functions? A function is a block of organized, reusable code that is used to perform a single, related action. Functions provide better modularity for your application and a high degree of code reusing.


    -  The components of the definition are: 
        - **def**	The keyword that informs Python that a function is being defined
        - **<function_name>**	A valid Python identifier that names the function
        - **<parameters>** parameters that may be passed to the function
       - **<statement(s)>**	A block of valid Python statements
Here more documentation about functions [here](https://www.programiz.com/python-programming/function)

either way, you have done really good job in the prework Nicole! 👏🏽🎉🔥🔥
