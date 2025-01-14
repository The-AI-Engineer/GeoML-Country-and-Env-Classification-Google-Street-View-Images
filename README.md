# GeoML-Country-and-Environment-Classification-Using-Google-Street-View-Images
This project uses machine learning to classify geographical locations and environmental types (e.g., urban, rural, forest) from Google Street View images. The project focuses on image preprocessing, annotation, feature extraction, and developing classification models.

Key Features and Workflow

1. Data Collection and Processing:
Google Street View API:
Used for the first time to download over 50,000 images.
Generated images based on longitude and latitude coordinates within a 3-mile radius around city centers.
Ensured images:
Were at least 10KB in size to avoid "no image found" errors.
Were spaced at least 10 meters apart to prevent duplicates.
Configured image settings for size, orientation, and outdoor views.
Updated coordinates for each city and saved data with the city's name.

2. Annotation and Preprocessing:
Annotations labeled images by country and environmental category:
Rural, Urban/City, Nature.
Images were cropped, resized, and normalized for consistency.
Applied an 80/10/10 split for training, validation, and testing.

3. Model Development:
Built and trained a Convolutional Neural Network (CNN) for feature learning and classification.
Saved the trained model in H5 format and deployed it temporarily using Gradio on Hugging Face for testing.
The model aimed to allow users to upload an image, with the system predicting the country and environment type.

4. Key Challenges and Learning:
Dataset size (50,000 images) limited the model’s accuracy in distinguishing countries.
The goal was inspired by the popular GeoGuessr game, aiming to use machine learning to identify a location's features.
Recognized the need for millions of images for the model to effectively capture the subtle differences between countries.

5. Results and Insights:
The model showed promising results in distinguishing environmental categories (rural, urban, nature).
Accuracy in differentiating countries was limited due to the small dataset size and insufficient computing power.
Highlighted the importance of larger, more diverse datasets and better hardware for future iterations.
Tools and Dependencies

6. Future Work
Scale Dataset:

Increase the dataset size to millions of images for better feature learning and classification.
Include more countries and environments for improved diversity.
Enhance Model Architecture:

Explore advanced transfer learning models like ResNet, EfficientNet, or Vision Transformers.
Increase Computational Power:

Use cloud computing platforms (e.g., AWS, Google Cloud) for faster and more efficient training.
Improve API Usage:

Automate data collection further to reduce manual updates for each city.
Revisit the Project:
This project was a fantastic learning opportunity, and future iterations will leverage new skills, better hardware, and larger datasets.
