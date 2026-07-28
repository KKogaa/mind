## Principles of responsible AI
### Unintended consequences
- Decisions that are wrong
- Decisions that are illegal
- Decisions that cannot be explained by anybody
- Decisions that are harmful to society  at large
tldr: ai isn't explainable and can go out of control (because of too much priviledges)

### Six Principles Should Guide AI Development
- Fairness
- Reliability and safety
- Privacy and security
- Inclusiveness
- Transparency
- Accountability

#### Principle of Fairness
AI systems should treat everyone fairly and avoid affecting similarly situated groups of people in different ways

tldr: ai should treat everyone equally with equal opportunity and avoiding discrimination

#### Principle of Reliability and Safety 
To build trust, it's critical that AI systems operate reliably, safely, and consistently under normal circumstances and in unexpected conditions 

#### Principle of Privacy and Security 
Many countries and regions in the world are developing new standards and laws to try to protect the data of its citizens. Laws are always slower than technology.

#### Principle of  Inclusiveness
At Microsoft, we firmly believe everyone should benefit from intelligent technology meaning it must incorporate and address a broad range of human needs and experiences 

e.g. working for ai voice models to be able to comprehend different types of accents 

#### Principle of Transparency 
When AI systems are used to help inform decisions that have tremendous impacts on people's lives, it is critical that people understand how those decisions were made 

e.g. when someone is rejected by an ai system for a job, life insurance or a bank loan why were they rejected? if you are unable to tell them, the system lack transparency

#### Principle of Accountability 
The people who design and deploy AI systems must be accountable for how their systems operate 

e.g. AI systems should not be the "final authority"  in any decision that has major impact on people's lives (employment, finances, health care, human safety, etc). There should be regular review of how the AI is operating, and regular improvement of the model

### Describe considerations for fairness in an AI solution
#### Fairness
An AI system should produce equitable outcomes for all people, regardless of demographic characteristics such as race, gender, age, disability, religion, or socioeconomic status 

Five different aspects where fairness need to be taken into consideration 
Training data bias
ML model is learning from historical records and based on that it makes predictions, but if there is bias in the historical data, then the AI system will inherit that bias. 

Performance parity
When splitting the training data with the testing data, when testing with people you need to make sure for example that the AI system treats men and female equally, or if the races are treated equally.

Sensitive feature leakage
You shouldn't be able to infer data from training data.

Allocation vs quality of service
AI system shouldn't give better salaries or quality of service based on race

Feedback loops
Using AI output as AI input to try to correct errors will create a feedback loops and will make the errors worse, compounding the errors over time. 

### Describe considerations for reliability and safety in an AI solution
#### Reliability and Safety
An AI system must behave consistently, handle unexpected inputs gracefully, and not cause harm ... whether through failure, misuse, or adversarial attack.





### Describe how generative AI models work
Generative AI models "create new content" such as images, text, audio or code.
Most modern GenAI models are based on deep learning, particularly neural networks trained on large datasets.


### Identify an appropriate AI model based on capabilities

### Identify an appropriate model deployment options 
- Deployed as cloud based services (send requests and receive response over the internet)
- Managed service  (Azure foundry tools)
	- Simplicity
	- Speed
	- Minimal maintenance
- Custom environment (Run them locally)
	- Control over performance
	- Control over security
	- Control over integration

Real time or batch? When do we need the model inference
Latency requirements
Scalability
Configuration parameters, control how the model behaves during inference
- Temperature (controls randomness or deterministic behavior)
- Max tokens
- Top-p (nucleus sampling)
These parameters control the balance between creativity and accuracy
Content filters and safety settings
Monitoring and logging

### Identify scenarios for common AI workloads
#### Generative AI
The goal is to create new human like content, suchas writing text, generating images, or producing code.

#### Agentic AI
The goal is to automate multi-step tasks by combining reasoning, tools, and decision-making.

#### Text analysis (NLP) 
When working with existing text to extract meaning or insights
Example: Sentiment analysis on customer reviews

#### Speech AI
When working with audio input or output
Example: Transcribe an online meeting 

#### Computer vision 
When working with existing images and video
Example: Detecting objects and images

#### Information extraction
When you need to pull structured data from unstructured documents 
Example: input the data from paper/PDF invoices from an external vendor into the accounting system

It's possible that multiple services needed to be connected to perform a workload
Take latency accuracy and cost into consideration
And responsible AI


### Describe common text analysis techniques
Text analysis (NLP) involves using AI to extract meaning and insights from written text

Unstructured text
- Emails
- Product reviews
- Documents
- Tweets
- Scientific papers

Types of techniques: 
- Keyword extraction (highlight important keywords from text)
- Entity detection (extract names, location, date, organization)
- Sentiment analysis (positive, negative or neutral sentiment over product reviews)
- Summarization

Combined techniques (on a prod environment you might need to use multiple of these techniques)

### Identify features of speech recognition and speech synthesis 
#### Speech Recognition (Speech-to-Text) 
Speech recognition converts spoken language into written text.
Use cases:
- Voice assistants
- Speech recognition can identify different languages and accents
- Some systems support real-time transcription for live conversations
- Speaker recognition
#### Speech synthesis (Text-to-Speech)
Speech synthesis converts written teext into spoken audio 
- Respond using a natural-sounding voice
- Navigation systems
- Some systems support neural voices, which use deep learning to produce more realistic speech
- Can train the AI on your own voice

### Identify features of computer vision and image-generation models
#### Computer vision enables AI systems to analyze and understand images and videos
Azure AI Vision Service
Core Features:
- Video analysis (video retrieval, spatial analysis, person counting, person in a zone, person crossing a line, person distance)
- Face (face detection and analysis, face liveness, face identification, face verification)
- Image analysis (image tagging, image classification, objection detection, image captioning, dense captioning, face detection, optical character recognition, image embeddings, and image search)
- Optical character recognition (OCR extracts printed and handwritten text from photos and documents)

#### Image-generation models create new images based on prompts or other inputs 
Foundry GPT-Image-2
### Extract information from text, images, audio and videos
AI systems can extract useful information from many types of data
Convert unstructured data into structured, searchable, and useful information

Extracting information from text (NLP and techniques)
Extracting information from images (OCR, object detection, image classification)
Extracting information from audio
Extracting information from video
Document information extraction

Azure AI document intelligence
The goal is to convert document data into structured information that can be stored in databases or business systems 
Prebuilt document models are available for common document types such as:
- Invoices
- Receipts
- ID cards
- Business cards
Custom models can be trained to extract information from organization-specific forms

### Implement AI solutions by using Microsoft Foundry 
#### Create effective prompts for generative AI models
Prompts are instructions or input given to a GenAI model

Prompt engineering
Well-designed prompts help produce outputs that are more:
- Accurate
- Relevant
- Consistent
- Useful

Two types of prompts:
- System prompts
A system prompt  defines the AI model's overall behavior, role, or rules.
System prompts are usually hidden from the end user and set by the developer.
They help establish:
- Tone
- Personality
- Formatting rules
- Safety boundaries
- Response style
![[Pasted image 20260728140553.png]]
On systems like chatgpt you will not be able to find the system prompt, on foundry you can edit the system prompt.

- User prompts
A user prompt is the direct request entered by the user.
User prompts describe the task the model should perform. e.g. Summarize the attatched document.
Good prompts often include:
- Context
- Desired output format
- Constraints
- Examples

Prompt engineering techniques
- Be specific about the task and expected output
- Provide context to improve relevance
- Define the desired format
- Use examples when possible
- Break complex tasks into smaller steps for more reliable responses

Using prompts in Foundry
In Microsoft Foundry, prompts can be tested and refined directly within the development environment.
Prompt design is a key skill when building generative AI applications and AI agents.

#### Deploy a model and interact with it in the Foundry portal
First you will have to create project after login to the Azure Foundry for the first time, if not choose an existing project 
![[Pasted image 20260728141240.png]]

After creating the project switch over to the discover tab, and select the models.
![[Pasted image 20260728141339.png]]

After picking the model you will see the model card, showing the capabilities of the model, pricing, context window, token limits.
![[Pasted image 20260728141519.png|697]]

![[Pasted image 20260728141639.png]]

#### Create a lightweight chat client application by using the Foundry SDK
![[Pasted image 20260728142135.png]]

![[Pasted image 20260728142159.png]]

![[Pasted image 20260728142337.png]]

![[Pasted image 20260728142436.png|691]]

A Foundry resource provides unified access to models, agents, and tools. This article explains which SDK and endpoint to use for your scenario.
The Foundry SDK is a thin-client SDK that exposes all of the Foundry project APIs through a single project endpoint. 
Higher-level SDKs build on it for example, the Agent Framework foundry package depends on the Foundry SDK to access Foundry models, tools, and project configuration.
Choose your SDK:
- Use Foundry SDK when building apps with agents, evaluations, or Foundry specific features
- Use Agent Framework for hosted agents or multi-agent systems in code
- Use OpenAI SDK when maximum OpenAI compatibility or lowest latency is requered, when generating embeddings, or when using Foundry direct models via Chat Completions
- Use Anthropic SDK when working with Anthropic Claude models deployed in Foundry
- Use Foundry Tools SDKs (Prebuilt solutions vision, speech, content safety and more) when working with specific AI services.

Run this command to install the packages for Foundry projects
pip install "azure-ai-projects>=2.0.0"

The Foundry SDK exposes two client types because Foundry and OpenAI have different API shapes
- Project client: use for Foundry  native operations where OpenAI has no equivalent
Example: listing connections, retrieving project properties, enable tracing
- OpenAI-compatible client: Use for Foundry functionality that builds on OpenAI concepts. The Responses API, agents, evaludations, and fine tuning all use OpenAI style request/response patterns.

Using Foundry SDK code example:

![[Pasted image 20260728144008.png]]

Using OpenAI SDK code example:
![[Pasted image 20260728144151.png]]

Using Anthropic SDK code example:
![[Pasted image 20260728144234.png]]

Python supported Foundry tools
- Speech
Add speech to text, text to speech, translation, and speaker recognition capabilities to applications
- Language
Build applications with natural language understanding capabilities. Language detection, pii detection, text analytics for health, sentiment analysis, opinion mining, key phrase extraction, summarization, entity linking, CQA, and CLU. 
- Translator
- Azure AI Search
- Content Safety
- Document Intelligence
- Vision
#### Create and test a single-agent solution in the Foundry portal 
On Foundry go to agents create agent
![[Pasted image 20260728144629.png]]

From there you can select models, system prompt, tools the agent can use.
![[Pasted image 20260728144711.png]]

Attatch Google Drive as a tool for the model
![[Pasted image 20260728144938.png]]
#### Create a lightweight client application for an agent

Using the azure ai project client
![[Pasted image 20260728145152.png]]

![[Pasted image 20260728145232.png]]

![[Pasted image 20260728145258.png]]
![[Pasted image 20260728145331.png]]




















