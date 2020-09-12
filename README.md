# Slide Reading System Evaluation Protocol
Slide presentations have been successfully used for an efficient and effective way of classroom teaching in the last three decades. However, blind and visually impaired (VI) students are not benefited by this way of teaching due to their limitation in reading slides. This shortcoming motivates us to design a system which can generate audio sound corresponding to the reading order of each slide and can help the blind and VI students to understand and interpret the content of the slides. 
## Technical aspects
This problem is posed as an image-to-markup language generation task. Extraction of meaningful regions like title, paragraph, list, equation, figure, table, etc from the slide image is the initial step. Due to the diversity of content, theme and layout of the slides, extraction of meaningful regions is a challenging task. We present an classroom slide narration system based on the semantic segmentation of classroom slide image. Here, we pose the extraction of meaningful regions as a pixel-wise classification task which is closely related to natural image semantic segmentation task in computer vision. 
We uses the recently published dataset of classroom slides to demonstrate our results. We improve the classroom segmentation accuracy using synthetic classroom slide and its automatically generated groundtruth.  We also used unlabelled classroom slide images to improve the segmentation accuracy.

## How to evaluate the system?

### Step1:
Open the list of slide images [here](http://10.2.16.142/cgi-bin/vi_project/list_slide.sh)
![table](tableLists1.jpg)<br/>
The list contains 332 slide images.
Each image has four outputs links given under the title of GT, PSP, DeepLab, and tesseract. The column titled "Table" indicates whether the slide image contains a table or not.<br/>
#### Each evaluator can randomly choose a minimum of 5 slide images and evaluate all the outputs corresponds to those images.
Eg: if you chose the image name "130110-DKLK0EGEYA-540_frame1770.jpg", then you suppose to evaluate all the outputs correspond to that image. (red marked boxes) 

### Step2: Evaluate the output
We have four different outputs for a slide image. We request you to evaluate the efficiency of these outputs for conveying the slide content to a visually impaired student. Our system have two modes of output 1) Interactive and 2) non-interactive modes.
#### Open the output links [eg link](http://10.2.16.142/cgi-bin/vi_project/read_slide.sh?p=vi_deeplab&k=130110-DKLK0EGEYA-540_frame1770.jpg)
![deeplab output](deeplab.jpg)<br/>
##### Interactive mode
In each of the output look similar to the image shown above.The slide image may contain the heading, lists, texts, figures, and table regions.
To convey the presents of these regions in the slide to a VI student, the system reads the region name such as heading, lists, etc. when the mouse cursor moves over the region of the slide image. Hence, a VI student can easily identify the regions. A mouse click on this region triggers the system to read out the content in the corresponding region.
##### Non-interactive mode
In non-interactive mode, the user has no option to select a region and play the content of the region. Instead, the system plays all the slide content from start to end. To evaluate this mode, kindly click the button shown below the right corner of the image.
### Step3: Submit the evaluation
Based on your experience, we request you to rate each output ranging from [0 to 10].
Kindly submit your result in a table format as shown below.

Sl No | Image Name | GT(I) | GT(N) | Deeplab(I) | Deeplab(N) | PSP(I) | PSP(N) | Tesseract 
--- | --- | --- | --- |--- |--- |--- |--- |--- 
1 | 130110-DKLK0EGEYA-540_frame1770.jpg | x | x | x | x | x | x | x 

