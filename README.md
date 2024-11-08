# Face-Recognition-System
(View master branch for code)

For our Facial Recognition System, we used MTCNN (a Deep Learning model) for face detection which detected and recognised images from the dataset, along with FaceNet (a Deep Learning Model) for creating embeddings of the dataset of different faces. SVM (a Machine Learning model) was used as the classifier to differentiate between the arrays. The language used was Python. We used a dataset for this project and trained the models accordingly, producing successful results.

-MTCNN model (Deep learning) is used to locate faces in images. It will identify coordinates of a face within an image. For each image, the model will extract the region containing the face (bounding box) so that the model focuses on the face only. 

-FaceNet model (Deep learning) will convert the face (after it is detected) into a numerical representation called an embedding. The embedding is a representation of the face’s unique features. Face embeddings generated for each image in the dataset are saved. Similar faces will have embeddings close to each other.

-SVM model (Machine learning) will learn and recognize different faces based on their embeddings. The SVM will classify a face embedding as belonging to a specific person (from the training data). Previously after generating all embeddings for the faces, the embeddings have been labelled with the identity of the person. SVM model is trained on this labelled dataset of embeddings. During training, it learns the boundaries that separate the embeddings of different individuals. After training, when a new face is detected and converted into an embedding, the SVM classifier can predict which person the face likely belongs to by checking where the embedding falls in relation to the learned boundaries.
