## MNIST_classification

### mnist 이미지 분류 task

---

### 파일 설명

- `dataset.py`: 데이터셋 관련 코드
- `model.py`: 모델 정의 코드
- `main.py`: 주 실행 파일

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

- Test Accuracy: ![LeNet5 Model Test Accuracy](https://github.com/KimYohan0317/mnist_classification/blob/main/img/plot_LeNet5_test_acc.png)
- Test Loss: ![LeNet5 Model Test Loss](https://github.com/KimYohan0317/mnist_classification/blob/main/img/plot_LeNet5_test_loss.png)
- Training Accuracy: ![LeNet5 Model Training Accuracy](https://github.com/KimYohan0317/mnist_classification/blob/main/img/plot_LeNet5_train_acc.png)
- Training Loss: ![LeNet5 Model Training Loss](https://github.com/KimYohan0317/mnist_classification/blob/main/img/plot_LeNet5_train_loss.png)

### CustomMLP Model

- Test Accuracy: ![CustomMLP Model Test Accuracy](https://github.com/KimYohan0317/mnist_classification/blob/main/img/plot_CustomMLP_test_acc.png)
- Test Loss: ![CustomMLP Model Test Loss](https://github.com/KimYohan0317/mnist_classification/blob/main/img/plot_CustomMLP_test_loss.png)
- Training Accuracy: ![CustomMLP Model Training Accuracy](https://github.com/KimYohan0317/mnist_classification/blob/main/img/plot_CustomMLP_train_acc.png)
- Training Loss: ![CustomMLP Model Training Loss](https://github.com/KimYohan0317/mnist_classification/blob/main/img/plot_CustomMLP_train_loss.png)
#### Test Loss 및 Accuracy

| Model | Loss | Accuracy |
|-------|-----------|----------|
|   LeNet5   |    1.5190  |   94.5%  |
|   CustomMLP   |    0.0928  |   97.31%  |

---

### 요구 사항

- 해당 프로젝트를 실행하기 위해 다음 사항이 필요합니다.
- 추가적인 설치나 설정에 대한 참고사항이 있을 경우 여기에 작성해주세요.
