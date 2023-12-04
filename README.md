# rknn-multi-threaded-3588
RKNN Multi threades for Orange Pi 5, 5B and 5 Plus

This is a copy (not forked) from this github https://github.com/leafqycc/rknn-multi-threaded

I've modified some files to use it on Orange Pi 5, 5B and 5 Plus

Depend on your Python version, you need to download the RKNN Toolkit Lite 2 from this https://github.com/rockchip-linux/rknn-toolkit2
Included in this github is the wheel version 1.5.2 for Python 3.9. Install it by typing command

` pip install rknn_toolkit_lite2-1.5.2-cp39-cp39-linux_aarch64.whl `

Maybe you also need to copy the file ` librknnrt.so ` to /usr/lib too, and install opencv module

` pip install opencv-python `

Check your Camera used in /dev/video0 or /dev/video1, and edit the code in main.py to the corresponance camera

` cap = cv2.VideoCapture(0) `

then run 

`python main.py`

If you want to increase image size, edit this line in func.py

`OBJ_THRESH, NMS_THRESH, IMG_SIZE = 0.25, 0.45, 640`

or number of frame, edit this on main.py

`TPEs = 3`

The rkcat.sh can be running with 

` sudo bash rkcat.sh ` 

to check the NPU performance

Here is demo i run on Orange Pi 5 PLus with HDMI In


![orangepi5plus](https://github.com/thanhtantran/rknn-multi-threaded-3588/assets/5319910/692c44dd-980c-4435-b67e-692586439bea)

## Acknowledgements
- https://github.com/ultralytics/yolov5
- https://github.com/rockchip-linux/rknn-toolkit2
- https://github.com/airockchip/rknn_model_zoo
- https://github.com/leafqycc/rknn-multi-threaded
