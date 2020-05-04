# cricket-vision

Exploring CV concepts with cricket visual data

## Audio Extractions

* To classify the acoustic events from a stream of sounds recorded in a cricket shot, the sound needs to be segmented into small sound windows on which a machine learning model is applied.
* Traditional acoustic analysis systems often partition the sound into equally-sized windows starting from the beginning of the soundrecording. However, since cricket events are sparsely distributed overtime and usually have a very short duration, the above approach may cause the sound of interest span over two different windows, which degrades the sound classification accuracy. To tackle this problem, __we implement a peak detection approach that detects thesound of interest and isolates it within a single window.__

The next step is to detect or determine which window corresponds to what event, else detect which window holds the striker's swing/contact with ball.

### Acoustic Data Other References

* MFCC feature extraction
* ML models can be learnt but unncessary for now, as it involves only one event detection and as such no classification.

#### Need to look up

1. Study with frequency, pitch and fft etc, involved signal processing

2. Analyze __HIERARCHICAL LANGUAGE MODELING FOR AUDIO EVENTS DETECTIONIN ASPORTS GAME__ <http://www.cvssp.org.uk/acasva/Publications/ICASSP_2010.pdf>

## References

* __Detection of Ball Hits in a Tennis Game Using Audio and Visual Information__: <http://www2.cmp.uea.ac.uk/~sjc/BH_AV_QH2_SJC2.pdf>

* __Detection of Tennis Events from Acoustic Data__: <https://researcher.watson.ibm.com/researcher/files/us-wangshiq/AB_MMSports2019.pdf>

* __Ball Tracking__: <https://github.com/nikhil-dev/hawkeye>

* __Pose Estimation__: Estimate and distinguish between poses of striker when the ball hits the bat.

* __Edge Detection System__: <https://www.researchgate.net/publication/266887698_The_5_th_Umpire_Crickets_Edge_Detection_System>
