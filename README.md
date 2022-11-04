# KrystalZhang-SugarCrush Game App
My replica of one of the world’s most famous games CandyCrush mainly using JavaScript. Same to CandyCrush, this replica allows the player to cancel candies whenever they have accumulated three consecutive same-branded candies in row or column, with a score the player getting simultaneously on-side. 
## ***[Copyright and Commercial Use Disclaimer](https://github.com/KrystalZhang612/KrystalZhang-SugarCrush-Game-App/blob/main/README.md#please-carefully-read-licensemd-about-the-open-source-restrictions-and-the-personal-use-policy-of-this-project-under-gpl-30-license-any-commericial-uses-on-this-project-by-other-than-the-owner-krystalzhang612-or-the-authorized-users-and-organizations-including-unauthorized-modifications-forks-pull-requests-and-other-commercial-related-uses-will-be-subjected-to-copyright-violation-with-sebsequent-legal-concerns)***

⏬

### ***Please carefully read [LICENSE.md](https://github.com/KrystalZhang612/KrystalZhang-SugarCrush-Game-App/blob/main/LICENSE) about the Open Source restrictions and the personal use policy of this project under [GPL-3.0 license](https://www.gnu.org/licenses/gpl-3.0.en.html), any commericial uses on this project by other than the owner [@KrystalZhang612](https://github.com/KrystalZhang612) or the authorized users and organizations, including unauthorized modifications, forks, pull requests, and other commercial-related uses will be subjected to copyright violation with sebsequent legal concerns.***
## SugarCrush Game App Overview:
<p align = "center"> 
  <img src = "https://user-images.githubusercontent.com/72481348/200014636-680d9547-5627-45eb-8fc1-fc6c5cd50a5f.mov" width = "380" height ="472.2" />&nbsp; 
  <img src ="https://user-images.githubusercontent.com/72481348/200014826-afe4c9d4-cd60-4e0b-b416-eccd7cf08653.mov" width = "380" height ="472.2" />
</p>

# Build
[Method to Run & Test the Project Locally](https://github.com/KrystalZhang612/KrystalZhang-SugarCrush-Game-App/blob/main/README.md#method-to-run--test-the-project-locally)<br/> 
[Prerequisites & Setups](https://github.com/KrystalZhang612/KrystalZhang-SugarCrush-Game-App/blob/main/README.md#prerequisites--setup)<br/> 
[Synchronous Developing Notes](https://github.com/KrystalZhang612/KrystalZhang-SugarCrush-Game-App/blob/main/README.md#synchronous-developing-notes)<br/> 
[Testing Result](https://github.com/KrystalZhang612/KrystalZhang-SugarCrush-Game-App/blob/main/README.md#testing-result)

# Contribution
[Author]()

# Functionalities/Demo
- A board that randomly generates candies all over the board.
- Allows players to switch out colors of different candies on board.
- Check for 3+ consecutive matches, which are the valid matches to cancel off. 
- All the candies get moved down if the player gets a match.

# Compatiability 

| Browsers       | Supported          |
| -------        | ------------------ |
| Google Chrome  | :white_check_mark: |
| Microsoft Edge | :white_check_mark: |
| FireFox        | :white_check_mark: |
| Apple Safari   | :white_check_mark: |
| Opera          | :white_check_mark: |
| DuckDuckGo     | :white_check_mark: |

# Method to Run & Test the Project Locally

### Download the entirep project of SugarCrush Game App to the local directory.
### Open the project with Vscode on local device.
### Install Vscode Extension [`Live Server Vscode Extension v5.7.9`](https://www.vsixhub.com/vsix/1950/)
### Open [index.html](https://github.com/KrystalZhang612/KrystalZhang-SugarCrush-Game-App/blob/main/index.html) in Vscode.
### Click `Go Live` on the bottom bar to play the fan and exciting SugarCrush Game! 

# Prerequisites & Setup
Create [index.html](https://github.com/KrystalZhang612/KrystalZhang-SugarCrush-Game-App/blob/main/index.html), [app.js](https://github.com/KrystalZhang612/KrystalZhang-SugarCrush-Game-App/blob/main/app.js) and [style.css](https://github.com/KrystalZhang612/KrystalZhang-SugarCrush-Game-App/blob/main/style.css) files in local directory to start off.

# 🛠️ Developing Languages, Tools, and Techniques Needed
[Vscode 1.73](https://code.visualstudio.com/updates/v1_73)<br/> 
[JavaScript](https://www.javascript.com/)<br/> 
[Live Server Vscode Extension v5.7.9](https://www.vsixhub.com/vsix/1950/)<br/>
[CSS3](https://en.wikipedia.org/wiki/CSS)<br/> 
[HTML5](https://en.wikipedia.org/wiki/HTML5)<br/> 
<div>
  <img src ="https://github.com/devicons/devicon/blob/master/icons/visualstudio/visualstudio-plain.svg" title ="Vscode" alt = "Vscode" width ="60" height ="60" />&nbsp; 
  <img src ="https://github.com/devicons/devicon/blob/master/icons/javascript/javascript-original.svg" title ="JavaScript" alt ="JavaScript" width ="60" height ="60"/>&nbsp; 
  <img src ="https://github.com/devicons/devicon/blob/master/icons/html5/html5-original.svg" title ="HTML5" alt ="HTML5"  width ="60" height ="60"/>&nbsp;
  <img src ="https://github.com/devicons/devicon/blob/master/icons/css3/css3-original.svg" title ="CSS3" alt ="CSS3"  width ="60" height ="60"/>  
</div>

# Synchronous Developing Notes
## ***Create board:***
Create a board of grids in app.js and call them:
```JavaScript 
function createBoard() {
        for (let i = 0; i < width * width; i++) {
            const square = document.createElement('div')
            grid.appendChild(square)
            squares.push(square)
} }
    createBoard()
})
```
Make the board randomly generate different candy colors:
```JavaScript 
  let randomColor = Math.floor(Math.random() * candyColors.length)
  square.style.backgroundColor = candyColors[randomColor]
```
So now we have:<br/> 
[board of randomly generated candy colors.PNG](https://github.com/KrystalZhang612/KrystalZhang-SugarCrush-Game-App/blob/main/board%20with%20randomly%20generated%20candy%20colors.png)<br/> 
To make the candy colors grid draggable:
```JavaScript 
square.setAttribute('draggable', true)
```
Now candies colors are draggable:<br/> 
[draggable candy colors.MOV](https://github.com/KrystalZhang612/KrystalZhang-SugarCrush-Game-App/blob/main/draggable%20candy%20colors.mov)<br/> 
## ***Drag the candies:***
Start to drag:
```JavaScript 
  function dragStart() {
     colorBeingDragged = this.style.backgroundColor     
squareIdBeingDragged = parseInt(this.id)
        console.log(colorBeingDragged)
        console.log(this.id, 'dragstart')
}
```
The dragged candies dropped:
```JavaScript 
 function dragDrop() {
        console.log(this.id, 'dragdrop')
        colorBeingReplaced = this.style.backgroundColor
        squareIdBeingReplaced = parseInt(this.id)
        this.style.backgroundColor = colorBeingDragged
        squares[squareIdBeingDragged].style.backgroundColor =
colorBeingReplaced
    }
```
Define valid moves:
```JavaScript 
 if (squareIdBeingReplaced && validMove) {
    squareIdBeingReplaced = null
        } else if (squareIdBeingReplaced && !validMove) {
    squares[squareIdBeingReplaced].style.backgroundColor =
colorBeingReplaced
    squares[squareIdBeingDragged].style.backgroundColor =
colorBeingDragged
        } else squares[squareIdBeingDragged].style.backgroundColor =
colorBeingDragged
```
## ***First check for row of consecutive 3:***
If row of 3 is matched, player’s score + 3:
```JavaScript 
 function checkRowForThree() {
        for (i = 0; i < 61; i++) {
            let rowOfThree = [i, i + 1, i + 2]
            let decidedColor = squares[i].style.backgroundColor
            const isBlank = squares[i].style.backgroundColor === ''
        if (rowOfThree.every(index =>
squares[index].style.backgroundColor === decidedColor && !isBlank)) {
                score += 3
                rowOfThree.forEach(index => {
                    squares[index].style.backgroundColor = ''
                })
        squares[index].style.backgroundColor = ''
                })
    checkRowForThree()
```














# Testing Result 
[board of randomly generated candy colors.PNG](https://github.com/KrystalZhang612/KrystalZhang-SugarCrush-Game-App/blob/main/board%20with%20randomly%20generated%20candy%20colors.png)<br/> 
[draggable candy colors.MOV](https://github.com/KrystalZhang612/KrystalZhang-SugarCrush-Game-App/blob/main/draggable%20candy%20colors.mov)<br/> 
  
  
  
  
  
  
  




