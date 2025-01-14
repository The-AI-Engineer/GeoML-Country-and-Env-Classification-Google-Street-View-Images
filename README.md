# GeoML-Country-and-Environment-Classification-Using-Google-Street-View-Images

This project shows the power of machine learning in geographic and environmental classification. Using Google Street View images, we built a model to classify images by country and environment type (e.g., urban, rural, nature). Incorporating data collection, preprocessing, annotation, and model development with real-world applications inspired by GeoGuessr.

Objective

Create models to classify images by country and environment type.
Build a user-friendly system where users can upload images, and the model predicts location characteristics.

Key Features and Workflow

1. Data Collection and Processing:
Google Cloud Platform and Street View API:
Collected 50,000 images using longitude and latitude coordinates.
Generated images within a 3-mile radius of city centers while ensuring:
Minimum file size of 10KB to filter valid images.
Minimum spacing of 10 meters between image coordinates to prevent duplicates.
Settings ensured outdoor images, but some indoor images were occasionally captured.
Dynamic Updates:
Only the coordinates and city name in the script needed updating for new locations.
Temporary storage tracked processed images.

2. Annotation and Preprocessing:
Manual Annotations:
Images labeled with country and environment type (e.g., rural, urban, nature).
Image Augmentation:
Techniques like flipping, rotation, and scaling were applied to increase data variability.
Data Splitting:
Followed an 80/10/10 split for training, validation, and testing.

3. Model Development:
Convolutional Neural Network (CNN):
Custom architecture built for feature extraction and classification.
Model saved in H5 format for reusability.
Transfer Learning:
Leveraged pre-trained models like ResNet for advanced feature learning.
Deployment:
Integrated with Gradio and deployed on Hugging Face for temporary user testing.

4. Evaluation and Results:
Metrics:
Evaluated using accuracy, precision, recall, and F1-score.
Visualizations:
Confusion matrices, learning curves, and PCA plots to explain the model’s performance.
Insights:
Promising results in distinguishing environmental types (e.g., rural vs. urban).
Limited accuracy in country classification due to dataset size.

5. Learning Outcomes:
Gained hands-on experience with:
Google Cloud Platform and API usage for large-scale image collection.
CNN model design and deployment with limited computational resources.
Managing and processing datasets with thousands of images.
Recognized the importance of dataset scale and computing power in machine learning projects.


Real-World Application:
Potential use cases include geographic research, environmental monitoring, and educational tools.

Challenges Faced:
Dataset size (50,000 images) limited the model’s accuracy for country classification.
Significant computational power is required for training with millions of images.

Future Work
Expand Dataset:
Collect millions of images for more accurate country classification.

Optimize Models:
Use advanced architectures like EfficientNet or Vision Transformers.

Enhance User Experience:
Develop a more robust interface for real-time location predictions.

Cloud-Based Scaling:
Use AWS or Google Cloud for distributed training on larger datasets.
