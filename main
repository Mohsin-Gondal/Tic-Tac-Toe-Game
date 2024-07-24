#include <iostream>
#include <iomanip>
using namespace std;
void Print_Board_n_Head(char Array2D[3][3]);
bool Search_Update(char Array2D[3][3], int TheTerm, char CharEntry);
bool All_Conditions(char BoardLoc[3][3], bool has_won, int loopcounter, string Playerone, string Playertwo);
bool Check_Dual_Entry(char Array2D[3][3], int index);
int main()
{
    char BoardLoc[3][3] = {
        {'1', '2', '3'}, {'4', '5', '6'}, {'7', '8', '9'}};
    Print_Board_n_Head(BoardLoc);
    // Board Printed Once//
    cout << " Both Users Enter Their First Names " << endl;
    string Playerone;
    string Playertwo;
    cout << " First Player: ";
    cin >> Playerone;
    cout << " Second Player: ";
    cin >> Playertwo;
    cout << " Okkaay!!! Start Now...\n";
    // Taking Names Completed//
    bool has_won = true;
    int loopcounter = 1;
    int Entry;
    while (has_won)
    {
    AgainEntry:
        if (loopcounter % 2 == 1)
        {
            cout << Playerone << "'s Turn: ";
            cin >> Entry;
        }
        else
        {
            cout << Playertwo << "'s Turn: ";
            cin >> Entry;
        }
        // Entry Taking Complete//
        int EntryToIndex = Entry - 1;
        int EntryToASCII = Entry + 48;
        char EntryToChar = EntryToASCII;
        //		index targeting machine bnai ha,, ASCII value nikaali ha,,int Entry ko Char Entry Bnaya ha....//
        if (Entry > 0 && Entry < 10)
        {
            //		Check_Dual_Entry(BoardLoc,EntryToIndex);
            if (Check_Dual_Entry(BoardLoc, EntryToIndex) == true)
            {
                cout << " This Move has Already been Played " << endl;
                goto Invalid_Move;
            }
            cout << " Valid Move!!" << endl;
            Search_Update(BoardLoc, loopcounter, EntryToChar);
            //			cout<<" Entry was "<<Entry<<" Ascii is "<<EntryToASCII<<" Char is "<<EntryToChar<<" Index is "<<EntryToIndex<<endl;
        }
        else
        {
            cout << " Invalid Move!!" << endl;
        Invalid_Move:
            goto AgainEntry;
        }
        // checking of entry wether it's valid or not is complete//
        system("cls");
        Print_Board_n_Head(BoardLoc);
        // printed board again//
        has_won = All_Conditions(BoardLoc, has_won, loopcounter, Playerone, Playertwo);

        loopcounter++;
    }
    return 0;
}

void Print_Board_n_Head(char Array2D[3][3])
{
    cout << "=======//Tic Tac Toe Game//======\n\n"
         << endl;
    for (int i = 0; i < 3; i++)
    {
        cout << setw(12);
        for (int j = 0; j < 3; j++)
        {
            cout << " " << Array2D[i][j];
            if (j == 2)
            {
                cout << " ";
                continue;
            }
            cout << " |";
        }
        cout << endl;
        if (i == 2)
            continue;
        cout << setw(22) << "-----------";
        cout << endl;
    }
    cout << "\n\n";
}

bool Search_Update(char Array2D[3][3], int TheTerm, char CharEntry)
{
    for (int i = 0; i < 3; i++)
    {
        for (int j = 0; j < 3; j++)
        {
            if (Array2D[i][j] == CharEntry)
            {
                if (TheTerm % 2 == 1)
                    Array2D[i][j] = 'X';
                else
                    Array2D[i][j] = 'O';
            }
        }
    }
}
// loop preset
// for(int i = 0 ; i < 3 ; i++){
//		for(int j = 0 ; j < 3 ; j++){
//		}
//	}
bool All_Conditions(char BoardLoc[3][3], bool has_won, int loopcounter, string Playerone, string Playertwo)
{
    //	    	00		01		02
    //			{'1'  ,  '2'  ,  '3'}
    //			10		11		12
    //			{'4'  ,  '5'  ,  '6'}
    //			20		21		22
    //			{'7'  ,  '8'  ,  '9'}
    if (BoardLoc[0][0] == BoardLoc[0][1] && BoardLoc[0][0] == BoardLoc[0][2])
    {
        if (loopcounter % 2 == 0)
        {
            cout << Playertwo << " Has Won The Game " << endl;
        }
        else
        {
            cout << Playerone << " Has Won The Game " << endl;
        }
        has_won = false;
    }
    else if (BoardLoc[1][0] == BoardLoc[1][1] && BoardLoc[1][0] == BoardLoc[1][2])
    {
        if (loopcounter % 2 == 0)
        {
            cout << Playertwo << " Has Won The Game " << endl;
        }
        else
        {
            cout << Playerone << " Has Won The Game " << endl;
        }
        has_won = false;
    }
    else if (BoardLoc[2][0] == BoardLoc[2][1] && BoardLoc[2][0] == BoardLoc[2][2])
    {
        if (loopcounter % 2 == 0)
        {
            cout << Playertwo << " Has Won The Game " << endl;
        }
        else
        {
            cout << Playerone << " Has Won The Game " << endl;
        }
        has_won = false;
    }
    else if (BoardLoc[0][0] == BoardLoc[1][0] && BoardLoc[0][0] == BoardLoc[2][0])
    {
        if (loopcounter % 2 == 0)
        {
            cout << Playertwo << " Has Won The Game " << endl;
        }
        else
        {
            cout << Playerone << " Has Won The Game " << endl;
        }
        has_won = false;
    }
    else if (BoardLoc[0][1] == BoardLoc[1][1] && BoardLoc[0][1] == BoardLoc[2][1])
    {
        if (loopcounter % 2 == 0)
        {
            cout << Playertwo << " Has Won The Game " << endl;
        }
        else
        {
            cout << Playerone << " Has Won The Game " << endl;
        }
        has_won = false;
    }
    else if (BoardLoc[0][2] == BoardLoc[1][2] && BoardLoc[0][2] == BoardLoc[2][2])
    {
        if (loopcounter % 2 == 0)
        {
            cout << Playertwo << " Has Won The Game " << endl;
        }
        else
        {
            cout << Playerone << " Has Won The Game " << endl;
        }
        has_won = false;
    }
    else if (BoardLoc[0][0] == BoardLoc[1][1] && BoardLoc[0][0] == BoardLoc[2][2])
    {
        if (loopcounter % 2 == 0)
        {
            cout << Playertwo << " Has Won The Game " << endl;
        }
        else
        {
            cout << Playerone << " Has Won The Game " << endl;
        }
        has_won = false;
    }
    else if (BoardLoc[0][2] == BoardLoc[1][1] && BoardLoc[0][2] == BoardLoc[2][0])
    {
        if (loopcounter % 2 == 0)
        {
            cout << Playertwo << " Has Won The Game " << endl;
        }
        else
        {
            cout << Playerone << " Has Won The Game " << endl;
        }
        has_won = false;
    }
    else
    {
        if (loopcounter == 9)
        {
            cout << " Match Has Been Drawn" << endl;
            has_won = false;
        }
    }
    return has_won;
}
//	    	00		01		02
//			{'1'  ,  '2'  ,  '3'}
//			10		11		12
//			{'4'  ,  '5'  ,  '6'}
//			20		21		22
//			{'7'  ,  '8'  ,  '9'}
bool Check_Dual_Entry(char Array2D[3][3], int index)
{
    int A_size_1 = 0;
    int A_size_2 = 0;
    bool flag = false;

    if (index == 0)
    {
        A_size_1 = 0;
        A_size_2 = 0;
    }
    else if (index == 1)
    {
        A_size_1 = 0;
        A_size_2 = 1;
    }
    else if (index == 2)
    {
        A_size_1 = 0;
        A_size_2 = 2;
    }
    else if (index == 3)
    {
        A_size_1 = 1;
        A_size_2 = 0;
    }
    else if (index == 4)
    {
        A_size_1 = 1;
        A_size_2 = 1;
    }
    else if (index == 5)
    {
        A_size_1 = 1;
        A_size_2 = 2;
    }
    else if (index == 6)
    {
        A_size_1 = 2;
        A_size_2 = 0;
    }
    else if (index == 7)
    {
        A_size_1 = 2;
        A_size_2 = 1;
    }
    else if (index == 8)
    {
        A_size_1 = 2;
        A_size_2 = 2;
    }
    else
    {
        cout << "No Index Found For 2D Array " << endl;
    }
    //	cout<<" The Value stored in this place is "<<Array2D[A_size_1][A_size_2]<<" "<<endl;
    if (Array2D[A_size_1][A_size_2] == 'X' || Array2D[A_size_1][A_size_2] == 'O')
    {
        flag = true;
    }
    return flag;
}
