## Installing Conda/Anaconda and configuring Virtual Environments (50 min)

Anaconda3 2020.07 버전을 설치하기.


### Anaconda 다운로드

다음 [링크](https://repo.anaconda.com/archive/)에 접속해서 시스템 환경에 맞는 아나콘다를 다운로드하고 설치합니다.

이미 시스템에 아나콘다가 설치되어있다면 다운로드 및 설치를 생략합니다.

### [Command line interface](https://docs.anaconda.com/anaconda/user-guide/getting-started/#open-anaconda-prompt) 실행

윈도우: Anaconda Prompt(Anaconda 3)를 실행합니다.

맥 또는 리눅스: terminal을 실행합니다.

### 아나콘다 가상환경(conda environment) 생성하기

기존의 가상 환경이 있는지 체크합니다. 아래 명령어를 실행했을 때 * 심볼이 base 환경 옆에 표시되는지 확인합니다..

```bash
$ conda info --envs
```

아래의 커맨드로 라이다 처리 작업을 수행할 새로운 Anaconda 가상 환경을 생성합니다. 실습 진행의 편의를 위해서 Python=3.6버전으로 진행하겠습니다.

```bash
$ conda create --name lidar python=3.6
```

위에서 생성한 **lidar** 가상 환경을 활성화합니다.

윈도우
```bash
$ conda activate lidar
```
맥 또는 리눅스
```bash
$ source ~/.bashrc
$ conda activate lidar
```

새로운 가상환경이 로드되었는지 확인합니다. 아래 커맨드를 실행했을 때 lidar옆에 * 심볼이 표시되는지 확인합니다.

```bash
$ conda info --envs
```
lidar 가상 환경이 로드되었으면 아래 패키지를 설치합니다.

```bash
$ conda install -c anaconda jupyter
$ conda install -c conda-forge gdal
$ conda install numpy matplotlib
$ conda install -c conda-forge laspy progressbar 
```

이제 패키지 설치가 완료되었습니다. Python을 실행해서 패키지가 잘 설치되었는지 확인합니다.

```bash
$ conda activate lidar
$ python
```

```python
>>> import numpy
>>> import matplotlib
>>> import gdal
>>> import laspy
```

Command line interface를 종료합니다.

Jupyter Notebook이 잘 실행되는지 확인합니다.

```bash
$ jupyter notebook
```

Jupyter Notebook이 잘 실행되었으면 다음 튜토리얼을 진행합니다.
