# VisualQuestionAnsweringSystem
Visual Question Answering System project - ITAI 1378 Computer Vision and AI
By Francisco Renteria Rios

Problem Statement
The difficulty visually impaired individuals face when attempting to read the grocery labels, make them make mistakes when choosing store items.  Their actions can have health consequences.
This project demonstrates a Visual Question Answering (VQA) system designed to help visually impaired users understand grocery labels and small print documents. 
It is important to support people with visual disabilities and make them more independent by inclusion using technology.

Solution Overview
A Visual Question Answering (VQA) system takes an image and a question about that image, then generates an answer. 
For example, this system can be an app in a smart phone.  The user ask a question, “Does this contain nuts?” They system then “sees” the label, understand the text, and gives the specific answer to the question, “Yes, the ingredient list includes almonds and peanuts”.
This system empowers visually impaired users to shop, choose, and eat safely.

Technical Approach
Model: BLIP-2 (Bootstrapped Language Image Pretraining)
Framework: PyTorch or TensorFlow for deep learning
Platform: Google Colab

BLIP-2 has an excellent balance of performance, efficiency, and strong reasoning capability.

Dataset Plan
Source: Public dataset (VizWiz-VQA).  It is a free public dataset. It can be access through Hugging Face, Kaggle, or the official VizWiz website. (VizWiz dataset was created specifically for visually impaired people).
Size: WizWiz contains over 31,000 image/question pairs.
Labels: If a specific ingredient is in a product.
Preparation: The dataset already contains labeled data.  Although the data contains images with poor quality to represent a real world scenario.

Metrics
Average Normalized Levenshtein Similarity (ANLS): it measures how similar the predicted text is to the correct text.
Answerability Prediction (this is a crucial metric drawn from the VizWiz dataset): The system must first decide if the question is even answerable from the image (e.g., the label is blurry, cut off, or doesn't contain the info).
Optical Character Recognition (OCR) Metrics: The VQA's performance is capped by its ability to read.

Week-by-Week Plan
Week	      Task	                            Milestone
10 (Oct 30)	Get dataset, set up environment	  Dataset ready
11 (Nov 6)	Train or fine-tune model	        Model working
12 (Nov 13)	Test and improve	                Good accuracy
13 (Nov 20)	Create demo / video	              Demo ready
14 (Nov 27)	Final testing / documentation	    Everything done
15 (Dec 4)	Present project	                  Presentation day

Resources needed
Resource         Options / Notes
Compute          Google Colab, VizWiz-VQA, Heidi
Frameworks       Pytorch
Estimated Cost   $0.00

Risks                              Probability       Mitigation
System fails to answer correctly   Medium            Fine-tuning
Poor image quality                 Medium            This condition reflects real world-sitautions
