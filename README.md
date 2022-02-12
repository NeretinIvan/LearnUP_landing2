# LearnUP Landing 2

## Description

This site was developed in educational purposes.

[Link to the site](https://amazing-joliot-e15ecf.netlify.app/)

## Using technologies

Using languages: **html, css**
Using css preprocessor **Sass** [sass-lang.com](https://sass-lang.com/)

## How to contribute

To make changes in html you just need to clone repository, open file and change file, no other actions is necessary
To make changes in .sass files you need to compile **style.scss** first. 

### Compile .scss in Windows Power Shell:
There is security problem if you try to compile .scss file through Power Shell in Windows, which not allows to compile files.
To solve this problem, you may do next.

**In VS Code:**
1. Go File -> Preferences -> Settings -> Terminal -> Integrated -> Automation profile -> Windows
2. Click "Edit in settings.json"
3. Add following lines of code:
  ```json
  "terminal.integrated.profiles.windows": {
        "my-pwsh": {
          "source": "PowerShell",
          "args": ["-ExecutionPolicy", "Bypass"]
        }
      }
  ```
This finally may look like this:
  ```json
  {
    "terminal.integrated.profiles.windows": {
        "my-pwsh": {
          "source": "PowerShell",
          "args": ["-ExecutionPolicy", "Bypass"]
        }
      },
    "terminal.integrated.defaultProfile.windows": "PowerShell"
  }
  ```
  You may replace "my-pwsh" to any name you want.
  This will add new custom terminal which will allow you to compile scss files and bypass power shell protection. To do this, you need to choose "my-pwsh" as terminal which you will use and write needed commands.
  
  ![image](https://user-images.githubusercontent.com/88938784/153714558-f7161181-1c38-4bb3-9764-21cac834cc33.png)

  However, this is not the only way and you may use any other method if you want.
  4. Write "sass style/scss/style.scss style.css" in terminal to compile style files. You may write "sass --watch style/scss/style.scss style.css" if you want it to compile style.scss file every time you save it.
