# OLIVE: Open-world Language Instruction for Visual-language Evaluation
This repository provides the download instructions for the OLIVE dataset, introduced in the NAACL'24 paper titled ["What Are We Measuring When We Evaluate Large Vision-Language Models? An Analysis of Latent Factors and Biases."](https://openreview.net/pdf/4a61e3a350ac775ec3fa5196beacec80ce26b85b.pdf)

## About OLIVE
OLIVE is a highly diverse, human-corrected multimodal dataset designed to simulate the variety and idiosyncrasies of user queries vision-language models (VLMs) face in real-world scenarios. It aims to support the training and evaluation of VLMs in conditions that more closely resemble their ultimate use cases.

OLIVE contains 9,450 images, 30,120 unique instructions, and 47,250 responses. The images are randomly sampled from [LAION-Aesthetics](https://laion.ai/blog/laion-aesthetics/). The instructions and responses are generated using ChatGPT and subsequently refined through human curation. 

Each image corresponds with five instruction-response pairs. Each pair features a unique response, although instructions may be reused across different pairs. The instruction-response pairs can be broadly categorized into four groups: visual recognition, creative writing, knowledge-based, and elaborated description. 

![image](https://github.com/jq-zh/olive-dataset/assets/164292001/9050cb3b-f263-4f07-8af3-8e37474adb6f)

The dataset is split into 6750 instruction-response pairs for training, 6750 pairs for validation, and 33750 for test. 

|               | Visual Recognition | Creative Writing | Knowledge-Based | Elaborated Description | Total |
|:-------------:|:------------------:|:----------------:|:---------------:|:----------------------:|:-----:|
| **Train**     |        1905        |       1415       |      1750       |          1680          | 6750  |
| **Validation**|        1900        |       1455       |      1755       |          1640          | 6750  |
| **Test**      |        9145        |       7220       |      8595       |          8790          | 33750 |

## Download OLIVE

The dataset can be downloaded via the following links: 

- Training: [images](https://entuedu-my.sharepoint.com/:u:/g/personal/junqi_zhao_staff_main_ntu_edu_sg/EbSaoe-SpOlJiUg_vL0mgVwBvAzwGFF5mIP1Lv1mMchxog?e=RakYIu), [annotations](https://entuedu-my.sharepoint.com/:u:/g/personal/junqi_zhao_staff_main_ntu_edu_sg/Efh_5gWoU-hHgyKlDTCqNtIB6zqD9v61bd8TPtLToLVspQ?e=pwDa1t)

- Validation:  [images](https://entuedu-my.sharepoint.com/:u:/g/personal/junqi_zhao_staff_main_ntu_edu_sg/ERy5kdNAFw1NqmcOT1lFmYEBuHQUrABfMPW7wGj98C9xIw?e=7Lb4fE), [annotations](https://entuedu-my.sharepoint.com/:u:/g/personal/junqi_zhao_staff_main_ntu_edu_sg/EayFAOSzPM1Pq-s2K57sd28BD-7kSIn8cy_NG17vUBa5DQ?e=7z5PbP)

- Testing: [images](https://entuedu-my.sharepoint.com/:u:/g/personal/junqi_zhao_staff_main_ntu_edu_sg/ET0196QSoBlDqqzx8zKxI0oB4gemCAeZk-OgtdtDEv1cWg?e=rnRykM), [annotations](https://entuedu-my.sharepoint.com/:u:/g/personal/junqi_zhao_staff_main_ntu_edu_sg/EZWwNrjqf31LuYmfPwJwliUB3K7x3kWho2wvlTt0JLALhw?e=wBCZ7f)

The annotations are in the following format: 
```
[
  {
    "image": "filename for the image, e.g. -1612194712933037756",
    "category": "category of the instruction-response pair, e.g. visual_recognition",
    "instruction": "task instruction related to the image, e.g. What is the item in the image?",
    "output": "response to the instruction, e.g. The item in the image is a solar sail, which
is a device that is designed to harness the energy from sunlight to propel a spacecraft through
space without the use of fuel. It is a square shaped piece of cloth that acts like a sail and
captures the radiation pressure from the sun to propel the spacecraft forward.",
    "id": "composite index that uniquely identifies each instruction-response pair associated
with a specific image, e.g. res_3_1486, where 3 is the id of the instruction-response pair and
1486 is the unique id for the image",
  },
]
```
