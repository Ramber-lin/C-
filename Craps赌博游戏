#include<stdlib.h>
#include<stdio.h>
#include<time.h>
int main()
{
	int i, first, second, j, k, money = 1000;
	char jixu;
	printf(" Craps赌博游戏\n\n玩家摇两颗色子,如果第一次摇出7点或11点 玩家胜;\n如果摇出2点 3点 12点, 庄家胜;\n其他情况游戏继续。玩家再次摇色子 如果摇出7点 庄家胜；\n如果摇出的点数与第一次摇的点数相同，则玩家胜；否则游戏继续；\n玩家继续摇色子玩家进入游戏时有1000元的赌注 全部输光游戏结束\n");
	printf("\n");
	srand((unsigned)time(NULL));
	while (money >= 0)
	{
		printf("你的总资产为：%d\n", money);
		if (money > 0)
		{
			jixu = 1;
			while (jixu == 1)
			{
				printf("请下注：");
				scanf_s("%d", &i);
				if (i > money)
				{
					printf("你没有这么多钱!");
				}
				else
					break;
			}
			j = 1 + (int)(6 * rand() / (RAND_MAX + 1));
			k = 1 + (int)(6 * rand() / (RAND_MAX + 1));
			first = j + k;
			printf("玩家摇出了%d点\n", first);
			if (first == 7 || first == 11)
			{
				printf("玩家胜！\n");
				money = money + i;
			}
			else if (first == 2 || first == 3 || first == 12)
			{
				printf("庄家胜！\n");
				money = money - i;
			}
			else
			{
				j = 1 + (int)(6 * rand() / (RAND_MAX + 1));
				k = 1 + (int)(6 * rand() / (RAND_MAX + 1));
				second = j + k;
				printf("玩家摇出了 % d点\n", second);
				if (second == 7)
				{
					printf("庄家胜！\n");
					money = money - i;
				}
				else if (second == first)
				{
					printf("玩家胜！\n");
					money = money + i;
				}
			}
		}
		else
		{
			jixu = 0;
			break;
		}
	}
	printf("你破产了！游戏结束！");
	return 0;
}
