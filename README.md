# tMNIST-PyTorch
PyTorch Dataset Generator for Transformed MNIST Digits

## How to generate
- Set the parameters in `generate.py` as desired.
- Run `python generate.py`.

## How to load into PyTorch
```
import tMNISTDataset from .

dataset = tMNISTDataset(data_file='tMNIST/data.npy', root_dir='tMNIST', transform=transforms.ToTensor())
data_loader = DataLoader(dataset=dataset, batch_size=batch_size, shuffle=True)

for epoch in range(epochs):
    for iteration, (x, y) in enumerate(data_loader):
        x, y = x.to(device), y.to(device)
        # Train model
```
