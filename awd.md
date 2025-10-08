##### 1. Implement Depth First Search (DFS) Algorithm. 
```
graph1 = { 
    'A': set(['B', 'C']), 
    'B': set(['A', 'D', 'E']), 
    'C': set(['A', 'F']), 
    'D': set(['B']), 
    'E': set(['B', 'F']), 
    'F': set(['C', 'E']) 
} 
def dfs(graph, node, visited): 
    if node not in visited: 
         visited.append(node) 
         for n in graph[node]: 
             dfs(graph,n, visited) 
    return visited 
visited = dfs(graph1, 'A', []) 
print(visited)
```
##### 2. Implement Breadth First Search (BFS) Algorithm. 
```
graph={ 
    '5':['3', '7'], 
    '3':['2','7'], 
    '7':['8'], 
    '2':[], 
    '4':['8'], 
    '8':[] 
    } 
visited=[] 
queue=[] 
def bfs(visited,graph,node): 
    visited.append(node) 
    queue.append(node) 
    while queue: 
        m=queue.pop(0) 
        print(m,end="") 
        for neighbour in graph[m]: 
            if neighbour not in visited: 
               visited.append(neighbour) 
        queue.append(neighbour)  
print("Breadth First Search") 
bfs(visited,graph,'5') 
```
##### 3. Solve Tower of Hanoi Problem.
```
def moveTower(height, fromPole, toPole, withPole): 
if height >= 1: 
moveTower(height-1, fromPole, withPole, toPole) 
moveDisk(fromPole, toPole) 
moveTower(height-1, withPole, toPole, fromPole) 
def moveDisk(fp, tp): 
print("moving disk from ", fp ,"to ", tp) 
moveTower(3, "A", "B", "C")
```
##### 4. Simulate tic-tac-toe game using min-max algorithm.
```
import os  
import time  
board = [' ',' ',' ',' ',' ',' ',' ',' ',' ',' ']  
player = 1  
win = 1  
Draw = -1  
Running = 0  
Stop = 1  
Game = Running  
Mark = 'X'  
def DrawBoard():  
          print("  %c  |  %c  |  %c  "%(board[1],board[2],board[3]))  
          print("  %c  |  %c  |  %c  "%(board[4],board[5],board[6]))  
          print("  %c  |  %c  |  %c  "%(board[7],board[8],board[9]))  
def CheckPosition(x):  
          if(board[x] == ' '):  
                    return True  
          else:  
                    return False  
def CheckWin():  
          global Game  
          if(board[1] == board[2] and board[2] == board[3] and board[1] != ' '):  
                    Game = win  
          elif(board[4] == board[5] and board[5] == board[6] and board[4] != ' '):  
                    Game = win  
          elif(board[7] == board[8] and board[8] == board[9] and board[7] != ' '):  
                    Game = win  
          elif(board[1] == board[4] and board[4] == board[7] and board[1] != ' '):  
                    Game = win  
          elif(board[2] == board[5] and board[5] == board[8] and board[2] != ' '):  
                    Game = win  
          elif(board[3] == board[6] and board[6] == board[9] and board[3] != ' '):  
                    Game = win  
          elif(board[1] == board[5] and board[5] == board[9] and board[1] != ' '):  
                    Game = win  
          elif(board[3] == board[5] and board[5] == board[7] and board[3] != ' '):  
                    Game = win  
          elif(board[1] != ' ' and board[2] != ' ' and board[3] != ' ' and board[5] != ' '  and 
board[6] != ' '  
and board[7] != ' ' and board[8] != ' ' and board[9] != ' ' ):  
                    Game = Draw  
          else:  
                    Game = Running  
print("Tic-Tac-Toe Game")  
print("Player 1[X]-----Player 2[O]\n")  
print()  
print()  
print("Please Wait.....")  
time.sleep(1)  
while(Game == Running):  
          os.system('cls')  
          DrawBoard()  
          if(player%2 != 0):  
                    print("Player 1's chance  ")  
                    Mark = 'X'  
          else:  
                    print("Player 2's chance ")  
                    Mark = 'O'  
          choice = int(input("Enter the position: "))  
          if(CheckPosition(choice)):  
                    board[choice] = Mark  
                    player+=1  
                    CheckWin()  
os.system('cls')  
DrawBoard()  
if(Game==Draw):  
          print("Game Draw")  
elif(Game==win): 
    player-=1 
    if(player%2!=0): 
print("Player 1 won")  
else: 
print("Player 2 won") 
```
##### 5. Shuffle deck of cards.
```
import itertools, random 
deck = list(itertools.product(range(1,14),['spade','Heart','Diamond','Club'])) 
random.shuffle(deck) 
print("Your got: ") 
for i in range(5): 
print(deck[i][0], "of", deck[i][1])
```
##### 6. Solve constraint satisfaction problem. 
```
(WA,SA,NT,QU,NSW,VI):- 
different(WA,SA), 
different(WA,NT), 
different(NT,SA), 
different(NT,QU), 
different(SA,QU), 
different(SA,NSW), 
different(SA,VI), 
different(QU,NSW), 
different(NSW,VI). 
different(red,blue). 
different(blue,red). 
different(blue,green). 
different(green,blue). 
different(green,red). 
different(red,green).
```
##### 7. Derive the expression based on Associative Law. 
```
associative_law(A, B, C, Result):- Result is A+(B+C). 
exp1(2,3,4). 
exp2(5,6,7). 
derive_results:- 
exp1(A,B,C), 
associative_law(A,B,C,Result1), 
exp2(X,Y,Z), 
associative_law(X,Y,Z,Result2), 
write('Results of expression1 using associative law: '),write(Result1),nl, 
write('Results of expression2 using associative law: '),write(Result2),nl. 
```
##### 8. Derive the expression based on Distributive Law. 
```
distributive_law(A,B,C,Result):- Result is A*(B+C). 
exp1(2,3,4). 
exp2(5,6,7). 
derive_results:- 
exp1(A,B,C), 
distributive_law(A,B,C,Result1), 
exp2(X,Y,Z), 
distributive_law(X,Y,Z,Result2), 
write('Results of expression1 using distributive law: '),write(Result1),nl, 
write('Results of expression2 using distributive law: '),write(Result2),nl. 
```
##### 9. Derive the predicate (for e.g., Sachin is batsman, batsman is cricketer) -> Sachin is Cricketer. 
```
batsman(williamson). 
bowler(boult). 
keeper(marsh). 
cricketer(X):-batsman(X);bowler(X);keeper(X). 
```
##### 10. Write a program which contains three predicates: male, female, parent. Make rules for following family relations: father, mother, grandfather, grandmother, brother, sister, uncle, aunt, nephew and niece, cousin.Question:i. Draw Family Tree. ii. Define: Clauses, Facts, Predicates and rules with conjunction and disjunction.
```
male(adam). 
male(george). 
male(john). 
male(steve). 
female(ana). 
female(steffi). 
female(eve). 
female(alice). 
parent(adam, george). 
parent(adam, steffi). 
parent(eve, george). 
parent(eve, steffi). 
parent(george, john). 
parent(ana, john). 
parent(steffi, alice). 
parent(steve, alice). 
mother(X,Y):- parent(X,Y),female(X). 
father(X,Y):- parent(X,Y),male(X). 
sister(X,Y):- parent(Z,X),parent(Z,Y),female(X),X\==Y. 
brother(X,Y):- parent(Z,X),parent(Z,Y),male(X),X\==Y. 
grandfather(X,Z):- father(X,Y),parent(Y,Z). 
grandmother(X,Z):- mother(X,Y),parent(Y,Z). 
siblings(X,Y):- ((brother(X,Y);sister(X,Y)),X\==Y). 
uncle(X,Y):- parent(Z,Y),brother(X,Z). 
aunty(X,Y):- parent(Z,Y),sister(X,Z). 
cousin(X,Y):- parent(A,X),parent(B,Y),siblings(A,B). 
```