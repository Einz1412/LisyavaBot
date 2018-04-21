const TelegramBot = require('node-telegram-bot-api');
const token = '428360983:AAEnz_DtveCcsryjCWc4prfPfX69b_BxhEc';
const bot = new TelegramBot(token, { polling: true });

bot.on('message', (msg) => {
    const chatId = msg.chat.id;
    bot.sendMessage(chatId, msg.text.toString());
});
