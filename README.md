### 1. Create `bearers.json`

You need to create a file named `bearers.json` in the root folder to store your authentication tokens (Bearer tokens). These tokens authenticate the bot to perform actions on your OpenLayer accounts.

The `bearers.json` file should have the following format:

```json
[
  "eyJhbGciOiJ...YourFirstBearerToken",
  "eyJhbGciOiJ...YourSecondBearerToken"
]
```

#### How to Get the Bearer Token?

1. Open the OpenLayer extension and log in to your account.
2. Right-click on the extension page and select **Inspect**.
3. Go to the **Console** tab.
4. Paste the following command into the console and press `Enter`:

   ```javascript
   console.log(localStorage.getItem('_open_layer_token_'))
   ```

5. Copy the value that appears. This is your Bearer token.
6. Add this token to your `bearers.json` file.

### 2. Run the Bot

You can now run the bot with the following command:

```bash
npm start
```

- The bot will display your account information.
- You'll be prompted to choose between an automatic daily check-in or exiting.

### 5. Automate Daily Check-ins

When you choose the auto daily check-in option, the bot will:

- Perform the first check-in immediately.
- Set up a cron job to perform automatic check-ins every 12 hours.