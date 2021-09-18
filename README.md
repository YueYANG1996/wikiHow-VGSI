# wikiHow-VGSI

The dataset and baseline model of EMNLP 2021 paper [Visual Goal-Step Inference using wikiHow](https://arxiv.org/abs/2104.05845).
## Dataset
The dataset is available [here](https://drive.google.com/drive/folders/1hjjcNSUSqv8AbA7R-5lIKmui-ySCEWJw?usp=sharing), it contains the following files:
	
* **wiki_images.zip**: all 770k images {*image_id.png*}
* **WikihowText_data.json**: json file of the textual annotation data, each line has the following structure: 

```
{'file_id': article ID (str, e.g. 10000798),
 'goal': textual goal (str, e.g. 'How to Hang an Ironing Board'),
 'goal_description': description of the goal (str),
 'category_hierarchy': (list of str),
 'methods': [{'name': 'Hanging an Ironing Board Over a Door',
   'steps': [{'headline': 'Find a door to hang your ironing board.',
     'description': (str),
     'img': url of image,
     'img_license': 'Creative Commons',
     'step_id': '10000798_0_0'},
     ...
     ]
  ...
  ]
```
Use the following code to read the json file:

```pythom
import json
articles = []
for line in open("WikihowText_data.json", "r"):
    articles.append(json.loads(line))
```

## Baseline Models
To be released soon.

## Cite
Please cite our work if you think it is useful. Thank you!

```
@article{yang2021visual,
  title={Visual Goal-Step Inference using wikiHow},
  author={Yang, Yue and Panagopoulou, Artemis and Lyu, Qing and Zhang, Li and Yatskar, Mark and Callison-Burch, Chris},
  journal={arXiv preprint arXiv:2104.05845},
  year={2021}
}
```
   
	

