# ELF24: Human Preference-Aligned Counter Trolling Dataset

## Overview

ELF24 is a dataset designed for studying human-preferred counter-response strategies in Reddit discussions. The dataset contains annotated posts and comments from various subreddits, including various type of trolling attempts and multiple response strategies. You can read our paper ["Towards Effective Counter-Responses: Aligning Human Preferences with Strategies to Combat Online Trolling"](https://arxiv.org/pdf/2410.04164) published in the Findings of EMNLP 2024.

## Dataset Structure

The dataset is located in the data directory and consists of three files:

`train.tsv`: 875 labeled instances (with Trolling Strategy and Response Strategy annotations)

`test.tsv`: 50 labeled instances (with Trolling Strategy and Response Strategy annotations)

`total.tsv`: a total of 1,189 instances, including non-troll examples

## Fields

Each row in the dataset contains the following fields:

| Field | Type | Description |
|-------|------|-------------|
| `Category` | str | The category of the post |
| `Subreddit` | str | The subreddit name |
| `Title` | str | The title of the post |
| `Post` | str | The body text of the original post |
| `Comment` | str | The root comment that potentially contains trolling |
| `TrollingCategory` | int | 1: Overt troll, 2: Covert troll |
| `TrollingStrategy` | int | 0: Non-troll, 1-6: Trolling strategies (refer to paper for details) |
| `TSReason` | int | The reason for the trolling strategy label (refer to Table 3 in our paper) |
| `ResponseCategory` | int | 1: Nudging, 2: Confrontational |
| `MostPreferredRS` | int | The most preferred response strategy |
| `LeastPreferredRS` | int | The least preferred response strategy |
| `RS1` to `RS7` | str | The model-generated response for each response strategy |
| `FlagTS` | str | Flag for trolling strategy |
| `FlagTroll` | str | Flag for troll identification |
| `ChosenFlagRS` | str | Chosen flag for response strategy |
| `RejectFlagRS` | str | Rejected flag for response strategy |
| `ChosenResponse` | str | The response corresponding to the most preferred strategy |
| `RejectResponse` | str | The response corresponding to the least preferred strategy |

## Citation

If you use this dataset in your research, please cite our paper:

```
@article{lee2024towards,
  title={Towards Effective Counter-Responses: Aligning Human Preferences with Strategies to Combat Online Trolling},
  author={Lee, Huije and Song, Hoyun and Shin, Jisu and Cho, Sukmin and Han, SeungYoon and Park, Jong C},
  journal={arXiv preprint arXiv:2410.04164},
  year={2024}
}
```
Note: This citation will be replaced with the ACL Anthology format once it becomes available.

## License

These resources are licensed under a <a rel="license" href="https://creativecommons.org/licenses/by-nc-sa/4.0/">Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License</a>.

<a rel="license" href="https://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png" /></a><br />
