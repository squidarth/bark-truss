# Deploy Bark with Baseten

## Pre-reqs
* Set up a [Baseten](https://www.baseten.co) account
* Clone this repo
* Install Baseten and [Truss](https://truss.baseten.co) client
```python
pip install baseten
pip install truss
```
* Auth into Baseten
```python
import baseten
baseten.login("*** BASETEN API KEY ***")
```

## Deploy to Baseten
```python
import baseten
import truss

bark_handle = truss.load(".")
baseten.deploy(bark_handle, model_name="Bark")
```

## Hardware
This model will deploy to a NVIDIA A10G. Inference time is 3-5 seconds depending on the length of the prompt.
