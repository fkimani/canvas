# canvas
Animate a shape on HTML5 Canvas

Set y = Math.cos(x)+1 to make the red box seem to be going in a wavy manner. Cos curvishly.
set y = Math.random() or a constant to make it smooth

<!DOCTYPE html>
<html>
<head><title>Canvas Moving Box</title></head>

<body>

<canvas id="canvas" width="500" height="500"></canvas>

<script>
	var canv = document.getElementById("canvas"),
		c = canv.getContext("2d"),
		x, y, i,
		time = 0,
		width = 20, height = 100;
	
	canv.style.backgroundColor = "beige";	
	
	//draw
	function draw(){
		c.clearRect(0, 0, canv.width, canv.height);//clear screen
		
		x = time,  y = Math.cos(x)+1, 
		
		c.fillStyle = "red";
		c.fillRect(x, y, width, height);
		time += 1;

	}
	setInterval(draw, 5);

</script>

</body>
</html>
