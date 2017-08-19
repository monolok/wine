---
layout: post
title:  "1855 Médoc classification"
date:   2017-08-18 14:00:00
categories: Bordeaux médoc
tag: 1855 classification growth
---

A classification based on reputation rather than terroir

<h3>Where and what growth ?</h3>
<span>Bonus practice: guess second wine</span>
<br>
<h4 id="bdx"></h4>
<button id="test_me">Try me !</button>

<script>
	var chateaux = ["Château Haut-Brion", "Château Lafite-Rothschild", "Château Latour", "Château Margaux", "Château Mouton-Rothschild"]

	$("#test_me").click(function(){
		var chateau = chateaux[Math.floor(Math.random()*chateaux.length)];
		$("#bdx").empty();
		$("#bdx").append("<span>" + chateau + "</span>");
	});

</script>