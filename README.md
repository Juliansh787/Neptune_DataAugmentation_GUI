# Neptune 3.0 (Data Augmentation Tool)

This tool convert png file to jpg file not only change name but also file format completely.
And this will help you change jpg Data set files name to recognize easily. Additionally you can choose many kind of noise options for data augmentation with txt file(for making yolo weight file)

# Change file name and .png to .jpg
First click Load button, and load png or jpg files to use Data set for DL.
And then write Target Name you want to change (e.g. hammer, 망치...)
If you choose Raw Data in Design Method then just you can change file name.
Finally Press Start Button. 
And if there is .txt file having same name with target png(jpg) file, then copy that conveted txt file at the same time in ./result path. But txt file SHOLUD BE EXISTS in same target image file path

When you want to reset current configuration, press reset button.

# Convert grayscale image, Rotate and Salt & Pepper noise
If you choose Gray Scale in Design Method then convert color image files to gray scale.
When you want to rotate images then write dgree on Rotate textbox.
And make Salt & Pepper noise in image by checking Salt Pepper check box.
If you use rotate or filep function, then it saves rotated txt file as well based on original label txt file.

# Bluring
This tool provide 5 knids of method
1. Convolution
2. Averaging Blurring
3. Gaussian Blurring
4. Median Blurring
5. Bilateral Filtering

# Image Quality (file size)
You can change image quality by using opencv method

# Nonlinear Mapping
Insert Nonlinear Mapping Effect

# Lens Distortion
Distort image with Lens Distortion effect

# Flip Image
It supports Horizontal Flip, Vertical Flip, Vertical & Horizontal Flip. And tool makes modified labeled txt file. 

# Contrast
You can set Contrast of images by using Histogram Stretching, Histogram Equalization, CLAHE.

# save format
./result/'targetName'_'i'.jpg

# Make exe
pyinstaller --noconsole --add-binary "neptune.png";"." --add-binary "jpgConverter.ui";"." --add-binary "sampleOriginal.jpg";"." --add-binary "sampleResult.jpg";"." --onefile --icon=../icons/neptune.ico "Neptune(DataAugmentation).py"

# icon, png
icon from https://icon-icons.com/ko/, and sampleOriginal.jpg has been taken by me
