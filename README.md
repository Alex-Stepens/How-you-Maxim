```py
# импортируем нужные библиотеки
from aiogram import Dispatcher, types, Bot
from aiogram.utils import executor

# твой токен который ты получишь после создания бота у @BotFather
TOKEN = '5786131616:AAE-XrDtk-52DQBAIau6KwTY3V34j4qu12Y'

# объекты бота
bot = Bot(TOKEN)
dp = Dispatcher(bot)

# функция которая будет слать сообщение в твою группу
@dp.message_handler(commands = ['maxim'])
async def main(message: types.Message):
    # строка, чтобы отправить что-нибудь в группу
    import random
    p=random.randint(0,100)
    Max=random.choice([f"🤡 Я Максим на {p}%",f"😈Я дед Максим на {p}%"])
    if message.from_user.id == 5323995074 :#
    	await message.reply(f'😈 Я Максим на 101% ')
    	return
   
    
    else:
    	await message.reply(f'{Max}')
    	return

@dp.message_handler(commands = ['Dania'])
async def mai(message: types.Message):
    # строка, чтобы отправить что-нибудь в группу
    import random
    p=random.randint(0,100)
    Max=random.choice([f"🤡 Я Даня на {p}%"])
    if message.from_user.id == 1456044714 :
    	await message.reply(f'😈 Я Даня на 0% ')
    	return
    else:
    	await message.reply(f'{Max}%')    
    	
    		    	    
@dp.message_handler(commands = ['Vika'])
async def ma(message: types.Message):
    # строка, чтобы отправить что-нибудь в группу
    import random
    p=random.randint(0,100)
    Max=random.choice([f"🤡 Я Вика на {p}%"])
   
    await message.reply(f'{Max}') 
    
@dp.message_handler(commands = ['Vera'])
async def m(message: types.Message):
    # строка, чтобы отправить что-нибудь в группу
    import random
    p=random.randint(0,100)
    Max=random.choice([f"🤡 Я Вероника на {p}%"])
   
    await message.reply(f'{Max}')           
@dp.message_handler(commands = ['masha'])
async def d(message: types.Message):
    # строка, чтобы отправить что-нибудь в группу
    import random
    p=random.randint(0,100)
    Max=random.choice([f"🤡 Я Маша на {p}%"])
   
    await message.reply(f'{Max}')                  

@dp.message_handler(commands="inline_url")
async def cmd_inline_url(message: types.Message):
    buttons = [
        types.InlineKeyboardButton(text="TikTok", url="https://www.tiktok.com/@darmen_3?_t=8V86h2u1KmT&_r=1"),
        types.InlineKeyboardButton(text="Инста", url="https://instagram.com/darmen_proxy?igshid=YmMyMTA2M2Y="),
        types.InlineKeyboardButton(text="Twitch", url="https://www.twitch.tv/father_darmen3?sr=a"),
        types.InlineKeyboardButton(text="Оф. канал Telegram", url="https://t.me/+ZNzxmC1FV51iYWRk")
        
        
    ]
    keyboard = types.InlineKeyboardMarkup()
    keyboard.add(*buttons)
    await message.answer("Соц сети 🏴‍☠️", reply_markup=keyboard)

          
                              
# запускаем бота
executor.start_polling(dp)
```
