
## LiDAR file I/O using laspy (60 min)

laspy 패키지를 이용한 LiDAR 입출력.

### 실습 자료 다운로드

git clone 명령을 이용하여 GitHub repository를 다운로드합니다. Command line interface에서 cd를 이용하여 저장할 장소로 이동한 뒤 아래 명령을 입력하여 다운로드합니다. 다운받을 폴더 경로상에 한글 또는 공백이 있으면 원활한 진행이 어려울 수 있으므로 필요한 경우 새로운 폴더를 생성합니다(mkdir).

```bash
$ git clone https://github.com/gdslab/tutorial_lidar_processing_with_python.git
```
### lidar 가상 환경 활성화하기

Anaconda Prompt를 실행하고 아래 커맨드를 입력합니다.

윈도우
```bash
$ conda activate lidar
```

맥, 리눅스

terminal을 실행하고 아래 커맨드를 입력합니다.
```bash
$ source ~/.bashrc
$ conda activate lidar
```

### .laz 파일(압축된 형태)을 .las 파일로 변환하고 LAS 버전을 1.3으로 변경

.laz 파일을 .las 파일로 변경하면 다음 과정인 raster 생성 과정을 Jupyter를 이용하여 편리하게 진행할 수 있습니다. 맥 사용자의 경우 LAS 버전을 1.3으로 변경하여야 가시화가 가능합니다.

```bash
$ las2las -i in2018_29651885_12.laz -o in2018_29651885_12.las
$ lascopy in2018_29651885_12.las in2018_29651885_12_las13.las 3 1.3
```

### LiDAR 파일 가시화하기

[CloudCompare](https://www.danielgm.net/cc/) 를 다운로드, 설치하고 in2018_29651885_12_las13.las를 가시화합니다.
