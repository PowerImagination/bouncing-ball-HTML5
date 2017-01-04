window.onload = function(){
	var canvas = document.getElementById("draw");
	   c = canvas.getContext("2d");
	   c.fillStyle = "black";
	   c.fillRect(0, 0, canvas.width, canvas.height);

	    var y =100;
	    var speed =5;
	setInterval(function(){
	   y = y + speed;
	   if (y >= 450){
	       speed -=2;
	   }
	   if (y <= 50){
	       speed +=2;
	   }
	   c.fillStyle = "black";
	   c.fillRect(0, 0, canvas.width, canvas.height);
	   
	   c.fillStyle = "white";
	   c.beginPath();
	   c.arc(250,y, 50, 0, Math.PI * 2, false);
	   c.fill();
	   
	}, 30);
	
};
