---
title:  "Vector and Space"
categories: [Linear Algebra]
tags: [Linear Algebra, 선형대수]
---

## Chapter 1 벡터 - 공학에서의 벡터 
---------------  

교수님이 말씀하시길, 선형대수학을 위해서는 벡터와 그 성질을 전제로 해야한다했다.  
이 챕터에서는 벡터의 성질을 n-차원으로 확장할 것이고, 내적의 정의, 직선과 평면의 방정식을 공부할 것이라고 했다.  

---------------

### 스칼라 VS 벡터 (Scalar vs Vector)  
---------------
  <span style="color:red">스칼라</span>: 일상적으로 사용하는 물리적인 양  
  크기만 주어지지만 이 것으로 완전히 표시가 가능한 양으로 길이, 넓이, 질량, 온도 등이 있다.  
  + 만약 k 가 scalar면, $k \in \mathbb{R}$ 라고 Chapter 7 까지 가정한다. 


  <span style="color:red">벡터</span>: 일상적으로 사용하는 물리적인 양  
  크기만 주어지지만 이 것으로 완전히 표시: 벡터는 **유향성분**으로 방향을 화살표로 표현이 가능하다.  
  + 속도, 위치이동, 힘과 같이 방향이 지정되지 않으면 표현 불가능이다.  
  + 또한 벡터는 **크기**와 **방향**이 같으면, 시작점과 상관없이 동일한 벡터다.  
  + 크기가 0인 벡터는 방향 상관없이 **영벡터**라고 한다.

--------------  

#### **1.1.1 정의: 벡터의 덧셈과 스칼라배**    
두 벡터 $\mathbf{x, y}$와 스칼라 $k$에 대하여 두 벡터의 합 $\mathbf{x+y}$와 $k$에 의한 $\mathbf{x}$의 스칼라배 $k \mathbf{x}$를 다음과 같이 정의한다.  
1.  $\mathbf{x+y}$는 $\mathbf{x, y}$에 의하여 결정되는 평행사변형의 대각선으로 표시되는 벡터다.  
2.  $k \mathbf{x}$는  
   1) if $k < 0$, $\mathbf{x}$ 의 방향이 반대로 $|k|$배 길어진다.  
   2) if $k > 0$, $\mathbf{x}$ 는 원래 방향으로 $|k|$배 길어진다.  
3. $- \mathbf{x}$을 $\mathbf{x}$의 `음벡터`라 한다. 
$R^2$은 2차원 '평면' 이고 $R^3$은 3차원 '공간'임은 당연히 알고있는 사실이다. 차원 별 벡터를 확인해보자.  

---------------   

#### **1.1.2 정의: 평면벡터(Vector in plane), 공간벡터(Vector in space)**  
두 실수들의 순서조 $x_1, x_2$를 `(평면)벡터(vector in plane)`라 하고, 이는  
<br/>
$$
\begin{align*}
\qquad \mathbf{x} = (x_1, x_2) \quad or \quad
\mathbf{x} = 
   \begin{bmatrix} x_1 \\ x_2 
   \end{bmatrix}
\end{align*}  
$$ 
로 나타낸다.  
두 실수들의 순서조  $x_1, x_2, x_3$은 `(공간)벡터(vector in space)`라 하고, 이는  
<br/>
$$
\begin{align*}
\qquad \mathbf{x} = (x_1, x_2, x_3) \quad or \quad
\mathbf{x} = 
   \begin{bmatrix} x_1 \\ x_2 \\ x_3
   \end{bmatrix}
\end{align*}  
$$ 
로 나타낸다.  

또한 $x_1, x_2$나 $x_1, x_2, x_3$을 벡터의 `성분(component)`라고 한다. \mathbb{R^n} 으로 확장했을 때도 마찬가지다.  

-------------------

#### **1.1.3 정의: 상등(Equivalent)** 
$R^2$의 벡터  
$$
\qquad \mathbf{x} = 
   \begin{bmatrix} x_1 \\ x_2 
   \end{bmatrix}, \quad
   \mathbf{y} = 
   \begin{bmatrix} y_1 \\ y_2 
   \end{bmatrix}
$$  
   에 대하여  $x_1 = y_1$, $x_2 = y_2$ 이면 $\mathbf{x} = \mathbf{y}$ 이고, `상등`이라한다. \mathbb{R^n} 으로 확장했을 때의 n차원 벡터 또한 마찬가지다.

--------------------  
#### **정리 1.1.1**  
$R^n$의 벡터 $\mathbf{x, y, z}$ 와 스칼라 $h, k$에 대하여 다음이 성립한다.
(1) $\mathbf{x + y} = \mathbf{y + x}$ (교환법칙)  
(2) $\mathbf{(x + y) + z} = \mathbf{x + (y + z)}$ (결합법칙)  
(3) $\mathbf{x + 0} = \mathbf{x} = \mathbf{0 + x}$  
(4) $\mathbf{x + (-x) = 0 = (-x) + x} $  
(5) $k \mathbf{(x + y)} = k \mathbf{x} + k \mathbf{y} $  
(6) $(h + k) \mathbf{x} = h \mathbf{x} + k \mathbf{x} $  
(7) $(hk) \mathbf{x} = h (k \mathbf{x})  
(8) 1 \mathbf{x} = \mathbf{x}  

-------------------  
#### **정리 1.1.2**  
$R^n$의 벡터 $\mathbf{x}$ 와 스칼라 $k$에 대하여 다음이 성립한다.  
(1) 0 \mathbf{x} = **0**
(2) k**0** = **0**  
(3) (-1) \mathbf{x} = $- \mathbf{x}$

-------------------  
#### **1.1.4 정의: 선형결합(Linear Combination)**
$\mathbf{v_1, v_2, ..., v_k}$가 $r^m$의 벡터이고, 계수 ${c_1, c_2, ..., c_k}$가 실수일 때,  
$$
\begin{align*}
\quad \mathbf{x} = c_1 * v_1 + c_2 * v_2 + ... + c_k * v_k
\end{align*}
$$
인 형태를 $\mathbf{v_1, v_2, ..., v_k}$ 들의 일차결합(Linear Combination)이라 한다.  
