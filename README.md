## MNIST_classification

### mnist 이미지 분류 task

---

### 파일 설명

- `dataset.py`: MNIST dataset load & data preprocessing
- `model.py`: LeNet-5 & CustomMLP
- `main.py`: train & test & save_plot

---

### 모델 설명

#### LeNet5
- conv1:입력 채널 수 1개, 출력 채널 수 6개, 커널 크기 5*5
- 파라미터: (1*6*5*5) + 6 = 156
- conv2: 입력 채널 수 6개, 출력 채널 수 16개, 커널 크기 5*5
- 파라미터: (6*16*5*5) + 16 = 2416
- conv3: 입력 채널 수 16개, 출력 채널 수 120개, 커널 크기 5*5
- 파라미터: (16*120*5*5) + 120 = 48120
- fc1: 입력 뉴런 수 120개, 출력 뉴런 수 84개
- 파라미터: (120*84) + 84 = 10164
- fc2: 입력 뉴런 수 84개, 출력 뉴런 수 10개
- 파라미터: (84 * 10) + 10 = 850
- **총 파라미터 수:** 156 + 2416 + 48120 + 10164 + 850 = 61506
- **dropout:** 0.5
- **활성화 함수:** tanh

#### CustomMLP
- fc1: 입력 뉴런 수 1024개, 출력 뉴런 수 60개
- 파라미터: (1024*60) + 60 = 61500
- fc2: 입력 뉴런 수 60개, 출력 뉴런 수 10개
- 파라미터: (60*10) + 10 = 610
- **총 파라미터 수:** 61500 + 610 = 62110
- **dropout:** 0.5
- **활성화 함수:** ReLU
---

## 실험결과
### LeNet5 Model

- **Test Accuracy:** View test accuracy [here](https://github.com/KimYohan0317/mnist_classification/blob/main/img/plot_LeNet5_test_acc.png)
- **Test Loss:** View test loss [here](https://github.com/KimYohan0317/mnist_classification/blob/main/img/plot_LeNet5_test_loss.png)
- **Training Accuracy:** View training accuracy [here](https://github.com/KimYohan0317/mnist_classification/blob/main/img/plot_LeNet5_train_acc.png)
- **Training Loss:** View training loss [here](https://github.com/KimYohan0317/mnist_classification/blob/main/img/plot_LeNet5_train_loss.png)

### CustomMLP Model

- **Test Accuracy:** View test accuracy [here](https://github.com/KimYohan0317/mnist_classification/blob/main/img/plot_CustomMLP_test_acc.png)
- **Test Loss:** View test loss [here](https://github.com/KimYohan0317/mnist_classification/blob/main/img/plot_CustomMLP_test_loss.png)
- **Training Accuracy:** View training accuracy [here](https://github.com/KimYohan0317/mnist_classification/blob/main/img/plot_CustomMLP_train_acc.png)
- **Training Loss:** View training loss [here](https://github.com/KimYohan0317/mnist_classification/blob/main/img/plot_CustomMLP_train_loss.png)

#### Test Loss 및 Accuracy

| Model | Loss | Accuracy |
|-------|-----------|----------|
|   LeNet5   |    1.5190  |   94.5%  |
|   CustomMLP   |    0.0928  |   97.31%  |

---

### 요구 사항

- requirements.txt
