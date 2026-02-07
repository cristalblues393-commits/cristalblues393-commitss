<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pong Game</title>
    <style>
        body {
            margin: 0;
            overflow: hidden;
            background-color: black;
        }
        #pong {
            background: black;
            display: block;
            margin: auto;
        }
    </style>
</head>
<body>
    <canvas id="pong" width="800" height="400"></canvas>
    <script>
        const canvas = document.getElementById('pong');
        const ctx = canvas.getContext('2d');

        class Paddle {
            constructor(x, y, width, height) {
                this.x = x;
                this.y = y;
                this.width = width;
                this.height = height;
                this.score = 0;
            }
            draw() {
                ctx.fillStyle = 'white';
                ctx.fillRect(this.x, this.y, this.width, this.height);
            }
            move(up) {
                if (up && this.y > 0) {
                    this.y -= 5;
                } else if (!up && this.y + this.height < canvas.height) {
                    this.y += 5;
                }
            }
        }

        class Ball {
            constructor(x, y, radius) {
                this.x = x;
                this.y = y;
                this.radius = radius;
                this.speedX = 5;
                this.speedY = 5;
            }
            draw() {
                ctx.fillStyle = 'white';
                ctx.beginPath();
                ctx.arc(this.x, this.y, this.radius, 0, Math.PI * 2, false);
                ctx.fill();
            }
            move() {
                this.x += this.speedX;
                this.y += this.speedY;
            }
            reset() {
                this.x = canvas.width / 2;
                this.y = canvas.height / 2;
                this.speedX = 5 * (Math.random() > 0.5 ? 1 : -1);
                this.speedY = 5 * (Math.random() > 0.5 ? 1 : -1);
            }
        }

        const user = new Paddle(0, canvas.height / 2 - 50, 10, 100);
        const computer = new Paddle(canvas.width - 10, canvas.height / 2 - 50, 10, 100);
        const ball = new Ball(canvas.width / 2, canvas.height / 2, 10);

        function draw() {
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            user.draw();
            computer.draw();
            ball.draw();
            ball.move();
            controlComputer();
            checkCollision();
            if (ball.x - ball.radius < 0 || ball.x + ball.radius > canvas.width) {
                ball.reset();
            }
            requestAnimationFrame(draw);
        }

        function controlComputer() {
            const center = computer.y + computer.height / 2;
            if (center < ball.y) {
                computer.move(false);
            } else {
                computer.move(true);
            }
        }

        function checkCollision() {
            if (ball.x - ball.radius < user.x + user.width && ball.y > user.y && ball.y < user.y + user.height) {
                ball.speedX = -ball.speedX;
            }
            if (ball.x + ball.radius > computer.x && ball.y > computer.y && ball.y < computer.y + computer.height) {
                ball.speedX = -ball.speedX;
            }
        }

        document.addEventListener('mousemove', (event) => {
            const rect = canvas.getBoundingClientRect();
            user.y = event.clientY - rect.top - user.height / 2;
        });

        draw();
    </script>
</body>
</html>
