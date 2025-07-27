“Overfitting” is the new, hot AI buzzword after Apple recently published a [widely-discussed paper](https://machinelearning.apple.com/research/illusion-of-thinking) highlighting the shortcomings of OpenAI and Claude’s flagship models. Similar to other buzzwords like “prompt engineering” and “fine-tuning,” overfitting is a central concept in machine learning, with a notable application in large language models (LLMs).

**What is overfitting?**

The goal of foundational LLMs is to be robust, meaning they should accurately answer as wide a range of questions as possible, also known as **generalization**. To accomplish this, models are trained on a set of data representative of this entire range of subject matter so they aren’t too strong or weak in any specific area. These models are then tested to measure their generalization abilities.

In the case of LLMs, this is done by examining their responses to questions of varying complexities.

This approach to training is comparable to all learning, not just AI. If someone is learning how to hit a baseball, but they only get tossed slowballs during practice, it is unlikely that they could consistently hit fastballs when facing a real pitcher. As such, a good trainer would throw various pitches so the batter gets better at hitting overall.

Overfitting, however, is analogous to tossing a neural network slowballs, resulting in models that are excellent at answering only a specific set of questions. This wasn’t a problem at the inception of ChatGPT in 2021, but in 2025 OpenAI and other AI companies have almost completely run out of viable data to train their models on. 

This could mean that some models are not well-generalized but rather massively overfitted to all available data, making them only *appear* generalized. Considering this possibility and many others, researchers at Apple tested current flagship models to determine the validity of these claims.

**Apple’s “bombshell” paper**

In Apple’s recent paper, “The Illusion of Thinking: Understanding the Strengths and Limitations of Reasoning Models via the Lens of Problem Complexity”, researchers highlight an issue sitting at the center of many recent flagship reasoning models. They found their “reasoning” abilities exhibit signs of **data poisoning**. Data poisoning, in this case, means that whatever data is used to test their models is likely also represented in the training data.

In the case of large reasoning models (LRMs) such as OpenAI’s o3 model, which are intentionally designed to handle higher levels of complexity, this issue becomes quite noticeable. When asked to solve problems like the Tower of Hanoi and write out each step they took to answer, the LRMs failed at higher levels of complexity. While most of these problems have mathematical solutions that work at all levels of complexity, the LRMs could not utilize the algorithmic reasoning solution the experiments were testing for. 

The researchers concluded that, though these models excelled in answering up to a certain level of complexity, they largely failed to perform outside of what they were likely trained on. In other words, they could not generalize to these difficult questions.

**Is this news?**

For many, the results of the study are unsurprising for a multitude of reasons. The most prominent of these is that, fundamentally, LLMs are not built to handle these types of questions. The bedrock of these models is semantic embeddings, meaning their ability to answer questions is based completely on the similarity of a prompt to what data a model is trained on. 

Without using external tools for help, the way language models do math is no different. If they have been told in training that two times two is four, they answer that problem in the same way they can discuss Wisconsin state history. Hence, when models reach a point at which users start asking highly complex questions the models have not seen before, they are *unable to answer* them.

This lack of surprise was particularly shared by those familiar with reasoning models. These models employ the chain of thought (CoT) technique, which essentially daisy-chains the language model together by breaking down a user’s prompt into subproblems to solve one by one for higher accuracy. 

While CoT leads to significantly more accurate outputs, the model isn’t actually “thinking” the way a human does by creating meaningful connections. Though the study showed that even these models have a limit, CoT was already generally known to have a [limit to its abilities](https://www.ibm.com/think/topics/chain-of-thoughts). 

It is also important to note that the scientific community met the paper with mixed responses. While some, such as Gary Marcus, a leading voice in the space, discussed the paper’s implications at length, others, especially researchers at Anthropic, rebutted by [denoting flaws](https://arxiv.org/html/2506.09250v1) in the experiments’ methodology. Many researchers also voiced their concerns that this paper played heavily in Apple’s favor, as “Apple Intelligence” has been regarded as a failure thus far.

**Is ChatGPT overfitted?**

Even though OpenAI is notoriously secretive about their practices, it is unlikely their models are overfitted. Though they may house an unfathomable amount of data, they have to procure and fairly represent this data effectively before training their models. 

The proof is in the pudding: the GPT models are so well generalized that, today, many people go to them whenever they need *any* question answered. 

Thus, the likely reason o3 didn’t perform well in the Apple study is not because the model is poorly-generalized. It is because of the complexity of what was being asked and the intrinsic limits of language models.

**Future implications of overfitting**

Due to these limits and unfortunately for OpenAI and others, the days of simply expanding the size of flagship models and feeding them more data are over. Any larger model with more data would likely be at risk of unavoidable generalization issues. 

Given this predicament, AI companies are faced with the challenge of coming up with the next “big thing” in the space. All enthusiasts can do in the meantime is guess what it will be.