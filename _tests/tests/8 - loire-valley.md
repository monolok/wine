---
layout: post
title:  "Loire Valley - AOC"
categories: LoireValley AOC
tag: AOC Loire Valley
---

<blockquote>
  <p>Working on it...</p>
</blockquote>

<div class="text-center">
	<h2>AOC belong to which subregion ?</h2>
	<strong class="text-primary"><u> Bonus practice: guess style and main grapes.</u> </strong>
	<h4 class="text-danger" id="bdx">AOC</h4>
	<h4 class="text-success" id="bdx_answer">Subregion?</h4>
	<button type="button" class="btn btn-success" id="test_me">Next</button>
	<button type="button" class="btn btn-danger" id="answer">Answer</button>
	<button type="button" class="btn btn-primary" id="study">Study</button>
</div>

<br>

<table class="table table-condensed hide" id="study_table">
	<thead>
		<tr> 
			<th>AOC</th>
			<th>Subregion / Style / Grapes</th>
		</tr>
	</thead>
	<tbody>
		
	</tbody> 
</table>

<script>
	var chateaux = ["Anjou", "Anjou Villages Brissac", "Anjou-Coteaux de la Loire", "Anjou-Villages", "Bonnezeaux", "Cabernet d' Anjou", "Cabernet de Saumur", "Coteaux de Saumur", "Coteaux de l' Aubance", "Coteaux du Layon", "Haut-Poitou", "Quarts de Chaume", "Rosé d'Anjou", "Saumur", "Saumur-Champigny", "Savennières", "Savennières Coulée de Serrant", "Savennières Roche Aux Moines", "Coteaux du Giennois", "Menetou-Salon", "Orléans", "Orléans-Cléry", "Pouilly Fumé", "Pouilly-sur-Loire", "Quincy Reuilly", "Sancerre", "Crémant de Loire", "Rosé de Loire", "Coteaux d' Ancenis", "Fiefs Vendéens", "Gros Plant du Pays Nantais", "Muscadet", "Muscadet Coteaux de la Loire", "Muscadet Côte de Grandlieu", "Muscadet Sèvre-et-Maine", "Bourgueil", "Cheverny", "Chinon", "Coteaux du Loir", "Coteaux du Vendômois", "Cour-Cheverny", "Jasnières", "Montlouis-sur-Loire", "Saint-Nicolas-de-bourgueil", "Touraine", "Touraine Noble-Joué", "Valençay", "Vouvray"];

	var chateaux_answers = ["Anjou-Saumur", "Anjou-Saumur", "Anjou-Saumur", "Anjou-Saumur", "Anjou-Saumur", "Anjou-Saumur", "Anjou-Saumur", "Anjou-Saumur", "Anjou-Saumur", "Anjou-Saumur", "Anjou-Saumur", "Anjou-Saumur", "Anjou-Saumur", "Anjou-Saumur", "Anjou-Saumur", "Anjou-Saumur", "Anjou-Saumur", "Anjou-Saumur", "Central Vineyards", "Central Vineyards", "Central Vineyards", "Central Vineyards", "Central Vineyards", "Central Vineyards", "Central Vineyards", "Central Vineyards", "General Appellation", "General Appellation", "Pays Nantais", "Pays Nantais", "Pays Nantais", "Pays Nantais", "Pays Nantais", "Pays Nantais", "Pays Nantais", "Touraine", "Touraine", "Touraine", "Touraine", "Touraine", "Touraine", "Touraine", "Touraine", "Touraine", "Touraine", "Touraine", "Touraine", "Touraine"];
	
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