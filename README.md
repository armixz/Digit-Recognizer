# Digit Recognizer
![MNIST](/42K-Digit.png)

## Competition Description
MNIST ("Modified National Institute of Standards and Technology") is the de facto “hello world” dataset of computer vision. Since its release in 1999, this classic dataset of handwritten images has served as the basis for benchmarking classification algorithms. As new machine learning techniques emerge, MNIST remains a reliable resource for researchers and learners alike.<br/><br/>
In this competition, your goal is to correctly identify digits from a dataset of tens of thousands of handwritten images. We’ve curated a set of tutorial-style kernels which cover everything from regression to neural networks. We encourage you to experiment with different algorithms to learn first-hand what works well and how techniques compare.
<br/>

## Data Description

- The data files **_train.csv_** and **_test.csv_** contain gray-scale images of hand-drawn digits, from zero through nine.
- Each image is 28 pixels in height and 28 pixels in width, for a total of 784 pixels in total. 
- Each pixel has a single pixel-value associated with it, 
  - indicating the lightness or darkness of that pixel, with higher number meaning darker. 
- This pixel-value is an integer between 0 and 255, inclusive.

<br/>

- The training data set, _(train.csv)_, has 785 columns. 
  - The first column, called **"label"**, is the digit that was drawn by the user. 
  - The rest of the columns contain the pixel-values of the associated image.
  - Each pixel column in the training set has a name like **_pixelx_**, where x is an integer between 0 and 783. 
  - To locate this pixel on the image, suppose that we have decomposed x as x = i * 28 + j | [i,j] ⊂ [0,...,27]. 
  - Then pixelx is located on row i and column j of a 28 x 28 matrix, (indexing by zero).
<br/>

For example, _pixel31_ indicates the pixel that is in the fourth column from the left, and second row from the top, as in the ascii-diagram below.
<br/>

---

Visually, if we omit the **_"pixel"_** prefix, the pixels make up the image like this:
<br/>

```
000 001 002 003 ... 026 027
028 029 030 031 ... 054 055
056 057 058 059 ... 082 083
 |   |   |   |  ...  |   |
728 729 730 731 ... 754 755
756 757 758 759 ... 782 783 
The test data set, (test.csv), is the same as the training set, except that it does not contain the "label" column.
```

---

<br/>
Your submission file should be in the following format: 
- For each of the 28000 images in the **_test_** set, output a single line containing the **_ImageId_** and the **_digit_** you predict. 
- For example, if you predict that the first image is of a 3, the second image is of a 7, and the third image is of a 8, then your submission file would look like:
<br/>
<br/>

```
ImageId,Label
1,3
2,7
3,8 
(27997 more lines)
```
<br/>
The evaluation metric for this contest is the categorization accuracy, or the proportion of test images that are correctly classified. For example, a categorization accuracy of 0.97 indicates that you have correctly classified all but 3% of the images.
