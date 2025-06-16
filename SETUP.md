# Wolfram Engine Setup Guide

This guide helps you set up the Wolfram Engine to run the tensor computation examples in this repository.

## Prerequisites

- Wolfram Engine (free for developers)
- Python 3.7+
- Jupyter notebook

## Installation Steps

### 1. Install Wolfram Engine

1. Go to [Wolfram Engine for Developers](https://www.wolfram.com/engine/)
2. Create a free Wolfram ID account
3. Download and install Wolfram Engine for your operating system

### 2. Configure Wolfram Engine

After installation, configure the engine:

```bash
# Configure Wolfram Engine
wolframscript -configure
```

When prompted, enter your Wolfram ID credentials.

### 3. Install Wolfram Language Kernel for Jupyter

```bash
# Install the Wolfram Language kernel
pip install wolframclient

# Or using conda
conda install -c conda-forge wolframclient
```

### 4. Configure Jupyter Kernel

```bash
# Add Wolfram Language kernel to Jupyter
python -c "from wolframclient import WolframLanguageSession; session = WolframLanguageSession(); session.start()"
```

### 5. Alternative: Use Wolfram Language Kernel

You can also install the official Wolfram Language kernel:

1. Download from [Wolfram Language Kernel for Jupyter](https://github.com/WolframResearch/WolframLanguageForJupyter)
2. Follow the installation instructions in the repository

## Verification

Test your setup:

1. Start Jupyter notebook:
   ```bash
   jupyter notebook
   ```

2. Create a new notebook with "Wolfram Language" kernel

3. Test with a simple command:
   ```mathematica
   $Version
   ```

4. You should see the Wolfram Engine version information

## Running the Examples

1. Open `tensor_examples.ipynb` in Jupyter
2. Select "Wolfram Language" as the kernel
3. Run the cells sequentially

## Troubleshooting

### Common Issues

1. **Kernel not found**: Make sure Wolfram Engine is properly installed and configured
2. **License issues**: Ensure you have a valid Wolfram ID and the engine is activated
3. **Path issues**: Verify that `wolframscript` is in your system PATH

### Getting Help

- [Wolfram Engine Documentation](https://reference.wolfram.com/language/)
- [Wolfram Community](https://community.wolfram.com/)
- [Wolfram Language Kernel Issues](https://github.com/WolframResearch/WolframLanguageForJupyter/issues)

## Alternative: Use Mathematica

If you have Mathematica installed, you can:

1. Open the `.nb` file directly in Mathematica
2. Copy and paste the code cells from the Jupyter notebook
3. Run the examples in the standard Mathematica interface

## Performance Notes

- Wolfram Engine provides the same computational capabilities as Mathematica
- For large tensor computations, ensure sufficient RAM is available
- The engine is optimized for symbolic and numerical computations

## Next Steps

Once your setup is working:

1. Run through the `tensor_examples.ipynb` notebook
2. Experiment with your own tensor computations
3. Explore the advanced techniques demonstrated in the examples

Happy computing with Wolfram Language!
