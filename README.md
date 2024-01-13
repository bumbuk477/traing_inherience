# traing_inherience
class Widget():
    def __init__(self,x,y,text):
        self.text = text
        self.x = x
        self.y = y
    def print_info(self):
        print(f"напис: {self.text}")
        print(f"Розташування:{self.x} {self.y}")
class Button(Widget):
    def __init__(self,text,x,y):
        super().__init__(text,x,y)
        self.is_clicked = False
    def click(self):
        self.is_clicked = True
        print("Ви зареєстровані")
q = Button("Брати участь",100,100)
q.print_info()
qwestion = input("Хочете зареєструватися? (так / ні):").lower()
if qwestion == "так":
    q.click()
else:
    print("А шкода!")
