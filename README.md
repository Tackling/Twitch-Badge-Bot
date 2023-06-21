# Twitch-Badge-Bot
This Node.js script monitors Twitch global badges and sends notifications to a Discord webhook when new badges become available.

## Prerequisites

Before running the BadgeBOT application, make sure you have the following:

- Node.js installed on your system
- Access to a Twitch developer account
- Access to a Discord server with a webhook URL
- The required credentials and configuration values (explained in the next section)

## Configuration

To configure the BadgeBOT application, you need to provide the following values in the `config.js` file:

- `clientId`: Your Twitch application client ID.
- `clientSecret`: Your Twitch application client secret.
- `roleId`: The Discord role ID to mention when sending notifications.
- `webhookUrl`: The Discord webhook URL to send notifications to.

Make sure to replace the placeholder values in the `config.js` file with your actual credentials and configuration.

## Installation

To install the dependencies required by the BadgeBOT application, run the following command: `npm install`

This will install the required packages specified in the `package.json` file.

## Usage

To start the BadgeBOT application, run the following command: `node index.js`

The application will initially send a notification to the Discord server indicating that BadgeBOT is online. It will then start checking for new badges on Twitch every minute.

If a new badge is found, BadgeBOT will send a Discord notification mentioning the specified role.

To stop the application, you can press `Ctrl + C` in the terminal.

## Troubleshooting

If you encounter any issues or errors while running the BadgeBOT application, please check the following:

- Ensure that the `config.js` file contains the correct credentials and configuration values.
- Make sure you have an active internet connection.
- Verify that the provided Discord webhook URL is valid and accessible.
- Double-check your Twitch application credentials and ensure they are correctly entered in the `config.js` file.

If the issue persists, please refer to the error message displayed in the terminal for further information.

## Customization

You can customize the behavior of the BadgeBOT application by modifying the following:

- Adjust the interval at which the application checks for badge updates by changing the value passed to `setInterval` in the code. The default is set to 1 minute (`60000` milliseconds).
- Modify the content of the initial Discord notification sent by modifying the `content` parameter in the `sendInitialDiscordNotification` function.
- Customize the format or content of the Discord notification sent for new badge updates by modifying the `message` parameter in the `sendDiscordNotification` function.

## License

This BadgeBOT application is open source and distributed under the [MIT License](https://opensource.org/licenses/MIT).
