# Sequence To Image

At it's heart, Rust doesn't care whether or data is biological or not and since we've already learned how to keep our data in an integer format, all we need to do to create an image from our sequences is to learn how to use the image library to make our first image!

In this example, we'll make each pixel a letter in our biological sequence, with a different color for each type of letter. If we applied this directly to a sequence, our image would be a single row of differing colored pixels. For example, AAACCC could be greengreegreenblueblueblue. If we think of an image as a quilt or mat of numbers, we could have our image be multiple sequences. Each row of pixels would be a sequence and these would be written out to a file like a typewriter, row by row, to create our final image.

Let's try it! First, we'll create a sequence and create an image that's a row of pixels:

```
// Import RgbImage from the Image crate
use image::RgbImage;

// Import colors from bioutils
use bioutils::utils::image::color::*;

// Set the width and height of our image. We'll make these constants (const) because they don't change for the whole program. 
const WIDTH: u32 = 50;
const HEIGHT: u32 = 50;

fn main() {
    // Make our sequence
    let seq = b"AAAACCCCTTTTGGGGNNNN";

    // Make a new image with height and width that we'll put our data in
    let mut img = RgbImage::new(HEIGHT, WIDTH); 

    // Set our y coordinate to 49 for first example (the bottom row of pixels in our image) If we set to 50, it'll be out of bounds (0 to 49 for a height of 50) and rust will panic/error.
    
    let y_pixel_coord=49; 
    // Print our unsigned integers for reference
    println!("{:?}", seq); 

    // For each unsigned integer in our sequence, color the pixel corresponding to the x coordinate and y coordinate, color by the unsigned integer present.
    for (x, &c) in seq.into_iter().enumerate() { 
        match c {
            67 => img.put_pixel(x as u32, y_pixel_coord, RED_RGB), // 67 is b"A", set Adenosine color
            65 => img.put_pixel(x as u32, y_pixel_coord, GREEN_RGB), // 65 is b"C", set Cytosine color
            84 => img.put_pixel(x as u32, y_pixel_coord, BLUE_RGB), // 84 is b"T", set Thymine color
            71 => img.put_pixel(x as u32, y_pixel_coord, PURPLE_RGB), // 71 is b"G", set Guanine color
            78 => img.put_pixel(x as u32, y_pixel_coord, GRAY_RGB), // 110 is b"N", set Undetermined color
            _ => img.put_pixel(x as u32, y_pixel_coord, BLACK_RGB), // 71 is b"G", set all other as black
        };
    }

    // write our image out to a file
    img.save("myfirstimage.png").unwrap();

}
```


*Our very first image!*

We've not only started working with images, we've even output it into a file we can send our friends!

