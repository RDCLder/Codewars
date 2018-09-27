# Tic-Tac-Toe-Like Table Generator

[6 Kyu Kata](https://www.codewars.com/kata/5b817c2a0ce070ace8002be0)

## Code

```python
def display_board(board, width):
    
    length = len(board) // width
    output = ''
    
    for i in range(length):
        if i == 0:
            for j in range(width):
                if j != width - 1:
                    output += ' {} |'.format(board[j + width * i])
                elif j == width - 1:
                    output += ' {} '.format(board[j + width * i])
        else:
            output += '\n{}\n'.format('-' * (width * 4 - 1))
            for j in range(width):
                if j != width - 1:
                    output += ' {} |'.format(board[j + width * i])
                elif j == width - 1:
                    output += ' {} '.format(board[j + width * i])
    
    return output
    ```
