## Algo's for Realtime detections

| Curr Algo  O(objects * detection time)                 |          Advanced Algo O(detection time)   |
| -------------------------------------                  |           -------------------------------- |

|1. Get Objects                                         |         1. Get Objects |
|2. See if all the objects in the scene are done?       |         2. See if all the objects are done |
|3. Segement the objects that are not done yet          |         3. Run logo detection on the whole frame once |
|4. Run logo detection on all of these objects          |         4. For each of the objects that are not done .. get logo's detected for that object |
|the logo detected of the same object have been         |         5. If the model confidence on any logo > 40% or       |
|detected same in 20 or more frames .. lock that object |         the logo detected of the same object have been        
                                                       |         detected same in 20 or more frames .. lock that object |

|Detections Run = Number of new objects in the scene    |         Detections Run = 1|






## Practical Problems with Advanced Algo
- As soon as we pass the entire frame to the model .. the model confidence on logo and the accuracy of the model decreases
   - Maybe because the training set mostly consists of data that is consisting a single object
- Since due to the reason 1 mentioned above we ultimately have to process more frames .. and run detection more number of times .. the time taken for processing again drops
- **Incorrect Assumption::** Model is as accurate in classifying in multiple logos in an image .. as it is in the single image


## Conclusion (Select Approach A as final)
- Approach A is faster overall .. B is faster for a frame .. but otherwise slower and will also give us bad results
