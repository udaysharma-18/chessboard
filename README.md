
<!DOCTYPE html>
<html>
<head>

    <title>Dynamic Chessboard</title>

    <style>

        body {
            text-align: center;
            font-family: Arial;
        }

        #chessboard {
            width: 400px;
            height: 400px;
            margin: 30px auto;

            display: grid;

            grid-template-columns: repeat(8, 1fr);
            grid-template-rows: repeat(8, 1fr);

            border: 3px solid black;
        }

        .cell {
            width: 50px;
            height: 50px;
        }

    </style>

</head>

<body>

    <h2>Dynamic Chessboard</h2>

    <div id="chessboard"></div>

    <script>

        let board = document.getElementById("chessboard");
        for (let i = 0; i < 8; i++) {
            for (let j = 0; j < 8; j++) {
                let cell = document.createElement("div");
                cell.className = "cell";
                if ((i + j) % 2 === 0) {
                    cell.style.backgroundColor = "white";
                }
                else {
                    cell.style.backgroundColor = "black";
                }
                board.appendChild(cell);
            }
        }

    </script>

</body>
</html>
