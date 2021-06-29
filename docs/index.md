# Getting Started

Photon is a hypersafe and fast language for manipulating images, with a quickly growing community! Let's take a look at some basic photon syntax:

```
OPEN 'image.png' as image
APPLY 'solarize' TO image
SAVE image TOSYS 'output.png'
CLOSE image
```
## Explanation

There's not much going on here, but let's look at this line by line:

First let's identify that each line in photon is called a `query`. Each `query` has a beginning `statement`. Think of statements as a commands to do something to an image. Photon tries to make these statements as user-friendly as possible.

### Statements

The `OPEN` statement opens our image, and loads it into our environment. The `'image.png'` signfies the file-path where the image is located. Here, our image is located in the root directory of our project, thus we can just reference it as `'image.png'`.

The `APPLY` statement applies an `effect` to our image. These effects can be pre-made effects within Photon, or effects from one of the open-source libraries that Photon uses. In this case, we use the `'solarize'` effect. The `TO` statement tells Photon what to apply the effect to. Here the `image` word is an `identifier` in Photon. So in Photon terms, we're applying the `solarize` effect to our `image` identifier.

The `SAVE` statement saves the `IO` attached to our identifier to a specified file-path. `TOSYS` exists to make it clear that we are saving it to our system rather than an identifier.

The `CLOSE` statement is good practice to use when you are finished with an image as it removes it from the environment, allowing you to use the same identifier name again.

Identifiers in Photon silently fail when assigning them to new images, allowing them to act like normal variables in other popular languages.