# wbb_Darknet
NET 챌린지 시즌 7 왕밤빵 - Darknet 수정 코드

<br>

## 수정 사항
- Original: [AlexeyAB/darknet](https://github.com/AlexeyAB/darknet)
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

## 학습 결과
![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/efa7cc4f-91a8-430e-90ca-2bef165958de/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220317%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220317T054416Z&X-Amz-Expires=86400&X-Amz-Signature=227c589673da02a32fa07b4c1f09a6ba95d37c0abf19a5db163059a7e8e52375&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)

<br>

## 동작
![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/f1a4d1b6-8751-4672-848a-46f347aa42c1/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220317%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220317T054430Z&X-Amz-Expires=86400&X-Amz-Signature=b6399410845a26122081b061f505fa1f8b1653d90cdc5fae9f4f3ed51099a4bb&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)

<br>

![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/0345bbef-4803-47d3-a328-f3d0a6996ff7/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220317%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220317T054500Z&X-Amz-Expires=86400&X-Amz-Signature=a000ced2450a5c8a0d7c18b650fce647bca7776bc84b93cdad66213a5b97ff5f&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)
