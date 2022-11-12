<!DOCTYPE html>
<html>
<head>
<title>
How to create drag and drop
features for images reorder
using HTML CSS and jQueryUI?
</title>
<link href =
"
https://code.jquery.com/ui/1.10.4/themes/ui-lightness/jquery-ui.css
"
rel = "stylesheet">
<script src =
"
https://code.jquery.com/jquery-1.10.2.js
">
</script>
<script src =
"
https://code.jquery.com/ui/1.10.4/jquery-ui.js
">
</script>
<style>
/* text align for the body */
body {
text-align: center;
}
/* image dimension */
img{
height: 200px;
width: 350px;
}
/* imagelistId styling */
#imageListId
{
margin: 0;
padding: 0;
list-style-type: none;
}
#imageListId div
{
margin: 0 4px 4px 4px;
padding: 0.4em;
display: inline-block;
}
/* Output order styling */
#outputvalues{
margin: 0 2px 2px 2px;
padding: 0.4em;
padding-left: 1.5em;
width: 250px;
border: 2px solid dark-green;
background : gray;
}
.listitemClass
{
border: 1px solid #006400;
width: 350px;
}
.height{
height: 10px;
}
</style>
<script>
$(function() {
$( "#imageListId" ).sortable({
update: function(event, ui) {
getIdsOfImages();
}//end update
});
});
function getIdsOfImages() {
var values = [];
$('.listitemClass').each(function (index) {
values.push($(this).attr("id")
.replace("imageNo", ""));
});
$('#outputvalues').val(values);
}
</script>
</head>
<body>
<h1 style="color:green">Image slider code</h1>
<div class="height"></div><br>
<div id = "imageListId">
<div id="imageNo1" class = "listitemClass">
<img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSuiuiYY--ENGKHCxoshOIavDEMIyHjKkpARw&usqp=CAU" alt="">
</div>
<div id="imageNo2" class = "listitemClass">
<img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQlK2M1Xug43c231c4fFZnqKT3JjZOR6S0boA&usqp=CAU" alt="">
</div>
<div id="imageNo3" class = "listitemClass">
<img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQTz3bmxHcqUT6UgLs9x2YvDISS-V1CwIdRtQ&usqp=CAU" alt="">
</div>
<div id="imageNo4" class = "listitemClass">
<img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRELwIdHzkB__7V2e9bKSTzUOfy2BTYLsTK7A&usqp=CAU" alt="">
</div>
<div id="imageNo5" class = "listitemClass">
<img src="https://img.freepik.com/free-photo/wide-angle-shot-single-tree-growing-clouded-sky-during-sunset-surrounded-by-grass_181624-22807.jpg?w=2000" alt="">
</div>
<div id="imageNo6" class = "listitemClass">
<img src="https://media-exp1.licdn.com/dms/image/C510BAQHQC2IWaEf3Ow/company-logo_200_200/0/1586344408014?e=2147483647&v=beta&t=GKmjcxnbnhI42izu04TPD_8OZHfPjPOpyKuHbJQ-_vE" alt="">
</div>
</div>
<div id="outputDiv">
<b>Output of ID's of images : </b>
<input id="outputvalues" type="text" value="" />
</div>
</body>
</html>
