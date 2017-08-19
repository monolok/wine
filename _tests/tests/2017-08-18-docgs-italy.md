---
layout: post
title:  "DOCGS of Italy"
date:   2017-08-18 14:00:00
categories: Italy DOCGS 
tag: classification 
---

<blockquote>
  <p>.......</p>
</blockquote>

<div class="text-center">
	<h2>Where and what growth ?</h2>
	<span>Bonus practice: guess second wine</span>
	<h4 class="text-danger" id="bdx">Montepulciano D' Abruzzo</h4>
	<button type="button" class="btn btn-success" id="test_me">Go !</button>
</div>

<script>
	var chateaux = ["1", "2"];

	$("#test_me").click(function(){
		var chateau = chateaux[Math.floor(Math.random()*chateaux.length)];
		$("#bdx").empty();
		$("#bdx").append("<span>" + chateau + "</span>");
	});
</script>