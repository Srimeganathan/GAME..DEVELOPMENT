# EX 7 : THREE DIMENSIONAL TRANSFORMATIONS

## AIM :
 
 To implement the various transformations on three dimensional odjects using a c coding.

## EQUIPMENT REQUIRED:

●	Hardware: Personal Computer (PC)

●	Software: C Compiler

## ALGORITHM :


   Step 1 : Start.

   Step 2 : Draw an image with default parameters.

   Step 3 : Get the choice from user.

   Step 4 : Get the parameters for transformation.

   Step 5 : Perform the transformation.

   Step 6 : Display the output.

   Step 7 : Stop.

## Program :
~~~
#include<stdio.h> 
#include<conio.h> 
#include<graphics.h> 
#include<math.h> 
int maxx,maxy,midx,midy; 
void axis() 
{ 
getch(); 
cleardevice(); 
line(midx,0,midx,maxy); 
line(0,midy,maxx,midy); 
} 
void main() 
{ 
int gd,gm,x,y,z,o,x1,x2,y1,y2; 
detectgraph(&gd,&gm); 
initgraph(&gd,&gm," "); 
setfillstyle(0,getmaxcolor()); 
maxx=getmaxx(); 
maxy=getmaxy(); 
midx=maxx/2; 
midy=maxy/2; 
axis(); 
bar3d(midx+50,midy-100,midx+60,midy-90,5,1); 
printf("Enter Translation Factor"); 
scanf("%d%d%d",&x,&y,&z); 
axis(); 
printf("after translation"); 
bar3d(midx+(x+50),midy-(y+100),midx+x+60,midy-(y+90),5,1); 
axis(); 
bar3d(midx+50,midy+100,midx+60,midy-90,5,1); 
printf("Enter Scaling Factor"); 
scanf("%d%d%d",&x,&y,&z); 
axis(); 
printf("After Scaling"); 
bar3d(midx+(x*50),midy-(y*100),midx+(x*60),midy-(y*90),5*z,1); 
axis(); 
bar3d(midx+50,midy-100,midx+60,midy-90,5,1); 
printf("Enter Rotating Angle"); 
scanf("%d",&o); 
x1=50*cos(o*3.14/180)-100*sin(o*3.14/180); 
y1=50*cos(o*3.14/180)+100*sin(o*3.14/180); 
x2=60*sin(o*3.14/180)-90*cos(o*3.14/180); 
y2=60*sin(o*3.14/180)+90*cos(o*3.14/180); 
axis(); 
printf("After Rotation about Z Axis"); 
bar3d(midx+x1,midy-y1,midx+x2,midy-y2,5,1); 
axis(); 
printf("After Rotation about X Axis"); 
bar3d(midx+50,midy-x1,midx+60,midy-x2,5,1); 
axis(); 
printf("After Rotation about Y Axis"); 
bar3d(midx+x1,midy-100,midx+x2,midy-90,5,1); 
getch(); 
closegraph(); 
}

~~~
## Output :
![440840313-09c0ecf2-6bbc-4019-8cd5-f2b4ff5a51f9](https://github.com/user-attachments/assets/220d84b5-b913-4401-95b6-f8b602df3271)
![440840395-578944b8-d3ab-417e-870f-b1e43375c505](https://github.com/user-attachments/assets/d0d6e427-455a-498a-bd09-03c730fc6ed8)
![440840566-b81c5a98-6a3b-40fe-8c4e-55929fd55266](https://github.com/user-attachments/assets/4b818bae-dd7e-41c0-ba6a-1466423fe1c3)
![440840632-eefb43e4-3195-42f5-9961-341c06aefb0d](https://github.com/user-attachments/assets/9809d81d-fe45-4910-9bd4-92572fda6e9c)
![440840706-7ab0d3cd-0d63-4803-90e3-9a6b63d89c7f](https://github.com/user-attachments/assets/914c40a4-fb6a-4cb9-9ba1-1b044a206e72)
![440840764-e38235ea-0f8a-437c-8700-5c0b08648c87](https://github.com/user-attachments/assets/8f6a0178-ca16-4696-a5c3-3136471d5c6c)
![440841060-593127e7-b404-447b-80ba-cca38adf78ed](https://github.com/user-attachments/assets/208c0f77-872b-4a2c-9b5c-17775cccf0be)
![440841138-d48cdc73-f198-4425-854f-33ef7b17fdb2](https://github.com/user-attachments/assets/820d050c-6f1a-4439-8914-4d248a3010c8)

## Result :
Thus, the C program for performing three-dimensional transformations — including translation, scaling, and rotation about the X, Y, and Z axes — was successfully implemented and the output was verified through graphical representation.
