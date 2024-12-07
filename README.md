# deblurring-images-with-richardson-lucy
First blurring images using a gaussian blur, then deblurring them using the Richardson Lucy algorithm

**dnorm**: Calculates the probability density function of the normal distribution <br>
**gaussian_kernel**: Generates a matrix that represents a discrete approximation of a Gaussian function <br>
**convolution**: Applies a given kernel on an image (in this case to blur it) <br>
**gaussian-blur**: Applies the gaussian_kernel onto the given image <br>

---

# Deblurring using the Richardson-Lucy algorithm: 
This only takes a single line of code: 
```
deconvolved_RL = restoration.richardson_lucy(blurred_image_cast, psf, num_iter=30)
```
<br>
All the code after this is just representing the before and after results.
<br>

Some results: <br>
<img width="817" alt="Screenshot 2024-12-07 at 21 03 14" src="https://github.com/user-attachments/assets/a08253a2-434d-426e-b1ac-fc56fa26678f">
<img width="817" alt="Screenshot 2024-12-07 at 21 03 28" src="https://github.com/user-attachments/assets/058ccbec-a411-4158-80a0-bc589b3be31f">
<img width="818" alt="Screenshot 2024-12-07 at 21 03 50" src="https://github.com/user-attachments/assets/6f87b04d-d638-4e17-b1a3-e23f3fabd1fe">
<img width="816" alt="Screenshot 2024-12-07 at 21 04 03" src="https://github.com/user-attachments/assets/1bc289f3-6b24-4042-98bb-ec2e100364f8">




Since this code doesn't actually dive into how the RL algorithm actually works and focuses mainly on representing the results of the algorithm, these are some more links to read up on how the algorithm actually works:
* https://en.wikipedia.org/wiki/Richardson–Lucy_deconvolution
* https://uk.mathworks.com/help/images/deblurring-images-using-the-lucy-richardson-algorithm.html
* https://stargazerslounge.com/topic/228147-lucy-richardson-deconvolution-so-what-is-it/
* https://www.isid.ac.in/~deepayan/SC2010/project-sub/RLA/report.pdf
