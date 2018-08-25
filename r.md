---
layout: null
---
<body onload="callGoogleScript();">
<script>
function callGoogleScript() {

	var url = "https://script.google.com/macros/s/AKfycbwQt4QiNTg8RjaAVd4KHZ_yClTbzgrvF34FZIIgEmIb8yGSHn8/exec?callback=loadData&id=1vsGEAbtDMvbURAUq-pio2O2oYaX-i76hjOPYNX4KwMk&sheet=Sheet1&num="+ getURLParameter("num");
// Make an AJAX call to Google Script
var request = jQuery.ajax({
      crossDomain: true,
      url: url,
      method: "GET",
      dataType: "jsonp"
    });
  }
 
 // print the returned data from jsonp
  function loadData(e) {
  //console.log(e);
  try {
  var rows= e;
         for (var i = 1; i < rows.length; i++) {
	 if (Array.isArray(rows[i])){
          for (var p = 0; p < rows[i].length; p++) { 
         $("#main").append(rows[i][p]+"<br>");
        	  }
	}else{
	//display everything
	  $("#main").append(rows[i]+"<br>");
	}
	  }
	}catch(err) {
        $("#main").append("No such id. "+ err);
	}
}
  </script>
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>
<div id="main"></div>
<script>
function getURLParameter(name) {
    var para= decodeURI((RegExp(name + '=' + '(.+?)(&|$)').exec(location.search)||[,null])[1]);
   console.log("Fetching: "+para);
   return para;
}	
</script>
</body>
