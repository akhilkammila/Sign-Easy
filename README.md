# Sign Easy 🤟 🎉
[Video Demo](https://www.youtube.com/watch?v=L3NoBqH5a7g&ab_channel=AkhilKammila)
<br />
[Live App](https://akhilkammila.github.io/Sign-Easy/)
(because heroku free trial ran out, the backend is not deployed and the "practice" tab is not working)

## 💡 Inspiration
Millions of people with impaired communication abilities rely on sign language to communicate with others. However, most people have no sign language knowledge in the slightest. We noticed a need for educating the mass public on how to use and understand basic ASL. Sign-Easy arose as a result of this.

## 💻 What it does
- Sign-Easy is a one-stop shop for basic ASL learning
- Users can type in any word, and see how to sign it in American Sign Language (ASL). Our website supports not only English, but Spanish, French, Hindi, German, Japanese, Korean, and Russian.
- Users can practice their ASL on our website. We take in their video feed – and use our machine learning model to translate their hand gestures into English. Users can see if their intended sentences were signed correctly. 

## 🔨 How we built it
We trained a machine learning model using Tensorflow and self-collected images. For each letter, we inputted 15 images to train the model to recognizing ASL hand patterns. During training and image collection, we used Python and Tensorflow, OpenCV, and ImgLabel.

To create our website, we used React on the frontend. We translated from international languages to English using the libretranslate api. To enable real-time signlanguage detection, we connected to a Flask backend deployed on Heroku. Our backend converts base64 images into a predicted letter result using our machine learning model.

## 🔜 What's next for Sign Easy

We would like to expand the number of sign language words that our machine learning algorithm can predict. Practically, it would be best to replace our own machine learning model with a large-scale pre-built model. This would save months of image collection and model training time.

We would also like to advertise our website and grow its user base. Down the road, we could explore monetization with advertisements.
