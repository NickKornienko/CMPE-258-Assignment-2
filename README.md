# CMPE-258-Assignment-2
Experimenting with closed and open source LLMs

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





