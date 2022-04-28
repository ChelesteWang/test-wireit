# test-wireit

test-wireit 

- 并行的根据依赖运行脚本
- 适用于大型 monorepo 的构建使用
- 支持增量构建
- 支持本地以及远程缓存

wireit 可以根据依赖关系图，并行安全的运行脚本。

如官方 README 中的案例，B 和 C 脚本将并行执行，而 A 脚本直到 B 和 C 全部执行后执行。

<img width="241" alt="image" src="https://user-images.githubusercontent.com/40495740/165771773-6cf33a5d-0afc-4c59-9327-406a9c35ef7c.png">

默认情况下，对于系统上检测到的每个CPU核心，WireIt最多将并行运行4个脚本。要更改此默认值，请将WireIt_Parallel Environall Varible设置为正整数，或无限运行。如果您在大型建筑中遇到资源饥饿，则可能需要降低此数字。例如，一次仅运行一个脚本：
