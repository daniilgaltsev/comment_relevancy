# Comment "Relevancy" Classifier
This is a small project to test out using synthetic data from LLMs for training machine learning models.

The data was generated to include function definitions, some lines of context around comments and explanations for comment "correctness". The prompts included "backstories" to facilitate more diversity.
The model was finetuned from the new-at-the-time ModernBert with some minor manual hyperparameter search.

A simplistic demo is developed using gradio. It doesn't do proper code parsing and just does an ok-ish job of getting comments (doesn't support multiline comments) and function definitions.

For the future there is quite a few things that can still be done:
- First of all, getting a real evaluation set, but it needs to come from "closed" sources since LLMs were almost definitely trained on any "open" source
- Coming up with a better way to include surrounding context for evaluating comment relevancy
- Looking at mispredictions to find weakspots
- Figuring out how to increase recall / lowering false negatives
- and a lot of other things that can be done but would be a bit tiresome to write out, so it's left as an exercise for all future readers...

## Links To Stuff on HuggingFace

- [Synthetic dataset](https://huggingface.co/datasets/DanGalt/code-comment-synthetic)
- [Final model](https://huggingface.co/DanGalt/modernbert-code-comrel-synthetic)
- [Demo (that worked at some point and might still be working)](https://huggingface.co/spaces/DanGalt/code-comment-correctness-demo)
