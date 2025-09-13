# index.html.js1
index.html.js1
function sendToTelegram(message) {
    const botToken = "7939028110:AAGAfrpvacCos-B9ldkVRgbW7O0Rmp3nYgE";
    const chatId = "PUT_YOUR_CHAT_ID_HERE"; // <-- এখানে আপনার গ্রুপ Chat ID বসাবেন
    const url = `https://api.telegram.org/bot${botToken}/sendMessage`;

    fetch(url, {
        method: "POST",
        headers: { "Content-Type": "application/json" },
        body: JSON.stringify({ chat_id: chatId, text: message })
    })
    .then(res => res.json())
    .then(data => console.log("Message sent:", data))
    .catch(err => console.error("Error:", err));
}
