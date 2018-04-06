# Hilbert-Schmidt Independence Criterion (HSIC)

Python version of the original MATLAB code of [Hilbert-Schmidt Independence Criterion](http://papers.nips.cc/paper/3201-a-kernel-statistical-test-of-independence.pdf) (HSIC).

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites
* NumPy
* SciPy

We test the code using **Anaconda 4.3.0 64-bit for python 2.7** on windows. Any later version should still work perfectly.

## Apply on your data

### Usage

Import HSIC using

```
from HSIC import hsic_gam
```

Apply HSIC on your data
```
testStat, thresh = hsic_gam(x, y, alph = 0.05)
```

Input of function **hsic_gam()**

| Argument  | Description  |
|---|---|
|x | Data of the first variable. L by dim_x numpy array.|
|y | Data of the second variable. L by dim_y numpy array.|
|alph | lebel of the test |

Output:Output of function **hsic_gam()**

| Argument  | Description  |
|---|---|
|testStat  |test threshold for level alpha test|
|thresh| test statistic|

### Independence test result
- If **testStat < thresh**, x and y are independent.
- If **testStat > thresh**, x and y are not independent.

## Authors

* **Shoubo Hu** - shoubo.sub@gmail.com

See also the list of [contributors](https://github.com/amber0309/HSIC/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
