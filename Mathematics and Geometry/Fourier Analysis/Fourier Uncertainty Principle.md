Category: [[Fourier Analysis]]
___
Prerequisites: [[Fourier Transform and Frequency Domain]]
___
Related: [[Discrete Fourier Transform]] [[Gaussian is FT of Itself]]
___
In the discrete fourier transform, we have seen the normalisation relationship: 
$$\Delta \xi \Delta T=\frac{1}{N}$$
In other words, the uncertainty of the time samples and frequency samples multiply to form the reciprocal of the cycle length. 

In the general case, the cycle length is infinity, but in another sense $2\pi$, since it appears as the renormalisation constant in the transform formulae. The functions also become distributions. Thus the uncertainty are the standard deviations. Indeed, it turns out that:
$$\boxed{\sigma_\xi\sigma_t=\frac{1}{2\pi}}$$
This relationship is easily satisfied by the gaussian function, which remains gaussian under the transform. Now, the power contained in the signal is the magnitude squared, in both time and frequency domain. Thus the Gaussian distributions each get dilated horizontally by a factor of $1/\sqrt{2}$, giving:
$$\boxed{\sigma_{energy,\ \xi}\sigma_{energy,\ t}=\frac{1}{4\pi}}$$

