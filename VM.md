
# Azure Virtual Machine (VM) Resource


## VM Selection Guidance
- https://docs.microsoft.com/en-us/azure/azure-stack/user/azure-stack-vm-considerations
- https://docs.microsoft.com/en-us/azure/virtual-machines/windows/sizes
- https://azure.microsoft.com/en-us/pricing/details/virtual-machines/series/


## Pricing
- https://azure.microsoft.com/en-us/pricing/
- https://azure.microsoft.com/en-us/pricing/calculator/
- https://azure.microsoft.com/en-us/pricing/details/virtual-machines/windows/
- https://azure.microsoft.com/en-us/pricing/purchase-options/pay-as-you-go/
- https://azure.microsoft.com/en-us/pricing/details/batch/windows-virtual-machines/
  + Follow-up Question: Batch AI pricing is also avaialble?
- https://azureprice.net/


## Azure Github Resources
- https://github.com/Azure
- https://github.com/Azure/azure-quickstart-templates 


## Machine Learning VMs
- https://azure.microsoft.com/en-us/pricing/details/machine-learning-service/


## Data Science Virtual Machines (DSVMs)
- https://azure.microsoft.com/en-us/services/virtual-machines/data-science-virtual-machines/
- https://docs.microsoft.com/en-us/azure/machine-learning/data-science-virtual-machine/
- https://docs.microsoft.com/en-us/azure/machine-learning/data-science-virtual-machine/overview
- https://docs.microsoft.com/en-us/azure/machine-learning/data-science-virtual-machine/vm-do-ten-things
- https://docs.microsoft.com/en-us/azure/machine-learning/data-science-virtual-machine/dsvm-tools-overview
- https://docs.microsoft.com/en-us/azure/machine-learning/data-science-virtual-machine/provision-vm
- https://docs.microsoft.com/en-us/azure/machine-learning/data-science-virtual-machine/dsvm-pools

- Github Resoruces
  + https://github.com/Azure/DataScienceVM
  + https://github.com/Azure/data-ai-iot

- Marketplace, DSVMs
  + https://azuremarketplace.microsoft.com/en-us/marketplace/apps/microsoft-ads.windows-data-science-vm 
    * https://azuremarketplace.microsoft.com/en-us/marketplace/apps/microsoft-ads.windows-data-science-vm
    * https://azuremarketplace.microsoft.com/en-us/marketplace/apps/microsoft-ads.windows-data-science-vm?tab=PlansAndPrice


## Deep Learning Virtual Machine
- https://docs.microsoft.com/en-us/azure/machine-learning/data-science-virtual-machine/deep-learning-dsvm-overview
- https://docs.microsoft.com/en-us/azure/machine-learning/data-science-virtual-machine/provision-deep-learning-dsvm
  + "The Deep Learning Virtual Machine (DLVM) is a specially configured variant of the popular Data Science Virtual Machine (DSVM) to make it easier to use GPU-based VM instances for rapidly training deep learning models. It is supported with either Windows 2016, or the Ubuntu DSVM as the base. The DLVM shares the same core VM images and hence all the rich toolset that is available on DSVM."
  + "The DLVM supports all NC and ND series GPU VM instances. When provisioning the DLVM, you must choose one of the locations in Azure that has GPUs"
  + "The provisioning should take about 10-20 minutes."

- Marketplace, DLVMs
  + https://azuremarketplace.microsoft.com/en-us/marketplace/apps/microsoft-ads.dsvm-deep-learning?tab=Overview
    * "The Deep Learning Virtual Machine (DLVM) is a specially configured variant of the Data Science Virtual Machine(DSVM) to make it easier to use GPU-based VM instances for training deep learning models"
    * "The DLVM runs on Azure GPU NC-series VM instances. These GPUs use discrete device assignment, resulting in performance close to bare-metal, and are well-suited to deep learning problems"


## Articles of Interest
- 2019 
  + https://azure.microsoft.com/en-us/blog/fastai-on-azure-dsvm/

- 2018
  + https://www.pyimagesearch.com/2018/03/21/my-review-of-microsofts-deep-learning-virtual-machine/
    * "22 minutes for the NVIDIA K80 to complete the pipeline, the NVIDIA V100 completed the task in only 5 minutes"
    * ImageNet training...
      * "...trained SqueezeNet for a total of 80 epochs on the NVIDIA K80. SGD was used to train the network with an initial learning rate of 1e-2 (I found the Iandola et al. recommendation of 4e-2 to be far too large for stable training). Learning rates were lowered by an order of magnitude at epochs 50, 65, and 75, respectively."
      * "Each epoch took approximately 140 minutes on the K80 so the entire training time was ~1 week."
      * "Using multiple GPUs could have...training time to 1-3 days, depending on the number of GPUs utilized."
      * "...obtained 58.86% rank-1 and 79.38% rank-5 accuracy"
      * "After [training] the SqueezeNet on ImageNet using the NVIDIA K80...repeated the experiment with a single V100 GPU."
        * "Compared to the K80 (~140 minutes per epoch), the V100 was completing a single epoch in 28 minutes"
        * "...able to train SqueezeNet and replicate the results...in just over 36 hours."
      * "On Amazon’s EC2, for a p2.xlarge instance, you’ll pay $0.90/hr (1x K80), $7.20/hr (8x K80), or $14.40/hr (16x K80). That is $0.90/hr per K80."
      * "On Microsoft Azure, prices are the exact same $0.90/hr (1x K80), $1.80/hr (2x K80), and $3.60/hr (4x K80). This also comes out to $0.90/hr per K80."
      * "Amazon has V100 machines ready and priced at $3.06/hr (1x V100), $12.24/hr (4x V100), $24.48/hr (8x V100). Be prepared to spend $3.06/hr per V100 on Amazon EC2."
      * "recently released V100 instances on Azure are priced competitively at $3.06/hr (1x V100), $6.12/hr (2x V100), $12.24/hr (4x V100).This also comes out to $3.06/hr per V100."
      * "Google charges $0.45/hr (1x K80), $0.90 (2x K80), $1.80/hr (4x K80), $3.60/hr (8x K80). This is clearly the best pricing model for the K80 at half the cost of MS/EC2. Google does not have V100 machines available from what I can tell. Instead they offer their own breed, the TPU which is priced at $6.50/hr per TPU."
  + https://blogs.technet.microsoft.com/machinelearning/2018/01/18/deep-learning-computer-vision-in-the-microsoft-azure-cloud/
  + https://blogs.technet.microsoft.com/machinelearning/2018/02/22/22-minutes-to-2nd-place-in-a-kaggle-competition-with-deep-learning-azure/
  + https://blogs.technet.microsoft.com/machinelearning/2018/03/21/training-state-of-the-art-neural-networks-in-the-microsoft-azure-cloud/


- 2017 
  + https://medium.com/@manikantayadunanda/setting-up-deeplearning-machine-and-fast-ai-on-azure-a22eb6bd6429


- 2016
  + https://www.petri.com/choose-azure-virtual-machine


