# What is liblinear?

A Library for Large Linear Classification

> [liblinear](https://www.csie.ntu.edu.tw/~cjlin/liblinear/)

## Installation / Usage

1. Install the `marusan10/liblinear` container:

    ``` sh
    $ docker pull marusan10/liblinear
    ```

2. Run 

    train

    ``` sh
    $ docker run --rm -v $(pwd):/data marusan10/liblinear train test01.data test01.model
    ```

    predict

    ``` sh
    $ docker run --rm -v $(pwd):/data marusan10/liblinear predict test01.data test01.model test01.predict
    ```

