# How to set up C++ visual studio project

Start with a C++ empty project at a centralize location.

No need to create it in a special folder because Create directory for solution is checked.

![](.gitbook/assets/image%20%2818%29.png)

When you open the folder you will see a .sln file and a project folder

![](.gitbook/assets/image%20%288%29.png)

Inside the folder contains the vcxproject and filter

 

![](.gitbook/assets/image%20%282%29.png)

Create a folder call source to store all the source code. 

![](.gitbook/assets/image%20%284%29.png)

When you click on you project, there is this button called **Show ALL Files.** If we click that, this view is your directory structure that is on your disk. So now we create a folder call src.

Now we want to configure where our output and intermediate Directory goes to.

For output: 

**$\(SolutionDir\)\bin\$\(Platform\)$\(Configuration\)\**

This will go to the root of the project where the .sln is at. 

For Intermediate directory:

**$\(SolutionDir\)\bin\intermediates\$\(Platform\)$\(Configuration\)\**

![](.gitbook/assets/image%20%286%29.png)

Now we can see bin properly setup in the root folder

![](.gitbook/assets/image%20%283%29.png)

















