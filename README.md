# VLSI Floorplanning Optimization Tool in Python


The Google Collab Link is  uploaded above, and you can directly access it using the link below:
https://colab.research.google.com/drive/1nWHZZK4hrABCxtRPvYjDV4oCDJWnoZZO?usp=sharing

FloorPlanning is a very important and NP-hard problem in the VLSI Industry. 
There are some standard simulation and feedback-type algorithms in which we can get the correct result at the end.

The above code is the implementation of two of the types. Even though the input is the same, the way in which the output is converged is different. 

<img width="1280" height="720" alt="image" src="https://github.com/user-attachments/assets/90cc74b8-d4ef-4ac2-bdd6-f1e03a5b78c0" />
As we can observe in the above image, there will be so many blocks, and we need to arrange them in such a way that they will leave very little wastage area when the entire design is realized as a rectangle. 

The floorplanning representation in the form of symbols is belo,w and their corresponding floorplanning:
![WhatsApp Image 2025-09-03 at 15 44 55_74d46d12](https://github.com/user-attachments/assets/fb24eeda-98e5-448a-9625-bc7a6fcf7737)

To minimize the above wastage area, we have some basic operations by which we can change the given configuration. They are given below:
![WhatsApp Image 2025-09-03 at 15 44 55_57f68a4f](https://github.com/user-attachments/assets/0456e3cd-01ff-43e9-bd8e-7eb29270b3c8)

Now, by using these basic operations, we will be doing a search to find the best possible combination of the blocks to get the minimum area. 

In the above notebook. I had used some sort of DFS algorithm to find them as the first method. In the second method, I had used a search for some time limit. Which can be changed upon our wish, till the time limit is done, we will search for all the possibilities and note their area wastages, and at the end, we will get the minimum answer output. 


The sample input:
<img width="379" height="543" alt="{5F45492A-1E8E-45A9-B421-65630C15D31F}" src="https://github.com/user-attachments/assets/503a8155-b99f-420f-b701-707fed5128ee" />
<img width="390" height="143" alt="{12512640-6877-41E8-8621-BC4FB784F0D8}" src="https://github.com/user-attachments/assets/0cb75f3f-b023-4d7a-b27b-29b961154aab" />

The output of the first Algorithm : 

[('ab-cd-|ef|g-|', 231.0),
 ('ab-ed-|cf|g-|', 189.0),
 ('ab-ce-|df|g-|', 189.0),
 ('eb-cd-|af|g-|', 220.0),
 ('ag-cd-|ef|b-|', 220.0),
 ('ba-cd-|ef|g-|', 231.0),
 ('ab-gd-|cf|e-|', 168.0),
 ('db-ea-|cf|g-|', 180.0),
 ('ae-bd-|cf|g-|', 180.0),
 ('ba-ed-|cf|g-|', 189.0),
 ('ab-ed-|cf|g-|', 189.0),
 ('ba-ce-|df|g-|', 189.0),
 ('cb-ae-|df|g-|', 189.0),
 ('ae-cb-|df|g-|', 189.0),
 ('ab-ce-|df|g-|', 189.0),
 ('ab-ce-|df|g-|', 189.0),
 ('eb-cd|-af|g-|', 180.0),
 ('db-ce-|af|g-|', 190.0),
 ('ec-bd-|af|g-|', 190.0),
 ('cb-ed-|af|g-|', 200.0),
 ('ed-cb-|af|g-|', 200.0),
 ('ag-ed-|cf|b-|', 200.0),
 ('ag-ce-|df|b-|', 200.0),
 ('eg-cd-|af|b-|', 209.0),
 ('ga-cd-|ef|b-|', 220.0),
 ('ae-cd-|gf|b-|', 220.0),
 ('ba-ed-|cf|g-|', 189.0),
 ('ba-ce-|df|g-|', 189.0),
 ('ga-cd-|ef|b-|', 220.0),
 ('be-cd-|af|g-|', 220.0),
 ('ab-cd-|ef|g-|', 231.0),
 ('ba-gd-|cf|e-|', 168.0),
 ('ab-gd-|cf|e-|', 168.0),
 ('ab-gd-|cf|e-|', 168.0),
 ('ab-dg-|cf|e-|', 168.0),
 ('ab-gd-|cf|e-|', 168.0),
 ('dg-ea-|cf|b-|', 171.0),
 ('db-e-a|cf|g-|', 171.0),
 ('bd-ea-|cf|g-|', 180.0),
 ('db-ea-|cf|g-|', 180.0),
 ('db-ea-|cf|g-|', 180.0),
 ('ae-gd-|cf|b-|', 171.0),
 ('ea-bd-|cf|g-|', 180.0),
 ('ae-bd-|cf|g-|', 180.0),
 ('ae-bd-|cf|g-|', 180.0),
 ('ae-db-|cf|g-|', 180.0),
 ('ba-gd-|cf|e-|', 168.0),
 ('ea-bd-|cf|g-|', 180.0),
 ('bd-ea-|cf|g-|', 180.0),
 ('ab-ed-|cf|g-|', 189.0),
 ('ba-ed-|cf|g-|', 189.0),
 ('ab-gd-|cf|e-|', 168.0),
 ('db-ea-|cf|g-|', 180.0),
 ('ae-bd-|cf|g-|', 180.0),
 ('ba-ed-|cf|g-|', 189.0),
 ('ab-ed-|cf|g-|', 189.0),
 ('ab-ce-|df|g-|', 189.0),
 ('ea-cb-|df|g-|', 189.0),
 ('bc-ae-|df|g-|', 189.0),
 ('ba-ce-|df|g-|', 189.0),
 ('ba-ce-|df|g-|', 189.0),
 ('db-ae-|cf|g-|', 180.0),
 ('cg-ae-|df|b-|', 180.0),
 ('bc-ae-|df|g-|', 189.0),
 ('ab-ce-|df|g-|', 189.0),
 ('ce-ab-|df|g-|', 189.0),
 ('ae-db-|cf|g-|', 180.0),
 ('ae-cg-|df|b-|', 180.0),
 ('ea-cb-|df|g-|', 189.0),
 ('ce-ab-|df|g-|', 189.0),
 ('ab-ce-|df|g-|', 189.0),
 ('ba-ce-|df|g-|', 189.0),
 ('cb-ae-|df|g-|', 189.0),
 ('ae-cb-|df|g-|', 189.0),
 ('ab-ce-|df|g-|', 189.0),
 ('ab-ce-|df|g-|', 189.0),
 ('ba-ce-|df|g-|', 189.0),
 ('cb-ae-|df|g-|', 189.0),
 ('ae-cb-|df|g-|', 189.0),
 ('ab-ce-|df|g-|', 189.0),
 ('ab-ce-|df|g-|', 189.0),
 ('be-cd|-af|g-|', 180.0),
 ('gb-cd|-af|e-|', 180.0),
 ('eb-cd|-af|g-|', 180.0),
 ('eb-cd|-af|g-|', 180.0),
 ('eb-dc|-af|g-|', 180.0),
 ('dg-ce-|af|b-|', 144.0)]


The final one is the minimum obtained. 


The output of the second Algorithm(It's short because it has been run for almost 50 times the time taken for the before algorithm):
[('af-cd-eh-bg-|-|', 165.0),
 ('hf-cd-ea-bg-|-|', 165.0),
 ('hb-cd-ea-fg-|-|', 117.0),
 ('hb-cd--aefg-|-|', 110.0)]

 Look into the collab Link for more details. 

 

