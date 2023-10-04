import discord, random, os
from discord.ext import commands
from botlogic import gen_pass
from botlogic import coins

intents = discord.Intents.default()
intents.message_content = True

bot = commands.Bot(command_prefix='/', intents=intents)

@bot.event
async def on_ready():
    print(f'We have logged in as {bot.user}')

@bot.command()
async def hello(ctx):
    await ctx.send(f'Hi! I am a bot {bot.user}!')

@bot.command()
async def heh(ctx, count_heh = 5):
    await ctx.send("he" * count_heh)

@bot.command()
async def flipkoin(ctx, detik = 1):
    await ctx.send(coins(detik))

@bot.command()
async def createpass(ctx, ):
    await ctx.send(gen_pass(8))

@bot.command()
async def meme(ctx):
    img_name = random.choice(os.listdir('images'))
    with open(f'images/{img_name}', 'rb') as f:
        picture = discord.File(f)
    await ctx.send(file=picture)

@bot.command()
async def ide_sampah(ctx):
    krj_name = random.choice(os.listdir('kerajinan'))
    with open(f'kerajinan/{krj_name}', 'rb') as f:
        picture = discord.File(f)
        f.close()
    await ctx.send(file=picture)

bot.run("MTE1MTUwMDI3MDc4MjY2NDcwNA.GD6iE_.22U3l39f7K4hsoIVvuQj-1qDbblF96XNU8rtf4")
