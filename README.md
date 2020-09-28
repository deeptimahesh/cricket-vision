# cricket-vision

Exploring CV concepts with cricket visual data

## 1. Audio Extractions

* To classify the acoustic events from a stream of sounds recorded in a cricket shot, the sound needs to be segmented into small sound windows on which a machine learning model is applied.
* Traditional acoustic analysis systems often partition the sound into equally-sized windows starting from the beginning of the soundrecording. However, since cricket events are sparsely distributed overtime and usually have a very short duration, the above approach may cause the sound of interest span over two different windows, which degrades the sound classification accuracy. To tackle this problem, __we implement a peak detection approach that detects thesound of interest and isolates it within a single window.__

The next step is to detect or determine which window corresponds to what event, else detect which window holds the striker's swing/contact with ball.

### Acoustic Data Steps

* MFCC feature extraction
* ML models can be learnt but unncessary for now, as it involves only one event detection and as such no classification.

#### Need to look up

1. Study with frequency, pitch and fft etc, involved signal processing

2. Analyze __HIERARCHICAL LANGUAGE MODELING FOR AUDIO EVENTS DETECTIONIN ASPORTS GAME__ <http://www.cvssp.org.uk/acasva/Publications/ICASSP_2010.pdf>

### References (Audio)

* __Detection of Ball Hits in a Tennis Game Using Audio and Visual Information__: <http://www2.cmp.uea.ac.uk/~sjc/BH_AV_QH2_SJC2.pdf>

* __Detection of Tennis Events from Acoustic Data__: <https://researcher.watson.ibm.com/researcher/files/us-wangshiq/AB_MMSports2019.pdf>

* __Ball Tracking__: <https://github.com/nikhil-dev/hawkeye>

* __Pose Estimation__: Estimate and distinguish between poses of striker when the ball hits the bat.

* __Edge Detection System__: <https://www.researchgate.net/publication/266887698_The_5_th_Umpire_Crickets_Edge_Detection_System>

## 2. Video Extractions

* Action detection in videos that learns to directly predict the temporal bounds of said action
* Formulate a model  as  a  recurrent  neural  network-based  agent  that  interacts  with  a  video  overtime.   The  agent  observes  video  frames  and  decides  bothwhere  to  look  next  and  when  to  emit  a  prediction.

### Another method

* It is mainly composed of three steps:

        (i) temporal sliding window,
        (ii) clip representation and classification, and
        (iii) post processing.
* Set the length of window as 150 frames and the slidingstep as 100 frames.
* Then, for each short temporal window, we perform the task of action recognition independently. Eventually, the recognition results of theseshort window are combined to yield the final result of the whole video stream.

### References (Video)

* __Motion and Recognition__ : <https://www.crcv.ucf.edu/THUMOS14/papers/CUHK&SIAT.pdf>
* __Action Detection from Frame Glimpses__ : <http://vision.stanford.edu/pdf/yeung2016cvpr.pdf>,

        Code: <https://github.com/syyeung/frameglimpses>

## 3. Ball Detection

### References (Ball Detection)

* Detection and Tracking : <https://www.analyticsvidhya.com/blog/2020/03/ball-tracking-cricket-computer-vision/>
