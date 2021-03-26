# YOLOv5-Object-detection-Counting

!python train.py --data custom_dataset/custom_data.yaml --cfg models/yolov5s.yaml --weights '' --epochs 10

python train.py --data custom_dataset/custom_data.yaml --cfg yolov5s.yaml --weights runs/train/exp4/weights/best.pt --epochs 500 

python detect.py --source custom_dataset/test/images --weights runs/train/exp4/weights/best.pt --conf 0.6


--img <> : ขนาดของ Image ขาเข้า(มีการปรับ Resolution ของ Image)
--batch <> : จำนวน Batch size
--epochs <> : จำนวน Epochs
--data <> : Path ที่ชี้ไปยังไฟล์ Data config
--cfg <> : Path ที่ชี้ไปยังไฟล์โครงสร้างโมเดลที่เลือกใช้
--weights <> : Path ที่ชี้ไปยังไฟล์ Pretrained model สำหรับทำ Transfer learning
--cache-images : กำหนดให้เก็บ Cache image ด้วยเพื่อเร่งความเร็วในการเทรนโมเดล