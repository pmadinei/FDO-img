# Introduction
Throughout this project, first we try to remove noises from images 1 to 4 by implementing proper filters. Then, improving details and visibility in Images 5 to 10 takes place. At last, Frequency Domain Operations come handy to make old people look younger in last 2 images.

# Requirement
* Matlab > R2019b
* Matlab Live Editor

# How to Use
Use the file "Removing the Noise.mlx" to remove noises from images 1 to 4 by implementing proper filters. Utilize the file "Frequency Domain Operations.mlx" to improve details and visibility in Images 5 to 10 plus implementing Frequency Domain Operations to make old people look younger. Good Luck!

# Results
## Part 1 - Removing Noises
Pictures Bellow illustrates noisy images:
![Noisy](https://github.com/pmadinei/FDO-img/blob/master/Results/Noisy%20Images.png)
![Removed1](https://github.com/pmadinei/FDO-img/blob/master/Results/Removed%20Niuses%201.png)
![Removed2](https://github.com/pmadinei/FDO-img/blob/master/Results/Removed%20Niuses%202.png)
Now by utilizing the code bellow, we can see images in frequency domain:
```Matlab
Fshift = fftshift(fft2(double(a)));
```
![FD](https://github.com/pmadinei/FDO-img/blob/master/Results/images%20in%20frequency%20domain.png)
To remove noises, we simply remove the noise representations in illustrations above. The code bellow is an instance for the noise removal:
```Matlab
M = zeros(size(a,1), size(a,2));
M(265:290,200:600) = 1;
figure, imshow(M, []);
Gshift = M .* Fshift;
G = ifftshift(Gshift);
g = abs(ifft2(G));
```

## Part 2 - Improving Visibility
### Image 5:
![1.1](https://github.com/pmadinei/FDO-img/blob/master/Results/1.1.png)
![1.2](https://github.com/pmadinei/FDO-img/blob/master/Results/1.2.png)
![1.3](https://github.com/pmadinei/FDO-img/blob/master/Results/1.3.png)

### Image 6:
![2.1](https://github.com/pmadinei/FDO-img/blob/master/Results/2.1.png)
![2.2](https://github.com/pmadinei/FDO-img/blob/master/Results/2.2.png)
![2.3](https://github.com/pmadinei/FDO-img/blob/master/Results/2.3.png)

### Image 7:
![3.1](https://github.com/pmadinei/FDO-img/blob/master/Results/3.1.png)
![3.2](https://github.com/pmadinei/FDO-img/blob/master/Results/3.2.png)
![3.3](https://github.com/pmadinei/FDO-img/blob/master/Results/3.3.png)

### Image 8:
![4.1](https://github.com/pmadinei/FDO-img/blob/master/Results/4.1.png)
![4.2](https://github.com/pmadinei/FDO-img/blob/master/Results/4.2.png)
![4.3](https://github.com/pmadinei/FDO-img/blob/master/Results/4.3.png)

### Image 9:
![5.1](https://github.com/pmadinei/FDO-img/blob/master/Results/5.1.png)
![5.2](https://github.com/pmadinei/FDO-img/blob/master/Results/5.2.png)
![5.3](https://github.com/pmadinei/FDO-img/blob/master/Results/5.3.png)

### Image 10:
![6.1](https://github.com/pmadinei/FDO-img/blob/master/Results/6.1.png)
![6.2](https://github.com/pmadinei/FDO-img/blob/master/Results/6.2.png)
![6.3](https://github.com/pmadinei/FDO-img/blob/master/Results/6.3.png)

## Part 3 - Making People Younger
### Image 11:
![7.1](https://github.com/pmadinei/FDO-img/blob/master/Results/7.1.png)
![7.2](https://github.com/pmadinei/FDO-img/blob/master/Results/7.2.png)
![7.3](https://github.com/pmadinei/FDO-img/blob/master/Results/7.3.png)
![7.4](https://github.com/pmadinei/FDO-img/blob/master/Results/7.4.png)

### Image 11:
![8.1](https://github.com/pmadinei/FDO-img/blob/master/Results/8.1.png)
![8.2](https://github.com/pmadinei/FDO-img/blob/master/Results/8.2.png)
![8.3](https://github.com/pmadinei/FDO-img/blob/master/Results/8.3.png)
![8.4](https://github.com/pmadinei/FDO-img/blob/master/Results/8.4.png)
