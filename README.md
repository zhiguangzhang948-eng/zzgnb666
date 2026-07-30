def login():
    print("**************\n1.添加学员\n2.删除学员\n3.修改学员信息\n4.查询学员信息\n5.显示所有学员信息\n6.退出系统\n")
def add():
    new_name = input("请输入新建姓名：")
    new_id = int(input("请输入新建id："))
    for i in info:
        if new_name == i["name"]:
            print("用户已存在！")
            return
    info_dict = {}
    info_dict["name"] = new_name
    info_dict["id"]  =  new_id
    info.append(info_dict)
    print("创建成功")
def del_():
    del0 = input("删除人姓名:")
    for i in info:
        info.remove(i:del0)
    print(f'{del0} 删除成功')
def modify():
    pass
def select():
    for i in info:
        print(f'name:{i["name"]}  id:{i["id"]}\n')
info = []
while True:
    login()
    print("请输入功能序号：")
    c = int(input())
    if c==1:
        print("添加\n")
        add()
    elif c==2:
        print("删除\n")
        del_()    
    elif c==3:
        print("修改\n")
    elif c==4:
        print("查询\n")
        select()
    elif c==5:
        print("显示\n")
    elif c==6:
        print("退出\n")
        break
    else:
        print("输入有误\n")
