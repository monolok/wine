---
layout: post
title:  "DOCGS of Italy"
categories: Italy DOCGS 
tag: classification 
---

<blockquote>
  <p>The word "garantia" in "DOCG" can be misleading as it is applied to an entire region. Both the best wine and worst of a particular area get to say they are DOCG.</p>
</blockquote>

<div class="text-center">
	<h2>DOCG: Subregion it belongs to ?</h2>
	<strong class="text-primary"><u> Bonus practice:</u> guess major grapes.</strong>
	<h4 class="text-danger" id="bdx">DOCG</h4>
	<h4 class="text-success" id="bdx_answer">Subregion</h4>
	<button type="button" class="btn btn-success" id="test_me">Next</button>
	<button type="button" class="btn btn-danger" id="answer">Answer</button>
	<button type="button" class="btn btn-primary" id="study">Study</button>
</div>

<br>

<table class="table table-condensed hide" id="study_table">
	<thead>
		<tr> 
			<th>DOCG</th>
			<th>Wine region</th>
		</tr>
	</thead>
	<tbody>
		
	</tbody> 
</table>

<script>
	var chateaux = ["Montepulciano D'Abruzzo", "Castel Del Monte Bombino Nero", "Castel Del Monte Bombino Nero Di Troia Riserva", "Castel Del Monte Rosso Riserva", "Primitivo Di Manduria Dolce Naturale", "Aglianico Del Vulture Superiore", "Aglianico Del Taburno", "Fiano Di Avellino", "Greco Di Tufo", "Taurasi", "Albana Di Romagna", "Colli Bolognesi Classico Pignoletto", "Colli Orientali Del Friuli Picolit", "Ramandolo", "Rosazzo", "Cannelino Di Frascati", "Cesanese Del Piglio", "Frascati Superiore", "Franciacorta", "Oltrepó Pavese Metodo Classico", "Scanzo", "Sforzato di Valtellina", "Valtellina Superiore", "Castelli Di Jesi Verdicchio Riserva", "Conero", "Offida", "Verdicchio Di Matelica Riserva", "Vernaccia Di Serrapetrona", "Alta Langa", "Asti", "Barbaresco", "Barbera D'Asti", "Barbera Del Monferrato Superiore", "Barolo", "Brachetto D'Acqui", "Dolcetto Di Diano D'Alba", "Dolcetto Di Dogliani", "Dolcetto Di Ovada Superiore", "Erbaluce Di Caluso", "Gattinara", "Gavi", "Ghemme", "Nizza", "Roero", "Ruché Di Castagnole Monferrato", "Vermentino Di Gallura", "Cerasuolo Di Vittoria", "Brunello Di Montalcino", "Carmignano", "Chianti", "Chianti Classico", "Elba Aleatico Passito", "Montecucco Sangiovese", "Morellino Di Scansano", "Suvereto", "Val Di Cornia Rosso", "Vernaccia Di San Gimignano", "Vino Nobile Di Montepulciano", "Amarone Della Valpolicella", "Asolo Prosecco", "Bagnoli Friularo", "Bardolino Superiore", "Colli Di Conegliano", "Colli Euganei Fior D'Arancio", "Conegliano Valdobbiadene-Prosecco", "Lison", "Montello", "Piave Malanotte", "Reciotto Della Valpolicella", "Reciotto Di Gambellara", "Reciotto Di Soave", "Soave Superiore", "Sagrantino Di Montefalco", "Torgiano Rosso Riserva"];

	var chateaux_answers = ["Abruzzi", "Apulia", "Apulia", "Apulia", "Apulia", "Basilicata", "Campania", "Campania", "Campania", "Campania", "Emilia-Romagna", "Emilia-Romagna", "Friuli-Venezia Giulia", "Friuli-Venezia Giulia", "Friuli-Venezia Giulia", "Lazio", "Lazio", "Lazio", "Lombardy", "Lombardy", "Lombardy", "Lombardy", "Lombardy", "Marche", "Marche", "Marche", "Marche", "Marche", "Piedmont", "Piedmont", "Piedmont", "Piedmont", "Piedmont", "Piedmont", "Piedmont", "Piedmont", "Piedmont", "Piedmont", "Piedmont", "Piedmont", "Piedmont", "Piedmont", "Piedmont", "Piedmont", "Piedmont", "Sardinia", "Sicily", "Tuscany", "Tuscany", "Tuscany", "Tuscany", "Tuscany", "Tuscany", "Tuscany", "Tuscany", "Tuscany", "Tuscany", "Tuscany", "Veneto", "Veneto", "Veneto", "Veneto", "Veneto", "Veneto", "Veneto", "Veneto", "Veneto", "Veneto", "Veneto", "Veneto", "Veneto", "Veneto", "Umbria", "Umbria"];
	
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