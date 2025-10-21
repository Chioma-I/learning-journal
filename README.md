# Learning Journal
My learning journal! ^_^

## 14/10/2025
If I dont add a README file while creating a github repository then there is nothing to see on the repository page. To fix this I need to click on the example README file, which creates a new blank README file

## 18/10/2025
I did not notice the ai on visual studio gave me the incorrect code immediatly and got briefly confused by the error, I noticed it quickly and fixed it.
I dont know how to make an object move with mouse input instead of keyboard input, I need to search up tutorials.
I got an error telling me I was missing a bracket, took me a bit to find where I was missing one but I found it.
I found a code that said would workk for mouse input, but it doesnt. Might be smarter to see if i can translate the script that I know moves character with arrow keys into moving it with the mouse, but I need to work out how to do that
Asked a friend, Theo, for help, he gave me "Input.GetMouseButtonDown(0)" I tried put it in place of "Input.GetAxis("Horizontal")" but it gives a syntax error. 
Vector3 move = Vector3.right * Input.GetMouseButtonDown(0);
transform.Translate(move * speed * Time.deltaTime);
I had a different friend, Kiara, help me she sent me the code and explained parts in comments, she also explained to me other things that she didnt add comments to (eg the Header for the inspector in the first line) She really helped me out because some of this code is actually things I already know so i can actually mostly see what things are doing
<img width="770" height="653" alt="image" src="https://github.com/user-attachments/assets/64f8b626-4c71-4f7f-a579-60811466a6b6" />
<img width="708" height="636" alt="image" src="https://github.com/user-attachments/assets/5d487893-bed2-4c78-bdf5-46e05e36119e" />
<img width="784" height="651" alt="image" src="https://github.com/user-attachments/assets/c36e788f-6252-4ec7-9c0a-6e0f2ff9777b" />
The code she gave me allows the player to move along the X axis and the Z axis. Im going to try editing it so it only moves along the X axis.
I worked it out, "targetPosition.[] = transform.position.[];" allows you to keep something in the same position on that axis throughout movement!
i should put a gif of it working

## 21/10/2025
I need to test if the character changes direction with this movement script. I guess id have to put some asset on it...?
