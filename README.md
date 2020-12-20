# customized-kernel
Music generation using CNN-based VAE with customized convolution kernels.

## Usage
```bash
cd ./code
python $filter_setting$_filter_$n$ch.py
```
where filter_setting is either "custom" or "tradidional", and n is either 2 or 6.


## Arguments
```bash
-w, --weights
```
* The weights file of the pretrained model one wants to load.
* No default value.
```bash
-m, --mode
```
* Either "train" or "test".
* Default value is "train".
```bash
-g, --gamma
```
* Parameter for focal loss.
* Default value is 0.25.
```bash
-a, --alpha
```
* Parameter for focal loss.
* Default value is 0.0.
```bash
-k, --klcoeff
```
* Defined as "total_loss = reconstruction_loss - klcoeff*kl_divergence". Was 0.5 in the original paper, which is too large for this experiment setting.
* Default value is 0.05.
## Reference
* Original code structure: https://github.com/awslabs/keras-apache-mxnet/blob/master/examples/variational_autoencoder_deconv.py
* Beethoven dataset: https://github.com/Tsung-Ping/functional-harmony
* Bach dataset: Tsung-Ping Chen (not public)
