# Quiz 038

## Python Code 
```.py
from kivymd.app import MDApp
from kivymd.uix.screen import MDScreen

class MysteryPageA(MDScreen):
    def next(self):
        self.parent.current = "MysteryPageB"
    def message1(self):
        print("This is the mystery page A you pressed the button")



class MysteryPageB(MDScreen):
    def back(self):
        self.parent.current = "MysteryPageA"

    def message2(self):
        print("This is the mystery page B you pressed the button")


class quiz37(MDApp):
    def build(self):
        return

t=quiz37()
t.run()


```

## KivyMD Code 

```.kv

ScreenManager:
    id:scr_manager

    MysteryPageA:
        name: "MysteryPageA"
    MysteryPageB:
        name: "MysteryPageB"

<MysteryPageA>:
    MDCard:

        size_hint: .5,.8
        pos_hint:{"center_x":.5,"center_y":.5}
        orientation:"vertical"
        md_bg_color:"FFA500"
        MDLabel:
            text: "Mystery Page A"
            font_style: 'H5'

            halign:"center"
            size_hint:1,.3
            color:'#FFFFFF'

        MDBoxLayout:
            orientation:"horizontal"
            spacing: "200dp"


            MDRaisedButton:
                text:'Print the message'
                pos_hint:{'center_x':.2}
                md_bg_color:"#e63946"
                on_press: root.message1()

            MDRaisedButton:
                text:'Next'
                pos_hint:{'center_x':.8}
                md_bg_color:"#e63946"
                on_press:root.next()







<MysteryPageB>:

    MDCard:
        size_hint: .5,.8
        pos_hint:{"center_x":.5,"center_y":.5}
        orientation:"vertical"
        md_bg_color:"FFA500"
        MDLabel:
            text: "Mystery Page B"
            font_style: 'H5'

            halign:"center"
            size_hint:1,.3
            color:'#FFFFFF'

        MDBoxLayout:
            orientation:"horizontal"
            spacing: "200dp"


            MDRaisedButton:
                text:'Print the message'
                pos_hint:{'center_x':.2}
                md_bg_color:"#e63946"
                on_press: root.message2()

            MDRaisedButton:
                text:'Back'
                pos_hint:{'center_x':.8}
                md_bg_color:"#e63946"
                on_press:root.back()


```

## Proof of work

![image](https://github.com/user-attachments/assets/85bf8a40-9200-4656-bd23-dcb11adfb748)

