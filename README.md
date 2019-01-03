# Image-Compression-using-Wavelet-Transform
Image compression is minimizing the size in bytes of a graphics file without degrading the quality of the image to an unacceptable level.
The reduction in file size allows more images to be stored in a given amount of disk or memory space.
It also reduces the time required for images to be sent over the Internet or downloaded from Web pages.

What's a Wavelet?
A wavelet is a wave-like oscillation with an amplitude that begins at zero, increases, and then decreases back to zero. It can typically be visualized as a "brief oscillation" like one recorded by a seismograph or heart monitor.
Each wavelet measurement (the wavelet transform corresponding to a fixed parameter) tells us something about the temporal extent of the signal, as well as something about the frequency spectrum of the signal. 

We are going to use Haar wavelet transform.
 	Its one of the simplest wavelet transforms 
	which is based on the idea of decomposing a 
	signal into two components :
		Average (Approximation)
		Difference (Detail)

We will take the following one-dimensional array 
	r =      <156   159   158   155   158   156   159   158>
Group the columns in pairs:  [156 159], [158 155], [158 156], [159 158]
Average  each  of  these  pairs,  then  replace  the  four  first  columns  of  r  with  those values and compute 1/2  the difference of each pair, then replace the last four columns of r with those.  Our array r becomes:
 	r0  =  <157.5   156.5   157   158.5   −1.5   1.5   1   0.5>
The first four entries are called approximation coefficients.  
The last four ones are called detail coefficients.
Repeat this process again and again till you get just one approximation coeff. 
Finally r =  <157.375   −0.375   0.5   −0.75   −1.5   1.5   1   0.5>

As we can see,  the resulting  array has only one entry that is big;  the leftmost one.  All the other entries, the detail coefficients, are close to 0.  The beauty of what we have done so far lies in the fact that it is completely reversible.
We  have  been  able  to  reconstruct  the  original  array.   We  call  this  type  of  compression lossless.





References
 [1]  Wavelet Analysis. Wolfram Documentation Center. 2016. Web. 1 Apr. 
        2016.https://reference.wolfram.com/language/guide/Wavelets.html
 [2]  Salomon, David. A Guide to Data Compression Methods. Springer Professional
 Computing. New York:  Springer-Verlag New York, 1 Feb. 2002. Print.
 [3]  Remigius, Onyshczak and Abdou Youssef. “Fingerprint Image Compression and the Wavelet 
       Scalar Quantization Specification”, a book chapter in Fingerprint Imaging Technologies. Springer-         	Verlag, 2004, pp. 385-413.
         https://www.seas.gwu.edu/ ayoussef/papers/FingerPrintWSQ- chapter.pdf
[4]  Machado, D. P., et al. Darth Fader:  Using Wavelets to Obtain Accurate Redshifts of
       Spectra at Very Low Signal-to-Noise. Astronomy and Astrophysics 560. (16 Dec. 2013):
       20. Web. 27 Feb. 2016.
        http://www.aanda.org/articles/aa/pdf/2013/12/aa19857-12.pdf
 
[5]  Tamboli, S. S., and V. R. Udupi. Image Compression Using Haar Wavelet Transform.
