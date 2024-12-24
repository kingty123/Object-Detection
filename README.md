# Object-Detection
목표 : 주간, 야간에 자율주행 차량의 객체 인식을 통한 장애물 회피 및 주행 원활화를 통한 차량 전방 모니터링 시스템 구축


## 1. 사용한 데이터 : aihub의 '상용 자율주행차 야간 자동차 전용도로 데이터.zip'의 차량 전방사진(160장)과 직접 수집한 데이터 12장으로, 총 172장의 데이터를 활용했다.
### 1) 데이터셋 구분
- train : 70%, 120장 -> 직접 수집한 12장의 데이터 포함
- val : 15%, 26장
- test : 15%, 26장


## 2. 과정
1) '상용 자율주행차 야간 자동차 전용도로.zip' 압축 해제
2) class와 Segmentation 확인
3) Segmentation ☞ bbox ☞ txt(YOLOv8)

4) 직접 수집한 영상을 500여장의 사진으로 분할
5) roboflow에서 annotation 수행
6) zip으로 다운로드

7) '상용 자율주행차 야간 자동차 전용도로.zip'파일과 '서강대교_저녁.zip' 파일을 'object_detection_on_road.v1i.yolov8.zip' 통합
8) yaml 파일 생성
9) YOLOv8로 학습
