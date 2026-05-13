# Giải bài 1

Dữ kiện:

- Hộp 1: $a=7$ bi đỏ, $b=6$ bi xanh, tổng $13$ bi.
- Hộp 2: $c=8$ bi đỏ, $d=11$ bi xanh, tổng $19$ bi.

## a)

Lấy ngẫu nhiên $3$ viên từ hộp 1. Gọi $X$ là số bi đỏ lấy được.

$X$ có phân phối siêu bội:

$$
P(X=k)=\frac{\binom{7}{k}\binom{6}{3-k}}{\binom{13}{3}}, \quad k=0,1,2,3.
$$

Vì $\binom{13}{3}=286$, bảng phân phối xác suất:

| $x$ | 0 | 1 | 2 | 3 |
|---:|---:|---:|---:|---:|
| $P(X=x)$ | $\frac{10}{143}$ | $\frac{105}{286}$ | $\frac{63}{143}$ | $\frac{35}{286}$ |

Hàm phân phối xác suất:

$$
F_X(x)=
\begin{cases}
0, & x<0,\\
\frac{10}{143}, & 0\le x<1,\\
\frac{125}{286}, & 1\le x<2,\\
\frac{251}{286}, & 2\le x<3,\\
1, & x\ge 3.
\end{cases}
$$

Kỳ vọng:

$$
E(X)=3\cdot \frac{7}{13}=\frac{21}{13}.
$$

Phương sai:

$$
\operatorname{Var}(X)=3\cdot \frac{7}{13}\cdot \frac{6}{13}\cdot \frac{13-3}{13-1}
=\frac{105}{169}.
$$

## b)

Lấy từ mỗi hộp một viên. Xác suất hai viên khác màu:

$$
P=\frac{7}{13}\cdot \frac{11}{19}+\frac{6}{13}\cdot \frac{8}{19}
=\frac{77+48}{247}
=\frac{125}{247}.
$$

## c)

Lấy từ mỗi hộp một viên. Gọi $Y$ là số bi đỏ trong hai viên lấy được.

$Y$ nhận giá trị $0,1,2$.

$$
P(Y=0)=\frac{6}{13}\cdot \frac{11}{19}=\frac{66}{247}.
$$

$$
P(Y=2)=\frac{7}{13}\cdot \frac{8}{19}=\frac{56}{247}.
$$

$$
P(Y=1)=1-\frac{66}{247}-\frac{56}{247}=\frac{125}{247}.
$$

Bảng phân phối xác suất:

| $y$ | 0 | 1 | 2 |
|---:|---:|---:|---:|
| $P(Y=y)$ | $\frac{66}{247}$ | $\frac{125}{247}$ | $\frac{56}{247}$ |

## d)

Lấy từ mỗi hộp một viên, sau đó chọn ngẫu nhiên một viên trong hai viên đó. Xác suất viên được chọn là bi đỏ:

$$
P=\frac{1}{2}\left(\frac{7}{13}+\frac{8}{19}\right)
=\frac{1}{2}\cdot \frac{237}{247}
=\frac{237}{494}.
$$

## e)

Hiểu đề là: lấy $2$ viên từ hộp 1 bỏ vào hộp 2, sau đó lấy ngẫu nhiên $2$ viên từ hộp 2. Tính xác suất lấy được hai bi đỏ.

Gọi $T$ là số bi đỏ trong $2$ viên chuyển từ hộp 1 sang hộp 2. Khi đó:

$$
P(T=t)=\frac{\binom{7}{t}\binom{6}{2-t}}{\binom{13}{2}}, \quad t=0,1,2.
$$

Ta có:

$$
P(T=0)=\frac{15}{78},\quad P(T=1)=\frac{42}{78},\quad P(T=2)=\frac{21}{78}.
$$

Sau khi chuyển, hộp 2 có tổng $21$ viên, trong đó có $8+T$ bi đỏ.

Xác suất lấy được hai bi đỏ:

$$
P=\sum_{t=0}^{2}P(T=t)\frac{\binom{8+t}{2}}{\binom{21}{2}}.
$$

$$
P=\frac{15}{78}\cdot\frac{\binom{8}{2}}{\binom{21}{2}}
+\frac{42}{78}\cdot\frac{\binom{9}{2}}{\binom{21}{2}}
+\frac{21}{78}\cdot\frac{\binom{10}{2}}{\binom{21}{2}}.
$$

$$
P=\frac{15\cdot 28+42\cdot 36+21\cdot 45}{78\cdot 210}
=\frac{2877}{16380}
=\frac{959}{5460}.
$$

---

# Giải bài thống kê

Dữ liệu ghép lớp:

| Trọng lượng | 30-35 | 35-40 | 40-45 | 45-50 | 50-55 | 55-60 | 60-65 | 65-70 |
|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| Số trái cây | 1 | 17 | 31 | 43 | 96 | 29 | 17 | 5 |

Dùng trung điểm lớp:

| Lớp | 30-35 | 35-40 | 40-45 | 45-50 | 50-55 | 55-60 | 60-65 | 65-70 |
|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| Trung điểm $x_i$ | 32.5 | 37.5 | 42.5 | 47.5 | 52.5 | 57.5 | 62.5 | 67.5 |
| Tần số $n_i$ | 1 | 17 | 31 | 43 | 96 | 29 | 17 | 5 |

Tổng mẫu:

$$
n=1+17+31+43+96+29+17+5=239.
$$

## a)

Trung bình mẫu:

$$
\bar{x}=\frac{\sum n_i x_i}{n}=50.7845.
$$

Phương sai mẫu hiệu chỉnh:

$$
s^2=\frac{\sum n_i(x_i-\bar{x})^2}{n-1}=47.2548.
$$

Độ lệch chuẩn mẫu:

$$
s=\sqrt{s^2}=6.8742.
$$

Nếu dùng phương sai mẫu không hiệu chỉnh:

$$
\frac{\sum n_i(x_i-\bar{x})^2}{n}=47.0571.
$$

## b)

Ước lượng khoảng cho trọng lượng trung bình với độ tin cậy $95\%$.

Vì $n=239$ lớn, dùng $z_{0.975}=1.96$:

$$
\bar{x}\pm 1.96\frac{s}{\sqrt{n}}
=50.7845\pm 1.96\frac{6.8742}{\sqrt{239}}.
$$

Suy ra:

$$
\mu\in(49.9130;51.6560).
$$

Muốn độ chính xác $\varepsilon=0.21g$ với độ tin cậy $99\%$, dùng $z_{0.995}=2.576$:

$$
n\ge \left(\frac{2.576s}{0.21}\right)^2
=7110.4888.
$$

Vậy cần tổng cộng ít nhất:

$$
n=7111.
$$

Số trái cần điều tra thêm:

$$
7111-239=6872.
$$

## c)

Trái cây có trọng lượng lớn hơn $55g$ thuộc các lớp $55-60,60-65,65-70$.

Số trái:

$$
29+17+5=51.
$$

Tỷ lệ mẫu:

$$
\hat{p}=\frac{51}{239}=0.2134.
$$

Ước lượng khoảng tỷ lệ với độ tin cậy $99\%$:

$$
\hat{p}\pm 2.576\sqrt{\frac{\hat{p}(1-\hat{p})}{n}}.
$$

Suy ra:

$$
p\in(0.1451;0.2817).
$$

Muốn sai số ước lượng không lớn hơn $2\%$, lấy trường hợp xấu nhất $p(1-p)\le 0.25$:

$$
n\ge \frac{2.576^2\cdot 0.25}{0.02^2}=4147.36.
$$

Vậy cần điều tra ít nhất:

$$
4148 \text{ trái}.
$$

## d)

Kiểm định ý kiến: trọng lượng trung bình nhỏ hơn $52g$.

Giả thuyết:

$$
H_0:\mu=52,\quad H_1:\mu<52.
$$

Mức ý nghĩa $\alpha=5\%$, kiểm định trái. Miền bác bỏ:

$$
Z<-1.645.
$$

Thống kê kiểm định:

$$
Z=\frac{\bar{x}-52}{s/\sqrt{n}}
=\frac{50.7845-52}{6.8742/\sqrt{239}}
=-2.7335.
$$

Vì:

$$
-2.7335<-1.645,
$$

nên bác bỏ $H_0$.

Kết luận: có cơ sở thống kê ở mức ý nghĩa $5\%$ để cho rằng trọng lượng trung bình nhỏ hơn $52g$.

## e)

Kiểm định tỷ lệ trái cây có trọng lượng $>55g$ so với $20\%$.

Giả thuyết:

$$
H_0:p=0.2,\quad H_1:p\ne 0.2.
$$

Mức ý nghĩa $\alpha=5\%$, kiểm định hai phía. Miền bác bỏ:

$$
|Z|>1.96.
$$

Thống kê kiểm định:

$$
Z=\frac{\hat{p}-0.2}{\sqrt{0.2(1-0.2)/239}}
=0.5175.
$$

Vì:

$$
|0.5175|<1.96,
$$

nên không bác bỏ $H_0$.

Kết luận: chưa có cơ sở thống kê ở mức ý nghĩa $5\%$ để nói tỷ lệ trái cây nặng hơn $55g$ khác $20\%$.

## f)

Trang trại B: $n_B=200$, $\bar{x}_B=52.5$, $s_B=7$.

So sánh trọng lượng trung bình hai trang trại A và B.

Giả thuyết:

$$
H_0:\mu_A=\mu_B,\quad H_1:\mu_A\ne\mu_B.
$$

Mức ý nghĩa $5\%$, kiểm định hai phía. Miền bác bỏ:

$$
|Z|>1.96.
$$

Thống kê kiểm định:

$$
Z=\frac{\bar{x}_A-\bar{x}_B}{\sqrt{\frac{s_A^2}{n_A}+\frac{s_B^2}{n_B}}}
=\frac{50.7845-52.5}{\sqrt{\frac{47.2548}{239}+\frac{49}{200}}}
=-2.5782.
$$

Vì:

$$
|-2.5782|>1.96,
$$

nên bác bỏ $H_0$.

Kết luận: có cơ sở thống kê ở mức ý nghĩa $5\%$ để cho rằng trọng lượng trung bình của loại trái cây ở hai trang trại khác nhau. Vì $\bar{x}_A<\bar{x}_B$, trang trại B có trọng lượng trung bình cao hơn.

## g)

Trang trại B: khảo sát $300$ quả, có $80$ quả nặng hơn $55g$.

Tỷ lệ mẫu ở A:

$$
\hat{p}_A=\frac{51}{239}=0.2134.
$$

Tỷ lệ mẫu ở B:

$$
\hat{p}_B=\frac{80}{300}=0.2667.
$$

Kiểm định tỷ lệ hai tổng thể:

$$
H_0:p_A=p_B,\quad H_1:p_A\ne p_B.
$$

Mức ý nghĩa $5\%$, kiểm định hai phía. Tỷ lệ gộp:

$$
\hat{p}=\frac{51+80}{239+300}=0.2430.
$$

Thống kê kiểm định:

$$
Z=\frac{\hat{p}_A-\hat{p}_B}{\sqrt{\hat{p}(1-\hat{p})\left(\frac{1}{239}+\frac{1}{300}\right)}}
=-1.4326.
$$

Vì:

$$
|-1.4326|<1.96,
$$

nên không bác bỏ $H_0$.

Kết luận: chưa có cơ sở thống kê ở mức ý nghĩa $5\%$ để cho rằng tỷ lệ trái cây nặng hơn $55g$ ở hai trang trại A và B khác nhau.
