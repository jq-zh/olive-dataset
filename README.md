# OLIVE: Open-world Language Instruction for Visual-language Evaluation
This repository provides the download instructions for the OLIVE dataset, introduced in the NAACL'24 paper titled ["What Are We Measuring When We Evaluate Large Vision-Language Models? An Analysis of Latent Factors and Biases."](https://openreview.net/pdf/4a61e3a350ac775ec3fa5196beacec80ce26b85b.pdf)

## About OLIVE
The OLIVE dataset is a highly diverse, human-corrected multimodal collection designed to simulate the variety and idiosyncrasies of user queries vision-language models (VLMs) face in real-world scenarios. It supports the training and evaluation of VLMs in conditions that more closely resemble their ultimate use cases.

The dataset contains 9,450 images, 30,120 unique instructions, and 47,250 responses. The images are randomly sampled from [LAION-Aesthetics](https://laion.ai/blog/laion-aesthetics/). The instructions and responses are generated using ChatGPT and subsequently refined through human curation. 

Each image corresponds with five instruction-response pairs. Each pair features a unique response, although instructions may be reused across different pairs. The instruction-response pairs can be broadly categorized into four groups: visual recognition, creative writing, knowledge-based, and elaborated description. 

![image](https://github.com/jq-zh/olive-dataset/assets/164292001/9050cb3b-f263-4f07-8af3-8e37474adb6f)

The dataset is split into 6,750 instruction-response pairs for training, 6,750 pairs for validation, and 33,750 for test. 

|               | Visual Recognition | Creative Writing | Knowledge-Based | Elaborated Description | Total |
|:-------------:|:------------------:|:----------------:|:---------------:|:----------------------:|:-----:|
|   **Train**   |        1905        |       1415       |      1750       |          1680          | 6750  |
| **Validation**|        1900        |       1455       |      1755       |          1640          | 6750  |
| **Test_v1.0** |        7285        |       5910       |      6805       |          7285          | 27000 |
| **Test_v2.0** |        9145        |       7220       |      8595       |          8790          | 33750 |

Note: Test_v1.0 is a subset of Test_v2.0 

## Download OLIVE

The OLIVE dataset can be downloaded via the following links: 

Images: [train](https://entuedu-my.sharepoint.com/:u:/g/personal/junqi_zhao_staff_main_ntu_edu_sg/EbSaoe-SpOlJiUg_vL0mgVwBvAzwGFF5mIP1Lv1mMchxog?e=RakYIu), [validation](https://entuedu-my.sharepoint.com/:u:/g/personal/junqi_zhao_staff_main_ntu_edu_sg/ERy5kdNAFw1NqmcOT1lFmYEBuHQUrABfMPW7wGj98C9xIw?e=7Lb4fE), [test](https://entuedu-my.sharepoint.com/:u:/g/personal/junqi_zhao_staff_main_ntu_edu_sg/ET0196QSoBlDqqzx8zKxI0oB4gemCAeZk-OgtdtDEv1cWg?e=rnRykM)

Annotations: [train](https://entuedu-my.sharepoint.com/:u:/g/personal/junqi_zhao_staff_main_ntu_edu_sg/Efh_5gWoU-hHgyKlDTCqNtIB6zqD9v61bd8TPtLToLVspQ?e=pwDa1t), [validation](https://entuedu-my.sharepoint.com/:u:/g/personal/junqi_zhao_staff_main_ntu_edu_sg/EayFAOSzPM1Pq-s2K57sd28BD-7kSIn8cy_NG17vUBa5DQ?e=7z5PbP), [test_v1.0](https://entuedu-my.sharepoint.com/:u:/g/personal/junqi_zhao_staff_main_ntu_edu_sg/EZheSs0Q68BOhtgCnXnislUBw2V1ixVNcml_qRv6jnslXQ?e=VHqlJ1), [test_v2.0](https://entuedu-my.sharepoint.com/:u:/g/personal/junqi_zhao_staff_main_ntu_edu_sg/EZWwNrjqf31LuYmfPwJwliUB3K7x3kWho2wvlTt0JLALhw?e=sgaABG)

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
## Performance

The table below reports the **zero-shot performance** of different models on the **test_v1.0** split, utilizing CIDEr as the evaluation metric.

|    Model     | Vision Encoder | Language Model | Size | CIDEr  | 
|:------------:|:--------------:|:--------------:|:----:|:------:|
|  **BLIP-2**  |     ViT-G      |   FlanT5-XL    |  4B  |  5.2   |
| **MiniGPT-4**|     ViT-G      |   Vicuna-7B    |  8B  |  1.6   |
| **mPLUG-Owl**|     ViT-L      |    LLaMA-7B    |  7B  |  4.4   |
|  **LLaVA**   |     ViT-L      |    LLaMA-7B    |  7B  |  29.6  |
