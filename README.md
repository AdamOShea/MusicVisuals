# Music Visualiser Project

Names: Shane Buckley, Adam O'Shea, Ignas Prakapas

Student Number: C20703429, C20372181, C20424992

## Instructions
- Fork this repository and use it a starter project for your assignment
- Create a new package named your student number and put all your code in this package.
- You should start by creating a subclass of ie.tudublin.Visual
- There is an example visualiser called MyVisual in the example package
- Check out the WaveForm and AudioBandsVisual for examples of how to call the Processing functions from other classes that are not subclasses of PApplet

# Description of the assignment
For my portion of the assignment, I decided to create a few visuals that are each based around a shape. I wanted the shape to grow everytime there is a beat in the song until it hits the borders of the screen. Once fully grown, the shape resets to its beginning size and its colour is changed. The background also changes colour with the shape but with a smaller opacity so that the colour in the shape is more prominent. In the centre of each visual is a rotating spiral of dots that grows and retracts with the amplitude analysed from the song. 
# Instructions
Press a corresponding number on your keyboard to change the visual.

| Keycode | Visual |
|---------|-----------|
| '1' | Centred Circle |
| '2' | Rectangles  |
| '3' | Hourglass Shape |
# How it works
In order to make shapes react to the beats in the song I used the isKick() method from ddf and made it increment a variable.
![image](https://user-images.githubusercontent.com/72108585/166341497-255b9695-edcd-452b-87b4-10c219fd7372.png)

The first visual is simply a circle that grows from the centre. Once its radius is more than the width of the screen it resets and reassignColours() is called to change its colour.
![image](https://user-images.githubusercontent.com/72108585/166342865-679a8c88-6952-42f3-b0d3-fbcc6eb6e7c7.png)

The second visual contains 4 rectangles that grow from the corners of the screen to the centre where the overlap to make the colour more prominent. They reset once they have fully overlapped.
![image](https://user-images.githubusercontent.com/72108585/166343026-c397a18f-3566-4e4d-ad87-e1b10ed94eb5.png)

The third visual is a series of triangles that are mirrored to create an hourglass shape. The visual is also rotates around the centre point.
![image](https://user-images.githubusercontent.com/72108585/166343302-4bfc366a-4e81-4791-89fb-22ad05402083.png)

For the spiral that is featured in each of the visuals I used the getSmoothedAmplitude() method to make the points expand and retract whenever there is a beat in the song. I used cos and sin to make the lines of dots curve. I also made them rotate 
![image](https://user-images.githubusercontent.com/72108585/166343879-4b0effde-b771-45d6-a456-817fc41c4c13.png)

# What I am most proud of in the assignment
I am especially proud of figuring out how to make the spiral. It was quite tricky for me as I have never had a great grasp on using trigonometric methods. I really like it because it kind of resembles the front of a big speaker which I think is very fitting for this assignment.

# Markdown Tutorial

This is *emphasis*

This is a bulleted list

- Item
- Item

This is a numbered list

1. Item
1. Item

This is a [hyperlink](http://bryanduggan.org)

# Headings
## Headings
#### Headings
##### Headings

This is code:

```Java
public void render()
{
	ui.noFill();
	ui.stroke(255);
	ui.rect(x, y, width, height);
	ui.textAlign(PApplet.CENTER, PApplet.CENTER);
	ui.text(text, x + width * 0.5f, y + height * 0.5f);
}
```

So is this without specifying the language:

```
public void render()
{
	ui.noFill();
	ui.stroke(255);
	ui.rect(x, y, width, height);
	ui.textAlign(PApplet.CENTER, PApplet.CENTER);
	ui.text(text, x + width * 0.5f, y + height * 0.5f);
}
```

This is an image using a relative URL:

![An image](images/p8.png)

This is an image using an absolute URL:

![A different image](https://bryanduggandotorg.files.wordpress.com/2019/02/infinite-forms-00045.png?w=595&h=&zoom=2)

This is a youtube video:

[![YouTube](http://img.youtube.com/vi/J2kHSSFA4NU/0.jpg)](https://www.youtube.com/watch?v=J2kHSSFA4NU)

This is a table:

| Heading 1 | Heading 2 |
|-----------|-----------|
|Some stuff | Some more stuff in this column |
|Some stuff | Some more stuff in this column |
|Some stuff | Some more stuff in this column |
|Some stuff | Some more stuff in this column |

