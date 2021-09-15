summary of the insanity presented at Tesla AI day, Aug 2021. Link [Here](https://www.youtube.com/watch?v=j0z4FweCy4M)
#Main idea: Engineering from ground up
- Anyone who has done ANY sort of end-to-end or half end-to-end ML project will have their jaw drop at this livestream. LOL
- Initiation question: how may we let cars drive themselves?
- Sub 2 questions: Need to be able to understand (see) the things in the environment. Need to be able to control the car based on information in the environment + objective (go from point A to point B)
Qn1: How to see.
- Vision
- So many end of line sub-tasks. No way you can train one NN for each task.
- Hydra method (I think this was presented last time liao) where you have one common backbone that is rarely trained, with multi-multi heads for each sub-task. 
- Only fine-tune the heads. 
- How tf is this co-ordinated? LOL. madness.
-  
Qn2: How to move.
- Based on ... derive the optimal pathing
- Simulations of all other entities as players.
- Run multiple sims, choose optimal path (even for simple task like wanna turn right, many ways to do it.)
- Optimal is optimising for stuff like safety, G's, ???

## Data pipeline
### Manual labelling:
- Start with outsourced labellers, too high latency/delays. So build inhouse labelling team (apparently 1k headcount of professional labellers.). What is needed: training for labellers. New Labelling platforms for VECTOR SPACE which is insane (anyone that used stuff like labelbox/diffgram/AWS for just 2D images will know lol). 
- labelling on 2D images with polygons too inefficient because need 3D/4D vector space labels. So build a labelling platform that can take in vector space labels, project onto 2D. 100x speedup.
- 
### Auto labelling
We want as little human labour as possible. So enter auto labeling methods.
- Pre trained networks are able to do most of the labelling, for simple stuff such as road surfaces, curbs, roadwalks etc. segmentation networks!
- Collection from fleet. In one week can collect 10k labelled video clips of shit falling off the top of a truck and occluding view. too insane.
- Simulations (Think GTA5 <> cityscapes). Why good? perfect labels, easily get rare cases, label multiple entities easily, ???. Whats tough? Need to encompass camera hardware characteristics into the simulation. Stuff like response to aperture angle, exposure, lighting?
- 
