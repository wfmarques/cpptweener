Tweener (http://code.google.com/p/tweener/) it´s a great library for Flash/Flex Iteration programmer´s, so i´m tried make a version to C++, this is a alpha version, but total funcional. The example are based in a  openFrameworks template (http://wiki.openframeworks.cc/) .

Demo vídeo : http://www.youtube.com/watch?v=D7-B2e_RRXE

Now a Ultra Simple Quick hello world ( :-P ):

#include "CppTweener.h"

float px=10,py=10; // for now just accept float properties

tween::Tweener tweener;

void setup(){
> tween::TweenerParam param(2000, tween::CUBIC, tween::EASE\_OUT); //2 seconds tween

> param.addProperty(&px, 200);

> param.addProperty(&py, 30);

> tweener.addTween(param);

}

void update(){
> tweener.step(YOUR\_SYSTEM\_TimeMillis()); // :-)
}

void draw() {
> drawRect(px, py, 200, 200);//Your draw routine
}

Complete example in Source.