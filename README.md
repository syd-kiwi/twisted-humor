# TwistedHumor Dataset

TwistedHumor is a research dataset for studying regular humor and dark humor in YouTube Shorts. The dataset supports research on short form video, humor understanding, dark humor, audience response, and context aware content moderation.

This repository only shares the dataset files and documentation needed to understand the released data.

## Paper

This dataset accompanies the paper:

**When Jokes Cross the Line: Analyzing Regular Humor and Dark Humor in YouTube Shorts**

## Dataset Overview

TwistedHumor contains 1,211 YouTube Shorts paired with 33,041 related comments. Each video includes platform metadata, transcript text, comments, and human annotations.

The dataset includes labels for:

| Label | Description |
| :-- | :-- |
| `humor_presence` | Whether the video contains humor |
| `humor_type` | Regular humor or dark humor |
| `joke_topic` | Main topic or topics referenced in the joke |
| `rhetorical_device` | Irony, satire, or neither |
| `stand_up` | Whether the video contains stand up comedy |
| `target_category` | Sensitive group or entity referenced by the humor |
| `intensity` | Mild, moderate, or severe dark humor label |

## Dataset Statistics

| Statistic | Value |
| :-- | :-- |
| Total videos | 1,211 |
| Distinct channels | 716 |
| Total comments | 33,041 |
| Humorous videos | 601 |
| Non humorous or ambiguous videos | 610 |
| Regular humor videos | 402 |
| Dark humor videos | 199 |
| Stand up videos | 176 |
| Dark humor stand up videos | 96 |

Among stand up videos, 96 out of 176 were labeled as dark humor, meaning 54.55 percent of stand up posts in the dataset were dark humor.

## Repository Contents

```text
twisted-humor/
│
├── data/
│   ├── twistedhumor.csv
│   ├── comments/
│   └── descriptions/
└── README.md

## Data Files

### `data/twistedhumor.csv`

Main dataset file. Each row corresponds to one YouTube Short.

Expected columns include:

| Column | Description |
| :-- | :-- |
| `video_id` | Unique YouTube video identifier |
| `url` | Direct YouTube video link |
| `title` | Video title |
| `description` | Video description |
| `transcript_text` | Transcript generated from the video audio |
| `channel` | YouTube channel name |
| `channel_id` | YouTube channel identifier |
| `uploader` | Uploader name |
| `uploader_id` | Uploader identifier |
| `upload_date` | Date the video was uploaded |
| `duration` | Video duration |
| `view_count` | Number of views |
| `like_count` | Number of likes |
| `comment_count` | Number of comments |
| `language` | Detected language |
| `searched_keyword` | Keyword used to find the candidate video |
| `humor_presence` | Human label for humor presence |
| `humor_type` | Human label for humor type |
| `joke_topic` | Human label for joke topic |
| `rhetorical_device` | Human label for irony or satire |
| `stand_up` | Human label for stand up comedy |
| `target_category` | Human label for sensitive target category |
| `intensity` | Human label for dark humor intensity |

### `data/comments/`

Contains comment files associated with videos in the dataset. Each file is organized by video ID.

### `data/descriptions/`

Contains original video descriptions organized by video ID.

## Annotation Labels

### Humor Presence

| Label | Meaning |
| :-- | :-- |
| `Humor` | The video contains humor |
| `Not Humor` | The video does not contain humor |
| `Ambiguous` | Humor is unclear or uncertain |

### Humor Type

| Label | Meaning |
| :-- | :-- |
| `Regular Humor` | Humor based on playful, surprising, or socially acceptable topics |
| `Dark Humor` | Humor involving taboo, offensive, sensitive, or morally provocative themes |
| `None of these` | No humor type applies |

### Rhetorical Device

| Label | Meaning |
| :-- | :-- |
| `Irony` | Meaning differs from literal expression |
| `Satire` | Humor critiques a person, system, institution, or social issue |
| `Neither` | No clear irony or satire |

### Target Category

Dark humor videos may include one of the following target categories:

| Target Category |
| :-- |
| `Gender or sex related` |
| `Mental health` |
| `Disability` |
| `Race or ethnicity` |
| `Violence or death` |
| `Other sensitive target` |
| `None` |

### Intensity

| Label | Meaning |
| :-- | :-- |
| `Mild` | Sensitive theme is present but low severity |
| `Moderate` | Sensitive theme is clear and potentially uncomfortable |
| `Severe` | Sensitive theme is highly offensive, harmful, or disturbing |

## Citation

If you use this dataset, please cite:

```bibtex
@misc{johns2026twistedhumor,
  title = {When Jokes Cross the Line: Analyzing Regular Humor and Dark Humor in YouTube Shorts},
  author = {Johns, Sydney and Parthasarathy, Sanjeev and Bhalla, Shantnu and Garg, Vaibhav},
  year = {2026},
  note = {Manuscript submitted to ACM}
}
```
