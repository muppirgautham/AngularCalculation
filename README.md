# AngularCalculation

# Web Page for Mathematical Calculations using Angular

## AIM:
To design a dynamic website to perform mathematical calculations using Angular Framwork

## DESIGN STEPS:

### Step 1:

Requirement collection.

### Step 2:

Creating the layout using HTML and CSS in component.html file

### Step 3:

Write typescript to perform the calculations.

### Step 4:

Validate the layout in various browsers.

### Step 5:

Validate the HTML code.

### Step 6:

Publish the website in the given URL.

## PROGRAM :

### app.component.html:
```
<body>
  <div class="container">
      <h1>Calculations</h1>
      <div class="subcontainer">
          
          <rectangle-area></rectangle-area>
      </div>
      <div class="subcontainer">
          <cylinder-area></cylinder-area>
      </div>
      <div class="footer">
          Developed by: GAUTHAM M
      </div>
  </div>
</body>

```
### rectangle.component.html:
```
<body>
    <h2>Area of Rectangle</h2>
    length = <input type="text" [(ngModel)]="length"> Meters<br>
    Breadth = <input type="text" [(ngModel)]="breadth"> Meters<br>
    <input type="button" (click)=" calculaterec()"  value="calculate"><br>
    area = <input type="text" [value]="area">
</body>
```
### cylinder.component.html:
```
<body>
    <h2>Area of cylinder</h2>
    radius = <input type="text" [(ngModel)]="radius"> Meters<br>
     height = <input type="text" [(ngModel)]="height"> Meters<br>
    <input type="button" (click)="calculatecyli()"  value="calculate"><br>
    area = <input type="text" [value]="area">
</body>
```
### app.comopnent.ts:
```
import { Component } from '@angular/core';

@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.css']
})
export class AppComponent {
  title = 'angularcalc';
}
```
### rectangle.component.ts:
```
import { Component } from "@angular/core";

@Component({
    selector:'rectangle-area',
    templateUrl:'./rectangle.component.html'
})
export class RectangleComponent{
    length:number
    breadth:number
    area:number
    constructor(){
        this.length=0
        this.breadth=0
        this.area=this.length*this.breadth
    }
    calculaterec(){
        this.area=this.length*this.breadth
    }

}
```
### cylinder.component.ts:
```
import { Component } from "@angular/core";

@Component({
    selector:'cylinder-area',
    templateUrl:'./cylinder.component.html'
})
export class CylinderComponent{
    radius:number
    height:number
    area:number
    constructor(){
        this.radius=0
        this.height=0
        this.area = this.area = 3.14*this.radius*this.radius*this.height
    }
    calculatecyli(){
        this.area = this.area = 3.14*this.radius*this.radius*this.height
    }

}
```
### app.component.css:
```
.container{
    background-color: skyblue;
    text-align: center;
    height: 700pxx;
}
.subcontainer{
    background-color: bisque;
    width: 600px;
    height: 290px;
    text-align: center;
    margin-left: 450px;
    margin-bottom: 50px;
}
h1{
    text-decoration: underline;
}
```
### app.module.ts:
```
import { NgModule } from '@angular/core';
import { FormsModule } from '@angular/forms';
import { BrowserModule } from '@angular/platform-browser';

import { AppComponent } from './app.component';
import { CylinderComponent } from './cylinder/cylinder.component';
import { RectangleComponent } from './Rectangle/rectangle.component';

@NgModule({
  declarations: [
    AppComponent,
    RectangleComponent,
    CylinderComponent
  ],
  imports: [
    BrowserModule,
    FormsModule
  ],
  providers: [],
  bootstrap: [AppComponent]
})
export class AppModule { }
```
### 

## OUTPUT:
![image](https://user-images.githubusercontent.com/94810884/154093030-b55806e2-04f5-4490-ad6d-11c85b5c213b.png)



## Result:
This is code successfully helps you to create a webpage to make mathematical calculations using angular.
