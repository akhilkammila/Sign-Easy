# Inspiration
From fewer educational and employment opportunities to social withdrawal and isolation; impaired communication adversely affects the quality of one’s interpersonal and intrapersonal relationships. Thus, overwhelming evidence indicates that it is critical for an individual, just as much as it is instrumental to society, that a means of resolution to enunciated miscommunication is accessible to all. While the lack of access to information may manifest in a multitude of varying ways, a significant factor in one’s potential lacking can be rooted in verbal and misunderstood transmission. In other words, when a discrepancy between what is said and what is heard occurs over a multitude of varying interactions, heavily emotional and professional ramifications birth as a result. Thus, we noticed a need for a solution for educating the mass public on how to use and understand basic ASL. Sign-Easy arose as a result of this.

# What it does
Sign-Easy is a multipurpose AI online platform that converts between ASL and a multitude of international and largely spoken languages. Through a user-friendly digital interface, Sign-Easy is intuitive, efficient, and built upon the objective of accessibility. When users launch the website, they are prompted to the home screen. From the home screen to the translator in the upper tab header, users are able to translate text from a variety of languagesーEnglish, Spanish, French, Hindi, German, Japanese, Korean, Russianーto one of the most universal languages: American Sign Language (ASL). In the "Practice," users can swiftly translate their own ASL directly to English with the ease of one click.

# How sign-easy was built
During the execution of the website, we trained our machine learning model to recognize various letters expressed physically in sign language to increase precision and accuracy in image recognition. Our model was trained using Tensorflow with various datasets that encompassed numerous sign language gestures and physical hand characteristics to maximize object recognition and object classification. For each letter, we inputted 15 images to train the model in recognizing ASL hand patterns. During training, we used imglabel to give each image a corresponding xml file.

(see Image Gallery for snippets of training folders + xml files)

To create our website, we used React on the frontend. On the "Translator" page, we translated from a multitude of internationally spoken languages to English using libretranslate api, and then used conditional rendering to translate the text into ASL. For the "Practice" page, we sent base64 images to our backend, which was run on Flask and deployed on Heroku. Our backend converts the base64 images into a predicted letter result using our machine learning model.

# Challenges
We ran into many challenges throughout this project, especially in terms of the visual ASL to English translation, given the limited amount of time we had. A significant problem was that the model had trouble isolating the user’s hand from the rest of their body and the background. However, these issues were solved by incorporating increasingly diverse and large datasets in training our model. Another issue we ran into was CORS blocking the connection between our frontend and backend. We found a workaround using a CORS proxy server. Being new to nearly all of the technologies we used in our project, we additionally ran into a multitude of technical issues, such as and installing dependencies and deploying our website to Github. We managed to work through each issue by sacrificing sleep.

# Notes to Self
npm run deploy to redeploy the website to gh-pages

### version as of Jul 15th:
Restored to original Jul 3rd commit
Added homepage and scripts to run gh-pages
 
### issue - backend heroku not working
<ost likely cause: heroku free trial ended, or was overloaded with too many requests
Fix: need to make new heroku acc or redeploy backend
 
### if CORS issue arises again - could use cors proxy server

# Improvements
Short-term improvements:
Fixing CORS blocking connection to backend
Adding backend to github

Long-term improvements:
Better machine learning model for improved accuracy
