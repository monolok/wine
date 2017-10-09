---
layout: post
title:  "51 Alsace Grand Cru"
categories: Alsace
tag: classification 
---

<blockquote>
  <p>25 vineyards were legally recognized as Grand Cru in 1983. As many wine classification attempt in France, it was widely controversial. Later, 26 more were added. Far too many according to some producers.</p>
</blockquote>

<div class="text-center">
	<h2>What village ?</h2>
	<strong class="text-primary"><u> Bonus practice: spot the original 25 (O-25).</u> </strong>
	<h4 class="text-danger" id="bdx">Alsace Grand Cru</h4>
	<h4 class="text-success" id="bdx_answer">Village</h4>
	<button type="button" class="btn btn-success" id="test_me">Next</button>
	<button type="button" class="btn btn-danger" id="answer">Answer</button>
	<button type="button" class="btn btn-primary" id="study">Study</button>
</div>

<br>

<table class="table table-condensed hide" id="study_table">
	<thead>
		<tr> 
			<th>Alsace Grand Cru</th>
			<th>Village</th>
			<th>Note</th>
		</tr>
	</thead>
	<tbody>
		
	</tbody> 
</table>

<script>
	var chateaux = ["Altenberg de Bergbieten", "Altenberg de Bergheim", "Altenberg de Wolxheim", "Brand", "Bruderthal", "Eichberg", "Engelberg", "Florimont", "Frankstein", "Froehn", "Furstentum", "Geisberg", "Gloeckelberg", "Goldert", "Hatschbourg", "Hengst", "Kaefferkopf", "Kanzlerberg", "Kastelberg", "Kessler", "Kirchberg de Barr", "Kirchberg de Ribeauvillé", "Kitterlé", "Mambourg", "Mandelberg", "Marckrain", "Moenchberg", "Muenchberg", "Ollwiller", "Osterberg", "Pfersigberg", "Pfingstberg", "Praelatenberg", "Rangen", "Rosacker", "Saering", "Schlossberg", "Schoenenbourg", "Sommerberg", "Sonnenglanz", "Spiegel", "Sporen", "Steinert", "Steingrubler", "Steinklotz", "Vorbourg", "Wiebelsberg", "Wineck-Schlossberg", "Winzenberg", "Zinnkoepflé", "Zotzenberg"];

	var chateaux_answers = ["Bergbieten / O-25", "Bergheim / O-25", "Wolxheim / Not O-25", "Turckheim / O-25", "Molsheim / Not O-25", "Eguisheim / O-25", "Dahlenheim, Scharrachbergheim / Not O-25", "Ingersheim, Katzenthal / Not O-25", "Dambach-La-Ville / Not O-25", "Zellenberg / Not O-25", "Kientzheim, Sigolsheim / Not O-25", "Ribeauville / O-25", "Rodern, Saint-Hippolyte / O-25", "Gueberschwihr / O-25", "Hattstatt, Voegtlinshoffen / O-25", "Wintzenheim / O-25", "Ammerschwihr / Not O-25", "Bergheim / O-25", "Andlau / O-25", "Guebwiller / O-25", "Barr / O-25", "Ribeauville / O-25", "Guebwiller / O-25", "Sigolsheim / Not O-25", "Mittelwihr, Beblenheim / Not O-25", "Bennwihr, Sigolsheim / Not O-25", "Andlau, Eichhoffen / O-25", "Nothalten / Not O-25", "Wuenheim / O-25", "Ribeauville / Not O-25", "Eguisheim, Wettolsheim / Not O-25", "Orschwihr / Not O-25", "Kintzheim / Not O-25", "Thann, Vieux-Thann / O-25", "Hunawihr / O-25", "Guebwiller / O-25", "Kientzheim / O-25", "Riquewihr, Zellenberg / Not O-25", "Niedermorschwihr, Katzenthal / O-25", "Beblenheim / O-25", "Bergholz, Guebwiller / O-25", "Riquewihr / Not O-25", "Pfaffenheim, Westhalten / Not O-25", "Wettolsheim / Not O-25", "Marlenheim / Not O-25", "Rouffach, Westhalten / Not O-25", "Andlau / O-25", "Katzenthal, Ammerschwihr / Not O-25", "Blienschwiller / Not O-25", "Soultzmatt, Westhalten / Not O-25", "Mittelbergheim / Not O-25"];

	var notes = ["...", "Blends spec. / min planting density: 5,500 vines per ha", "...", "Clos de la Treille (F. Baur)", "...", "...", "...", "...", "...", "...", "...", "...", "...", "Clos St Imer (E. Burn)", "...", "...", "Blends spec. / Newest G.C (2007)", "Smallest G.C (3.23 ha)", "...", "...", "...", "...", "...", "...", "...", "...", "...", "...", "...", "Clos du Zahnacker (La Cave de Ribeauvillé)", "...", " Clos Schild (Lucien Albrecht)", "...", "Clos St Urbain (Zind-Humbrecht) & Clos St Théobald (Schoffit)", "Clos Ste Hune (Trimbach)", "...", "Biggest G.C (80.28 ha) / 1rst G.C", "...", "...", "...", "...", "...", "...", "...", "...", "Clos St Landelin (R. Muré)", "...", "...", "...", "...", "Sylvaner allowed"];
	
	// generating study table
	var counter = 0
	for (var i = chateaux.length - 1; i >= 0; i--) {
		$("tbody").append("<tr><td>" + chateaux[counter] + "</td><td>" + chateaux_answers[counter] + "</td><td>" + notes[counter] + "</td></tr>");
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