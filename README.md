# textchecks
#[Devpost](https://devpost.com/software/textchecks)
## 💡**Inspiration**
The apparent rise of mental health crises in post-secondary institutions over the past few years has unveiled a small part of a long existing issue. University students have always seemed a bit sad, but in all of history, it’s never been this bad. With 1 in 5 seriously contemplating suicide in the last year and nearly half in Ontario reporting unmet mental health needs, we could all use a caring, conventional, and confidential friend who points you in the right direction and answers any questions you may have. In creating TextChecks, our hope is to connect students to a system they can depend on as they undertake the process of understanding their identity and place in the world.

## 🧠**What it does**
TextChecks is an Azure conversational AI that can find local supports for students and answer any mental health questions by pulling from our database of three hundred medical articles and two common therapy workbooks. It can be accessed through SMS or our web interface. Users simply begin sending START and follow the prompts accordingly. It follows a phased approach and guides the user through viewing resources on their mental health topic of interest, learning about available supports near them, and free-for-all Q&A for any other questions they may have.

## 💻**How we built it**
The front-end of our web interface was built with HTML, CSS, JavaScript, and BootStrap. We use a Twilio API to enable text messaging and use the Azure Bot Service’s provided elements for the web chatbox. To generate all of our responses, we used Azure Cognitive Search and Language Studio to extract question-answer pairs from three hundred medical articles and two common therapy workbooks to train the model. When there isn’t a direct match, it parses over the full contents of each article and book to pick the best match. 

## ❓**Challenges we ran into**
Our primary challenge was implementing the phased approach through the chatbot. Deciding the user flow and how we wanted information to be accessed was a significant factor in our application. We spent the most time with flow diagrams and maps, determining how users may interact with the application and translating it into Azure. Another challenge was ensuring data quality and ensuring our question-answer pairs had high confidence levels. In the beginning, we started with importing self-help books, but found that our question-answer pairs were often inaccurate. Instead, we opted for peer-reviewed medical articles and therapy workbooks that provided better pairing. We also wanted our application to work on desktop as well as mobile, and spent time tinkering with our front-end to ensure responsive design.

## 💗**Accomplishments that we're proud of**
1. Although some of us have created chatbots in the past, TextChecks exceeds their capabilities and utilizes additional technologies to offer a more personalized experience. 
2. It can be difficult to control the quality of responses from the bot, but we are satisfied with our approach in creating more accurate question-answer pairs.
3. Our user interface is clean, simple, and easy to use. Our animated homepage is a bonus!
4. It was our first time working with the Twilio API and we were able to get our chatbot working in SMS in under 30 minutes!

## 📚**What we learned**
We thoroughly explored Azure Bot Service, Language Studio and Azure Cognitive Search to create our application, by seeing how their capabilities best fit with our desired application features. We also learned how to train our bot with quality data, as well as connect it to SMS!

## 🚘**What's next for TextChecks**
In the future, we hope to have users calling into an automated phone system enabled by Natural Language Understanding and text-to-speech services. We can also partner with universities themselves, connecting with databases and exam schedules to pre-emptively reach out to stressed students. Finally, we can work together with Kids Help Phones and other textable lines to help lighten their basic question-and-answer load and potentially reroute in distress to their counselors. 
