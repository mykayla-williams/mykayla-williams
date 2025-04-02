//
// Created by Mykayla Williams on 4/1/25.
//

#ifndef GENERATOR_H
#define GENERATOR_H

#endif //GENERATOR_H

//**@file generator.h
/**
* @file generator.h
* @brief Function prototypes for generating random solvable Sudoku boards.
*
* This header defines functions to:
* - Create empty Sudoku boards.
* - Fill independent diagonal boxes.
* - Solve and generate a complete Sudoku board.
* - Randomly delete cells to create a solvable puzzle.
* - Generate a complete Sudoku puzzle with a specific number of empty cells.
*
* Detailed function descriptions and parameters are provided below.
*
* @author
* Keshav Bhandari
*
* @date
* February 7, 2025
*/

#ifndef GENERATOR_H
#define GENERATOR_H

#include <vector>



/**
 * TODO: Provide appropriate Documentation, see other examples provided within the projects
 */
int** getEmptyBoard() {
  int** board = new int*[9];
  for (int i = 0; i<9; i++)
    {
      board[i] = new int[9] {0, 0, 0, 0, 0, 0, 0, 0, 0};
    }
  return board;
}

/**
  * TODO: Provide appropriate Documentation, see other examples provided within the projects
  */
 vector<int> getShuffledVector();
 vector<int> vect = {1,2,3,4,5,6,7,8,9};
shuffle(vect.begin(), vect.end(), dafault_random_engine(time(0)));
return vect;

/**
  * TODO: Provide appropriate Documentation, see other examples provided within the projects
  */
void fillBoardWithIndependentBox(int** BOARD) {
  int staticBoard[9][9] = {
    {1, 5, 6, 0, 0, 0, 0, 0, 0},
    {2, 4, 7, 0, 0, 0, 0, 0, 0},
    {8, 3, 9, 0, 0, 0, 0, 0, 0},
    {0, 0, 0, 1, 7, 4, 0, 0, 0},
    {0, 0, 0, 6, 2, 8, 0, 0, 0},
    {0, 0, 0, 5, 9, 3, 0, 0, 0},
    {0, 0, 0, 0, 0, 0, 1, 6, 7},
    {0, 0, 0, 0, 0, 0, 2, 5, 8},
    {0, 0, 0, 0, 0, 0, 3, 4, 9}
  };

  for (int i = 0; i < 9; i++) {
    for (int j = 0; j < 9; j++) {
      BOARD[i][j] = staticBoard[i][j];
    }
  }
}
}

/**
  * TODO: Provide appropriate Documentation, see other examples provided within the projects
  */
void deleteRandomItems(int** BOARD, const int& n);
  if (BOARD == nullptr || n < 1 || n > 81) {
  cout << "Invalid input parameters." << endl;
   return;

 }

vector<int>availableCells;
  for (int i = 0; i < 81; i++)
{
  availableCells.push_back(i);
}

shuffle(availableCells.begin(), availableCells.end(), gen);
  for (int i = 0; i< n; i++)
{
  int index

/**
  * TODO: Provide appropriate Documentation, see other examples provided within the projects
  */
int** generateBoard(const int& empty_boxes);

#endif // GENERATOR_H
