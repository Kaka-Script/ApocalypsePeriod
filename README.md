addEventListener("keydown", function(a) {
if (a.keyCode==192){
lag()
lag2()
}
function lag(){
var a = player.x + targetDst * MathCOS(targetDir) + camX,
d = player.y + targetDst * MathSIN(targetDir) + camY;
for (var e = [], b = 0; b < selUnits.length; ++b) e.push(selUnits[b].id);
socket.emit("5", UTILS.roundToOne(a), UTILS.roundToOne(d), e, 0, -1)
}
function lag2(){
var a = player.x + targetDst * MathCOS(targetDir) + camX,
d = player.y + targetDst * MathSIN(targetDir) + camY;
for (var e = [], b = 0; b < selUnits.length; ++b) e.push(selUnits[b].id);
socket.emit("5", UTILS.roundToTwo(a), UTILS.roundToTwo(d), e, 0, -1)
}})
