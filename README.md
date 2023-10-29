# Control-System2  

![image](https://github.com/kangjunhyeong/Control-System2/assets/144297425/8f267e3b-914d-4cf6-a368-44924af004a9)  

 
(a) $$y(t) = x_1(t), \frac{dy(t)}{dt} = x_2(t) $$  
(b)
$$\frac{dx_1(t)}{dt} = x_2(t)\$$  
$$M\frac{d^2y(t)}{dt^2} + b\frac{dy(t)}{dt} + ky(t) = F(t)\$$  
$$\frac{dx_2(t)}{dt} = \frac{F(t) - bx_2(t) - kx_1(t)}{M}\$$  
(c)  

$$
\frac{dy}{dt} = \begin{bmatrix} 0 & 1 \\\ -\frac{k}{M} & -\frac{b}{M} \end{bmatrix} y(t) + \begin{bmatrix} 0 \\\ \frac{1}{M} \end{bmatrix} F(t)\
$$

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

이 식들을 상태미분방정식으로 표현해주면  

$$
\begin{bmatrix} \frac{dx_1(t)}{dt} \\\ \frac{dx_2(t)}{dt} \end{bmatrix} = \begin{bmatrix} 0 & 1 \\\ \frac{1}{C} & \frac{1}{RC} \end{bmatrix} \begin{bmatrix} x_1(t) \\\ x_2(t) \end{bmatrix} + \begin{bmatrix} \frac{1}{L} & -\frac{1}{L} \\\ 0 & -\frac{1}{RC} \end{bmatrix} \begin{bmatrix} v_1(t) \\\ v_2(t) \end{bmatrix}
$$

A행렬이 다음과 같으므로  
![image](https://github.com/kangjunhyeong/Control-System2/assets/144297425/37288a2a-5dab-4c58-b4b5-fcf680669ff1)  

$$
\begin{bmatrix} \frac{dx_1(t)}{dt} \\\ \frac{dx_2(t)}{dt} \end{bmatrix} = \begin{bmatrix} 0 & 1 \\\ \frac{-1}{C} & \frac{-1}{RC} \end{bmatrix} \begin{bmatrix} x_1(t) \\\ x_2(t) \end{bmatrix} + \begin{bmatrix} \frac{1}{L} & -\frac{1}{L} \\\ 0 & -\frac{-1}{RC} \end{bmatrix} \begin{bmatrix} v_1(t) \\\ v_2(t) \end{bmatrix}
$$

![image](https://github.com/kangjunhyeong/Control-System2/assets/144297425/7975f19d-6bde-4dad-9681-065672028140)
![image](https://github.com/kangjunhyeong/Control-System2/assets/144297425/6f9f90ab-cd16-4f23-b955-139ab63adc42)  

(a)

$$
\frac{Y(s)}{R(s)} = \frac{(\frac{s+2}{s+8})(\frac{1}{s-3})(\frac{1}{s})}{1+(\frac{s+2}{s+8})(\frac{1}{s-3})(\frac{1}{s})}
$$

$$
T(s)=\frac{s+2}{s^3+5s^2-23s+2}
$$  

(b)  

$$
\frac{Y(s)}{R(s)}=\frac{s+2}{s^3+5s^2-23s+2}\frac{w(s)}{w(s)}
$$  

$$
Y(s)=sw(s)+2w(s), R(s)=s^3w(s)+5w^2(s)-23sw(s)+2w(s)
$$

$$
w(t)=x_1, w'(t)=x_2, w''(t)=x_3
$$

$$
y(t)=w'(t)+2w(t), r(t)=w'''(t)+5w''(t)-23'(t)+2w(t)
$$

$$
\[ \begin{bmatrix} \dot{x}_1 \\\ \dot{x}_2 \\\ \dot{x}_3 \end{bmatrix} = \begin{bmatrix} 0 & 1 & 0 \\\ 0 & 0 & 1 \\\ -2 & 203 & -5 \end{bmatrix} \begin{bmatrix} x_1 \\\ x_2 \\\ x_3 \end{bmatrix} + \begin{bmatrix} 0 \\\ 0 \\\ 1 \end{bmatrix} r(t) \]
$$
