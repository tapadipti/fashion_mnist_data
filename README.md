# fashion_mnist_data

This repository contains the Fashion Mnist Dataset, which is obtained using the following Python script:

```
import pickle
from tensorflow.keras.datasets import fashion_mnist

data = fashion_mnist.load_data()

with open("fashion_mnist_data.pkl", "wb") as fd:
    pickle.dump(data, fd)
```

To use this data, use the following Python script:

```
with open("fashion_mnist_data.pkl", "rb") as fd:
    data = pickle.load(fd)
    
(x_train, y_train),(x_test, y_test) = data
```
