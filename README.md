# Tic-Tac-Toe-Game....-
#include <iostream>
using namespace std;

// Function to display the game board
void displayBoard(char board[3][3])
{
    cout << "\n";
    cout << "     |     |     \n";
    cout << "  " << board[0][0] << "  |  "
         << board[0][1] << "  |  " << board[0][2] << "\n";
    cout << "_____|_____|_____\n";

    cout << "     |     |     \n";
    cout << "  " << board[1][0] << "  |  "
         << board[1][1] << "  |  " << board[1][2] << "\n";
    cout << "_____|_____|_____\n";

    cout << "     |     |     \n";
    cout << "  " << board[2][0] << "  |  "
         << board[2][1] << "  |  " << board[2][2] << "\n";
    cout << "     |     |     \n";
}

// Function to check whether a player has won
bool checkWin(char board[3][3], char player)
{
    // Check rows
    for (int i = 0; i < 3; i++)
    {
        if (board[i][0] == player &&
            board[i][1] == player &&
            board[i][2] == player)
        {
            return true;
        }
    }

    // Check columns
    for (int j = 0; j < 3; j++)
    {
        if (board[0][j] == player &&
            board[1][j] == player &&
            board[2][j] == player)
        {
            return true;
        }
    }

    // Check main diagonal
    if (board[0][0] == player &&