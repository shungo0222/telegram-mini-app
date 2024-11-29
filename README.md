# Telegram Mini App Demo

A simple Telegram Mini App built with HTML, CSS, and JavaScript. This project demonstrates the basic features of Telegram Mini Apps, including retrieving initialization data, handling `startapp` parameters via direct links, and supporting home screen shortcuts.

## Features

1.  **StartApp Parameter Handling**
    
    -   Displays the `start_param` passed to the Mini App via a direct link (e.g., `https://t.me/botusername/appname?startapp=yourParam`).
2.  **Telegram Initialization Data Parsing**
    
    -   Parses and displays the data provided by the Telegram WebApp API for better readability.
3.  **Home Screen Shortcut Support**
    
    -   Checks the device's capability for adding the Mini App to the home screen.
    -   Responds to user actions such as adding a shortcut.
4.  **API Version Compatibility Check**
    
    -   Ensures that the necessary Telegram WebApp API version (`8.0+`) is supported for home screen shortcuts.

## Project Structure

-   **`index.html`**: Main HTML file containing the UI structure.
-   **`styles.css`**: Stylesheet for UI design.
-   **`script.js`**: JavaScript logic for interacting with the Telegram WebApp API.

## How to Use

### 1. Run the Mini App Locally

1.  Start a local server:
    
    `python3 -m http.server 3000` 
    
2.  Use [ngrok](https://ngrok.com/) to expose your local server:
    
    `ngrok http 3000`     

### 2. Configure the Telegram Bot

1.  Go to Telegram's `@BotFather` bot.
2.  Set the Web App URL to the `https` URL provided by `ngrok`.

### 3. Launch the Mini App

-   Open the bot in Telegram and tap the "Open App" button to launch the Mini App.
-   Alternatively, use a direct link format:
    
    `https://t.me/botusername/appname?startapp=yourParam` 

## Displayed Information

The following data is displayed in the Mini App UI:

1.  **StartApp Parameter**
    
    -   Displays the `start_param` passed via the direct link.
2.  **Telegram Data**
    
    -   Shows parsed initialization data from the Telegram WebApp API.
3.  **Version Support Status**
    
    -   Indicates whether the current device supports the required WebApp API version.
4.  **Home Screen Shortcut Status**
    
    -   Displays the current status of the home screen shortcut:
        -   `Unsupported`: Device doesn't support shortcuts.
        -   `Unknown`: Unable to determine if the shortcut is added.
        -   `Added`: Shortcut already added.
        -   `Missed`: Shortcut not yet added.

## Limitations

-   **Device Compatibility**: Home screen shortcut features may behave differently across devices.
-   **Version Restrictions**: Requires Telegram WebApp API version `8.0+` for home screen features.

## License

This project is for educational purposes. Feel free to modify and adapt as needed.

## Acknowledgments

-   [Telegram WebApp API Documentation](https://core.telegram.org/bots/webapps)
-   [ngrok](https://ngrok.com/) for exposing local servers.
