# Learning Journal

## 14/10/2025
If I dont add a README file while creating a github repository then there is nothing to see on the repository page. To fix this I need to click on the example README file, which creates a new blank README file


## 18/10/2025
I did not notice the ai on visual studio gave me the incorrect code immediatly and got briefly confused by the error, I noticed it quickly and fixed it.

I dont know how to make an object move with mouse input instead of keyboard input, I need to search up tutorials.

I got an error telling me I was missing a bracket, took me a bit to find where I was missing one but I found it.

I found a code that said would work for mouse input, but it doesnt. Might be smarter to see if I can translate the script that I know moves character with arrow keys into moving it with the mouse, but I need to work out how to do that.

Asked a friend, Theo, for help, he gave me "Input.GetMouseButtonDown(0)" I tried put it in place of "Input.GetAxis("Horizontal")" but it gives a syntax error. 
Vector3 move = Vector3.right * Input.GetMouseButtonDown(0);
transform.Translate(move * speed * Time.deltaTime);

I had a different friend, Kiara, help me she sent me the code and explained parts in comments, she also explained to me other things that she didnt add comments to (eg the Header for the inspector in the first line). She really helped me out because some of this code is actually things I already know so I can actually mostly see what things are doing

<img width="770" height="653" alt="image" src="https://github.com/user-attachments/assets/64f8b626-4c71-4f7f-a579-60811466a6b6" />
<img width="708" height="636" alt="image" src="https://github.com/user-attachments/assets/5d487893-bed2-4c78-bdf5-46e05e36119e" />
<img width="784" height="651" alt="image" src="https://github.com/user-attachments/assets/c36e788f-6252-4ec7-9c0a-6e0f2ff9777b" />

The code she gave me allows the player to move along the X axis and the Z axis. Im going to try editing it so it only moves along the X axis.

I worked it out, "targetPosition.[] = transform.position.[];" allows you to keep something in the same position on that axis throughout movement!
![Point   Click Movement](https://github.com/user-attachments/assets/a970c126-97c0-4c66-acf6-b72ced1a885c)


## 21/10/2025
I need to test if the character changes direction with this movement script. I guess I'd have to put some asset on it...?

In Unity 6 to create a script you need to right click, create, scripting, the choose the type of script, usually MonoBehaviour

## 24/10/2025
I was quickly trying to make a movement script from memory (I managed to do half of it, I'll memorise it eventually) but I decided I also wanted to try moving up and down too, not jump movement but top down rpg style movement. It moves in the Z axis instead of the Y axis, need to figure out how to change that. 
Tried to change it in the Input Manager, did not do anything.
Worked it out, im supposed to put "up" for the second vector3 code, not forward. Also worth noting you can have any variable after vector3. I dont know what variable name would be smarter but since "move" was in use I used "evom".
I cant recall the difference between MonoBehaviour and ScriptableObject, not sure which the camera should use
First im trying to use a tutorial online, I entered only a bit of code and but the moment I ran my program it caused an error
<img width="753" height="37" alt="image" src="https://github.com/user-attachments/assets/4b2c5a78-b99c-44a0-a51b-9878de506701" />
Thought I worked it out, the first line of code, "public class" didnt say the name of the file. Fixed it but that didnt fix the error.
Removed this code to start afresh.

## 27/10/2025
Kiara has given me a script and explained some things in the script, some things in our texts when I asked questions.
https://www.programiz.com/online-compiler/3LqwlEVJVSyVA
At first it seemed like it didnt work. The movement seemed to no longer work.
![2D Camera error](https://github.com/user-attachments/assets/2b9eaa28-4fbe-47ee-85be-c0e1256daadd)
Afterwards I realised that it might look like it doesnt work because theres nothing else in the scene, after I added something it was clear that it was always fine.
![2D Camera](https://github.com/user-attachments/assets/b6120136-2041-4901-8877-313cf3594d28)

## 28/10/2025
You need to upload Assets, Packages and ProjectSettings files from your Unity project into GitHub. Dont upload anything while Unity is open, close Unity first.
I need to remove the spaces from my Unity Project. To do this I need to rename the folder in the files and then remove the project from the project list and then re-add it to the unity hub again


## 8/11/2025
I tried searching up how you would make audio trigger in Unity. I read through https://discussions.unity.com/t/trigger-audio-event/640358 for my intial script. After following this I had logical errors, the code itself has what I assume is a variable underlined in green? The script confuses me because if it is a variable should it not be stated earlier in the code, why is the underline green?
It says I need to give an object a rigid body for it to activate triggers, upon doing this nothing happens still.

I worked it out, adding a capsule collider to the audio game object made it so it triggered audio! It retriggers the audio every time movement happens within the hitboxes though, need to fix that.
https://github.com/user-attachments/assets/cc56e35a-470f-479d-8c25-83aea01ed2f1
Kiara helped me fix it, by adding "&& !audio.isPlaying" you set an instruction to only play if its is not already playing. && is the and operator for C# and ! in front of a statement means not like it meant in python too.
https://github.com/user-attachments/assets/709c2663-dca9-434c-b73a-3c773616359e
<img width="626" height="305" alt="image" src="https://github.com/user-attachments/assets/9d8f88d8-cd91-4808-a27e-025657ae575a" />

Voiceline used for the audio is from Lauren Impsumm in the game Date Everything, voiced by Allegra Clark

## 16/11/2025
I have asked Kiara for help regarding triggering texts. This is the script she gave me alongside other explanations
<img width="739" height="625" alt="image" src="https://github.com/user-attachments/assets/38829b61-9a70-46ba-b0cd-8a38ec0f5bf0" />
<img width="545" height="738" alt="image" src="https://github.com/user-attachments/assets/acac5b37-8bfa-439d-89f4-a6bd0442bda0" />
<img width="785" height="96" alt="image" src="https://github.com/user-attachments/assets/564992e4-d3f0-42b3-8a94-0b76dcfd639b" />
However 7 different errors appeared after doing doing this, the first error is with unity not recognising the Player tag, which confuses me because this worked fine with the audio trigger. Figured it out, it was the speechmarks from copying the script, not sure why this happened but somehow the speechmarks were wrong. All 7 errors were because of this.
![Text Trigger error](https://github.com/user-attachments/assets/3c8446cd-6834-4b9d-86ab-8e9c6056dd64)
Logical error, the text isnt appearing and I dont know why.
Adding a debug script to the script to find the issue
<img width="607" height="268" alt="image" src="https://github.com/user-attachments/assets/bf1926e1-0ec5-4ce8-b229-f1ab6f5e3f8d" />
"OnTriggerEnter" shows as an error, not sure why. It gives a suggestion but the suggestion is also an error

We ended up starting from scratch with a new script
<img width="781" height="405" alt="image" src="https://github.com/user-attachments/assets/310d70d1-73e6-4229-9498-3c561355b74b" />
<img width="645" height="658" alt="image" src="https://github.com/user-attachments/assets/09ab04c0-6bc8-49c0-808a-79d43d710b1a" />

The new script worked perfectly!
![Text Trigger](https://github.com/user-attachments/assets/b6f61237-08bb-442e-abef-472639bf4925)


## 28/11/2025
<img width="635" height="338" alt="image" src="https://github.com/user-attachments/assets/43b00041-c04e-474c-ac6d-a63b307e83a5" />
Some error wont let me add scripts to objects in unity
<img width="771" height="108" alt="image" src="https://github.com/user-attachments/assets/c9e26484-3fbb-417f-b24e-7e0c4722ef64" />
Something about the camera script broke the movement script and I'm not sure why

The loop in the movement script is in place so that the script works with or without a camera, broke when a camera was added, not sure why this is but commenting it out fixed the issue anyway.
Did not fix it, now the movement doesnt work...
The camera moves on its own? For some reason?
Brought back the script, cant just comment it out, I need to edit it, I think
<img width="505" height="113" alt="image" src="https://github.com/user-attachments/assets/db22988c-9350-4e7f-9bdb-fa98f7dd722c" />

## 2/12/2025
With Paul's help I figured out what was wrong. First of all I named my script "Camera" and Unity already has a Camera script so there was confusion there, where in my script I refferred to Unity's Camera, Unity thought I reffered to my Camera. To fix that we just needed to define we were refferring to Unity's Camera in the script with "UnityEngine.Camera.main". The second problem was a logical error, the movement not working at all. This was because the camera was positioned at the same height as the player, and so the ray cast from the player was a point thin and nigh impossible to click. This wasnt a problem in the original script because it made no changes to Unity's camera and was already positioned in a way that let the player hit the ray. To fix this we had to move the camera's position up on the y axis.

## 4/12/2025
The text trigger script did not work, I realised this was simply because I forgot to move the poem trigger game object so it would be on the same invisible plane as the player.


https://github.com/user-attachments/assets/cd8fe07c-b60d-430a-9d22-5235de0117e5

## 9/12/2025
Uploading the project on github gives me an error, saying "fatal: detected dubious ownership in repository {file}". I get this error because my project is on my external hard drive and github does not trust this. All you need to do to fix it is make github trust it. Currently dont know how to get the pop up to show up again...
<img width="794" height="307" alt="image" src="https://github.com/user-attachments/assets/e85866fb-fc25-4450-afcf-bf023ff10ac9" />

## 16/12/2025
Figured out the solution. If I search "gitcongif" in my files I'll find a file, if I open this as a notepad there will be some information. Under [safe] I can write "directory = {filelocation}". Writing a command that makes any specific file I write safe to github. 
