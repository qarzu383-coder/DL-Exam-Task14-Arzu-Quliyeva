​Student ID: 14
•​Name: Quliyeva Arzu Kamran
​•Task: 14 Flowers Recognition
•​Seed: 20240214

Presentation 



Architecture
•​Base Model: torchvision.models.resnet18(weights='IMAGENET1K_V1')
•​Configuration: Freeze all layers (requires_grad=False)
•​Final Layer: model.fc = Linear(512, 5)
•​Training: Only the final fc layer is trained

Training Configuration
​Two versions were compared:
▪︎​Version 1:
  •​Optimizer: Adam
  •​Learning Rate: 0.0001
  •​Batch Size: 32
  •​Epochs: 10
▪︎​Version 2 (Option C):
  •​Optimizer: SGD (momentum=0.9)
  •​Learning Rate: 0.001
  •​Batch Size: 32
  •​Epochs: 10
  
Deliverables
​1.Training comparison plot (Version 1 vs Version 2 curves)
​2.Comparison table with both accuracies
​3. Confusion matrix from best model (5x5)
4​.10 sample predictions: image, true label, predicted label

Results
Version Final Accuracy
Version 1 ~83.2%
Version 2 ~90.5%

Analysis
​Version 2 (Option C) better and why:
Version 2 performed better because SGD with momentum provided more stable optimization for the final layer of the pre-trained ResNet model compared to Adam. The learning rate of 0.001 in Version 2 allowed the model to converge more effectively and exceed the target accuracy of 85%.
















