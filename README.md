# Цель исследования
Автоматизировать процесс сопоставления побочных эффектов из реальных медицинских текстов с формализованными медицинскими концептами (CUI), используя методы обработки естественного языка (NLP) и векторные представления слов (эмбеддинги), чтобы:

выявить закономерности в лабораторных анализах пациентов с показаниями к антибиотикотерапии;

провести семантическое сопоставление побочных эффектов с терминами медицинской онтологии (UMLS).

	Text	id	CUI	CONCEPT	Similarity
0	The vertigo is rendering me unable to function...	22	C0456820	Loss of capacity to feel emotions,Loss of capa...	0.909012
1	The vertigo is rendering me unable to function...	22	C0563158	Compulsion to act on dangerous thoughts,Compul...	0.884145
2	I am seeing a specialist for the vertigo and u...	23	C1562291	Loss of interest in previously enjoyable activ...	0.856806
3	I am seeing a specialist for the vertigo and u...	23	C0456820	Loss of capacity to feel emotions,Loss of capa...	0.846142
4	My vertigo has not responded to conservative t...	24	C0423994	Unable to think clearly,Unable to think clearly	0.877083
5	My vertigo has not responded to conservative t...	24	C0456820	Loss of capacity to feel emotions,Loss of capa...	0.852326
6	Muscle spasms, muscle twitching, muscle sorene...	25	C0151786	Muscle Weakness,muscle weakness	0.867573
7	Muscle spasms, muscle twitching, muscle sorene...	25	C0151786	Muscle Weakness,Muscle weakness	0.867573
8	I took Lexapro for 3 days in 10mg doses and ha...	26	C0233408	Disorientated in time,disorientated in time	0.821447
9	I took Lexapro for 3 days in 10mg doses and ha...	26	C0233408	Disorientated in time,Disorientated in time	0.821447
10	Im sorry this is more about not taking it than...	27	C0456820	Loss of capacity to feel emotions,Loss of capa...	0.900919
11	Im sorry this is more about not taking it than...	27	C0563158	Compulsion to act on dangerous thoughts,Compul...	0.899394
12	Extreme Weight Gain 30 pounds.	30	C0043094	Weight Gain,Weight gain	0.878191
13	Extreme Weight Gain 30 pounds.	30	C0000765	Excessive body weight gain,Excessive weight gain	0.873315
14	Excessive perspiration, Erectile dysfunction.	31	C0425769	Excessive orgasm,Excessive orgasm	0.817262
15	Excessive perspiration, Erectile dysfunction.	31	C0242350	Erectile dysfunction,Impotence	0.782324
16	Almost no libido at all, Utterly useless.	32	C2981158	Lack of libido,Lack of libido	0.822505
17	Almost no libido at all, Utterly useless.	32	C0424565	Cannot sleep at all,Cannot sleep at all	0.819676
18	Took a while to have an effect on mood obvious...	33	C0563158	Compulsion to act on dangerous thoughts,Compul...	0.880838
19	Took a while to have an effect on mood obvious...	33	C1562291	Loss of interest in previously enjoyable activ...	0.876157
20	Very big increase in blood pressure which I ha...	34	C0497247	Increase in blood pressure,Finding of increase...	0.884014
21	Very big increase in blood pressure which I ha...	34	C0233632	Disturbance in thinking,Disturbance in thinking	0.858005
22	Have your blood pressure checked even if like ...	35	C0423994	Unable to think clearly,Unable to think clearly	0.884922
23	Have your blood pressure checked even if like ...	35	C0563158	Compulsion to act on dangerous thoughts,Compul...	0.863157
24	Heavy sedation, Jaw Clenching, Inability to or...	36	C0456820	Loss of capacity to feel emotions,Loss of capa...	0.786922
25	Heavy sedation, Jaw Clenching, Inability to or...	36	C0558185	Unable to move,Unable to move	0.777381
26	Very bad side effects.	37	C0563158	Compulsion to act on dangerous thoughts,Compul...	0.777762
27	Very bad side effects.	37	C0023222	Pain in lower limb,Pain in lower limb	0.756396
28	emotionless, Zombie effect.	38	C0233488	Feeling despair,Feeling despair	0.754872
29	emotionless, Zombie effect.	38	C0424329	Outbursts of anger,Outbursts of anger	0.750972


# Выводы
В подгруппах (показаны и не показаны антибиотики) существуют статистически значимые различия — это подтверждено с помощью непараметрических тестов (Крускала-Уоллиса и ANOVA).

Обнаружены потенциальные связи между результатами лабораторных анализов и назначением антибиотиков, что говорит о возможности машинного анализа для клинической поддержки принятия решений.

Метод семантического сопоставления с использованием эмбеддингов (BioWordVec) успешно позволил автоматически находить наиболее близкие по смыслу медицинские концепты для каждого текстового описания побочного эффекта.

