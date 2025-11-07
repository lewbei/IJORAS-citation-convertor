# IJORAS Reference Examples

This document contains example references for various types of academic sources to help you format your citations correctly using the IJORAS Citation Converter.

## Table of Contents

1. [Journal Articles](#journal-articles)
2. [Conference Papers](#conference-papers)
3. [Books](#books)
4. [Book Chapters](#book-chapters)
5. [Theses and Dissertations](#theses-and-dissertations)
6. [Patents](#patents)
7. [Technical Reports](#technical-reports)
8. [Standards](#standards)
9. [Websites and Online Resources](#websites-and-online-resources)
10. [Preprints (arXiv, bioRxiv)](#preprints)

---

## Journal Articles

### Example 1: Standard Journal Article

**Input:**
```
W. C. Fang, K. Y. Wang, N. Fahier, Y. L. Ho, and Y. D. Huang, "Development and validation of an EEG-based real-time emotion recognition system using edge AI computing platform with convolutional neural network system-on-chip design," IEEE Journal on Emerging and Selected Topics in Circuits and Systems, vol. 9, no. 4, pp. 693-702, December 2019. DOI: 10.1109/JETCAS.2019.2951232
```

**Expected Output:**
```
[1]	W. C. Fang, K. Y. Wang, N. Fahier, Y. L. Ho and Y. D. Huang, "Development and validation
	of an EEG-based real-time emotion recognition system using edge AI computing platform
	with convolutional neural network system-on-chip design," *IEEE Journal on Emerging and
	Selected Topics in Circuits and Systems*, vol. 9, no. 4, pp. 693-702, 2019.
	DOI: https://doi.org/10.1109/JETCAS.2019.2951232
```

### Example 2: Journal Article with Many Authors

**Input:**
```
J. Smith, K. Jones, L. Brown, M. Davis, R. Wilson, S. Miller, T. Moore, and A. Taylor, "Machine learning approaches for pattern recognition in biomedical signals," IEEE Transactions on Biomedical Engineering, vol. 67, no. 3, pp. 445-459, 2020. DOI: 10.1109/TBME.2020.123456
```

**Expected Output:**
```
[1]	J. Smith, K. Jones, L. Brown, M. Davis, R. Wilson, S. Miller, T. Moore and A. Taylor,
	"Machine learning approaches for pattern recognition in biomedical signals," *IEEE
	Transactions on Biomedical Engineering*, vol. 67, no. 3, pp. 445-459, 2020.
	DOI: https://doi.org/10.1109/TBME.2020.123456
```

### Example 3: Journal Article - Single Author

**Input:**
```
A. M. Turing, "Computing machinery and intelligence," Mind, vol. 59, no. 236, pp. 433-460, 1950.
```

**Expected Output:**
```
[1]	A. M. Turing, "Computing machinery and intelligence," *Mind*, vol. 59, no. 236,
	pp. 433-460, 1950.
```

---

## Conference Papers

### Example 1: Standard Conference Paper

**Input:**
```
K. He, X. Zhang, S. Ren, and J. Sun, "Deep residual learning for image recognition," Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition (CVPR), pp. 770-778, 2016. DOI: 10.1109/CVPR.2016.90
```

**Expected Output:**
```
[1]	K. He, X. Zhang, S. Ren and J. Sun, "Deep residual learning for image recognition,"
	*Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition (CVPR)*,
	pp. 770-778, 2016.
	DOI: https://doi.org/10.1109/CVPR.2016.90
```

### Example 2: Conference Paper with Location

**Input:**
```
A. Vaswani, N. Shazeer, N. Parmar, J. Uszkoreit, L. Jones, A. N. Gomez, L. Kaiser, and I. Polosukhin, "Attention is all you need," Proceedings of the 31st International Conference on Neural Information Processing Systems (NIPS), Long Beach, CA, USA, pp. 6000-6010, 2017.
```

**Expected Output:**
```
[1]	A. Vaswani, N. Shazeer, N. Parmar, J. Uszkoreit, L. Jones, A. N. Gomez, L. Kaiser and
	I. Polosukhin, "Attention is all you need," *Proceedings of the 31st International
	Conference on Neural Information Processing Systems (NIPS)*, Long Beach, CA, USA,
	pp. 6000-6010, 2017.
```

---

## Books

### Example 1: Entire Book

**Input:**
```
I. Goodfellow, Y. Bengio, and A. Courville, Deep Learning, MIT Press, 2016.
```

**Expected Output:**
```
[1]	I. Goodfellow, Y. Bengio and A. Courville, *Deep Learning*, MIT Press, 2016.
```

### Example 2: Book with Edition

**Input:**
```
S. Russell and P. Norvig, Artificial Intelligence: A Modern Approach, 4th ed., Pearson, 2020.
```

**Expected Output:**
```
[1]	S. Russell and P. Norvig, *Artificial Intelligence: A Modern Approach*, 4th ed.,
	Pearson, 2020.
```

### Example 3: Book with Multiple Editions and Page Range

**Input:**
```
D. E. Knuth, The Art of Computer Programming, Vol. 1: Fundamental Algorithms, 3rd ed., Addison-Wesley, pp. 1-650, 1997.
```

**Expected Output:**
```
[1]	D. E. Knuth, *The Art of Computer Programming, Vol. 1: Fundamental Algorithms*, 3rd ed.,
	Addison-Wesley, pp. 1-650, 1997.
```

---

## Book Chapters

### Example 1: Chapter in Edited Book

**Input:**
```
G. O. Young, "Synthetic structure of industrial plastics," in Plastics, 2nd ed., J. Peters, Ed. New York: McGraw-Hill, 1964, pp. 15-64.
```

**Expected Output:**
```
[1]	G. O. Young, "Synthetic structure of industrial plastics," in *Plastics*, 2nd ed.,
	J. Peters, Ed. New York: McGraw-Hill, pp. 15-64, 1964.
```

### Example 2: Chapter with Multiple Editors

**Input:**
```
M. Thompson, "Neural network architectures," in Handbook of Machine Learning, vol. 2, A. Smith and B. Johnson, Eds., Springer, pp. 120-145, 2019.
```

**Expected Output:**
```
[1]	M. Thompson, "Neural network architectures," in *Handbook of Machine Learning*, vol. 2,
	A. Smith and B. Johnson, Eds., Springer, pp. 120-145, 2019.
```

---

## Theses and Dissertations

### Example 1: PhD Dissertation

**Input:**
```
S. M. Brown, "Advanced techniques in deep reinforcement learning," Ph.D. dissertation, Dept. Computer Science, Stanford University, Stanford, CA, 2021.
```

**Expected Output:**
```
[1]	S. M. Brown, "Advanced techniques in deep reinforcement learning," Ph.D. dissertation,
	Dept. Computer Science, Stanford University, Stanford, CA, 2021.
```

### Example 2: Master's Thesis

**Input:**
```
J. Williams, "Real-time object detection using convolutional neural networks," M.S. thesis, Massachusetts Institute of Technology, Cambridge, MA, 2020.
```

**Expected Output:**
```
[1]	J. Williams, "Real-time object detection using convolutional neural networks," M.S. thesis,
	Massachusetts Institute of Technology, Cambridge, MA, 2020.
```

---

## Patents

### Example 1: US Patent

**Input:**
```
J. P. Inventor and A. B. Co-Inventor, "Method and apparatus for neural network processing," U.S. Patent 10,123,456, Nov. 12, 2019.
```

**Expected Output:**
```
[1]	J. P. Inventor and A. B. Co-Inventor, "Method and apparatus for neural network processing,"
	U.S. Patent 10,123,456, Nov. 12, 2019.
```

### Example 2: International Patent

**Input:**
```
M. Schmidt, "System for autonomous vehicle navigation," European Patent EP 3,456,789, filed Mar. 15, 2018.
```

**Expected Output:**
```
[1]	M. Schmidt, "System for autonomous vehicle navigation," European Patent EP 3,456,789,
	filed Mar. 15, 2018.
```

---

## Technical Reports

### Example 1: Technical Report

**Input:**
```
D. Johnson, "Performance analysis of distributed computing systems," Tech. Rep. TR-2020-45, Computer Science Department, University of California, Berkeley, 2020.
```

**Expected Output:**
```
[1]	D. Johnson, "Performance analysis of distributed computing systems," Tech. Rep. TR-2020-45,
	Computer Science Department, University of California, Berkeley, 2020.
```

### Example 2: Technical Report with DOI

**Input:**
```
L. Anderson and M. Roberts, "Energy-efficient algorithms for IoT devices," NIST Tech. Rep. NIST-TR-8325, National Institute of Standards and Technology, 2021. DOI: 10.6028/NIST.TR.8325
```

**Expected Output:**
```
[1]	L. Anderson and M. Roberts, "Energy-efficient algorithms for IoT devices," NIST Tech. Rep.
	NIST-TR-8325, National Institute of Standards and Technology, 2021.
	DOI: https://doi.org/10.6028/NIST.TR.8325
```

---

## Standards

### Example 1: IEEE Standard

**Input:**
```
IEEE Standard for Floating-Point Arithmetic, IEEE Std 754-2019, 2019.
```

**Expected Output:**
```
[1]	*IEEE Standard for Floating-Point Arithmetic*, IEEE Std 754-2019, 2019.
```

### Example 2: ISO Standard

**Input:**
```
Information technology - Programming languages - C++, ISO/IEC 14882:2020, International Organization for Standardization, 2020.
```

**Expected Output:**
```
[1]	*Information technology - Programming languages - C++*, ISO/IEC 14882:2020,
	International Organization for Standardization, 2020.
```

---

## Websites and Online Resources

### Example 1: Website with Author

**Input:**
```
J. Doe, "Introduction to machine learning," Google AI Blog, 2021. [Online]. Available: https://ai.googleblog.com/2021/intro-ml
```

**Expected Output:**
```
[1]	J. Doe, "Introduction to machine learning," *Google AI Blog*, 2021. [Online].
	Available: https://ai.googleblog.com/2021/intro-ml
```

### Example 2: Website without Author

**Input:**
```
"TensorFlow: An end-to-end open source machine learning platform," TensorFlow.org. [Online]. Available: https://www.tensorflow.org. Accessed: Jan. 15, 2024.
```

**Expected Output:**
```
[1]	"TensorFlow: An end-to-end open source machine learning platform," *TensorFlow.org*.
	[Online]. Available: https://www.tensorflow.org. Accessed: Jan. 15, 2024.
```

---

## Preprints

### Example 1: arXiv Preprint

**Input:**
```
A. Dosovitskiy, L. Beyer, A. Kolesnikov, et al., "An image is worth 16x16 words: Transformers for image recognition at scale," arXiv:2010.11929, 2020.
```

**Expected Output:**
```
[1]	A. Dosovitskiy, L. Beyer, A. Kolesnikov, et al., "An image is worth 16x16 words:
	Transformers for image recognition at scale," 2020.
	DOI: https://doi.org/10.48550/arXiv.2010.11929
```

### Example 2: bioRxiv Preprint

**Input:**
```
M. Chen, J. Tworek, H. Jun, et al., "Evaluating large language models trained on code," bioRxiv preprint, 2021. DOI: 10.1101/2021.07.09.451642
```

**Expected Output:**
```
[1]	M. Chen, J. Tworek, H. Jun, et al., "Evaluating large language models trained on code,"
	bioRxiv preprint, 2021.
	DOI: https://doi.org/10.1101/2021.07.09.451642
```

---

## Tips for Best Results

1. **Include DOIs when available** - They help verify and link to the source
2. **List all authors** - IJORAS style requires full author lists (no "et al." in reference list)
3. **Use consistent formatting** - The AI works best with consistent input
4. **Verify output** - Always review the converted references for accuracy
5. **Provide volume/issue/pages** - Include all available publication details
6. **Use standard abbreviations** - Follow IEEE abbreviation standards for journals

---

## Testing Your References

Paste any of these examples into the IJORAS Citation Converter to see how they're formatted. You can also use them as templates for your own references.

## Need Help?

If you have questions about formatting specific types of references:

1. Check the [IJORAS style guide](https://ijoras.com/author-guidelines) (if available)
2. Look at published IJORAS articles for examples
3. Open an issue on GitHub with your specific question
4. Consult the IEEE Editorial Style Manual for technical publications

---

**Last Updated:** 2025
**Version:** 2.0
