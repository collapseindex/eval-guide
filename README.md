# ML EVALUATION METRICS - INTERACTIVE LESSONS

**Version 1.0.0**

Learn ML evaluation metrics by running actual code and seeing real results!

## Quick Start

**All notebooks are pre-run with outputs!** You can just read through them to learn, or run the code yourself:

1. **Just reading?** Open any notebook and scroll through - all outputs are already there!
2. **Want to run it yourself?** Open in Jupyter/VS Code, run the first cell (auto-installs packages), then run all cells
3. **Want to experiment?** Try the 🎯 CHALLENGE sections in each lesson to modify parameters and see what happens!

## What's Inside

### 📓 Self-Contained Interactive Notebooks

Each notebook includes theory, code, **pre-run outputs**, and commentary - everything you need in one place! Read them like a tutorial or run the code yourself.

1. **[lesson1_classification.ipynb](lesson1_classification.ipynb)** - Classification Metrics 🌸
   - Accuracy, Precision, Recall, F1-Score explained with analogies
   - Confusion Matrix visual analysis (WHERE DID IT MESS UP?)
   - The Accuracy Trap (why 99% accuracy can mean your model is useless)
   - TP/FP/TN/FN explained, harmonic mean breakdown
   - Dataset: Iris flowers (3 classes)
   - **Metaphors:** Metal detectors, lost keys, sorting M&Ms, grading tests

2. **[lesson2_regression.ipynb](lesson2_regression.ipynb)** - Regression Metrics 📈
   - MAE, MSE, RMSE, R² (the most popular regression metric)
   - Actual vs predicted scatter plots with analysis
   - Error distribution histograms
   - Mathematical symbols explained (Σ, √, variance)
   - Dataset: Diabetes (scaled to simulate house prices)
   - **Metaphors:** Dartboards, roommate food theft fines

3. **[lesson3_text_classification.ipynb](lesson3_text_classification.ipynb)** - Text Classification 📝
   - TF-IDF vectorization explained (teaching math to poetry)
   - Handling imbalanced text data
   - Macro vs weighted averaging with clear examples
   - Naive Bayes classifier introduction
   - Dataset: Synthetic news articles (4 categories)
   - **Analysis:** Dynamic commentary based on actual model output

4. **[lesson4_text_generation.ipynb](lesson4_text_generation.ipynb)** - BLEU & ROUGE 🌍
   - BLEU for translation quality (precision-focused)
   - ROUGE for summarization (recall-focused)
   - N-grams explained (why "dog bites man" ≠ "man bites dog")
   - When to use what (translation vs summarization)
   - Precision vs Recall difference clarified
   - **Real talk:** Limitations of word-counting metrics

5. **[lesson5_advanced_classification.ipynb](lesson5_advanced_classification.ipynb)** - ROC/AUC 📈
   - ROC curves visualized (smart vs lucky models)
   - AUC score interpretation (0.9+ = excellent)
   - Precision-Recall curves (better for imbalanced data)
   - Threshold tuning explained with examples
   - TPR/FPR formulas and probability predictions
   - **Learn:** Which models actually understand data vs just guessing

6. **[lesson6_cross_validation.ipynb](lesson6_cross_validation.ipynb)** - Cross-Validation 🔄
   - Why single splits are unreliable (don't get fooled by luck)
   - K-fold visualization with color-coded splits
   - Stratified sampling explained (essential for classification!)
   - Model comparison with box plots
   - Standard deviation and consistency analysis
   - **Basketball analogy:** One free throw ≠ player evaluation

## Installation

### Option 1: Auto-install (Recommended)
Just run the first cell of any notebook - it auto-installs everything!

### Option 2: Manual install
```bash
pip install -r requirements.txt
```

## Requirements

- Python 3.8+
- Jupyter Notebook or VS Code with Jupyter extension
- Internet connection (for downloading datasets)

## Package Dependencies

All auto-installed by the notebooks:
- numpy
- matplotlib
- seaborn
- scikit-learn
- nltk (for text metrics)
- rouge-score (for summarization)
- pandas

## How to Use

### In VS Code:
1. Open any `.ipynb` file
2. Select Python kernel
3. Click "Run All" or run cells one by one

### In Jupyter:
1. Start Jupyter: `jupyter notebook`
2. Open any `.ipynb` file
3. Run cells with Shift+Enter

## Learning Path

**Beginner?** Start here:
1. Lesson 1 (Classification) - Learn the basics
2. Lesson 2 (Regression) - Understand error metrics
3. Lesson 6 (Cross-Validation) - Don't get fooled by lucky splits

**Intermediate?**
1. Lesson 3 (Text Classification) - Handle real-world imbalance
2. Lesson 5 (ROC/AUC) - Advanced model evaluation

**Working with text/LLMs?**
1. Lesson 4 (Text Generation) - BLEU and ROUGE explained

## What Makes This Different

- **Real code, real outputs** - Not just formulas
- **Visual explanations** - See the metrics in charts
- **Practical examples** - Understand when to use what
- **Auto-setup** - No installation headaches
- **Beginner-friendly** - Clear explanations, no PhD required

## Beyond Standard Metrics

This project teaches **standard ML evaluation metrics** (accuracy, F1, RMSE, etc.). For advanced model stability and robustness evaluation, check out:

### Structural Retention Index (SRI) & Collapse Index (CI)

**What they measure:**
- **Collapse Index (CI)** - Prediction instability under perturbations
- **Structural Retention Index (SRI)** - Structural quality and retention under stress
- **Together:** Comprehensive failure mode analysis beyond accuracy

**Why it matters:**
Standard metrics say "90% accuracy - ship it!" But under real-world perturbations (typos, paraphrasing, noise), models fail in distinct ways:
- **Type I:** Confidently wrong (most dangerous)
- **Type II:** Hidden instability (brittleness)
- **Type III-V:** Various flip patterns

SRI + CI reveal these failure modes that confidence alone misses.

**Comparison: Standard Metrics vs SRI/CI**

| Aspect | Standard Metrics (This Guide) | SRI + CI (Collapse Index Labs) |
|--------|-------------------------------|--------------------------------|
| **What they measure** | Static performance on test set | Dynamic stability under perturbations |
| **Question answered** | "How accurate is the model?" | "How will it break in production?" |
| **Test conditions** | Clean, curated data | Real-world noise (typos, paraphrasing) |
| **Failure detection** | Only final errors | Failure modes & severity types (I-V) |
| **Example** | "90% accuracy" ✅ | "90% accuracy but Type I failures (confidently wrong)" ⚠️ |
| **Discrimination power** | Confidence: AUC ~0.17 | SRI/CI: AUC ~0.87 (5× better) |
| **Use case** | Model selection, benchmarking | Production readiness, robustness testing |
| **When to use** | Initial development & comparison | Pre-deployment validation |
| **Availability** | Open-source (scikit-learn, NLTK) | Proprietary (Collapse Index Labs) |

## 🚨 Real-World Problem Preview

Imagine: Your sentiment model shows 92% accuracy in testing.
You deploy it. Users complain it's "weirdly confident but wrong."

Standard metrics say: ✅ 92% - ship it!
SRI/CI reveal: ⚠️ Type I failures (confidently wrong on critical cases)

**This guide teaches you the 92%. Lesson 6 hints at why that's not enough.**

**Bottom line:** Standard metrics tell you *if* your model works. SRI/CI tell you *how* it will fail.

**Learn more:**
- **Website:** [collapseindex.org](https://collapseindex.org)
- **Evals:** [collapseindex.org/evals.html](https://collapseindex.org/evals.html)
- **Research:** [SRI Paper (Zenodo)](https://doi.org/10.5281/zenodo.18016507)
- **GitHub:** [@collapseindex](https://github.com/collapseindex)

*Note: SRI/CI are advanced proprietary metrics from Collapse Index Labs. This project focuses on foundational evaluation metrics that are open-source and widely used.*

**⚖️ Legal Note:** SRI (Structural Retention Index), CI (Collapse Index), and CSI (Collapse Severity Index) are proprietary methodologies © 2025 Collapse Index Labs - Alex Kwon. They are NOT covered by this repository's MIT License and may NOT be reproduced, implemented, or reverse-engineered without authorization. For licensing: ask@collapseindex.org

## Tips

- Run cells in order (some depend on previous cells)
- Read the markdown cells - they explain what's happening
- Experiment! Change parameters and see what happens
- Check the guide when you need quick reference

## Troubleshooting

**Packages won't install?**
- Make sure you have internet connection
- Try manual install: `pip install -r requirements.txt`

**Plots not showing?**
- Make sure you're using Jupyter or VS Code with Jupyter extension
- Try adding `%matplotlib inline` at the top

**Dataset download fails?**
- Check internet connection
- Scikit-learn downloads datasets automatically
- May take a minute on first run

## Next Steps

After completing the notebooks:
1. Try the metrics on your own datasets
2. Build a real ML project using these evaluation techniques
3. Read the full guide for deeper understanding
4. Experiment with different models and see how metrics change

---

## Credits & Acknowledgments

### Datasets Used

- **Iris Dataset** - Fisher, R.A. (1936) - Classic flower classification dataset from UCI ML Repository
- **Diabetes Dataset** - Scikit-learn built-in dataset - Used for regression examples
- **Synthetic Text Data** - Generated for text classification examples (sports, tech, politics, health)

### Libraries & Metrics

- **scikit-learn** - Machine learning library providing datasets and evaluation metrics
  - Classification metrics: accuracy_score, precision_score, recall_score, f1_score, confusion_matrix
  - Regression metrics: mean_absolute_error, mean_squared_error, r2_score
  - Model selection: cross_val_score, KFold, StratifiedKFold
  - License: BSD 3-Clause

- **NLTK (Natural Language Toolkit)** - Text processing and BLEU score implementation
  - License: Apache 2.0

- **rouge-score** - Google's ROUGE metric implementation for summarization evaluation
  - License: Apache 2.0

- **matplotlib** - Visualization library for plots and charts
  - License: PSF-based

- **seaborn** - Statistical data visualization built on matplotlib
  - License: BSD 3-Clause

- **NumPy** - Numerical computing library
  - License: BSD 3-Clause

- **pandas** - Data manipulation and analysis
  - License: BSD 3-Clause

### Inspiration & References

- Scikit-learn documentation and examples
- Research papers on evaluation metrics
- ML community best practices

---

## Author

**Collapse Index Labs - Alex Kwon**
- GitHub: [@collapseindex](https://github.com/collapseindex)
- ORCID: [0009-0002-2566-5538](https://orcid.org/0009-0002-2566-5538)

## Citation

If you find this project helpful and want to cite it in your research or teaching:

```bibtex
@software{kwon2026evalguide,
  author = {Kwon, Alex},
  organization = {Collapse Index Labs},
  title = {ML Evaluation Metrics - Interactive Lessons},
  year = {2026},
  url = {https://github.com/collapseindex/eval-guide},
  version = {1.0.0}
}
```

Or use the "Cite this repository" feature on GitHub (see [CITATION.cff](CITATION.cff))

## License

MIT License - Feel free to use, modify, and share!

See [LICENSE](LICENSE) for details.

**Note**: This project uses datasets and libraries with their own licenses (listed above). All are permissive open-source licenses compatible with this project's MIT License.

---

Made with ❤️ for ML learners

Last updated: 2026-01-02
