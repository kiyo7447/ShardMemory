﻿
# Interprocess Communication（IPC）には複数の手法があります。以下はそのいくつかの例です：
1. Interprocess Communication (IPC)を実装する一般的な方法のひとつは、名前付きパイプを使用することです。

1. 共有メモリ（Shared Memory）: 2つ以上のプロセスが同じメモリ領域を読み書きすることでデータを交換します。

1. ソケット（Sockets）: ソケットを使用して、ネットワーク越しにもプロセス間通信ができます。ローカルホスト内で使えば、高度なIPCの一形態となります。

1. メッセージキュー（Message Queues）: プロセスがメッセージキューにデータを送り、別のプロセスがそのキューからデータを読み取る形式です。

1. 信号（Signals）: シグナルを用いてプロセスに何らかのイベントが発生したことを通知します。ただし、データの受け渡しには向いていません。

1. セマフォ（Semaphores）: マルチプロセスの同期を取るために使用されます。

1. ファイル: 単純ですが、ファイルシステムを介してデータを交換する方法もあります。

1. D-Bus: LinuxやUnix系OSでよく使われる、メッセージバスシステムを提供するIPCの一種です。

1. COM（Component Object Model）: Windows環境でよく用いられるプロセス間通信手法の一つです。

1. RPC（Remote Procedure Call）: プロセスが別のアドレス空間（同じマシン内でも可）に存在する関数を呼び出す手法です。

1. Web API: HTTPやgRPCなどのプロトコルを使用して、異なるプロセスやマシン間で通信する現代的な手法もあります。
# 実装パターン
1. [Memory-Mapped Files（メモリマップトファイル）](./Memory-MappedFiles)  
メモリマップトファイル（共有メモリ）を作成して・アクセスできます。
1. [Named Pipes（名前付きパイプ）](./NamedPipes)  
名前付きパイプを介したデータ共有ができます。これはプロセス間で小量のデータを効率的に共有するのに使えます。
1. 