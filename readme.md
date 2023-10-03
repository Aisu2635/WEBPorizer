# Image Conversion Bot

This bot automates the conversion of JPG and PNG images in your repository to the WebP format, optimizes them, and updates the code base to work with the new format.

## How to Contribute

We welcome contributions to this project! To get started, follow these steps:

1. Fork this repository to your GitHub account.

2. Clone your forked repository to your local device:

   ```bash
   git clone https://github.com/your-username/image-conversion-bot.git
   cd image-conversion-bot
   code .
   ```

3. Install the required dependencies:
   ```bash
   npm install
   ```

4. Set up a webhook proxy using smee.io:
+ Visit https://smee.io/ in your browser.
+ Click "Start a new channel."
+ Copy the full URL under "Webhook Proxy URL." You will use this URL in a later step.

5. Create a GitHub App in your developer settings and note the following values:
+ APP_ID: Your GitHub App's ID.
+ WEBHOOK_SECRET: A secret key for secure communication.
+ PRIVATE_KEY_PATH: Path to your GitHub App's private key.

6. Create a .env file in the root of your project and add the following values:
```bash
APP_ID="YOUR_APP_ID"
WEBHOOK_SECRET="YOUR_WEBHOOK_SECRET"
PRIVATE_KEY_PATH="YOUR_PRIVATE_KEY_PATH"
```

7. Run the server with smee.io proxy URL:
```bash
npx smee -u WEBHOOK_PROXY_URL -t http://localhost:3000/api/webhook
```

Test your app and create a branch for the issue you want to work on.
Make your desired changes and commits to the branch.
When you're ready to contribute, create a pull request (PR) from your branch to the main repository's branch you intend to merge with.

## Documentation
For more details on writing code for a GitHub App and other relevant information, check out the [GitHub App Quickstart Guide](https://docs.github.com/en/apps/creating-github-apps/writing-code-for-a-github-app/quickstart).

Thank you for contributing to this project!
