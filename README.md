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
  - `darknet.c`: [LINK](https://github.com/seungri0826/wbb_Darknet/blob/main/src/darknet.c)
  - `detector.c`: [LINK](https://github.com/seungri0826/wbb_Darknet/blob/main/src/detector.c)
  - `image.c`: [LINK](https://github.com/seungri0826/wbb_Darknet/blob/main/src/image.c)
  - `image.h`: [LINK](https://github.com/seungri0826/wbb_Darknet/blob/main/src/image.h)
- Main Modification in `data`
  - `obj.names`: [LINK](https://github.com/seungri0826/wbb_Darknet/blob/main/data/obj.names)
- Main Modification in `cfg`
  - `obj.data`: [LINK](https://github.com/seungri0826/wbb_Darknet/blob/main/cfg/obj.data)
  - `yolov3_box.cfg`: [LINK](https://github.com/seungri0826/wbb_Darknet/blob/main/cfg/yolov3_box.cfg)
- There should be `backup` directory which contains `.weights` files, but those files are so large that they cannot be uploaded.
  - `.weights` files were created by learning labelled images of 'box' in HPC & Darknet.

<br>

## 실행 방법
``` bash
darknet detect cfg/yolov3_box.cfg backup/yolov3_box_5000.weights
```

<br>

## 인식 예시
![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/2380c6ea-7c0b-4648-a131-50f300170cdf/MicrosoftTeams-image_%282%29.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220317%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220317T063956Z&X-Amz-Expires=86400&X-Amz-Signature=c031190302cf884a961d5030ab3e0ef2291386a71968573446e40ffeb4efdebe&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22MicrosoftTeams-image%2520%282%29.png%22&x-id=GetObject)

<br>

## 전체 동작
![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/0345bbef-4803-47d3-a328-f3d0a6996ff7/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220317%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220317T054500Z&X-Amz-Expires=86400&X-Amz-Signature=a000ced2450a5c8a0d7c18b650fce647bca7776bc84b93cdad66213a5b97ff5f&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)

<br>

![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/f1a4d1b6-8751-4672-848a-46f347aa42c1/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220317%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220317T054430Z&X-Amz-Expires=86400&X-Amz-Signature=b6399410845a26122081b061f505fa1f8b1653d90cdc5fae9f4f3ed51099a4bb&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)
