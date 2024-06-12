# EditVid-QA Dataset
[![CC BY-NC 4.0][cc-by-nc-shield]][cc-by-nc]

## Data Preparation
### Parse and Download public videos for EditVid-QA-Funny/Meme/Game 
Funny/Meme/Game videos can be downloaded from TikTok publicly. In each test sample of the test_qa json, the `video_name` field is defined in `<tiktok_video_id>.mp4` format. To form the public URL of the corresponding video, simply concatenate as
```
https://www.tiktok.com/@default/video/<tiktok_video_id>
```
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
