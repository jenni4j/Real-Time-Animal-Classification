<a id="readme-top"></a>

<!-- PROJECT SHIELDS -->
[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]

<!-- PROJECT LOGO -->
<br />
<div align="center">
  <h3 align="center">Real-Time Animal Classification on Raspberry Pi 4</h3>

  <p align="center">
    A cross-discipline project at Georgia Tech — real-time fox detection to automate vaccine biscuit distribution on campus.
    <br />
    <a href="demo.gif">View demo of real-time object detection</a>
  </p>
</div>

---

<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li><a href="#about-the-project">About The Project</a>
      <ul><li><a href="#built-with">Built With</a></li></ul>
    </li>
    <li><a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
  </ol>
</details>

---

## About The Project

This repo is the software component of a cross-discipline at Georgia Tech. The goal was to design and implement a device that detects foxes on campus via camera and automatically distributes vaccine biscuits when one was detected.

**Phase 1 — Pretrained inference:** Run a MobileNetV2 model (pretrained on ImageNet) on a Raspberry Pi 4 for real-time image classification. ImageNet includes fox classes, making it a starting point without any custom training.

**Phase 2 — Fine-tuning:** Fine-tune the model on ~200 fox images captured by an on-campus camera. Due to the small dataset size, overfitting was a known challenge; expanding the dataset was left as a priority for future semesters.

### Built With

[![Python][Python-badge]][Python-url]
[![TensorFlow][TF-badge]][TF-url]
[![Raspberry Pi][RPi-badge]][RPi-url]

<p align="right">(<a href="#readme-top">back to top</a>)</p>

---

## Getting Started

### Prerequisites

- Python 3.10+
- A Raspberry Pi 4 (for on-device inference) or any machine for notebook experimentation
- pip

### Installation

1. Clone the repo
   ```sh
   git clone https://github.com/jenni4j/Real-Time-Animal-Classification.git
   ```
2. Create and activate a virtual environment
   ```sh
   python -m venv myenv
   source myenv/bin/activate
   ```
3. Install dependencies
   ```sh
   pip install -r requirements.txt
   ```

<p align="right">(<a href="#readme-top">back to top</a>)</p>

---

## Usage

**Run pretrained inference on Raspberry Pi:**
```sh
python pretrained_model.py
```

**Fine-tuning experiments:**

Open and run `finetune.ipynb` in Jupyter. The notebook walks through data loading, model fine-tuning, and evaluation.

A demo of the device performing real-time classification is available in [demo.gif](demo.gif).

<p align="right">(<a href="#readme-top">back to top</a>)</p>

---

<!-- MARKDOWN LINKS & IMAGES -->
[contributors-shield]: https://img.shields.io/github/contributors/jenni4j/Real-Time-Animal-Classification.svg?style=for-the-badge
[contributors-url]: https://github.com/jenni4j/Real-Time-Animal-Classification/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/jenni4j/Real-Time-Animal-Classification.svg?style=for-the-badge
[forks-url]: https://github.com/jenni4j/Real-Time-Animal-Classification/network/members
[stars-shield]: https://img.shields.io/github/stars/jenni4j/Real-Time-Animal-Classification.svg?style=for-the-badge
[stars-url]: https://github.com/jenni4j/Real-Time-Animal-Classification/stargazers
[issues-shield]: https://img.shields.io/github/issues/jenni4j/Real-Time-Animal-Classification.svg?style=for-the-badge
[issues-url]: https://github.com/jenni4j/Real-Time-Animal-Classification/issues
[Python-badge]: https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white
[Python-url]: https://www.python.org/
[TF-badge]: https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white
[TF-url]: https://www.tensorflow.org/
[RPi-badge]: https://img.shields.io/badge/Raspberry%20Pi-C51A4A?style=for-the-badge&logo=raspberry-pi&logoColor=white
[RPi-url]: https://www.raspberrypi.com/
