# Image Background

A computer understands an image a little differently from us: in [pixels](https://en.wikipedia.org/wiki/Pixel)! Pixels are the elemental building blocks of images, usually each comprised of three colors: red, green, and blue. Depending on the intensity of each color in the pixel, we can make any other color. For example, white would be 100% red, green, blue (RGB), where black would be 0% red, green, blue.

![magnified pixels](./img/magpix.jpg)

*Magnified pixels. If we squint, we can see that each 'pixel' is made of three rectangular stripes colored red, green, and blue in differing intensities. Image also from Wikipedia.*

In the Rust Image library each pixel is represented by three values for RGB, respectively. Most conveniently, these are the same type of values we store for each letter of our sequence ([unsigned 8-bit integer](https://doc.rust-lang.org/book/ch03-02-data-types.html))! 

