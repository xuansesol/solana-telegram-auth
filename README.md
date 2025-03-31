# Solana Telegram Auth WebApp

This is a lightweight HTML/JS WebApp designed to allow users to authenticate via a Solana wallet (Phantom, Backpack, etc.) directly inside a Telegram WebApp.

## Features

- Generates a random challenge message
- Signs it using the user's connected wallet
- Sends the result back to a Telegram bot via `WebApp.sendData()`

## Usage

1. Deploy this `auth.html` to Vercel, Netlify, or Fly.io (static hosting)
2. In your Telegram bot, send a button with:

```python
InlineKeyboardButton("Sign with Wallet", web_app={"url": "https://yourdomain.com/auth.html"})
```

3. Handle the returned `web_app_data` in your bot to verify the signature

## License

MIT