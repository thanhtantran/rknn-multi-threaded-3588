# rknn-multi-threaded-3588
RKNN Multi threades for Orange Pi5, 5B and 5 Plus

This is a copy (not forked) from this github https://github.com/leafqycc/rknn-multi-threaded

I've modified some files to use on Orange Pi 5, 5B and 5 Plus

Depend on your Python, you need to download the RKNN Toolkit Lite 2 from this https://github.com/rockchip-linux/rknn-toolkit2
Included in this github is the wheel version 1.5.2 for Python 3.9. Install it by typing command

` pip install rknn_toolkit_lite2-1.5.2-cp39-cp39-linux_aarch64.whl `

Maybe you also need to copy the file librknnrt.so to /usr/lib too, and install opencv module

` pip install opencv-python `

Check your Camera used in /dev/video0 or /dev/video1, and edit the code in main.py to the corresponance camera

` cap = cv2.VideoCapture(0) `

the run 

`python main.py`

The rkcat.sh can be running with 

` sudo bash rkcat.sh ` 

to check the NPU performance
