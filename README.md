# CNN_Waste_Segregation
## Waste Material Segregation for Improving Waste Management
## Objective
The objective of this project is to implement an effective waste material segregation system using convolutional neural networks (CNNs) that categorises waste into distinct groups. This process enhances recycling efficiency, minimises environmental pollution, and promotes sustainable waste management practices.

## The key goals are:
* Accurately classify waste materials into categories like cardboard, glass, paper, and plastic.
* Improve waste segregation efficiency to support recycling and reduce landfill waste.
* Understand the properties of different waste materials to optimise sorting methods for sustainability.

## Data Understanding
The Dataset consists of images of some common waste materials.

1. Food Waste
2. Metal
3. Paper
4. Plastic
5. Other
6. Cardboard
7. Glass

## Data Description

* The dataset consists of multiple folders, each representing a specific class, such as Cardboard, Food_Waste, and Metal.
* Within each folder, there are images of objects that belong to that category.
* However, these items are not further subcategorised.
  For instance, the Food_Waste folder may contain images of items like coffee grounds, teabags, and fruit peels, without explicitly stating that they are actually coffee grounds or teabags.

## CNN Based Waste Segregation Model Conclusions
### Strengths:

* The model performs well on most classes, especially Cardboard, Food Waste, and Plastic.
* It exhibits a strong overall accuracy of 85.1%, with good precision and recall values for most classes.

### Areas for Improvement:

* The Glass class requires attention, especially improving precision to reduce false positives.
* The Other class might benefit from further tuning to improve both precision and recall.

1. Data Insights:
   - Dataset contains 7625 images across 7 waste categories
   - Class distribution is somewhat imbalanced
   - Image dimensions vary from 256x256 to 256x256
   - Standardized all images to 224x224 for consistent processing

2. Model Architecture:
   - Implemented a CNN with 3 convolutional layers
   - Used batch normalization to stabilize training
   - Applied dropout (0.25-0.5) to prevent overfitting
   - Final model has a dense layer with softmax activation for classification

3. Training Results:
   - Model achieved 61.90% accuracy on the test set
   - Used early stopping to prevent overfitting
   - Learning rate reduction helped fine-tune the model

4. Performance Analysis:
   - Best performing class: Cardboard (F1-score: 0.76)
   - Worst performing class: Other (F1-score: 0.47)

5. Potential Improvements:
   - Collect more data for underperforming classes
   - Experiment with deeper architectures (e.g., ResNet, VGG)
   - Apply more extensive data augmentation
   - Implement transfer learning using pre-trained models
   - Try ensemble methods to improve accuracy

6. Real-world Applications:
   - This model can be integrated into smart waste bins
   - Can assist in automated sorting facilities
   - Could be deployed as a mobile app for educational purposes
   - Helps improve recycling efficiency and reduces environmental impact
