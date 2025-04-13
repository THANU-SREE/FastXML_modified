 **FastXML_modified**
Enhanced FastXML algorithm with noise injection for dependable AI and robustness
 n1_fastXML: Enhanced FastXML with Noise Injection

A modified implementation of FastXML (Fast eXtreme Multilabel Learning) algorithm with Gaussian noise injection for improved robustness, reliability, and performance on extreme classification tasks.

 **Overview**

This project enhances the original FastXML algorithm by incorporating a controlled noise injection technique during training. By introducing Gaussian noise into the feature matrix, n1_fastXML achieves better generalization performance and enhanced resilience against input perturbations.

 **Key Features**

 **Enhanced Robustness**: Demonstrates improved stability under noisy and adversarial conditions
 **Dependable AI**: Aligns with principles of reliable and trustworthy machine learning
 **Tunable Noise Scale**: Adjustable noise injection via the `noise_scale` parameter
 **Minimal Overhead**: Maintains FastXML's computational efficiency with negligible additional cost
 **Preserved Interpretability**: Retains the explainable treebased structure of the original algorithm

 
 **Requirements**
 C++ compiler with C++11 support
 CMake (optional, for build automation)
 MATLAB (for evaluation scripts)


**Installation**

```bash
 Clone the repository
git clone https://github.com/yourusername/n1fastXML.git
cd n1fastXML

 Compile the code
g++ O3 o n1_fastXML_train Modified_n1_fastXML_train.cpp
g++ O3 o n1_fastXML_predict fastXML_predict.cpp
```

Usage

Training
```
./n1_fastXML_train [options] train_data_file model_dir
```

Options:

-T : Number of trees (default: 50)
-m : Maximum leaf size (default: 10)
-n : Number of labels per leaf (default: 20)
-l : Log loss coefficient (default: 1.0)
-s : Noise scale (default: 0.001)

Prediction
```
./n1_fastXML_predict [options] test_data_file model_dir score_file
```

Experimental Results
The modified n1_fastXML demonstrates significant improvements in:

Propensity-weighted precision metrics (P@k_wt)
Propensity-weighted nDCG (nDCG@k_wt)
Robustness under noise injection during test time

See the full report for detailed experimental results and analysis.


Directory Structure
```
n1-fastXML/
├── src/
│   ├── Modified_n1_fastXML_train.cpp
│   ├── Modified_n1_fastXML.h
│   ├── fastXML.cpp
│   └── fastXML_predict.cpp
├── evaluation/
│   └── matlab_scripts/
│       └── evaluate_metrics.m
├── examples/
│   └── example_usage.sh
├── data/
│   └── README.md
├── docs/
│   └── report.pdf
└── README.md
```

Citation
If you use this code in your research, please cite:
@article{shree2023enhancing,
  title={Enhancing FastXML for Dependable AI: Robustness through Noise Injection},
  author={Shree, Avula Thanu and Singh, Vishwanath},
  journal={},
  year={2023}
}

Acknowledgments

Original FastXML algorithm by Yashoteja Prabhu and Manik Varma
Extreme Classification Repository: http://manikvarma.org/downloads/XC/XMLRepository.html
