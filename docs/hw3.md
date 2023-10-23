# Coursework (3)

第三次作业的第三题大家可能存在困难，注意分别取 inf 是可能比一起取 inf 更小的，也就是 inf f(x_1,y) + inf f(x_2,y) <= inf [ f(x_1,y)+f(x_2,y) ]
回顾实数情况下的 inf f(x)，如果 inf f(x) ≠ -∞，那么可以取到一个 non-decreasing 的序列 x_n，使得 \lim_{n\to ∞} f(x_n) = inf f(x)。可以参考一下。
实在做不出来的同学，可以处理为存在 x_0 使得 f(x_0) = inf f(x)，这也比伪证和错证好一些。
