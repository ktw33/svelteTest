<div id="test" ondrop="drop(event)" ondragover="allowDrop(event)">

<h1 draggable="true" ondragstart="drag(event)" id="canvas">Canvas</h1> 

</div>

<div id="testTarget" ondrop="drop(event)" ondragover="allowDrop(event)"></div>


<style>
#test {
    border: 2px solid black;
    width: 100%;
    height: 200px;
}
#testTarget {
    border: 2px solid black;
    width: 100%;
    height: 200px;
}

</style>

<script>
function allowDrop(ev) {
  ev.preventDefault();
}

function drag(ev) {
  ev.dataTransfer.setData("text", ev.target.id);
}

function drop(ev) {
  ev.preventDefault();
  var data = ev.dataTransfer.getData("text");
  ev.target.appendChild(document.getElementById(data));
}

</script>
