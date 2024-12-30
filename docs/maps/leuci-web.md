# Web applications for density exploration

## django-python app
There is a django-framework web application available to explore the density interactively. 
This is not satsifactory as it is not fast enough, unnecessary, overengineered and I can't afford to 
host it anywhere sensible.  However it is really useful for exploration. I am most likely to run it locally. 

Here it is on a free tier on azure - [maptial@azure](https://maptial.azurewebsites.net/)

The primary usefulness of the web app over the colab pages for specific analyses and images, 
is the ability to navigate and explore. I am particularly pleased with the navigation panel 
that allows orthogonal movement in space, plus tilts on all axes and the plane. 
The yellow dots are the position dots on the plane - they go cyan when they are forward of the plane and line green when behind. 
Because this is written in djanjo there is considerable work on both the client and server, 
and with javascript and python to optimise as much as possible - caching in javascript when a 
calculation is not necessary e.g. the changing of the hue. Quite unnecessary but quite fun.  


![Alt Text](imgs/streamlit-peptide.gif)  
Structure 2bf9

<!-- 
Converted from a streamlit screen cast to a gif
https://cloudconvert.com/webm-to-gif
 -->

## python-app as a docker image

The image is on dockerhub at [raea/maptial](https://hub.docker.com/repository/docker/raea/maptial/general).  
It can be downloaded and run with docker, it will use it's own internal fileset which will not 
persist when the image is destroyed, for pdb and ccp4 files:

If you run the below from a command line it will pull it the first time:

```
docker run -p 8000:8000 raea/maptial
```

This will then run on the localhost and can be found at: [http://localhost:8000](http://localhost:8000)

## C# web application
Before the python webapp, there was a .net C# version. Before that there was a fully fledged windows C# application. The windows applicaiton was substantially faster, the web is not a good medium for the data and numerical intensity of the calculations, but it is the easiest to use for distribution.  To mess about with C# I need to use my windows laptop and Visual Studio rather than VSCode.  The main interest of the C# applicaiton was it integrated a neighbours search (you could hover over and see what the closest residue was in space) and it did some superposition. I elect to deprecate this now.  

## C++ web applicaiton
Until the day this gets turned off, because I would not be able to resurrect the code, an early version of some of the electorn density code in C++ is hosted at Birkbeck via a CGI webserver, using python to call the C++ executable. One day someone will realise, until then: 
[Leucippus@Birkbeck](https://student.cryst.bbk.ac.uk/~ab002/Leucippus.html)  






