# CMPE-258-Assignment-2
Experimenting with closed and open source LLMs

Demo link: https://youtu.be/lkMRGpMqtaE

----------------------------------------------
OpenAI: 

OpenAI uses an API to access GPT models, the same of which can be acessed through ChatGPT. GPT-4 is considerably more advanced than GPT-3.5, which is used in the colab. GPT-4 is much more complex, and as a result expensive to use. It also has access to make important features such as file reading, and live access to the internet via bing, which allows it to get live information. This is one of its strengths compared to other models such as Llama-2, which only has access to the information is it already trained on, or is manually provided to it.

For example the prompt: "can you get live weather data and give me a forcast for campbell, ca" in GPT-4 gives a full response: "From the National Weather Service: The area is experiencing rain with a temperature around 52°F (11°C), and the humidity is at 76%. The wind speed is coming from the southeast at 9 MPH." Along with additional sources "Weather Underground mentions a current temperature of 56°F at a station in Campbell with partly cloudy conditions. The pressure is at 30.19 in, and visibility is at 10 miles"

With GPT-3.5 it is unable to do so and responds with: 
"I'm sorry for any inconvenience, but as an AI model, I don't have real-time capabilities or access to current data, including weather updates."

Being able to have this live information is one of the most valuable features than OpenAI provides.

It can be used for other topics such as code genration, or writing. It is very strong in this regard due to its size and the data its trained on.

CreativeAI: The system is given instructions to be creative and give unsual responses. This will hopefully give some interesting results that the model would not usually give.

Explain why the earth cannot be flat: The model lists several examples of why the earth cannot be flat in a whimsical tone. The examples are scientifically correct, but their value is in their creativity. These answers could be used to teach children about basic science in a way that is interesting. One of the biggest challenges in science is explaining complex topics to ordinary people who are not experts in the field. Combing the scientific knowledge with the creativity that likely comes from the creative pieces GPT models are trained on can be useful to help make these topic more accessible and more interesting.

This run is contained within the colab.

----------------------------------------------
Create our own code interpreter:

Used a basic tax function to calculate the final price after tax. The schema and form of the data was similar to the sum example. The use of AI in this problem isn't to the actual calculation but instead to transform the request into a form that the function can use to calculate. 

The prompt was: "Use the `get_tax` function to solve this: Value is 30000 and the sales tax is 9.25" 

The values that need to extracted are the price (30000) and the sales tax (9.25), AI simply interprets this sentance and returns the values. The most important part of this is to configure the function prompt to make sure the AI knows which values to return. 

I ran into issues where the AI wanted to keep trying to do the caluation itself and would return:

{
  "a": 30000,
  "b": (30000 * 9.25) / 100
}

and had to change the prompt to make sure it got the correct values. 

The main value in something like this would be to read through documents have unsolved problems and use the AI to put the problems in formats a program can solve. An example would be reading a math textbook and using a calculator to solve each problem. It could be used to quality control to ensure solutions are correct.

----------------------------------------------
Llama:

One of the biggest limitations with running Llama2 is due to memory and storage restrictions in colab it will run out of memory or storage. I was not able to load llama_cpp due to these restrictions, and ran into similar issues with meta's llama models. What I instead chose to use were pipelines to induvidual models. These are much smaller and use fewer resources.

I used "SamLowe/roberta-base-go_emotions" which is a text classifier that does sentiment analysis on text and produces emotion. I ran it on two basic sentances "I am not having a great day" "This assignment is difficult, and things are not working well", and got similar results both classifiying the sentance under dissapointment, sadness, and related emotions.

I ran it on a longer text of an AI-generated announcements of workers being laid off. The model classified the emotion as gratiftude, which indicated that it can handle much longer texts as well.

Something like this is very lightweight, and could be used in companies to scan through meeting transcripts, or chat logs to get a very basic insight into attidudes regarding work. For example if changes are made, and the overall sentiment in company-wide communications tends to be negative, those changes could be reviewed to understand why they lead to the reaction that they have. This could help give managers better insight into employee approval, and help reduce fatigue and turnover.







