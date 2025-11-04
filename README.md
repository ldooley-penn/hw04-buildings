# CIS 5660 HW04 Procedural Buildings

## Project Planning

For this project I want to recreate the style of the Sugarbush Resort in Warren VT.

These reference images are courtesy of the sugarbush website:

![](Images/SugarbushTopView.jpg)

![](Images/SugarbushSideView.jpg)

![](Images/SugarbushCloseup.jpg)

I envision the procedural process of building this being:

1.  Define a base layout using lines , whether fully procedural or art directable.
2. Segment the layout into 2 types, either the more barn like type you can see on the right of the first image, or the more standard sloped building you see on the left of the first image.
3. Give the layout thickness depending on the segmented type.
4. Build up floors, with the bottom one being stone and wood otherwise.
5. Add first floor overhang with support columns.
6. Adding balconies with support beams.
7. Use booleans or other methods for creating roofs.

### Assets
I will need assets for windows with 2 and 3 panels, fenced balconies, doors, and a roof at a base level.

## Building Process

I first started by implementing the box stacking from the tutorial:

<img width="1382" height="678" alt="BoxStacking" src="https://github.com/user-attachments/assets/d9569873-68bb-476e-8d49-b5e6fe6372a3" />

After this I made assets for the windows, door, and balcony in blender, and scattered them over the floors:

<img width="925" height="695" alt="AddingDetails" src="https://github.com/user-attachments/assets/037ad830-e9be-41ac-b04d-1e0457884979" />

Next, I added pillars and borders on the floors:

<img width="622" height="625" alt="Pillars" src="https://github.com/user-attachments/assets/53b87af8-2cf4-417b-9660-6dec30e88caf" />

<img width="621" height="660" alt="Borders" src="https://github.com/user-attachments/assets/ee43c5e9-64fc-41a9-9fb9-90c02e77fb29" />

Then I followed the tutorial's guidelines on adding support beams:

<img width="858" height="702" alt="SupportBeams" src="https://github.com/user-attachments/assets/52a6cc8f-3272-40f0-9583-25a9055ba608" />

Since my reference had a roof, I decided to augment slightly by adding a new subnetwork after my for loop over the floors which added a roof that is the same scale as the last floor. I did this by splitting the box by normals, and used attribute wrangles to do the transformations I wanted. Finally I extruded the plane to make the roof thicker.

<img width="692" height="711" alt="Roof" src="https://github.com/user-attachments/assets/6feb8927-38d6-4427-ac73-826f7246acd7" />

In action, the tool looks like this:

https://github.com/user-attachments/assets/c134c555-1ead-46b8-b19a-2bf83d2adaec

I'll also note that the inspiration has quite a few less features than in the video (namely that floors are not random and are also uniformly sized), but I am including everything here for demonstration purposes.
