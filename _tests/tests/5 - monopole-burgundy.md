---
layout: post
title:  "Monopole in Burgundy"
categories: Burgundy Monopole
tag: Monopole Vineyard Cru single
---

<blockquote>
  <p>The Napoleonic laws did not fractionate all vineyards after all. The "Monopole" concept of one producer owning a whole vineyard is a must know in Burgundy.</p>
</blockquote>

<div class="text-center">
	<h2>Who owns it ?</h2>
	<strong class="text-primary"><u> Bonus practice:</u> guess village and classification.</strong>
	<h4 class="text-danger" id="bdx">Monopole</h4>
	<h4 class="text-success" id="bdx_answer">Producer</h4>
	<button type="button" class="btn btn-success" id="test_me">Next</button>
	<button type="button" class="btn btn-danger" id="answer">Answer</button>
	<button type="button" class="btn btn-primary" id="study">Study</button>
</div>

<br>

<table class="table table-condensed hide" id="study_table">
	<thead>
		<tr> 
			<th>Vineyard</th>
			<th>Producer</th>
		</tr>
	</thead>
	<tbody>
		
	</tbody> 
</table>

<script>
	var chateaux = ["La Moutonne", "Les Ruelles", "La Mission", "Clos des Monts Luisants", "Ruchottes-Chambertin 'Clos des Ruchottes'", "Clos de Tart", "Romanée-Conti", "La Tâche", "La Grande Rue", "La Romanée", "Corton 'Clos des Marechaudes'", "Corton 'Clos des Cortons Faiveley'", "Clos des Porrets", "Clos des Noiterons", "Clos Napoléon", "Clos de la Mousse", "Clos des Réas", "Clos des Corvées", "Le Clos de Thorey", "Clos de la Maréchale", "La Bossiere", "Savigny-Champ-Chevrey", "Clos de l'ecu", "Clos des ursule", "Clos des Épeneaux", "Clos Marey-Monge", "Fremiets Clos de la Rougeotte", "Clos des Ducs", "Clos de la Bousse d'Or", "Clos des 60 Ouvrées", "Clos des Santenots", " Clos de la Chapelle", "Clos de la Bare", "Le Clos Blanc de Vougeot", "Clos De Prieuré", "Clos Saint Paul", "Clos Salomon", "Clos des Myglands", "Clos de la Fontaine", "La Montagne", "Clos des Langres", "Pièce du Chapître", "Clos de la Chaume Gaufriot", "Clos des Ursulines", " Clos la Marche"];

	var chateaux_answers = ["Chablis / Albert Bichot (Domaine Long Depaquit)", "1er Cru, Mercurey / Château de Chamirey", "1er Cru, Mercurey / Château de Chamirey", "1er Cru, Morey-St-Denis / Domaine Ponsot", "G.C, Gevrey-Chambertin / Domaine Armand Rousseau", "G.C, Morey-St-Denis / Mommessin", "G.C, Vosne-Romanée / D.R.C", "G.C, Vosne-Romanée / D.R.C", "G.C, Vosne-Romanée / Domaine François Lamarche", "G.C, Vosne-Romanée / Compte Liger-Belair", "G.C, Aloxe-Corton / Albert Bichot", "G.C, Aloxe-Corton / Domaine Faiveley", "1er Cru, Nuits-St-Georges / Domaine Henri Gouges", "Village, Mercurey / Château d'Etroyes", "1er Cru, Fixin / Pierre Gelin", "1er Cru, Beaune / Bouchard Père et Fils", "1er Cru, Vosne-Romanée / Michel Gros", "Village, Mercurey / Château d'Etroyes", "1er Cru, Nuits-St-Georges / Antonin Rodet", "1er Cru, Nuits-St-Georges / Jacques Frederic Mugnier", "1er Cru, Gevrey-Chambertin / Domaine Harmand Geoffroy", "1er Cru, Savigny-lès-Beaune / Domaine Tollot-Beaut", "1er Cru, Beaune / Domaine Faiveley", "1er Cru, Beaune / Louis Jadot", "1er Cru, Pommard / Compte Armand", "Village, Pommard / Château de Pommard", "1er Cru, Volnay / Bouchard Père et Fils", "1er Cru, Volnay / Marquis d'Angerville",
	 
	 "1er Cru, Volnay / La Pousse d'or", "1er Cru, Volnay / La Pousse d'Or", "1er Cru, Volnay / Domaine Jacques Prieur", "1er Cru, Volnay / Domaine Clos de la Chapelle", "1er Cru, Volnay / Louis Jadot", "1er Cru, Vougeot / Domaine de la Vougeraie", "Village, Vougeot / Domaine de la Vougeraie", "1er Cru, Givry / Domaine Silvestre Du Closel", "1er Cru, Givry / Gardin Perrotto", "1er Cru, Mercurey / Domaine Faiveley", "Village, Vosne-Romanée / A.F Gros", "Village, Vosne-Romanée / Bruno Clavelier", "Village, Corgoloin / Domaine d'Ardhuy", "Village, Savigny-lès-Beaune / Domaine Tollot-Beaut", "Village, Beaune / Antonin Guyon", "Village, Pommard / Albert Bichot (Domaine du Pavillon)", "Village, Mercurey / Louis Max"];
	
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