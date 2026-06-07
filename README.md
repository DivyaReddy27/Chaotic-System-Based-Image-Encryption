# Chaotic-System-Based-Image-Encryption

## Overview

This project demonstrates the implementation and analysis of chaos-based image encryption techniques using three popular chaotic systems:

* Arnold Cat Map
* Henon Map
* Logistic Map

The project provides encryption and decryption functionality for grayscale and RGB images while evaluating security through:

* Histogram Analysis
* Adjacent Pixel Correlation Analysis
* Key Sensitivity Testing

Chaos-based cryptography leverages the properties of chaotic systems such as randomness, ergodicity, and extreme sensitivity to initial conditions, making them suitable for secure image encryption.

---

## Features

### Arnold Cat Map Encryption

* Pixel position permutation (confusion)
* Reversible transformation
* Supports image reconstruction through decryption
* Demonstrates scrambling behavior using iterative transformations

### Henon Map Encryption

* Chaotic key-stream generation using the Henon system
* XOR-based pixel diffusion
* Supports grayscale and color images
* Strong key sensitivity

### Logistic Map Encryption

* Dynamic chaotic sequence generation
* Pixel diffusion and substitution
* Key-dependent encryption process
* Enhanced resistance to statistical attacks

---

## Security Analysis

The project includes several evaluation techniques commonly used in image cryptography.

### Histogram Analysis

Compares pixel intensity distributions between:

* Original image
* Encrypted image

A secure encryption scheme should produce a nearly uniform histogram.

### Adjacent Pixel Correlation Analysis

Measures correlation between neighboring pixels:

* Horizontal
* Vertical
* Diagonal

Encrypted images should exhibit significantly reduced correlation compared to the original image.

### Key Sensitivity Testing

Demonstrates that even a minor change in:

* Encryption key
* Initial chaotic parameters

results in completely different encrypted/decrypted outputs.

---

## Project Structure

```text
├── images/
│   ├── HorizonZero.png
│   ├── lena.bmp
│
├── arnold_cat.py
├── henon_map.py
├── logistic_map.py
├── analysis.py
│
├── outputs/
│   ├── *_ArnoldcatEnc.png
│   ├── *_ArnoldcatDec.png
│   ├── *_HenonEnc.png
│   ├── *_HenonDec.png
│   ├── *_LogisticEnc.png
│   └── *_LogisticDec.png
│
└── README.md
```

---

## Requirements

Install the required dependencies:

```bash
pip install numpy pillow matplotlib opencv-python tqdm
```

---

## Usage

### Arnold Cat Map

```python
key = 20

ArnoldCatEncryption("HorizonZero.png", key)
ArnoldCatDecryption("HorizonZero_ArnoldcatEnc.png", key)
```

### Henon Map

```python
key = (0.1, 0.1)

HenonEncryption("HorizonZero.png", key)
HenonDecryption("HorizonZero_HenonEnc.png", key)
```

### Logistic Map

```python
key = "abcdefghijklm"

LogisticEncryption("HorizonZero.png", key)
LogisticDecryption("HorizonZero_LogisticEnc.png", key)
```

---

## Example Workflow

1. Load an image.
2. Encrypt using a chaotic encryption algorithm.
3. Generate encrypted image output.
4. Perform decryption using the same key.
5. Compare:

   * Original image
   * Encrypted image
   * Decrypted image
6. Analyze security using:

   * Histograms
   * Correlation plots

---

## Results

### Original Image

* High adjacent pixel correlation
* Non-uniform histogram

### Encrypted Image

* Randomized pixel distribution
* Reduced neighboring pixel correlation
* Uniform histogram characteristics

### Decrypted Image

* Successful recovery of original image when correct key is used

---

## Research Background

This implementation is inspired by chaos-based image encryption techniques discussed in:

**"A Review of Chaos Based Image Encryption"**
Kanika Suneja, Shelza Dua, Mohit Dua (2019)

The paper reviews various chaotic systems including:

* Logistic Map
* Arnold Cat Map
* Henon Map

and their applications in image cryptography.

---

## Future Improvements

* AES + Chaos hybrid encryption
* DNA-based image encryption
* Multi-dimensional chaotic systems
* NPCR and UACI evaluation metrics
* Real-time video encryption
* Performance benchmarking

---

## License

This project is intended for educational and research purposes.

Feel free to modify and extend the implementation for academic work and experimentation.

---

## Author

Developed as an implementation and study of chaos-based image encryption algorithms for secure multimedia communication.
