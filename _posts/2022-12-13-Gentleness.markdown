---
layout: post
title: Characterization of Gentleness in Surgical Tasks
image: img/gentle_title.gif
tags: [Hand Tracking, Image Recognition, Depth Imaging, Motion Analysis, Surgery]
featured: false
hidden: false
author: dk
---

Surgical skill evaluation is highly qualitative and
subjective in its current state. In the field of pediatric congenital
heart surgery, surgical skill and dexterity are directly related
to the level of gentleness used while operating on the sensitive
tissue of young children. We propose a method for quantifying
gentleness in surgical procedures to eliminate its qualitative and
subjective nature. The proposed method is based on video-based
motion analysis of surgeons with varying skill levels (i.e. a highly
experienced pediatric cardio-thoracic surgeon, a recently certi-
fied pediatric cardio-thoracic surgeon, and a complete novice).
The motion analysis was that of the participants’ dominant
and non-dominant hands during a surgical procedure known
as an anastomosis, where two Lifelike femoral artery structures
were bridged together through suturing. We consider a number
of different metrics when building our gentleness model (e.g.
mean linear acceleration, mean jerk, linear acceleration stan-
dard deviation, jerk standard deviation,path length, and time
span). Through data analysis, we saw statistically significant
differences between the participants’ non-dominant hand usage
during the surgical procedure. Furthermore, we saw statistically
significant differences in the timespan of the needle being passed
through the model tissue during the anastomosis procedure.
These results show quantitative differences in the surgical
dexterity of the participants. Furthermore, this study sets a
general framework for a quantitative analysis of gentleness
during anastomosis procedures


Keywords:[Hand Tracking, Image Recognition, Depth Imaging, Motion Analysis, Surgery]



# INTRODUCTION

The requirements to become a pediatric cardiothoracic
surgeon include at least 4 years of medical school, 5
years of a general surgical residency program, a 3 year
cardiothoracic (CT) residency program, and an additional
2-4 years of training in pediatric heart surgery [1]. This
lengthy process requires a significant monetary and temporal
investment which adds an additional, unnecessary barrier to
entry to a field with a growing need for qualified surgeons.
Furthermore, it is not uncommon for an aspiring surgeon to
go through years of training before realizing that they lack
the hand-eye coordination to be a good surgeon; this leads to
an increased number of mediocre surgeons since they have
already invested too many resources to pursue a different
career.

The current scope of training within the residency pro-
grams includes receiving verbal feedback from experienced
surgeons based on their observations. This highly qualitative
process is prone to high variability and subjectivity since
different surgeons have distinct operating styles. The field of
pediatric cardiothoracic surgery is particularly impacted by
the current process of qualitative evaluation of surgical skill.

Pediatric CT surgery outcomes are significantly dependent
on the skill of the operating surgeon, which is highlighted
by the extensive training required. Furthermore, the skill of
a surgeon depends on their dexterity with surgical tools and
their anatomical knowledge [2]. Dexterity in this context
refers to the level of gentleness that a surgeon can accomplish
while operating on the sensitive tissue of young children.
Increased gentleness in surgeries leads to increased perfor-
mance. These facts show the significance of a quantitative
evaluation of surgical skill, which directly translates to an
evaluation of gentleness in surgical procedures. Therefore,
the motivation for our study addresses two questions: First,
how can we measure gentleness in surgical procedures?
Second, can we assess whether someone has the surgical
dexterity to become a good surgeon?

Previous studies have aimed to evaluate surgical skill and
dexterity using various techniques. Surgical skill has been
assessed in [2], [11], [4], [3], [14], [16] by collecting and
analyzing motion data of the surgical tool using electromag-
netic sensors. The study also uses a camera to collect eye-
gaze information for further analysis. Furthermore, Hidden
Markov Models are used for surgical skill evaluation while
analyzing motion data in [2], [11], [17].

Other studies have tried to eliminate use of electro-
magnetic trackers by using video-based motion analysis to
characterize and evaluate surgical skills, while achieving a
more easily scalable framework for analysis in open surgeries
[8]. Many of these studies collect data from simulations and
from robotic devices, including haptic teleoperated devices
[14], [6]. This leads to limitations on the types of surgical
procedures that can be used to collect data for surgical skill
evaluation.

The characteristics of the motion data used to evaluate
and characterize surgical skill in these studies includes an-
gular velocity variability, linear acceleration variability, path
length, deliberate hand movements, eye-gaze information,
and mean jerk [2], [11], [7], [14]. A few of these metrics
are also used to defined stylistic cues as seen in [5].
Our work differs from previous studies in that we explore
a wider range of surgical expertise levels: 1. a highly
experienced pediatric cardio-thoracic surgeon, 2. a recently
certified pediatric CT surgeon, 3. a medical student with
some training in suturing, and 4. a complete novice with
zero training in suturing. Furthermore, our study is done with
video-based motion analysis in a non-simulated environment.
Many of the previous studies use electromagnetic motion
tracking sensors which are prone to low fidelity measure-
ments when in environments with close proximity to metal
objects and magnetic fields (e.g. hospital operating rooms)
[9]. Moreover, we aim to quantify gentleness using different
metrics derived from our motion analysis of both dominant
and non-dominant hands. These metrics include linear ac-
celeration standard deviation, jerk standard deviation, mean acceleration, mean jerk, path length, and time span.

# METHODOLOGY

In this study, we aim to evaluate the congenital pediatric
surgeons’ surgical dexterity by analyzing acceleration stan-
dard deviation (ASD), jerk standard deviation (JSD), mean
acceleration (MA), mean jerk (MJ), path length (PL), and
time span (TS). Three participants performed anastomosis
and skin sutures on a surgical model of a femoral artery,
and their hand trajectories were recorded using IMUs and
an RGBD camera.

## Participants
wo congenital pediatric surgeons at Texas Center for
Pediatric & Congenital Heart Disease, Dr. M and
Dr. V participated in the study, a medical student
(pending), and a complete novice

## Experimental Protocol

<div class="post-flex-display">
    <img src="/img/gentle/fig1.png" alt="fig1">
</div>


Participants used DeBakey forceps and a Castrovieojo
needle holder to demonstrate surgical skills such as knot
tying and suturing, etc on LifeLike large femoral arteries
for anastomosis and triple layer skins for skin suture. They
used their personal binocular loupes during the experiments.
Those surgical models were placed on the conference table,
and the participants rearranged the setup at their convenience
using plastic bins to adjust the height of the surgical models
(fig. 1). The experiments took place in the conference room
at Dell Children’s - Texas Center for Pediatric and Congenital
Heart Disease.

Arduino Uno and a MPU-6050 external IMU are attached
to the Castrovieojo needle holder to measure the 6-axis
acceleration of the end of the tool and the right elbow of
the participant (fig. 1) during his surgical task. Additionally,
the ZED 2i RGBD camera was placed in front of the surgical
models at a distance of about 0.3 m to track the participant’s
both hands.

The data recording consists of a total of 4 sessions with
two participants demonstrating two types of surgical tasks.
For each recording session, the integrated IMU in Arduino
Uno and the external IMU (MPU6050) were calibrated after
they had been secured to the participant’s arm. Dr. Venardos
assisted with Dr.Mery’s surgical tasks during the first two
recording sessions while Prof. Ann Fey assisted Dr. Venrados
for the last two sessions. The assistance involved holding
onto the seams and surgical tools. The participants were
not restricted to any constraints besides the instructions to
perform surgical anastomosis and suture with provided tools
and surgical models.

Additionally, the surgeons originally performed three
seprate tests: 1.) suturing on a thin model of human skin,
2.) suturing on a thicker model of human skin, and 3.)
an anastomosis on a Lifelike model of a femoral artery.
However, Dr. Mery and Dr. Venardos determined that the two
skin tests were not accurate to an actual surgical procedure
that would be done on real human skin. The setup we used
for the skin tests was not realistic because the platform
holding the skin was not providing enough tension and the
model skin simply felt unrealistic while suturing.

## Data Collection
While the built-in IMU of Arduino Uno measured accel-
eration data of the right elbow at 100 Hz, the external IMU
connected to the Arduino Uno measured acceleration data at
the tool at 100 Hz. An I2C communication protocol was set
up to establish communication between the external IMU and
our arduino. Furthermore, we set up a serial communication
protocol between the serial port where the arduino was
connected and a python program on the same computer. This
protocol allowed us to record acceleration data from both
IMU’s using Arduino IDE on a laptop, sending over data to
the python program, and saving it as a CSV file. We collected
time, acceleration values in x,y, and z directions, and angular
velocity values in x,y, and z directions. The values were
saved as a dataframe in a csv file.

The RGBD camera recorded color and depth images in
1280x720 resolution at 60 Hz using ZED SDK. Each video
was compressed using H.264 encoder format and saved in
an SVO format. We synced the data from the IMUs and the
camera by shaking the accelerometer in the frame of view
of the camera. This allowed us to find the peak acceleration
in the IMU data and sync it to the frame where the camera
shows the initial shaking of the IMU.

## Data Analysis
<div class="post-flex-display">
    <img src="/img/gentle/gentle.gif" alt="gentle">
</div>



Using Blender’s rendering software, we manually chose
17 clips of Dr. Venardos and 30 clips of Dr. Mery steering a needle in a spiral motion which is one of the most
significant tasks involving high-risk surgical errors during
anastomosis. Furthermore, we extracted the corresponding
frame numbers to extract the position data of the left and
right pointer fingers for analysis. We chose this task because
in a meeting with Dr. Neil Venardos, he mentioned that this
is one of the more delicate and prone to error procedures
within congenital heart surgery. Dr. Venardos elaborates and
mentions that there is a risk of enlarging the hole while
passing the needle through the tissue. This is known as
torquing the needle in the field of cardiothoracic surgeries.
To avoid torquing the needle, the surgeon must perform a
perfectly circular motion with a radius equal to the radius
of the curved needle while passing the needle through the
tissue. If the surgeon is unable to perform a perfect motion,
the hole becomes unnecessarily enlarged and leakage occurs.
This leakage causes significantly more internal bleeding post surgery, which can be detrimental to the recovering patient.

In order to track the positions of hands from the recorded
videos, Google’s MediaPipe Hands model which can detect
and localize 21 3D hand-knuckle coordinates inside the
detected hand regions via regression was used [12]. We
have created two Python scripts with MediaPipe API and
ZED SDK to track the primary and secondary hands of the
participant separately in the videos because the number of
maximum hands to detect was set to 1 due to the model’s
incapability to individually track two hands. ZED SDK
provides a function to obtain a 3d point cloud value from a
pixel using depth information, and we filtered 3d trajectories
of participants’ pointer fingers during a total of 47 video
clips of anastomosis tasks using a Butterworth filter.

Gentleness during surgical tasks can be assessed by evaluating metrics such as ASD, JSD, MA, MJ, PL, and TS of
the surgeon’s hand motion[2][7]. It is crucial to minimize the
timespan (TS) of these procedures because there is a trade off when taking too much time on a procedure. The risk of
cardiac dysfunction increases significantly as the TS of the
surgery increases. Therefore, to minimize the risk of cardiac
dysfunction it is important to complete the surgical procedure
within a reasonable TS. We selected to investigate pointer
fingers that directly manipulate surgical tools. With given
trajectories of pointer fingers, their acceleration and jerk
were calculated using numerical differentiation via NumPy
library’s gradient function to, and their standard deviations
and means were evaluated. PL was defined by calculating
the sum of Euclidean distances from the current to the proceeding frame while TS was determined by the total
frame number of each clip.

<div class="post-flex-display">
    <img src="/img/gentle/eq1.png" alt="eq1">
</div>

# RESULTS

ASD, JSD, MA, MJ, and PL of Dr. Mery and Dr. Venardos
are compared using the box and whisker plots. Fig. 4 and
5 show MA and MJ accordingly. Figure 4 show a statistical
significance between the non-dominant hand usage of Dr.
Mery and Dr. Venardos. As a study of intermanual transfer
of skill learning suggests that specific training of the nondominant upper extremity appears to lead to improvement of
skills on the dominant side, it is noticeable that Dr. Mery,
who is a more experienced surgeon, utilizes his secondary
hand more than Dr. Venardos [13]. We can see a similar
trend in Fig. 2 and 3 that Dr. Mery has greater ASD and
JSD in his secondary hand while his primary hand which
drives the needle performs in smaller ASD and JSD than
Dr. Venardos’ data. Fig 7 shows the comparison of TS of
three participants who are Dr. Venarados, Dr. Mery, and a
non-medical professional novice. A low TS is crucial for the
success of a pediatric heart surgery as the risk for cardiac
dysfunction increases as the TS increases. The novice took a
significantly longer duration of time to accomplish the spiral
motion of needle steering compared to both Dr. Mery and Dr.
Venardos. Furthermore, Dr. Mery took significantly less time
than Dr. Venardos. This further proves the difference in skill
level amongst the three participants studied. We evaluated
the statistical significance using Microsoft Excel’s statistical
analysis package.

# DISCUSSION

In future studies, we plan to implement various changes
to our data collection process to achieve better data.The data collected from our IMU’s was not usable due to not
accounting for gravity during the data collection process.
It is typically possible to filter out gravity to obtain solely
linear acceleration in post-collection processing with high fidelity gyroscope measurements [15]. However, our gyroscope measurements were low-fidelity and this led to issues
when attempting to filter out gravity from our measurements.
For future studies, we plan to compensate for gravity by
selecting a higher resolution IMU and filtering it out during
data collection with a gravity compensation filter. As another
option, we are also exploring the use of electromagnetic
tracking sensors which are heavily used in motion tracking.
However, these sensors are prone to noisy data when near a
lot of metal objects and strong magnetic fields; this can be an
issue since the hospital operating rooms are an environment
with a lot of metal and machines that emit strong magnetic
fields.

The ZED camera extracts position estimates using a stereo
camera setup, so the accuracy and reliability of measurements decrease at very short range. With depth measurements varying due to instrument accuracy, the quality of the outcomes are suspect. For example, as seen in figure 6 the
mean path lengths for operations lasting between 3 and 15
seconds are calculated to be in the range of 5 to 10 meters.
This is obviously an error. Another challenge that we encountered is the H.264
compression format that ZED SDK uses decreases in a
lower resolution which significantly affects the hand detection model’s accuracy during the analysis. In addition, the
participants’ hands occasionally moved outside the FOV of
the camera. Since the SVO file recording script does not
provide any GUI of hand detection model performance for
the robustness of the camera, we were not aware of these
issues during the recording sessions. We plan to use H.265
which can compress with less deterioration of the recording’s
resolutions and implement a GUI to ensure the precision and
accuracy of hand detection during the recording in the future
with a computer with higher video processing capability.

Yet only one hand detection model was used for data
analysis, we plan to compare the results of different models
such as YOLO and Tensorflow Objection Detection. The
model’s inability to track the rotation of the hands limited
data analysis while angular velocity variability is one of the
metrics to evaluate the dexterity of a surgeon’s hands [2].
Tracking the 6D pose (3D translation and 3D rotation) of
hands requires more complex models and high-fidelity CAD
models of hands. we plan to implement a model which can
estimate 6D pose of hands with deep learning for future data
collection [10].

# CONCLUSION

In this study, we showed the quantitative evaluation of
gentleness by analyzing the trajectories of the primary and
secondary hands of participants during anastomosis surgical
tasks on dummy surgical models. 6D acceleration data of the
primary hand from IMU and 3D trajectories of both hands
using RGBD camera were retrieved. However, IMU data
was excluded from the data analysis due to not inadequate
quality of measurements. Using a hand detection model and
depth information from the camera, ASD, JSD, MA, MJ,
PL, and TS of participants’ hands were studied. Analysis of
MA and MJ showed that dexterous movement in surgical
tasks involves frequent usage of the secondary hand. In
addition, PL was the most significant factor among the
gentleness evaluation metrics which can differentiate surgical
experiences among participants.

This study does not sufficiently evaluate gentleness in
surgical tasks due to significant errors in our data collection.
However, we established a working framework and guidelines which allow future studies to thoroughly investigate
gentleness during surgical tasks by improving data collection
apparatus and procedures.

### REFERENCES

[1] What is a cardiothoracic surgeon?: The patient guide to heart, lung,
and esophageal surgery.

[2] Narges Ahmidi, Gregory Hager, Lisa Ishii, Gabor Fichtinger, Gary
Gallia, and Masaru Ishii. Surgical task and skill classification from
eye tracking and tool motion in minimally invasive surgery. volume 13,
pages 295–302, 09 2010.

[3] Simon Bann, Mansoor Khan, and Ara Darzi. Measurement of surgical
dexterity using motion analysis of simple bench tasks. World journal
of surgery, 27:390–4, 04 2003.

[4] Marzieh Ershad, Zachary Koesters, Robert Rege, and Ann Majewicz.
Meaningful assessment of surgical expertise: Semantic labeling with
data and crowds. In MICCAI, 2016.

[5] Marzieh Ershad, Robert Rege, and Ann Majewicz Fey. Adaptive
surgical robotic training using real-time stylistic behavior feedback
through haptic cues. IEEE Transactions on Medical Robotics and
Bionics, 3(4):959–969, 2021.

[6] Jake Farmer, Doga Demirel, Recep Erol, Daniel Ahmadi, Tansel
Halic, Sinan Kockara, Sreekanth Arikatla, Kevin Sexton, and Shahryar
Ahmadi. Systematic approach for content and construct validation:
Case studies for arthroscopy and laparoscopy. The International
Journal of Medical Robotics and Computer Assisted Surgery, 16, 03
2020.

[7] Germain Forestier, Franc¸ois Petitjean, Pavel Senin, Fabien Despinoy,
Arnaud Huaulme, Hassan Ismail Fawaz, Jonathan Weber, Lhassane ´
Idoumghar, Pierre-Alain Muller, and Pierre Jannin. Surgical motion
analysis using discriminative interpretable patterns. Artificial Intelligence in Medicine, 91, 08 2018.

[8] Carly Glarner, Yue-Yung Hu, Chia-Hsiung Chen, Robert Radwin,
Qianqian Zhao, Mark Craven, Douglas Wiegmann, Carla Pugh,
Matthew Carty, and Caprice Greenberg. Quantifying technical skills
during open operations using video-based motion analysis. Surgery,
156, 06 2014.

[9] Neil Glossop. Advantages of optical compared with electromagnetic
tracking. The Journal of bone and joint surgery. American volume,
91 Suppl 1:23–8, 03 2009.

[10] Yisheng He, Yao Wang, Haoqiang Fan, Jian Sun, and Qifeng Chen.
Fs6d: Few-shot 6d pose estimation of novel objects. 2022.

[11] Nicholas Howells, Mark Brinsden, Richie Gill, Andrew Carr, and
Jonathan Rees. Motion analysis: A validated method for showing skill
levels in arthroscopy. Arthroscopy : the journal of arthroscopic related
surgery : official publication of the Arthroscopy Association of North
America and the International Arthroscopy Association, 24:335–42,
03 2008.

[12] Camillo Lugaresi, Jiuqiang Tang, Hadon Nash, Chris McClanahan, Esha Uboweja, Michael Hays, Fan Zhang, Chuo-Ling Chang,
Ming Guang Yong, Juhyun Lee, Wan-Teh Chang, Wei Hua, Manfred
Georg, and Matthias Grundmann. Mediapipe: A framework for
building perception pipelines. CoRR, abs/1906.08172, 2019.

[13] Theodoor E. Nieboer, Vicdan Sari, Kirsten B. Kluivers, Martin J. N.
Weinans, Mark E. Vierhout, and Dick F. Stegeman. A randomized trial
of training the non-dominant upper extremity to enhance laparoscopic
performance. Minimally Invasive Therapy & Allied Technologies,
21(4):259–264, 2012. PMID: 21939399.

[14] Ilana Nisky, Michael H. Hsieh, and Allison M. Okamura. Uncontrolled manifold analysis of arm joint angle variability during robotic
teleoperation and freehand movement of surgeons and novices. IEEE
Transactions on Biomedical Engineering, 61:2869–2881, 2014.

[15] Jonathan R. Nistler and Majura F. Selekwa. Gravity compensation in
accelerometer measurements for robot navigation on inclined surfaces.
Procedia Computer Science, 6:413–418, 2011. Complex adaptive
sysytems.

[16] George M. Saleh, Yiorgos Voyazis, Julian Hance, Joel Ratnasothy, and
Ara Darzi. Evaluating Surgical Dexterity During Corneal Suturing.
Archives of Ophthalmology, 124(9):1263–1266, 09 2006.

[17] Lingling Tao, Ehsan Elhamifar, Sanjeev Khudanpur, Gregory D.
Hager, and Rene Vidal. Sparse hidden markov models for surgical ´
gesture classification and skill evaluation. In Purang Abolmaesumi,
Leo Joskowicz, Nassir Navab, and Pierre Jannin, editors, Information Processing in Computer-Assisted Interventions, pages 167–177,
Berlin, Heidelberg, 2012. Springer Berlin Heidelberg
