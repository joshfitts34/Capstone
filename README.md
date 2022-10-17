# Capstone: AI Sudoku Solver

## Goal

Create an application that utilizes image processing to create a model that is able to accurately and efficiently find and read in a sudoku board from a picture and then display the solution of the board back to the original image.

---

## Background

### What is Sudoku?

Sudoku is a logic-based, combinatorial number-placement puzzle that aims at challenging the player analytically and logically. The main objective of the game is to fill a 9 x 9 grid with various digits, some of which are already filled in depending on difficulty, so that each column, row, and each of the 3 x 3 subgrids that compose the grid all contain the digits from 1 to 9 once.



### Basic Rules

- Sudoku grid consists of 9x9 spaces.
- You can use only numbers from 1 to 9.
- Each 3×3 block can only contain numbers from 1 to 9.
- Each vertical column can only contain numbers from 1 to 9.
- Each horizontal row can only contain numbers from 1 to 9.
- Each number in the 3×3 block, vertical column or horizontal row can be used only once.
- The game is over when the whole Sudoku grid is correctly filled with numbers.

Rules from [Sudoku.com](https://sudoku.com/sudoku-rules/)

---

## Process

1. Creating the CNN model to use to detect and predict the digits in each of the boxes on the board.
2. Using backtracking, creating a solution to the board game itself, given we have a board in the shape of a 9 x 9 matrix.
3. Defining some functions to use along with OpenCV to do some image preprocessing like contouring and finding the board in an image and splitting the image up into 81 smaller boxes to run the model on.
4. Lastly, using OpenCV to read, process, and then display the solution back to the original image filling in the missing boxes.

![image](image_ans.png)

---

## Next Steps

- Some of the images used weren't as easy to detect the digits as others for some reason. Actual pictures taken rather than images for the internet worked a little better as long as the sudoku board was the majority of the image.
- Had some trouble with certain fonts used on the web images with 5's looking like 6 and things of that nature. Try to refine model a little more and maybe train on web text rather than written text.
- Main next step that I wasn't able to complete would be the app. I had to use colab for this project, as a temporary solution, and running streamlit from Colab had a few dependencies and nuances that I couldn't get working from Colab reliably. 
