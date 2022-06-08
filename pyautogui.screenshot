import cv2
import numpy as np
import pyautogui

SCREEN_SIZE = (1920, 1080)

fourcc = cv2.VideoWriter_fourcc(*"XVID")

out = cv2.VideoWriter("output.avi", fourcc, 20.0, (SCREEN_SIZE))

while True:
    # сделать скриншот
    img = pyautogui.screenshot(region=(0, 0, 300, 400))
    # преобразовываем эти пиксели в правильный массив numpy для работы с OpenCV
    frame = np.array(img)
    # конвертировать цвета из BGR в RGB
    frame = cv2.cvtColor(frame, cv2.COLOR_BGR2RGB)
    # пишем фрейм
    out.write(frame)
    # показать рамку
    cv2.imshow("screenshot", frame)
    # если пользователь нажимает q, он выходит
    if cv2.waitKey(1) == ord("q"):
        break
# убедитесь, что все закрыто при выходе
cv2.destroyAllWindows()
out.release()

cv2.destroyAllWindows()
out.realeas()
