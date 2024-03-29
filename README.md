# Autonomous-Cockroach-Detecting-Python-Algorithm
In sixth grade, I experimented to determine if cockroaches can overcome their fear of light. Though it took months to analyze all 24000 images taken, I was thrilled to discover that once one roach ventured into the light, others quickly learned from its example.

This tedious image analysis process inspired me to delve into my next research problem: the inefficiency of image analysis. To address this issue, the next year, in seventh grade, I wrote an algorithm that automatically detected cockroaches by comparing images to detect changes caused by a cockroach's entrance. I used thresholds to filter out very large changes caused by large changes in lighting (when someone accidentally turned the lights on in the room) and small changes caused by slight movement of the roaches as they ate. In the end, the algorithm is able to detect cockroach entrances with a 86.2% accuracy. What had taken me months of late nights amazingly took this algorithm mere seconds.

**comparison methods**
- subtraction -- OpenCV's subtract()
- Structural SIMilarity index -- scikit-image's SSIM

**comparison baselines**
each image was compared to three baseline images
- the first image in the batch 
  - pros: usually no roaches since I turned on the room light when I came in to download a batch (twice a day), so detected all images with a roach
  - cons: slight changes in ambient lighting levels caused false hits
- the previous image (images are taken once a minute):
  - pros: less sensitive to ambient lighting changes
  - cons: does not check first image (which has no previous image)
- the median image:
  - pros: most images don’t have cockroaches eating, so the median will not have any cockroaches.
    Also, since the median is the most common, most pictures will not have any irrelevant changes.
  

**AutonomousCockroachDetectingAlgorithmPoster.pdf:** poster from my presentation at the Pittsburgh Regional Science and Engineering Fair where I won 1st place in the Computer Science Intermediate division and the Intermediate Division Carnegie Science Award.

As the poster indicates, combining different methods and baselines improved performance. The success of this computer vision approach led me to apply more complex neural networks to tackle this image analysis problem the next year (Cockroach-Detecting-Neural-Network Repository).
