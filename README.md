import pyautogui
import time

# 设置保护措施：将鼠标移动到屏幕四个角之一即可停止脚本
pyautogui.FAILSAFE = True

print("程序将在 5 秒后开始，请将鼠标移至目标位置...")
time.sleep(5)

try:
    while True:
        # 执行点击
        pyautogui.click()
        
        # 设置点击间隔（例如每 0.5 秒点击一次）
        time.sleep(0.5) 
        
        print("点击中... 按下 Ctrl+C 或将鼠标甩至屏幕角以退出")
except KeyboardInterrupt:
    print("\n程序已停止")
