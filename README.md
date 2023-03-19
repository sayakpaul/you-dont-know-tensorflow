# You don't know TensorFlow

Contains materials for my talk "You don't know TensorFlow".

In this talk, I present some under-appreciated and under-used features
of TensorFlow. I focus on two things: **(1)** handling variable-length sequences
in TensorFlow and **(2)** XLA. 

**⚠️Disclaimer 1 ⚠️**: Please note that it's my observation that I have found the usage of these two things to be poorer than expected. Someone else may have other findings, and I don't have any immediate conflicts with those.  

**⚠️Disclaimer 2 ⚠️**: The title of this talk is meant to be humorous and is NOT so to hurt anyone’s sentiments. 

## Notebooks

* `notebooks/variable_length_sequences.ipynb`: Shows how to use [`padded_batch()`](https://www.tensorflow.org/api_docs/python/tf/data/Dataset#padded_batch) to handle variable-length sequences.
* `notebooks/xla_surgery.ipynb`: Shows some explorative interactions with `tf.function` with `jit_compile` enabled.

Additionally, for XLA, I use [this Colab Notebook](https://colab.research.google.com/github/huggingface/blog/blob/main/notebooks/91_tf_xla_generate.ipynb) to demonstrate how XLA can speed up text generation in TensorFlow by 100x.  

## Slides

[Link](https://docs.google.com/presentation/d/1USj_B0KCvxwJDGnDs2hhXMC70AV2Kmk5NJ-h9XC1duQ/edit?usp=sharing)

## Notes

In the interest of time, I may not be able to even scratch the surface of XLA. I suggest
going through the following resources in case XLA in TensorFlow interests you:

* [Official documentation](https://www.tensorflow.org/xla)
* [Faster Text Generation with TensorFlow and XLA](https://huggingface.co/blog/tf-xla-generate)
* [XLA Integration for TensorFlow Models](https://huggingface.co/docs/transformers/tf_xla)

## Not covered in the Slides

But I wanted to cover: 

* Exporting TensorFlow SavedModels for deployment ([example](https://huggingface.co/blog/tf-serving-vision))
  * How should you export your SavedModels for deployment?
  * Model surgery 
  * TF Serving
* Taking advantage of TensorRT to speedup inference ([example](https://huggingface.co/spaces/sayakpaul/tensorrt-tf))
