
# Call classifier

Building AI course project

## Summary

Building an automatic call classifier for emergency services' control rooms to help them to react quickly and in an appropriate manner even during busy times. 

Input: what the first responders say on their talk groups. Output: real-time classification reflecting the priority of the call (from routine to emergency).


## Background

Emergency services throughout the world communicate typically via group calls regardless of the nature of the incident they are dealing with. This makes it sometimes challenging for their control rooms to react quickly in an appropriate manner especially during busy times with lots of group calls ongoing simultaneously. AI could be used to automatically highlight those calls that are likely to require more attention than others. 


## How is it used?

The classifier would probably run automatically in the background, transforming spoken language into text and classifying the call based on what has been said. 

The classification of each group call is provided together with other call information to the control room (or supervisor out on the field). First respondents on the field would not see the classifications, only the effect of those i.e. faster and better matching support from their control room or field commanders.


## Data sources and AI methods

Data to be gathered includes words, phrases and sentences said and priorities of the calls. Voice recognition is used to transform spoken language into text and each call is classified per its priority, e.g. into "routine", "advice required", "assistance required" or "emergency". 

Some pre-work will be required to build up a training data set, including both capturing the spoken words and classifying each call.

The classification challenge is in a way similar to classifying incoming email into suitable groups, e.g. business messages or spam. Techniques that could be used include Naive Bayes classifier, tf-idf, word embeddings and possibly also neural networks.


## Challenges

One of the non-technical challenges that needs to be faced is how to informing people whose calls are classified about this new service and why what they say will be automatically translated into text and analysed. It is likely that not everyone is going to like the idea of every single word they say being fed into a computer for analysis. 

Technical challenges are related to security, speed, accuracy and realibility. 

Security: As e.g. paramedics often deal with personal data the solution needs to be designed with suitable data protection in mind. For example, it should not be possible to dig into the algorithm or other material to link anyone to any place, incident or similar. Police communication in turn may require high confidentiality e.g. when dealing with organised crime. For this reason the solution would need to meet certain requirements and pass relevant security audits before it could be allowed to be used with those talk groups (or even allowed to run in the same network).

Speed: To be effective, the classifier has to work in (almost) real time - it is not useful to know some minutes or hours later that someone was in a situation that could quickly escalate into something dangerous. 

Accuracy: This is challenging especially in the early days when there will not be lots of training data, resulting to higher portion of inaccurate classifications. But even after being in use for a longer time, considering that the emergency services often deal with life threatening situations it is likely that the classifier can only be used as an assistive tool rather than a decision making one.

Classification changes during the call: It is not enough to label a call once and then move on. While speed is important, as any situation may quickly escalate into something more serious also later on the classification engine has run throughout the call. Any changes should respectively be fed to the control room or field commmander. 


## What next?

The project needs to start with a "friendly user" and a smaller set of training data and simpler techniques to prove the concept. 

In order to be able to go mainstream and be widely used in real life, the functionality needs to be first be proven to work at less dangerous environments, e.g. testing it at a police academy during their training exercises.


## Acknowledgments

Various discussions with my colleagues over the many years I have been working in the field of mission critical mobile communications.
