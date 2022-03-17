# wbb_Darknet
NET 챌린지 시즌 7 왕밤빵 - Darknet 수정 코드

<br>

## 설명
- 실시간 물체 인식을 위해 YOLOv3를 이용하여 택배 상자 이미지를 학습하였다.
- Darknet의 소스코드를 수정하여 인식된 택배 상자의 개수가 추출되게 하였고, 연속적인 물체 인식이 한 번의 weight upload만으로 가능하도록 하였다.

<br>

## 수정 사항
> Original: [AlexeyAB/darknet](https://github.com/AlexeyAB/darknet)
- Main Modification in `src` 
  - `darknet.c`: [LINK](https://github.com/seungriyou/wbb_Darknet/blob/main/src/darknet.c)
  - `detector.c`: [LINK](https://github.com/seungriyou/wbb_Darknet/blob/main/src/detector.c)
  - `image.c`: [LINK](https://github.com/seungriyou/wbb_Darknet/blob/main/src/image.c)
  - `image.h`: [LINK](https://github.com/seungriyou/wbb_Darknet/blob/main/src/image.h)
- Main Modification in `data`
  - `obj.names`: [LINK](https://github.com/seungriyou/wbb_Darknet/blob/main/data/obj.names)
- Main Modification in `cfg`
  - `obj.data`: [LINK](https://github.com/seungriyou/wbb_Darknet/blob/main/cfg/obj.data)
  - `yolov3_box.cfg`: [LINK](https://github.com/seungriyou/wbb_Darknet/blob/main/cfg/yolov3_box.cfg)
- There should be `backup` directory which contains `.weights` files, but those files are so large that they cannot be uploaded.
  - `.weights` files were created by learning labelled images of 'box' in HPC & Darknet.

<br>

## 실행 방법
``` bash
darknet detect cfg/yolov3_box.cfg backup/yolov3_box_5000.weights
```

<br>

## 인식 예시
![](https://user-images.githubusercontent.com/43572543/158790511-bfa19205-e9d4-4469-afe9-8b6fcea5fb40.png)

<br>

## 전체 동작
![](https://user-images.githubusercontent.com/43572543/158790536-bb0c6aeb-5ff8-4235-b033-f5deb46d7f2d.png)

<br>

![](https://user-images.githubusercontent.com/43572543/158790555-dca20c52-784a-4f3b-978f-0bd7ef7676e2.png)
