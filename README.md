# [EditVid-QA Dataset](https://arxiv.org/pdf/2406.10484v1)
[![CC BY-NC 4.0][cc-by-nc-shield]][cc-by-nc]

[Beyond Raw Videos: Understanding Edited Videos
with Large Multimodal Model](https://arxiv.org/pdf/2406.10484v1):
```
@article{xu2024beyond,
  title={Beyond Raw Videos: Understanding Edited Videos with Large Multimodal Model},
  author={Xu, Lu and Zhu, Sijie and Li, Chunyuan and Kuo, Chia-Wen and Chen, Fan and Wang, Xinyao and Chen, Guang and Du, Dawei and Yuan, Ye and Wen, Longyin},
  journal={arXiv preprint arXiv:2406.10484},
  year={2024}
}
```

## Data Preparation

### Parse and Download public videos for EditVid-QA-Funny/Meme/Game 
Funny/Meme/Game videos can be downloaded from TikTok publicly. In each test sample of the test_qa json, the `video_name` field is defined in `<tiktok_video_id>.mp4` format. To form the public URL of the corresponding video, simply concatenate as
```
https://www.tiktok.com/@default/video/<tiktok_video_id>
```

To download in batch, you can first install the download tool following [tiktok-downloader](https://github.com/n0l3r/tiktok-downloader/tree/main/cli), then run [download_tt.sh](https://github.com/XenonLamb/EditVid-QA/blob/main/download_tt.sh).
### Download edited videos for EditVid-QA-Edit
Edited Videos can be downloaded from [Google Drive](https://drive.google.com/drive/folders/1jV_dKIgeh-sJTn-RnsdcgUiErZ2be-c8?usp=sharing)

## Evaluation
We provide an example python script for evaluating model predictions on EditVid-QA in MSVD-QA style. For example, you can evaluate by
```
python3 eval_editvid_qa.py \
 --pred_path <your directory to predictions> \
 --output_dir <directory for storing judge results> \
 --output_json <path to save aggregated result json> \
 --num_tasks <number of parallel tasks> \
 --num_chunks <num of splits> \
 --use_gpt4 <True/False> \
 --api_key <Your OpenAI key> \
 --api_base <OpenAI api_base> | tee <path to save evaluation log>

```

## Usage Terms
This work is licensed under a
[Creative Commons Attribution-NonCommercial 4.0 International License][cc-by-nc].

[![CC BY-NC 4.0][cc-by-nc-image]][cc-by-nc]

[cc-by-nc]: https://creativecommons.org/licenses/by-nc/4.0/
[cc-by-nc-image]: https://licensebuttons.net/l/by-nc/4.0/88x31.png
[cc-by-nc-shield]: https://img.shields.io/badge/License-CC%20BY--NC%204.0-lightgrey.svg


## Disclaimer
Your access to and use of this dataset are at your own risk. We do not guarantee the accuracy of this dataset. The dataset is provided "as is" and we make no warranty or representation to you with respect to it and we expressly disclaim, and hereby expressly waive, all warranties, express, implied, statutory or otherwise. This includes, without limitation, warranties of quality, performance, merchantability or fitness for a particular purpose, non-infringement, absence of latent or other defects, accuracy, or the presence or absence of errors, whether or not known or discoverable.

In no event will we be liable to you on any legal theory (including, without limitation, negligence) or otherwise for any direct, special, indirect, incidental, consequential, punitive, exemplary, or other losses, coset, expenses, or damages arising out of this public license or use of the licensed material.

The disclaimer of warranties and limitation of liability probided above shall be interpreted in a manner that, to the extent possible, most closely approximates an absolute disclaimer of all liability.

