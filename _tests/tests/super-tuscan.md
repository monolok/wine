---
layout: post
title:  "Super-Tuscan"
categories: Italy Toscana Super-Tuscan 
tag: classification 
---

<blockquote>
  <p>It all started in Castiglioncello where Mario Incisa della Rocchetta decided to plant Cabernet Sauvignon in a supposedly Sangiovese country. Today, Bolgheri Sassicaia is Italy's sole vineyard DOC and Super-Tuscans paved the way for better quality in Chianti vineyards.</p>
</blockquote>

<div class="text-center">
	<h2>What is the Blend ?</h2>
	<strong class="text-primary"><u> Bonus practice:</u> guess producer.</strong>
	<h4 class="text-danger" id="bdx">Super-Tuscan</h4>
	<h4 class="text-success" id="bdx_answer">Current Blend</h4>
	<button type="button" class="btn btn-success" id="test_me">Next</button>
	<button type="button" class="btn btn-danger" id="answer">Answer</button>
	<button type="button" class="btn btn-primary" id="study">Study</button>
</div>

<br>

<table class="table table-condensed hide" id="study_table">
	<thead>
		<tr> 
			<th>Super-Tuscan</th>
			<th>Blend / Producer</th>
		</tr>
	</thead>
	<tbody>
		
	</tbody> 
</table>

<script>
	var chateaux = ["Acciaiolo", "L' Apparita", "Tignanello", "Solaia", "Guado al Tasso", "Grifi", "Desiderio", "50 & 50", "SummuS", "Casalferro", "Boscarelli", "il Blu", "Cabreo il Borgo", "Il Caberlot", "Cantico", "Ghiaie della Furba", "I Sodi di San Niccolò", "Il Corzano", "Fontalloro", "Maestro Raro", "Flaccianello della Pieve", "Mormoreto", "Lamaione", "Luce", "Giramonte", "Grattamacco", "Cepparello", "Paleo Rosso", "Messorio", "Scrio", "Nemo", "Gabbro", "Nardo", "Le Pergole Torte", "Avvoltore", "Ornellaia", "Masseto", "Il Carbonaione", "Le Stanze del Poliziano", "Saffredi", "Camartina", "Sammarco", "Vigna d'Alceo", "La Gioia", "Vigorello", "Percarlo", "La Ricolma", "Sassicaia", "Il Bosco", "Redigaffi", "Anfiteatro", "Bruno di Rocca", "Balifico"];

	var chateaux_answers = ["Sangiovese, Cab. S / Castello D'Albola", "Merlot / Castello di Alma", "75-85% Sangiovese, Cab. S & Cab. F / Antinori", "75% Cab. S, 20% Sangiovese & 5% Cab. F / Antinori", "50-65% Cab. S & 30-40% Merlot plus other varieties / Antinori", "50-60% Sangiovese & 40-50% Cab. S / Avignonesi", "85% Merlot & 15% Cab. S / Avignonesi", "50% Merlot (Avignonesi) & 50% Sangiovese (Capannelle)", "Cab. S, Sangiovese & Syrah / Banfi", "Merlot / Barone Ricasoli", "Merlot / Boscarelli", "50% Sangiovese, 45% Merlot & 5% Cab. S / La Brancaia", "70% Sangiovese & 30% Cab. S / Tenute del Cabreo", "Caberlot / Il Carnasciale", "Merlot / La Cappella", "60% Cab. S, 30% Merlot & 10% Syrah / Capezzana", "85-90% Sangioveto & 10-15% Malvasia Nera / Castellare di Castelina", "Sangiovese, Cab. S & Merlot / Corzano e Paterno", "Sangiovese / Felsina", "Cab. S / Felsina", "Sangiovese / Fontodi", "Cab. S, Merlot, Cab. F & PV / Frescobaldi", "Merlot / Frescobaldi", "Sangiovese & Merlot / Frescobaldi", "Mostly Merlot plus Sangiovese / Frescobaldi", "65% Cab. S, 20% Merlot & 15% Sangiovese / Grattamacco", "Sangiovese / Isole e Olena", "Cab. F / Le Macchiole", "Merlot / Le Macchiole", "Syrah / Le Macchiole", "Cab. S / Monsanto", "Cab. S / Montepeloso", "35% Montepulciano, 35% Sangiovese, 22% Marselan & 8% Alicante Bouschet / Montepeloso", "Sangioveto / Montevertine", "Mostly Sangiovese, Cab. S & Syrah / Moris Farms", "Cab. S, Merlot, Cab. F & PV / Tenuta dell'Ornellaia", "Merlot / Tenuta dell'Ornellaia", "Sangiovese / Poggio Scalette", "70% Cab. S & 30% Merlot / Poliziano", "Cab. S, Merlot & Alicante / Le Pupille", "70% Cab. S & 30% Sangiovese / Querciabella", "Mostly Cab. S / Castello dei Rampolla", "80% Cab. S & PV / Castello dei Rampolla", "Mostly Sangiovese / Riecine", "Cab. S, Merlot & PV / San Felice", "Sangiovese / San Giusto a Rentennano", "Merlot / San Giusto a Rentennano", "85% Cab. S & 15% Cab. F / Tenuta San Guido", "Syrah / Tenimenti d'Alessandro", "Merlot / Tua Rita", "Sangiovese / Vecchie Terre di Montefili", "60% Cab. S & 40% Sangiovese / Vecchie Terre di Montefili", "Sangiovese & Cab. S / Volpaia"];
	
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