# Compression models test

## Neural net for testing - custom CNN:
```
Net(
  (conv1): Conv2d(3, 6, kernel_size=(5, 5), stride=(1, 1))
  (pool): MaxPool2d(kernel_size=2, stride=2, padding=0, dilation=1, ceil_mode=False)
  (conv2): Conv2d(6, 16, kernel_size=(5, 5), stride=(1, 1))
  (fc1): Linear(in_features=400, out_features=120, bias=True)
  (fc2): Linear(in_features=120, out_features=84, bias=True)
  (fc3): Linear(in_features=84, out_features=10, bias=True)
)
```

## Dataset for evaluation - CIFAR
https://www.cs.toronto.edu/~kriz/cifar.html

## Results

| Aproach       | Accuracy | Inference time on RTX 2070 |
|---------------|----------|----------------------------|
| Default state | 64 %     | 413 µs ± 56.7 µs           |
| Pruning       | 62 %     | 1.06 ms ± 491 µs           |
| Quantization  | 64 %     | 390 µs ± 43.4 µs           |
| Distilation   | 60 %     | 396 µs ± 97.9 µs           |


## Experiments

In jupyter notebook
