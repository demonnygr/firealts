# firealts
import discord
from discord.ext.commands import Bot
from discord.ext import commands
import asyncio
import time
import random
from discord import Game


Client = discord.client
client = commands.Bot(command_prefix = '!')
Clientdiscord = discord.Client()


@client.event
async def on_ready():
    await client.change_presence(game=Game(name='FireAltsMC'))
    print('Ready, Freddy') 


@client.event
async def on_message(message):
    if message.content == '$shop':
        await client.send_message(message.channel,'**Shop:** https://selly.gg/@FireAltsMC')
    if message.content == '$commands':
        await client.send_message(message.channel,'Help Commands: $shop')
client.run('NDgyOTAxMjg1MDQ2MzIxMTg1.DovGgQ.UklCHztowRdbb1z9ks5CDqtNFcE')
