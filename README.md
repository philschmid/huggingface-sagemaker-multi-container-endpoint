# Hugging Face Transformers with Amazon SageMaker and Multi-Container Endpoints
### Deploy multiple Transformer models to the same Amazon SageMaker Infrastructure


Welcome to this getting started guide. We will use the Hugging Face Inference DLCs and Amazon SageMaker to deploy multiple transformer models as [Multi-Container Endpoint](https://docs.aws.amazon.com/sagemaker/latest/dg/multi-container-endpoints.html). 
Amazon SageMaker Multi-Container Endpoint is an inference option to deploy multiple containers (multiple models) to the same SageMaker real-time endpoint. These models/containers can be accessed individually or in a pipeline. Amazon SageMaer [Multi-Container Endpoint](https://docs.aws.amazon.com/sagemaker/latest/dg/multi-container-endpoints.html) can be used to improve endpoint utilization and optimize costs. An example for this is **time zone differences**, the workload for model A (U.S) is mostly at during the day and the workload for model B (Germany) is mostly during the night, you can deploy model A and model B to the same SageMaker endpoint and optimize your costs. 

_**NOTE:** As the time of writing this only `CPU` Instances are supported for Multi-Container Endpoint._


![mce](imgs/mce.png)

