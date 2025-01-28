# Quiz 036


## Python Code 
```.py


from kivymd.app import MDApp


class colorchange(MDApp):


    def build(self):
        return

    def change_mode(self):
        print(self.root.ids.main.md_bg_color)
        if self.root.ids.main.md_bg_color == [1.0, 1.0, 1.0, 1.0]:
            self.root.ids.main.md_bg_color = "#000000"
            self.root.ids.theme_mode.text_color = 1, 1, 1, 1
            self.root.ids.my_name.text_color = 1, 1, 1, 1
            self.root.ids.theme_mode.text = "LIGHT"
            self.root.ids.theme_mode.md_bg_color = "#B7B78A"
        else:
            self.root.ids.main.md_bg_color = "#FFFFFF"
            self.root.ids.theme_mode.text_color = 0, 0, 0, 1
            self.root.ids.my_name.text_color = 0, 0, 0, 1
            self.root.ids.theme_mode.text = "DARK"
            self.root.ids.theme_mode.md_bg_color = "#658864"


test = colorchange()
test.run()

```

## KivyMD Code 

```.kv
Screen:
    size:500,500
    MDBoxLayout:
        id: main
        orientation:"vertical"
        md_bg_color: "#FFFFFF"
        MDLabel:
            id:my_name
            text: "Anar"
            halign: "center"
            theme_text_color: "Custom"
            text_color: 0, 0, 0, 1
            pos_hint: {"center_x": .5, "center_y": .5}
        MDRaisedButton:
            id: theme_mode
            text: "Dark Mode"
            md_bg_color: "B7B78A"
            pos_hint: {"center_x": 0.05, "center_y": 0.1}
            on_release: app.change_mode()


```

## Proof of work

1.![image](https://github.com/user-attachments/assets/dc64d2b7-a16c-422d-94bf-7e701d366ebf)
2. ![image](https://github.com/user-attachments/assets/ee168cd1-4990-4a52-bf02-d3e69cf4d766)


