# 🚀 Spark Workshop Labs

An introductory Apache Spark workshop using PySpark and Jupyter notebooks, designed to run in GitHub Codespaces.

## 🎯 What You'll Learn

- Creating and configuring SparkSessions
- Working with DataFrames
- Performing transformations and aggregations
- Using Spark SQL for data analysis
- Best practices for Spark development

## 🚀 Quick Start with GitHub Codespaces

### Option 1: One-Click Launch (Recommended)

1. Click the green **"Code"** button at the top of this repository
2. Select the **"Codespaces"** tab
3. Click **"Create codespace on main"**
4. Wait for the environment to build (2-3 minutes on first launch)
5. Once ready, VS Code will open in your browser with everything pre-configured!

### Option 2: From GitHub.com

1. Navigate to this repository on GitHub
2. Press `.` (period) to open in github.dev, then switch to Codespaces
3. Or use the URL: `https://codespaces.new/YOUR_USERNAME/spark-workshop-labs`

## 📓 Running the Jupyter Notebook

### In Codespaces (VS Code in Browser)

Once your Codespace is ready:

1. **Open the notebook**: Click on `intro_lab.ipynb` in the file explorer
2. **Select kernel**: When prompted, select "Python 3" as your kernel
3. **Run cells**: Click the ▶️ play button on each cell, or use `Shift + Enter`

### Alternative: Using JupyterLab Interface

If you prefer the classic Jupyter interface:

```bash
# Start JupyterLab server
jupyter lab --ip=0.0.0.0 --port=8888 --no-browser --allow-root
```

Then click the link in the terminal or use the "Ports" tab to open port 8888.

## 📁 Project Structure

```
spark-workshop-labs/
├── .devcontainer/
│   └── devcontainer.json    # Codespaces configuration
├── intro_lab.ipynb          # Main workshop notebook
├── requirements.txt         # Python dependencies
├── pyproject.toml          # Project configuration
└── README.md               # This file
```

## 🛠️ Local Development Setup

If you prefer to run locally instead of Codespaces:

### Prerequisites

- Python 3.10 or higher
- Java 11 or higher (required for Spark)

### Installation

```bash
# Clone the repository
git clone https://github.com/YOUR_USERNAME/spark-workshop-labs.git
cd spark-workshop-labs

# Create virtual environment
python -m venv .venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Start Jupyter
jupyter lab
```

## 📋 Requirements

The following packages are automatically installed:

- **pyspark** >= 3.5.0 - Apache Spark Python API
- **jupyterlab** >= 4.0.0 - Interactive development environment
- **notebook** >= 7.0.0 - Jupyter notebook support
- **ipykernel** >= 6.25.0 - IPython kernel for Jupyter

## 🔧 Troubleshooting

### Common Issues

**1. Kernel not found**
```bash
python -m ipykernel install --user --name=python3
```

**2. Spark initialization errors**
- Ensure Java is installed: `java -version`
- In Codespaces, Java is pre-installed via the devcontainer

**3. Out of memory errors**
- Reduce dataset size for local development
- Use `.config("spark.driver.memory", "2g")` when creating SparkSession

**4. Port already in use**
```bash
jupyter lab --port=8889
```

### Reinstall Dependencies

```bash
pip install -r requirements.txt --force-reinstall
```

## 📚 Additional Resources

- [Apache Spark Documentation](https://spark.apache.org/docs/latest/)
- [PySpark API Reference](https://spark.apache.org/docs/latest/api/python/)
- [GitHub Codespaces Documentation](https://docs.github.com/en/codespaces)

## 🤝 Contributing

Feel free to open issues or submit pull requests to improve this workshop!

## 📄 License

This project is open source and available under the MIT License.

---

Happy Learning! 🎉
