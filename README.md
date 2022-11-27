# Multi-VQG: Generating Engaging Questions for Multiple Images

MVQG is the dataset of EMNLP 2022 long paper "[MultiVQG: Generating Engaging Questions for Multiple Images](https://arxiv.org/abs/2211.07441)." This dataset is collected to enhance the ability of visual-and-language (VL) models to generate engaging questions for image sequences. We sampled the image sequences from the VIST dataset [1], and collected engaging questions corresponding to these image sequences via Amazon Mechanical Turk.

## Data Structure

We split MVQG dataset into `train`, `val`, and `test` set. Each set is formed as a json file with the structure shown below.

```
{
    [key of the 1st image sequence]: [
        {
            "Summary": "...",
            "Question": "..."
        },
        ...
    ],
    [key of the 2nd image sequence]: [],
    ...
}
```
The key of each image sequence is consisted of five numbers concatenated with "_". Each number is the image id in the VIST dataset. You can download the images from [here](https://visionandlanguage.net/VIST/dataset.html).

Each image sequence has 2 to 5 data points. Every data point include a summary and an engaging question written by workers from Amazon Mechanical Turk.

[1]: Ting-Hao (Kenneth) Huang et al., "[Visual Storytelling](https://arxiv.org/abs/1604.03968)", Proceedings of the 2016 Conference of the North American Chapter of the Association for Computational Linguistics (NAACL 2016)