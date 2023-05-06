Download Link: https://assignmentchef.com/product/solved-ece4830-lab2
<br>
You will be given the following image (left) in a Matlab file (JB.mat) that you can load using the command <em>load JB.mat</em>. These portrait images are usually subject to some filtering to soften undesired details such as skin wrinkles below the eyes. A poor method to do this would be to actually use Vaseline in the camera lens. Other nice effects would use a cardboard with a hole to make the effects of a vignette during darkroom developing. In the digital age we would like to do these things with the computer and obtain the image on the right. How would you do both operations using signal processing operations? You can work with the gray scale image using the command rgb2gray or whatever your solution is you can operate on the three Red, Green and Blue fields to obtain the results shown below. You can use the 2D FFT command <em>fft2</em> for frequency operations.

Try ideal filters in the shape of a square and circular ones. Try also Gaussian based filters with different cutoff frequencies. Search for the closed form solution of the DFT of a Gaussian function with mean  and standard deviation . Having found that expression then you can discern that the following commands can create a Gaussian filter in the frequency domain.

(a) One way to create the two dimensional Gaussian filter hf would be:

h = gausswin(9,0.1); h = (h*h’);

hf = fft2(h,660*2,660*2);




or you can use the following:

h = fspecial(‘gaussian’, [9 9], 2); hf = fft2(h,660*2,660*2);







<ul>

 <li>Do you need to work in the frequency domain or the original image domain for the vignette effects?</li>

 <li>Does using zero-padding makes a difference?</li>

 <li>Does the order, vignette-filtering or filtering-vignette, is important?</li>

</ul>

Please document all your findings?

<strong>Problem 2 </strong>

You will be given a matlab file containing 16 ultrasound scans at the same position such as the one shown next:




The first peak as indicated by the first arrow corresponds to the equipment and is always there but has no meaning. The strongest response around time bin 100 is caused by multiple reflections as explained in class. What type of filtering can be used to eliminate any further response from the extra pulses sent caused by this bouncing back and forth at the beginning of the ultrasound pulse trajectory? Please design the filter, decide for LPF, HPF or BPF and its frequency support.

<strong>Problem 3.  </strong>

Please solve the following problems:




5.1.2       5.1.4 (d) to (i)       5.1.7 (d) to (h)

5.1.9       5.2.2                       5.2.8

5.2.14










5.1.7 Find the inverse of