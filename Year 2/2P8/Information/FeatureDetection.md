Colour is not very useful to us as it changes with orientation and lighting. We more care about edges

0D - featureless
1D - edges
2D - corners - has a desirable invariance to lighting

1D edge detection -
We must smooth our signal, then differentiate it.
We will be smoothing by convolving with the Gaussian kernel: $g_\sigma(x)=\frac{1}{\sigma\sqrt{2\pi}}exp(-\frac{x^2}{2\sigma^2})$

Then take the derivative. As it is a linear operation, we could do it in either order
$s'(x)=\frac{d}{dx}[g_{\sigma}(x)*I(x)]=g_{\sigma}'*I(x)$

Interpolation can be used to find the maxima. Or we can take the derivative again and find where we get a zero crossing.
A smaller $\sigma$ brings out all the edges, a larger one only brings out the larger ones

2D edge detection-
We do a 2D convolution with the 2D Gaussian $G_{\sigma}(x,y)$
$S(x,y)=\int_{-\infty}^{\infty}\int_{-\infty}^{\infty}G_{\sigma}(u,v)I(x-u,y-v)dudv$

The next step would be to take the gradient using the grad function $\nabla S = \nabla (G_{\sigma}*I)$
The next step is non-maximal suppression. Edge elements, or edgels are placed at locations where $|\nabla S|$ is greater than local values of $|\nabla S|$ in the directions $\pm \nabla S$.
Next all the edgels are thresholded, so only that with a magnitude over a certain value are kept.

In practice, the image and filter kernels are discrete quantities.
$S(x,y)=\sum_{-n}^{n}\sum_{-n}^{n}G_{\sigma}(u,v)I(x-u,y-v)dudv$
For acceptable accuracy, we usually retain only Gaussian values that are more than say 0.001 of the peak value. This gives us $2n+1$ elements.

2D convolution can be split into 2 1D convolutions, allowing for a saving of $(2n+1)^2/2(2n+1)$

Differentiation is also computed discretely. We use the central limit theorem: $\frac{\partial S}{\partial x}\approx \frac{S(x+1,y)-S(x-1,y)}{2}$
This is equivalent to convolving with the kernel $[1/2, 0, -1/2]$
It is in this order as it gets flipped in the convolution process.

Edges aren't great when working with images at different angles or scales. They suffer from the aperture problem: when viewing a moving edge, it's only possible to measure motion normal to the edge locally.
Corners do not have this issue so are very valuable to us.

We want to find corners. This can be done by comparing adjacent regions of pixels to a given region of pixels and determining the similarity, or the cross-correlation function. An edge will have a distinct peak, as it's not like anything else around.

Methods of measuring similarity between matrices:
1) Finding the sum of squared differences, essentially the Euclidian distance squared
2) Subtract the mean and normalise, then find the dot product between the two

A blob is an area of uniform intensity in the image. Blob detection is ideal for fixing the location of an object in a scene. Larger objects become more like blobs at larger values of $\sigma$

![[Pasted image 20260504155212.png]]

