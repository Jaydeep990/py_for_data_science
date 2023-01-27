# **20 Python Project**

| **No** |            **Name**             | **Information** | **Project Link** |
| :----: | :-----------------------------: | --------------- | ---------------- |
| **1**  |        **Email Sender**         |                 |                  |
| **2**  |  **Word Replacement Program**   |                 |                  |
| **3**  |      **Basic Calculator**       |                 |                  |
| **4**  |        **Email Slicer**         |                 |                  |
| **5**  |   **Binary Search Algorithm**   |                 |                  |
| **6**  |        **Quiz Program**         |                 |                  |
| **7**  |      **QR Code Generator**      |                 |                  |
| **8**  | **Interest Payment Calculator** |                 |                  |
| **9**  |  **Random Password Generator**  |                 |                  |
| **10** |   **Dice Rolling Simulator**    |                 |                  |
| **11** |  **Site Connectivity Checker**  |                 |                  |
| **12** |     **Currency Converter**      |                 |                  |
| **13** |      **Leap Year Checker**      |                 |                  |
| **14** |       **Word Dictionary**       |                 |                  |
| **15** |    **Rock, Paper, Scissors**    |                 |                  |
| **16** |    **Python Face Detection**    |                 |                  |
| **17** |      **Python Automation**      |                 |                  |
| **18** |         **Web Scraper**         |                 |                  |
| **19** |        **Image Resizer**        |                 |                  |
| **20** |        **Graph Plotter**        |                 |                  |

## **1. Email Sender**

<!-- info -->

> Step I follow to build this `Email Sender`.

1. Go over to your gmail account and setup 2 factor authentication.

2. Generate app password from your google account's security section. [google account security section link](https://myaccount.google.com/security)

3. Crate a function to send the mail.

> **I used `EmailMessage` class, `ssl` module and `smtplib` module.**

```python
from email.message import EmailMessage
import ssl
import smtplib
```

### **EmailMessage**

Python has EmailMessage class which can be used build email messages. This class has the required methods to customize different parts of the email message like - the TO and FROM tags, the Subject Line as well as the content of the email.

### **ssl**

This module provides access to Transport Layer Security (often known as “Secure Sockets Layer”) encryption and peer authentication facilities for network sockets, both client-side and server-side.

### **smtplib**

The smtplib module defines an SMTP client session object that can be used to send mail to any internet machine with an SMTP or ESMTP listener daemon. For details of SMTP and ESMTP operation, consult RFC 821 (Simple Mail Transfer Protocol) and RFC 1869 (SMTP Service Extensions).

## **2. Word Replacement Program**

<!-- info -->

> Step I follow to build this `Word Replacement Program`.

1. I build a `replce_word()` function to run the word replacement program.

2. I used `replace()` method to replaces a specified phrase with another specified phrase.

## **3. Basic Calculator**

<!-- info -->

> Step I follow to build this `Basic Calculator`.

1. Define a four function to calculate a certain operation on two numbers.

   - `add()` -> Additon
   - `sub()` -> Substraction
   - `mul()` -> Multiplication
   - `div()` -> Division

2. Define infinte while loop to take input from user to perform basic calculation.

3. If user give `E` as a input then program end.

### **4. Email Slicer**

<!-- info -->

> Step I follow to build this `Email Slicer`.

1. I build a `slicer()` function to run the `Email Slicer`.

2. I used `split()` method to split the string.

3. Show the Username, Domain and Extension.

### **5. Binary Search Algorithm**

<!-- info -->

> Step I follow to build this `Binary Search Algorithm`.

1. Set the start index to the first element of the list and the end index to the last element.
2. Set the middle index to the average of the start and end indices.
3. If the element at the middle index is the target element, return the middle index.
4. If the target element is less than the element at the middle index, set the end index to the middle index – 1.
5. If the target element is greater than the element at the middle index, set the start index to the middle index + 1.
6. Repeat steps 3-6 until the element is found or it is clear that the element is not present in the list.

### **6. Quiz Program**

<!-- info -->

> Step I follow to build this `Quiz Program`.

1. I creat a `quiz`, it is a dictionary of questions.

2. I creat a `test()` function to conduct test.

3. I creat a `show_result()` function to show the result.

### **7. QR Code Generator**

<!-- info -->

#### What is a QR Code?

A Quick Response code is a two-dimensional pictographic code used for its fast readability and comparatively large storage capacity. The code consists of black modules arranged in a square pattern on a white background. The information encoded can be made up of any kind of data (e.g., binary, alphanumeric, or Kanji symbols)

> Step I follow to build this `QR Code Generator`.

1. I have to install two library `qrcode` and `Image`.

2. I create a `generate_qrcode` function which generate QR code and save it as a image.

### **qrcode**

QR Code image generator

### **Image**

Django application that provides cropping, resizing, thumbnailing, overlays and masking for images and videos with the ability to set the center of attention,
