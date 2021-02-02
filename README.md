# PKlot_YOLOv5

2021-02-02
YOLOv5 와 Roboflow PKlot data를 사용해 작성

https://github.com/ultralytics/yolov5
(Transfer Learning with Frozen Layers 사용)

https://public.roboflow.com/object-detection/pklot
1. roboflow public dataset 에서 PKlot 데이터를 찾는다 (위 링크)

2. 데이터를 다운로드 (파일 or 링크 둘다 가능), roboflow model libaray 에서 yolo v5 colab ver 선택

3. colab 에서 열리면 해당 파일을 '드라이브에 사본으로 저장' (해당파일에서는 저장이 안됨)

4. 위에서 부터 아래로 코드 실행, 아래 사항들 수정할것 line 6의 주소 참고
content/yolov5/train.py 파일의 freeze 부분을 10개 레이어 freeze 시켜서 14개만 사용
(https://github.com/ultralytics/yolov5/issues/1314),

5. epoch 하기 전 링크의 result 부분 참고해서 weight 와 hyp 수정

# 주의사항 - image 크기가 너무 크면 ram 사용량을 초과해서 fail 에러가 날 수 있음. 320~416 정도면 적당


# 참고
!pwd : 현재 디렉토리를 확인
%cd : 디렉토리 변경
예시) %cd ./yolov5 : 디렉토리를 yolov5로 변경

*쓸데없이 오류 수정하겠다고 이상한거 건들지말고 기본대로 할것... 오늘 괜히 돌다가 시간많이 날림..
