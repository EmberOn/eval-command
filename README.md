# eval-command

eval-command is a simple project with no more than 3 files.

This project use python with discord.py for an eval bot command.

> What's an eval command ?

*It's an OWNER command to execute code directly on discord, you could just run simple instruction, or more, asynchronous instructions like create a channel in a guild, ban user, ...
We use it to test our other commands quickly,
Make sure you know what you do before using this command. It's not like using <a href="http://tio.run">Tio.run</a>, that's to use for only OWNER with precautions, with tio.run,
we can't access to context discord command, no built-in module, ...*

`[PREFIX]eval code`

![Use example image command](https://cdn.discordapp.com/attachments/711607976150171691/748192408532942848/unknown.png)
![Use example image output](https://cdn.discordapp.com/attachments/711607976150171691/748193180599713792/unknown.png)

`return` is not always useful with eval command, so if you return something, you will have a description oh the object you return : object representation, type, lenght, dir (method associated with the objet)

Eventually, a single message is sent, with the output (like print, or error), and the return object description if not null. If this message exceeds 2000 characters (discord limit), the whole message is sent to http://bin.drlazor.be/ and response sent to you.

After this message, one :boom: reaction appears, if you click on, it will be deleted for more visibility.

If you want to use this, you just need to install all the requirements in `requirements.txt` by using :
```
pip install -U -r requirements.txt
```

If not work, use `py -m pip` instead `pip`.
You have only `discord.py` and `aiohttp`, other modules are built-in python module.

In eval.py you just have to define `PREFIXES` with your prefix(es) and `TOKEN` with your bot token at the top of file