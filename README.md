# Android Test Task Introduction

Product we do at Springworks works in a different countries like Sweden, Denmark and Switzerland.
The Product supports Swedish/Danish/English/Swiss-German/Italian/French languages. Each market has a different configurations and requirements. To support all of them, the app should be really flexible, views-dynamic and based on a data fetched from the server. That's why we want to see how you will solve similar problem.

# Initial information
Imagine, you have few different *markets*, where your app will be presented: Sweden, Spain, Poland. Each *market* has specific requirements which defines: 
1. How to show user information. Some *markets* could display it in the app, other should navigate to external website.
2. Some *markets* has a WiFi feature, other don't.
3. Each market has list of supported languages. 
Thats mean the app should support only specific languages for a selected market.

Example: You have Spanish, Swedish and English translations. Market 'sweden' supports locales "se" and "en". 
* If user start the app with Swedish locale on the phone, he should see the app in swedish. 
* If user start the app with Danish locale on the phone, he should see the app in english. 
* If user start the app with Spanish locale on the phone, he still should see it in english, because "es" not supported by market.

All this data provided from the server as configuration in a *json* format.
All translations provided from the server in a *json* format.
You also have a design which shows all existing UI elements you could have  

# Design
Design provided in a [Sketch file](/settings-screen.sketch) 

If you don't have Sketch, use this exported images.

![Settings Screen](/settings-screen.png)
![WiFi Edit Screen](/wifi-edit-screen.png)
![Color Palette](/theme.png)

# Implementation 

Using the initial information and all provided resources, you need to write an Android application which displays Settings screen according to provided market configuration.

1. Use Java or Kotlin or both, it's up to you.
2. Frameworks/Libraries up to you.
3. Think about the app as a potential big scalable project.
4. The app should have a Settings screen which displays [information](/user_data) according provided [Market configuration](/config).
5. User should be able to change WiFi name and password on [WiFi Edit Screen](/wifi-edit-screen.png)
6. The app should persist state during configuration changes.
7. The app should support only specific locales for market.
8. Tests would be nice
9. Do your best.

## What we don't require
1. We don't care which library you will use to parse a json.
2. We don't care about edge cases for stuff like storing, reading, parsing of initial data.
3. You don't even need to test file reading, parsing, and etc.

# Submiting
Just send us your code along with a description on how to run the app and the tests. If there is anything that you have not had time to complete or intentionally left out please reason on how you would implement it or why it was left out.
