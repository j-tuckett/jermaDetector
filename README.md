# Jerma Detector


A Siamese Neural Network built to detect frames of Jerma in youtube videos. The URL for the repo is a link to a shared google drive folder that contains the assets folder, variables folder, fingerprint.pb, keras_metadata.pb, and saved_model.pb files, which were saved automatically by TensorFlow through the model.save() API.

This project originally started as a joke when my friend hid a singular frame of Jerma, a popular Twitch streamer, in a 2.5 hour long Youtube video and said the first person to find it gets cookies. Though someone found it that day, I decided to prepare for future competitions by creating this AI model. It was trained using augmented data of the LFW Dataset, images I collected of Jerma, and lots of images I collected of anything that wasn't a face to make the model more robust in situations when a face wasn't present in the image. 

The final version of the model that I trained achieved an accuracy of 0.979 on its test dataset.

Youtube-DL is used to download the youtube video, with OpenCV being used to feed frames of the video into the model in batches. I optimized the model to process the video at 6x the normal playback speed (the maximum that my friends had achieved while they were manually looking for Jerma was 5x the normal playback speed). 
