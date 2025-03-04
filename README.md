java cAssignment 
MISCADA Computer Vision module
Academic year 2024/2025
  
Academic in charge and contact information
Professor Paolo Remagnino, Department of Computer Science
Introduction
This assignment is split in two parts, with separate deadlines; details follow.
Description (15%)
A thorough description of the used libraries and methods and the results is expected. Please refer to the marking scheme table for more detail.
Part 1 (30%)
A computed tomography (CT) scan is a non-invasive imaging procedure that uses X-rays to create detailed pictures of the inside of the body. CT scans are used to diagnose and treat a variety of conditions, such as tumours, pneumonia and internal bleeding.
A CT scan is composed of a large and variable number of slices, each one of them is a greyscale image, examples of CT slices are provided in figure 1.
	
	
figure 1 examples of CT scan slices: top row contains raw data, bottom row annotated data: both leg bones and calcium concentration are labelled.
For this part, you will have to search for areas that might indicate the presence of calcium deposit. In CT scans, calcium and bones are visible as brighter areas, while other organs usually have low intensity values. The provided data (see later in the document for details) represent portions of CT scans of the lower limbs. In simpler terms, those slices represent cross sections of both patient’s legs. Presence of calcium might indicate serious indication of blockages in the arteries. So, the larger is the amount of deposit, the higher the risk is for a patient.
For this part, you will have to develop code in Python, using Jupyter Notebook to provide solutions to the following two tasks:
Task 1 (15%): creating masks on a slice basis
You are asked to create greyscale masks for each slice of the given CT scans. Each CT slice will need to be normalised to represent a probability density map. Segmentation must then be applied to each map to highlight those pixels that might indicate the presence of calcium concentration.
Task 2 (15%): estimating volumes of calcium deposit
Calcium deposit is a three-dimensional object, as an artery is a 3D object, while each CT slice is merely a 2D representation of the deposit at a given position in the CT scan. You are asked to make use of the probability density maps created for the previous task, to develop code to estimate the volume of calcium deposit across CT scan slices. Do assume the thickness of each slice is 0.5mm, assume pixels are squares of 1mmx1mm size. 
Part 2 (55%)
You must develop code to analyse video clips taken from the last Olympic games (Paris 2024). 
To start with, you are asked to download the video clips from Blackboard. They have been prepared for you, instructions where data can be found are provided later.
For this part, you have additional tasks to solve; please read the following instructions for details:
Task 3 (15%): Target detection - for this part, you are asked to exploit one of the taught algorithms to extract bounding boxes that identify the targets in the scene. Targets are represented by either objects or people moving in the video clips.
Expected Output: Bounding rectangles should be used to show the target, as well as an ID and/or a different colour per target. 
Task 4 (20%): Target tracking - for this part, you are asked to use one of the taught techniques to track the targets. Tracking does mean using a filter to estimate and predict the dynamics of the moving target, not simply detecting targets in each frame.
Expected Output: For this task you should provide short video clips using the processed image frames, the current position of the targets in the scene and their trajectories. Targets should be highlighted with a bounding rectangle in colour or a polygonal shape and their trajectories with a polyline in red (do see the examples in figure 2). Ideally, you could have prediction and new measurement highlighted using two bounding rectangles of different colour per target.
	
figure 2 example of tracked targets: bounding rectangles and trajectories.
Task 5 (20%): Optical flow – for this task, you are asked to use one of the algorithms taught in class to estimate and visualise the optical flow of the analysed scene.
Expected output: Once you have run the algorithm of your choice you can use any of methods used in the workshop or any method you find one the Internet to visualise the optical flow. A video clip must be generated, with optical flow overlapped to the original clip. Figure 3 shows two different ways to visualise optical flow.
	
figure 3 visualising optical flow using vectors (left), and dynamics direction using colour.
Dataset
Dataset of CT scans and Olympic clips are available in our Assignment folder on Blackboard. 
Marking scheme
Task	comment	%
Descriptions 	A general introduction to your solutions must be provided (5%), as well as a detailed description of how you solve each of the following tasks (10%).	15
Task 1	Hint: CT scan slices are greyscale images, segmentation can be implemented using one of the taught methods/algorithms. For the normalisation and generation of probability maps needs to enforce each map to sum up to one. 
Marking: 10% will be assigned to a fully working method, 5% only if the method partially works.	15
Task 2	Hint: one can think of aligning CT slices and related segmented maps. Combining adjacent slices means checking the likelihood of calcium deposit and building an estimate of the volume. 
Marking: the imp代 写MISCADA、Python
代做程序编程语言lementation must clearly demonstrate volume estimates are correctly built. Full 15% to a complete solution, if the solution works in part, then 10%.	15
Task 3	Hint: For this part I am expecting you to exploit the latest YOLO and SAM versions to detect the targets. You are also welcome to use any traditional method of your choice. 
Marking: the implementation exploits existing deep architectures, so validation and testing will be essential to get full marks. Ideally, the result will have to show “tight” bounding rectangles or closed polylines for the extracted targets, with an error measure such as the intersection over union (IoU) as a viable metric. Comparison of existing architectures/methods applied to the problem attracts 10%, the other 5% is for the most suitable metric to assess the result.	15
Task 4	Hint: For this task, you can use the dynamic filters you have been taught to track targets in the scene. You can feel free to use any deep learning method as well you have read during the four weeks.
Marking: the accuracy of the tracking will be a determining factor to obtain full marks, you are recommended to use the metrics you used to solve Task 3. Full marks if any spatial-temporal filter is implemented and manages to track the targets in the scene. A comparison of at least two filters attracts 8%. The other 5% is for the generation of a video clip as qualitative output and 7% for quantitative results.	20
Task 5	Hint: For this task, you can use any of the algorithms taught to use for the detection and visualisation of optical flow. Again, you can feel free to use any deep learning method as well you have read during the four weeks.
Marking: 10% for the detection of the optical flow, trying to disambiguate between moving camera and targets and 10% for the visualisation. The latter must be integrated in a video clip, with flow overlapped over the video clip frames.	20
Total 	100
Submission instructions
For each part, you are asked to create a Jupyter Notebook, where you will provide the textual description of your solutions and the implemented code. Your notebook should be structured in sections. An introduction should describe in detail the libraries you used, where to find them and how you solved the tasks. Then you should include one section for each task solution, where again you describe your solution. The code must be executed, so that the solutions are visualised, in terms of graphics, images and results; it is strongly recommended you also include snippets of the formulae implemented by the used algorithms and the graphics of the employed architecture. Your code should be implemented in Python, using OpenCV as the main set of computer vision libraries. PyTorch or TensorFlow can be used to use the deep learning methods you have chosen. Please do make sure your code runs and it is executed.  Notebooks will have to be uploaded on Gradescope, while all the videos to Panopto.
Submission and feedback deadlines
Please refer to the following table for details on the submissions:
Part 	Release date	Submission date	Submission method	Feedback date
1	17 Jan 2025	20 Feb 2025	Gradescope	20 Mar 2025
2	3 Feb 2025	17 Mar 2025	Gradescope and Panopto	14 Apr 2025
Extension policy and related documents
If you require an extension for a piece(s) of summative coursework/assignment you MUST complete the form via the Extension Requests App.
On this form you must specify the reason for the request and the extra time required.  Please also ensure that supporting documentation is provided to support your extension request.  
Your extension request will not be considered until supporting documentation has been received.
If the extension is granted the new deadline is at the discretion of the Programme Director.
Once the completed form has been received by the Learning and Teaching Coordinator it will be distributed to your Programme Director who will decide on the outcome.  You will normally be notified by email within two working days of the outcome of your request.
Please note that, until you have received confirmation that your extension request has been approved, you MUST assume that the original deadline still stands.
Further information on the University's extension policy and academic support can be found here.
Where circumstances are extreme and an extension request is not enough a Serious Adverse Circumstances form (SAC) should be considered.

PLAGIARISM and COLLUSION
Students suspected of plagiarism, either of published work or work from unpublished sources, including the work of other students, or of collusion will be dealt with according to Computer Science and University guidelines. Please see:
https://durhamuniversity.sharepoint.com/teams/LTH/SitePages/6.2.4.aspx
https://durhamuniversity.sharepoint.com/teams/LTH/SitePages/6.2.4.1.aspx

PLAGIARISM with chatGPT or/and similar AI tool
Examples of plagiarism include (but are not limited to) presentation of another person's thoughts or writings as one's own, including:
- cutting and pasting text, code or pictures from generative AI services (e.g. ChatGPT).

What is acceptable?
If you want to include any text or code produced using generative AI in a submission, that text or code must be clearly marked as being AI generated, and the generative AI that has produced the text or code must be clearly cited as the source.
The University has provided a guide on generative AI, with the following page on whether it can be used in assessment:

         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
