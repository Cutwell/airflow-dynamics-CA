# Parsing images into Numpy arrays

1. Image must be 8bit Greyscale (8Bpc GREY) PNG image.
2. Incrementing greyscale values indicate map objects.

| Pixel value | Representation |
|:--:|:--:|
|#000000|Air|
|#010101|Wall|
|#020202|Window|