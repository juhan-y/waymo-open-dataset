kitti 데이터셋: kitti dataset은 자율주행 플랫폼을 위한 vision task를 포함하고 있다.
2D, 3D, Lidar와 같은 여러 버전의 dataset이 존재한다. dataset의 구성은 training 파일에서 image파일은 7481개를 갖고 있으며, label 파일이 txt파일도 그에 맞는 7481개를 가진다.
testing을 위한 dataset은 image파일이 7518개 있다. testing 파일은 labelling되어 있지않아
라벨 파일인 txt파일이 존재하지 않는다. 사용자가 원할 시에 직접 labelling을 통해 txt파일을 생성시켜줘야 한다. 추가적으로 설명하면 kitti dataset의 수집 위치는 독일이며, 그 이유로 인해 한국과는 다른 환경에서 데이터가 수집되었으므로 데이터셋이 일반성을 가지지 못해 한국과 같은 다른 나라에서는 독일에서는 인지했던 표지판이나 버스, 화물차 등을 인지하지 못할 수도 있다는 단점이 있다.
labelling을 통한 라벨이 저장된 txt파일 안에는 객체를 인지하는 바운딩 박스의 왼쪽 위 지점과 오른쪽 아래 지점의 좌표를 가지고 있다.
kitti dataset의 여러 버전들을 이용해서 여러 가지의 형태로 image를 변환하는 튜토리얼을 다른 사람의 git에서 가져왔다.
내용은 ladar로 수집된 data를 파노마라형식의 image로, top-view로, 투영된 사진으로 변환시키는 튜토리얼이 있으며, 3D상의 image에서 객체를 추적하는 튜토리얼도 있다.
모두 파이썬파일로 코드가 구현되어있다.
![image](https://user-images.githubusercontent.com/81463668/113805143-f2407380-979a-11eb-90d1-7a700e550141.png)

<kitti dataset중 3D>
![image](https://user-images.githubusercontent.com/81463668/113805150-f53b6400-979a-11eb-8738-36fe7d806348.png)

<kitti dataset중 2D>
Faster R-CNN, YOLOv3, YOLOv2 알고리즘을 적용하고 객체가 차량, 보행자, 여러 가지혼합된 경우일때의 image이다.
