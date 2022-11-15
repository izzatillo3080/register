


class Registiation_form:
    royxat = {"Ali|vali":"1234"}
    def __init__(self) -> None:
        pass
    def chek_pwd(self, p1, p2):
        if p1 == p2:
            return True
        else:
            return False
    def register(self, name, surname, pwd, pwd_agein):
        self.name = name
        self.surname = surname
        self.pwd = pwd
        self.pwd_agein = pwd_agein
        self.tekshiruv = Registiation_form.chek_pwd(self.pwd, self.pwd_agein)
        self.full = f'{self.name}|{self.surname}'
        if self.tekshiruv and self.full not in list((Registiation_form).keys()):
            Registiation_form.royxat[self.full] == self.pwd
            print("Siz royxatdan muvoffiqiyatli o'tting'iz")
        elif self.tekshiruv == False:
            print("Kiritilgan parol bir biriga mos kelmadi")
        elif self.full in list((Registiation_form).keys()):
            print("Siz oldin po'yxatdan o'tg'ansiz")
        else:
            print("Kutilmagan xatolik yuz berda")
            
royx = Registiation_form()
royx.register("ali", "Aliyev", "parol123", "parol123")
print("Xatolik berdi")

royx2 = Registiation_form()
royx2.register("ali", "Aliyev", "parol123", "parol123")
print("Xoyxatdan otgansiz")

royx1 = Registiation_form()
royx1.register("ali", "Aliyev", "parol123", "parol123")
print("parol xatoligi")
