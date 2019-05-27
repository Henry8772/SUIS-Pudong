---
layout: home
title: Home
landing-title: SUIS Pudong
description: 
image: 
author: 
nav-menu: 
---

<!-- Banner -->
<section id="banner" class="major">
	<div class="inner">
		<header class="major">
			<h1>{{ page.landing-title }}</h1>
		</header>
		<div class="content">
			<p style="text-transform: uppercase;">{{ site.description }}</p>
			<ul class="actions">
				<li><a href="#one" class="button next scrolly">Get Started</a></li>
			</ul>
		</div>
	</div>
</section>

<!-- Main -->
<div id="main">

<!-- One -->
{% include tiles.html %}

<!-- Two -->
<section id="house" style="background-color: white">
	<div class="inner">
		<header class="major">
			<h2 style="color: #242943;border-bottom: 3px solid #242943;margin-bottom: 0px;">House activities</h2>
		</header>
		<div style="width: 100%;">
					<!--Chart 1 bar chart-->
		<div style="width: 50%;height: auto;float: left;display: block;">
		<p style="color: #242943;font-weight: bold;font-size: 30px;"># of green cards for each house</p>
		<canvas id="myChart"></canvas>
		<script>
			var ctx = document.getElementById("myChart").getContext('2d');
			var myChart = new Chart(ctx, {
				type: 'bar',
				data: {
					labels: ["Red", "Blue", "Yellow", "Green"],
					datasets: [{
						label: '# of Green cards',
						data: [12, 19, 3, 5, 2, 3],
						backgroundColor: [
							'rgba(255, 99, 132, 0.3)',
							'rgba(54, 162, 235, 0.3)',
							'rgba(255, 206, 86, 0.3)',
							'rgba(75, 192, 192, 0.3)',
						],
						borderColor: [
							'rgba(255,99,132,1)',
							'rgba(54, 162, 235, 1)',
							'rgba(255, 206, 86, 1)',
							'rgba(75, 192, 192, 1)',
						],
						borderWidth: 2
					}]
				},
				options: {
					scales: {
						yAxes: [{
						    ticks: {
						        beginAtZero:true
							}
						}]
					}
				}
		});
		</script>
	</div>
	<!--Chart 2 bar chart-->
	<div style="width: 50%;height: auto;float: left;display: block;">
		<p style="color: #242943;font-weight: bold;font-size: 30px;">Top 3 teachers who give out the highest # of green cards</p>
	<br>
		<canvas id="myChart2" style="margin-top: 30px;"></canvas>
			<script src="Chart.js/Chart.js"></script>
			<script>
				new Chart(document.getElementById("myChart2"),{"type":"doughnut","data":{"labels":["Student 1","Student 2","Student 3"],"datasets":[{"label":"My First Dataset","data":[300,50,100],"backgroundColor":["rgb(255, 99, 132)","rgb(54, 162, 235)","rgb(255, 205, 86)"]}]}});
			</script>
	</div>
		</div>
	<!--div2-->
	<div style="width: 100%;display: none;" id="chart2">
					<!--Chart 1 bar chart-->
		<div style="width: 50%;height: auto;float: left;display: block;">
		<p style="color: #242943;font-weight: bold;font-size: 30px;"># of green cards for each house</p>
		<canvas id="chart3"></canvas>
		<script>
			var ctx = document.getElementById("chart3").getContext('2d');
			var myChart = new Chart(ctx, {
				type: 'bar',
				data: {
					labels: ["Red", "Blue", "Yellow", "Green"],
					datasets: [{
						label: '# of Green cards',
						data: [12, 19, 3, 5, 2, 3],
						backgroundColor: [
							'rgba(255, 99, 132, 0.3)',
							'rgba(54, 162, 235, 0.3)',
							'rgba(255, 206, 86, 0.3)',
							'rgba(75, 192, 192, 0.3)',
						],
						borderColor: [
							'rgba(255,99,132,1)',
							'rgba(54, 162, 235, 1)',
							'rgba(255, 206, 86, 1)',
							'rgba(75, 192, 192, 1)',
						],
						borderWidth: 2
					}]
				},
				options: {
					scales: {
						yAxes: [{
						    ticks: {
						        beginAtZero:true
							}
						}]
					}
				}
		});
		</script>
	</div>
	<!--Chart 2 bar chart-->
	<div style="width: 50%;height: auto;float: left;display: block;">
		<p style="color: #242943;font-weight: bold;font-size: 30px;">Top 3 students who have the most green cards</p>
	<br>
		<canvas id="chart4" style="margin-top: 30px;"></canvas>
			<script src="Chart.js/Chart.js"></script>
			<script>
				new Chart(document.getElementById("chart4"),{"type":"doughnut","data":{"labels":["Student 1","Student 2","Student 3"],"datasets":[{"label":"My First Dataset","data":[300,50,100],"backgroundColor":["rgb(255, 99, 132)","rgb(54, 162, 235)","rgb(255, 205, 86)"]}]}});
			</script>
	</div>
		</div>
	<ul class="actions" style="display: block;">
		<li><a href="javascript:expand();" class="button next" style="border:3px solid #242943;color: #242943;">Expand more</a></li>
	</ul>
	</div>
</section>

<script type="text/javascript">
	function expand(){
		var chart2 = document.getElementById("chart2").style.display;
		if(chart2 == "none"){
			document.getElementById("chart2").style.display = "block";
		}
		else{
			document.getElementById("chart2").style.display = "none";
		}
	}
</script>

</div>

