# screen_recorder
Now you can make your own screen recorder by just 22 lines of python code!!
I have done it by using Pycharm which is an python code editor.
Then in the terminal I have written **pip install Pillow numpy opencv-contrib-python** and **pip install win32api** and then press enter.
In the first I have imported datetime which is dafult in Pycharm.
And then I have written from PIL import Image Grab.
Then I have imported numpy as np.
Then I have imported cv2.
And thn I have written from win32api import GetSystemMetrics.
Then I have created a variable called width and entered the value as GetSystemMetrics(0).
Then I have created another varibale called height and entered the value as GetSystemMetrics(1).
Then I have created another variable called time_stamp and entered the value as datetime.datetime.now().strftime('%Y-%m-%d-%H-%M-%S').
Then I have created another varible called file_name and entered th value as f'{time_stamp}.mp4'.
Then I have created another variable called fourcc and entered the value as cv2.VideoWriter_fourcc('m', 'p', '4', 'v').
Then I have created another variable called captured_video and entered the value as cv2.VideoWriter(file_name, fourcc, 20.0, (width, height)).
Then I have written while True: and inside this I have written img = ImageGrab.grab(bbox=(0, 0, width, height)) img_np = np.array(img) img_final = cv2.cvtColor(img_np, cv2.COLOR_BGR2RGB) cv2.imshow('Kushals Screen Recorder', img_final) captured_video.write(img_final) if cv2.waitKey(10) == ord('q'): break.
And now your own screen recrder is ready and now you can enjoy it!!
