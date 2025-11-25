# auto-responder-bot
from pyrogram import Client, filters
from pyrogram.types import Message

api_id = 28880179
api_hash = "6194886a7eab72abd9ce4dda80d91e5d"

app = Client("auto_responder_bot", api_id=api_id, api_hash=api_hash)

@app.on_message(filters.private & ~filters.me)
async def auto_reply(client: Client, message: Message):
    await message.reply_text(
        "📨 Salom! Hozirda men onlayn emasman.\n\n"
        "🛠 Agar sizda savol, buyurtma yoki hamkorlik bo‘yicha murojaat bo‘lsa, iltimos @om1rbayev ga yozing.\n\n"
        "✅ Tez orada aloqaga chiqaman. Tashrifingiz uchun rahmat!"
    )

app.run()
