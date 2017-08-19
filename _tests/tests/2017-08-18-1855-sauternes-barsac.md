---
layout: post
title:  "1855 Sauternes & Barsac classification"
date:   2017-08-18 14:00:00
categories: Bordeaux Sauternes Barsac 
tag: 1855 classification growth sweet 
---

<blockquote>
  <p>A classification based on reputation rather than terroir.</p>
</blockquote>

<div class="text-center">
	<h2>Where and what growth ?</h2>
	<span>Bonus practice: guess second wine</span>
	<h4 class="text-danger" id="bdx">Château d’Yquem</h4>
	<button type="button" class="btn btn-success" id="test_me">Go !</button>
</div>

<script>
	var chateaux = ["Château d’Yquem", "Château La Tour Blanche", "Château Lafaurie-Peyraguey", "Clos Haut Peyraguey", "Château Rayne Vigneau", "Château Suduiraut", "Château Coutet", "Château Climens", "Château Guiraud", "Château Rieussec", "Château Rabaud-Promis", "Château Sigalas-Rabaud", "Château de Myrat", "Château Doisy-Daene", "Château Doisy-Dubroca", "Château Doisy-Vedrines", "Château d’Arche", "Château Filhot", "Château Broustet", "Château Nairac", "Château Caillou", "Château Suau", "Château de Malle", "Château Romer", "Château Lamothe", "Château Lamothe-Guignard", "Château Romer-du-Hayot"];

	$("#test_me").click(function(){
		var chateau = chateaux[Math.floor(Math.random()*chateaux.length)];
		$("#bdx").empty();
		$("#bdx").append("<span>" + chateau + "</span>");
	});
</script>