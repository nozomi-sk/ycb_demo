# YCB objects demo weights for Yolov4 & Yolov5

## Yolov4

1. Compile darknet.

2. Copy `yolov4/ycb` and `test1.mp4`to the folder of darknet.

   ![image-20210227202736516](https://i.loli.net/2021/02/28/eWtJM3p9sjAf27C.png)

3. Go to the folder of darknet, run `./darknet detector demo ycb/obj.data ycb/yolo-test.cfg ycb/weights/yolo-obj_7000.weights -thresh 0.5 -ext_output test1.mp4` . 

4. For a headless server, you will meet an error (something looks like Gtk-WARNING cannot open display) if you execute line 3. Just try `./darknet detector demo ycb/obj.data ycb/yolo-test.cfg ycb/weights/yolo-obj_7000.weights -thresh 0.5 test1.mp4 -dont_show -ext_output -out_filename res.avi`



## Yolov5

1. Install yolov5 (assume you yolov5 project is located at `<yolov5_root>`)

2. Execute `mkdir -p <yolov5_root>/runs/train `

3. Copy `yolov5/exp2` to `<yolov5_root>/runs/train`

   ![image-20210227202532270](https://i.loli.net/2021/02/28/ioXfnA5jVdR2F8h.png)

4. Copy `test1.mp4` to `<yolov5_root>`

4. Run `python detect.py --source test1.mp4 --weights runs/train/exp2/weights/best.pt --conf-thres 0.25 --view-img`

## Test Videos

The videos `test1.mp4` and `test2.mp4` are collected from internet, **I don’t own the rights to them**.

