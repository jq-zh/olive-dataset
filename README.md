# OLIVE dataset

The OLIVE (Open-world Language Instruction for Visual-language Evaluation) dataset is a highly diverse, human-corrected multimodal collection designed to simulate the variety and idiosyncrasies of user queries vision-language models (VLMs) face in real-world scenarios. It aims to support the training and evaluation of VLMs in conditions that more closely resemble their ultimate use cases.

OLIVE contains 9,450 images, 30,120 unique instructions, and 47,250 responses. The images are randomly sampled from [LAION-Aesthetics](https://laion.ai/blog/laion-aesthetics/). The instructions and responses are generated using ChatGPT and subsequently refined through human curation. 

Each image corresponds with five instruction-response pairs. Each pair features a unique response, although instructions may be reused across different pairs. The instruction-response pairs can be broadly categorized into four groups: visual recognition, creative writing, knowledge-based, and elaborated description. 
 
Below are some examples:

![image](https://github.com/jq-zh/olive-dataset/assets/164292001/9050cb3b-f263-4f07-8af3-8e37474adb6f)

OLIVE is split into 6750 instruction-response pairs for training, 6750 pairs for validation, and 33750 for test. 

|               | Visual Recognition | Creative Writing | Knowledge-Based | Elaborated Description | Total |
|:-------------:|:------------------:|:----------------:|:---------------:|:----------------------:|:-----:|
| **Train**     |        1905        |       1415       |      1750       |          1680          | 6750  |
| **Validation**|        1900        |       1455       |      1755       |          1640          | 6750  |
| **Test**      |        9145        |       7220       |      8595       |          8790          | 33750 |

This page provides the download instructions for OLIVE. For more details on the dataset, please refer to [arXiv paper](https://openreview.net/pdf?id=2mfxLkYcyL).

## Download images 
The images for OLIVE can be downloaded here: [train](https://entuedu-my.sharepoint.com/:u:/g/personal/junqi_zhao_staff_main_ntu_edu_sg/EbSaoe-SpOlJiUg_vL0mgVwBvAzwGFF5mIP1Lv1mMchxog?e=RakYIu), [validation](https://entuedu-my.sharepoint.com/:u:/g/personal/junqi_zhao_staff_main_ntu_edu_sg/ERy5kdNAFw1NqmcOT1lFmYEBuHQUrABfMPW7wGj98C9xIw?e=7Lb4fE), [test](https://entuedu-my.sharepoint.com/:u:/g/personal/junqi_zhao_staff_main_ntu_edu_sg/ET0196QSoBlDqqzx8zKxI0oB4gemCAeZk-OgtdtDEv1cWg?e=rnRykM)

## Download annotations 
The annotations for OLIVE can be downloaded here: [train](https://entuedu-my.sharepoint.com/:u:/g/personal/junqi_zhao_staff_main_ntu_edu_sg/Efh_5gWoU-hHgyKlDTCqNtIB6zqD9v61bd8TPtLToLVspQ?e=pwDa1t), [validation](https://entuedu-my.sharepoint.com/:u:/g/personal/junqi_zhao_staff_main_ntu_edu_sg/EayFAOSzPM1Pq-s2K57sd28BD-7kSIn8cy_NG17vUBa5DQ?e=7z5PbP), [test](https://entuedu-my.sharepoint.com/:u:/g/personal/junqi_zhao_staff_main_ntu_edu_sg/EZWwNrjqf31LuYmfPwJwliUB3K7x3kWho2wvlTt0JLALhw?e=wBCZ7f)
