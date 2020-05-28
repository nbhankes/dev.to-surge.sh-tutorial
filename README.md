This tutorial will teach you how to design your first website and deploy it to the web.

What you'll need:
-The free VS Code software
-Your computer
-An internet connection

#Download VS Code

Click [here] (https://code.visualstudio.com/download) to download VS Code, which is the software you will use to write your code during this tutorial. Select the option that applies to your operating system and follow the commands.
![Picture of VS Code Download Option](https://dev-to-uploads.s3.amazonaws.com/i/1aqdwwwlrau9ff73mglz.png)


#Setting Up the Project
Let's start by preparing the folder where your website will be stored. Go to your documents folder and create a folder called WebProjects. Within this folder create a folder called Project-1.

Now go back to your desktop and Open VS Code. Create a new file named index.html and save it inside of the Project-1 folder. Now create another file called stylesheet.css and save this in the Project-1 folder.

We have successfully generated the files for our project. Your file path should now look like this:
![Picture of Files in Folder](https://dev-to-uploads.s3.amazonaws.com/i/rl4l52ks8tri8rckrf41.png)

And your VS Code will look like this:
![Picture of VS Code with project Files](https://dev-to-uploads.s3.amazonaws.com/i/173vva0nig9chximhxk2.png)

#Writing Your HTML Code
I will provide each segment of code individually, so that I can explain it's purpose as we go.

In order for the web browser to know that it is rendering an HTML document, all HTML documents must start with this identifier:
```
<!DOCTYPE html>
```
This is the code that will always be at the top of any HTML file. Copy and paste that line into the index.html file in VS code.

Computers are hyper-literal, so we must put all of our code within the following elements:
```
<html>
   /* You will insert all of the rest of your HTML elements between the <html> </html> two brackets */
   /* Any writing between the forward slash and asterisk are skipped over when the document renders */
   /* Developers rely on these areas to write notes */
</html>
```

Your index.html file will now look like this:
![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/084xs0nd2s3eok3xn9di.png)

Great! Now delete all of the notes and insert the following header in their place:
```
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My First Website</title>
</head>
```

Beneath the end of the head element, insert the body of your website:
```
        <body>
            <div class="top">
                <h1>This is My First Website.</h1>
            </div>
            <div class="middle">
                <p>"The Internet is the first thing that humanity has built that humanity doesn't understand, the largest experiment in anarchy that we have ever had." - Eric Schmidt, Google</p>
            </div>
            <div class="bottom">
                The End.
            </div>
        </body>
```

Now clean up your code by indenting any nested elements, like so:
![The HTML code](https://dev-to-uploads.s3.amazonaws.com/i/cfqsckobkaq681kza9m3.png)

Now if you drag the index.html file from your VS Code into your favorite browser, or navigate into your Project-1 folder and choose to open the index.html file with the browser of your choice, you will see this:
![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/6ntxr0drc1ntrywnbdy7.png)

This is what basic HTML looks like. Now we will use CSS to change how our HTML elements look.

#Writing Your CSS

Before we can style the index.html with any CSS code, we'll need to ensure that the index.html file knows that it should look for the stylesheet.css document. We do this by creating a link.

Inside of the index.html head element, insert the following code:
```
    <link rel="stylesheet" href="stylesheet.css">
```

Save the changes to the index.html document. Now access your stylesheet.css file within the VSCode editor. Add the following code:
```
html {
background: red;
}
```

Now when you open or refresh the index.html file within your browser, the background should appear red. We now know that the index.html is referencing the stylesheet.css file.

Delete the previous CSS code and insert the following code into the document:
```
html {
  font-family: sans-serif;
}

.top {
  width: 100%;
  height: 8rem;
  background: black;
  color: white;
  font-family: sans-serif;
  text-align: center;
  padding-top: 2.5rem;
}

.middle {
  font-size: 6rem;
  margin: 0rem 2rem;
}

.bottom {
  width: 100%;
  height: 8rem;
  background: black;
  color: white;
  font-size: 6rem;
  font-family: sans-serif;
  text-align: center;
  padding-top: 1rem;
}
```

Now save your changes and refresh the index.html file in your browser. Your website should now look like this:
![Website Preview with CSS changes](https://dev-to-uploads.s3.amazonaws.com/i/ndhs80vm0wc90ucl49c5.png)

While this is basic and unsexy, you should now have enough familiarity to begin tinkering with the look and layout of your very own webpage.

#Deploying to the Internet

Now comes the scary part for most beginners. The next step requires us to work with the command line. We are going to install surge. Enter the following code into the terminal and hit return:
```
npm install --global surge
```

Once surge successfully installs, we'll drag and drop our Project-1 folder into the terminal. But first, type cd, add a space, and then drag the Project-1 folder into the terminal. Hit return.

The terminal will now display that you are inside of the Project-1 folder. You should see something like this:
![cd in terminal](https://dev-to-uploads.s3.amazonaws.com/i/mtnypgzmnimra9ybwm9y.png)

Now type surge and hit return. Follow the prompts. Surge provides a randomized URL name, but you can delete this and add your own. It must, however, end in "surge.sh".

If you have successfully deployed your website to the surge server, your terminal should say "Success!" and display your URL. It will look something like this:
![surge successful in terminal](https://dev-to-uploads.s3.amazonaws.com/i/ksnzee4morvmvcu8e0t8.png)


Now follow the link to view and share your very first website:

[project-1-devDemo.surge.sh](project-1-devDemo.surge.sh)

For more information about surge, visit [surge.sh](https://surge.sh/)
For more information about working in the terminal, visit [Introduction to the Command Line Interface](https://tutorial.djangogirls.org/en/intro_to_command_line/)


Welcome to the world of web dev, Champ.
