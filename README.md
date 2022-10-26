# TAILWIND

In this quick guide I will introduce you to [Tailwind CSS](https://tailwindcss.com/).
Tailwind is a low-level CSS framework which will speed up your development process.
The framework is composed of a long list of CSS classes and queries but as opposed to Bootstrap it will only insert the classes you need into your stylesheet, keeping the files much much smaller.

## INSTALLATION

### 1. Terminal

To install tailwind you will have to run those 2 commands, first one will download the required files and the second one will create all needed files within your folder structure.

```
npm install -D tailwindcss
npx tailwindcss init
```

### 2. tailwind.config.js

Here you need to specify which files tailwind will track by default you want to make sure it tracks all html and js files. If you are using subfolders, make sure to include them.

```
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ["./*.{html,js}"],
  theme: {
    extend: {},
  },
  plugins: [],
}

```

### 3. Adding tailwind directives to your style file

This step will make sure where Tailwind should search for used styles, we need to provide it with components.

```
@tailwind base;
@tailwind components;
@tailwind utilities;
```

### 4. Starting Tailwind

Next step is to start Tailwind you have to specify which file is the stylesheet linked in your files (output) and the path to it, whatever we include in our input.css file will be transferred over to the output.css. <br><br> You can comment this line at the top of your stylesheet so when you come back to the project you can quickly copy-paste it into console instead of trying to figure out what it was.

```
npx tailwindcss -i ./style/input.css -o ./dist/output.css --watch
```

### 5. Basic configuration Done

Feel free to start using it, for documentation on markup check [This link](https://tailwindcss.com/docs/utility-first)

##### If you run into problems, make sure that your file paths are correct.

## Usage

To use Tailwind simply use one of the classes in your markup and Tailwind will insert needed code in your stylesheet. While designing remember that Tailwind is meant for mobile first development style.

### Media queries

You can affect media queries by including a prefix in front of your styling.

```
<img class="w-16 md:w-32 xl:w-48" src="#">
```

With this styling by default the image will have size of 4rem (16/4, as default unit is 0.25rem), but when your screen will reach the first breakpoint (md = 768px) the width will increase to 8rem and so on. <br> for more information on media query usage check [this link](https://tailwindcss.com/docs/responsive-design).

### Components

Tailwind doesn't include components by default, but there is plenty of free sources from which you can find the HTML code. Tailwind will take care of downloading the CSS as soon as you save your HTML file.

### Examples

- [My porftolio assignment](https://relcnob.github.io/portfolio-2022/)
- [My designing with frameworks assignment](https://relcnob.github.io/13C.02.02.designing-with-frameworks/)
