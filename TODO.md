## TODO list:

 - [x] 内核
   - [x] 棋盘接口
   - [x] Player接口
   - [x] UI接口
 - [x] 棋盘
 - [x] 样例Player AI算法
 - [x] 样例Player人工智障算法
 - [ ] 棋盘UI
   - [x] 直播平台
   - [ ] 方块移动Animation
 - [x] 与用户Web提交平台的对接
   - [x] 代码提交
   - [x] 复盘展示
 
 - [ ] 文档
   - [x] 具体规则文档
   - [x] Player接口文档
   - [ ] Web提交平台文档

## Architecture:
```
+-------------------------------------------------+
|                                                 |
|   +---------+   +---------+                     |
|   | Player1 |   | Player2 |                     |
|   +----+----+   +----+----+                     |
|        |             |                          |          +---------------+
|   +----+-------------+----+                     | Firewall |               |
|   |                       |         +-------+   +----------+ Web Platform  |
|   |          Core         <---------+ Board |   |          |               |
|   |                       |         +-------+   |          +---------------+
|   +----+------------+-----+                     |
|        |            |                           |
|        |            |                           |
+-------------------------------------------------+
         |            |
         |            |
    +----+-----+ +----+-----+                                +---------------+
    |          | |          |                                |               |
    | Database | | Local UI |                                | Documentation |
    |          | |          |                                |               |
    +----------+ +----------+                                +---------------+


```
