# Sign Easy

## 💡 Inspiration
Millions of people with impaired communication abilities rely on sign language to communicate with others. However, most people have no sign language knowledge in the slightest. We noticed a need for educating the mass public on how to use and understand basic ASL. Sign-Easy arose as a result of this.

## 💻 What it does
Sign-Easy is a multipurpose AI online platform that converts between ASL and a multitude of international and largely spoken languages. When users launch the website, they are prompted to the home screen. From the home screen to the translator in the upper tab header, users are able to translate text from a variety of languagesーEnglish, Spanish, French, Hindi, German, Japanese, Korean, Russianーto one of the most universal languages: American Sign Language (ASL). In the "Practice," users can swiftly translate their own ASL directly to English in just one click.

## 🔨 How we built it
During the execution of the website, we trained our machine learning model to recognize various letters expressed physically in sign language to increase precision and accuracy in image recognition. Our model was trained using Tensorflow with various datasets that encompassed numerous sign language gestures and physical hand characteristics to maximize object recognition and object classification. For each letter, we inputted 15 images to train the model in recognizing ASL hand patterns. During training, we used imglabel to give each image a corresponding xml file.

To create our website, we used React on the frontend. On the "Translator" page, we translated from a multitude of internationally spoken languages to English using libretranslate api, and then used conditional rendering to translate the text into ASL. For the "Practice" page, we sent base64 images to our backend, which was run on Flask and deployed on Heroku. Our backend converts the base64 images into a predicted letter result using our machine learning model.

## 🔜 What's next for Sign Easy

We would like to expand the number of sign language words that our machine learning algorithm can predict. Practically, it would be best to replace our own machine learning model with a large-scale pre-built model. This would save months of image collection and model training time.

We would also like to advertise our website and grow its user base. Down the road, we could explore monetization with advertisements.

## Try It OUT!
[Youtube Link](https://www.youtube.com/watch?v=L3NoBqH5a7g&ab_channel=AkhilKammila)
<br />
[Live App](https://akhilkammila.github.io/signeasy-app/)
