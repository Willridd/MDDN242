Will Ridd MDDN242

Clock.js
function draw_clock(obj) {
    // draw your own clock here based on the values of obj:
    //    obj.hours goes from 0-23
    //    obj.minutes goes from 0-59
    //    obj.seconds goes from 0-59
    //    obj.millis goes from 0-1000
    //    obj.seconds_until_alarm is:
    //        < 0 if no alarm is set
    //        = 0 if the alarm is currently going off
    //        > 0 --> the number of seconds until alarm should go off

// Update this function to draw you own maeda clock on a 960x500 canvas
 
 
 
 background(102,111,124);
 fill(66, 134, 244);
 const ballWidth = 100;
 let millis = obj.millis
 let sec = obj.seconds;
 let mins = obj.minutes
 let hour = obj.hours
 

strokeWeight(0);
fill(0,35,91);
let posX = map(obj.millis, 0 , 999, ballWidth/2, width-ballWidth/2);
let posY = map(72,0, 100, 0, height);
square(posX, posY, ballWidth);

fill(255);
textSize(50);
text(sec,posX+27,posY+70);

 // fill(255,255,0);
 // let secs = obj.seconds;
 // let millis = obj.millis
 // let exactSeconds = secs + millis/ 1000.0;

// strokeWeight(0);
// fill(0,35,91);
// posX = map(sec, 0 , 59, ballWidth/2, width-ballWidth/2);
// posY = map(60,0, 100, 0, height);
// ellipse(posX, posY, ballWidth);


strokeWeight(0);
fill(0,35,91);
posX = map(mins, 0 , 59, ballWidth/2, width-ballWidth/2);
posY = map(40,0, 100, 0, height);

strokeWeight(0);
fill(0,35,91);
posX = map(hour, 0 , 23, ballWidth/2, width-ballWidth/2);
posY = map(20,0, 100, 0, height);

strokeWeight(0);
fill(0,35,91);
posX = map(millis, 0 , 999, ballWidth/2, width-ballWidth/2);
posY = map(20,0, 100, 0, height);


//conveyor belt 
square(40,250,200,250);
fill(0,70,130);
square(1,290,200,290);     
stroke(0,70,130);
strokeWeight(10)
line(200,485,1000,485);
stroke(0,35,91);
line(220,445,1000,445);
strokeWeight(0);
stroke(1);

fill(0,70,130);
beginShape(); //top of the conveyor belt conponent
vertex(0,290); 
vertex(40,250);
vertex(240,250);
vertex(202,290);
endShape(CLOSE);


strokeWeight(0);
fill(255);
textSize(100);

text(hour,40,425);

fill(188,210,244);
strokeWeight(5);  

//Right Window
square(20,20,200,40);
square(700,20,200,40); 
line(115,20,115,220);
line(795,20,795,220); 
line(20,120,220,120);
line(700,120,900,120); 
}





=======
