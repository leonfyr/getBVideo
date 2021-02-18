#导入
from webbrowser import open
import tkinter as tk
from tkinter.filedialog import askdirectory
from tkinter import messagebox

#定义一个没有啥用的错误
class HappyError(Exception):
    def __init__(self,error):
        self.error = error
    def __str__(self,*args,**kwargs):
        return self.error
#获取视频函数
def getVideo(where,url):
    from os import system
    command = "you-get -o "+where+" "+url
    system(command)

#获取保存文件夹函数
def wow():
    d = askdirectory()
    e2.delete(0,tk.END)
    e2.insert(tk.END,d)

#提交函数
def submit():
    try:
        a = str(e1.get())
        if e1[:2] != "av":
            raise HappyError("错误:av号开头两个字母必须是小写的\"av\"")
    except:
        getVideo(e2.get(),"https://www.bilibili.com/video/"+e1.get())
        root.destroy()

#主循环
while True:
    root = tk.Tk()
    root.title("下载视频程序v0.1")
    root.geometry("350x100")
    root.resizable(False,False)
    b1 = tk.Label(root,text="请输入av号:")
    b1.grid(row=1,column=0)
    e1 = tk.Entry(root)
    e1.grid(row=1,column=1)
    e1.insert(tk.END,"av")
    b2 = tk.Label(root,text="请选择保存文件夹")
    b2.grid(row=2,column=0)
    e2 = tk.Entry(root)
    e2.grid(row=2,column=1)
    Button = tk.Button(root,text="选择文件夹",command=wow)
    Button.grid(row=2,column=2)
    Button = tk.Button(root,text="提交",command=submit)
    Button.grid(row=3,column=1)
    root.mainloop()
    break
