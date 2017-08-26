---
layout: post
title:  "1855 Médoc classification"
categories: Bordeaux médoc
tag: 1855 classification growth
---

<blockquote>
  <p>A classification based on reputation rather than terroir.</p>
</blockquote>

<div class="text-center">
	<h2>Where and what growth ?</h2>
	<strong class="text-primary"><u> Bonus practice:</u> guess second wine.</strong>
	<h4 class="text-danger" id="bdx">Wine</h4>
	<h4 class="text-success" id="bdx_answer">Answer</h4>
	<button type="button" class="btn btn-success" id="test_me">Next</button>
	<button type="button" class="btn btn-danger" id="answer">Answer</button>
	<button type="button" class="btn btn-primary" id="study">Study</button>
</div>

<br>

<table class="table table-condensed hide" id="study_table">
	<thead>
		<tr> 
			<th>Château</th>
			<th>Growth</th>
		</tr>
	</thead>
	<tbody>
		
	</tbody> 
</table>

<script>
	var chateaux = ["Château Haut-Brion", "Château Lafite-Rothschild", "Château Latour", "Château Margaux", "Château Mouton-Rothschild", "Château Rausan-Ségla", "Château Rauzan-Gassies", "Château Léoville-Las Cases", "Château Léoville-Poyferré", "Château Léoville-Barton", "Château Durfort-Vivens", "Château Gruaud-Larose", "Château Lascombes", "Château Brane-Cantenac", "Château Pichon-Longueville", "Château Pichon-Longueville, Comtesse de Lalande", "Château Ducru-Beaucaillou", "Château Cos d'Estournel", "Château Montrose", "Château Kirwan", "Château d'Issan", "Château Lagrange", "Château Langoa-Barton", "Château Giscours", "Château Malescot Saint-Exupéry", "Château Boyd-Cantenac", "Château Cantenac-Brown", "Château Palmer", "Château La Lagune", "Château Desmirail", "Château Calon-Ségur", "Château Ferrière", "Château Marquis d'Alesme-Becker", "Château Saint-Pierre", "Château Talbot", "Château Branaire-Ducru", "Château Duhart-Milon-Rothschild", "Château Pouget", "Château La Tour-Carnet", "Château Lafon-Rochet", "Château Beychevelle", "Château Prieuré-Lichine", "Château Marquis-de-Terme", "Château Pontet-Canet", "Château Batailley", "Château Haut-Batailley", "Château Grand-Puy-Lacoste", "Château Grand-Puy-Ducasse", "Château Lynch-Bages", "Château Lynch-Moussas", "Château Dauzac", "Château d'Armailhac", "Château du Tertre", "Château Haut-Bages-Libéral", "Château Pédesclaux", "Château Belgrave", "Château de Camensac", "Château Cos-Labory", "Château Clerc-Milon", "Château Croizet-Bages", "Château Cantemerle"];

	var chateaux_answers = ["1st, Pessac", "1st, Pauillac", "1st, Pauillac", "1st, Margaux", "1st, Pauillac", "2nd, Margaux", "2nd, Margaux", "2nd, Saint-Julien", "2nd, Saint-Julien", "2nd, Saint-Julien", "2nd, Margaux", "2nd, Saint-Julien", "2nd, Margaux", "2nd, Margaux", "2nd, Pauillac", "2nd, Pauillac", "2nd, Saint-Julien", "2nd, Saint-Estephe", "2nd, Saint-Estephe", "3rd, Margaux", "3rd, Margaux", "3rd, Saint-Julien", "3rd, Saint-Julien", "3rd, Margaux", "3rd, Margaux", "3rd, Margaux", "3rd, Margaux", "3rd, Margaux", "3rd, Haut-Médoc", "3rd, Margaux", "3rd, Saint-Estephe", "3rd, Margaux", "3rd, Margaux", "4th, Saint-Julien", "4th, Saint-Julien", "4th, Saint-Julien", "4th, Pauillac", "4th, Margaux", "4th, Haut-Médoc", "4th, Saint-Estephe", "4th, Saint-Julien", "4th, Margaux", "4th, Margaux", "5th, Pauillac", "5th, Pauillac", "5th, Pauillac", "5th, Pauillac", "5th, Pauillac", "5th, Pauillac", "5th, Pauillac", "5th, Margaux", "5th, Pauillac", "5th, Margaux", "5th, Pauillac", "5th, Pauillac", "5th, Haut-Médoc", "5th, Haut-Médoc", "5th, Saint-Estephe", "5th, Pauillac", "5th, Pauillac", "5th, Haut-Médoc"];

	// generating study table
	var counter = 0
	for (var i = chateaux.length - 1; i >= 0; i--) {
		$("tbody").append("<tr><td>" + chateaux[counter] + "</td><td>" + chateaux_answers[counter] + "</td></tr>");
		counter++
	};

	//clicking JS logic
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

	var hide = true
	$("#study").click(function(){
		if (hide) {
			$( "#study_table" ).removeClass("hide");
			hide = false;
		}else{
			$( "#study_table" ).addClass("hide");
			hide = true;
		};
	});
</script>