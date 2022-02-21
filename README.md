# Design a Website for Server Side Processing

## AIM:
To design a website to perform mathematical calculations in server side.

## DESIGN STEPS:

### Step 1:
Desing your website for calculation using wireframe work.

### Step 2:
Then to execute the wireframe work desing use html,css.


### Step 3:
Use views.py to execute the coding in serverside.


### Step 4:
Mention the path of the website in urls.py.

### Step 5:
Publish the website in the given URL.

## PROGRAM :
### Math.html:
```

<!DOCTYPE html>
<html>
<head>
    <meta charset='utf-8'>
    <meta http-equiv='X-UA-Compatible' content='IE=edge'>
    <title>Page Title</title>
    <meta name='viewport' content='width=device-width, initial-scale=1'>
    
</head>
<style>
    *{
        box-sizing: border-box;
        font-family:'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif
    }
    body{
    background-color: rgb(183, 44, 238);
    }

    .container{
    width: 1080px;
    height: 350px;
    margin-top: 100px;
    margin-left: auto;
    margin-right: auto;
    border-radius: 25px;
    border: 10px solid rgba(151, 92, 117, 0);
    box-shadow: inset 0 0 15px rgb(86, 6, 161);
    background-color:rgb(188, 133, 240);
    }
    h1{
        text-align: center;
        padding-top: 15px;
    }
    .calculate{
        padding-top: 10px;
        padding-bottom: 10px;
        padding-left: 10px;
        padding-right:10px;
        text-align: center;
        font-size: 20px;
    }
</style>
<body>
    <div class="container">
        <h1>AREA OF A RECTANGLE</h1>
        <form method="POST">
            <div class="calculate"> 
                Base:<input type="text" name="base" value=></input><br/>
            </div>
            <div class="calculate">
                Height:<input type="text" name="height" value=></input><br/>
            </div>
            <div class="calculate">
                <input type="submit" value="Calculatearea"></input><br/>
            </div>
            <div class="calculate">
                Area:<input type="text" name="area" value=></input>
            </div>
        </form>
    </div>
</body>

```

### views.py:
from django.shortcuts import render

def areacalculation(request):
    context ={}
    context["area"]='0'
    context["b"]='0'
    context["h"]='0'
    if request.method == 'POST':
        
        l=request.POST.get('base','0')
        b=request.POST.get('height','0')
        area=int(l)*int(b)
        context['area'] = area
        context['b']=b
        context['h']=h
    return render(request,"mathapp/area.html",context)

### urls.py:
from django.shortcuts import render

def areacalculation(request):
    context ={}
    context["area"]='0'
    context["b"]='0'
    context["h"]='0'
    if request.method == 'POST':
        
        l=request.POST.get('base','0')
        b=request.POST.get('height','0')
        area=int(l)*int(b)
        context['area'] = area
        context['b']=b
        context['h']=h
    return render(request,"mathapp/area.html",context)
## OUTPUT:
![output](https://github.com/Saibandhavi75/serversideprocessing/blob/main/web%20neww.PNG?raw=true)

## Result:
A website to perform mathematical calculations in server side is created.
