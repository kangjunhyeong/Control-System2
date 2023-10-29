# Control-System2  

![image](https://github.com/kangjunhyeong/Control-System2/assets/144297425/8f267e3b-914d-4cf6-a368-44924af004a9)  


(a) $$y(t) = x_1(t), \frac{dy(t)}{dt} = x_2(t) $$  
(b)
$$\frac{dx_1(t)}{dt} = x_2(t)\$$  
$$M\frac{d^2y(t)}{dt^2} + b\frac{dy(t)}{dt} + ky(t) = F(t)\$$  
$$\frac{dx_2(t)}{dt} = \frac{F(t) - bx_2(t) - kx_1(t)}{M}\$$  
(c)
$$\frac{dy(t)}{dt} = \begin{bmatrix}0&1\\\ (\frac{-k}{M})&\frac{-b}{M}\end{bmatrix}y(t) + \begin{bmatrix}0\\\ (\frac{1}{M}F(t)$$

![image](https://github.com/kangjunhyeong/Control-System2/assets/144297425/7fe5c29b-973e-41c8-a3a4-405d6c65014f)  

$$x_1(t)=i_L(t), x_2(t)=v_C(t)$$  

이걸로 왼쪽 오른쪽 KVL을 돌려주면  
(1) 왼쪽 KVL  

$$-v_1(t)+L\frac{di_L(t)}{dt}+R(i_L(t)-i_C(t))=0$$  

상태변수를 대입해주면  

$$-v_1(t)+L\frac{di_L(t)}{dt}+R(x_1(t)-C\frac{x_2(t)}{dt})=0$$  

위 식을 정리해주면  

$$\frac{dx_1(t)}{dt} = \frac{1}{L}(v_1(t)-v_2(t)+x_2(t))$$  

(2) 오른쪽 KVL  

$$-v_2(t)+v_C(t)+R(i_L(t)-i_C(t))=0$$

상태변수를 대입해주면

$$-v_2(t)+x_2(t)+R(x_1(t)-i_C(t))=0$$  

위 식을 정리해주면  
$$\frac{dx_2(t)}{dt} = \frac{1}{C}x_1(t) - \frac{v_2(t)}{RC} + \frac{x_2(t)}{RC}$$  

$$\begin{bmatrix}0&1\\\ (\frac{-k}{M})&\frac{-b}{M}\end{bmatrix}y(t)$$  

$$
dy/dt = | 0   1 | y(t)   + | 0      |
        | -k/M -b/M|         | 1/M  | F(t)
$$
