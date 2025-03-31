M: All right welcome everyone to the Deep dive today we're uh taking a deep dive into something pretty huge foundational large language models or llms and how they create text I mean it seems like they're popping up everywhere right changing how we write code how we even write stories.

W: Yeah the advancements have been uh incredibly fast it's hard to keep up for this deep dag we're going all the way up to February 2025 so we're talking Cutting Edge stuff.

M: Yeah seriously Cutting Edge so our mission today is to um to still all that down right get to the core of these llms what are they made of how do they evolve you know how do they actually learn of course how do we even measure how good they are we're going to look at all that even some of the tricks used to uh make them run faster it's a lot to cover but hopefully we can make it uh make it a fun ride. You know the starting point for all this the foundation of most modern llms is the Transformer architecture and it's actually kind of funny it came from a Google project focused on language translation back in 2017.

W: Okay so this Transformer thing I remember hearing about that the original one had this encoder and decoder right like it would take a sentence in one language and turn it into uh another language.

M: Yeah exactly so the encoder would take the input you know like a sentence in French and create this representation of It kind of like a summary of the meaning then the decoder uses that representation to generate the output like the English translation piece by piece and each piece they call it a token it could be a whole word like cat or part of word like pre and prefix but the real magic is what happens inside each lay layer of this Transformer thing.

W: All right well let's get into that magic what's actually going on in a Transformer layer.

M: So first things first the input text needs to be prepped for the model right we turn the text into those tokens based on a specific vocabulary the model uses and inch of these tokens gets turned into this dense Vector we call it an embedding that captures the meaning of that token but and this is important Transformers process all the tokens at the same time so we need to add in some information about the order they appeared in the sentence that's called positional encoding and there are different types of positional encoding like sinodal and learned encodings the choice can actually subtly affect how well the model understands longer sentences or longer sequences of text.

W: Makes sense otherwise it's like just throwing all the words in a bag you lose all the structure. Then we get to I think the most famous part the multi-head attention I saw this thirsty tiger example I thought was uh pretty helpful to try and understand self attention.

M: Oh yeah the Thirsty tiger a classic so the sentence is the tiger jumped out of a tree to get a drink because it was thirsty now self attention it's what lets the model figure out that it refers back to the tiger and it does this by uh creating these vectors query key and value vectors for every single word.

W: Okay so wait let me let me try this so it that would be the query it's like asking hey which other words in this sentence are important to understanding me.

M: Yeah you got it and the key it's like a label attached to each word telling you what it represents then the value that's the actual information the word carries so like it looks at all the other words keys and sees that the Tiger has a key that's really similar so it pays more attention to the tiger.

W: Exactly and the model calculates this score you know for how well each query matches up with all the other Keys then it normalizes these scores so they become weights attention weights these weights tell you how much each word should pay attention to the others then it uses those weights to create a weighted sum of all the value vectors and what you get is this Rich representation for each word which takes into account its relationship to every other word in the sentence and the really cool part is all of this all this comparison and calculation happens in parallel using these matrices for the query q key K and value V of all the tokens this ability to process all these relationships at the same time is a huge reason why Transformers are so good at capturing these subtle meanings in language that previous models you know the sequential ones really struggled with especially across longer distances within a sentence.

M: Okay I think I'm starting to get it and multi-edges means doing the self attention thing like several times at the same time right but with different sets of those query key and value matrices.

W: Yes and each head each of these parallel self- attention processes learns to focus on different types of relationships one head might look for grammatical stuff another one might focus on the uh the meaning connections between words and by combining all those different views you know those different perspective the model gets this much deeper understand understanding of what's going on in the text it's like getting a second opinion or a third or a fourth it's powerful stuff.

M: Now I also saw these terms layer normalization and residual connections they seem to be important for uh keeping the training on track especially when you have these really Jeep networks.

W: Oh they're essential layer normalization it helps to keep the activity level of each layer you know the activations at a steady level that makes the training go much faster and usually gives you better results in the end residual connections they act like shortcuts you know within the network it's like they let the original input of a layer bypass everything and get added directly to the output so it's a way for the network to remember what it learned earlier even if it's gone through many many layers.

M: Exactly that's why they're so important in these really deep models it prevents that Vanishing Radiance problem where the signal gets weaker and weaker as it goes deeper then after all that we have the feed forward layer right.

W: The feed forward layer yeah it's this network a feed forward Network that's applied to each token's representation separately after we've done all that attention stuff it usually has two linear Transformations with a what's called a nonlinear activation function in between like relu or gelu this gives the model even more power to represent information helps it learn these complex functions of the input.

M: So we've talked about encoders and decoders in the original Transformer design but I noticed in the materials that many of the newer llms they're going with a decoder only architecture what's the advantage of just using the decoder.

W: Well you see when you're focused on generating texts like writing or having a conversation you don't always need the encoder part the encoder's main job is to create this representation of the whole input sequence up front decoder only models they kind of skip that step and directly generate the output token by token they use this special type of self- attention called masked self- attention it's a way to make sure that uh when the model is predicting the next token it can only see the tokens that came before it you know just like when we write or speak so it's a simpler design and it makes sense for generating text.

M: Exactly and before we move on from architecture there's one more thing um mixture of experts or Moi it's this really clever way to make these models even bigger but without making them super slow.

W: I was just going to ask about that how do you make these massive models more efficient Moi seems to be a key part of that.

M: It really is so in Moi you have these specialized submodels these experts right and they all live within one big model but the trick is is there's this gating Network that decides which experts are the best ones to use for each input so you might have a model with billions of parameters but for any given input only a small fraction of those parameters those experts are actually active it's like having a team of Specialists and you only call in the ones you need for the specific job.

W: Makes sense yeah it's all about efficiency now I think it would be good to step back and look at the big picture how llms have evolved over time you know the Transformer was the spark but then things really started taking off.

M: Yeah there's this whole family tree of llms now where did it all begin after that first Transformer paper.

W: Well GPT one from open AI in 2018 was a real turning point it was decoder only and they trained it in an unsupervised way on this massive data set of books they called it books scorpus this unsupervised pre-training was key it let the model learn General language patterns from all this raw text then they would fine-tune it for specific Tas but gpt1 had its limitations right.

M: I remember reading that sometimes it would get stuck repeating the same phrases over and over.

W: Yeah I wasn't perfect sometimes the text would get a bit repetitive and it wasn't so good at long conversations but it was still a major step then that same year Google came out with Bert now Bert was different it was encoder only and its focus was on understanding language not generating it it was trained on these tasks uh like massed language modeling and next sentence prediction which are all about figuring out the meaning of text.

M: So gpt1 could talk but sometimes it would get stuck and Bert could understand but couldn't really hold a conversation.

W: That's a good way to put it then came gpt2 in 2019 also from open AI they took the gpt1 idea and just scaled it up way more data from this data set called Web text which was taken from Reddit and many more parameters in the model itself the result much better coherence it could handle longer dependencies between words and the really cool thing was it could learn new tasks without even being specifically trained on them they call it zero shot learning you just show it an example of the task in the prompt and it could often figure out how to do it.

M: Whoa just from an example that's amazing.

W: It was quite a leap and then starting in 2020 we got the gpt3 family these models just kept getting bigger and bigger billions of parameters gpt3 with its 175 billion parameters it was huge and it got even better at fuse shot learning learning from just a handful of examples we also saw these instruction tune models like instruct GPT trained specifically to follow instructions written in natural language then came models like GPT 3.5 which were amazing at understanding and writing code and GPT 4 that was a GameChanger a truly multimodal model it could handle images and text together the context window size also exploded meaning it could consider much longer pieces of text at once.

M: And Google they were pushing things forward as well right I remember Lambda their conversational AI was a big deal.

W: Absolutely Lambda came out in 2021 and it was designed from the ground up for natural sounding conversations while the gpts were becoming more general purpose Lambda was all about dialogue and it really showed then Deep Mind got in on the action with gopher in 2021.

M: Gopher what made that one Stand Out.

W: Gopher was another big decoder only model but deep mine they really focused on using highquality data for training a data set they called massive text and they also used some pretty Advanced optimization techniques gopher did really well on knowledge intensive tasks but it still struggled with um more complex reasoning problems one interesting thing they found was that that just making the model bigger you know adding more parameters doesn't help with every type of task some tasks need different approaches.

M: Right it's not just about size then there was Jam from Google which used this mixture of experts idea we were talking about earlier making those huge models run much faster.

W: Exactly Graham showed that you could get the same or even better performance than a dense model like gpt3 but use way less compute power it was a big step forward in efficiency then came chinchilla in 2022 also from deepmind they really challenge those scaling laws you know the idea that bigger is always better.

M: Yeah chinell was a really important paper they found that for a given number of parameters you should actually train on a much larger data set than people were doing before they had this 70 billion parameter model that actually outperformed much larger models because they trained it on this huge amount of data it really changed how people thought about scaling.

W: So it's not just about the size of the model it's also about the size of the data you train it on.

M: Yeah exactly and then Google released uh paulm and paulm 2 paulm came out in 2022 and had really impressive performance on all kinds of benchmarks part of that was because of Google's pathway system which made it easier to scale up models efficiently pollen 2 came out in 2023 and it was even better at things like reasoning coding and math even though it actually had fewer parameters than the first PM Palm 2 is now the foundation for a lot of Google's uh generative AI stuff in Google cloud.

W: And then we have Gemini Google's newest family of models which are multimodal right from the start.

M: Yeah Gemini is really pushing the boundaries it's designed to handle not just text but also images audio and video they've been working on architectural improvements that let them scale these models up really big and they've optimized Gemini to run really fast on their tensor processing units tpus they also use Moi in some of the Gemini models there are different sizes to ultra pro nano and Flash each for different needs. Gemini 1.5 Pro with its massive context window that's been particularly impressive it can handle millions of tokens which is incredible.

W: It's mindboggling how fast these context windows are growing what about the open source side of things there's a lot happening there too right.

M: Oh absolutely the open source llm Community is exploding Google released Gemma and Gemma 2 in 2024 which are these lightweight but very powerful open models building off of their Gemini research Gemma has a huge vocabulary and there's even a two billion parameter version that can run on a single GPU so it's much more accessible Gemma 2 is performing comparably to much bigger models like meta llama 370b. Meta llama family has been really influential starting with llama 1 then llama 2 which had a commercial use license and now llama 3 they've been improving in areas like reasoning coding general knowledge safety and they've even added multilingual and vision models in the Llama 3.2 release mistal AI they have mixol which uses a sparse mixture of experts set up eight experts but only two are active at any given time it's great at math coding and multilingual tasks and many of their models are open source then you have open AI 01 models which are all about complex reasoning they're getting top results in these really challenging scientific reasoning benchmarks deep seek has also been doing some really interesting work on reasoning using this new reinforcement learning technique called group relative policy optimization their deep seek R1 model is comparable to open ai's 01 on many tasks although it's still closed Source even though they release the model weights and Beyond those there are tons of other open models being developed all the time like cu 1.5 from Alibaba ye from U1 Ai and grock 3 from XII it's a really exciting space but it's important to check the licenses on those open models before you use them.

W: Yeah keeping up with all these models is a full-time job in itself it's incredible.

M: It is and you know all these models all these advancements they're all built on that basic Transformer architecture we talked about earlier right but these foundational models they're powerful but they need to be tailored for specific tasks and that's where fine-tuning comes in.

W: Exactly so training in llm US usually involves two main steps first you have pre-training you feed the model tons and tons of data just raw text No Labels this lets it learn the basic patterns of language how words and sentences work together it's like learning the grammar and vocabulary of a language pre-training is super resource intensive it takes huge amounts of compute power it's like giving the model a general education in language.

M: Exactly then comes fine-tuning you take that pre-trained model which has all that General knowledge and you train it further on a smaller more targeted data set this data set is specific to the task you want it to do like translating languages writing different kinds of creative text formats or answering questions so you're specializing the model making it an expert in a particular area.

W: And supervis fine-tuning or sft that's one of the main techniques use for this right.

M: Yeah sft is really common it involves training the model on labeled examples where you have a prompt and the desired response so for example if you want it to answer questions you get lots of examples of questions and the correct answers this helps the model learn how to perform that specific task and also helps to shape its overall Behavior so you're not just teaching it what to do you're also teaching it how to behave.

W: Exactly you want it to be helpful safe and good at following instructions and then there's reinforcement learning from Human feedback or rhf this is a way to make the model's output more aligned with what humans actually prefer.

M: I was wondering about that how do teach these models to be you know more humanlike in their responses.

W: Well rhf is a big part of that it's not just about giving the model correct answers it's about teaching it to generate responses that humans find helpful truthful and safe they do this by training a separate reward model based on human preferences so you might have human evaluators rank different responses from the llm you know telling you which ones they like better then this reward model is used to fine-tune the llm using reinforcement learning algorithms so the llm learns to generate responses that get higher rewards from the reward model which is based on what humans prefer there are also some newer techniques like reinforcement learning from AI feedback rla aif and direct preference optimization DPO that are trying to make this alignment process even better.

M: It's fascinating how much human input goes into making these models uh more humanlike.

W: Now fully fine-tuning these massive models it sounds computationally expensive are there ways to you know adapt them to new ask without having to retrain the whole thing.

M: Yeah that's a good point fully fine-tuning these huge models it can be really expensive so people have developed these techniques called parameter efficient fine-tuning or PFT the idea is to only train a small part of the model leaving most of the pre-trained weights Frozen this makes fine-tuning much faster and cheaper.

W: So it's like just making small adjustments instead of overhauling the entire system yeah what are some examples of these pea techniques.

M: One popular method is adapter-based fine tuning you add these small modules called adapters into the model and you only train the parameters within those adapters the original weights stay the same another one is low rank adaptation or Laura in Laura you use low rank matrices to approximate the changes you would make to the original weights during full fine tuning this drastically reduces the number of parameters you need to train there's also Cura which is like Laura but even more efficient because it uses quantized weights and then there's soft prompting where you learn the small Vector a soft prompt that you add to the input this soft prompt helps the model perform the desired task without changing the original weights.

W: So it sounds like there are several different approaches toine tuning and each one has its own trade-offs between performance cost and efficiency.

M: Exactly and these PF techniques are making it possible for more people to use and customize these powerful llms it's really democratizing the technology now once you have a fine-tuned model how do you actually use it effectively brumpt engineering seems to be key skill here.

W: Oh it's absolutely essential prompt engineering is all about designing the input you give to the model The Prompt in a way that gets you the output you're looking for it can make a huge difference in the quality and relevance of the model's response.

M: So what are some good prompt engineering techniques.

W: There are a few that are really commonly used zero shot prompting is where you give the model a direct instruction or question without giving it any examples you're relying on its pre-existing knowledge F shot prompting is similar but you give it a few examples to help it understand the format and style you're looking for and for more complex reasoning tasks Chain of Thought prompting is really useful you basically show the model How to Think Through the problem step by step which often leads to better results.

M: It's like teaching it how to break down a complex problem into smaller more manageable steps.

W: Exactly and then there's the uh the way the model actually generates text the sampling techniques these can have a big impact on the quality creativity and diversity of the output.

M: Yeah I was curious about that what are some of the different sampling techniques.

W: Well the simplest is greedy search where the model always picks the most likely next token this is fast but can lead to repetitive output random sampling as the name suggests introduces more Randomness which can lead to more creative outputs but also a higher chance of getting nonsensical text temperature is a parameter you can adjust to control this Randomness higher temperature more Randomness topk sampling limits the model's choices to the top K most likely pokin which helps to control the output top P sampling also called nucleus sampling is similar but uses a dynamic threshold based on the probabilities of the tokens and finally best of end sampling generates multiple responses and then picks the best one based on some criteria.

M: So fine-tuning these sampling parameters is key to getting the kind of output you want whether it's factual and accurate or more creative and imaginative.

W: Yeah it's a powerful tool now I think it's time we talk about how we actually know if these models are any good how do we evaluate their performance.

M: That's a great question question evaluating these llms it's not like traditional machine learning tasks where you have a clear right or wrong answer how do you measure something as subjective as you know the quality of generated text.

W: It's definitely challenging especially as we're trying to move Beyond uh you know those early demos to real world applications those traditional metrics like accuracy or F1 score They Don't Really capture the whole picture when you're dealing with something as open-ended as text generation.

M: So what does a good evaluation framework look like for l it needs to be multifaceted that's for sure first you need data specifically designed for the task you're evaluating this data should reflect what the model will see in the real world and should include real user interactions as well as synthetic data to cover all kinds of situations second you can't just evaluate the model in isolation you need to consider the whole system it's part of like if you're using retrieval augmented generation r or if the llm is controlling an agent and lastly you need to Define what good actually means for your specific specific use case it might be about accuracy but it might also be about things like helpfulness creativity factual correctness or adherence to a certain style.

W: It sounds like you need to tailor your evaluation to the specific application what are some of the main methods used for evaluating llms.

M: We still use traditional quantitative methods you know comparing the model's output to some grown truth answers using metrics like Blu or Rouge but these metrics don't always capture the nuances of language sometimes a creative or unexpected response might be just as good or even better than the expected one that's why human evaluation is so important human reviewers can provide more nuanced judgments on things like fluency coherence and overall quality but of course human evaluation is expensive and timec consuming so people have started using llm powered aerators.

W: So you're using AI to judge other AI.

M: Exactly it sounds strange but it can be quite effective you basically give the aerator model the task the evaluation criteria and the responses generated by the model your testing the aerator then gives you a score often with a reason for its judgment there are different types of aerators too generative models reward models and discriminative models but one important thing is that you need to calibrate these aerators meaning you need to compare their judgments to human judgments to make sure they're actually measuring what you want them to measure you also need to be aware of the limitations of the autter rator model itself and there are even more advanced approaches being developed like breaking down tasks into subtasks and using rubrics with multiple criteria to make the evaluation more interpretable this is especially useful for evaluating multimodal generation where you might need to assess the quality of the text images or videos separately.

W: It sounds us evaluation is a complex area but really important for making sure these models are reliable and actually useful in the real world.

M: Now all these models they can be incredibly large and getting responses from them can take time what are some ways to speed up the inference process you know make them respond faster.

W: Yeah as these models get bigger they also get slower and more expensive to run so optimizing inference the process of generating responses is really important especially for applications where speed is critical.

M: So what are some of the techniques used to accelerate inference.

W: Well there are different approaches but a lot of it comes down to trade-offs you often have to balance the quality of the output with the speed and cost of generating it so sometimes you might sacrifice little accuracy to gain a lot of speed.

M: Exactly and you also need to consider the tradeoff between the latency of a single request you know how long it takes to get one response and the overall throughput of the system how many requests it can handle per se the best approach depends on the application now we can broadly categorize these techniques into two groups there are the output approximating methods which might involve changing the output slightly to gain efficiency and then there are the output preserving methods which keep the output exactly the same but try to optimize the computation.

W: Let's start with the output approximating methods I know quantization is a popular technique.

M: Yeah quantization is all about reducing the numerical Precision of the models weights and activations so instead of using 32-bit floating Point numbers you might use 8 bit or even four bit integers this saves a lot of memory and makes the calculations faster often with only a very small drop in accuracy there are also techniques like quantization aware training qat which can help to minimize those accuracy losses and you can even fine-tune the quantization strategy itself.

W: What about distillation isn't that where you train a smaller model to mimic a larger one.

M: Yes distillation is another way to improve efficiency you have a large accurate teacher model and you train a smaller student model to copy Its Behavior the student model is often much faster and more efficient and it can still achieve good accuracy there are a few different distillation techniques like data distillation knowledge distillation and on policy distillation.

W: Okay those are the methods that might change the output a little bit what about the the output preserving methods I've heard of flash attention.

M: Flash attention is really cool it's specifically designed to optimize the self attention calculations within the Transformer it basically minimizes the amount of data movement needed during those calculations which can be a big bottleneck the great thing about Flash attention is that it doesn't change the results of the attention computation just the way it's done so the output is exactly the same.

W: And prefix caching that seems like a good trick for conversational applications.

M: Yeah prefix caching is all about saving time when you have repeating parts of the input like in a conversation where each turn Builds on the previous ones you cache the results of the attention calculations for the initial part of the input so you don't have to redo them for every turn Google AI studio and vertex AI they both have features that use this idea.

W: So it's like remembering what you've already calculated so you don't have to do it again what about speculative decoding.

M: Speculative decoding is pretty clever you use a smaller faster draft or model to predict a bunch of future tokens and then the main model checks those predictions in parallel if the drafter is right you can accept those tokens and skip the calculations for them which speeds up the decoding process the key is to have a drafter model that's well aligned with the main model so its predictions are usually correct.

W: And then there's the more General optimization techniques like batching and parallelization right.

M: Batching is where you process multiple requests at the same time which can be more efficient than doing them one by one parallel ization is about splitting up the computation across multiple processors or devices there are different types of parallelization each with its own tradeoffs.

W: So there's a whole toolbox of techniques for making these models run faster and more efficiently.

M: Now before we wrap up I'd love to hear some examples of how all this is being used in practice.

W: Oh the applications are just exploding it's hard to even keep track in code and math llms are being used for code generation completion refactoring debugging translating code between languages writing documentation and even helping to understand large code bases we have models like Alpha code 2 that are doing incredibly well in programming competitions and projects like fund search and Alpha geometry are actually helping mathematicians make new discoveries in machine translation llms are leading to more fluent accurate and natural sounding translations text summarization is getting much better able to condense large amounts of text down to the key points question answering systems are becoming more knowledgeable and precise thanks in part to techniques like RX chat Bots are becoming more humanlike in their conversations able to engage in more Dynamic and interesting dialogue content creation is also being transformed with llms being used for writing ads scripts and all sorts of creative text formats and we're seeing advancements in natural language inference which is used for things like sentiment analysis analyzing legal documents and even assisting with medical diagnoses text classification is getting more accurate which is useful for spam detection news categorization and understanding customer feedback and LMS are even being used to evaluate other llms acting as those aerators we talked about in text analysis llms are helping to extract insights and identify Trends from huge data sets.

M: It's really an incredible range of applications and we're only scratching the surface right especially with the multimodal capabilities coming online.

W: Exactly multimodal llms they're enabling entirely new categories of applications you know where you combine text images audio and video we're seeing them being used in Creative content creation education assist Technologies business scientific research you name it it's truly a transformative technology.

M: Well I have to say this has been a fascinating Deep dive we started with the basic building blocks of the Transformer architecture explored the evolution of all these different llm models got into the nitty-gritty of fine-tuning and evaluation and even learned about the techniques used to make them faster and more efficient it's incredible to see how far this field has come in such a short time.

W: Yeah the progress has been remarkable and it seems like things are only accelerating who knows what amazing things we'll see in the next few years.

M: That's a good question and it's one I think our listenership honder as well given the rapid pace of innovation what new applications do you think will be possible with the next generation of llms what challenges do you think we need to overcome to make those applications a reality let us know your thoughts and thanks for joining us for another deam dive.

W: Thanks everyone it's been a pleasure.