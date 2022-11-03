# A02
float x = 300;
float y = 300;
float angle = 0;
float dia = 20;

void setup() {
size (900, 900);
surface.setLocation(987, 70);

}

void draw() {
  background(25,5,207,32);
  
  translate(width/2, height/2);
  rotate(radians(angle/3));
  for (float a=0; a<360; a+=10) {
    
    pushMatrix();
  rotate(radians(a));
  stroke(245,35,45,200);
  strokeWeight(3);
  line(x* sin(radians(angle)), 0, 0, y-dia/2);
  
  noStroke();
  fill(255);
  ellipse(x*sin(radians(angle)), 0, dia/2, dia/2);
  stroke(245,35,45,200);
  noFill();
  ellipse(0, y, dia, dia);
  popMatrix();
 
  }
angle++;
//saveFrame("####_out.png");
}
