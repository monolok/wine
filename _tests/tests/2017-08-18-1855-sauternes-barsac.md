---
layout: post
title:  "1855 Sauternes & Barsac classification"
categories: Bordeaux Sauternes Barsac 
tag: 1855 classification growth sweet 
---

<blockquote>
  <p>A classification based on reputation rather than terroir.</p>
</blockquote>

<div class="text-center">
	<h2>Where and what growth ?</h2>
	<span>Bonus practice: guess second wine</span>
	<h4 class="text-danger" id="bdx">Wine</h4>
	<h4 class="text-success" id="bdx_answer">Answer</h4>
	<button type="button" class="btn btn-success" id="test_me">Next</button>
	<button type="button" class="btn btn-danger" id="answer">Answer</button>
</div>

<script>
	var chateaux = ["Château d’Yquem", "Château La Tour Blanche", "Château Lafaurie-Peyraguey", "Clos Haut Peyraguey", "Château Rayne Vigneau", "Château Suduiraut", "Château Coutet", "Château Climens", "Château Guiraud", "Château Rieussec", "Château Rabaud-Promis", "Château Sigalas-Rabaud", "Château de Myrat", "Château Doisy-Daene", "Château Doisy-Dubroca", "Château Doisy-Vedrines", "Château d’Arche", "Château Filhot", "Château Broustet", "Château Nairac", "Château Caillou", "Château Suau", "Château de Malle", "Château Romer", "Château Lamothe", "Château Lamothe-Guignard", "Château Romer-du-Hayot"];

	var chateaux_answers = ["Château d’Yquem", "Château La Tour Blanche", "Château Lafaurie-Peyraguey", "Clos Haut Peyraguey", "Château Rayne Vigneau", "Château Suduiraut", "Château Coutet", "Château Climens", "Château Guiraud", "Château Rieussec", "Château Rabaud-Promis", "Château Sigalas-Rabaud", "Château de Myrat", "Château Doisy-Daene", "Château Doisy-Dubroca", "Château Doisy-Vedrines", "Château d’Arche", "Château Filhot", "Château Broustet", "Château Nairac", "Château Caillou", "Château Suau", "Château de Malle", "Château Romer", "Château Lamothe", "Château Lamothe-Guignard", "Château Romer-du-Hayot"];
	
	$("#test_me").click(function(){
		var rand = Math.floor(Math.random()*chateaux.length)
		var chateau = chateaux[rand];
		var chateau_answer = chateaux_answers[rand];
		$("#bdx").empty();
		$("#bdx_answer").empty();
		$("#bdx_answer").append("Answer");
		$("#bdx").append("<span>" + chateau + "</span>");
		$("#answer").click(function(){
			$("#bdx_answer").empty();
			$("#bdx_answer").append("<span>" + chateau_answer + "</span>");
		});
	});
</script>