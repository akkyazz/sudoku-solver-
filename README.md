# sudoku-solver-
Sudoku can be solved by one by one assigning numbers to empty cells. Before assigning a number, check whether it is safe to assign. Check that the same number is not present in the current row, current column and current 3X3 subgrid. After checking for safety, assign the number, and recursively check whether this assignment leads to a solution or not. If the assignment doesn’t lead to a solution, then try the next number for the current empty cell. And if none o
f the number (1 to 9) leads to a solution, return false and print no solution exists
Algorithm: 

Create a function that checks after assigning the current index the grid becomes unsafe or not. Keep Hashmap for a row, column and boxes. If any number has a frequency greater than 1 in the hashMap return false else return true; hashMap can be avoided by using loops.
Create a recursive function that takes a grid.
Check for any unassigned location. If present then assign a number from 1 to 9, check if assigning the number to current index makes the grid unsafe or not, if safe then recursively call the function for all safe cases from 0 to 9. if any recursive call returns true, end the loop and return true. If no recursive call returns true then return false.
If there is no unassigned location then return true.
![Screenshot (11)](https://user-images.githubusercontent.com/52878265/187995996-8337260a-af20-44ca-b723-a316cceccdac.png)
![Screenshot (12)](https://user-images.githubusercontent.com/52878265/187996037-8a5c3ad4-f86f-4c7f-8b4e-5d262f7a1258.png)
![Screenshot (13)](https://user-images.githubusercontent.com/52878265/187996092-8b71840d-e0ad-4148-a5f4-29a86ade9cd7.png)
![Screenshot (14)](https://user-images.githubusercontent.com/52878265/187996142-15697cdb-dca2-4983-a64f-0dac5517bf57.png)

