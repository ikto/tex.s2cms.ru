# Торможение реликтовым излучением

http://susy.written.ru/2014/01/05/CMB_drag

На втором курсе за неделю перед досрочным экзаменом по теоретической физике Семен Соломонович Герштейн задал мне две задачи. В одной требовалось найти угловое распределение синхротронного излучения электрона, движущегося по окружности. Вторая оказалась интереснее: найти силу торможения со стороны реликтового излучения на площадку, движущуюся перпендикулярно самой себе. Остановимся на ней подробнее. Записей с тех времен у меня не сохранилось, а в литературе опубликованы противоречивые результаты. Хороший повод заново разобраться в задаче.

## Обозначения и соглашения

Под реликтовым излучением мы подразумеваем равновесное тепловое излучение при некоторой температуре *T*. Напомним, что плотность энергии и давление равновесного излучения определяются температурой: *ε* = 4*πσT*^4^/*c*, *P* = *ε*/3.

В системе отсчета, связанной с реликтовым излучением, оно однородно и изотропно. Относящиеся к ней величины будем обозначать символами без штрихов. Относительно этой системы со скоростью *v* движется площадка (например, диск) с коэффициентом отражения *R*. Штрихами обозначим величины в сопутствующей системе отсчета (связанной с площадкой).

Будем опускать скорость света c в тех формулах, где она легко восстанавливается из соображений размерности.

## Обзор литературы

В публикациях по этой проблеме нет консенсуса. Например, в письме Андрея Шепелева в УФН под названием "[Космический микроволновой фон и аристотелевы представления о движении](http://ufn.ru/ru/articles/2005/1/i/)" приведена формула для давления на площадку $$P=-v\,(1+v^2/2)\,\varepsilon/2$$. Этот ответ, как мы увидим ниже, явно ошибочен. Автор не раскрывает вычислений, поэтому невозможно понять, где ошибка.

В работе Баласаняна и Мкртчяна "[Blackbody radiation drag on a relativistically moving mirror](http://arxiv.org/abs/0907.2311)" вычисляется плотность импульса в системе отсчета, связанной с диском, и она отождествляется с давлением (с точностью до учета отражения). По поводу этой работы у меня есть два замечания. Во-первых, для вычисления плотности импульса авторы предлагают непростой путь. Они интегрируют импульс фотона $$\vec{k}'$$ по импульсному пространству c функцией распределения

$$n'(\vec{k}')={1\over e^{\gamma(\omega' +k'_xv)/T}-1}.$$(1)

В то же время плотность импульса электромагнитного излучения отличается на множитель 1/c^2^ от вектора Поинтинга, проекции которого есть компоненты $$T_{0i}$$ тензора энергии-импульса. Записав преобразование Лоренца для компоненты $$T_{01}$$ тензора

$$T^{\mu\nu}=\begin{pmatrix}\varepsilon &0&0&0\\0&\varepsilon/3&0&0\\0&0&\varepsilon/3&0\\0&0&0&\varepsilon/3\end{pmatrix},$$

сразу получаем плотность импульса (см. II том Ландау и Лифшица, §35, формула 35.3)

$$S'_x=-{4\over 3}\,\varepsilon\,{v\over 1-v^2}.$$(2)

Во-вторых, неправильно отождествлять проекцию импульса электромагнитной волны, падающей на площадку под углом *θ* к нормали, с давлением, потому что сама площадка находится под углом, и ее эффективная площадь уменьшается. Из-за дополнительного фактора |cos *θ*|, появляющегося под интегралом (см. ниже), формула (2) не является правильным ответом, и использовать ее вообще нельзя.

## Вычисление в сопутствующей системе отсчета

Давление как силу на единицу поверхности определим через импульс, передаваемый диску при отражении или поглощении фотонов за единицу времени:

$$P={F\over S}={1\over S}{\hbar\Delta k\over\Delta t}.$$

Если фотоны летят под углом *θ* к нормали, то за время Δ*t* до неподвижной площадки *S* долетят фотоны из объема *S c*Δ*t* |cos *θ*|. Из них доля *R* отразится и доля (1−*R*) поглотится. Каждый поглощенный фотон отдаст импульс $$\hbar k\cos\theta=\hbar\omega\cos\theta/c$$, а каждый отраженный --- в два раза больше. Собирая всё вместе, получаем в сопутствующей системе отсчета

$$P=\int{\hbar\omega'\cos\theta'\over S\,c\Delta t'}\,(1+R)\,S\,c\Delta t'\,|\cos\theta'|\,n'(\vec{k}')\,d^3k'.$$

Напомним, что частота ω и волновой вектор $$\vec{k}$$ образуют четырехвектор <nobr>$$(\omega, \vec{k})$$.</nobr> Переход к движущейся системе координат осуществляется преобразованиями Лоренца

$$\omega'={\omega-k_xv\over\sqrt{1-v^2}},\qquad k_x'={k_x-\omega v\over\sqrt{1-v^2}}.$$

Функция распределения $$n(\vec{k})$$ в фазовом пространстве инвариантна относительно преобразований Лоренца, так как и элемент фазового объема $$d^3r\,d^3k$$, и число частиц $$dN=n(\vec{r},\vec{k})\,d^3r\,d^3k$$ есть инварианты (подробнее см. II том Ландау и Лифшица, §10). Именно поэтому функция распределения в движущейся системе $$n'(\vec{k'})=n(\vec{k})$$ есть обычное распределение Бозе --- Эйнштейна (1), в которое подставлена преобразованная частота.

В итоге давление определяется следующим интегралом

$$P=\int \hbar\omega'\cos\theta'\,(1+R)\,|\cos\theta'|\,{const\over exp\left(\dfrac{\hbar\omega'}{kT}\,\dfrac{1+v\cos\theta'}{\sqrt{1-v^2}}\right)-1}\,\omega'^2\,d\omega'\,{d(\cos\theta')\over 2}.$$(3)

Вместо того чтобы следить за комбинацией констант, которая в итоге должна свестись к постоянной Стефана-Больцмана *σ*, мы примем условие нормировки в выражении для плотности энергии с той же самой константой:

$$\varepsilon=\int \hbar\omega\,{const\over exp\left(\dfrac{\hbar\omega}{kT}\right)-1}\,\omega^2\,d\omega={4\pi\sigma\over c}T^4.$$

Еще отсюда видно, что (3) можно упростить, проинтегрировав по частотам. Множитель $${\sqrt{1-v^2}}/{(1+v\cos\theta')}$$ перед температурой в экспоненте появится под интегралом в четвертой степени. Дальнейшее вычисление тривиально:

$$P=\varepsilon\,(1+R)\int\limits_{-1}^{1}\cos\theta'\,|\cos\theta'|\,\dfrac{(1-v^2)^2}{(1+v\cos\theta')^4}\,{d(\cos\theta')\over 2},$$

$${\Large\boxed{P=-\varepsilon\,(1+R)\,\frac{v\,(1+v^2/3)}{1-v^2}}.}$$(4)

Чтобы убедиться в правильности результата, вычислим тем же методом давление фотонного газа на одну сторону покоящейся пластины. Зависящий от скорости подынтегральный множитель исчезает, а интеграл в пределах от 0 до 1 равен 1/3. Полное давление есть (1+*R*) *ε*/6. Если пластина всё отражает и ничего не поглощает, давление совпадает с ожидаемой величиной *ε*/3. Если пластина всё поглощает, давление равно *ε*/6 и составляет половину от давления фотонного газа *ε*/3. Вторая половина набегает за счет собственного излучения пластины, которое мы в наших расчетах не учитывали.

Формула (4) не совпадает ни с результатом Шепелева, который утверждает, что ответ сложен, и раскладывает его в ряд, ни с результатом Баласаняна, который ошибочно отождествляет в этой задаче плотность импульса и давление.

## Вычисление в неподвижной системе отсчета

<img align="right" src="http://susy.written.ru/_pictures/relativity/relic_disc.png" alt="" width="188" height="288">
Тот же результат получается и в неподвижной системе отсчета. В ней не нужно иметь дела с функцией распределения фотонов, однако из-за движения площадки геометрические выкладки сложнее.

Чтобы понять, сколько летящих под углом *θ* фотонов с частотой ω попадет за время Δ*t* на площадку AB, нужно ввести понятие "заметаемого объема" (объем, фотоны из которого попадут на диск) и умножить его величину на плотность фотонов *n*ω. За это время площадка переместится из положения A~1~B~1~ в положение A~2~B~2~, а фотоны из точек C и D долетят до диска. Таким образом, заметаемый объем соответствует фигуре A~1~B~1~DС, и его величина равна <nobr>*S* |*c*Δ*t* cos *θ* − *v*Δ*t*|</nobr>.

При отражении фотона от площадки в сопутствующей системе отсчета знак проекции волнового вектора фотона изменяется на противоположный: $$k'_{2x}=-k'_{1x}$$. Найдем соответствующее изменение в неподвижной системе:

$$\begin{array}{ll}\Delta k\!\!\!&=k_{1x}-k_{2x}=k_{1x}-\gamma(k'_{2x}+\omega'_2v)=k_{1x}+\gamma(k'_{1x}-\omega'_1v)=\\ &=k_{1x}+\gamma\left(\gamma(k_{1x}-\omega_1 v)-\gamma(\omega_1-k_{1x}v) v\right)=k_{1x}+\gamma^2\left(k_{1x}(1+v^2)-2v\omega\right).\end{array}$$

Выражая проекцию волнового вектора через частоту фотона и азимутальный угол $$k_x=\omega\cos\theta$$, получаем

$$\Delta k=\omega\left[\cos\theta\left(1+{1+v^2\over 1-v^2}\right)-2{v\over 1-v^2}\right]={2\omega\over 1-v^2}\,(\cos\theta-v).$$

Ясно, что двойку в последнем выражении нужно заменить на (1+*R*), чтобы учесть случай произвольного коэффициента отражения *R*. Давление

$$P_\omega=\int{\hbar\omega\over S\,c\Delta t}\,{1+R\over 1-v^2}\,(\cos\theta-v)\,S|c\Delta t\cos\theta-v\Delta t|\,n_\omega\,{d(\cos\theta)\over2},$$

$$P_\omega={n_\omega\over 2}\hbar\omega\,{1+R\over 1-v^2}\int\limits_{-1}^{1}dx\,(x-v)|x-v|.$$

После вычисления интеграла и усреднения плотности энергии $$n_\omega\hbar\omega$$ по частотам получается формула (4).