# Materialize Parallax Instructions from Katie!
#### For my wonderful FEWD Students

___

Hey guys,

I know some of you mentioned you were having trouble figuring out how to implement Materialize's parallax effect, found here: http://materializecss.com/parallax.html

While Materialize does offer their own instructions, here I'm going to give you more detailed steps for setting this up. You can also use these instructions as a reference to implementing other Materialize javascript effects.

## Step 1: Download Materialize

Go <a href='http://materializecss.com/getting-started.html'> here</a> and click the download button that says "MATERIALIZE."
___

## Step 2: Place Materialize Files in Project Folder

Open up that zip file you just downloaded. In it, you should see a folder structure that looks like this:
```
├── README.md
├── LICENSE
├── css
│   ├── materialize.css
│   └── materialize.min.css
├── fonts
│   └── roboto
└── js
    ├── materialize.js
    └── materialize.min.js
```

First, place materialize.css into your project's styles folder. You don't need to use both materialize.css and materialize.min.css - they're two versions of the same thing. For now, if you want to be able to read Materialize's code more clearly, don't use the .min.css version. That version will load more quickly in browsers, however, so once you've completed your project, you may want to use that one instead.

Next, place materialize.js in your scripts folder, alongside your app.js file.

___

## Step 3: Link to Materialize Files in Your HTML Doc

Now we need to link to those files in your HTML `<head>`. Add both of these to link to both their css and their javascript libraries:
```
<link rel="stylesheet" href='style/materialize.css'>
```
Be sure to list your own main.css file AFTER materialize.css in your `<head>` so that their styles don't override your own!
```
<script src='scripts/materialize.js'></script>
```
___

## Step 4: Link to jQuery in Your HTML Doc

This is an important one. In order for the browser to read Materialize's js, we need to import the jQuery library in our `<head>` as well.

```
<script type="text/javascript" src="https://code.jquery.com/jquery-3.2.1.min.js"></script>
```
Order is important here as well. JQuery must be listed ABOVE materialize.js. In all, your `<head>` should look similar to this:
```
head>
  <meta charset="utf-8">
  <title>Title Goes Here</title>
  <link rel="stylesheet" href='style/materialize.css'>
  <link rel='stylesheet' href='style/main.css'>
  <script type="text/javascript" src="https://code.jquery.com/jquery-3.2.1.min.js"></script>
  <script src='scripts/materialize.js'></script>
  <script src='scripts/app.js'></script>
</head>
```
___


## Step 5: Apply Materialize Classes in Your HTML Doc

Next we need to apply Materialize's CSS classes in your HTML file.

If you go back to Materialize's documentation page, they include a sample of what your parallax section should look like:
```
<div class="parallax-container">
  <div class="parallax"><img src="images/parallax1.jpg"></div>
</div>
```
You'll want to use the same structure and class names.

___

## Step 6: Call Materialize Functions to Your Javascript

Alright, we're almost there! For this last part, we need to call the Materialize js functions in our own app.js file. On the instructions from Materialize, they always give us the code we need to use to call whatever feature we want to add, under a heading that says "Initialization". That's where I got the code below. Open app.js and place this in there:
```
$(document).ready(function(){
  $('.parallax').parallax();
});
```

Now if you save all your files and refresh your page, it should be working! Please feel free to reach out if you have further questions.
