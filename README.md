\# OpenCV Credit Card OCR



A classical computer vision project that recognizes credit card numbers using OpenCV, contour detection, and template matching.



!\[Credit card example](images/credit\_card\_01.png)



\## Features



\- Extracts digit templates from an OCR-A reference image

\- Locates groups of credit card digits using morphology and contour detection

\- Recognizes each digit with template matching

\- Identifies the card type from the first digit

\- Includes five sample images for testing



\## Processing Pipeline



1\. Convert the input image to grayscale

2\. Highlight bright regions with a top-hat operation

3\. Calculate the horizontal Sobel gradient

4\. Connect digit regions with morphological closing

5\. Apply Otsu thresholding

6\. Detect and sort digit groups

7\. Match each digit against the OCR-A templates

8\. Display the recognized number and card type



\## Project Structure



```text

opencv-credit-card-ocr/

├── images/

│   ├── credit\_card\_01.png

│   ├── credit\_card\_02.png

│   ├── credit\_card\_03.png

│   ├── credit\_card\_04.png

│   ├── credit\_card\_05.png

│   └── ocr\_a\_reference.png

├── myutils.py

├── ocr\_template\_match.py

├── requirements.txt

└── README.md

```



\## Installation



```bash

pip install -r requirements.txt

```



\## Usage



```bash

python ocr\_template\_match.py \\

&#x20; --image images/credit\_card\_01.png \\

&#x20; --template images/ocr\_a\_reference.png

```



The program displays each processing stage in an OpenCV window. Press any key to continue to the next stage.



\## Verified Examples



| Image | Recognized Number | Card Type |

|---|---|---|

| `credit\_card\_01.png` | `4000123456789010` | Visa |

| `credit\_card\_02.png` | `4020340002345678` | Visa |

| `credit\_card\_03.png` | `5412751234567890` | MasterCard |

| `credit\_card\_04.png` | `4000123456789010` | Visa |

| `credit\_card\_05.png` | `5476767898765432` | MasterCard |



\## Requirements



\- Python 3

\- OpenCV

\- NumPy

\- imutils



\## Notes



This is an educational project using classical image processing. Recognition works best when the card layout and digit style are similar to the included examples.

