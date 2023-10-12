# Simple_Image_Processing_System
A mini project carried out to perform simple tasks on images using Python

## Abstract:
In general, an image is treated as a multi-dimensional array (or a matrix), in which a pixel is represented by an array of three values corresponding to three color channels in the RGB color system. The way this program works is we mainly deal with the image in the converted form of a numpy matrix and conducting the required tasks means making corresponding changes on the array (e.g: flipping the image means inverting the matrix, changing brightness means increasing/decreasing the pixels' RGB values, etc...)

## Techniques:
### Libraries:
<ul>
  <li><b>Numpy</b>: conducting tasks relating numeric and matrix calculations relating to numpy ndarrays, including multiplication, inversion, addition, etc...</li>
  <li><b>Pyplot</b>: displaying images for visualization and comparison</li>
  <li><b>Image</b>: mainly for image processing (pdf or png) (can be improved to other formats of choice)</li>
  <li><b>datetime</b>: keep track of runtime</li>
</ul>

### Implemented Functionalities:
<ul>
  <li><b>Changing the image's brightness: </b> this task is simply conducted by adding each pixel of the image with a scalar with the assurance that the color values are in the (0,255) range (in my version of the implementation i "stiff put" it as 60 but it can be better if the user gets to decide)
  </li>

  <li><b>Changing the image's contrast: </b> this task is simply conducted by multiplying each pixel of the image with a value (contrast rate) with the assurance that the color values are in the (0,255) range (in my version of the implementation i "stiff put" it as 1.3 but it can be better if the user gets to decide)
  </li>

  <li><b>Flipping the image: </b> regarding this task, it can easily be done by flipping the matrix in accordance with the direction that the user chooses to flip the image
  </li>

  <li><b>Converting the image to Grayscale/Sepia type: </b> as for this task, both the minitasks take the same approach as the conversion first takes place in the pixel then applied to the whole image. For Grayscale, the pixel's values are multiplied with a scalar representing the contribution rate while for Sepia, new RGB values are calculated based on a pre-given formula and assigned to the pixel itself
  </li>

  <li><b>Blurring/Sharpening the image: </b> for this task, the Gaussian Blur algortim is applied with a blurring kernel, leaving the pixels surrounding the image and calculating the new pixel's RGB values. The same steps are applied for image sharpening, with a different kernel and making sure that the RGB values stays in the (0,255) bounds
  </li>

  <li><b>Cropping the image to a pre-defined size: </b> regarding this task, the idea is just to somehow create a centralized frame that is in rate with the image's height and width, then just define an image size (e.g: 110) then extract that specific section from the image using array slicing
  </li>

  <li><b>Cropping the image using a circular frame: </b> in this task, we need to write a circular equation with the coordinates of the center calculated by halving the image's height and width. After having the circular equation, any pixel that belongs to the circle is kept while the others are converted to black pixels
  </li>

  <li><b>Cropping the image using elipses frame: </b> in this task, we need to write two elipse equations overlapping each other with the coordinates of the center calculated by halving the image's height and width. After having the elipse equations, any pixel that belongs both of the elipses is kept while the others are converted to black pixels
  </li>
</ul>

## Results Demonstration: 
Please refer to the jupyter notebook for the results and runtime of each functionality, thank you
