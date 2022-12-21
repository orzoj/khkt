# Hướng dẫn cơ bản về Pycord

## Các nguồn tài liệu khác
* [Docs từ chính chủ](https://docs.pycord.dev/en/stable/)
* [Discord của nhóm phát triển](https://discord.com/invite/pycord)
* Zootube tất nhiên rồi (ai lại phải đọc docs khi đã có zootube)

## Cách cài Pycord trên python
Muốn ăn thì lăn vào bếp, còn muốn code thì phải cài thư viện:)))

Theo hướng dẫn trên docs thì mình sẽ cài như sau

```
pip install -U py-cord
```

Cài Python trước hộ tôi cái (3.8 trở lên nhé, không là bị bủ bủ lmao đó)

Chạy thử cái này coi có được không, mà nhớ bỏ token của bot vô chứ không là chạy không được đâu, nếu không thì xin vĩnh biệt cụ.

```
import discord

class MyClient(discord.Client):
    async def on_ready(self):
        print(f'Logged on as {self.user}!')

    async def on_message(self, message):
        print(f'Message from {message.author}: {message.content}')

client = MyClient()
client.run(<token>)
```

Để biết chạy được hay không thì thử chat cái gì đó nếu nó phản hồi lại thì là chạy được còn không thì ...

## Cơ chế của Pycord
Ở đây mình sẽ nói theo một cách đơn giản có thể không chuẩn lắm nhưng nó có thể làm bạn có thể hiểu về cơ chế của nó.
