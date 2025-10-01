# Ex04 Places Around Me
# Date:1.10.2025
# AIM
To develop a website to display details about the places around my house.

# DESIGN STEPS
## STEP 1
Create a Django admin interface.

## STEP 2
Download your city map from Google.

## STEP 3
Using <map> tag name the map.

## STEP 4
Create clickable regions in the image using <area> tag.

## STEP 5
Write HTML programs for all the regions identified.

## STEP 6
Execute the programs and publish them.

# CODE
```
map.html
{% load static %}
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MY PLACE</title>
</head>
<style>
    h1{
        color: rgba(0, 21, 255, 0.873);
        font-weight: bolder;
        }
    body{
        background-color: aqua;
    }   
</style>
<body>
    <h1 align="center">URAPAKKAM</h1>
    <h2 align="center">MONISHA.S - 25017984</h2>
    <center>
        <img src="{% static 'img.png' %}"  usemap="#My Place" height="700" width="1600">
        <map name="My Place">
        <area shape="rect" coords="762,273,909,263,750,371,895,383" href="{% url 'img' %}" title="My home town">
        <area shape="poly" coords="224,68,352,50,184,141,387,91,285,20,289,138,191,35" href="{%url 'park'%}" title="park">
        <area shape="poly" coords="378,597,469,565,543,528,426,703,526,672,615,642,398,648,609,555" href="{% url 'shop' %}" title="shop">
        <area shape="poly" coords="157,599,232,571,306,529,350,604,318,668,240,683,175,651" href="{% url 'place' %}" title="sirpi nagar">
        <area shape="circle" coords="1131,557,31" href="{% url 'sports' %}" title="sports academy">
        </map>
    </center>    

    
    
</body>
</html>

img.html
{% load static %}
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body bgcolor="plum">
    <h1 align="center">Urapakkam</h1>
    <img src="{% static 'urapakkam.png' %}" height="600" width="900" align=" right center">
    <p><h2 text-align="center">Urapakkam is a southern suburb of Chennai, in the Chengalpattu district, Tamil Nadu.

It is governed as a census town / panchayat; it lies on the National Highway 32 (previously GST Road or NH45). 

It is fairly close to Tambaram (about 8 km) and about 21 km from Chengalpattu. 

The postal code is 603210.</h2></p>
</body>
</html>

park.html
{% load static %}
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Park</title>
</head>
<body bgcolor="pink">
    <h1 align="center">PARK</h1>
    <img src="{% static 'park1.png' %}" height="500" width="800"> <img src="{% static 'park2.png' %}" height="500" width="800">
    <p><h2>It has a walking / jogging path, green lawns, lots of trees, benches.
Children play area (slides, swings etc.), although some are said to be broken or in need of repair. 
The Times of India
Outdoor sports: people mention badminton courts, shuttle, etc. 
There is a public library (quite old; established mid-20th century, 1957) inside the park with a good collection of books, periodicals.</h2></p>
    
</body>
</html>

shop.html
{% load static %}
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>shop</title>
</head>
<body bgcolor="orange">
    <h1 align="center">SHOP</h1>
    <img src="{% static 'shop1.png' %}" height="500" width="800"> <img src="{% static 'shop2.png' %}" height="500" width="800">
    <p><h2>Zudio has a branch in Selaiyur, East Tambaram. 
Address: Plot No. 153, Velachery Main Road, Opposite Selaiyur Police Station, Selaiyur, East Tambaram, Chennai - 600059, Tamil Nadu 
Another listing shows a Zudio “Garment Showroom” in Tambaram Sanatorium area. 
Justdial
The local listing (Magicpin) gives the address for “Zudio, Tambaram, Chennai” as 59, Raja Iyer St, Tambaram East, ChennaiThe store typically offers men’s, women’s, and kids clothing, casual wear, accessories, footwear, etc.</h2></p>

    
</body>
</html>

place.html
{% load static %}
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>place</title>
</head>
<body bgcolor="violet">
    <h1 align="center">SIRPI NAGAR</h1>
    <img src="{% static 'sirpi1.png' %}" height="500" width="800"> <img src="{% static 'art.png' %}" height="500" width="800">
    <p><h2>Siripi Nagar is a locality in Guduvancheri, in the Kanchipuram / Chengalpattu district area of Tamil Nadu. 
It is part of the Chennai metropolitan region (southern part) — many real estate listings refer to it as “Siripi Nagar, Guduvancheri, Chennai South.” 
Its PIN code is 603202 (Postal sub-office: Guduvanchery)
Infrastructure & Facilities

Education: Several schools in or near Siripi Nagar:

St. John’s Matriculation Higher Secondary School (≈ 800 m) 
Housing

Bharathiyar Matriculation Higher Secondary School (≈ 1.3 km) 
Housing

Govt Boys Higher Secondary School, Nandivaram (≈ 1.3 km) 
Housing

Holy Sai International School, Sivananda Gurukulam etc.</h2></p>
    
</body>
</html>

sports.html
{% load static %}
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>sports</title>
</head>
<body bgcolor="yellow">
    <h1 align="center">SPORTS</h1>
    <img src="{% static 'sports1.png' %}" height="500" width="800"> <img src="{% static 'sports2.png' %}" height="500" width="800">
    <p><h2>CSK Sports Academy Turf, Urapakkam: This is a facility listed under “CSK Sports Academy Turf” at Urapakkam (which is near Tambaram / Chennai). It's for cricket ground, nets etc. 
turftown.in

CSK Sports Academy (Badminton Courts), Urapakkam: Also at Urapakkam, there are badminton courts associated with CSK Sports Academy. 
turftown
Kinetic Sports Academy, Tambaram: Offers coaching in multiple sports (cricket, football, basketball, tennis, boxing, etc.). 
Super Sports Turf / Grounds in Tambaram area for cricket & football. 
super-sports-cricket-and-football-turf.cricketground.in</h2></p>
    
</body>
</html>

```
# OUTPUT
![alt text](<../mapapp/static/Screenshot 2025-10-01 191444.png>)
![alt text](<../mapapp/static/Screenshot 2025-10-01 191412.png>)
![alt text](<../mapapp/static/Screenshot 2025-10-01 191328.png>)
![alt text](<../mapapp/static/Screenshot 2025-10-01 191253.png>)
![alt text](<../mapapp/static/Screenshot 2025-10-01 191156.png>)
![alt text](<../mapapp/static/Screenshot 2025-10-01 191132.png>)

# RESULT
The program for implementing image maps using HTML is executed successfully.
