class Paddle {
  float x, y;
  float vy;
  float radius;
  color c;

  Paddle(int pos) {
    x=pos;
    y=random(height);
    radius=10;
    vy=random(8);
    c=color(125, 125, 125);
  }

  void draw() {
    fill (c);
    rect(x, y, 15, 80);
  }

  void move() {
    y=y+vy;
    if (y<radius || y>height-radius) {
      vy=-vy;
    }
  }
}

void setup() {
  size(500, 500);
}

class Ball {
  float x, y;
  float vx, vy;
  float radius;
  color c;

  Ball() {
    x=random(width);
    y=random(height);
    radius=10;
    vx=random(6);
    vy=random(6);
    c=color(random(255), random(255), random(255));
  }

  void draw() {
    fill (c);
    ellipse(x, y, radius*2, radius*2);
  }

  void move() {
    x=x+vx;
    y=y+vy;
    if (x<radius || x>width-radius) {
      vx=-vx;
    }
    if (y<radius || y>height-radius) {
      vy=-vy;
    }
  }
}

Ball b = new Ball();
Paddle p = new Paddle(10);
Paddle p2 = new Paddle(475);

void draw() {
  noStroke();
  background(255);
  b.draw();
  b.move();
  p.draw();
  p.move();
  p2.draw();
  p2.move();
}
