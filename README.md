# VideoGenHub

[![contributors](https://img.shields.io/github/contributors/TIGER-AI-Lab/VideoGenHub)](https://github.com/TIGER-AI-Lab/VideoGenHub/graphs/contributors)
[![license](https://img.shields.io/github/license/TIGER-AI-Lab/VideoGenHub.svg)](https://github.com/TIGER-AI-Lab/VidenGenHub/blob/main/LICENSE)
[![GitHub](https://img.shields.io/github/stars/TIGER-AI-Lab/VideoGenHub?style=social)](https://github.com/TIGER-AI-Lab/VideoGenHub)
[![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2FTIGER-AI-Lab%2FVideoGenHub&count_bg=%23C83DB9&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=visitors&edge_flat=false)](https://hits.seeyoufarm.com)

VideoGenHub is a one-stop library to standardize the inference and evaluation of all the conditional video generation models.
* We define 2 prominent generation tasks (Text-to-Video and Image-to-Video).
* We built a unified inference pipeline to ensure fair comparison. We currently support around 10 models.

## 📄 Table of Contents

- [🛠️ Installation](#%EF%B8%8F-installation-)
- [👨‍🏫 Get Started](#-get-started-)
- [🎫 License](#-license-)

## 🛠️ Installation [🔝](#-table-of-contents)
To install from pypi:
```commandline
pip install videogen-hub
```

To install from github:
```python
git clone https://github.com/TIGER-AI-Lab/VideoGenHub.git
cd VideoGenHub
cd env_cfg
pip install -r requirements.txt
cd ..
pip install -e .
```
The requirement of opensora is in `env_cfg/opensora.txt`

For some models like show one, you need to login through `huggingface-cli`.

```shell
huggingface-cli login
```

## 👨‍🏫 Get Started [🔝](#-table-of-contents)

### Benchmarking
To reproduce our experiment using benchmark.

Example for text-to-video generation: TBD

### Infering one model
```python
import videogen_hub

model = videogen_hub.load('VideoCrafter2')
video = model.infer_one_video(prompt="A child excitedly swings on a rusty swing set, laughter filling the air.")

# Here video is a torch tensor of shape torch.Size([16, 3, 320, 512])
```
See Google Colab here: https://colab.research.google.com/drive/145UMsBOe5JLqZ2m0LKqvvqsyRJA1IeaE?usp=sharing


## 🧠 Philosophy [🔝](#-philosophy-)
By streamlining research and collaboration, VideoGenHub plays a pivotal role in propelling the field of Video Generation.

* Purity of Evaluation: We ensure a fair and consistent evaluation for all models, eliminating biases.
* Research Roadmap: By defining tasks and curating datasets, we provide clear direction for researchers. 
* Open Collaboration: Our platform fosters the exchange and cooperation of related technologies, bringing together minds and innovations.

### Implemented Models
We included more than 10 Models in video generation.

|    Method     	    | Venue  	  |        Type           	         |
|:------------------:|:---------:|:-------------------------------:|
|     LaVie   	      |    - 	    |   Text-To-Video Generation 	    |
| VideoCrafter2   	  |    - 	    |   Text-To-Video Generation 	    |
|   ModelScope   	   |    - 	    |   Text-To-Video Generation 	    |
|  StreamingT2V   	  |    - 	    |   Text-To-Video Generation 	    |
|     Show 1  	      |    - 	    |   Text-To-Video Generation 	    |
|    OpenSora  	     |    - 	    |   Text-To-Video Generation 	    |
| DynamiCrafter2   	 |    - 	    |   Image-To-Video Generation 	   |
|     SEINE   	      | ICLR'24 	 |   Image-To-Video Generation 	   |
|    Consisti2v 	    |    - 	    |   Image-To_Video Generation 	   |
|      I2VGenXL      |    - 	    |   Image-To_Video Generation 	   |


## 🎫 License [🔝](#-table-of-contents)

This project is released under the [License](LICENSE).

