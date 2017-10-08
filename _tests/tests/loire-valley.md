---
layout: post
title:  "Tête de Cuvée - Champagne"
categories: Champagne Cuvée 
tag: prestige échelle 
---

<blockquote>
  <p>The first prestige or "Tête de Cuvée" was made in 1876 by Roederer for Czar Alexander II (Russia), who wanted an exclusive wine bottled in cristal not available to the "common" people.</p>
</blockquote>

<div class="text-center">
	<h2>Tête de Cuvée is/are ?</h2>
	<strong class="text-primary"><u> Bonus practice: spot the "RM" producers.</u> </strong>
	<h4 class="text-danger" id="bdx">Champagne</h4>
	<h4 class="text-success" id="bdx_answer">Tête de Cuvée</h4>
	<button type="button" class="btn btn-success" id="test_me">Next</button>
	<button type="button" class="btn btn-danger" id="answer">Answer</button>
	<button type="button" class="btn btn-primary" id="study">Study</button>
</div>

<br>

<table class="table table-condensed hide" id="study_table">
	<thead>
		<tr> 
			<th>Maison Champagne</th>
			<th>Tête de Cuvée</th>
		</tr>
	</thead>
	<tbody>
		
	</tbody> 
</table>

<script>
	var chateaux = ["Ayala", "Billecart-Salmon", "Bollinger", "Boizel", "Canard-Duchêne", "Compte Audoin de Dampierre", "De Castellane", "De Meric", "De Venoge", "Delamotte", "Deutz", "Diebolt-Valois", "Drappier", "Duval-Leroy", "Gosset", "Alfred Gratien", "Charles Heidsieck", "Henriot", "Jacquesson", "Lanson", "Laurent-Perrier", "AR Lenoble", "Moët & Chandon", "Mumm", "Bruno Paillard", "Joseph Perrier", "Perrier-Jouët", "Piper-Heidsieck", "Ployez-Jacquemart", "Pol Roger", "Pommery", "Louis Roederer", "Ruinard", "Taittinger", "Veuve Clicquot", "Henri Billiot", "Bonnaire", "Chartogne-Taillet", "Hubert Dauvergne", "Paul Déthune", "Guy Larmandier", "Jacques Selosse", "Vilmart & Cie", "Nicolas Feuillatte", "Jacquart", "Mailly Grand Cru", "Agrapart", "Billecart-Salmon (monoparcel)", "Cattier", "Chartogne-Taillet (monoparcel)", "Claude Cazals", "Drappier", "Duval-Leroy (monoparcel)", "Egly-Ouriet", "Jacquesson (monoparcel)", "Krug", "Larmandier-Bernier", "Jean Milan", "Pierre Peters", "Philipponnat", "Taittinger (monoparcel)", "Tarlant", "Veuve Fourny"];

	var chateaux_answers = ["Cuvée Perle d'Ayala", "Nicolas François Billecart / Grande Cuvée / Elisabeth Salmon Rosé", "La Grande Année / R.D / Vieilles Vignes Françaises", "Joyau de France", "Charles VII", "Prestige", "Cuvée Commodore", "Catherine de Médicis", "Grand vin des princes / Louis XV", "Nicolas Louis Delamotte", "Cuvée William Deutz", "Fleur de passion", "Charles de Gaulle", "Femme de Champagne", "Celebris", "Cuvée Paradis", "Champagne Charlie", "Cuvée des Enchanteleurs", "Grand vin Signature", "Noble Cuvée", "Grand Siècle / Alexandra", "Cuvée Les Aventures / Cuvée Gentil-homme", "Dom Pérignon / Oenothèque", "Cuvée R. Lalou", "Nec-Plus-Ultra", "Cuvée Josephine", "Belle Époque or Fleur de Champagne (USA only)", "Rare", "Liesse d'Harbonville", "Cuvée Sir Winston Churchill", "Cuvée Louise", "Cristal", "Dom Ruinard", "Compte de Champagne, Taittinger Collection", "La grande dame", "Cuvée Laetitia/ Cuvée Julie", "Cuvée Prestige", "Fiacre", "Fine Fleur de Bouzy", "Brut Prestige", "Cramant Grand Cru Cuvée", "Substance", "Coeur de Cuvée", "Palmes d'Or", "Cuvée Alpha", "Les Échansons / L'Intemporelle", "Venus", "Clos St-Hilaire", "Clos du Moulin", "Les Barres / Les Orizeaux / Les Alliées", "Clos Cazals", "Grande Sendrée", "Clos des Bouveries", "Les Crayères", "Dizy Corne Bautray / Aÿ Vauzelle Terme / Dizy Terres Rouges Rosé / Avize Champ Cain", "Clos du Mesnil", "Vieille Vigne de Cramant / Terre de Vertus", "Terres de Noël", "Cuvée Spéciale les Chétillons", "Clos des Goisses", "Les Folies de la Marquetterie", "La vigne d'Or / La vigne d'Antan / La vigne Royale / Cuvée Louis", "Clos Faubourg Notre Dame"];
	
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