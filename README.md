# Android Test Task Introduction

Product we do at Springworks live in a different countries like Sweden, Denmark and Switzerland.
In our project we support Swedish/Danish/English/Swiss-German/Italian/French languages. Also each market has a different configurations and requirements. To support that, our app should be really flexible, views dynamic, based on a data fetched from the server. That's why we want to see how you will solve similar problem.

# Initial information
Imagine that you have few different *markets* where your app will be presented: Sweden, Spain, Poland. Each *market* has specific requirements which defines: 
1. How to show user information, some *markets* could display it in the app, other should navigate to external website
2. Some *markets* has WiFi feature, other don't.
3. Some *markets* supports HardwareA other HardwareB and HardwareC
All this data provided from the server as configuration in a *json* format.
You also have a design which shows all existing UI elements you could have  

# Design
Design provided in a [Sketch file](/settings-screen.sketch) 

![Settings Screen](/settings-screen.png)
![WiFi Edit Screen](/wifi-edit-screen.png)
![Color Palette](/theme.png)

# implementation 
All up to you
## Anti-requirements
1. We don't care which library you will use to parse a json
2. We don't care about edge cases for stuff like storing, reading, parsing of intiail data
3. You don't even need to test file reading, parsing, and etc.
