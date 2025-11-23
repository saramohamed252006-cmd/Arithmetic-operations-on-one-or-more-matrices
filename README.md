// Arithmetic-operations-on-one-or-more-matrices
#include <iostream>
#include <vector>
using namespace std;

int main()
{
   int NumberOfRows , NumberOfColumns;
   cout << "Enter the matrix must be bigger than 2*2 " << endl;
   cout << "The processs you want with one or two matrices ?"<<endl<<"Answer with 1 or 2";
   int answer;
   cin >>answer;
   if (answer == 1){
    cout << "Enter number of rows";
    cin >> NumberOfRows;
    cout <<"Enter number of columns";
    cin >> NumberOfColumns;
    if ( NumberOfRows <2 || NumberOfColumns <2 || ( NumberOfRows ==2 && NumberOfColumns ==2 )){
        cout <<"Matrix must be bigger than 2*2"<<endl;}

       vector<vector<int> > matrix(NumberOfRows, vector<int>(NumberOfColumns));
            cout << "Enter the elements of the matrix:" << endl;
            for (int i = 0; i < NumberOfRows; i++) {
                for (int j = 0; j < NumberOfColumns; j++) {
                    cout << "Element [" << i + 1 << "][" << j + 1 << "]: ";
                    cin >> matrix[i][j];
                }
            }
            cout << "Your matrix is: " << endl;
            for (int i = 0; i < NumberOfRows; i++) {
                for (int j = 0; j < NumberOfColumns; j++) {
                    cout << matrix[i][j] << " ";
                }
                cout << endl;
            }
        string operation;
        cout <<"what operation do you want to perform on the matrix ?"<<endl;
        cout << "which do you need transpose or inverse ?";
        cin >>operation;
        if (operation == "transpose"){
        int transpose;
            vector<vector<int> > transpose(NumberOfColumns, vector<int>(NumberOfRows));

for (int i = 0; i < NumberOfRows; i++) {
    for (int j = 0; j < NumberOfColumns; j++) {
        transpose[j][i] = matrix[i][j];
    }
}

cout << "The transposed matrix is:" << endl;
for (int i = 0; i < NumberOfColumns; i++) {
    for (int j = 0; j < NumberOfRows; j++) {
        cout << transpose[i][j] << " ";
    }
    cout << endl;
}
}  else (operation == "inverse"){
       int inverse
          }


   }
           else
            {int NumberOfRowsMatrix1 , NumberOfColumnsMatrix1;
            int NumberOfRowsMatrix2 , NumberOfColumnsMatrix2;
                cout << "Enter the number of rows in the Matrix_1 "<<" ";
    cin >> NumberOfRowsMatrix1;
    cout <<"Enter the number of columns in the Matrix_1"<<" ";
    cin >> NumberOfColumnsMatrix1;

    if ( NumberOfRowsMatrix1 <2 || NumberOfColumnsMatrix1 <2 || ( NumberOfRowsMatrix1 ==2 && NumberOfColumnsMatrix1 ==2 )){
       cout <<"Matrix must be bigger than 2*2";}

vector<vector<int> > matrix1(NumberOfRowsMatrix1, vector<int>(NumberOfColumnsMatrix1));
    cout << "Enter the elements of Matrix_1:" << endl;
    for (int i = 0; i < NumberOfRowsMatrix1; i++) {
        for (int j = 0; j < NumberOfColumnsMatrix1; j++) {
            cout << "Matrix_1 [" << i + 1 << "][" << j + 1 << "]: ";
            cin >> matrix1[i][j];
        }
    }

    cout << "Matrix_1 is:" << endl;
    for (int i = 0; i < NumberOfRowsMatrix1; i++) {
        for (int j = 0; j < NumberOfColumnsMatrix1; j++) {
            cout << matrix1[i][j] << " ";
        }
        cout << endl;
    }

    cout <<"Enter the number of rows in the Matrix_2"<<" ";
       cin >> NumberOfRowsMatrix2;
      cout <<"Enter the number of columns in the Matrix_2"<<" ";
      cin >> NumberOfColumnsMatrix2;
      if ( NumberOfRowsMatrix2 <2 || NumberOfColumnsMatrix2 <2 || ( NumberOfRowsMatrix2 ==2 && NumberOfColumnsMatrix2 ==2 )){
        cout <<"Matrix must be bigger than 2*2"<<endl;}
         vector<vector<int> > matrix2(NumberOfRowsMatrix2, vector<int>(NumberOfColumnsMatrix2));
    cout << "Enter the elements of Matrix_2:" << endl;
    for (int i = 0; i < NumberOfRowsMatrix2; i++) {
        for (int j = 0; j < NumberOfColumnsMatrix2; j++) {
            cout << "Matrix_2 [" << i + 1 << "][" << j + 1 << "]: ";
            cin >> matrix2[i][j];
        }
    }

    cout << "Matrix_2 is:" << endl;
    for (int i = 0; i < NumberOfRowsMatrix2; i++) {
        for (int j = 0; j < NumberOfColumnsMatrix2; j++) {
            cout << matrix2[i][j] << " ";
        }
        cout << endl;
    }
     string operation;
        cout <<"what operation do you want to perform on the matrix ?"<<endl;
        cout << "which do you need sum or minus or multiplication ?";
        cin >>operation;
 if (operation == "sum") {
            if (NumberOfRowsMatrix1 == NumberOfRowsMatrix2 && NumberOfColumnsMatrix1 == NumberOfColumnsMatrix2) {
                vector<vector<int> > sumMatrix(NumberOfRowsMatrix1, vector<int>(NumberOfColumnsMatrix1));
                for (int i = 0; i < NumberOfRowsMatrix1; i++)
                    for (int j = 0; j < NumberOfColumnsMatrix1; j++)
                        sumMatrix[i][j] = matrix1[i][j] + matrix2[i][j];

                cout << "Result of addition";
                for (int i = 0; i < NumberOfRowsMatrix1; i++) {
                    for (int j = 0; j < NumberOfColumnsMatrix1; j++)
                        cout << sumMatrix[i][j] << " ";
                    cout << endl;
                }
            } else {
                cout << "Error: matrices must have the same dimensions to be added";
            }
        }

    }

    return 0;
}
       }
    }



    return 0;

}
