<!DOCTYPE (null)>
<html>
	<head>
		<link rel="stylesheet" href="css/snake.css" />
		<script type="text/javascript" src="js/snake.js"></script>
		<script type="text/javascript" src="js/snake-grid.js"></script>
		<script type="text/javascript" src="js/snake-images.js"></script>
		<script type="text/javascript" src="js/snake-level.js"></script>
		<script type="text/javascript" src="js/snake-events.js"></script>
		<script type="text/javascript">
			window.gameLoop = function() {
				Snake.move();
				Snake.drawGrid();
				Snake.drawScore();
				if (Snake.gameOver == false) {
					setTimeout(window.gameLoop, 200);
				} else {
					Snake.drawGameOver();
				}
			}
			
			window.onload = function() {
				Snake.init('game-screen', 0, window.gameLoop);
			};
		</script>
	</head>
	<style>

.content {
    max-width: 500px;
    margin: auto;
}

</style>
	<body>
		<div class="content">
<h1>P2 VS JURY</h1>
	
		<canvas id="game-screen" width="800" height="600"></canvas>
<p style="position:relative; left:0; top:27px;">&copy; 2017 - D&eacute;velopp&eacute; par R&eacute;my Dubian - 
			<a href="https://www.facebook.com/profile.php?id=100004611497423">My Facebook</a>
		</p>
					</body>
</html>
