# Lane Finding For Self Driving Car.
This project is aimed to develop a machine learning model that can identify lane on the road for self driving cars.
Below are the steps that involves step by step development of this project:
1. Reading the images from the directory.
2. Edge Detection: Identifying sharp changes in intensity in adjacent pixels. 
Image is made up of pixels: intensity from 0 to 255, 0 for black and 255 for white.
3. Image noise reduction: By using Gaussian Blur, it average out the pixel's brighteness using it's neighbouring pixels.
4. Bitwise AND Operation: This occurs between two images element - wise, between two arrays of pixels.
Computing the bitwise & of both images as we saw in the theory section, takes the bitwise & of each homologous pixel in both arrays, ultimately masking the canny image to only show the region of interest traced by the polygonal contour of the mask.

# Concept used
HOUGH SPACE: it is a parametric space.
let a line: y=mx+b
in Cartesian Coordinate we plot curve b/w x&y.
in Hough Space i.e. parametric system, we plot between m&b i.e. slope v/s intercept.
So, a family of lines in cartesian coordinate can be represented by a straight line in Hough Space.
And, if in Hough Space, two lines intersect means having same slope and intercept value. Therefore, two lines of two different family of line on coordinate system are consistent having infinite solution.

Now, there can be a straight line, having a slope of infinite. But this infinite value cannot be represented on a Hough Space. So, we use POLAR COORDINATE SYSTEM. 
        rho(Þ) = r.cos(ɵ) + r.sin(ɵ)
        where rho and ɵ are parameters.
So, the representation of parametric condition of polar coordinate system in Hough Space is Sinosuidal. 
And, for different family of lines in POLAR COORDINATE SYSTEM(PCS), different SINOSUIDAL curve interesect at a point in a Hough Space. That show that for a particular value of rho and ɵ lines in PCS are consistent.
