# Android Test Task Introduction

Springworks' product is live in a several different countries such as Sweden, Denmark and Switzerland.
The Product supports Swedish/Danish/English/Swiss-German/Italian/French languages. Each market has a different configuration and different requirements. To support all of them, the app should be really flexible, views-dynamic and based on a data fetched from the server. That's why we want to see how you will solve similar problem.

# Initial information
Imagine, you have a few different *markets*, where your app will be presented: Sweden, Spain, Poland. Each *market* has specific requirements which define:
1. How to show user information. Some *markets* could display it in the app, other should navigate to external website.
2. Some *markets* have a WiFi feature, other do not.
3. Each market has list of supported languages.
That means the app should support only specific languages for a selected market.

Example: You have Spanish, Swedish and English translations. Market 'sweden' supports locales "se" and "en".
* If a user starts the app with Swedish locale on the phone, he should see the app in swedish.
* If a user starts the app with Danish locale on the phone, he should see the app in english.
* If a user starts the app with Spanish locale on the phone, he should still see it in english, because "es" not supported by market.

Market should be configured with the app build.
To configure the 'market' for the app, just hardcode a value in build.gradle or Application. So to build app for market 'Sweden' you need to set param in build.gradle to 'sweden' to build for Spain to 'spain' and etc.

All data is provided from the server as configuration in a *json* format.
All translations are provided from the server in a *json* format.
You also have a design which shows all existing UI elements you could have  

# Design
Design provided in a [Sketch file](/settings-screen.sketch)

If you don't have Sketch, use these exported images.
Here you could see, what is expected results for each market.

![Settings Screen for Sweden](/settings_screen_sweden.png)
![Settings Screen for Spain](/settings_screen_spain.png)
![Settings Screen for Poland](/settings_screen_poland.png)
![Color Palette](/theme.png)

# Implementation

Using the initial information and all provided resources, you will need to write an Android application which displays a Settings screen according to provided market configuration.

1. Use Java or Kotlin or both, it's up to you.
2. Frameworks/Libraries are up to you.
3. Think about the app as a potentialy large scaleable project.
4. The app should have a Settings screen which displays [information](/user_data) according to provided [Market configuration](/config).
5. The app should persist state during configuration changes.
6. The app should support only specific locales for market.
7. Tests would be nice
8. Do your best.

# Tests

You might wonder, 'What should I test here?'. I would like to give you few examples.
Since the app should be flexible and dynamic for a configuration you provide, I would like to see tests which verifies:
1. Which view is displayed by provided configuration.
2. Proper language used in the app.
3. By clicking on the button app do correct interaction.
4. Values displayed / or not on the screen are correct.

## What we don't require
1. We don't care which library you will use to parse a json.
2. We don't care about edge cases for stuff like storing, reading, parsing of initial data.
3. You don't even need to test file reading, parsing, and etc.

# Submiting
Just send us your code along with a description on how to run the app and the tests. If there is anything that you have not had time to complete or intentionally left out please provide an explanation for how you would implement it, or why it was left out.
