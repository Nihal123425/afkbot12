const mineflayer = require('mineflayer');

// Configuration
const config = {
    host: 'Nihal1234123.aternos.me', // Replace with your Minecraft server IP
    port: 19303, // Default Minecraft Java port
    username: 'AFK_Bot', // Change to your bot's username
    version: false // Auto-detects the version
};

// Function to create bot
function createBot() {
    const bot = mineflayer.createBot(config);

    bot.on('login', () => {
        console.log('Bot has logged in!');
    });

    bot.on('end', (reason) => {
        console.log(`Bot disconnected: ${reason}`);
        setTimeout(createBot, 5000); // Reconnect after 5 seconds
    });

    bot.on('kicked', (reason) => {
        console.log(`Bot was kicked: ${reason}`);
    });

    bot.on('error', (err) => {
        console.log(`Error: ${err}`);
    });
}

// Start the bot
createBot();
