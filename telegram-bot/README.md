# BarkPaws Telegram Bot
**Enhancing DeFi experience on Solana blockchain**

![BarkPaws Logo](./assets/logo.png)

The BarkPaws Telegram bot is designed to provide an intuitive and user-friendly interface for various functionalities related to decentralized finance (DeFi) on the Solana blockchain. This bot enhances the user experience by simplifying the processes of token swaps, trade monitoring, humanitarian support, fundraising campaigns, donations using BARK tokens, and accessing support. Utilizing the Solana Token-2022 standard, BarkPaws ensures enhanced functionality and security for its users.

## Key Features:

### Token Swaps
- Facilitate easy and efficient swapping of tokens on the Solana blockchain.
- Support for multiple token pairs with real-time price updates.
- Simple and secure transaction processes.

### Trade Monitoring
- Real-time updates on trade statuses.
- Notifications for completed, pending, or failed transactions.
- Detailed transaction history and analytics.

### Humanitarian Aid Support
- Platform to support and monitor humanitarian aid initiatives.
- Integration with various charitable organizations and causes.
- Transparent tracking of donations and fund utilization.

### Fundraising Campaigns
- Tools for launching and managing fundraising campaigns.
- Support for various campaign types, including emergency relief, development projects, and community initiatives.
- Real-time progress tracking and donor engagement features.

### Donations with BARK Tokens
- Facilitate donations using BARK tokens with fees.
- Secure and transparent donation processes.
- Integration with various causes and organizations.

### Support and Assistance
- 24/7 support through the Telegram bot.
- Automated responses for common queries and issues.
- Access to a support team for complex problems.

### Enhanced Security and Functionality
- Leveraging Solana Token-2022 standard for improved security.
- Advanced features such as token locking, multi-signature accounts, and more.
- Regular security updates and audits to ensure user safety.
- Develop Factory Program.

## Benefits of Using BarkPaws
- **User-Friendly Interface**: Simplifies complex DeFi operations making them accessible to a broader audience.
- **Real-Time Updates**: Keeps users informed about their trades, donations, and campaign statuses instantly.
- **Low Fees**: Cost-effective transactions, especially for donations using BARK tokens.
- **Transparency**: Clear tracking of funds and donations, ensuring trust and reliability.
- **Enhanced Security**: Adopting the latest standards and practices to protect user assets and data.

## Frameworks and Technologies Used

- **Node.js**: JavaScript runtime for the server.
- **Express**: Web framework for Node.js.
- **Telegram Bot API**: Library for interacting with the Telegram Bot API.
- **Axios**: Promise-based HTTP client for the browser and Node.js.
- **MongoDB**: NoSQL database for storing user data and trade histories.
- **i18next**: Internationalization framework for Node.js applications.
- **dotenv**: Module for loading environment variables from a `.env` file.
- **@solana/web3.js**: Solana JavaScript API for interacting with the Solana blockchain.

## Getting Started

### Prerequisites
- Node.js (v18 or later)
- MongoDB (v4 or later)
- Solana CLI
- Telegram account

barkpaws-telegram-bot/
│
├── src/
│   ├── controllers/
│   │   ├── authController.js          # Controller for authentication endpoints
│   │   └── swapController.js          # Controller for token swap endpoints
│   │
│   ├── middleware/
│   │   └── authMiddleware.js          # Middleware for user authentication
│   │
│   ├── services/
│   │   ├── authService.js             # Service for user authentication
│   │   └── swapService.js             # Service for token swap logic
│   │
│   ├── routes/
│   │   ├── authRoutes.js              # Routes for authentication endpoints
│   │   └── swapRoutes.js              # Routes for token swap endpoints
│   │
│   ├── utils/
│   │   └── helpers.js                 # Utility functions
│   │
│   ├── locales/
│   │   └── en/
│   │       └── translation.json       # Translation file for English
│   │
│   ├── app.js                         # Main application file
│   ├── bot.js                         # Telegram bot setup and logic
│   ├── config.js                      # Configuration file
│   ├── database.js                    # Database connection file
│
├── assets/
│   └── logo.png                       # Project logo
│
├── .env                               # Environment variables
├── .gitignore                         # Git ignore file
├── package.json                       # Project dependencies and scripts
├── README.md                          # Project documentation
├── LICENSE                            # License file
└── CODE_OF_CONDUCT.md                 # Code of conduct file

### Installation

1. Clone the repository
    ```sh
    git clone https://github.com/bark-community/barkpaws-bot-monorepo.git
    cd barkpaws-telegram-bot
    ```

2. Install dependencies
    ```sh
    npm install
    ```

3. Create a `.env` file with configuration
    ```sh
    touch .env
    ```

    Add the following variables to your `.env` file:
    ```
    TELEGRAM_BOT_TOKEN=bark_telegram_bot_token
    MONGO_URI=mongodb://localhost:27017/barkpaws
    BARK_DEV_SWAP_API=https://api-dev-swap.barkpaws.app
    SOLANA_TRADE_STATUS_API=https://api.solana.trade/status
    ```

4. Set up localization files
    Create the `locales` directory and add JSON files for each supported language (e.g., `locales/en/translation.json`).

    Example `locales/en/translation.json`:
    ```json
    {
        "welcome_message": "Welcome to BarkPaws Bot! How can we assist you today?",
        "initiate_swap": "Initiate Token Swap",
        "monitor_trade": "Monitor Trade Status",
        "support": "Support",
        "settings": "Settings",
        "resources": "Educational Resources",
        "stake_tokens": "Stake BARK Tokens",
        "governance": "Governance",
        "swap_prompt": "Please provide the following details to initiate a token swap:\n1. Token to Swap From\n2. Token to Swap To\n3. Amount\n4. Confirm Wallet Address",
        "swap_success": "Swap initiated successfully. Transaction ID: {{txId}}",
        "swap_failure": "Failed to initiate swap: {{error}}",
        "status_prompt": "Please enter your Trade ID to check the status:",
        "status_success": "Trade status: {{status}}",
        "status_failure": "Failed to check trade status: {{error}}",
        "support_message": "How can we assist you? Please describe your issue, and our support team will get back to you shortly.",
        "settings_message": "Settings:\n- Change Language\n- Notification Preferences\n- Security Settings",
        "resources_message": "Choose a topic to learn more:\n- How to Use BarkPaws Bot\n- Understanding DeFi\n- FAQs",
        "stake_message": "Enter the amount of BARK Tokens you want to stake:",
        "governance_message": "View current proposals and vote using your BARK Tokens.",
        "invalid_input": "Invalid input. Please provide all the necessary details."
    }
    ```

### Running the Bot

1. Ensure MongoDB is running and the `.env` file is properly configured.
2. Start the bot:
    ```sh
    node src/bot.js
    ```

## Usage

Interact with the bot on Telegram by sending commands or using the inline menu. Available commands include:
- `/start` to initiate interaction with the bot.
- `/swap` to initiate a token swap.
- `/status` to monitor trade status.
- `/support` to get support.
- `/settings` to configure settings.
- `/resources` to access educational resources.
- `/stake` to stake BARK Tokens.
- `/governance` to participate in governance.

## Contributing

Contributions are welcome! Please fork the repository and create a pull request with your improvements.

## References

- [Telegram Bot API Documentation](https://core.telegram.org/bots/api): Official documentation for the Telegram Bot API, providing detailed information about available methods and parameters for building Telegram bots.
- [Solana Documentation](https://docs.solana.com/): Official documentation for the Solana blockchain platform, offering resources for developers to build applications on Solana.
- [MongoDB Documentation](https://docs.mongodb.com/): Official documentation for MongoDB, providing guidance on installation, setup, and usage of MongoDB database.

## License

MIT License.
