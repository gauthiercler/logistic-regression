
# Pseudo neural network logistic regression classifier from scratch

Implementation of a logistic regression classifier ([wiki](https://en.wikipedia.org/wiki/Logistic_regression)) based on a neural network mindset.

Pseudo neural network refers to the fact that Logistic regression is a considered as a single layered NN.

![](https://miro.medium.com/max/680/1*ZKLJUL36yQ9lc9Gkq1oISw.png)

### For each <img src="https://latex.codecogs.com/svg.latex?%5Cdpi%7B300%7D%20%24x%5E%7B%28i%29%7D%24" height="20">:

#### Compute <img src="https://latex.codecogs.com/svg.latex?%5Cdpi%7B300%7D%20%24a%5E%7B%28i%29%7D%24" height="20">![]():

<p align="center">
  <img src="https://latex.codecogs.com/svg.latex?%5Cdpi%7B300%7D%20%24%24z%5E%7B%28i%29%7D%20%3D%20w%5ET%20x%5E%7B%28i%29%7D%20&plus;%20b%20%5Ctag%7B1%7D%24%24" height="30">
</p>

#### Make prediction:
<p align="center">
  <img src="https://latex.codecogs.com/svg.latex?%5Cdpi%7B300%7D%20%24%24%5Chat%7By%7D%5E%7B%28i%29%7D%20%3D%20a%5E%7B%28i%29%7D%20%3D%20sigmoid%28z%5E%7B%28i%29%7D%29%5Ctag%7B2%7D%24%24" height="30">
</p>

*Sigmoid ([wiki](https://en.wikipedia.org/wiki/Sigmoid_function)) is defined as*:
<p align="center">
  <img src="https://latex.codecogs.com/svg.latex?%5Cdpi%7B300%7D%20%24%24sigmoid%28%20w%5ET%20x%20&plus;%20b%29%20%3D%20%5Cfrac%7B1%7D%7B1%20&plus;%20e%5E%7B-%28w%5ET%20x%20&plus;%20b%29%7D%7D%24%24" height="50">
</p>



#### Calculate loss:
 <p align="center">
	 <img src="https://latex.codecogs.com/svg.latex?%5Cdpi%7B300%7D%20%24%24%20%5Cmathcal%7BL%7D%28a%5E%7B%28i%29%7D%2C%20y%5E%7B%28i%29%7D%29%20%3D%20-%20y%5E%7B%28i%29%7D%20%5Clog%28a%5E%7B%28i%29%7D%29%20-%20%281-y%5E%7B%28i%29%7D%20%29%20%5Clog%281-a%5E%7B%28i%29%7D%29%5Ctag%7B3%7D%24%24" height="30">
 </p>


#### Forward propagation, compute cost:
<p align="center">
 <img src="https://latex.codecogs.com/svg.latex?%5Cdpi%7B300%7D%20%24%24%20J%20%3D%20%5Cfrac%7B1%7D%7Bm%7D%20%5Csum_%7Bi%3D1%7D%5Em%20%5Cmathcal%7BL%7D%28a%5E%7B%28i%29%7D%2C%20y%5E%7B%28i%29%7D%29%24%24" height="60">
</p>

#### Backward propagation, compute gradients:
<p align="center">
 <img src="https://latex.codecogs.com/svg.latex?%5Cdpi%7B300%7D%20%24%24%20%5Cfrac%7B%5Cpartial%20J%7D%7B%5Cpartial%20w%7D%20%3D%20%5Cfrac%7B1%7D%7Bm%7DX%28A-Y%29%5ET%24%24" height="50">
</p>
<p align="center">
 <img src="https://latex.codecogs.com/svg.latex?%5Cdpi%7B300%7D%20%24%24%20%5Cfrac%7B%5Cpartial%20J%7D%7B%5Cpartial%20b%7D%20%3D%20%5Cfrac%7B1%7D%7Bm%7D%20%5Csum_%7Bi%3D1%7D%5Em%20%28a%5E%7B%28i%29%7D-y%5E%7B%28i%29%7D%29%24%24" height="60">
</p>

Repeat process until convergence by minimizing cost value.
