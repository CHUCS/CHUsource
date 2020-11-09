---
title: Parallel Programming MS-MPI install
keywords: Parallel MS-MPI install
date: 2020-11-09 19:14:25
categories: Parallel Programming
tags:
---
# Parallel Programming 平行程式
平行計算是一種類型的計算，許多計算或執行過程是同時進行的。把大問題分為小問題，然後同時解決。以下式建置平行程式環境的流程。

<!-- more -->
## MS-MPI 安裝教學
首先打開[MS-MPI](https://docs.microsoft.com/en-us/message-passing-interface/microsoft-mpi)然後到下載的地方點擊MS-MPI vxx.x.x，如下圖紫色字體。

![](Otdr8uZ.png)

接著將所有檔案打勾然後按下一步就會把檔案下載下來了。

![](a8jSD2x.png)

下載下來後執行並下移步到底，若要更換路徑請自行記得路徑。  
接著打開Visual Studio 開啟一個C++專案。

![](hfmZ9fk.png)

點擊右邊專案右鍵，屬性。

![](eC9A1o6.png)

打開後按`C/C++`->`其他include目錄`，將剛剛按裝好的`MPI/Include`路徑設好。

![](1LVNsYp.png)

![](tXWUuIj.png)

建置完後就會產出一個`.exe`的檔案。

![](1q8F8cx.png)

```c=
#include <mpi.h>
#include <stdio.h>

int main(int argc, char *argv[])
{
	int rank, size;
	MPI_Init(&argc, &argv);

	MPI_Comm_rank(MPI_COMM_WORLD, &rank);
	MPI_Comm_size(MPI_COMM_WORLD, &size);

	printf("Hello, World.  I am %d of %d\n", rank, size);

	MPI_Finalize();
	return 0;
}
```

![](HKDJrkG.png)

將終端機打開`source\repos\MpiTest\Debug`執行面下指令(這個路徑是你的專案路徑，因此可能會有所不同)，你就會看到下圖結果。
```bash=
$ mpiexec -n 4 MpiTest.exe
```
若無此指令請確認環境變數是否有設定完成。  
![](aXnvwD9.png)