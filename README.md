# **Task 07: Frequency Domain Filtering with LPF and HPF**

**Roll Number:** 2023-SE-06

### **Prompt**

*"Write a Python program using NumPy, OpenCV, and Matplotlib, fully compatible with Google Colab, to demonstrate Frequency Domain Filtering on a grayscale image. The program should perform the following tasks:

* Allow the user to upload a grayscale image safely in Colab.
* Display the original image.
* Implement Low-Pass Filters (LPF): Ideal, Butterworth, Gaussian.
* Implement High-Pass Filters (HPF) corresponding to each LPF type.
* Apply all filters in the frequency domain using FFT and obtain filtered images using Inverse FFT.
* Include a spatial domain Gaussian blur as a comparison.
* Display all filtered results together in a clear, well-organized layout (LPF, HPF, Spatial Blur).
* Provide a brief analysis explaining: Effects of LPF vs HPF, Differences between Ideal, Butterworth, Gaussian filters, Comparison with spatial filtering.
* Ensure the code is well-commented, error-free, and lab-ready, with proper handling of data types and images in Colab."*

---

## **Objective**

The objective of this task is to explore **frequency domain filtering** by applying **Low-Pass Filters (LPF)** and **High-Pass Filters (HPF)** to a grayscale image, and to compare their effects with **spatial domain Gaussian blur**. This illustrates the differences between Ideal, Butterworth, and Gaussian filters and demonstrates their impact on image details.

---

## **Methodology / Approach**

1. Upload a **grayscale image** in Google Colab using `files.upload()` and display it.
2. Implement **LPF masks**:

   * Ideal LPF (sharp cutoff)
   * Butterworth LPF (smooth transition)
   * Gaussian LPF (smoothest transition)
3. Implement corresponding **HPF masks** by subtracting LPF masks from 1.
4. Apply all masks in the **frequency domain using FFT** and reconstruct the filtered images using Inverse FFT (IFFT).
5. Apply **spatial Gaussian blur** on the original image as a comparison.
6. Display all filtered results in a **well-organized grid layout**, including LPFs, HPFs, and spatial blur.
7. Analyze and compare the effects of each filter type on image details, edges, and smoothness.

---

## **Results / Observations**

* **Low-pass filters (LPF)** remove high-frequency details, resulting in smooth and blurred regions.
* **High-pass filters (HPF)** emphasize edges and fine details, highlighting rapid intensity changes.
* **Ideal filter** has a sharp cutoff and may introduce ringing artifacts.
* **Butterworth filter** provides a smoother frequency transition, reducing artifacts.
* **Gaussian filter** produces the smoothest frequency transition and natural results.
* **Spatial Gaussian blur** achieves smoothing in the spatial domain but does not allow precise frequency control like FFT-based filters.
* Frequency domain filtering provides precise control over which frequency components are retained or removed, offering advantages over basic spatial filters.

---

## **Tools and Libraries Used**

* **Python 3.x**
* **NumPy (np):** FFT, IFFT, and frequency domain operations
* **OpenCV (cv2):** Image reading, grayscale conversion, and spatial Gaussian blur
* **Matplotlib (plt):** Visualization of original and filtered images
* **Google Colab:** Image upload and execution environment

---
