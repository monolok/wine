---
layout: post
title:  "DOCGS of Italy"
categories: Italy DOCGS 
tag: classification 
---

<blockquote>
  <p>.......</p>
</blockquote>

<div class="text-center">
	<h2>Where and what growth ?</h2>
	<span>Bonus practice: ...</span>
	<h4 class="text-danger" id="bdx">Wine</h4>
	<h4 class="text-success" id="bdx_answer">Answer</h4>
	<button type="button" class="btn btn-success" id="test_me">Next</button>
	<button type="button" class="btn btn-danger" id="answer">Answer</button>
</div>

<script>
	var chateaux = ["1", "2"];

	var chateaux_answers = ["1", "2"];
	
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