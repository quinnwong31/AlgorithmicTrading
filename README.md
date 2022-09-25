# Algorithmic Trading Bot
## Description

The Algorithmic Trading Bot notebook provides an example of how one can use Jupyter and Python to build an algorithmic trading bot.

The notebook is divided into the following phases:

- **Establish a Baseline Performance**
- **Tune the Baseline Trading Algorithm**
- **Evaluate a New Machine Learning Classifier**
- **Create an Evaluation Report**

## Technologies

This example uses the following technologies:

- **Jupyter** - Jupyter is a web-based interactive development environment for data science and analysis. Please see [Jupyter documentation](https://jupyter.org/) for more information.
- **pandas** - pandas is a software library written for the Python programming language for data manipulation and analysis. Please see [pandas documentation](https://pandas.pydata.org/) for more information.
- **numpy**
- **sklearn**
- **pandas.tseries.offsets**

## Installation

The `pathlib` and `csv` libraries are already installed with Python 3.7.

In order to use the Algorithmic Trading Bot notebook, you will need to install `Jupyter` and `pandas`. Below are the instructions for installing each required library.

### Installing Jupyter

To install Jupyter, please refer to the [Jupyter Installation Guide](https://jupyter.org/install).

### Installing pandas

To install `pandas`, please refer to the [pandas Installation Guide](https://pandas.pydata.org/pandas-docs/stable/getting_started/install.html).

## Usage

### Launching the Algorithmic Trading Bot Notebook

To launch the Algorithmic Trading Bot Notebook, perform the following steps:

1. Open Terminal.

![Launch_Terminal](/images/launching_open_terminal.jpg)

2. Navigate to the location of the Algorithmic Trading Bot Notebook.
3. Enter `jupyter lab` at the Terminal prompt.

![Launch_Jupyter](/images/launching_jupyter.jpg)

4. Verify that you can access Jupyter in your browser.

![Jupyter](/images/jupyter.jpg)

## Tuning the Baseline Algorithm
**Step 1: Tune the training algorithm by adjusting the size of the training dataset.**
To do so, slice your data into different periods. Rerun the notebook with the updated parameters, and record the results in your README.md file.

Baseline - 3 months
![3 Months](/images/baseline.png)



6 months
![6 Months](/images/table_tune_6mos.png)

9 months
![9 Months](/images/table_tune_9mos.png)

12 months
![12 Months](/images/table_tune_12mos.png)


Answer the following question: What impact resulted from increasing or decreasing the training window?
When increasing the training window, the strategy results matched the actual results a little closer. 


**Step 2: Tune the trading algorithm by adjusting the SMA input features.**

Baseline - 3 months
![3 Months](/images/baseline.png)

12 months w/ 30 day short
![12 months w/ 30 day short](/images/table_tune_12mos_30days_short.png)

12 months w/ 60 day short
![12 months w/ 60 day short](/images/table_tune_12mos_60days_short.png)

12 months w/ 90 day short
![12 months w/ 90 day short](/images/table_tune_12mos_90days_short.png)


Answer the following question: What impact resulted from increasing or decreasing either or both of the SMA windows?
It appears that increasing or decreasing the short SMA does not have any effect.   However, increase the long SMA does have some effect on actual vs strategy returns. 

**Step 3: Choose the set of parameters that best improved the trading algorithm returns.**
Save a PNG image of the cumulative product of the actual returns vs. the strategy returns, and document your conclusion in your README.md file.

12 months
60 days short SMA
200 days long SMA

![12 months w/ 90 day short](/images/tune_12mos_60days_short_200days_long.png)



## Contributors

This sample application was authored by:

Quinn Wong (quinn.wong@gmail.com)
LinkedIn: https://www.linkedin.com/in/quinnwong/

## License

The MIT License (MIT)

Copyright (c) 2022 Quinn Wong

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
