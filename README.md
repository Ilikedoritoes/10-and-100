#define _CRT_SECURE_NO_WARNINGS
#include <stdlib.h>
#include <stdio.h>
#define row 10
#define colume 10

int main()
{
	int i, x, y, temp = 0;
	int num = 0;
	int array[10] = { 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 };
	int mtrx[row][colume] = { {1,2,3,4,5,6,7,8,9,10},
							{0,0,0,0,0,0,0,0,0,0},
							{1,2,3,4,5,6,7,8,9,10},
							{0,0,0,0,0,0,0,0,0,0},
							{0,0,0,0,0,0,0,0,0,0},
							{1,2,3,4,5,6,7,10,9,8},
							{0,0,0,0,0,0,0,0,0,0},
							{0,0,0,0,0,0,0,0,0,0},
							{0,0,0,0,0,0,0,0,0,0},
							{0,0,0,0,0,0,0,0,0,0} };

	/*for (i = 0;i < 10;i++)
	{
		scanf("%d", array[i]);
	}

	for (x = 0;x < row;x++)
	{
		for (y = 0;y < colume;y++)
		{
			scanf("%d", mtrx[x][y]);
		}
	}*/

	for (x = 0;x < row;x++)
	{
		temp = 0;
		for (y = 0;y < colume;y++)
		{
			//for (i = 0;i < 10;i++)
			//{
				if (mtrx[x][y] == array[y])
				{
					//printf("the numbers are the same %d\n", temp);
					temp = temp + 1;
				}

				if (temp == 9)
				{
					printf("line is the same in the %d line\n", x);
					temp = 0;
				}
			//}
		}
	}
}
