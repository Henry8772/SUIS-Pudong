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
		<p style="color: #242943;">Green cards of the month</p>
		<div style="width: 90%;height: auto;">
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
	<ul class="actions">
		<li><a href="landing.html" class="button next" style="border:3px solid #242943;color: #242943;">Expand more</a></li>
	</ul>
	</div>
</section>

</div>

