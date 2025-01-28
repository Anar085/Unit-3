# Quiz 037

## Python Code 
```.py

from kivymd.app import MDApp
from kivy.lang import Builder

class TICTOE(MDApp):
    def build(self):
        self.title = "Tic Tac Toe"
        self.current_player = "X"
        self.board = [""] * 9
        self.kv=Builder.load_file("TICTOE.kv")
        return self.kv

    def on_button_press(self, button_id):
        if self.board[button_id] == "":
            self.board[button_id] = self.current_player
            self.update_button(button_id)
            if self.check_winner():
                self.display_winner()
                return
            self.current_player = "O" if self.current_player == "X" else "X"
            self.kv.ids.label2.text = f"Player's turn: {self.current_player}"

    def update_button(self, button_id):
        button=self.kv.ids[f'box{button_id + 1}']
        button.text=self.board[button_id]
        button.disabled=True

    def check_winner(self):
        win_combs=[
            [0, 1, 2], [3, 4, 5], [6, 7, 8], 
            [0, 3, 6], [1, 4, 7], [2, 5, 8],  
            [0, 4, 8], [2, 4, 6]               
        ]
        for c in win_combs:
            if self.board[c[0]] == self.board[c[1]] == self.board[c[2]] != "":
                return True
        return False

    def display_winner(self):
        winner = self.current_player
        self.kv.ids.label2.text = f"Player {winner} wins!"
        for i in range(9):
            self.kv.ids[f'box{i + 1}'].disabled = True

t=TICTOE()
t.run()


```

## KivyMD Code 

```.kv

MDScreen:
    size: 500,500
    id: screen
    md_bg_color: "#FFFFFF"

    MDLabel:
        id: label1
        text: "Tic Tac Toe by Anar"
        font_size: "18pt"
        pos_hint: {"center_y": 0.9}
        halign: "center"

    MDLabel:
        id: label2
        text: "Player's turn: X"
        font_size: "15pt"
        text_color: "#000000"
        pos_hint: {"center_y": 0.85}
        halign: "center"

    MDBoxLayout:
        id: main_base
        orientation: "vertical"
        md_bg_color: "#000000"
        size_hint: 0.6, 0.5
        pos_hint: {"center_x": 0.5, "center_y": 0.5}

        MDBoxLayout:
            orientation: "horizontal"
            md_bg_color: "#000000"
            spacing: 10
            padding: 5
            MDRaisedButton:
                id: box1
                md_bg_color: "#FF0150"
                size_hint: 0.2, 0.8
                on_release: app.on_button_press(0)
            MDRaisedButton:
                id: box2
                md_bg_color: "#FF0150"
                size_hint: 0.2, 0.8
                on_release: app.on_button_press(1)
            MDRaisedButton:
                id: box3
                md_bg_color: "#FF0150"
                size_hint: 0.2, 0.8
                on_release: app.on_button_press(2)

        MDBoxLayout:
            orientation: "horizontal"
            md_bg_color: "#000000"
            spacing: 10
            padding: 5
            MDRaisedButton:
                id: box4
                md_bg_color: "#FF0150"
                size_hint: 0.2, 0.8
                on_release: app.on_button_press(3)
            MDRaisedButton:
                id: box5
                md_bg_color: "#FF0150"
                size_hint: 0.2, 0.8
                on_release: app.on_button_press(4)
            MDRaisedButton:
                id: box6
                md_bg_color: "#FF0150"
                size_hint: 0.2, 0.8
                on_release: app.on_button_press(5)

        MDBoxLayout:
            orientation: "horizontal"
            md_bg_color: "#000000"
            spacing: 10
            padding: 5
            MDRaisedButton:
                id: box7
                md_bg_color: "#FF0150"
                size_hint: 0.2, 0.8
                on_release: app.on_button_press(6)
            MDRaisedButton:
                id: box8
                md_bg_color: "#FF0150"
                size_hint: 0.2, 0.8
                on_release: app.on_button_press(7)
            MDRaisedButton:
                id: box9
                md_bg_color: "#FF0150"
                size_hint: 0.2, 0.8
                on_release: app.on_button_press(8)


```

## Proof of work




![video](https://github.com/user-attachments/assets/d178fe6d-261d-4787-b355-d50ed7620785)

