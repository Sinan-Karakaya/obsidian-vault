# Types of ML

- [[Supervised learning]]
- Unsupervised learning
- Reinforcement learning

## The project

```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt

# The cols of the csv/labels, are not included in the sample data
cols = ["fLength", "fWidth", "fSize", "fConc", "fConc1", "fAsym", "fM3Long", "fM3Trans", "fAlpha", "fDist", "class"]
df = pd.read_csv('sample_data/magic04.data', names=cols)

# Labels are g or h, we need to convert them to 0 or 1
df["class"] = (df["class"] == "g").astype(int)
```

#### Show our data

```python
for label in cols[:-1]:
    # Everywhere the label == 1, we get the label and draw it on the histogram
    plt.hist(df[df["class"] == 1][label], color='blue', label='gamma', alpha=0.7, density=True)

  

    # The opposite
    plt.hist(df[df["class"] == 0][label], color='red', label='hadron', alpha=0.7, density=True)

    plt.title(label)
    plt.ylabel("Probability") # Since its a density plot
    plt.xlabel(label)
    plt.legend()
    plt.show()
```

#### Train, validation, test datasets

