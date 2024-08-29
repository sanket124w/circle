#include<graphics.h>
#include<dos.h>
#include<iostream.h>
#include<stdio.h>
#include<conio.h>
#include<stdlib.h>
#include<math.h>
void drawline(int x1, int y1, int x2, int y2)
{
	int dx,dy,m,s;
	float xi,yi,x,y;
	dx=x2-x1;
	dy=y2-y1;
	if(abs(dx)>abs(dy))
	   s=abs(dx);
	else
	   s=abs(dy);
	 xi=dx/(float)s;
	 yi=dy/(float)s;
	 x=xi;
	 y=yi;
	  putpixel(x,y,WHITE);
     }
     
      int main()
     {
      int gd = DETECT,gm = DETECT,gmode;
	  int x1,y1,x2,y2;
	  initgraph(&gd, &gm,"C:\\TURBOC3\\BGI");
	  drawline(80,80,400,80);
	  drawline(400,80,400,400);
	  drawline(400,400,80,400);
	  drawline(80,400,80,80);
	  drawline(80,240,240,80);
	  drawline(240,80,400,240);
	  drawline(400,240,240,400);
	  drawline(80,240,240,400);
	  circle(240,240,113);
	  delay(300);
	  getch();
	  closegraph();
	  return 0;
	  	  
}

