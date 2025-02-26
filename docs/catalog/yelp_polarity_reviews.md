<div itemscope itemtype="http://schema.org/Dataset">
  <div itemscope itemprop="includedInDataCatalog" itemtype="http://schema.org/DataCatalog">
    <meta itemprop="name" content="TensorFlow Datasets" />
  </div>

  <meta itemprop="name" content="yelp_polarity_reviews" />
  <meta itemprop="description" content="Large Yelp Review Dataset.&#10;This is a dataset for binary sentiment classification. We provide a set of 560,000 highly polar yelp reviews for training, and 38,000 for testing. &#10;ORIGIN&#10;The Yelp reviews dataset consists of reviews from Yelp. It is extracted&#10;from the Yelp Dataset Challenge 2015 data. For more information, please&#10;refer to http://www.yelp.com/dataset&#10;&#10;The Yelp reviews polarity dataset is constructed by&#10;Xiang Zhang (xiang.zhang@nyu.edu) from the above dataset.&#10;It is first used as a text classification benchmark in the following paper:&#10;Xiang Zhang, Junbo Zhao, Yann LeCun. Character-level Convolutional Networks&#10;for Text Classification. Advances in Neural Information Processing Systems 28&#10;(NIPS 2015).&#10;&#10;&#10;DESCRIPTION&#10;&#10;The Yelp reviews polarity dataset is constructed by considering stars 1 and 2&#10;negative, and 3 and 4 positive. For each polarity 280,000 training samples and&#10;19,000 testing samples are take randomly. In total there are 560,000 trainig&#10;samples and 38,000 testing samples. Negative polarity is class 1,&#10;and positive class 2.&#10;&#10;The files train.csv and test.csv contain all the training samples as&#10;comma-sparated values. There are 2 columns in them, corresponding to class&#10;index (1 and 2) and review text. The review texts are escaped using double&#10;quotes (&quot;), and any internal double quote is escaped by 2 double quotes (&quot;&quot;).&#10;New lines are escaped by a backslash followed with an &quot;n&quot; character,&#10;that is &quot;&#10;&quot;.&#10;&#10;To use this dataset:&#10;&#10;```python&#10;import tensorflow_datasets as tfds&#10;&#10;ds = tfds.load(&#x27;yelp_polarity_reviews&#x27;, split=&#x27;train&#x27;)&#10;for ex in ds.take(4):&#10;  print(ex)&#10;```&#10;&#10;See [the guide](https://www.tensorflow.org/datasets/overview) for more&#10;informations on [tensorflow_datasets](https://www.tensorflow.org/datasets).&#10;&#10;" />
  <meta itemprop="url" content="https://www.tensorflow.org/datasets/catalog/yelp_polarity_reviews" />
  <meta itemprop="sameAs" content="https://course.fast.ai/datasets" />
  <meta itemprop="citation" content="@article{zhangCharacterlevelConvolutionalNetworks2015,&#10;  archivePrefix = {arXiv},&#10;  eprinttype = {arxiv},&#10;  eprint = {1509.01626},&#10;  primaryClass = {cs},&#10;  title = {Character-Level {{Convolutional Networks}} for {{Text Classification}}},&#10;  abstract = {This article offers an empirical exploration on the use of character-level convolutional networks (ConvNets) for text classification. We constructed several large-scale datasets to show that character-level convolutional networks could achieve state-of-the-art or competitive results. Comparisons are offered against traditional models such as bag of words, n-grams and their TFIDF variants, and deep learning models such as word-based ConvNets and recurrent neural networks.},&#10;  journal = {arXiv:1509.01626 [cs]},&#10;  author = {Zhang, Xiang and Zhao, Junbo and LeCun, Yann},&#10;  month = sep,&#10;  year = {2015},&#10;}" />
</div>

# `yelp_polarity_reviews`

Note: This dataset has been updated since the last stable release. The new
versions and config marked with
<span class="material-icons" title="Available only in the tfds-nightly package">nights_stay</span>
are only available in the `tfds-nightly` package.

*   **Description**:

Large Yelp Review Dataset. This is a dataset for binary sentiment
classification. We provide a set of 560,000 highly polar yelp reviews for
training, and 38,000 for testing. ORIGIN The Yelp reviews dataset consists of
reviews from Yelp. It is extracted from the Yelp Dataset Challenge 2015 data.
For more information, please refer to http://www.yelp.com/dataset

The Yelp reviews polarity dataset is constructed by Xiang Zhang
(xiang.zhang@nyu.edu) from the above dataset. It is first used as a text
classification benchmark in the following paper: Xiang Zhang, Junbo Zhao, Yann
LeCun. Character-level Convolutional Networks for Text Classification. Advances
in Neural Information Processing Systems 28 (NIPS 2015).

DESCRIPTION

The Yelp reviews polarity dataset is constructed by considering stars 1 and 2
negative, and 3 and 4 positive. For each polarity 280,000 training samples and
19,000 testing samples are take randomly. In total there are 560,000 trainig
samples and 38,000 testing samples. Negative polarity is class 1, and positive
class 2.

The files train.csv and test.csv contain all the training samples as
comma-sparated values. There are 2 columns in them, corresponding to class index
(1 and 2) and review text. The review texts are escaped using double quotes ("),
and any internal double quote is escaped by 2 double quotes (""). New lines are
escaped by a backslash followed with an "n" character, that is " ".

*   **Homepage**:
    [https://course.fast.ai/datasets](https://course.fast.ai/datasets)

*   **Source code**:
    [`tfds.text.YelpPolarityReviews`](https://github.com/tensorflow/datasets/tree/master/tensorflow_datasets/text/yelp_polarity.py)

*   **Versions**:

    *   **`0.2.0`** (default): No release notes.

*   **Download size**: `158.67 MiB`

*   **Dataset size**: `435.14 MiB`

*   **Auto-cached**
    ([documentation](https://www.tensorflow.org/datasets/performances#auto-caching)):
    No

*   **Splits**:

Split     | Examples
:-------- | -------:
`'test'`  | 38,000
`'train'` | 560,000

*   **Features**:

```python
FeaturesDict({
    'label': ClassLabel(shape=(), dtype=tf.int64, num_classes=2),
    'text': Text(shape=(), dtype=tf.string),
})
```

*   **Supervised keys** (See
    [`as_supervised` doc](https://www.tensorflow.org/datasets/api_docs/python/tfds/load#args)):
    `('text', 'label')`

*   **Citation**:

```
@article{zhangCharacterlevelConvolutionalNetworks2015,
  archivePrefix = {arXiv},
  eprinttype = {arxiv},
  eprint = {1509.01626},
  primaryClass = {cs},
  title = {Character-Level {{Convolutional Networks}} for {{Text Classification}}},
  abstract = {This article offers an empirical exploration on the use of character-level convolutional networks (ConvNets) for text classification. We constructed several large-scale datasets to show that character-level convolutional networks could achieve state-of-the-art or competitive results. Comparisons are offered against traditional models such as bag of words, n-grams and their TFIDF variants, and deep learning models such as word-based ConvNets and recurrent neural networks.},
  journal = {arXiv:1509.01626 [cs]},
  author = {Zhang, Xiang and Zhao, Junbo and LeCun, Yann},
  month = sep,
  year = {2015},
}
```

*   **Figure**
    ([tfds.show_examples](https://www.tensorflow.org/datasets/api_docs/python/tfds/visualization/show_examples)):
    Not supported.

*   **Examples**
    ([tfds.as_dataframe](https://www.tensorflow.org/datasets/api_docs/python/tfds/as_dataframe)):
    Missing.
