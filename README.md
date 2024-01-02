# Autonomous-Cockroach-Detecting-Python-Algorithm
In sixth grade, I experimented to determine if cockroaches can overcome their fear of light. Though it took months to analyze all 24000 images taken, I was thrilled to discover that once one roach ventured into the light, others quickly learned from its example.

This tedious image analysis process inspired me to delve into my next research problem: the inefficiency of image analysis. To address this issue, the next year, in seventh grade, I wrote an algorithm that automatically detected cockroaches by comparing images to detect changes caused by a cockroach's entrance. I used thresholds to filter out very large changes caused by large changes in lighting (when someone accidentally turned the lights on in the room) and small changes caused by slight movement of the roaches as they ate. In the end, the algorithm is able to detect cockroach entrances with a 86.2% accuracy. What had taken me months of late nights amazingly took this algorithm mere seconds.

**comparison methods**
- subtraction -- OpenCV's subtract()
- Structural SIMilarity index -- scikit-image's SSIM

**comparison baselines**
each image was compared to...
- the first image in the batch (2 batches per day since I downloaded images twice a day)
  - usually no roaches since the roaches were afraid when I came in to take the phone and download images
- the previous image
- the median image

**AutonomousCockroachDetectingAlgorithmPoster.pdf:** poster from my presentation at the Pittsburgh Regional Science and Engineering Fair where I won 1st place in the Computer Science Intermediate division and the Intermediate Division Carnegie Science Award.
