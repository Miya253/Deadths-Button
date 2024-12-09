import tkinter as tk
from tkinter import messagebox
import time

# 初始化主窗口
root = tk.Tk()
root.title("System Shutdown")
root.geometry("400x300")
root.configure(bg="black")

# 设置全屏模式
root.attributes("-fullscreen", True)

# 创建标签显示倒计时
countdown_label = tk.Label(root, text="", font=("Helvetica", 48, "bold"), fg="red", bg="black")
countdown_label.pack(expand=True)

# 模拟关机的倒计时
def fake_shutdown():
    for i in range(10, -1, -1):  # 从10开始倒计时到0
        countdown_label.config(text=f"Shutting down in {i} seconds...")
        root.update()
        time.sleep(1)

    # 假装关机完成后显示一个消息
    messagebox.showinfo("Shutdown", "System shutdown completed.")
    root.destroy()  # 关闭窗口

# 模拟一个假的蓝屏背景（可选）
def blue_screen_of_death():
    root.configure(bg="blue")
    countdown_label.config(fg="white", text="A critical error has occurred.")
    root.update()
    time.sleep(3)
    fake_shutdown()

# 开始假关机
blue_screen_of_death()
root.mainloop()
