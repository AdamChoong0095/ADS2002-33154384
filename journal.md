ADS2002 indv. portfolio

ADS2002 week 2 entry

This week, I was allocated to my group and introduced to the technique of using convolutional neural networks (CNNs) to classify image data which belonged to a medical imaging dataset. Prior to the introduction of the topic, I conducted research on neural networks, in general, collecting resources and notebook tutorials on how to implement and optimise them. I shared to resources I found to my group members and helped them get TensorFlow (TF) set up as I had already used TF prior to the project’s introduction. No code was generated by our group as we were familiarising ourselves with the mechanics of TF, however, the resources I distributed assisted in this process. The source of the notebooks I distributed to my group members can be found here (the notebooks were in PyTorch but I explained to my group members that the processes explored and mechanics explained in the notebooks are similar to TF): https://www.learnpytorch.io. No particular insights were generated this week.

ADS2002 week 3 entry

This week I did basic exploratory data analysis and an assessment on the cleanliness of the data. This involved conducting research on the variables observed in the dataset. For example, I found out what CVC, ETT and NGT described in the dataset and their implications for determining a conclusive result for the project. Since it was relatively difficult to access the data, our group’s main priority was to decide our research question. I proposed that we study casual features in the images which are outlined by the training annotations data set and determine which feature seems to result in an improper placement of each given type of catheter. I also wanted to consider the reliability and accuracy of our predictions when applied to the testing set of images. My other group member suggested a research question about using our results to help streamline the catheter placement process for medical professionals and although the purpose of this project may be to assist in the automation of identifying of misplaced catheters, I believe their suggestion is too implicative meaning that it should be a question answered during the evaluation of the results. The current state of our code only deals with the contents of the csv files as indicated below:

<img width="452" alt="image" src="https://github.com/AdamChoong0095/ADS2002-33154384/assets/130020182/91e8ed09-3ee7-4ff1-a505-e2c81a813e5b">

To assist with comprehending the data, I wanted to answer the following questions: How many patients were being analysed? How many images were taken of each patient? How can I best choose a visual to represent the data? I did not manage to find an adequate way to visualise the data but next week, I aim to finish this process. The main insights that I generated, however, were to do with discovering what each variable meant in the context of medicine and radiology. 

Github commit link: https://github.com/louisechilds/ADS2002-Catheter/pull/7

ADS2002 portfolio entry week 4

This week, I reviewed the previous semester’s notebooks and devised a plan to apply K-means clustering and principal component analysis to the data set. However, I had a lot of trouble importing all the data, so I had to search up methods to import samples of data for testing.  Since only small amounts of data could be imported, in my opinion it would be better to use unsupervised methods to prevent either severe overfitting or underfitting due to the lack of data in the samples extracted. My team members and I each found a way to visualise separate parts of the dataset. The visual I produced was a stacked bar graph which had the purpose of comparing quantities of certain attributes. Perhaps, it could have benefitted from being proportional rather than counted. This is because small quantities with significant meaning will be omitted or hard to see in the stacked bar chart. 

<img width="272" alt="image" src="https://github.com/AdamChoong0095/ADS2002-33154384/assets/130020182/f5cb3143-9834-4762-b782-4074e267fbb8">

However, this stacked bar chart clearly shows the heavy biases that exist in our dataset and that we must balance it some way or another if we are going to use a substantial proportion of all the data. Next week, our aims are to at least read the image data, perform the above-mentioned classical machine learning techniques before configuring our convolutional neural networks (CNNs) in the coming weeks. 

Git pull request link: https://github.com/louisechilds/ADS2002-Catheter/pull/9

ADS2002 week 5 portfolio entry

During this week, the main task I managed to solve was reading the image data successfully as a sample. Other activities I engaged in were some experimentations with reducing the images unsuccessfully using PCA, although I intend to get some assistance and try again since I know it is possible to conduct PCA on image data that is in the right format. Currently, I have my image data in the format of a list of arrays which will not work during PCA so I may require to find solutions to make sure I can create an array of array representations of the data so I can start implementing PCA and K means like I wanted to last week. Other activities I engaged in with my group were supervising and advising another group member as they generated visuals for the data and conducted further EDA. Admittedly, I was a bit vague in my instructions so I could foresee some upcoming complications in next week’s studio which I intend to resolve as soon as possible. The code I generated this week to read the image data successfully is included below. I used an external library, cv2, instead of tensorflow because of its ability to rapidly read images in large quantities like I aimed to last week.

<img width="452" alt="image" src="https://github.com/AdamChoong0095/ADS2002-33154384/assets/130020182/adaad653-4ebb-4acc-a717-94a0d848a97c">
 
As a result, I managed to preview some images in the notebook which was quite an important milestone to me as we could begin meaningfully interacting with the dataset.

<img width="452" alt="image" src="https://github.com/AdamChoong0095/ADS2002-33154384/assets/130020182/40869e0f-37f1-405b-a01d-9e3127553520">

No results related insights were generated this week but perhaps after I make the data compatible to PCA for reduction purposes, I will be able to pass images through a model to generate insights.

The github link for this week’s commit (no merge request this week) is: https://github.com/louisechilds/ADS2002-Catheter/commit/e5f89e43ef68cc5d6f0d0c848b590d9e19542fff 

ADS2002 week 6 portfolio entry

During this week, I simplified the purpose of our project, modified the data frame to suit the purposes of our research question and altered the image reading function I discovered last week to match our project’s specifications. In addition, I began researching sampling methods with image data because we needed to reduce the amount of data inputted into our models. The main issues encountered when I researched sampling methods were that our dataset was heavily biased and since I could not load the whole dataset into colab, I firstly had to manually pick images to place in an extra folder then, from that extra folder, I had to sample some images. This was due to the extremely limited RAM on colab, which particularly frustrated me, especially when I was trying to configure the image reading function as well. 

With the assistance of my supervisor, I coordinated the technical aspects of the project by delegating duties to myself and another member in such a way that we could both work on different models at the same time without modifying each other’s data significantly or having to create copies of data (which would not have been possible due to RAM limitations). I also discussed the less technical aspects of the project and what they entailed with my other group members to enable them to conduct their own background research on our project. 

The current state of my code for the image reading function allows for the automatic readjustment of image dimensions for compatibility purposes and the ‘wrangling’ I did allows the image data to be indirectly incorporated as a ‘feature’ variable within the main data frame. Below is the code I used to simplify our data frames to suit our research question and an example output.

<img width="345" alt="image" src="https://github.com/AdamChoong0095/ADS2002-33154384/assets/130020182/d932725e-7a20-4800-8ac3-cfdfd3ddc119">
<img width="345" alt="image" src="https://github.com/AdamChoong0095/ADS2002-33154384/assets/130020182/6b9316a5-e539-4008-a02e-7873088cda05">

Note how we have partitioned the data to only include NGT related outcomes. I also made sure that we were not performing modelling on incomplete images by removing the corresponding StudyInstanceUID rows. Lastly, I ensured that all these rows were only pertaining to instances where NGT catheters were actually placed, meaning for all rows, there is at least a 1 in either abnormal, normal or borderline categories. I repeated this procedure for the other two catheters. 

To get an image to be represented indirectly on the data frame, I created a function outlined here.

<img width="452" alt="image" src="https://github.com/AdamChoong0095/ADS2002-33154384/assets/130020182/4e8b2bfd-a4ff-4535-afb9-982a812e9a8d">

The result is a data frame with each row containing the directory path of the image corresponding to the row’s study instance UID. No contributing figures were produced this week but a lot of useful pre-processing work was done. For this week, the most useful insight was related to how I managed to solve the issue of including a representation of the image data compactly in the existing data frame. I was also told to simplify my group’s problem type from a multiclassification to a binary classification which made managing many aspects of the project a lot easier. 

This week’s github commit link is: https://github.com/louisechilds/ADS2002-Catheter/commit/15787234e9e4f8f14c79a2fa72f9e472f928a6da


ADS2002 midsemester portfolio reflection

From this project, so far, I have learned about the importance of clearly defining our project’s goals and giving concise yet specific instructions and advice when delegating tasks to others. For example, I wanted one of our group members to handle the exploratory data analysis component of our project and build upon the work I did at that stage, but they struggled to do so because I was unclear with what I wanted them to achieve. Even though I provided a lot of technical advice, which I thought was sufficient for them to perform the task, it was not completed because the advice seemed to overwhelm that group member and was sometimes perceived as conflicting or confusing to them. I also learned about the practical aspects of project scalability, meaning that our project should start small and gradually increase in size. This means handling smaller datasets first then increasing in size and also setting a basic classification problem, say binary classification, then moving forwards to a more complicated problem, like a multiclassification problem afterwards.

There were many technical challenges, which mainly arose because for almost everyone in my group, it was the first time that we encountered image data and neural networks. Reading the data was particularly challenging because none of us had any experience in handling anything but csv files. With the guidance of our supervisors and some external research into different techniques used to read images from different inbuilt libraries, I managed to solve this issue, but it slowed our project’s progression significantly at the beginning. Other challenges included pre-processing the data in such a way that the images themselves were a representation of the feature variable and the outcomes were the labels. 

I believe my contribution to the project was partially technical and managerial as I assigned tasks and mapped out the plan for our project whilst conducting partial exploratory data analysis and wrangling and sampling the data. My technical activities have resulted in the preparation of the data in such a way that it can be pipelined to the neural network models I am yet to configure. 

In future projects, I aim to be clearer when communicating with other members so that they can produce their best work. With an increased familiarity of how to handle image data, I want to improve upon my technical capabilities when processing and using such data for modelling purposes. This could mean applying techniques like PCA and clustering more proficiently than I have been during this project, for example. 

ADS2002 week 7 entry


During this week, I managed to load the image data as an array representation into a data frame containing the outcome for each instance. I also managed to load a tensor representation into this data frame. However, despite my initial thoughts, this was not the right thing to do because unlike other supervised learning methods that used traditional data frames containing label columns and feature columns separately on the same data frame, I could not apply this same principle to neural networks. Instead, I had to wrangle the data some more and create a custom data loader to pipeline the processed data. Wrangling the data involved separating the data into separate training and testing folders in the directory and separating the data inside each folder by class, if I wanted to do supervised neural networks, which was my intention. Therefore, I will need to revert the code to its old state to achieve this. Some good news, however, was that I managed to create a baseline model from the research I conducted (although I did not push it to github since it was incomplete). So once my image data is ready, I have a clear idea of what I want to achieve. The purpose of the project is to not only classify binary outcomes but also, to compare different neural network configurations, loss functions and optimisers based on different measures of performance so once I complete pre-processing, I believe out project will be completed quickly afterwards. 

A significant piece of new code for this week managed to get array representations of images as feature variables into the data frame containing the labels.


<img width="452" alt="image" src="https://github.com/AdamChoong0095/ADS2002-33154384/assets/130020182/b9ec4d68-2283-4437-ab91-5cd3534b3e8b">


The link for this week’s github commit is https://github.com/louisechilds/ADS2002-Catheter/commit/3ef9068cce4a129162099e770cfb93f4b0e29d19 

ADS2002 week 8 entry


During this week, I had to reset my approach to data pre-processing the image data. I copied the same steps from previous weeks to include the images’ corresponding directories into the data frame, but a significant change was that I needed to create a custom dataset to load the images. This was especially difficult because I was mostly learning how to create a custom data set from the documentation of the libraries I used. Part of creating this custom dataset involved formatting the file directories in the right way. So I had to find functions that moved the images to the right folders. Using my external tutorial resources on PyTorch, I wanted to copy the structure that it had on its directory but this did not work for the project because the labels and image tensors had dimension compatibility issues. For example, in the resources I consulted, the label tensors were converted so that it had the same number of entries as classes but the project’s current pre-processing code caused the label tensor to have only one entry. However, I did manage to find a function to preview random images and their label and dimension. I wanted to use this function to see if I could understand the problem that was occurring. The code and an example of an output it produce is shown below. *Taken from PyTorch tutorial by Daniel Bourke¬.


<img width="363" alt="image" src="https://github.com/AdamChoong0095/ADS2002-33154384/assets/130020182/d3774579-19b6-476a-99f9-76b723bf11e2">


<img width="452" alt="image" src="https://github.com/AdamChoong0095/ADS2002-33154384/assets/130020182/dbdebf4e-ab17-45ef-b082-b80e30083872">


The code took 5 random images, displayed them, their shape and outcome. Oddly, the shape was 64x64x1 when I expected it to be resized to just 64x64. I suspected that the additional dimension was containing the label which made it difficult to do any sort of train, test, split  functions on the data. However, once I resolve this issue, I believe I will be ready to test the metrics of different models and carry out our aim of comparing different models. The link to this week’s github commit is https://github.com/louisechilds/ADS2002-Catheter/commit/f5e46425e4febc4d8fccd5510323dc68e3144ea0  


ADS2002 week 9 entry


During this week and the midsemester break, a lot of progress was made. The main activities I did were creating functions to organise directories for use in tensorflow deep learning models, fitting ResNet to images for the first time and completion of exploratory data analysis, including visualisation of the images and their annotations. I managed to cooperate with another group member to complete the technical task of normalising images which I had some issues with and I managed to get my other group members to start writing on parts of the report that did not require modelling to be done. I started a new notebook just to manage and download files into the local directory so a lot of new code was generated. The main highlight of this procedure was the iterative copying and pasting of files from the source directory into different destination directories. The code for this function is shown here.


<img width="332" alt="image" src="https://github.com/AdamChoong0095/ADS2002-33154384/assets/130020182/e72adfc0-7881-42a0-910b-a40193fb6812">


Another significant part of these week’s activities was preparing the training, testing and validating directories, which I managed to do in a flexible way that allowed me to only transfer a few selected files from the source to my local directory based on the random state of the train_test_split function. This was quite important because I needed to find a way to randomly generate a directory that followed the structure of the data required for fitting a neural network. For the exploratory data analysis stage of the project, I borrowed a function to visualise the annotations on the images for the purposes of expanding the scope that our EDA covered and I managed to fix up one of the visuals that I generated very early on in the project so it would be more useful when explaining the statistical properties of the data. This visual and the annotated images are shown. The bar chart indicate roughly the degree of imbalance that each category in the data (each type of catheter) has while the annotated image example, which was produced for all types of catheters and qualities of their placements, provides a visual pattern of each catheter’s positioning for the same category of images, that can be interpreted.


<img width="222" alt="image" src="https://github.com/AdamChoong0095/ADS2002-33154384/assets/130020182/ab91afd0-c27c-4260-b1e2-1497fe41af05">
<img width="227" alt="image" src="https://github.com/AdamChoong0095/ADS2002-33154384/assets/130020182/5f314c3c-43c6-47fd-9227-6fe4d3ccca26">


The coordinates and annotation plot were later normalised by my group member with my assistance. My research into the exploratory data analysis and visualization section of the project enabled me to think of a logical process to tackle our project’s relevant multiclassification problem and a theoretical way in which we could proceed in tackling the issue. It is briefly summarised below here:

•	Import a copy of approximately one-third of each type of placement for each type of catheter or a balanced proportion of images (pending) directly from source. For training and validating folders, only use annotations. For testing, only use images that are not annotated. We should have catheter => train, validate => normal, abnormal, borderline as the directory for each type. Do not change the random state. 

•	Standardise both the coordinates found under the ‘data’ column of the annotations file and the image sizes. This will enable the images to be propagated through ResNet, etc. The model’s interpretability of the results lies in the position of the scatter plots that indicate the catheter’s position. In theory, a non-linear boundary should be formed for the placement (normal,etc.) of each type of catheter during training then we can test the accuracy of this non-linear boundary during validation to the scatter plots formed for the validation images.

•	Finally, we test on images that are not annotated and see how well our non-linear boundaries could predict placement.

•	Comment on results, possible improvements, hyperparameter tuning, etc.

The links to this week’s commits in github are https://github.com/louisechilds/ADS2002-Catheter/commit/a504b6378c20f67d6f13c44b30d9965d9e79e4f4 and https://github.com/louisechilds/ADS2002-Catheter/commit/c39ac51f4fbebe0c9126151c71ca978bf5996b63 


ADS2002 week 10 entry


During this week, I successfully managed to implement my method that I mentioned last week on forming a boundary around annotated coordinates. My group began coordinating presentation roles and I organised the assembly of our project’s report. This involved assigning sections to other members and assisting with specific sections beyond my assigned scope of the report. I managed to simulate a training, validating, testing split function of images into different folders by deletion and file copying functions. Now we have files separated by catheter type and training, validating, and testing folders, each being pre-classified into folders. This allowed me to run supervised neural network methods requiring image data generators without running the risk of copying duplicates, like previous weeks. Additionally, the most important outcome for my work on refining the splitting functions for images was that the random state did not have to be fixed anymore so different configurations could be tested. With regards to the neural network construction involved to fulfil the vision I set out for the method I mentioned last week, I learned about the types of neural networks we could use to produce results using only coordinate annotation data with a handful of assumptions outlined in the method I was using. (such as assuming that all image x-rays’ chest sizes were standardised when image size was standardised by my group member) One of these were recurrent neural networks which I chose for its ability to retain long short term memory (LSTM) of sequential paths of coordinates outlining the paths of the catheters in each image. LSTMs and other RNN architecture are usually reserved for NLP methods so finding resources that cited this method’s feasibility was moderately difficult. I also used a convolutional 1-dimensional neural network method on the coordinate data. I justified using this method because of the structure of the coordinate data being “1 dimensional’ in the sense that it was not defined by two axes as an image but was rather a list of coordinates being expressed as an array. The useful figures were generated by my group member who resized the images and corresponding coordinates but I produced loss and validation loss plots relating to the training and validating of the neural networks we used to assess the quality of the models. The plot on the left is for convolutional 1D networks and the plot on the right is for RNNs. The data we tested on for these plots is the CVC annotations.


<img width="221" alt="image" src="https://github.com/AdamChoong0095/ADS2002-33154384/assets/130020182/dee9f5e8-c428-4da3-833d-1d6b47df54ec">
<img width="225" alt="image" src="https://github.com/AdamChoong0095/ADS2002-33154384/assets/130020182/5a8ee4a7-3657-4818-8f47-6b0e4d821afe">


Overall, with an unbalanced selection of images, our accuracy was not super high but I consider the model’s performance to be decent given we are doing multiclassification and our accuracy exceeds guessing images’ outcomes to a visible degree. I deem this progress a as being significant because at the very least, I will be able to produce a sound analysis on my current findings. The main points I will be able to focus on are the overall model’s performance with regards to various metrics, such as accuracy, specificity and sensitivity. 

This week’s github commit is: https://github.com/louisechilds/ADS2002-Catheter/commit/f02dba59caa0e710849bb19461461cad54d7f845 


ADS2002 week 11 entry 


During this week, I was able to gain all the results I needed to formulate a sound presentation on my findings using recurrent neural networks on a sequence of coordinates. However, as I delved into research papers on the general use of RNNs in different situations, especially those involving coordinate data, I realised that my reasoning for justifying the use of RNNs in our project’s context was fundamentally flawed because the LSTM properties of RNNs rely on time series elements of data which our data lacked. Still, I chose to proceed with this approach because I wanted to conduct a test on the validity of my hypothesis that catheter placements could be mapped this way. My thinking was that we could map the insertion of catheters through predicting a trail for each catheter and testing the accuracy of our prediction. Model interpretability was nigh impossible so I resorted to simpler measures, mainly accuracy, to assess our model’s performance on a selection of images. The most useful figures produced from this week’s progress were the confusion matrices associated with the testing phases of the models. From these matrices, I realised that we could calculate model sensitivity and specificity as well as other measures that could be very useful when trying to reach a meaningful conclusion that could be useful to the medical context we are applying our modelling to. One of the figures generated were a confusion matrix for the CVC catheter.


<img width="320" alt="image" src="https://github.com/AdamChoong0095/ADS2002-33154384/assets/130020182/1c73d6e7-0639-4f13-88a2-fa6150804f2c">


Admittedly, the accuracy isn’t so great for this catheter (the accuracy is greatly improved for other catheters) but it is significantly high enough that our model is at least not guessing image classifications. Given the random nature of the training processes behind each run of a model, I realised that the accuracies produced were not definite but rather, our accuracy results took the form of a confidence interval, though I did not know the distribution of accuracies. Perhaps I might repeat the training, validating and testing processes multiple times and assume a t-distribution to deduce the confidence interval for the true accuracy of our models. Other activities I did during the week included writing sections of the report relating to model development for recurrent neural networks, background information and explanations on the rationale behind our group’s methods. I am currently working on trying to fit a convolutional neural network with increased pixel intensity effects applied to its images. I managed to fit a baseline convolutional neural network but it was being trained on a lot of noisy data which made its accuracy decline and the model’s training process inefficient. 

This week’s github commit is: https://github.com/louisechilds/ADS2002-Catheter/commit/97233c359369e3e4906b98fca2987750b4061bae


ADS2002 end of semester reflection

From engaging in this project, I have learned about the importance of facilitating communication between teammates to produce tangible results. Furthermore, I developed my ability to produce creative solutions to problems faced by our team, both in a technical and interpersonal sense. Some of these solutions employed to handle the difficulties regarding meeting deadlines included breaking tasks assigned down to manageable chunks for other team members who may be struggling to express their ideas. I also learned how to become independently flexible, in the sense that I could assist others in their contributions to the team’s project as they managed multiple commitments and subsequently could not produce the input required to meet the project’s requirements. 

I faced many challenges when trying to establish expectations of frequent communication between group members. To resolve this issue, I acted as a mediator through which concerns could be expressed. Furthermore, other challenges included the unfamiliarity associated with the project’s requirements. I managed to overcome the challenges associated with this by demonstrating resourcefulness and searching for all the required elements to complete the project. As group members struggled to meet deadlines in advance, there were some challenges in managing the quality of the work we produced. To reach a compromise when dealing with this issue, I negotiated group expectations as our team became more time constrained. 

Given my flexibility and knowledge of almost all aspects of the project, I was able to write substantially on the general aspects of the report and the sections that I was directly involved in completing. This included the introduction, executive summary, analysis of results, model development and evaluation. Furthermore, I was able to improve upon other sections that I was indirectly involved in creating through productive suggestions and feedback. 

There was a distinct lack of communication in this project compared to past experiences so I would improve the way in which I would handle such a situation in future encounters. Furthermore, on the technical front, I aim to improve the approaches I used to achieve the results obtained from the project by exploring more creative approaches to the very interesting problem posed by this project. I aim to establish expectations within myself and other group members, regarding deadlines and standards of contributions produced to better organise how projects are completed in the future. This will not only reduce the stress involved during the process of completing the project but will also elevate its quality. 
