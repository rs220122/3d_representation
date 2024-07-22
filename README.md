# 3d_representation
3次元表現　の記事アーカイブ

## オイラー角について
$\alpha$: roll (x軸周りの $\alpha$ 回転)  
$\beta$: pitch (y軸周りに $\beta$ 回転する)  
$\gamma$: yaw  (z軸周りに $\gamma$ 回転する)

オイラー角による、回転関数を $R(\alpha, \beta, \gamma)$ とする。

### ジンバルロック
[参考](https://qiita.com/Arihi/items/4b306feb3d9e6cd93204)  
ある角度において、自由度が２になってしまう現象である。  
たとえば、pitchを90度にした後に、roll, yawは、同じ方向での回転になってしまう。  
これは、数式的には、微小回転によって、作用する向きが同じ値になることを表す。  
→つまり、勾配が一致してしまうことを表す。  

これらそれぞれの勾配の2つが一致してしまう現象である。  
```math
\frac{\partial R}{\partial \alpha}, \frac{\partial R}{\partial \beta}, \frac{\partial R}{\partial \gamma}
```
