---
layout: post
title: Image Manipulation
tags: [NumPy, Array operations]
image: "/posts/camaro.jpg"
---

Let's import the necessary packages to dive in!
import numpy,
import scikit-image as io - allows to read an image
import matplotlib - to visualize the image

**io.imread** functionality will read an image into array of pixels
In an color image we have intensity values for each of the three color channels red, green, blue.

**Shape** attribute display the how the image looks in a structure like much width/tall/dimenional array(1d, 2d, 3d).

Now let's create a camaro object to read our and finds our shape of the image.

>camaro = io.imread("camaro.jpg")
plt.imshow(camaro)
plt.show()

##### Array operations

> Slicing an image - specify the axis
> vertical stack - stack an array in a vertical order
> flip the array - start, -stop, -step logic to exactly how we want to flip. For instance, -1 indicates to reverse the image

##### Cropped Image

    cropped_array = img_array[start_row:end_row, start_col:end_col, :]
    # The ':', in the third dimension is for retaining all color channels (if present)

>cropped = camaro[0:500,:,:]
plt.imshow(cropped)
plt.show()

cropped = camaro[:,400:1000,:]
plt.imshow(cropped)
plt.show()

cropped = camaro[350:1100,200:1400,:]
plt.imshow(cropped)
plt.show()

![alt](/posts/cropped.jpg)



![alt](https://images.unsplash.com/photo-1429734160945-4f85244d6a5a?ixlib=rb-0.3.5&q=80&fm=jpg&crop=entropy&w=1080&fit=max&s=0e46d4b45ffdd302bc6b44ec8917fe83)

##### Unordered Lists

Duis id ante elit. Aliquam quis tellus id orci eleifend finibus. Donec consequat justo ligula, eget sodales purus hendrerit at.

* Ut at interdum nunc. Maecenas commodo turpis quis elementum gravida.
*    Nunc ac sapien tellus. Quisque risus enim, tempus eget porttitor in, pellentesque vel urna.
*    Donec nibh massa, rutrum a sollicitudin eu, lacinia in lorem.

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec diam augue, luctus a lacus vitae, ullamcorper interdum lacus. Sed consequat, nisi non mattis euismod, mi metus venenatis lacus, id feugiat orci mi eu urna. Donec condimentum lacus eget nibh consectetur, ac venenatis erat tristique. Nunc eros metus, venenatis in cursus ut, aliquam eu diam.

##### Quote

> Graphic design is the paradise of individuality, eccentricity, heresy, abnormality, hobbies, and humors. — George Santayana
