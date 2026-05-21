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
