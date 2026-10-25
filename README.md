# 🎮 Tic Tac Toe — Python in Jupyter Notebook

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange)

A simple 2-player Tic Tac Toe game in pure Python, built for learning basics: lists, functions, loops, and input validation.

## ✨ Features
- 2-player mode (Player vs Player)
- Automatic win / draw detection
- Input validation + replay option
- No external libraries

## 🚀 Quickstart

```bash
pip install notebook
jupyter notebook
```

Open `Tic Tac Toe Game.ipynb` and run cells with `Shift + Enter`.

> Works in JupyterLab, VS Code, and Google Colab.

## 🎯 How to Play
Board positions use numpad layout (index `0` unused):

```
 7 | 8 | 9
-----------
 4 | 5 | 6
-----------
 1 | 2 | 3
```

- `player_input()` picks `X` / `O`
- `choose_first()` picks who starts randomly
- Enter `1-9` on your turn (`player_choice`)
- Three in a row wins, full board = draw

## 🧩 Functions

| Function | Description |
|---|---|
| `display_board(board)` | Show board (with `clear_output`) |
| `player_input()` | Choose `X`/`O`, return `(p1, p2)` markers |
| `place_marker(board, marker, position)` | Place marker |
| `win_check(board, mark)` | Check 8 win combos |
| `choose_first()` | Random first player |
| `space_check(board, position)` | Is cell free? |
| `full_board_check(board)` | Is board full? (draw) |
| `player_choice(board)` | Validated `1-9` input |
| `replay()` | Play again? `y/n` |

<details>
<summary>Show win_check code</summary>

```python
def win_check(board, mark):
    return ((board[7] == mark and board[8] == mark and board[9] == mark) or
            (board[4] == mark and board[5] == mark and board[6] == mark) or 
            (board[1] == mark and board[2] == mark and board[3] == mark) or 
            (board[7] == mark and board[4] == mark and board[1] == mark) or 
            (board[8] == mark and board[5] == mark and board[2] == mark) or 
            (board[9] == mark and board[6] == mark and board[3] == mark) or 
            (board[7] == mark and board[5] == mark and board[3] == mark) or 
            (board[9] == mark and board[5] == mark and board[1] == mark))
```

</details>

## 📁 Structure
```
.
├── Tic Tac Toe Game.ipynb
└── README.md
```

## 🔮 Next Steps
- AI opponent (Minimax)
- GUI with `ipywidgets`
- Score tracking

## ⭐ Star if useful!
