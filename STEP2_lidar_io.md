
## LiDAR file I/O using laspy (60 min)

laspy 패키지를 이용한 LiDAR 입출력.

### 실습 자료 다운로드

실습 자료가 위치한 폴더 경로는 되도록 영어, 대소문자만 포함하도록 합니다. (공백 X)

### lidar 가상 환경 활성화하기

윈도우

Anaconda Prompt를 실행하고 아래 커맨드를 입력합니다.
```bash
$ conda activate lidar
```

맥, 리눅스

terminal을 실행하고 아래 커맨드를 입력합니다.
```bash
$ source ~/.bashrc
$ conda activate lidar
```

### Anaconda Prompt 또는 terminal에서 실습 자료가 위치한 폴더로 이동

```bash
$ cd 폴더경로
```

### 맥 사용자의 경우 가시화를 위해 다음 작업을 수행

```bash
$ las2las -i in2018_29651885_12.laz -o in2018_29651885_12.las
$ lascopy in2018_29651885_12.las in2018_29651885_12_las13.las 3 1.3
```

### LiDAR 파일 가시화하기

[CloudCompare](https://www.danielgm.net/cc/) 를 다운로드, 설치하고 in2018_29651885_12_las13.las를 가시화한다.
