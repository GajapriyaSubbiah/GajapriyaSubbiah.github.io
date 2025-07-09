---
layout: post
title: Image Manipulation
tags: [NumPy, Array operations]
image: "/posts/camaro.jpg"
---

Let's import the necessary packages to dive in!<br/>
import numpy,<br/>
import scikit-image as io - allows to read an image<br/>
import matplotlib - to visualize the image<br/>

**io.imread** functionality will read an image into array of pixels<br/>
In an color image we have intensity values for each of the three color channels red, green, blue.

**Shape** attribute display the how the image looks in a structure like how much width/tall/dimenional array(1d, 2d, 3d).<br/>
Now let's create a camaro object to read our image and finds our shape of the image.

>camaro = io.imread("camaro.jpg")
>plt.imshow(camaro)
>plt.show()

##### Array operations

> Slicing an image - specify the axis<br/>
> vertical stack - stack an array in a vertical order<br/>
> flip the array - start, -stop, -step logic to exactly how we want to flip. For instance, -1 indicates to reverse the image<br/>

##### Cropped Image

    cropped_array = img_array[start_row:end_row, start_col:end_col, :]
    # The ':', in the third dimension is for retaining all color channels (if present)

    cropped = camaro[0:500,:,:]
    plt.imshow(cropped)
    plt.show()
    
    cropped = camaro[:,400:1000,:]
    plt.imshow(cropped)
    plt.show()
    
    cropped = camaro[350:1100,200:1400,:]
    plt.imshow(cropped)
    plt.show()

![alt](../img/posts/cropped.jpg)

##### To flip image vertically and horizontally

    vertical_flip = camaro[::-1,:,:]
    plt.imshow(vertical_flip)
    plt.show()
    io.imsave("vertical_flip.jpg", vertical_flip)

![alt](../img/posts/vertical_flip.jpg)
    
    horizontal_flip = camaro[:,::-1,:]
    plt.imshow(horizontal_flip)
    plt.show()
    io.imsave("horizontal_flip.jpg", horizontal_flip)

 ![alt](../img/posts/horizontal_flip.jpg)

##### To colour our image

First we need to create an object called red with zeros.

    red = np.zeros(camaro.shape, dtype = "uint8")

We now want to fill in the rows and columns with the values for only the red channel and leave the other two color channel as zeros.

    red = np.zeros(camaro.shape, dtype = "uint8")
    
    red[:,:,0] = camaro[:,:,0]
    plt.imshow(red)
    plt.show()
    io.imsave("red.jpg", red)

 ![alt](../img/posts/red.jpg)
 
    green = np.zeros(camaro.shape, dtype = "uint8")
    
    green[:,:,1] = camaro[:,:,1]
    plt.imshow(green)
    plt.show()
    io.imsave("green.jpg", green)

 ![alt](../img/posts/green.jpg)
    
    blue = np.zeros(camaro.shape, dtype = "uint8")
    
    blue[:,:,2] = camaro[:,:,2]
    plt.imshow(blue)
    plt.show()
    io.imsave("blue.jpg", blue)

 ![alt](../img/posts/blue.jpg)

##### To stack all of our images

 ![alt](../img/posts/vertical_stack.jpg)

    vertical_stack = np.vstack((red,green,blue))
    plt.imshow(vertical_stack)
    plt.show()
    io.imsave("vertical_stack.jpg", vertical_stack)

How :cool: is that :sunglasses:!!!
