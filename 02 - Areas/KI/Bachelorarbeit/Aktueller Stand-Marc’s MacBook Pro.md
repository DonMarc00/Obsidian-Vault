---

excalidraw-plugin: parsed
tags: [excalidraw]

---
==⚠  Switch to EXCALIDRAW VIEW in the MORE OPTIONS menu of this document. ⚠==


# Text Elements
Kann die Anwendung von Document Understanding Transformers 
die Effizienz und Genauigkeit der Verarbeitung von Dokumenten verbessern? ^0Sxsd4xa

Pipeline ^Ftfc8Y7j

Analyse: Wie können Donuts
auf die Interpretation visueller/layoutbasierter
und textueller Elemente in Docs angewandt werden? ^hMLVEAaB

Vergleich OCR und Donut ^F5S1SapX

%%***>>>text element-link:[[Metriken]]<<<***%%Welche Metriken? ^FNph8gTi

Ist Vergleichbar? ^T0LGSDBJ

Nur kleiner Abschnitt ^Fx0f99RY

Vergleich Donuts zu CNN
sind sie vergleichbar? ^6skFYu1f

Zur Forschungsfrage: ^4SAe5j5u

Was ist die Methode
der Untersuchung? ^FvQFSSeG

Was heißt Effizienz und
Genauigkeit ^ADYkBx6f

Was ist der Status quo?
Wie werden Dokumente
verarbeitet? ^w60xs0BQ

Wie bemesse ich das Verfahren? ^lybaiNpM

Wie komme ich an Daten?
Wie mache ich einen Benchmark? ^zDA442T9

Wie implementiere ich es in ELO? ^ZI2ERpPD

Wie bleiben die Daten anonym? ^1diugU5G

Modelltraining -> Endanwendung ^lN4r6F9b

Woher kommen die Daten? ^YfFs7OSH

Vom Unternehmen ^DtWmhxNi

Von ELO ^f1XDIw1z

Um eigene Daten erweiterbar? ^RGhKpEUS

Ab wie viel Input
performt das Ding gut? ^HO5myDMu

Schätzung Nina:
~1000 ^k04DUpPC

Was ist der BusinessCase? ^YOggx1IA

Was zeichnet Donuts aus? ^gwn666Q3

Abgrenzung ViT <-> Donut <-> CNN ^Qt3INyaj

Theoretisch
Architektur über
Finetuning
--> Weboberfläche
wo selbst gelabelt werden
kann ^VSvIjoXG

Gebaut von
Benoit --> St ^SLq7IKd2

Auf Encoder-Ebene vergleichbar ^7pAYEmPM

ELO Finanzabteilung kriegt Doc
Metadaten werden zugeordnet ^u0Z76VlV

F1 ^yucGVVYm

Cost/
GPUh ^itM61GGJ

Accuracy ^dR4gcCtT

ANLS ^OAnnn6zU

EM ^ZHoU15G6

CIDEr ^u6xabILC

RA ^l3NSHzyZ

FPS ^YKWUOdjQ

Flops ^u0UX9Q1B

Methode: Experiment ^yDbQkuES

Genauigkeit:
Accuracy ^WmCx6Eyx

Effizienz (Abseits von Acc):
- F1
- Cost (i.e. GPUh)
- RA
- CIDEr
- FPS (vermutlich weniger
- EM
- ANLS ^LaCgdref

Händischen Labeling :( ^sU375XuL

VDU/VrDU ^iUNxf4qO

OCR + Downstream ^FMtrDmlQ

E2E ^KALykMsh

Donut
(OCR-Free)
10.2022 ^qeBnBXfT

OCR + BERT ^YRfrDvsO

LayoutLM3
7.2022 ^n8TpO48n

FastStrucText
(Hourglass)
5.2023
 ^uaRKhToE

DocFormer
 ^vhpTu6ZQ

Dublin
(OCR-Free)
12.2023 ^2QN8n7F6

Ernie
10.2022 ^vW8ARdTi

Rationale 
Distillation
11.2023 ^5b8wj5yd

ViT
6.2021 ^FQU6ZfX3

Swin
8.2021 ^ykCCNjtF

Donut
(OCR-Free)
10.2022 ^diuI977G

CNNs ^HjpYuqra

Hohe Datenmenge für Training ^5zRGmAPY

Niedrige Datenmenge für
Training ^7VKLZQpl

Auf Basis von Rechnungen
~1000 Stück ^M05mtzOP

Spezifikation ^W49u9ni6

Betrachtet für den UseCase ELO Rechnungsverarbeitung
im Vergleich zu OCR + Downstream
- Keine Massenverarbeitung sondern Einzelverarbeitung. Daher
FPS vermutlich weniger wichtig
- Evtl. Austausch der OCR
- Interessant: Wie performt es gegen heutiges SOTA? ^5AnFcCOl

Architektur u. Pipeline Donut: ^zGx4Stj3

Interessant: Self-Attention wird mit Shifting Windows
umgesetzt. Das ganze Bild wird über übergreifende
Panelgrenzen erzeugt ^pT81dz7F

Encoder:
Swin Transformer ^v3sdjfYk

Image ^vgRVOvmh

CNN Möglich ^NwBFTz2Y

Decoder:
BART ^KmxJJkC3

Embeddings ^DBWZJWAH

Token
Sequence ^wX6cBUtm

Output ^UbrMdh5z

Question/
Classification/
Parsing ^mYrmjY95

TIME ^hTOORAQ2

Hier auch die Abwägung:
Was sind Vor- und Nachteile ^3EKwmCYR

Grundsätzlicher Trend:
Mit fortlaufender Zeit bessere
Modelle ^j7Iky1iz

Projektgestalltung: ^wpkgGt0g

Daten labeln ^jvSjlKg0

Pipeline bauen ^7s8gxoce

Pipeline testen ^bdADuUFt

Experiment ^CtXGEDip

Modell Swap ^spCg6y4Z

Ergebniss ^uCIhlCXI

Neues Modell/
andere OCR ^GmTrhxDK

~1000 Rechnungen
via. Azure ^eVRLPXoH

- Sparrow Anpassung ELO ^dPeJIHKM

- FineTuning Sparrow ^StvMzI98

Flows-Kompatibel machen ^npz1A8Vq

- Inference ^RTFQL0hQ

10 - 20 genau anschauen
Effizienz auf 1000 prüfen --> GPUh oder Kosten betrachten
Nicht zu viele verschiedene Modelle
Eine Refferenz --> Das möchten wir haben
Dann 2-3 Aufbauten
Schlussstrich Ende 2023

1. Einleitung: Das Ziel dieser Arbeit ist: Dann Ziel der Arbeit
2. Um dieses Ziel zu beantworten machen wir: Experiment bewertung etc. deswegen ist die Arbeit so aufgebaut:
Dann so viel einleitend wir gehen jetzt in Kapitel 2
3. Gliederung Theorie typischerweise zu groß max. 20 S
4. OCR wichtig, dass es da drinne ist aber keine Details (Keine 5 Seiten für OCR, nur Details die ich brauche)
5. Arbeit so dass der Leser immer weiß wo er ist und was er liest, an die Hand nehmen und durchführen
(Es sollen nun OCR erklärt werden..)
6. Methodik ausformulieren
7. In 4. und 5. ich habe gemacht --> Wegen Eigenständigen Ergebnissen
8. Bei Ergebnissen: Nicht nur Modelle reflektieren sondern auch kritische Reflektion des Vorgehens
Wenn ich es nochmal mache, was würde ich anders/besser machen 
Auch mit dem Betreuer zusammensetzten und Fragen: Was hätten wir vor 4 Monaten besser machen können
9. Bewertungsstil: Formalien: 4, Wir biegen es noch hin 3, Liest sich flüssig: 2, Liest sich flüssig, keine Rechtschreibfehler
Kritische Distanz zu Quellen, Experiment funzt, Schöne Auswertung, Hinterfragen von Experiment: 1
10. Keine Internetquellen
11. Durchlesen lassen

Wenn ein Teil fertig, dann schicken
Beschreibung wie Experiment aussieht, aber nicht was
TIKZ: Latex Plugin für Skizzen --> ChatGPT
Für Metriken graphische Aufbereitung: TGFPlots bzw TIKZ kann auch Balkendiagramme etc.  ^kC4X6XX2

Classification ^kY3fi9wB

QA ^DoBWY3zE

Extraktiv ^oPfX0jNz

Swin-Transformer ^zbfCLHvA

OCR-Free ^Q7oADDsB

Donut Paper:
Swin kann durch CNN
ersetzt werden ^Z1RkZv9A

Limitation auf:
1 Refferrenzmodell
2 Vergleichsmodelle ^8Ddj1mKM

Offtermatt Feedback: ^pt2kV4O2

Ist OCR+Bert nicht vielleicht schon outdated?
Evtl. neuere Modelle? --> Grundlagenmodell, Herzstück
--> Neues wie DUBLIN ^fVH5yFv9

Betrachtung der wirtschaftlichkeit von BERT ^rwgMZMSa

Wirtschaftsseite OCR ^LqMd2y83

Acc /= Acc ^G3JKh93E

CRISP-DM als Datamining Framework ^EEMK3wnK

Wie messe ich GPU/h ^02kS9RHP

Kosten vom Training oder nur Pre-Training? ^CZRxvirA

Evtl. mit CORD testen ^kpEg77cn

Die 1000 die ich habe ^KGP34Je3

Anonymisiert von Kunden ^t1s4fSqD

Azure ^ITS51aOl

Welche Aufgabe ^IKkGwmwm

DocVQA ^Th9MkAuG

Parsing ^jnnNh8Kd

Classification ^ILK4au7K


# Embedded files
c64d24b765085d3519ee7c9c406d8490efba0bca: [[Pasted Image 20240223102308_663.png]]

%%
# Drawing
```json
{
	"type": "excalidraw",
	"version": 2,
	"source": "https://github.com/zsviczian/obsidian-excalidraw-plugin/releases/tag/2.0.17",
	"elements": [
		{
			"type": "freedraw",
			"version": 3,
			"versionNonce": 1074616793,
			"isDeleted": false,
			"id": "zfVn0U391JW2R_B3DvDJ0",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1694.3825920390032,
			"y": -798.7976616805108,
			"strokeColor": "#1971c2",
			"backgroundColor": "#ffc9c9",
			"width": 0.0001,
			"height": 0.0001,
			"seed": 1800691191,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710339700003,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					0.0001,
					0.0001
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 34,
			"versionNonce": 1367149207,
			"isDeleted": false,
			"id": "IEcWqwkYf8a_jx4E2b1gI",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -488.2187235877302,
			"y": 1273.2113966473917,
			"strokeColor": "#1971c2",
			"backgroundColor": "#ffc9c9",
			"width": 66.30944468890789,
			"height": 21.428915927167054,
			"seed": 1721895289,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252175617,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					-0.5230830858013178,
					0
				],
				[
					-1.4559690766348012,
					0
				],
				[
					-3.147162078415704,
					0
				],
				[
					-5.248321448693332,
					0
				],
				[
					-8.299530473557297,
					0
				],
				[
					-11.887063124831911,
					0
				],
				[
					-15.474595776106298,
					0
				],
				[
					-20.79255266059681,
					1.3251165734523056
				],
				[
					-24.916245474817515,
					2.144640651785039
				],
				[
					-28.028589835334515,
					3.3171640813011436
				],
				[
					-36.197349537441596,
					6.477484968594126
				],
				[
					-37.2479292225803,
					6.826234269705537
				],
				[
					-44.03051874731432,
					9.799062563431562
				],
				[
					-47.618051398588705,
					11.38138889798006
				],
				[
					-50.66926042345267,
					12.898329846803335
				],
				[
					-53.24544462102358,
					13.62631438512085
				],
				[
					-55.34660399130121,
					14.672480556723258
				],
				[
					-57.03779699308211,
					15.688079060499149
				],
				[
					-58.31935055329495,
					16.64270569208611
				],
				[
					-60.01070701854019,
					17.627899991499817
				],
				[
					-60.94359300937367,
					18.233777321975595
				],
				[
					-61.52764796736369,
					18.809168716356908
				],
				[
					-61.81975717809064,
					19.096864413547337
				],
				[
					-62.111702925353484,
					19.38456011073822
				],
				[
					-62.37324446825414,
					19.38456011073822
				],
				[
					-62.37324446825414,
					19.641769871834413
				],
				[
					-63.567672001988285,
					19.641769871834413
				],
				[
					-64.50055799282177,
					20.247647202309963
				],
				[
					-65.43328052019092,
					20.85352453278574
				],
				[
					-66.01749894164527,
					21.428915927167054
				],
				[
					-66.30944468890789,
					21.428915927167054
				],
				[
					-66.30944468890789,
					21.428915927167054
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 35,
			"versionNonce": 685576279,
			"isDeleted": false,
			"id": "txbqcwtx2GZMckMGH-RN6",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -427.7503188691139,
			"y": 1292.5523937448904,
			"strokeColor": "#1971c2",
			"backgroundColor": "#ffc9c9",
			"width": 26.284925061509284,
			"height": 103.43526670364668,
			"seed": 1938672345,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252173238,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					0,
					1.0461661716024082
				],
				[
					0,
					5.161031958750073
				],
				[
					0,
					11.795523584816465
				],
				[
					-1.5517586667222076,
					20.661781889146596
				],
				[
					-3.639840959854837,
					29.5280401934765
				],
				[
					-5.85411704743683,
					40.02451962739883
				],
				[
					-9.554929879480142,
					53.716219398244675
				],
				[
					-11.64301217261277,
					62.58247770257435
				],
				[
					-13.482466536525408,
					68.68080916569465
				],
				[
					-14.973253331058913,
					75.56368352578443
				],
				[
					-16.81270769497155,
					81.53557599925875
				],
				[
					-18.146569563764615,
					86.84486932014056
				],
				[
					-19.38889189254246,
					90.95973510728845
				],
				[
					-20.565828835595084,
					94.53852246322208
				],
				[
					-21.30255866925313,
					97.10596136545223
				],
				[
					-21.91718129506944,
					98.66654705924725
				],
				[
					-22.209290505796616,
					99.24193845362856
				],
				[
					-22.209290505796616,
					99.52963415081922
				],
				[
					-22.483909125842274,
					99.52963415081922
				],
				[
					-23.081041160977065,
					100.43628425563043
				],
				[
					-23.695663786793602,
					101.36042495112338
				],
				[
					-24.310286412609912,
					102.28448391488405
				],
				[
					-24.894341370599705,
					102.85987530926536
				],
				[
					-25.18645058132688,
					103.43526670364668
				],
				[
					-25.478559792054057,
					103.43526670364668
				],
				[
					-25.744351385026675,
					103.43526670364668
				],
				[
					-26.010306441463626,
					103.43526670364668
				],
				[
					-26.010306441463626,
					103.16506159713731
				],
				[
					-26.010306441463626,
					102.89044297709165
				],
				[
					-26.010306441463626,
					102.615824357046
				],
				[
					-26.284925061509284,
					102.04909652627339
				],
				[
					-26.284925061509284,
					101.46937335008784
				],
				[
					-26.284925061509284,
					101.46937335008784
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 41,
			"versionNonce": 100351223,
			"isDeleted": false,
			"id": "2oMOlgFzJvCtfT_oSTR1o",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -327.71509222317513,
			"y": 1300.804029423404,
			"strokeColor": "#1971c2",
			"backgroundColor": "#ffc9c9",
			"width": 41.70279901549907,
			"height": 55.76065694640556,
			"seed": 1394663161,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252171634,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					-0.2615415429006589,
					0.25712802936413937
				],
				[
					1.102887993718923,
					1.5909898981569768
				],
				[
					2.5936747882522013,
					3.779275294913532
				],
				[
					4.176001122800926,
					6.473153186789432
				],
				[
					5.823712843074645,
					7.994425917417402
				],
				[
					7.60219533479858,
					9.772908409141337
				],
				[
					9.602988137988177,
					11.74321527623647
				],
				[
					9.921251503005124,
					12.379578542806257
				],
				[
					10.845310466765795,
					13.940164236601277
				],
				[
					11.830504766179502,
					15.304512041488806
				],
				[
					13.513034204351925,
					16.63837391028187
				],
				[
					15.03438866671172,
					19.301765866063533
				],
				[
					16.93481490281306,
					21.965076090112916
				],
				[
					18.32981210725916,
					24.057408433317732
				],
				[
					18.99674304165569,
					25.74001960322221
				],
				[
					19.60253864039919,
					26.664160298714933
				],
				[
					20.177930034780502,
					27.239551693096246
				],
				[
					20.46562573197116,
					27.81494308747756
				],
				[
					20.753321429161815,
					28.102638784668443
				],
				[
					21.023689999135286,
					28.372843891177354
				],
				[
					21.311385696325942,
					28.93082642660943
				],
				[
					22.326984200101833,
					30.613437596513904
				],
				[
					22.675651769481192,
					31.659603768116312
				],
				[
					25.90143977423122,
					37.295824017624
				],
				[
					27.89340555034778,
					40.46480846852546
				],
				[
					29.34937462698258,
					43.032247370755385
				],
				[
					30.36497313075847,
					44.71485854066009
				],
				[
					30.940364525139785,
					45.2902499350414
				],
				[
					31.22806022233044,
					45.865641329422715
				],
				[
					31.515755919521098,
					46.153337026613144
				],
				[
					32.069406673148706,
					46.7069060485087
				],
				[
					34.99000839002679,
					49.62750776538678
				],
				[
					36.03617456162897,
					50.32492463587755
				],
				[
					38.3202495484727,
					52.609081354453565
				],
				[
					39.941807114456424,
					54.57930648981642
				],
				[
					40.865866078217095,
					55.18526555202425
				],
				[
					41.15356177540775,
					55.76065694640556
				],
				[
					41.44125747259841,
					55.76065694640556
				],
				[
					41.44125747259841,
					55.76065694640556
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 38,
			"versionNonce": 1488384727,
			"isDeleted": false,
			"id": "GgFdqZrKDy_sBGWruZsHL",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -228.76084946673723,
			"y": 1134.4722717022378,
			"strokeColor": "#1971c2",
			"backgroundColor": "#ffc9c9",
			"width": 123.77012166416739,
			"height": 113.52210669600072,
			"seed": 32268729,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252168910,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					-0.5230830858010904,
					0
				],
				[
					-1.5169409488235033,
					1.0461661716024082
				],
				[
					-4.4069749978748405,
					4.341589612149846
				],
				[
					-7.418952791303809,
					8.20374088346989
				],
				[
					-11.11976562334712,
					13.225338507161268
				],
				[
					-15.26519907832153,
					17.806647289725788
				],
				[
					-20.670445452755075,
					23.203148368818802
				],
				[
					-25.88819923362189,
					27.941382077123762
				],
				[
					-32.46155552403525,
					33.49480808195699
				],
				[
					-39.60163964522121,
					38.542559859938365
				],
				[
					-48.1890292794335,
					43.904161489400394
				],
				[
					-60.78225457009694,
					53.206295121320636
				],
				[
					-69.86640967235599,
					60.01512053207671
				],
				[
					-78.73266797668589,
					66.63645334926605
				],
				[
					-87.03219845024319,
					73.25778616645516
				],
				[
					-95.11383212587134,
					79.18611562669003
				],
				[
					-99.6123466637614,
					83.20077831021399
				],
				[
					-104.2024007416669,
					87.33746646984764
				],
				[
					-108.07321557659566,
					90.75491538650454
				],
				[
					-110.3661175905122,
					93.03907210508032
				],
				[
					-112.15326364584485,
					94.81755459680426
				],
				[
					-113.72692641678464,
					96.0598769255821
				],
				[
					-114.31098137477466,
					96.63526831996342
				],
				[
					-114.6030905855016,
					96.9229640171543
				],
				[
					-114.87329569201097,
					97.18883734185897
				],
				[
					-114.87329569201097,
					97.45037888475963
				],
				[
					-114.87329569201097,
					97.71633394119681
				],
				[
					-116.27695646006555,
					100.13559321302705
				],
				[
					-117.86794635822253,
					102.82947110490318
				],
				[
					-118.69621573189602,
					104.88690399847701
				],
				[
					-120.69700853508539,
					108.05588844937847
				],
				[
					-122.8633898276239,
					111.7349606406683
				],
				[
					-123.1860667061776,
					112.3713239072381
				],
				[
					-123.47801245344021,
					112.9467153016194
				],
				[
					-123.77012166416739,
					113.52210669600072
				],
				[
					-123.77012166416739,
					113.52210669600072
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 4,
			"versionNonce": 840322041,
			"isDeleted": false,
			"id": "dv096utuH2pIXPOTOGwUb",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -742.2626877706812,
			"y": 1382.0300873529864,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 0,
			"height": 0.27461862004565774,
			"seed": 883115191,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252164178,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					0,
					0.27461862004565774
				],
				[
					0,
					0.27461862004565774
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 29,
			"versionNonce": 1589346457,
			"isDeleted": false,
			"id": "kP3ZsTSi3mpBXf0hdn8jj",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 253.99101086032556,
			"y": 1129.233228655534,
			"strokeColor": "#1971c2",
			"backgroundColor": "#ffc9c9",
			"width": 63.02239307337004,
			"height": 93.78997321417933,
			"seed": 2140660921,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160946,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					-1.3346226593378105,
					3.560425756795894
				],
				[
					-2.7638936045516402,
					7.597297892132474
				],
				[
					-6.393532625154421,
					15.48195016227669
				],
				[
					-9.768412282621739,
					21.802723622424082
				],
				[
					-13.143428320904604,
					27.70167122059206
				],
				[
					-16.020108859777793,
					33.418755001446925
				],
				[
					-18.318671122242677,
					38.40122352024105
				],
				[
					-21.693550779709994,
					44.30010292800148
				],
				[
					-26.25780752813239,
					52.966694603144106
				],
				[
					-30.05464942839467,
					58.86557401090454
				],
				[
					-33.72056574588942,
					64.18626695184844
				],
				[
					-37.80830792536358,
					69.50695989279257
				],
				[
					-41.76880680408544,
					73.85293914619456
				],
				[
					-45.020125442815925,
					76.85693117622782
				],
				[
					-47.87866733324336,
					80.0792007012817
				],
				[
					-50.63546913539494,
					82.82863793940282
				],
				[
					-53.04668195136628,
					85.23255438175079
				],
				[
					-54.95955926792794,
					87.13827170550508
				],
				[
					-56.792517426675204,
					88.67296502100976
				],
				[
					-59.58205062451884,
					91.16055109359536
				],
				[
					-60.45843374416995,
					91.74248803283467
				],
				[
					-61.52765933677256,
					92.80441725181413
				],
				[
					-62.30598465016328,
					93.30991274403118
				],
				[
					-62.793273303526576,
					93.78997321417933
				],
				[
					-63.02239307337004,
					93.78997321417933
				],
				[
					-63.02239307337004,
					93.78997321417933
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 35,
			"versionNonce": 489501047,
			"isDeleted": false,
			"id": "pOZcnHLpg8Wdf17tbYWNZ",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 942.4195459831772,
			"y": 994.4744585003057,
			"strokeColor": "#1971c2",
			"backgroundColor": "#ffc9c9",
			"width": 144.7600526801166,
			"height": 4.83333609717306,
			"seed": 1171632889,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160946,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					2.371116856248591,
					0
				],
				[
					7.353653565450486,
					0
				],
				[
					14.147327502938651,
					0
				],
				[
					21.5446229293118,
					0
				],
				[
					29.043658443960794,
					0
				],
				[
					37.09558178417228,
					0
				],
				[
					44.49287721054543,
					0
				],
				[
					51.23554472308024,
					0
				],
				[
					60.74592450299724,
					0
				],
				[
					64.11725825926487,
					0
				],
				[
					74.23125952806686,
					0
				],
				[
					77.60259328433449,
					0
				],
				[
					84.3452607968693,
					0
				],
				[
					93.56078525392832,
					0
				],
				[
					99.69983127757814,
					0
				],
				[
					103.73670341291427,
					0
				],
				[
					108.16635229655367,
					0
				],
				[
					112.09766568078385,
					0
				],
				[
					115.53091632723499,
					0
				],
				[
					120.51345303643711,
					0
				],
				[
					123.4991018468013,
					0
				],
				[
					127.43068799266211,
					0.7091802399914968
				],
				[
					129.96900772856998,
					1.3419872233686192
				],
				[
					132.24574906057387,
					1.9238559722001582
				],
				[
					133.35861651409869,
					2.1638862072741176
				],
				[
					133.8896834092002,
					2.4293514644170955
				],
				[
					137.7481694380158,
					3.036723425725313
				],
				[
					140.73409101001062,
					3.6949654311712266
				],
				[
					142.87608809641597,
					4.302337392479444
				],
				[
					144.27999220996844,
					4.593305862098987
				],
				[
					144.7600526801166,
					4.83333609717306
				],
				[
					144.7600526801166,
					4.83333609717306
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 31,
			"versionNonce": 2089944441,
			"isDeleted": false,
			"id": "VTNEcJtCYaW-AtpJCNSLw",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 536.6776190849787,
			"y": 1096.24359588969,
			"strokeColor": "#1971c2",
			"backgroundColor": "#ffc9c9",
			"width": 61.105833474793144,
			"height": 4.247853256733833,
			"seed": 1853107385,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160946,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					0.6581738150384808,
					0
				],
				[
					3.6440953870335306,
					0
				],
				[
					7.077209652669353,
					0
				],
				[
					10.979473923222713,
					0
				],
				[
					13.56893646489948,
					0
				],
				[
					17.00205073053553,
					0
				],
				[
					20.435301376986672,
					0
				],
				[
					25.104980495700147,
					0
				],
				[
					26.374140363654305,
					0
				],
				[
					30.232899154100323,
					0
				],
				[
					31.502059022054482,
					0
				],
				[
					35.36081781250073,
					0
				],
				[
					39.39768994783708,
					0
				],
				[
					42.38347513901681,
					0
				],
				[
					47.02410514405369,
					1.1565093144477032
				],
				[
					50.457219409689515,
					2.1857753281428813
				],
				[
					53.443004600869244,
					2.8440173335889085
				],
				[
					55.58513806808992,
					3.451389294897126
				],
				[
					56.64713547747715,
					3.982319809183082
				],
				[
					57.127195947625296,
					3.982319809183082
				],
				[
					57.84728665284729,
					3.982319809183082
				],
				[
					58.07272414067552,
					3.982319809183082
				],
				[
					58.84368489003555,
					3.982319809183082
				],
				[
					59.37475178513682,
					4.247853256733833
				],
				[
					60.14571253449685,
					4.247853256733833
				],
				[
					60.86580323971907,
					4.247853256733833
				],
				[
					61.105833474793144,
					4.247853256733833
				],
				[
					61.105833474793144,
					4.247853256733833
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 46,
			"versionNonce": 1368779415,
			"isDeleted": false,
			"id": "SmNtw4r-4RsiiJlX4r8iR",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 496.20333898050853,
			"y": 1044.2370904172496,
			"strokeColor": "#1971c2",
			"backgroundColor": "#ffc9c9",
			"width": 109.37386803595473,
			"height": 50.23907829548443,
			"seed": 1990545753,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160946,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					2.1493616504358215,
					0
				],
				[
					6.080811415481094,
					-1.0619974093872315
				],
				[
					12.2197210583156,
					-2.302108163665025
				],
				[
					17.202257767517494,
					-3.836869669577254
				],
				[
					22.29008046619515,
					-4.680589583944084
				],
				[
					25.2760020381902,
					-5.026110379716783
				],
				[
					30.47661167118963,
					-5.397066197558615
				],
				[
					33.46239686236936,
					-5.397066197558615
				],
				[
					36.44831843436441,
					-5.397066197558615
				],
				[
					38.98677455108805,
					-5.717083780854864
				],
				[
					43.41642343472745,
					-6.458995416538301
				],
				[
					46.90054412531663,
					-6.458995416538301
				],
				[
					52.1956656633763,
					-6.910006773009854
				],
				[
					58.840138988835406,
					-6.910006773009854
				],
				[
					61.05496343065511,
					-7.280962590851459
				],
				[
					64.04088500265016,
					-7.946500969920407
				],
				[
					67.05571930750648,
					-8.855683675671116
				],
				[
					67.58678620260775,
					-9.124831214829328
				],
				[
					68.91418067873042,
					-10.4631361561826
				],
				[
					69.97617808811788,
					-11.266896491642228
				],
				[
					71.46000135948475,
					-12.75801613663225
				],
				[
					72.57286881300979,
					-14.169080242992322
				],
				[
					74.15843217265251,
					-16.39842924165032
				],
				[
					75.32230605113091,
					-18.151400052175404
				],
				[
					76.5369135929318,
					-20.30076170261134
				],
				[
					77.40975081138276,
					-22.053732513136538
				],
				[
					78.57362468986116,
					-23.806635133254076
				],
				[
					79.68649214338643,
					-25.21776743002181
				],
				[
					81.33029011119743,
					-27.163444332683184
				],
				[
					82.4431575647227,
					-28.574508439043257
				],
				[
					83.92698083608957,
					-30.065628084033165
				],
				[
					84.45791135037553,
					-30.600240880334468
				],
				[
					87.73841548359792,
					-33.54606649260688
				],
				[
					91.08792830940388,
					-36.55735489626329
				],
				[
					94.41193792273339,
					-39.4922700433051
				],
				[
					96.73954929887486,
					-41.827109602661835
				],
				[
					100.64181356942822,
					-44.8929503324714
				],
				[
					104.07492783506427,
					-46.95864235266981
				],
				[
					106.71894270289408,
					-48.62794353295749
				],
				[
					108.12271043563123,
					-49.4826421029627
				],
				[
					109.13383780088066,
					-49.99543396880267
				],
				[
					109.37386803595473,
					-50.23907829548443
				],
				[
					109.37386803595473,
					-50.23907829548443
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 46,
			"versionNonce": 721743449,
			"isDeleted": false,
			"id": "Y60Fc2OknT9_Vz3VkYFjD",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1331.0603983742462,
			"y": 608.5928477840573,
			"strokeColor": "#e03131",
			"backgroundColor": "#ffc9c9",
			"width": 382.05677133976724,
			"height": 222.56076679181388,
			"seed": 1953128343,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160946,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					1.2691161374964395,
					0
				],
				[
					9.845849167374126,
					0
				],
				[
					25.607809868299228,
					3.959465248306401
				],
				[
					39.28251253098006,
					8.707502908485822
				],
				[
					54.622910358423724,
					15.09996783902318
				],
				[
					70.9961846635806,
					22.310495607504322
				],
				[
					89.07310427965012,
					29.672823960584992
				],
				[
					107.57174489481031,
					37.88270557768021
				],
				[
					127.8961037909985,
					46.34139784047068
				],
				[
					154.01007373357197,
					55.59277378096726
				],
				[
					171.04130869760274,
					59.84738047839346
				],
				[
					195.57813381643018,
					67.5765602442566
				],
				[
					204.95181991545542,
					70.25418024354553
				],
				[
					221.57398392911182,
					76.00576208097641
				],
				[
					244.58442254466854,
					86.86788453712279
				],
				[
					258.9548778867643,
					94.35252304873256
				],
				[
					273.32533322886,
					102.4780446534487
				],
				[
					285.20372897377865,
					110.21149381075361
				],
				[
					296.5002224777327,
					118.5267661462193
				],
				[
					306.6118807937646,
					128.02695273241113
				],
				[
					315.53427640482414,
					138.71624389796648
				],
				[
					324.4568301414929,
					149.40553506352182
				],
				[
					331.5914576176742,
					158.1846688728656
				],
				[
					340.43811106204294,
					169.62450324133965
				],
				[
					342.87957046435304,
					173.04428578627267
				],
				[
					350.87440125326566,
					183.5142567322033
				],
				[
					353.31586065557576,
					186.93403927713632
				],
				[
					363.1955487032669,
					200.1027399911518
				],
				[
					369.781954693191,
					208.88187380049555
				],
				[
					373.8173202337971,
					213.89548342091985
				],
				[
					377.2412140445631,
					218.1796596072212
				],
				[
					379.0207596477753,
					220.29640807153646
				],
				[
					379.94421320408946,
					221.21986162785072
				],
				[
					380.5008153476215,
					221.7764637713825
				],
				[
					380.77911641938726,
					222.05476484314852
				],
				[
					381.04049805099476,
					222.05476484314852
				],
				[
					381.2977684167695,
					222.05476484314852
				],
				[
					381.5464999996602,
					222.05476484314852
				],
				[
					381.5464999996602,
					222.30776581748114
				],
				[
					381.80377036543496,
					222.30776581748114
				],
				[
					381.80377036543496,
					222.56076679181388
				],
				[
					382.05677133976724,
					222.56076679181388
				],
				[
					382.05677133976724,
					222.56076679181388
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 49,
			"versionNonce": 650805175,
			"isDeleted": false,
			"id": "l8BtXsTnjBTsiauLACgF0",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1295.5643616753723,
			"y": 631.4514858150143,
			"strokeColor": "#e03131",
			"backgroundColor": "#ffc9c9",
			"width": 87.84193828830394,
			"height": 201.66288631193504,
			"seed": 1317734807,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160946,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					0.26565102304948596,
					0
				],
				[
					0.5143826059402272,
					0
				],
				[
					1.4082666733793303,
					0
				],
				[
					3.8919456132816777,
					0.6747219734234022
				],
				[
					6.679225722382853,
					3.4619230197201887
				],
				[
					9.984999703257017,
					7.197877719764506
				],
				[
					13.409051639631798,
					11.482053906065858
				],
				[
					16.49566352649026,
					16.83302451320185
				],
				[
					20.400259188488235,
					23.67251054026326
				],
				[
					26.257231744289584,
					34.90994412927125
				],
				[
					28.33183973381756,
					39.577812105709086
				],
				[
					32.7803874906308,
					50.03521206572759
				],
				[
					36.9296034696863,
					59.370948018603144
				],
				[
					39.94885384712916,
					67.94768104848072
				],
				[
					43.76062977666879,
					78.97425413794338
				],
				[
					46.598510080636515,
					86.09204123677068
				],
				[
					49.347840043587894,
					92.50980626474131
				],
				[
					52.67480285606234,
					99.13843179225728
				],
				[
					56.09031600955359,
					106.46707939063003
				],
				[
					58.928038187912534,
					113.58478742665284
				],
				[
					60.669633644974965,
					118.26530545180731
				],
				[
					62.84117263279404,
					123.46447547434366
				],
				[
					64.76824942916392,
					128.91664647121274
				],
				[
					65.62418335045322,
					131.48460636068933
				],
				[
					67.7620415835645,
					136.6205261396426
				],
				[
					72.46359031471002,
					146.94723528385748
				],
				[
					74.69426828027963,
					152.72403815591713
				],
				[
					75.94662310322656,
					157.2823250853471
				],
				[
					76.73930678093257,
					161.3218809545906
				],
				[
					77.50257909537231,
					164.78380397431079
				],
				[
					77.89899999702993,
					168.24564793122659
				],
				[
					78.29526277307832,
					171.70757095094677
				],
				[
					78.69168367473594,
					175.68814596804896
				],
				[
					79.42538650030065,
					178.63133792758265
				],
				[
					79.42538650030065,
					180.25900388339107
				],
				[
					79.42538650030065,
					181.15296701363468
				],
				[
					79.70368757206643,
					181.98787022893248
				],
				[
					79.95241915495717,
					182.23660181182322
				],
				[
					79.95241915495717,
					182.7384134318512
				],
				[
					80.34884005661479,
					184.7286614090001
				],
				[
					83.00535028710783,
					190.50554334386425
				],
				[
					85.0209774244945,
					194.54509921310773
				],
				[
					86.91848473198934,
					199.47861821259482
				],
				[
					87.53406772766266,
					200.76892318169143
				],
				[
					87.84193828830394,
					201.66288631193504
				],
				[
					87.84193828830394,
					201.66288631193504
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 26,
			"versionNonce": 1625799481,
			"isDeleted": false,
			"id": "mpQJdPvgocXhcs-hwZulu",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1278.1394304050411,
			"y": -4.812241365718933,
			"strokeColor": "#e03131",
			"backgroundColor": "#ffc9c9",
			"width": 92.47269855458671,
			"height": 348.40735295774186,
			"seed": 178267739,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160946,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					0,
					-0.3414586690427086
				],
				[
					0,
					-0.7227541828070798
				],
				[
					0,
					-4.251160429581887
				],
				[
					0,
					-6.99421173755843
				],
				[
					0,
					-9.68604424517855
				],
				[
					0,
					-20.97694423485791
				],
				[
					0,
					-26.258171649385417
				],
				[
					4.9226958120325435,
					-46.07984738731545
				],
				[
					12.30958501899022,
					-72.90711681843868
				],
				[
					23.634630875573748,
					-106.82534461001569
				],
				[
					28.96707709045768,
					-126.04377669930363
				],
				[
					40.246595124502164,
					-170.09763598363224
				],
				[
					46.89365721520062,
					-191.15994488575086
				],
				[
					57.96830004781964,
					-233.28456268998798
				],
				[
					69.9478083534018,
					-273.56530368139454
				],
				[
					76.35015839795278,
					-291.7138319410152
				],
				[
					81.52325723395006,
					-312.96963408892464
				],
				[
					86.1272582882093,
					-327.66373881339655
				],
				[
					89.66135551280149,
					-340.354619346151
				],
				[
					90.2361442723568,
					-343.82611581475203
				],
				[
					91.68165263797096,
					-347.1894837048228
				],
				[
					92.47269855458671,
					-348.40735295774186
				],
				[
					92.47269855458671,
					-348.40735295774186
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 4,
			"versionNonce": 1324314839,
			"isDeleted": false,
			"id": "tl8fF8JmHlkXBuNEOZTvP",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 2510.7561483820346,
			"y": -586.2646767725281,
			"strokeColor": "#e03131",
			"backgroundColor": "#ffc9c9",
			"width": 0.0001,
			"height": 0.0001,
			"seed": 698497147,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160947,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					0.0001,
					0.0001
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 55,
			"versionNonce": 1855843353,
			"isDeleted": false,
			"id": "I7_axiLRFlg17uiXBa9A6",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1689.4449592844558,
			"y": 343.29163631551705,
			"strokeColor": "#e03131",
			"backgroundColor": "#ffc9c9",
			"width": 715.568373218729,
			"height": 458.04334136248826,
			"seed": 68698811,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160947,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					0.32337242752146267,
					0
				],
				[
					1.6387856920150625,
					0
				],
				[
					7.56362627083854,
					0
				],
				[
					22.142789952309613,
					0
				],
				[
					25.4806511109623,
					0
				],
				[
					42.74545020744108,
					0.8659803991249646
				],
				[
					49.87608627871714,
					3.003526953927121
				],
				[
					65.7158543386613,
					9.810790597681603
				],
				[
					78.9028723152096,
					18.64050213559517
				],
				[
					86.81727545657986,
					24.97092847097076
				],
				[
					101.06210493332537,
					38.54708953826537
				],
				[
					110.76327775896607,
					49.64040806882838
				],
				[
					120.64531990847445,
					63.47965178902177
				],
				[
					128.84472925715136,
					76.19531334579358
				],
				[
					137.74569234689125,
					95.70727676911577
				],
				[
					140.59575441996094,
					102.8379128403916
				],
				[
					144.42689555279867,
					120.6124345768618
				],
				[
					145.92865902976246,
					137.16471815507327
				],
				[
					145.92865902976246,
					150.8066498855926
				],
				[
					140.70537219200196,
					171.61758390760235
				],
				[
					125.79187430580578,
					197.63536210156587
				],
				[
					115.50972728834722,
					214.07802790773633
				],
				[
					90.31956327329408,
					245.50544315192997
				],
				[
					62.56434339247835,
					276.4560210877447
				],
				[
					45.95725092824614,
					291.9504931657592
				],
				[
					11.635926502166512,
					321.8322978241729
				],
				[
					-6.078305459680905,
					336.21963040457194
				],
				[
					-44.39519767665979,
					363.29522009873256
				],
				[
					-85.00310132929872,
					388.0743174686313
				],
				[
					-106.78963352247456,
					398.38934981770217
				],
				[
					-147.04127941597972,
					415.78020935202835
				],
				[
					-187.61081684840383,
					427.514791849032
				],
				[
					-231.8963967530226,
					437.46808555036705
				],
				[
					-255.97394038185848,
					440.90460270385665
				],
				[
					-304.12902763952934,
					448.92314272866577
				],
				[
					-328.20657126836477,
					451.2141541643256
				],
				[
					-376.3616585260356,
					455.796177035645
				],
				[
					-422.58199210718067,
					458.04334136248826
				],
				[
					-442.8667608233927,
					458.04334136248826
				],
				[
					-481.66049034875095,
					458.04334136248826
				],
				[
					-516.9793365004048,
					458.04334136248826
				],
				[
					-525.2609591781127,
					458.04334136248826
				],
				[
					-543.9946364199427,
					458.04334136248826
				],
				[
					-559.4123760575285,
					458.04334136248826
				],
				[
					-566.1812734810687,
					458.04334136248826
				],
				[
					-568.0995844917886,
					458.04334136248826
				],
				[
					-569.2724946526287,
					457.2705360695983
				],
				[
					-569.6397141889665,
					456.9033165332605
				],
				[
					-569.6397141889665,
					456.55802055133086
				],
				[
					-569.6397141889665,
					455.82358147865534
				],
				[
					-569.6397141889665,
					455.01789085415294
				],
				[
					-569.6397141889665,
					455.01789085415294
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 57,
			"versionNonce": 1134116343,
			"isDeleted": false,
			"id": "PZC-J3SzDzjS_vyfQ4zOf",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 478.8366129328065,
			"y": 459.24227132178794,
			"strokeColor": "#1971c2",
			"backgroundColor": "#ffc9c9",
			"width": 142.3093903320912,
			"height": 69.65673685873037,
			"seed": 1132976117,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160947,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					0,
					-0.8042729166792242
				],
				[
					1.7559958680831187,
					-3.552205382000011
				],
				[
					3.364541701441567,
					-4.631271545211462
				],
				[
					4.7854238542415715,
					-5.616505868143577
				],
				[
					8.733063420275812,
					-7.332288090392581
				],
				[
					13.793280521049383,
					-9.376481753619146
				],
				[
					17.874965573196732,
					-10.06011373279648
				],
				[
					21.822605139230973,
					-10.06011373279648
				],
				[
					26.500792604581875,
					-11.23301173628704
				],
				[
					29.664266076853664,
					-11.86972779532482
				],
				[
					38.84638187560881,
					-14.061371493275828
				],
				[
					42.0098553478806,
					-15.33480361135139
				],
				[
					50.173225452175075,
					-16.702067569706173
				],
				[
					60.374086945390445,
					-19.624259166974184
				],
				[
					64.4557719975378,
					-20.991523125328854
				],
				[
					71.89529647682116,
					-23.042419062861086
				],
				[
					79.14045500124007,
					-25.683115139291317
				],
				[
					82.30392847351186,
					-26.956547257366765
				],
				[
					88.63087541805544,
					-28.866695434480107
				],
				[
					94.1334426230028,
					-31.313025556046227
				],
				[
					97.29691609527458,
					-32.586457674121675
				],
				[
					102.79948330022194,
					-35.66280158041991
				],
				[
					108.49641646003352,
					-38.83967960130303
				],
				[
					111.6598899323053,
					-40.743125504110594
				],
				[
					117.59810496712066,
					-45.374397049322056
				],
				[
					122.66502434220001,
					-49.18128885493729
				],
				[
					124.27357017555846,
					-50.26035501814863
				],
				[
					127.63140960269448,
					-53.095417049443085
				],
				[
					130.3123193249587,
					-55.78973132031865
				],
				[
					131.92086515831716,
					-56.86879748352999
				],
				[
					134.50794304030228,
					-58.93309796967344
				],
				[
					136.46500713755518,
					-60.414300591224446
				],
				[
					137.44353918618162,
					-61.39953491415656
				],
				[
					138.86442133898163,
					-62.344555591254675
				],
				[
					139.74912154732874,
					-63.242660348213235
				],
				[
					140.19147165150252,
					-63.242660348213235
				],
				[
					140.19147165150252,
					-63.69171272669246
				],
				[
					140.6070126584534,
					-64.11395600794913
				],
				[
					140.6070126584534,
					-64.52949701490002
				],
				[
					141.04936276262697,
					-64.95174029615669
				],
				[
					141.04936276262697,
					-65.40079267463591
				],
				[
					141.04936276262697,
					-65.82303595589258
				],
				[
					141.49171286680053,
					-66.2720883343718
				],
				[
					141.49171286680053,
					-66.72114071285102
				],
				[
					141.49171286680053,
					-67.17019309133036
				],
				[
					141.49171286680053,
					-67.59243637258692
				],
				[
					141.90725387375142,
					-68.01467965384359
				],
				[
					141.90725387375142,
					-68.43022066079448
				],
				[
					141.90725387375142,
					-68.83905939343981
				],
				[
					142.3093903320912,
					-68.83905939343981
				],
				[
					142.3093903320912,
					-69.24789812608515
				],
				[
					142.3093903320912,
					-69.65673685873037
				],
				[
					142.3093903320912,
					-69.65673685873037
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 68,
			"versionNonce": 1276838137,
			"isDeleted": false,
			"id": "CF9uO8LJp-euiSY8cYhM0",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 569.9607343925672,
			"y": 505.9370164093252,
			"strokeColor": "#1971c2",
			"backgroundColor": "#ffc9c9",
			"width": 107.8865094982184,
			"height": 113.6772744983092,
			"seed": 1732910357,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160947,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					0.9249138541813409,
					0
				],
				[
					1.3203480382151156,
					0
				],
				[
					2.7412301910153474,
					0
				],
				[
					3.7197622396417955,
					0
				],
				[
					5.1406443924418,
					0
				],
				[
					7.1915403299738045,
					0
				],
				[
					9.778618211958928,
					0
				],
				[
					11.387164045317377,
					0.5361819444528919
				],
				[
					13.344228142570273,
					2.003980017392564
				],
				[
					15.683321875245838,
					3.1701757465774563
				],
				[
					17.828049653057178,
					5.31490352438891
				],
				[
					20.562577569766745,
					8.049431441098363
				],
				[
					21.051843594080083,
					9.027963489724812
				],
				[
					22.472725746880087,
					9.959579618211592
				],
				[
					23.3574259552272,
					10.844279826558818
				],
				[
					23.799776059400756,
					11.286629930732488
				],
				[
					24.73139218788765,
					12.707512083532492
				],
				[
					27.606667865016107,
					16.219503819698616
				],
				[
					28.585199913642555,
					17.198035868325064
				],
				[
					33.20306691024257,
					23.136250903140308
				],
				[
					38.26998628532192,
					28.203170278219773
				],
				[
					40.16672991382393,
					30.736629965759448
				],
				[
					43.672019375684386,
					34.342453542204794
				],
				[
					45.13981744862417,
					36.29951763945769
				],
				[
					46.11834949725062,
					36.788783663770914
				],
				[
					47.00304970559773,
					37.67348387211814
				],
				[
					48.96011380285063,
					39.14128194505781
				],
				[
					50.56865963620908,
					40.21364583396348
				],
				[
					54.080651372375314,
					43.08892151109194
				],
				[
					58.370106927997995,
					46.74166100767695
				],
				[
					59.97865276135667,
					47.81402489658262
				],
				[
					61.93571685860957,
					49.77108899383552
				],
				[
					62.82041706695668,
					50.655789202182746
				],
				[
					63.262767171130236,
					51.0981393063563
				],
				[
					64.14746737947758,
					51.98283951470353
				],
				[
					65.03216758782469,
					52.867539723050754
				],
				[
					65.47451769199824,
					53.30988982722431
				],
				[
					67.43158178925114,
					55.26695392447721
				],
				[
					68.89937986219093,
					56.73475199741688
				],
				[
					69.87791191081737,
					57.2240180217301
				],
				[
					70.76261211916449,
					58.10871823007733
				],
				[
					71.20496222333804,
					58.551068334250886
				],
				[
					71.62050323028916,
					58.966609341201774
				],
				[
					71.62050323028916,
					59.37544807384711
				],
				[
					71.62050323028916,
					59.77758453218678
				],
				[
					72.4783943414136,
					60.63547564331134
				],
				[
					75.35367001854206,
					64.14746737947746
				],
				[
					77.88712970608162,
					66.68092706701714
				],
				[
					83.90577203256498,
					76.48635437619862
				],
				[
					88.71800498402922,
					83.38969691102898
				],
				[
					90.61474861253123,
					86.55317038330077
				],
				[
					93.4431083695199,
					89.91771208474245
				],
				[
					94.95782236259925,
					91.96860802227457
				],
				[
					95.4001724667728,
					92.41095812644812
				],
				[
					96.28487267511991,
					93.29565833479535
				],
				[
					96.77413869943325,
					94.2741903834218
				],
				[
					98.52343229321059,
					98.95237784877281
				],
				[
					101.58637165089749,
					103.82493126898817
				],
				[
					102.8531014946675,
					106.98840474125996
				],
				[
					104.99782927247884,
					110.20549640797697
				],
				[
					106.51254326555795,
					112.25639234550908
				],
				[
					107.00180928987129,
					113.23492439413553
				],
				[
					107.8865094982184,
					113.6772744983092
				],
				[
					107.8865094982184,
					113.6772744983092
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 45,
			"versionNonce": 1473013527,
			"isDeleted": false,
			"id": "dIjYDBgro7TXsoKvqqPl9",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -2312.7510844541857,
			"y": 41.932166887146195,
			"strokeColor": "#2f9e44",
			"backgroundColor": "#ffc9c9",
			"width": 184.35184534614473,
			"height": 48.78434678422104,
			"seed": 1013643067,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160947,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					-4.001624446513233,
					0
				],
				[
					-10.552760313242288,
					0
				],
				[
					-11.295444074783518,
					0
				],
				[
					-17.846579941512573,
					0
				],
				[
					-20.51802451660842,
					0
				],
				[
					-24.818939434190725,
					0
				],
				[
					-29.441314487364707,
					0
				],
				[
					-32.11275906246101,
					0
				],
				[
					-35.37169974743256,
					0
				],
				[
					-40.88086138155177,
					0
				],
				[
					-42.510331724037314,
					0
				],
				[
					-50.4249019589688,
					0
				],
				[
					-57.2974979612909,
					0
				],
				[
					-62.54062362112654,
					2.095033297481905
				],
				[
					-73.02687494079737,
					5.232040827573883
				],
				[
					-83.51312626046865,
					8.369048357665633
				],
				[
					-87.39281755210186,
					9.33342876444317
				],
				[
					-96.51563450357025,
					11.339783403830552
				],
				[
					-103.06677037029931,
					13.190950391552633
				],
				[
					-105.73821494539561,
					14.077736972497405
				],
				[
					-111.08110409558776,
					15.851310134386722
				],
				[
					-116.42399324577946,
					17.624883296276266
				],
				[
					-120.30368453741266,
					18.589263703053575
				],
				[
					-126.85482040414172,
					20.440430690775656
				],
				[
					-135.97763735561057,
					23.49984439503487
				],
				[
					-139.85732864724378,
					24.46422480181218
				],
				[
					-147.61671123050974,
					27.357366022144333
				],
				[
					-154.1678470972388,
					30.095319590811187
				],
				[
					-156.83929167233464,
					30.98210617175596
				],
				[
					-161.1402065899165,
					32.67808550781274
				],
				[
					-165.44112150749834,
					34.37406484386952
				],
				[
					-168.11256608259464,
					35.260851424814064
				],
				[
					-171.3715067675662,
					37.688429690150315
				],
				[
					-175.67242168514804,
					40.27119560715187
				],
				[
					-177.30189202763404,
					41.88958111737588
				],
				[
					-179.7516399574938,
					44.317159382712134
				],
				[
					-182.12379406152104,
					45.857951067103386
				],
				[
					-182.12379406152104,
					46.58954999638286
				],
				[
					-183.6091615846035,
					48.05274785494157
				],
				[
					-184.35184534614473,
					48.78434678422104
				],
				[
					-184.35184534614473,
					48.78434678422104
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 38,
			"versionNonce": 652376537,
			"isDeleted": false,
			"id": "uQSyKVHmhsZ49x3a_-Qqh",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -2323.658559399806,
			"y": -22.714574863723556,
			"strokeColor": "#2f9e44",
			"backgroundColor": "#ffc9c9",
			"width": 123.01946844155555,
			"height": 37.156357741583406,
			"seed": 1120491707,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160947,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					-0.665089935708238,
					0
				],
				[
					-2.29456027819424,
					0
				],
				[
					-4.666714382221471,
					0
				],
				[
					-6.296184724707018,
					0
				],
				[
					-7.781552247789477,
					0
				],
				[
					-11.040492932761481,
					0
				],
				[
					-11.78317669430271,
					0
				],
				[
					-17.29233832842192,
					0
				],
				[
					-21.59325324600377,
					0
				],
				[
					-24.264697821099617,
					0
				],
				[
					-29.607586971291312,
					0
				],
				[
					-37.36696955455773,
					0
				],
				[
					-40.038414129653574,
					0
				],
				[
					-49.16123108112242,
					-2.992904710688208
				],
				[
					-58.605508168183405,
					-8.247115202785835
				],
				[
					-62.48519945981661,
					-10.186960848602212
				],
				[
					-69.03633532654567,
					-13.911464488570118
				],
				[
					-73.33725024412797,
					-17.325592825207195
				],
				[
					-74.96672058661352,
					-18.955063167693197
				],
				[
					-77.33887469064075,
					-20.518024516608193
				],
				[
					-78.82424221372321,
					-22.003392039690652
				],
				[
					-80.45371255620921,
					-22.82366962706442
				],
				[
					-82.82586666023599,
					-24.386630975979415
				],
				[
					-85.19802076426322,
					-25.94959232489464
				],
				[
					-86.82749110674922,
					-26.769869912268405
				],
				[
					-92.17038025694092,
					-29.452399319626238
				],
				[
					-98.72151612366997,
					-33.17690295959392
				],
				[
					-107.84433307513882,
					-35.205427263505044
				],
				[
					-111.72402436677203,
					-36.18089250254411
				],
				[
					-118.27516023350108,
					-37.156357741583406
				],
				[
					-119.90463057598708,
					-37.156357741583406
				],
				[
					-122.27678468001432,
					-37.156357741583406
				],
				[
					-123.01946844155555,
					-37.156357741583406
				],
				[
					-123.01946844155555,
					-37.156357741583406
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 49,
			"versionNonce": 167603255,
			"isDeleted": false,
			"id": "EtIy_eOWlKa7qTT-IIqlr",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -2430.502632308741,
			"y": -601.4779529132077,
			"strokeColor": "#2f9e44",
			"backgroundColor": "#ffc9c9",
			"width": 89.31695245977289,
			"height": 97.67520399249781,
			"seed": 394851573,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160947,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					-1.4769269736998467,
					0
				],
				[
					-4.364773011660418,
					0
				],
				[
					-9.24110732147301,
					0
				],
				[
					-13.143824967059572,
					-0.7838439245891777
				],
				[
					-16.58448724657228,
					-1.5099309284191804
				],
				[
					-23.672086522594782,
					-5.594170324963102
				],
				[
					-28.42465600220976,
					-9.505138959229384
				],
				[
					-28.977472243761895,
					-10.057955200781748
				],
				[
					-34.03532830453241,
					-13.671888242572095
				],
				[
					-37.53374750480407,
					-17.830386537234972
				],
				[
					-39.70375752761447,
					-20.000396560045147
				],
				[
					-42.12954819950119,
					-22.426187231931863
				],
				[
					-43.342443535444545,
					-23.639082567875107
				],
				[
					-46.65934098475873,
					-26.295900922798637
				],
				[
					-49.43992416988067,
					-29.67880628155217
				],
				[
					-50.65281950582403,
					-30.891701617495528
				],
				[
					-54.811317800486904,
					-34.39012081776741
				],
				[
					-58.194223159240664,
					-37.77302617652094
				],
				[
					-59.52263233670192,
					-39.761514448373646
				],
				[
					-62.90553769545568,
					-43.14441980712718
				],
				[
					-65.3313283673424,
					-45.57021047901378
				],
				[
					-66.54422370328575,
					-46.78310581495714
				],
				[
					-68.36769220154065,
					-48.606574313212036
				],
				[
					-69.47332468464538,
					-49.71220679631688
				],
				[
					-70.68622002058873,
					-50.32277995862853
				],
				[
					-71.84960942445286,
					-52.08849153612425
				],
				[
					-73.07075574907594,
					-54.514282208010854
				],
				[
					-74.39916492653765,
					-56.50277047986356
				],
				[
					-76.51141802858865,
					-61.3791047896766
				],
				[
					-79.16823638351207,
					-65.3560813333819
				],
				[
					-82.43562790074748,
					-70.54595321303066
				],
				[
					-83.5990173046116,
					-72.31166479052638
				],
				[
					-84.20959046692269,
					-73.52456012646962
				],
				[
					-84.72940275375595,
					-74.04437241330254
				],
				[
					-84.72940275375595,
					-75.15000489640738
				],
				[
					-84.72940275375595,
					-75.66981718324018
				],
				[
					-85.24921504058875,
					-76.74244571162546
				],
				[
					-85.24921504058875,
					-77.95534104756882
				],
				[
					-85.97530204441864,
					-82.05608242147241
				],
				[
					-86.70138904824898,
					-87.8317744973931
				],
				[
					-87.36971913131947,
					-89.8202627692458
				],
				[
					-88.7641362182203,
					-94.69659707905873
				],
				[
					-89.31695245977289,
					-96.46230865655446
				],
				[
					-89.31695245977289,
					-97.67520399249781
				],
				[
					-89.31695245977289,
					-97.67520399249781
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 64,
			"versionNonce": 805820089,
			"isDeleted": false,
			"id": "sOguDkoAkC4fFIAAyaWAI",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -1811.3071868266493,
			"y": -391.77907561388906,
			"strokeColor": "#2f9e44",
			"backgroundColor": "#ffc9c9",
			"width": 24.257906718866707,
			"height": 314.8412260471139,
			"seed": 128911867,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160947,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					-0.536314264192697,
					0
				],
				[
					-0.536314264192697,
					-2.2030139775297357
				],
				[
					-0.536314264192697,
					-5.09086001549008
				],
				[
					-0.536314264192697,
					-12.896295306662864
				],
				[
					-0.536314264192697,
					-17.929398401393655
				],
				[
					-0.536314264192697,
					-30.404893285382286
				],
				[
					-0.536314264192697,
					-48.8045980415294
				],
				[
					-0.536314264192697,
					-57.94669349884384
				],
				[
					-0.536314264192697,
					-81.15672465536488
				],
				[
					-0.536314264192697,
					-102.6422991777896
				],
				[
					-0.536314264192697,
					-115.10954307309828
				],
				[
					-0.536314264192697,
					-134.99442579162508
				],
				[
					-0.536314264192697,
					-149.1696243436703
				],
				[
					-0.536314264192697,
					-156.82654183860507
				],
				[
					-1.4356720303003385,
					-169.40104858675227
				],
				[
					-3.118873720997044,
					-179.46725477621396
				],
				[
					-3.9027176455863355,
					-183.3699724218004
				],
				[
					-5.412648574005516,
					-190.1605361053471
				],
				[
					-7.99520803081009,
					-200.35050712500708
				],
				[
					-8.836808876158557,
					-205.38361021973788
				],
				[
					-10.577767487614665,
					-216.70396668854232
				],
				[
					-13.399605616135887,
					-229.7487797914431
				],
				[
					-13.399605616135887,
					-232.63662582940344
				],
				[
					-15.982165072940461,
					-243.9569822982079
				],
				[
					-18.391453767467283,
					-252.89280303852502
				],
				[
					-19.175297692056574,
					-256.79552068411147
				],
				[
					-21.469072545065046,
					-263.58608436765815
				],
				[
					-22.195159548894935,
					-268.4624186774711
				],
				[
					-22.92124655272505,
					-271.3502647154314
				],
				[
					-23.589576635795765,
					-275.3272412591368
				],
				[
					-24.257906718866707,
					-278.5286248669328
				],
				[
					-24.257906718866707,
					-279.74152020287613
				],
				[
					-24.257906718866707,
					-282.16731087476285
				],
				[
					-24.257906718866707,
					-284.59310154664945
				],
				[
					-24.257906718866707,
					-285.8059968825928
				],
				[
					-24.257906718866707,
					-288.2317875544794
				],
				[
					-24.257906718866707,
					-291.43317116227547
				],
				[
					-24.257906718866707,
					-293.4216594341282
				],
				[
					-24.257906718866707,
					-295.8474501060148
				],
				[
					-24.257906718866707,
					-297.6131616835106
				],
				[
					-24.257906718866707,
					-298.165977925063
				],
				[
					-24.257906718866707,
					-299.2716104081678
				],
				[
					-24.257906718866707,
					-299.7914226950006
				],
				[
					-24.257906718866707,
					-300.3029839931536
				],
				[
					-24.257906718866707,
					-300.81454529130656
				],
				[
					-24.257906718866707,
					-301.3343575781395
				],
				[
					-24.257906718866707,
					-301.88717381969184
				],
				[
					-23.11101929236247,
					-303.65288539718756
				],
				[
					-21.964131865858235,
					-305.4185969746833
				],
				[
					-21.361809692226416,
					-306.63149231062664
				],
				[
					-20.09940842420383,
					-309.8328759184227
				],
				[
					-18.952520997699594,
					-311.5985874959184
				],
				[
					-18.40795574482695,
					-312.1514037374708
				],
				[
					-17.863390491954533,
					-313.2570362205756
				],
				[
					-17.863390491954533,
					-313.809852462128
				],
				[
					-17.360080182481397,
					-314.32141376028096
				],
				[
					-16.86502086168821,
					-314.32141376028096
				],
				[
					-16.353459563535353,
					-314.8412260471139
				],
				[
					-16.353459563535353,
					-314.8412260471139
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 57,
			"versionNonce": 370199895,
			"isDeleted": false,
			"id": "M7zk8eq5bwdlDi8IaygLa",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -1897.9920738975381,
			"y": -391.96059736484665,
			"strokeColor": "#2f9e44",
			"backgroundColor": "#ffc9c9",
			"width": 151.40564227591926,
			"height": 253.44561928007738,
			"seed": 1809921083,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160947,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					-0.6105731623115389,
					-1.7079546567364332
				],
				[
					-6.080978657076457,
					-7.962204076090529
				],
				[
					-8.424259442164157,
					-11.864921721676865
				],
				[
					-10.94081098952961,
					-16.89802481640777
				],
				[
					-14.612500952079245,
					-22.789230733846807
				],
				[
					-18.110920152351127,
					-26.947729028509684
				],
				[
					-18.77925023542207,
					-28.936217300362387
				],
				[
					-19.94263963928597,
					-30.14911263630563
				],
				[
					-21.708351216781693,
					-31.914824213801467
				],
				[
					-23.878361239591868,
					-34.08483423661164
				],
				[
					-29.175495972079034,
					-39.38196896909881
				],
				[
					-36.00731459902522,
					-46.99763152063417
				],
				[
					-39.36546699173914,
					-51.197384758696444
				],
				[
					-47.45143589802797,
					-61.07381820852072
				],
				[
					-52.921841392792885,
					-68.10366056378416
				],
				[
					-55.265122177880585,
					-72.0063782093705
				],
				[
					-59.77841298577869,
					-77.30351294185778
				],
				[
					-64.46497455595409,
					-85.10894823303045
				],
				[
					-66.80825534104201,
					-89.0116658786169
				],
				[
					-70.59545914511,
					-95.80222956216357
				],
				[
					-75.28202071528563,
					-103.60766485333625
				],
				[
					-77.62530150037333,
					-106.73478956301335
				],
				[
					-82.31186307054895,
					-112.98903898236733
				],
				[
					-86.99842464072458,
					-120.01888133763077
				],
				[
					-89.34170542581228,
					-123.14600604730776
				],
				[
					-94.14378083750648,
					-130.23360532333038
				],
				[
					-99.18513492091711,
					-138.50934696925674
				],
				[
					-102.54328731363103,
					-142.709100207319
				],
				[
					-107.22984888380665,
					-149.73894256258245
				],
				[
					-111.91641045398228,
					-156.76878491784578
				],
				[
					-114.25969123906998,
					-159.89590962752288
				],
				[
					-118.04689504313797,
					-166.68647331106956
				],
				[
					-122.97273528503024,
					-174.06285719088817
				],
				[
					-125.31601607011794,
					-177.9655748364745
				],
				[
					-130.17584840257132,
					-186.90139557679174
				],
				[
					-134.0868170368376,
					-193.93123793205518
				],
				[
					-135.65450488601596,
					-197.83395557764152
				],
				[
					-137.70900106730778,
					-202.71028988745456
				],
				[
					-139.64798340708103,
					-205.9116734952505
				],
				[
					-140.8608787430244,
					-207.12456883119387
				],
				[
					-142.02426814688852,
					-208.8902804086896
				],
				[
					-142.63484130920006,
					-210.6559919861853
				],
				[
					-143.2454144715116,
					-211.86888732212867
				],
				[
					-144.4665607961349,
					-214.2946779940154
				],
				[
					-146.7025787283842,
					-223.9730877155224
				],
				[
					-148.4435373398403,
					-235.29344418432686
				],
				[
					-150.06898210977783,
					-244.46854359636075
				],
				[
					-150.06898210977783,
					-247.3563896343211
				],
				[
					-150.79506911360818,
					-252.23272394413402
				],
				[
					-151.40564227591926,
					-253.44561928007738
				],
				[
					-151.40564227591926,
					-250.7145420270349
				],
				[
					-151.40564227591926,
					-250.7145420270349
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 51,
			"versionNonce": 707696537,
			"isDeleted": false,
			"id": "Ps1QyeVxH3qYcSFrR7_8z",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -2340.377082958339,
			"y": -561.1388692572419,
			"strokeColor": "#2f9e44",
			"backgroundColor": "#ffc9c9",
			"width": 377.5982459463312,
			"height": 158.5509984727014,
			"seed": 51459643,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160947,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					0.9818676529062031,
					0
				],
				[
					3.391156347433025,
					0
				],
				[
					5.37139363060578,
					0
				],
				[
					10.231225963058932,
					0
				],
				[
					12.211463246231688,
					0
				],
				[
					18.985524952418928,
					0
				],
				[
					25.759586658605713,
					0
				],
				[
					30.784438764656443,
					0
				],
				[
					43.45795737696244,
					0
				],
				[
					60.24046835185163,
					0
				],
				[
					69.37431282048647,
					2.029743215252097
				],
				[
					89.24269356165314,
					7.219615094900746
				],
				[
					110.83553093691671,
					12.640514657586323
				],
				[
					121.57006720944901,
					15.85840024274205
				],
				[
					134.59837833499023,
					19.678608001529597
				],
				[
					149.89571134749986,
					23.490564771637196
				],
				[
					154.92056345355104,
					25.16551547365418
				],
				[
					169.0792600282366,
					29.88508099854937
				],
				[
					180.38311451968093,
					32.50889539875334
				],
				[
					188.03178102593574,
					34.41487378380714
				],
				[
					201.9594499175846,
					39.010674478503915
				],
				[
					217.25678293009423,
					43.779745935478445
				],
				[
					220.13637797937463,
					44.497581950628614
				],
				[
					233.75050930118778,
					49.15113956608457
				],
				[
					245.0543637926321,
					53.51591257774464
				],
				[
					252.70303029888737,
					57.33612033653219
				],
				[
					264.00688479033215,
					62.53424320486067
				],
				[
					276.0780812290059,
					69.94363103939895
				],
				[
					282.7696330483941,
					74.72095348505331
				],
				[
					296.5652861211647,
					85.58750557646397
				],
				[
					303.2568379405527,
					90.36482802211833
				],
				[
					312.11014879407094,
					97.30390950190292
				],
				[
					321.68129566273956,
					105.13409775911532
				],
				[
					325.57576231964595,
					107.4691275555233
				],
				[
					332.5891026975496,
					112.92303107292832
				],
				[
					341.8632139737422,
					118.84724094508692
				],
				[
					346.0547162231246,
					122.1971423491209
				],
				[
					355.01528992948147,
					131.15771605547775
				],
				[
					363.9758636358383,
					141.9170052940499
				],
				[
					366.3108934322463,
					145.03587901504704
				],
				[
					371.8225538704105,
					151.38914029855982
				],
				[
					375.3622280140819,
					155.7126583668204
				],
				[
					375.9645501877137,
					156.9173027140838
				],
				[
					377.05368069345855,
					158.00643321982886
				],
				[
					377.5982459463312,
					158.5509984727014
				],
				[
					377.5982459463312,
					158.5509984727014
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 43,
			"versionNonce": 1197148791,
			"isDeleted": false,
			"id": "Ykhj1j8Ng6cn2pl3WSSyq",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -2063.8864522953386,
			"y": -372.5212680350337,
			"strokeColor": "#2f9e44",
			"backgroundColor": "#ffc9c9",
			"width": 225.73879929301847,
			"height": 14.827026657756278,
			"seed": 1249185083,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160947,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					-0.4950593207931888,
					0
				],
				[
					-2.4835475926461186,
					0
				],
				[
					-8.366502521404982,
					0
				],
				[
					-17.302323261721995,
					0
				],
				[
					-22.3354263564529,
					0
				],
				[
					-33.655782825257575,
					0
				],
				[
					-41.93152447118382,
					0
				],
				[
					-46.964627565914725,
					0
				],
				[
					-57.030833755376534,
					0
				],
				[
					-68.59046889589763,
					0
				],
				[
					-73.62357199062853,
					0
				],
				[
					-83.68977818009034,
					0
				],
				[
					-96.37979876975578,
					-0.9571146868668166
				],
				[
					-101.41290186448668,
					-1.798715532215283
				],
				[
					-116.7267368543562,
					-5.627174279682663
				],
				[
					-130.6709077233645,
					-8.383004498764876
				],
				[
					-134.57362536895062,
					-9.166848423354054
				],
				[
					-147.14813211709816,
					-10.965563955569337
				],
				[
					-157.21433830655997,
					-11.807164800917803
				],
				[
					-161.11705595214607,
					-12.591008725506981
				],
				[
					-169.03800508483755,
					-13.432609570855448
				],
				[
					-174.81369716075778,
					-14.15869657468545
				],
				[
					-177.70154319871835,
					-14.15869657468545
				],
				[
					-182.5778775085314,
					-14.827026657756278
				],
				[
					-186.55485405223635,
					-14.827026657756278
				],
				[
					-188.54334232408928,
					-14.827026657756278
				],
				[
					-192.52031886779469,
					-14.827026657756278
				],
				[
					-196.49729541149964,
					-14.827026657756278
				],
				[
					-198.48578368335257,
					-14.827026657756278
				],
				[
					-203.3621179931656,
					-14.827026657756278
				],
				[
					-208.23845230297866,
					-14.827026657756278
				],
				[
					-211.12629834093923,
					-14.827026657756278
				],
				[
					-216.00263265075182,
					-13.449111548215228
				],
				[
					-220.87896696056487,
					-12.071196438674178
				],
				[
					-222.8674552324178,
					-11.411117344283184
				],
				[
					-224.6331668099133,
					-10.866552091410654
				],
				[
					-225.73879929301847,
					-10.866552091410654
				],
				[
					-225.73879929301847,
					-10.866552091410654
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 68,
			"versionNonce": 931806329,
			"isDeleted": false,
			"id": "8nTuiUGkICmPXaixIPFDg",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 196.20637243086924,
			"y": 472.35013525482134,
			"strokeColor": "#1971c2",
			"backgroundColor": "#ffc9c9",
			"width": 161.70969465676967,
			"height": 19.153799494689792,
			"seed": 1948912501,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160947,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					0.6612054506590539,
					0
				],
				[
					3.7768055341641684,
					0
				],
				[
					6.273517315852587,
					0
				],
				[
					10.616314715780845,
					0
				],
				[
					13.113026497469264,
					0
				],
				[
					19.5558124086906,
					0
				],
				[
					25.998598319911707,
					0
				],
				[
					29.21999127552249,
					0
				],
				[
					36.46680301474498,
					0
				],
				[
					40.46048393672527,
					0
				],
				[
					43.68187689233605,
					0
				],
				[
					49.39998162963502,
					0
				],
				[
					54.39340519301186,
					0
				],
				[
					57.61479814862241,
					0
				],
				[
					61.95759554855067,
					0
				],
				[
					67.67570028584964,
					0
				],
				[
					70.17241206753806,
					0.9997426413964376
				],
				[
					75.89051680483703,
					2.5707667921622033
				],
				[
					80.88394036821387,
					3.5652197899532894
				],
				[
					83.38065214990229,
					4.062446288848832
				],
				[
					88.3740757132789,
					5.056899286640032
				],
				[
					93.36749927665574,
					6.051352284431118
				],
				[
					95.86421105834415,
					6.548578783326661
				],
				[
					100.93168963219455,
					7.543031781117861
				],
				[
					105.92511319557138,
					8.537484778908947
				],
				[
					108.4218249772598,
					9.03471127780449
				],
				[
					112.76462237718806,
					10.494652912859578
				],
				[
					117.7580459405649,
					11.489105910650665
				],
				[
					120.25475772225309,
					12.488848552047102
				],
				[
					125.24818128562993,
					13.483301549838302
				],
				[
					129.59097868555818,
					14.440727042392496
				],
				[
					132.0876904672466,
					15.440469683788933
				],
				[
					136.43048786717486,
					16.397895176343127
				],
				[
					138.2765734854147,
					16.858094170001777
				],
				[
					140.3183759170497,
					17.6674096416084
				],
				[
					141.93700686026295,
					18.09058113003016
				],
				[
					142.28612333821093,
					18.09058113003016
				],
				[
					142.98435629410687,
					18.09058113003016
				],
				[
					143.68258925000282,
					18.439697607978133
				],
				[
					144.45487721637255,
					18.439697607978133
				],
				[
					146.49667964800756,
					18.439697607978133
				],
				[
					148.0412555807468,
					18.825841591162998
				],
				[
					149.58583151348626,
					18.825841591162998
				],
				[
					150.358119479856,
					18.825841591162998
				],
				[
					151.05635243575193,
					18.825841591162998
				],
				[
					151.4054689136999,
					18.825841591162998
				],
				[
					151.75458539164788,
					18.825841591162998
				],
				[
					152.06667436435873,
					18.825841591162998
				],
				[
					153.18807880867644,
					18.825841591162998
				],
				[
					154.4575932739417,
					18.825841591162998
				],
				[
					157.0759668585515,
					18.825841591162998
				],
				[
					157.848254824921,
					18.825841591162998
				],
				[
					159.89005725655602,
					18.825841591162998
				],
				[
					161.01146170087372,
					18.825841591162998
				],
				[
					161.3605781788217,
					18.825841591162998
				],
				[
					161.70969465676967,
					18.825841591162998
				],
				[
					161.70969465676967,
					19.153799494689792
				],
				[
					161.70969465676967,
					19.153799494689792
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 47,
			"versionNonce": 178299799,
			"isDeleted": false,
			"id": "inIHm-J4HgV50oGXzcfU5",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 385.5309642278737,
			"y": 1132.5602707119142,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 19.616413094993504,
			"height": 101.5880226749905,
			"seed": 2054992693,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160947,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					0,
					0.9532814139035963
				],
				[
					0,
					2.9975404459412403
				],
				[
					0,
					4.268582331145808
				],
				[
					0,
					5.539624216350603
				],
				[
					0,
					9.236237699154572
				],
				[
					0,
					11.857761587389405
				],
				[
					0,
					15.888023565059484
				],
				[
					0,
					18.08586682489272
				],
				[
					0,
					22.433889273863997
				],
				[
					0,
					24.28219601526598
				],
				[
					0,
					27.978809498069722
				],
				[
					0,
					31.67542298087369
				],
				[
					0,
					33.52372972227545
				],
				[
					0,
					37.294487315049764
				],
				[
					0.5348967933571203,
					44.550018076426795
				],
				[
					1.5358422779556804,
					47.04973378399632
				],
				[
					3.071684555911588,
					52.12330930910525
				],
				[
					4.570454778882095,
					57.12274072424384
				],
				[
					5.031207462268867,
					58.971047465645825
				],
				[
					5.878568719072064,
					61.513131236055415
				],
				[
					6.763002030860434,
					64.78606409045756
				],
				[
					7.260826769232153,
					67.28577979802708
				],
				[
					9.559294178310893,
					75.34630375336724
				],
				[
					13.2347236296946,
					85.16510231657412
				],
				[
					14.309813224263507,
					88.39037110028107
				],
				[
					17.111401379569088,
					95.64590186165833
				],
				[
					18.493659429729405,
					99.34251534446207
				],
				[
					18.88026800314583,
					100.11573249129515
				],
				[
					19.616413094993504,
					101.23848615655925
				],
				[
					19.616413094993504,
					101.5880226749905
				],
				[
					19.616413094993504,
					101.5880226749905
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 72,
			"versionNonce": 1742619993,
			"isDeleted": false,
			"id": "mWgWAyqsPlpf5Gag7e3Zp",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -902.6064343328925,
			"y": 984.0231384021725,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 38.72440943590516,
			"height": 138.5170854480441,
			"seed": 770346107,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160947,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					0,
					-0.3177604713011988
				],
				[
					0,
					-1.8747867806770273
				],
				[
					0,
					-3.151124673736831
				],
				[
					0,
					-5.7038004598564385
				],
				[
					0,
					-7.557403209113318
				],
				[
					0,
					-12.641570749932384
				],
				[
					-0.5401928012121289,
					-18.377147256918875
				],
				[
					-1.1174576574092043,
					-22.412705242444076
				],
				[
					-3.0028364537963625,
					-32.3162399313311
				],
				[
					-6.074521009707837,
					-42.145630510248
				],
				[
					-6.6888579208900865,
					-47.060325799706334
				],
				[
					-8.844333117883139,
					-53.82862383842178
				],
				[
					-10.613199741459766,
					-61.9738839194423
				],
				[
					-12.228482137240917,
					-65.20444871100437
				],
				[
					-14.315109232118743,
					-70.94002521799086
				],
				[
					-15.707959297988964,
					-74.64723071650474
				],
				[
					-16.13693593424557,
					-75.92356860956454
				],
				[
					-17.455641890145444,
					-79.05350925188122
				],
				[
					-18.313595162658658,
					-81.60618503800083
				],
				[
					-19.166252427316863,
					-82.88252293106063
				],
				[
					-20.52203043820191,
					-86.01246357337732
				],
				[
					-22.06846473186772,
					-91.74804008036381
				],
				[
					-23.074706224321517,
					-94.25305179578822
				],
				[
					-25.081893201373987,
					-99.33721933660729
				],
				[
					-27.09437618628158,
					-104.34724276745601
				],
				[
					-28.02117756091002,
					-106.200845516713
				],
				[
					-29.339883516810005,
					-109.33078615902969
				],
				[
					-30.54737330775447,
					-110.96195657837575
				],
				[
					-30.939277889026016,
					-111.74046973306372
				],
				[
					-31.27292638389224,
					-112.07411822792994
				],
				[
					-31.27292638389224,
					-112.42895075421632
				],
				[
					-31.27292638389224,
					-112.75730324122753
				],
				[
					-31.27292638389224,
					-113.44578426238013
				],
				[
					-31.27292638389224,
					-113.80061678866639
				],
				[
					-31.627758910178613,
					-114.93396246964073
				],
				[
					-32.41156807272148,
					-116.49098877901656
				],
				[
					-32.41156807272148,
					-117.26950193370442
				],
				[
					-32.80347265399291,
					-118.40284761467865
				],
				[
					-33.19537723526446,
					-119.53619329565288
				],
				[
					-33.55020976155072,
					-119.89102582193925
				],
				[
					-33.55020976155072,
					-120.22467431680548
				],
				[
					-33.55020976155072,
					-120.55832281167181
				],
				[
					-33.55020976155072,
					-120.88667529868303
				],
				[
					-33.942114342822265,
					-121.66518845337089
				],
				[
					-34.40816303406393,
					-125.37239395188476
				],
				[
					-34.87421172530571,
					-129.07959945039863
				],
				[
					-35.80101309993415,
					-130.93320219965563
				],
				[
					-36.733110482417715,
					-134.6404076981695
				],
				[
					-37.97767232834735,
					-136.69525874591727
				],
				[
					-38.369576909618786,
					-137.47377190060513
				],
				[
					-38.72440943590516,
					-138.18343695317776
				],
				[
					-38.72440943590516,
					-138.5170854480441
				],
				[
					-38.72440943590516,
					-138.5170854480441
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 59,
			"versionNonce": 1075189943,
			"isDeleted": false,
			"id": "eaVG31VYj5IDLJfAmOh9o",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -594.8130498148493,
			"y": 857.5438788085886,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 154.00261241612202,
			"height": 132.0453638492097,
			"seed": 1049867835,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160947,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					0,
					0.31246446344619017
				],
				[
					-1.3557780108851603,
					3.431813090052856
				],
				[
					-2.859844241710789,
					5.433704059250317
				],
				[
					-8.701340905797679,
					11.804801508839205
				],
				[
					-21.448831812830463,
					24.65821257297239
				],
				[
					-27.269144445497204,
					30.473229197784235
				],
				[
					-35.78512507636913,
					38.43842501173401
				],
				[
					-50.32796264625358,
					50.67220315682982
				],
				[
					-56.53488385233686,
					54.11460826259281
				],
				[
					-69.28767076722465,
					63.340253946037365
				],
				[
					-78.94758909478082,
					70.19328811043306
				],
				[
					-80.80119184403782,
					71.11479347720649
				],
				[
					-86.9551529715709,
					75.56873608327817
				],
				[
					-91.96517640241962,
					78.56627652921941
				],
				[
					-93.9723633794722,
					80.06504675219003
				],
				[
					-97.37240042239489,
					82.95137103317586
				],
				[
					-100.77243746531758,
					85.83769531416158
				],
				[
					-102.1652875311878,
					87.22524937217679
				],
				[
					-107.05350278137121,
					92.10287260665007
				],
				[
					-111.75635775662874,
					96.25494276498569
				],
				[
					-114.63738602975957,
					99.13067503026139
				],
				[
					-119.52560127994286,
					103.50517751850782
				],
				[
					-124.91693727635311,
					107.80553589678391
				],
				[
					-126.92412425340558,
					109.80742686598148
				],
				[
					-130.93849820751063,
					112.80496731192261
				],
				[
					-132.94568518456322,
					114.30373753489323
				],
				[
					-136.27687412537068,
					116.77167719533259
				],
				[
					-137.05538728005854,
					117.15828576874901
				],
				[
					-137.8339004347465,
					117.54489434216543
				],
				[
					-138.96724611572074,
					118.66764800742965
				],
				[
					-141.0220971634684,
					120.2882264110657
				],
				[
					-141.80061031815637,
					121.06144355789866
				],
				[
					-145.08413518826865,
					123.91069578389931
				],
				[
					-147.9810514849645,
					127.30014081111199
				],
				[
					-149.98823846201708,
					128.7989110340826
				],
				[
					-152.15960168257516,
					130.95968223893067
				],
				[
					-153.2929473635494,
					131.69582733077846
				],
				[
					-153.64777988983576,
					132.0453638492097
				],
				[
					-154.00261241612202,
					132.0453638492097
				],
				[
					-154.00261241612202,
					132.0453638492097
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 36,
			"versionNonce": 108933689,
			"isDeleted": false,
			"id": "ENnDtsN2_yq07hWhyYEY7",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -650.2622520569071,
			"y": 797.2276453477676,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 169.1968589521739,
			"height": 0,
			"seed": 1632064091,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160947,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					-0.3177604713011988,
					0
				],
				[
					-2.8227721867255013,
					0
				],
				[
					-15.586151117323425,
					0
				],
				[
					-22.481553344559188,
					0
				],
				[
					-43.36900832475749,
					0
				],
				[
					-71.2313056500169,
					0
				],
				[
					-85.9065434162768,
					0
				],
				[
					-113.76884074153622,
					0
				],
				[
					-131.41513891446232,
					0
				],
				[
					-141.85886640456147,
					0
				],
				[
					-153.54715574059026,
					0
				],
				[
					-162.64569723551438,
					0
				],
				[
					-165.1507089509388,
					0
				],
				[
					-167.78282485488364,
					0
				],
				[
					-168.49248990745627,
					0
				],
				[
					-169.1968589521739,
					0
				],
				[
					-169.1968589521739,
					0
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 42,
			"versionNonce": 1298131415,
			"isDeleted": false,
			"id": "WMReoQRaO1nPCUUBLFhd4",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -876.1316910656484,
			"y": 601.709627356145,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 120.42062660744114,
			"height": 7.038394439321337,
			"seed": 539886869,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160947,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					-2.171363220558078,
					0
				],
				[
					-4.676374935982494,
					0
				],
				[
					-12.096081940865247,
					0
				],
				[
					-20.24134202188577,
					0
				],
				[
					-26.109318725247817,
					0
				],
				[
					-36.8919907180682,
					0
				],
				[
					-50.68279517253984,
					0
				],
				[
					-57.57819739977572,
					0
				],
				[
					-70.34157633037353,
					0
				],
				[
					-82.0775297370975,
					0
				],
				[
					-86.1130877226226,
					0
				],
				[
					-95.94247830153938,
					0
				],
				[
					-101.02664584235856,
					0
				],
				[
					-103.53165755778286,
					-0.5031207462268412
				],
				[
					-109.26723406476935,
					-2.0495550398926525
				],
				[
					-110.54357195782916,
					-2.4785316761492595
				],
				[
					-114.32492156631326,
					-3.9137498048596626
				],
				[
					-116.87759735243287,
					-5.195383705774361
				],
				[
					-118.15393524549268,
					-5.624360342031082
				],
				[
					-119.7109615548685,
					-6.016264923302515
				],
				[
					-120.42062660744114,
					-6.371097449588774
				],
				[
					-120.42062660744114,
					-7.038394439321337
				],
				[
					-120.42062660744114,
					-7.038394439321337
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 86,
			"versionNonce": 676168473,
			"isDeleted": false,
			"id": "o58U-TAsUzJrZFs5IAIs4",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1466.2116901811414,
			"y": 350.3377052804132,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 95.88955994828575,
			"height": 75.06841015642789,
			"seed": 1538921051,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160947,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					0,
					-0.19137086205751075
				],
				[
					0.25516114941001433,
					-0.9600438246552017
				],
				[
					0.765483448230043,
					-1.7287167872528926
				],
				[
					2.806772643510385,
					-3.473381146343911
				],
				[
					4.312223425029515,
					-4.379203226749496
				],
				[
					5.517859855991901,
					-5.285025307155024
				],
				[
					6.723496286954287,
					-6.493851252485001
				],
				[
					7.9291327179164455,
					-7.702677197814978
				],
				[
					9.134769148878831,
					-8.608499278220563
				],
				[
					10.755042447632604,
					-9.906631625844057
				],
				[
					11.960678878594763,
					-11.115457571174034
				],
				[
					13.903093128478531,
					-12.088259453299713
				],
				[
					15.198035961734604,
					-13.711722266420963
				],
				[
					16.92994226335486,
					-15.446818082409095
				],
				[
					18.87235651323863,
					-16.419619964534775
				],
				[
					22.336169116479596,
					-19.889811596511095
				],
				[
					24.415732484171258,
					-21.280439860795695
				],
				[
					26.14763878579197,
					-23.015535676783827
				],
				[
					28.22720215348363,
					-24.75063149277196
				],
				[
					30.443914638983188,
					-26.970533492639106
				],
				[
					33.190086509508546,
					-29.327584610314204
				],
				[
					38.682430250559264,
					-34.433997112882196
				],
				[
					41.42860212108462,
					-36.791048230557294
				],
				[
					44.17477399160998,
					-39.540409615450244
				],
				[
					46.39148647710954,
					-41.76031161531739
				],
				[
					47.5971229080717,
					-42.96913756064737
				],
				[
					50.18381906021568,
					-44.81905589387003
				],
				[
					51.915725361836394,
					-46.55415170985816
				],
				[
					53.995288729528056,
					-47.94477997414276
				],
				[
					58.202258180425815,
					-51.09283065498886
				],
				[
					59.037910944743544,
					-51.93167293367435
				],
				[
					60.54336172626245,
					-52.83749501407988
				],
				[
					62.048812507781804,
					-53.74331709448546
				],
				[
					63.25444893874419,
					-54.95214303981544
				],
				[
					64.75989972026309,
					-55.857965120221024
				],
				[
					65.96553615122548,
					-56.76378720062661
				],
				[
					67.0786766655267,
					-57.321952214961016
				],
				[
					69.11996586080704,
					-59.066616574052034
				],
				[
					70.72110207335481,
					-60.418970665925144
				],
				[
					71.48658552158486,
					-60.932482479112764
				],
				[
					72.69222195254724,
					-61.83830455951835
				],
				[
					75.10349481447201,
					-63.64994872032952
				],
				[
					76.60894559599092,
					-64.55577080073505
				],
				[
					77.8145820269533,
					-65.46159288114063
				],
				[
					79.32003280847243,
					-66.36741496154622
				],
				[
					80.52566923943482,
					-67.2732370419518
				],
				[
					82.03112002095395,
					-68.17905912235733
				],
				[
					82.79660346918399,
					-68.692570935545
				],
				[
					83.56208691741404,
					-69.20608274873268
				],
				[
					84.02775601508733,
					-69.44210681193692
				],
				[
					84.49342511276063,
					-69.67813087514122
				],
				[
					85.25890856099068,
					-70.1916426883289
				],
				[
					86.02439200922072,
					-70.70515450151657
				],
				[
					86.49006110689402,
					-70.94117856472081
				],
				[
					87.99551188841315,
					-71.5471862945696
				],
				[
					89.10865240271437,
					-72.105351308904
				],
				[
					90.22179291701559,
					-72.66351632323847
				],
				[
					91.33493343131681,
					-73.22168133757287
				],
				[
					92.44807394561803,
					-73.77984635190728
				],
				[
					93.56121445991903,
					-74.33801136624169
				],
				[
					94.3266979081493,
					-74.59636203001935
				],
				[
					94.7923670058226,
					-74.83238609322365
				],
				[
					95.46854405175918,
					-75.06841015642789
				],
				[
					95.88955994828575,
					-75.06841015642789
				],
				[
					95.88955994828575,
					-74.87384978000273
				],
				[
					94.40962528170758,
					-71.91716996121414
				],
				[
					94.40962528170758,
					-71.91716996121414
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 75,
			"versionNonce": 1871877879,
			"isDeleted": false,
			"id": "PZu50cdnzfuUykoofZiTV",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1507.4042682390218,
			"y": 365.165757575503,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 116.97862894702348,
			"height": 17.264841271955504,
			"seed": 1578740251,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160947,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					0.5741125861723049,
					0
				],
				[
					2.0795633676916623,
					0
				],
				[
					7.342262074273094,
					0
				],
				[
					12.869690473367882,
					-0.9217696522437109
				],
				[
					14.81210472325165,
					-0.9217696522437109
				],
				[
					18.961662915532088,
					-1.339596034402632
				],
				[
					23.111221107812526,
					-2.1720592843527697
				],
				[
					27.260779300092963,
					-2.1720592843527697
				],
				[
					31.4103374923734,
					-3.0045225343029642
				],
				[
					35.55989568465384,
					-3.0045225343029642
				],
				[
					39.090688089615014,
					-3.0045225343029642
				],
				[
					42.62148049457619,
					-3.0045225343029642
				],
				[
					46.152272899537365,
					-3.0045225343029642
				],
				[
					50.3018310918178,
					-3.0045225343029642
				],
				[
					53.83262349677875,
					-3.0045225343029642
				],
				[
					58.648790191892886,
					-3.0045225343029642
				],
				[
					62.79834838417355,
					-3.0045225343029642
				],
				[
					67.61451507928746,
					-3.0045225343029642
				],
				[
					75.91363146384856,
					-3.0045225343029642
				],
				[
					80.81272553252074,
					-3.0045225343029642
				],
				[
					83.76940535130939,
					-3.0045225343029642
				],
				[
					86.19662578507223,
					-3.0045225343029642
				],
				[
					88.139040034956,
					-3.329852999800778
				],
				[
					90.08145428483977,
					-3.655183465298535
				],
				[
					91.19459479914099,
					-3.935860729649562
				],
				[
					92.30773531344221,
					-4.216537994000589
				],
				[
					93.07321876167225,
					-4.474888657778251
				],
				[
					93.53888785934555,
					-4.710912720982492
				],
				[
					93.74939580760883,
					-4.710912720982492
				],
				[
					94.95503223857122,
					-5.616734801388077
				],
				[
					95.72051568680126,
					-6.1302466145757535
				],
				[
					96.18618478447434,
					-6.5991052266166434
				],
				[
					96.9516682327046,
					-6.857455890394306
				],
				[
					97.4173373303779,
					-7.326314502435196
				],
				[
					97.88300642805098,
					-7.562338565639493
				],
				[
					98.3486755257245,
					-7.7983626288437335
				],
				[
					98.55918347398756,
					-8.01206009147461
				],
				[
					98.76969142225107,
					-8.225757554105542
				],
				[
					98.98019937051413,
					-8.225757554105542
				],
				[
					100.09333988481558,
					-8.783922568439948
				],
				[
					100.85882333304562,
					-9.297434381627625
				],
				[
					102.06445976400778,
					-10.203256462033153
				],
				[
					104.00687401389177,
					-11.17605834415889
				],
				[
					107.45473904529445,
					-13.054682306690154
				],
				[
					109.39715329517821,
					-14.027484188815833
				],
				[
					112.84501832658134,
					-15.58396720021699
				],
				[
					114.35046910810024,
					-15.886971065141381
				],
				[
					115.11595255633029,
					-16.400482878329058
				],
				[
					115.88143600456033,
					-16.658833542106663
				],
				[
					116.34710510223385,
					-16.658833542106663
				],
				[
					116.55761305049691,
					-16.872531004737596
				],
				[
					116.7681209987602,
					-16.872531004737596
				],
				[
					116.97862894702348,
					-16.872531004737596
				],
				[
					116.97862894702348,
					-17.063901866795106
				],
				[
					116.97862894702348,
					-17.264841271955504
				],
				[
					116.97862894702348,
					-17.264841271955504
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 77,
			"versionNonce": 2042607609,
			"isDeleted": false,
			"id": "XMVa4Mu2IOLotF3d2OLx_",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1273.6741651506934,
			"y": 346.6404367583891,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 132.70440224041704,
			"height": 63.325284169549604,
			"seed": 1133286811,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160947,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					-0.654468529872247,
					0
				],
				[
					-2.563335075332816,
					0
				],
				[
					-5.143031863912256,
					-1.0362418389643153
				],
				[
					-10.378780102889777,
					-3.103271612477272
				],
				[
					-11.180504051983235,
					-3.103271612477272
				],
				[
					-13.089370597443803,
					-3.5832152010502227
				],
				[
					-14.998237142904372,
					-3.5832152010502227
				],
				[
					-17.114352056157713,
					-3.5832152010502227
				],
				[
					-17.47976365200293,
					-3.5832152010502227
				],
				[
					-18.281487601096387,
					-3.5832152010502227
				],
				[
					-19.083211550189844,
					-3.5832152010502227
				],
				[
					-20.992078095650413,
					-3.5832152010502227
				],
				[
					-21.79380204474387,
					-3.5832152010502227
				],
				[
					-23.108193008903754,
					-4.461293811962037
				],
				[
					-25.017059554364323,
					-5.415727084692321
				],
				[
					-28.343941247881276,
					-7.079167931450797
				],
				[
					-31.905340831269086,
					-9.457070256653083
				],
				[
					-35.4667404146569,
					-11.834972581855368
				],
				[
					-40.52796371233512,
					-14.36558423069448
				],
				[
					-44.95653409780357,
					-17.52884879174337
				],
				[
					-50.017757395481794,
					-20.059460440582484
				],
				[
					-54.44632778095024,
					-22.590072089421597
				],
				[
					-60.83830375603543,
					-26.14056386397823
				],
				[
					-65.89952705371365,
					-28.038522600607564
				],
				[
					-67.80839359917422,
					-28.99295587333785
				],
				[
					-76.48010161998059,
					-32.936128765817784
				],
				[
					-78.38896816544116,
					-33.41607235439068
				],
				[
					-82.54484333012942,
					-35.19949909829239
				],
				[
					-85.87172502364638,
					-36.31209559907512
				],
				[
					-89.19860671716333,
					-37.9755364458336
				],
				[
					-92.52548841068028,
					-39.638977292592074
				],
				[
					-95.10518519925995,
					-41.18788614662293
				],
				[
					-97.68488198783939,
					-42.22412798558719
				],
				[
					-102.11345237330784,
					-44.7547396344263
				],
				[
					-105.49487311098096,
					-47.18172709936903
				],
				[
					-108.0745698995604,
					-48.730635953399826
				],
				[
					-110.65426668813984,
					-50.27954480743068
				],
				[
					-112.72129646165286,
					-51.82845366146154
				],
				[
					-114.78832623516587,
					-53.37736251549239
				],
				[
					-116.85535600867888,
					-54.92627136952319
				],
				[
					-118.76422255413945,
					-55.88070464225348
				],
				[
					-120.07861351829933,
					-56.75878325316535
				],
				[
					-122.14564329181235,
					-58.30769210719615
				],
				[
					-123.46003425597246,
					-59.18577071810802
				],
				[
					-124.77442522013234,
					-60.06384932901989
				],
				[
					-125.5761491692258,
					-60.46743825577437
				],
				[
					-126.89054013338568,
					-61.34551686668624
				],
				[
					-127.69226408247914,
					-61.74910579344072
				],
				[
					-128.4939880315726,
					-62.15269472019526
				],
				[
					-129.29571198066606,
					-62.556283646949794
				],
				[
					-130.0974359297595,
					-62.959872573704274
				],
				[
					-130.89915987885297,
					-62.959872573704274
				],
				[
					-131.2645714746982,
					-62.959872573704274
				],
				[
					-131.6299830705434,
					-63.325284169549604
				],
				[
					-131.99539466638885,
					-63.325284169549604
				],
				[
					-132.36080626223406,
					-63.325284169549604
				],
				[
					-132.70440224041704,
					-63.325284169549604
				],
				[
					-132.70440224041704,
					-63.325284169549604
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 65,
			"versionNonce": 1295163415,
			"isDeleted": false,
			"id": "pesxdMEB9w-aKkymgQ5yt",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1664.4192952790545,
			"y": 416.91325766662965,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 159.61861631161514,
			"height": 26.074958028816923,
			"seed": 58492757,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160947,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					-1.2591529027999968,
					0
				],
				[
					-3.095417552716526,
					0
				],
				[
					-6.295764513999984,
					0
				],
				[
					-9.496111475283442,
					0
				],
				[
					-13.493921941673307,
					0
				],
				[
					-17.4917324080634,
					0
				],
				[
					-21.48954287445349,
					0
				],
				[
					-26.358267431946842,
					0
				],
				[
					-30.356077898336935,
					0
				],
				[
					-34.35388836472703,
					0
				],
				[
					-39.22261292222038,
					0
				],
				[
					-44.09133747971373,
					0
				],
				[
					-48.96006203720708,
					0
				],
				[
					-59.641875829293895,
					0
				],
				[
					-65.45496506388736,
					0
				],
				[
					-70.32368962138071,
					0
				],
				[
					-75.19241417887406,
					0
				],
				[
					-80.06113873636741,
					0
				],
				[
					-84.92986329386099,
					0
				],
				[
					-89.79858785135434,
					-0.6085905696866121
				],
				[
					-94.66731240884769,
					-1.8257717090600636
				],
				[
					-99.53603696634104,
					-3.0429528484334014
				],
				[
					-103.53384743273114,
					-4.186683401810001
				],
				[
					-108.40257199022449,
					-5.403864541183339
				],
				[
					-112.40038245661458,
					-6.547595094560052
				],
				[
					-116.39819292300467,
					-8.263190924625064
				],
				[
					-118.2344575729212,
					-8.724880322318427
				],
				[
					-121.43480453420466,
					-9.795160289698401
				],
				[
					-125.43261500059475,
					-10.938890843075114
				],
				[
					-129.43042546698484,
					-12.654486673140127
				],
				[
					-131.26669011690137,
					-13.572618998098505
				],
				[
					-136.13541467439495,
					-16.00698127684518
				],
				[
					-137.97167932431148,
					-16.92511360180356
				],
				[
					-140.44801336648493,
					-17.916696512758563
				],
				[
					-143.64836032776816,
					-19.516869993400178
				],
				[
					-146.12994084036995,
					-21.006867595046856
				],
				[
					-148.61152135297175,
					-22.003696976430206
				],
				[
					-151.09310186557332,
					-23.000526357813555
				],
				[
					-152.92936651549007,
					-23.918658682771934
				],
				[
					-154.76563116540683,
					-24.380348080465296
				],
				[
					-157.3731269682885,
					-25.6867192171203
				],
				[
					-158.1443581212534,
					-25.6867192171203
				],
				[
					-158.91558927421852,
					-26.074958028816923
				],
				[
					-159.26710279291683,
					-26.074958028816923
				],
				[
					-159.61861631161514,
					-26.074958028816923
				],
				[
					-159.61861631161514,
					-26.074958028816923
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 102,
			"versionNonce": 1289244889,
			"isDeleted": false,
			"id": "1BCPE09l-XaFJ7EkQwkwu",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1488.5785924030324,
			"y": 430.3652078448765,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 90.76393841016784,
			"height": 91.53516956313274,
			"seed": 460890741,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160947,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					0.6243299809718792,
					0
				],
				[
					1.390314663508434,
					0
				],
				[
					2.1562993460452162,
					0
				],
				[
					2.5025663943151812,
					0
				],
				[
					3.268551076851736,
					0
				],
				[
					4.034535759388518,
					0
				],
				[
					4.380802807658483,
					0
				],
				[
					5.1467874901952655,
					0.3829923412682774
				],
				[
					5.91277217273182,
					0.7659846825366685
				],
				[
					6.6787568552686025,
					1.148977023804946
				],
				[
					7.444741537805157,
					1.531969365073337
				],
				[
					8.284176806338564,
					2.791122267873334
				],
				[
					10.760510848511785,
					3.782705178828337
				],
				[
					12.743676670422019,
					5.2674563100466685
				],
				[
					13.509661352958574,
					6.033440992583337
				],
				[
					16.174868330552044,
					8.163507986486707
				],
				[
					17.43402123335204,
					9.002943255020114
				],
				[
					21.58397934216373,
					13.11617607083349
				],
				[
					23.567145164073736,
					15.099341892743496
				],
				[
					25.550310985983742,
					16.584093023961827
				],
				[
					27.53347680789375,
					18.567258845871834
				],
				[
					31.49980845171376,
					22.03517579900017
				],
				[
					33.48297427362377,
					24.01834162091029
				],
				[
					35.466140095533774,
					25.503092752128623
				],
				[
					37.44930591744378,
					26.987843883346954
				],
				[
					38.934057048662225,
					28.97100970525696
				],
				[
					40.91722287057223,
					30.455760836475292
				],
				[
					42.90038869248224,
					32.4389266583853
				],
				[
					44.883554514392245,
					34.42209248029542
				],
				[
					46.86672033630225,
					35.90684361151375
				],
				[
					48.351471467520696,
					37.89000943342376
				],
				[
					50.3346372894307,
					39.37476056464209
				],
				[
					51.10062197196726,
					40.14074524717876
				],
				[
					51.86660665450404,
					40.906729929715425
				],
				[
					52.63259133704082,
					41.289722270983816
				],
				[
					52.97885838531079,
					41.63598931925378
				],
				[
					53.32512543358075,
					41.982256367523746
				],
				[
					53.67139248185072,
					42.328523415793825
				],
				[
					54.05438482311911,
					43.09450809833049
				],
				[
					55.539135954337326,
					45.0776739202405
				],
				[
					57.52230177624733,
					47.060839742150506
				],
				[
					59.652368770150815,
					49.72604671974386
				],
				[
					62.501202212735734,
					53.14674543901731
				],
				[
					63.98595334395418,
					55.129911260927315
				],
				[
					66.83478678653933,
					58.55060998020065
				],
				[
					68.96485378044258,
					61.215816957794004
				],
				[
					70.44960491166103,
					63.19898277970401
				],
				[
					71.8241801638842,
					64.5735580319274
				],
				[
					73.42960011495438,
					66.59869561726407
				],
				[
					73.81259245622255,
					67.36468029980074
				],
				[
					74.15885950449274,
					67.71094734807082
				],
				[
					74.5051265527627,
					68.05721439634078
				],
				[
					74.85139360103267,
					68.40348144461075
				],
				[
					74.85139360103267,
					68.72876261116744
				],
				[
					75.19766064930263,
					69.0750296594374
				],
				[
					75.5439276975726,
					69.42129670770748
				],
				[
					75.96364533183942,
					70.68044961050748
				],
				[
					76.34663767310758,
					71.44643429304415
				],
				[
					77.18607294164099,
					72.70558719584415
				],
				[
					77.56906528290938,
					73.47157187838081
				],
				[
					77.91533233117934,
					73.81783892665078
				],
				[
					78.29832467244773,
					74.58382360918756
				],
				[
					78.6445917207177,
					74.93009065745753
				],
				[
					78.99085876898766,
					75.27635770572749
				],
				[
					79.33712581725763,
					75.62262475399757
				],
				[
					79.33712581725763,
					75.96889180226754
				],
				[
					79.6833928655276,
					76.3151588505375
				],
				[
					80.06638520679599,
					77.08114353307417
				],
				[
					80.97927106132602,
					78.91216171256258
				],
				[
					81.81870632985942,
					80.17131461536258
				],
				[
					83.30345746107764,
					82.15448043727258
				],
				[
					84.78820859229609,
					84.13764625918259
				],
				[
					86.27295972351453,
					86.1208120810926
				],
				[
					87.95183026058112,
					88.6391178866927
				],
				[
					88.33482260184951,
					89.40510256922937
				],
				[
					89.10080728438606,
					90.17108725176604
				],
				[
					89.44707433265626,
					90.517354300036
				],
				[
					89.79334138092622,
					90.86362134830608
				],
				[
					90.13960842919619,
					91.20988839657605
				],
				[
					90.44915018446773,
					91.20988839657605
				],
				[
					90.44915018446773,
					91.53516956313274
				],
				[
					90.76393841016784,
					91.53516956313274
				],
				[
					90.76393841016784,
					91.53516956313274
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 93,
			"versionNonce": 1211401527,
			"isDeleted": false,
			"id": "QP47a1kVAdgzTJo6cGV9Z",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1424.099470838815,
			"y": 423.36116982305145,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 11.174982012350256,
			"height": 113.16636713915125,
			"seed": 13005301,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160947,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					0,
					1.5686946580716494
				],
				[
					0,
					4.763795148926647
				],
				[
					0,
					8.756359144888393
				],
				[
					0,
					13.619837231953397
				],
				[
					0,
					19.427679996118513
				],
				[
					0,
					29.154636170248637
				],
				[
					0,
					34.01811425731364
				],
				[
					0,
					38.88159234437876
				],
				[
					0,
					39.64757702691543
				],
				[
					0,
					43.640141022877174
				],
				[
					0,
					46.11647506505051
				],
				[
					0,
					49.311575555905506
				],
				[
					0,
					51.142593735393916
				],
				[
					0,
					52.97361191488221
				],
				[
					0,
					54.80463009437062
				],
				[
					0,
					57.28096413654396
				],
				[
					0,
					59.11198231603237
				],
				[
					0,
					63.104546311994
				],
				[
					0,
					64.363699214794
				],
				[
					0,
					66.1947173942824
				],
				[
					0,
					68.67105143645574
				],
				[
					0,
					69.93020433925574
				],
				[
					0,
					71.76122251874415
				],
				[
					0,
					72.52720720128082
				],
				[
					0,
					73.78636010408081
				],
				[
					0,
					74.55234478661748
				],
				[
					0,
					74.89861183488745
				],
				[
					0,
					75.66459651742423
				],
				[
					0,
					76.0108635656942
				],
				[
					0,
					76.35713061396416
				],
				[
					0.346267048269965,
					76.35713061396416
				],
				[
					0.346267048269965,
					76.70339766223424
				],
				[
					0.6925340965401574,
					76.70339766223424
				],
				[
					0.6925340965401574,
					77.02867882879082
				],
				[
					1.0125687926683895,
					77.02867882879082
				],
				[
					1.0125687926683895,
					77.34871352491916
				],
				[
					1.0125687926683895,
					77.67399469147585
				],
				[
					1.4690117199334054,
					79.50501287096426
				],
				[
					1.9621799401968474,
					81.9813469131376
				],
				[
					2.381897574463437,
					83.2404998159376
				],
				[
					2.875065794726652,
					85.71683385811093
				],
				[
					3.368234014990094,
					88.19316790028438
				],
				[
					3.8246769422551097,
					90.02418607977268
				],
				[
					4.700837503786715,
					93.11435716206108
				],
				[
					5.0838298450551065,
					93.88034184459775
				],
				[
					5.466822186323498,
					94.64632652713442
				],
				[
					5.466822186323498,
					94.99259357540438
				],
				[
					5.466822186323498,
					95.33886062367446
				],
				[
					5.7763639415950365,
					95.33886062367446
				],
				[
					5.7763639415950365,
					95.68512767194443
				],
				[
					5.7763639415950365,
					95.99991589764443
				],
				[
					6.101645108151843,
					95.99991589764443
				],
				[
					6.101645108151843,
					96.34618294591439
				],
				[
					6.426926274708421,
					96.67146411247109
				],
				[
					6.426926274708421,
					96.99674527902778
				],
				[
					6.773193322978386,
					96.99674527902778
				],
				[
					6.773193322978386,
					97.34301232729774
				],
				[
					7.119460371248579,
					97.34301232729774
				],
				[
					7.119460371248579,
					97.66829349385443
				],
				[
					7.434248596948464,
					98.0145605421244
				],
				[
					8.31040915848007,
					101.1047316244128
				],
				[
					8.31040915848007,
					102.93574980390122
				],
				[
					9.643012647276919,
					107.85693906567792
				],
				[
					10.062730281543509,
					109.11609196847792
				],
				[
					10.482447915810098,
					110.37524487127791
				],
				[
					10.482447915810098,
					111.14122955381458
				],
				[
					10.482447915810098,
					111.48749660208455
				],
				[
					10.82871496408029,
					111.83376365035463
				],
				[
					10.82871496408029,
					112.18003069862459
				],
				[
					10.82871496408029,
					112.52629774689456
				],
				[
					10.82871496408029,
					112.84108597259467
				],
				[
					11.174982012350256,
					112.84108597259467
				],
				[
					11.174982012350256,
					113.16636713915125
				],
				[
					11.174982012350256,
					113.16636713915125
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 88,
			"versionNonce": 1730858425,
			"isDeleted": false,
			"id": "xT6_PAR2FWxBFNv1YVX4h",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1286.5842344417686,
			"y": 532.2096917996844,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 42.44919223564534,
			"height": 119.4306528305815,
			"seed": 1752365141,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160947,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					0,
					-0.33577410741338554
				],
				[
					0,
					-2.801615208730027
				],
				[
					0,
					-4.637879858646784
				],
				[
					0,
					-8.635690325036762
				],
				[
					0,
					-11.117270837638443
				],
				[
					0,
					-15.115081304028536
				],
				[
					0.5298935132616407,
					-18.31542826531188
				],
				[
					1.0597870265232814,
					-21.515775226595224
				],
				[
					2.7701363861599475,
					-25.513585692985316
				],
				[
					3.300029899421588,
					-28.71393265426866
				],
				[
					4.438513982369841,
					-32.71174312065875
				],
				[
					5.576998065318321,
					-36.709553587048845
				],
				[
					8.00611387363665,
					-41.578278144542196
				],
				[
					9.716463233273316,
					-45.576088610932175
				],
				[
					11.536988471905033,
					-50.44481316842564
				],
				[
					13.2473378315417,
					-54.44262363481562
				],
				[
					15.067863070173416,
					-59.31134819230908
				],
				[
					17.496978878491745,
					-63.57148218011582
				],
				[
					19.091905888705014,
					-66.77182914139917
				],
				[
					20.802255248341908,
					-70.76963960778914
				],
				[
					22.512604607978574,
					-74.76745007417924
				],
				[
					24.941720416296903,
					-79.02758406198598
				],
				[
					26.76224565492862,
					-83.89630861947933
				],
				[
					28.472595014565286,
					-87.89411908586942
				],
				[
					29.957346145783504,
					-90.3756995984711
				],
				[
					31.66769550542017,
					-94.3735100648612
				],
				[
					33.262622515633666,
					-97.57385702614454
				],
				[
					35.24578833754367,
					-102.5370180513479
				],
				[
					36.08522360607708,
					-103.80141742457624
				],
				[
					36.46821594734524,
					-104.57264857754126
				],
				[
					36.851208288613634,
					-105.34387973050627
				],
				[
					37.1974753368836,
					-105.69539324920459
				],
				[
					37.543742385153564,
					-106.0469067679029
				],
				[
					37.89000943342376,
					-106.0469067679029
				],
				[
					37.89000943342376,
					-106.37743440488794
				],
				[
					38.27300177469192,
					-107.14866555785295
				],
				[
					38.65599411596031,
					-107.91989671081797
				],
				[
					39.0389864572287,
					-108.69112786378298
				],
				[
					39.42197879849709,
					-109.462359016748
				],
				[
					39.42197879849709,
					-110.23359016971301
				],
				[
					39.76824584676706,
					-110.58510368841132
				],
				[
					40.114512895037024,
					-111.28813072580806
				],
				[
					40.114512895037024,
					-111.63964424450637
				],
				[
					40.4397940615936,
					-111.63964424450637
				],
				[
					40.4397940615936,
					-111.95967894063472
				],
				[
					40.4397940615936,
					-112.2849601071913
				],
				[
					40.4397940615936,
					-112.61548774417633
				],
				[
					40.4397940615936,
					-112.94601538116137
				],
				[
					40.4397940615936,
					-113.27129654771807
				],
				[
					40.4397940615936,
					-113.62281006641638
				],
				[
					40.786061109863795,
					-113.97432358511469
				],
				[
					40.786061109863795,
					-114.7455547380797
				],
				[
					41.13232815813376,
					-115.09706825677802
				],
				[
					41.13232815813376,
					-115.44858177547644
				],
				[
					41.13232815813376,
					-115.80009529417475
				],
				[
					41.13232815813376,
					-116.15160881287306
				],
				[
					41.45760932469034,
					-116.4821364498581
				],
				[
					41.45760932469034,
					-116.80217114598645
				],
				[
					41.45760932469034,
					-117.1222058421148
				],
				[
					41.782890491247144,
					-117.1222058421148
				],
				[
					41.782890491247144,
					-117.4737193608131
				],
				[
					41.782890491247144,
					-117.80424699779803
				],
				[
					41.782890491247144,
					-118.12952816435472
				],
				[
					42.12915753951711,
					-118.12952816435472
				],
				[
					42.12915753951711,
					-118.44956286048307
				],
				[
					42.44919223564534,
					-118.77484402703976
				],
				[
					42.44919223564534,
					-119.10012519359645
				],
				[
					42.44919223564534,
					-119.4306528305815
				],
				[
					42.44919223564534,
					-119.4306528305815
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 77,
			"versionNonce": 268224087,
			"isDeleted": false,
			"id": "ujmUiOngLqPDY6Z1uam3e",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1141.7449253267685,
			"y": 494.9440123472323,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 129.87112898296482,
			"height": 73.50829717137924,
			"seed": 397987285,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160947,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					0.30954175527153893,
					0
				],
				[
					1.5686946580715357,
					0
				],
				[
					3.399712837559946,
					0
				],
				[
					5.876046879733394,
					0
				],
				[
					8.352380921906615,
					0
				],
				[
					10.828714964080064,
					0
				],
				[
					13.305049006253512,
					-0.9968293813833498
				],
				[
					15.781383048426733,
					-0.9968293813833498
				],
				[
					18.25771709060018,
					-1.9936587627666995
				],
				[
					21.452817581455292,
					-2.528798746456687
				],
				[
					22.218802263991847,
					-2.528798746456687
				],
				[
					24.049820443480257,
					-3.446931071415065
				],
				[
					28.913298530545262,
					-5.272702780475129
				],
				[
					31.38963257271871,
					-6.2695321618584785
				],
				[
					32.64878547551871,
					-7.114213900820118
				],
				[
					35.84388596637382,
					-8.714387381461847
				],
				[
					37.674904145862,
					-9.176076779155096
				],
				[
					39.65806996777201,
					-10.666074380801774
				],
				[
					42.134404009945456,
					-12.156071982448452
				],
				[
					45.32950450080057,
					-13.756245463090181
				],
				[
					47.80583854297379,
					-15.24624306473686
				],
				[
					52.06072606035218,
					-17.680605343483535
				],
				[
					57.57476648053057,
					-20.53993172692526
				],
				[
					59.40578466001898,
					-21.45806405188364
				],
				[
					63.66067217739737,
					-23.892426330630315
				],
				[
					65.49169035688578,
					-24.810558655588693
				],
				[
					67.968024399059,
					-26.30055625723537
				],
				[
					71.16312488991412,
					-27.900729737876986
				],
				[
					73.63945893208756,
					-29.390727339523664
				],
				[
					76.11579297426078,
					-30.880724941170342
				],
				[
					78.59212701643423,
					-31.877554322553692
				],
				[
					81.06846105860768,
					-33.36755192420037
				],
				[
					83.5447951007809,
					-34.85754952584705
				],
				[
					86.96549382005423,
					-37.145010632600474
				],
				[
					89.44182786222768,
					-38.63500823424715
				],
				[
					92.6369283530828,
					-40.23518171488888
				],
				[
					96.05762707235613,
					-42.522642821642194
				],
				[
					98.72283404994937,
					-44.65795628597391
				],
				[
					100.55385222943778,
					-45.57608861093229
				],
				[
					103.03018627161123,
					-47.066086212578966
				],
				[
					105.69539324920447,
					-49.20139967691057
				],
				[
					108.17172729137792,
					-50.69139727855725
				],
				[
					113.50214124656463,
					-54.96202420722068
				],
				[
					115.48530706847464,
					-56.45202180886736
				],
				[
					117.46847289038465,
					-58.44043410120571
				],
				[
					119.45163871229465,
					-60.42884639354406
				],
				[
					121.43480453420466,
					-62.417258685882416
				],
				[
					122.9195556654231,
					-64.40567097822077
				],
				[
					126.38747261855156,
					-68.38249556289747
				],
				[
					127.22690788708474,
					-69.64689493612582
				],
				[
					128.06634315561814,
					-70.91129430935416
				],
				[
					128.44933549688653,
					-71.68252546231918
				],
				[
					128.8323278381547,
					-72.45375661528419
				],
				[
					129.1785948864249,
					-72.8052701339825
				],
				[
					129.52486193469485,
					-73.15678365268093
				],
				[
					129.87112898296482,
					-73.15678365268093
				],
				[
					129.87112898296482,
					-73.50829717137924
				],
				[
					129.87112898296482,
					-73.50829717137924
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 108,
			"versionNonce": 265989785,
			"isDeleted": false,
			"id": "NfPmyW2kAjFS53PMnjn_Z",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1241.6429687526645,
			"y": 385.32425921763434,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 162.5041750471985,
			"height": 6.217067457575126,
			"seed": 375899317,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160947,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					-0.9443646770998839,
					0
				],
				[
					-2.7806293270166407,
					0
				],
				[
					-4.616893976933397,
					0
				],
				[
					-8.934739139451722,
					0
				],
				[
					-13.971350750651709,
					0
				],
				[
					-19.653278224536734,
					0
				],
				[
					-22.13485873713853,
					0
				],
				[
					-25.335205698421987,
					0
				],
				[
					-28.535552659705218,
					0
				],
				[
					-31.735899620988675,
					0
				],
				[
					-35.73371008737877,
					0
				],
				[
					-38.934057048662,
					0
				],
				[
					-42.134404009945456,
					0
				],
				[
					-45.33475097122869,
					0
				],
				[
					-48.535097932512144,
					0
				],
				[
					-52.53290839890224,
					0
				],
				[
					-54.36917304881899,
					0
				],
				[
					-60.18226228341223,
					0
				],
				[
					-64.18007274980232,
					0
				],
				[
					-66.01633739971908,
					0
				],
				[
					-69.21668436100231,
					0
				],
				[
					-73.2144948273924,
					0
				],
				[
					-76.41484178867586,
					0
				],
				[
					-79.61518874995909,
					0
				],
				[
					-82.81553571124255,
					0
				],
				[
					-86.015882672526,
					0
				],
				[
					-89.21622963380923,
					0
				],
				[
					-92.41657659509269,
					0
				],
				[
					-94.89815710769426,
					0
				],
				[
					-98.09850406897772,
					0
				],
				[
					-100.58008458157951,
					-0.4984146906916749
				],
				[
					-105.54324560678288,
					-1.9936587627666995
				],
				[
					-108.02482611938467,
					-2.9904881441500493
				],
				[
					-110.50640663198624,
					-3.488902834841724
				],
				[
					-112.98798714458803,
					-3.987317525533399
				],
				[
					-114.82425179450456,
					-4.905449850491777
				],
				[
					-116.66051644442132,
					-5.36713924818514
				],
				[
					-118.49678109433808,
					-5.36713924818514
				],
				[
					-119.76118046756642,
					-5.792103352880076
				],
				[
					-121.02557984079476,
					-5.792103352880076
				],
				[
					-122.2899792140231,
					-6.217067457575126
				],
				[
					-123.55437858725145,
					-6.217067457575126
				],
				[
					-124.81877796047979,
					-6.217067457575126
				],
				[
					-126.08317733370814,
					-6.217067457575126
				],
				[
					-126.85440848667304,
					-6.217067457575126
				],
				[
					-128.11880785990138,
					-6.217067457575126
				],
				[
					-129.38320723312995,
					-6.217067457575126
				],
				[
					-130.6476066063583,
					-6.217067457575126
				],
				[
					-131.91200597958664,
					-6.217067457575126
				],
				[
					-132.68323713255154,
					-6.217067457575126
				],
				[
					-133.94763650577988,
					-6.217067457575126
				],
				[
					-134.718867658745,
					-6.217067457575126
				],
				[
					-135.4900988117099,
					-6.217067457575126
				],
				[
					-136.26132996467481,
					-6.217067457575126
				],
				[
					-137.03256111763994,
					-6.217067457575126
				],
				[
					-137.80379227060484,
					-6.217067457575126
				],
				[
					-139.83942279679832,
					-6.217067457575126
				],
				[
					-140.96216746846153,
					-6.217067457575126
				],
				[
					-141.73339862142666,
					-6.217067457575126
				],
				[
					-142.50462977439156,
					-6.217067457575126
				],
				[
					-142.8561432930901,
					-6.217067457575126
				],
				[
					-143.2076568117884,
					-6.217067457575126
				],
				[
					-143.55917033048672,
					-6.217067457575126
				],
				[
					-143.88969796747165,
					-6.217067457575126
				],
				[
					-144.24121148616996,
					-6.217067457575126
				],
				[
					-145.0124426391351,
					-5.834075116306735
				],
				[
					-145.7836737921,
					-5.834075116306735
				],
				[
					-146.1351873107983,
					-5.48780806803677
				],
				[
					-146.90641846376343,
					-5.48780806803677
				],
				[
					-147.67764961672833,
					-5.104815726768493
				],
				[
					-148.44888076969346,
					-5.104815726768493
				],
				[
					-148.80039428839177,
					-5.104815726768493
				],
				[
					-149.15190780709008,
					-5.104815726768493
				],
				[
					-149.5034213257884,
					-4.758548678498414
				],
				[
					-149.8549348444867,
					-4.758548678498414
				],
				[
					-150.20644836318502,
					-4.758548678498414
				],
				[
					-150.55796188188333,
					-4.758548678498414
				],
				[
					-151.32919303484846,
					-4.375556337230137
				],
				[
					-152.10042418781336,
					-4.375556337230137
				],
				[
					-153.3648235610417,
					-3.955838702963433
				],
				[
					-154.62922293427005,
					-3.5361210686967297
				],
				[
					-155.8936223074984,
					-3.11640343443014
				],
				[
					-157.72988695741515,
					-3.11640343443014
				],
				[
					-159.76551748360862,
					-2.6966858001634364
				],
				[
					-161.02991685683696,
					-2.6966858001634364
				],
				[
					-161.38143037553527,
					-2.6966858001634364
				],
				[
					-162.15266152850018,
					-2.6966858001634364
				],
				[
					-162.5041750471985,
					-2.6966858001634364
				],
				[
					-162.5041750471985,
					-2.6966858001634364
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 20,
			"versionNonce": 1935663991,
			"isDeleted": false,
			"id": "aGrDhUwsTXhxE-toTLYN7",
			"fillStyle": "hachure",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 708.9310946457304,
			"y": 396.4059251840739,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 0.0001,
			"height": 0.0001,
			"seed": 1088958336,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160947,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					0.0001,
					0.0001
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 21,
			"versionNonce": 1570468729,
			"isDeleted": false,
			"id": "FVoOaLYzRJsa6baorB67a",
			"fillStyle": "hachure",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -683.1819809230828,
			"y": -1175.6070284359464,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 0.0001,
			"height": 0.0001,
			"seed": 1038514304,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160947,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					0.0001,
					0.0001
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 57,
			"versionNonce": 1923243159,
			"isDeleted": false,
			"id": "_yNqMT5N9DjUqFeT6X26J",
			"fillStyle": "hachure",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -1277.5571920167515,
			"y": -54.59731224011273,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 87.32517036678018,
			"height": 423.9496174258193,
			"seed": 2090199168,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160947,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					0,
					-7.0423524489339115
				],
				[
					4.225411469360324,
					-22.535527836588358
				],
				[
					15.493175387654674,
					-52.11340812211074
				],
				[
					26.760939305948796,
					-78.87434742805942
				],
				[
					33.80329175488259,
					-100.00140477486104
				],
				[
					45.07105567317694,
					-132.3962260399569
				],
				[
					50.70493763232389,
					-152.11481289697167
				],
				[
					59.15576057104454,
					-183.1011636722808
				],
				[
					66.19811301997856,
					-202.81975052929567
				],
				[
					71.83199497912551,
					-223.9468078760973
				],
				[
					76.05740644848584,
					-242.25692424332533
				],
				[
					77.46587693827269,
					-261.9755111003402
				],
				[
					80.28281791784616,
					-273.2432750186344
				],
				[
					81.69128840763301,
					-284.51103893692857
				],
				[
					83.09975889741986,
					-295.7788028552228
				],
				[
					83.09975889741986,
					-309.8635077530905
				],
				[
					83.09975889741986,
					-312.6804487326641
				],
				[
					83.09975889741986,
					-321.13127167138475
				],
				[
					83.09975889741986,
					-326.76515363053187
				],
				[
					83.09975889741986,
					-335.2159765692525
				],
				[
					83.09975889741986,
					-342.2583290181864
				],
				[
					83.09975889741986,
					-350.709151956907
				],
				[
					83.09975889741986,
					-356.34303391605414
				],
				[
					83.09975889741986,
					-363.385386364988
				],
				[
					83.09975889741986,
					-373.24467979349544
				],
				[
					83.09975889741986,
					-377.47009126285576
				],
				[
					84.50822938720648,
					-383.1039732220029
				],
				[
					85.91669987699333,
					-391.5547961607235
				],
				[
					85.91669987699333,
					-400.0056190994442
				],
				[
					87.32517036678018,
					-402.8225600790177
				],
				[
					87.32517036678018,
					-408.4564420381648
				],
				[
					87.32517036678018,
					-411.27338301773835
				],
				[
					87.32517036678018,
					-416.9072649768855
				],
				[
					87.32517036678018,
					-421.1326764462458
				],
				[
					87.32517036678018,
					-422.54114693603253
				],
				[
					87.32517036678018,
					-423.9496174258193
				],
				[
					87.32517036678018,
					-423.9496174258193
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 66,
			"versionNonce": 1152425049,
			"isDeleted": false,
			"id": "Te0-GlsfQI2Id33jR7fmh",
			"fillStyle": "hachure",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -1500.128666884445,
			"y": 93.8945669543998,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 278.26690297325445,
			"height": 250.0054206400332,
			"seed": 483690624,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160948,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					-4.347920358957026,
					2.173960179478513
				],
				[
					-10.869800897392679,
					13.043761076871306
				],
				[
					-21.739601794785358,
					26.08752215374261
				],
				[
					-36.95732305113529,
					47.82712394852808
				],
				[
					-58.696924845920876,
					71.74068592279218
				],
				[
					-100.00216825601319,
					121.74177005079878
				],
				[
					-113.0459293328845,
					132.61157094819157
				],
				[
					-134.78553112767008,
					158.69909310193418
				],
				[
					-152.17721256349841,
					176.09077453776263
				],
				[
					-171.74285417880537,
					193.48245597359096
				],
				[
					-178.26473471724103,
					200.0043365120266
				],
				[
					-195.65641615306959,
					213.04809758889792
				],
				[
					-204.35225687098364,
					219.56997812733357
				],
				[
					-221.7439383068122,
					230.43977902472625
				],
				[
					-230.43977902472625,
					232.61373920420488
				],
				[
					-250.0054206400332,
					241.30957992211916
				],
				[
					-260.8752215374261,
					243.48354010159755
				],
				[
					-273.9189826142974,
					247.8314604605548
				],
				[
					-278.26690297325445,
					250.0054206400332
				],
				[
					-278.26690297325445,
					250.0054206400332
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 37,
			"versionNonce": 293122487,
			"isDeleted": false,
			"id": "ud7teOjKuWy8K4Vyx8u8F",
			"fillStyle": "hachure",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -1559.7744630138766,
			"y": -69.24451904397722,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 178.26473471724125,
			"height": 250.00542064003338,
			"seed": 1590737024,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160948,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					-2.1739601794786267,
					0
				],
				[
					-4.347920358957026,
					0
				],
				[
					-6.521880538435653,
					-2.1739601794786267
				],
				[
					-10.869800897392679,
					-6.521880538435653
				],
				[
					-17.391681435828332,
					-17.391681435828446
				],
				[
					-39.13128323061392,
					-43.47920358957106
				],
				[
					-60.8708850253995,
					-73.91464610227081
				],
				[
					-80.43652664070646,
					-97.82820807653479
				],
				[
					-100.00216825601342,
					-128.26365058923454
				],
				[
					-128.26365058923443,
					-173.9168143582841
				],
				[
					-141.30741166610574,
					-193.48245597359107
				],
				[
					-150.00325238402002,
					-208.7001772299409
				],
				[
					-156.52513292245567,
					-221.7439383068122
				],
				[
					-167.39493381984835,
					-236.96165956316207
				],
				[
					-176.09077453776263,
					-245.6575002810763
				],
				[
					-178.26473471724125,
					-250.00542064003338
				],
				[
					-178.26473471724125,
					-250.00542064003338
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 230,
			"versionNonce": 1693296953,
			"isDeleted": false,
			"id": "qBbjKVQAhispikOQQNRar",
			"fillStyle": "hachure",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 404.1379815677119,
			"y": -1319.082515752031,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 236.8452134705908,
			"height": 436.84783817908954,
			"seed": 2020939904,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160948,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					6.579033707516373,
					0
				],
				[
					11.842260673529609,
					0
				],
				[
					26.31613483006572,
					0
				],
				[
					31.57936179607873,
					0
				],
				[
					39.47420224509847,
					0
				],
				[
					44.737429211111476,
					0
				],
				[
					51.316462918628076,
					1.3158067415033656
				],
				[
					67.10614381666733,
					3.9474202245098695
				],
				[
					76.31679100719043,
					5.263226966013235
				],
				[
					86.84324493921667,
					6.579033707516373
				],
				[
					103.94873257875929,
					9.210647190522877
				],
				[
					119.73841347679854,
					11.842260673529609
				],
				[
					128.94906066732165,
					14.473874156536112
				],
				[
					136.84390111634139,
					15.789680898039478
				],
				[
					143.42293482385776,
					18.421294381045982
				],
				[
					148.68616178987077,
					19.737101122549348
				],
				[
					155.26519549738714,
					23.68452134705899
				],
				[
					160.52842246340037,
					26.31613483006572
				],
				[
					164.47584268791024,
					28.947748313072225
				],
				[
					168.4232629124201,
					31.57936179607873
				],
				[
					176.31810336143985,
					39.47420224509847
				],
				[
					178.94971684444636,
					42.10581572810497
				],
				[
					182.89713706895623,
					47.36904269411821
				],
				[
					186.8445572934661,
					51.316462918628076
				],
				[
					193.42359100098247,
					57.89549662614445
				],
				[
					194.7393977424856,
					61.84291685065432
				],
				[
					196.05520448398897,
					63.158723592157685
				],
				[
					198.68681796699548,
					65.79033707516419
				],
				[
					201.31843145000198,
					69.73775729967406
				],
				[
					202.63423819150535,
					72.36937078268056
				],
				[
					202.63423819150535,
					73.6851775241837
				],
				[
					205.26585167451185,
					77.63259774869357
				],
				[
					205.26585167451185,
					80.2642112317003
				],
				[
					206.58165841601522,
					82.8958247147068
				],
				[
					206.58165841601522,
					85.52743819771331
				],
				[
					207.89746515751858,
					86.84324493921667
				],
				[
					209.21327189902172,
					88.15905168071981
				],
				[
					209.21327189902172,
					90.79066516372654
				],
				[
					210.52907864052509,
					92.10647190522968
				],
				[
					210.52907864052509,
					94.73808538823619
				],
				[
					210.52907864052509,
					97.36969887124292
				],
				[
					211.84488538202845,
					100.00131235424942
				],
				[
					213.1606921235316,
					103.94873257875929
				],
				[
					214.47649886503496,
					106.5803460617658
				],
				[
					214.47649886503496,
					109.2119595447723
				],
				[
					215.7923056065381,
					110.52776628627566
				],
				[
					217.10811234804146,
					114.47518651078553
				],
				[
					217.10811234804146,
					115.7909932522889
				],
				[
					217.10811234804146,
					118.4226067352954
				],
				[
					218.42391908954482,
					119.73841347679877
				],
				[
					219.73972583104796,
					121.05422021830191
				],
				[
					219.73972583104796,
					123.68583370130841
				],
				[
					219.73972583104796,
					125.00164044281178
				],
				[
					221.05553257255133,
					126.31744718431514
				],
				[
					221.05553257255133,
					127.63325392581828
				],
				[
					221.05553257255133,
					130.26486740882478
				],
				[
					222.3713393140547,
					131.58067415032815
				],
				[
					222.3713393140547,
					132.89648089183152
				],
				[
					222.3713393140547,
					134.21228763333488
				],
				[
					222.3713393140547,
					135.52809437483802
				],
				[
					223.68714605555783,
					138.15970785784452
				],
				[
					225.0029527970612,
					139.4755145993479
				],
				[
					225.0029527970612,
					140.79132134085125
				],
				[
					225.0029527970612,
					142.1071280823544
				],
				[
					225.0029527970612,
					143.42293482385776
				],
				[
					226.31875953856434,
					144.7387415653609
				],
				[
					226.31875953856434,
					146.05454830686426
				],
				[
					226.31875953856434,
					148.686161789871
				],
				[
					227.6345662800677,
					150.00196853137413
				],
				[
					227.6345662800677,
					152.63358201438064
				],
				[
					228.95037302157107,
					153.949388755884
				],
				[
					228.95037302157107,
					155.26519549738737
				],
				[
					230.2661797630742,
					156.5810022388905
				],
				[
					230.2661797630742,
					159.212615721897
				],
				[
					230.2661797630742,
					160.52842246340037
				],
				[
					230.2661797630742,
					161.84422920490374
				],
				[
					231.58198650457757,
					164.47584268791024
				],
				[
					231.58198650457757,
					165.7916494294136
				],
				[
					231.58198650457757,
					167.10745617091675
				],
				[
					231.58198650457757,
					169.73906965392348
				],
				[
					231.58198650457757,
					171.05487639542662
				],
				[
					231.58198650457757,
					173.68648987843312
				],
				[
					232.89779324608094,
					173.68648987843312
				],
				[
					232.89779324608094,
					176.31810336143985
				],
				[
					232.89779324608094,
					177.633910102943
				],
				[
					232.89779324608094,
					181.58133032745286
				],
				[
					232.89779324608094,
					182.89713706895623
				],
				[
					232.89779324608094,
					184.2129438104596
				],
				[
					234.21359998758408,
					185.52875055196273
				],
				[
					234.21359998758408,
					188.16036403496923
				],
				[
					235.52940672908744,
					190.79197751797597
				],
				[
					235.52940672908744,
					192.1077842594791
				],
				[
					235.52940672908744,
					194.7393977424856
				],
				[
					235.52940672908744,
					198.6868179669957
				],
				[
					235.52940672908744,
					200.00262470849884
				],
				[
					236.8452134705908,
					201.3184314500022
				],
				[
					236.8452134705908,
					202.63423819150535
				],
				[
					236.8452134705908,
					203.9500449330087
				],
				[
					236.8452134705908,
					206.58165841601522
				],
				[
					236.8452134705908,
					207.89746515751858
				],
				[
					236.8452134705908,
					209.21327189902172
				],
				[
					236.8452134705908,
					211.84488538202845
				],
				[
					236.8452134705908,
					213.1606921235316
				],
				[
					236.8452134705908,
					214.47649886503496
				],
				[
					236.8452134705908,
					217.10811234804146
				],
				[
					236.8452134705908,
					219.7397258310482
				],
				[
					236.8452134705908,
					221.05553257255133
				],
				[
					236.8452134705908,
					223.68714605555783
				],
				[
					236.8452134705908,
					225.0029527970612
				],
				[
					236.8452134705908,
					226.31875953856456
				],
				[
					236.8452134705908,
					230.2661797630742
				],
				[
					235.52940672908744,
					234.2135999875843
				],
				[
					235.52940672908744,
					235.52940672908744
				],
				[
					235.52940672908744,
					236.84521347059058
				],
				[
					235.52940672908744,
					240.79263369510068
				],
				[
					234.21359998758408,
					242.10844043660381
				],
				[
					234.21359998758408,
					243.42424717810718
				],
				[
					234.21359998758408,
					244.74005391961032
				],
				[
					234.21359998758408,
					247.37166740261705
				],
				[
					232.89779324608094,
					248.68747414412042
				],
				[
					231.58198650457757,
					250.00328088562355
				],
				[
					231.58198650457757,
					251.3190876271267
				],
				[
					231.58198650457757,
					252.63489436863006
				],
				[
					230.2661797630742,
					253.95070111013342
				],
				[
					230.2661797630742,
					256.5823145931399
				],
				[
					228.95037302157107,
					257.8981213346433
				],
				[
					227.6345662800677,
					260.5297348176498
				],
				[
					226.31875953856434,
					263.1613483006565
				],
				[
					226.31875953856434,
					264.47715504215967
				],
				[
					225.0029527970612,
					265.7929617836628
				],
				[
					223.68714605555783,
					269.7403820081729
				],
				[
					222.3713393140547,
					271.05618874967604
				],
				[
					221.05553257255133,
					273.68780223268254
				],
				[
					221.05553257255133,
					276.3194157156893
				],
				[
					219.73972583104796,
					276.3194157156893
				],
				[
					218.42391908954482,
					280.2668359401989
				],
				[
					218.42391908954482,
					281.5826426817023
				],
				[
					217.10811234804146,
					282.89844942320565
				],
				[
					217.10811234804146,
					284.214256164709
				],
				[
					217.10811234804146,
					285.53006290621215
				],
				[
					214.47649886503496,
					289.477483130722
				],
				[
					214.47649886503496,
					290.7932898722254
				],
				[
					213.1606921235316,
					292.1090966137285
				],
				[
					213.1606921235316,
					294.74071009673503
				],
				[
					211.84488538202845,
					296.0565168382384
				],
				[
					210.52907864052509,
					298.688130321245
				],
				[
					210.52907864052509,
					300.00393706274826
				],
				[
					209.21327189902172,
					301.3197438042515
				],
				[
					209.21327189902172,
					305.2671640287614
				],
				[
					206.58165841601522,
					306.58297077026464
				],
				[
					206.58165841601522,
					309.21458425327125
				],
				[
					206.58165841601522,
					310.5303909947745
				],
				[
					203.9500449330087,
					314.4778112192844
				],
				[
					202.63423819150535,
					317.1094247022909
				],
				[
					201.31843145000198,
					318.42523144379425
				],
				[
					201.31843145000198,
					319.7410381852975
				],
				[
					198.68681796699548,
					325.0042651513106
				],
				[
					198.68681796699548,
					327.6358786343171
				],
				[
					198.68681796699548,
					328.9516853758205
				],
				[
					197.37101122549234,
					331.583298858827
				],
				[
					197.37101122549234,
					332.89910560033036
				],
				[
					196.05520448398897,
					334.2149123418336
				],
				[
					196.05520448398897,
					335.53071908333686
				],
				[
					196.05520448398897,
					336.8465258248401
				],
				[
					194.7393977424856,
					338.1623325663435
				],
				[
					193.42359100098247,
					340.79394604935
				],
				[
					193.42359100098247,
					342.10975279085324
				],
				[
					192.1077842594791,
					344.74136627385985
				],
				[
					192.1077842594791,
					346.0571730153631
				],
				[
					192.1077842594791,
					347.37297975686636
				],
				[
					190.79197751797574,
					347.37297975686636
				],
				[
					189.4761707764726,
					350.004593239873
				],
				[
					188.16036403496923,
					353.95201346438284
				],
				[
					186.8445572934661,
					357.8994336888926
				],
				[
					185.52875055196273,
					359.21524043039597
				],
				[
					184.21294381045936,
					360.5310471718992
				],
				[
					184.21294381045936,
					363.16266065490584
				],
				[
					181.58133032745286,
					367.1100808794156
				],
				[
					181.58133032745286,
					368.42588762091896
				],
				[
					180.2655235859495,
					371.05750110392546
				],
				[
					178.94971684444636,
					373.6891145869321
				],
				[
					177.633910102943,
					375.00492132843533
				],
				[
					177.633910102943,
					377.63653481144183
				],
				[
					176.31810336143985,
					378.9523415529452
				],
				[
					173.68648987843312,
					384.2155685189583
				],
				[
					172.37068313692998,
					388.1629887434682
				],
				[
					172.37068313692998,
					389.47879548497144
				],
				[
					171.05487639542662,
					392.11040896797795
				],
				[
					169.73906965392325,
					394.74202245098456
				],
				[
					169.73906965392325,
					397.37363593399107
				],
				[
					168.4232629124201,
					400.0052494169977
				],
				[
					167.10745617091675,
					402.6368629000042
				],
				[
					165.79164942941338,
					405.2684763830108
				],
				[
					164.47584268791024,
					406.58428312451406
				],
				[
					164.47584268791024,
					409.2158966075207
				],
				[
					163.16003594640688,
					411.8475100905272
				],
				[
					161.84422920490374,
					414.4791235735338
				],
				[
					160.52842246340037,
					415.79493031503705
				],
				[
					159.212615721897,
					417.1107370565403
				],
				[
					159.212615721897,
					419.7423505395469
				],
				[
					156.5810022388905,
					423.6897707640568
				],
				[
					156.5810022388905,
					425.00557750556004
				],
				[
					155.26519549738714,
					427.63719098856654
				],
				[
					153.949388755884,
					430.26880447157316
				],
				[
					153.949388755884,
					431.5846112130764
				],
				[
					152.63358201438064,
					432.90041795457967
				],
				[
					151.3177752728775,
					434.21622469608303
				],
				[
					151.3177752728775,
					435.5320314375863
				],
				[
					150.00196853137413,
					436.84783817908954
				],
				[
					150.00196853137413,
					436.84783817908954
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 106,
			"versionNonce": 1762091735,
			"isDeleted": false,
			"id": "dl7vb0R8K_VDY7iLNRil9",
			"fillStyle": "hachure",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 362.03216583960693,
			"y": -1183.554421377193,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 278.9510291986958,
			"height": 407.9000898660174,
			"seed": 1417320576,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160948,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					5.263226966013008,
					-2.631613483006504
				],
				[
					9.210647190522877,
					-6.579033707516373
				],
				[
					17.105487639542616,
					-11.842260673529609
				],
				[
					26.316134830065494,
					-17.105487639542616
				],
				[
					42.10581572810497,
					-26.31613483006572
				],
				[
					51.31646291862785,
					-30.263555054575363
				],
				[
					65.79033707516396,
					-34.21097527908523
				],
				[
					75.00098426568707,
					-39.47420224509847
				],
				[
					90.79066516372632,
					-44.737429211111476
				],
				[
					101.31711909575256,
					-47.36904269411821
				],
				[
					111.8435730277788,
					-48.684849435621345
				],
				[
					121.05422021830191,
					-51.31646291862785
				],
				[
					131.58067415032815,
					-52.632269660131215
				],
				[
					152.63358201438064,
					-53.94807640163458
				],
				[
					160.52842246340037,
					-53.94807640163458
				],
				[
					175.0022966199365,
					-53.94807640163458
				],
				[
					192.1077842594791,
					-53.94807640163458
				],
				[
					215.7923056065381,
					-51.31646291862785
				],
				[
					226.31875953856434,
					-48.684849435621345
				],
				[
					240.79263369510045,
					-46.05323595261484
				],
				[
					246.05586066111368,
					-44.737429211111476
				],
				[
					252.63489436863006,
					-42.10581572810497
				],
				[
					255.26650785163656,
					-39.47420224509847
				],
				[
					257.89812133464306,
					-35.5267820205886
				],
				[
					259.21392807614643,
					-34.21097527908523
				],
				[
					261.84554155915293,
					-30.263555054575363
				],
				[
					265.7929617836628,
					-22.368714605555624
				],
				[
					269.7403820081727,
					-17.105487639542616
				],
				[
					271.05618874967604,
					-11.842260673529609
				],
				[
					272.3719954911792,
					-6.579033707516373
				],
				[
					275.0036089741859,
					7.894840449019739
				],
				[
					276.31941571568905,
					15.789680898039478
				],
				[
					277.6352224571924,
					26.31613483006572
				],
				[
					277.6352224571924,
					34.21097527908546
				],
				[
					278.9510291986958,
					42.10581572810497
				],
				[
					278.9510291986958,
					52.632269660131215
				],
				[
					278.9510291986958,
					59.21130336764759
				],
				[
					278.9510291986958,
					67.10614381666733
				],
				[
					278.9510291986958,
					73.6851775241837
				],
				[
					275.0036089741859,
					88.15905168071981
				],
				[
					272.3719954911792,
					100.00131235424942
				],
				[
					268.4245752666693,
					113.1593797692824
				],
				[
					263.1613483006563,
					122.37002695980527
				],
				[
					256.5823145931399,
					139.4755145993479
				],
				[
					253.95070111013342,
					148.686161789871
				],
				[
					250.00328088562355,
					157.89680898039387
				],
				[
					247.37166740261682,
					167.10745617091686
				],
				[
					246.05586066111368,
					173.68648987843324
				],
				[
					239.4768269535973,
					189.4761707764726
				],
				[
					235.52940672908744,
					201.3184314500021
				],
				[
					230.2661797630742,
					213.1606921235317
				],
				[
					227.6345662800677,
					219.73972583104808
				],
				[
					219.73972583104796,
					236.8452134705907
				],
				[
					217.10811234804146,
					243.42424717810718
				],
				[
					213.1606921235316,
					253.95070111013342
				],
				[
					207.89746515751835,
					261.84554155915305
				],
				[
					206.58165841601522,
					264.47715504215967
				],
				[
					205.26585167451185,
					269.7403820081728
				],
				[
					201.31843145000198,
					276.31941571568916
				],
				[
					197.3710112254921,
					282.89844942320565
				],
				[
					193.42359100098247,
					288.16167638921877
				],
				[
					190.79197751797574,
					292.1090966137285
				],
				[
					188.16036403496923,
					296.0565168382384
				],
				[
					185.52875055196273,
					301.3197438042515
				],
				[
					182.897137068956,
					305.2671640287614
				],
				[
					181.58133032745286,
					306.58297077026464
				],
				[
					180.2655235859495,
					310.5303909947745
				],
				[
					176.31810336143963,
					314.4778112192844
				],
				[
					173.68648987843312,
					318.42523144379425
				],
				[
					173.68648987843312,
					321.05684492680075
				],
				[
					169.73906965392325,
					327.6358786343171
				],
				[
					167.10745617091675,
					331.583298858827
				],
				[
					165.79164942941338,
					335.53071908333686
				],
				[
					161.8442292049035,
					342.10975279085324
				],
				[
					160.52842246340037,
					342.10975279085324
				],
				[
					159.212615721897,
					346.0571730153631
				],
				[
					157.89680898039364,
					347.37297975686636
				],
				[
					156.5810022388905,
					347.37297975686636
				],
				[
					156.5810022388905,
					348.6887864983697
				],
				[
					155.26519549738714,
					348.6887864983697
				],
				[
					155.26519549738714,
					350.004593239873
				],
				[
					155.26519549738714,
					351.3203999813762
				],
				[
					153.949388755884,
					352.6362067228795
				],
				[
					152.63358201438064,
					353.95201346438284
				],
				[
					151.31777527287727,
					353.95201346438284
				],
				[
					151.31777527287727,
					353.95201346438284
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 28,
			"versionNonce": 397810201,
			"isDeleted": false,
			"id": "UDjlMOUntqmmtdjm_iLLd",
			"fillStyle": "hachure",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 230.45149168927878,
			"y": -1294.0821876634686,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 14.473874156536112,
			"height": 94.73808538823641,
			"seed": 76494976,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160948,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					0,
					1.3158067415033656
				],
				[
					0,
					6.579033707516373
				],
				[
					0,
					14.473874156536112
				],
				[
					3.9474202245098695,
					42.10581572810497
				],
				[
					7.894840449019512,
					63.15872359215746
				],
				[
					13.158067415032747,
					86.84324493921667
				],
				[
					14.473874156536112,
					94.73808538823641
				],
				[
					14.473874156536112,
					94.73808538823641
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 28,
			"versionNonce": 2044915703,
			"isDeleted": false,
			"id": "VNdjBY9SO65heO7oiyFVF",
			"fillStyle": "hachure",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 422.5592759487579,
			"y": -1030.9208393628123,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 90.79066516372632,
			"height": 90.79066516372632,
			"seed": 569104512,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160948,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					3.9474202245098695,
					-3.947420224509642
				],
				[
					23.68452134705899,
					-22.36871460555585
				],
				[
					43.42162246960834,
					-42.10581572810497
				],
				[
					57.89549662614445,
					-57.89549662614445
				],
				[
					77.63259774869357,
					-78.94840449019694
				],
				[
					86.84324493921645,
					-88.15905168071981
				],
				[
					90.79066516372632,
					-90.79066516372632
				],
				[
					90.79066516372632,
					-90.79066516372632
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 28,
			"versionNonce": 1040019193,
			"isDeleted": false,
			"id": "t4nYJfBkGkd6V3ialela1",
			"fillStyle": "hachure",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 243.60955910431153,
			"y": -1148.0276393566044,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 5.263226966013235,
			"height": 109.2119595447723,
			"seed": 647002240,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160948,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					0,
					2.631613483006504
				],
				[
					0,
					9.210647190522877
				],
				[
					0,
					25.000328088562355
				],
				[
					-2.631613483006504,
					48.68484943562157
				],
				[
					-5.263226966013235,
					68.42195055817069
				],
				[
					-5.263226966013235,
					88.15905168071981
				],
				[
					-5.263226966013235,
					109.2119595447723
				],
				[
					-5.263226966013235,
					109.2119595447723
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 27,
			"versionNonce": 1041226007,
			"isDeleted": false,
			"id": "hIhe03ae3MX24J9yHHm0Q",
			"fillStyle": "hachure",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 672.5625568343814,
			"y": -776.9701382526789,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 64.47453033366082,
			"height": 9.210647190522991,
			"seed": 507906176,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160948,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					13.158067415032747,
					-1.315806741503252
				],
				[
					25.000328088562355,
					-2.631613483006504
				],
				[
					35.5267820205886,
					-5.2632269660131215
				],
				[
					51.31646291862785,
					-7.894840449019625
				],
				[
					61.84291685065409,
					-9.210647190522991
				],
				[
					64.47453033366082,
					-9.210647190522991
				],
				[
					64.47453033366082,
					-9.210647190522991
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 29,
			"versionNonce": 1313286105,
			"isDeleted": false,
			"id": "0j1r9FxiPEXpWGGwUhHoW",
			"fillStyle": "hachure",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 173.8718018046377,
			"y": -703.2849607284951,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 218.4239190895446,
			"height": 50.00065617712471,
			"seed": 1303492736,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160948,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					14.473874156536112,
					-3.9474202245098695
				],
				[
					32.89516853758187,
					-10.526453932026243
				],
				[
					56.579689884641084,
					-15.789680898039364
				],
				[
					92.10647190522968,
					-23.684521347059103
				],
				[
					127.63325392581828,
					-31.57936179607873
				],
				[
					186.84455729346587,
					-42.105815728105085
				],
				[
					213.1606921235316,
					-47.36904269411821
				],
				[
					218.4239190895446,
					-50.00065617712471
				],
				[
					218.4239190895446,
					-50.00065617712471
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 33,
			"versionNonce": 2063769143,
			"isDeleted": false,
			"id": "j2TNFHeN2S9PWi8-SSf1e",
			"fillStyle": "hachure",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -32.70985661137752,
			"y": -1012.4995449817663,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 151.31777527287727,
			"height": 9.210647190522991,
			"seed": 679979136,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160948,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					1.3158067415031383,
					0
				],
				[
					3.947420224509642,
					0
				],
				[
					11.842260673529381,
					-1.315806741503252
				],
				[
					19.73710112254912,
					-2.631613483006504
				],
				[
					34.21097527908523,
					-3.947420224509756
				],
				[
					50.00065617712448,
					-6.579033707516373
				],
				[
					67.10614381666733,
					-6.579033707516373
				],
				[
					92.10647190522968,
					-7.894840449019625
				],
				[
					109.2119595447723,
					-7.894840449019625
				],
				[
					126.31744718431491,
					-7.894840449019625
				],
				[
					146.05454830686426,
					-7.894840449019625
				],
				[
					151.31777527287727,
					-9.210647190522991
				],
				[
					151.31777527287727,
					-9.210647190522991
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 40,
			"versionNonce": 581354681,
			"isDeleted": false,
			"id": "k3PjXJC_M2O_E0ijIY7pP",
			"fillStyle": "hachure",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 63.344035518362034,
			"y": -758.5488438716329,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 148.68616178987077,
			"height": 197.37101122549223,
			"seed": 510199936,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160948,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					3.947420224509642,
					-9.210647190522991
				],
				[
					7.894840449019512,
					-15.789680898039364
				],
				[
					14.473874156536112,
					-28.947748313072225
				],
				[
					25.000328088562355,
					-47.36904269411821
				],
				[
					38.1583955035951,
					-68.42195055817069
				],
				[
					55.26388314313772,
					-102.63292583725604
				],
				[
					64.4745303336606,
					-118.4226067352954
				],
				[
					75.00098426568707,
					-132.89648089183152
				],
				[
					82.89582471470658,
					-146.05454830686426
				],
				[
					88.15905168071981,
					-152.63358201438075
				],
				[
					93.42227864673282,
					-157.89680898039387
				],
				[
					97.36969887124269,
					-163.160035946407
				],
				[
					102.63292583725593,
					-167.10745617091675
				],
				[
					115.79099325228867,
					-177.6339101029431
				],
				[
					125.00164044281178,
					-184.21294381045948
				],
				[
					136.84390111634116,
					-190.79197751797585
				],
				[
					142.1071280823544,
					-193.42359100098247
				],
				[
					147.3703550483674,
					-197.37101122549223
				],
				[
					148.68616178987077,
					-197.37101122549223
				],
				[
					148.68616178987077,
					-197.37101122549223
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 36,
			"versionNonce": 1402978135,
			"isDeleted": false,
			"id": "E581asJXGdJ6KYJRH9SiJ",
			"fillStyle": "hachure",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -30.078243128371014,
			"y": -763.812070837646,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 109.21195954477253,
			"height": 198.6868179669956,
			"seed": 584722560,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160948,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					-1.3158067415033656,
					0
				],
				[
					-14.473874156536112,
					-15.789680898039364
				],
				[
					-28.947748313072225,
					-36.842588762091964
				],
				[
					-40.79000898660183,
					-57.89549662614445
				],
				[
					-59.211303367647815,
					-84.21163145621006
				],
				[
					-71.0535640411772,
					-105.26453932026254
				],
				[
					-88.15905168071981,
					-134.21228763333477
				],
				[
					-94.73808538823641,
					-146.05454830686426
				],
				[
					-98.68550561274628,
					-160.52842246340037
				],
				[
					-102.63292583725593,
					-172.37068313692998
				],
				[
					-105.26453932026266,
					-184.21294381045948
				],
				[
					-107.89615280326916,
					-190.79197751797585
				],
				[
					-107.89615280326916,
					-194.73939774248572
				],
				[
					-109.21195954477253,
					-197.37101122549234
				],
				[
					-109.21195954477253,
					-198.6868179669956
				],
				[
					-109.21195954477253,
					-198.6868179669956
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 51,
			"versionNonce": 113231257,
			"isDeleted": false,
			"id": "X-u6PiRp-KvLJ14INZSSa",
			"fillStyle": "hachure",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -202.448926265301,
			"y": -724.3378685925476,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 288.16167638921866,
			"height": 102.63292583725604,
			"seed": 1519859840,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160948,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					-5.263226966013008,
					-1.3158067415033656
				],
				[
					-6.579033707516373,
					-2.6316134830066176
				],
				[
					-15.78968089803925,
					-5.2632269660131215
				],
				[
					-30.263555054575363,
					-10.526453932026243
				],
				[
					-40.790008986601606,
					-14.473874156536112
				],
				[
					-52.632269660131215,
					-18.421294381045982
				],
				[
					-57.89549662614445,
					-19.737101122549234
				],
				[
					-67.10614381666733,
					-23.684521347059103
				],
				[
					-71.0535640411772,
					-23.684521347059103
				],
				[
					-81.58001797320344,
					-27.631941571568973
				],
				[
					-94.7380853882363,
					-31.579361796078842
				],
				[
					-107.89615280326905,
					-36.842588762091964
				],
				[
					-117.10679999379204,
					-39.47420224509847
				],
				[
					-134.21228763333465,
					-46.053235952614955
				],
				[
					-151.31777527287738,
					-53.94807640163458
				],
				[
					-177.633910102943,
					-61.84291685065432
				],
				[
					-192.1077842594791,
					-67.10614381666744
				],
				[
					-218.4239190895447,
					-76.31679100719043
				],
				[
					-231.58198650457757,
					-80.26421123170019
				],
				[
					-246.05586066111368,
					-85.52743819771331
				],
				[
					-257.8981213346432,
					-89.47485842222318
				],
				[
					-263.1613483006563,
					-92.1064719052298
				],
				[
					-268.4245752666694,
					-93.42227864673305
				],
				[
					-273.68780223268254,
					-96.05389212973955
				],
				[
					-276.31941571568916,
					-97.36969887124292
				],
				[
					-278.95102919869566,
					-98.68550561274617
				],
				[
					-280.2668359401989,
					-100.00131235424942
				],
				[
					-281.5826426817023,
					-100.00131235424942
				],
				[
					-286.8458696477154,
					-101.31711909575279
				],
				[
					-288.16167638921866,
					-102.63292583725604
				],
				[
					-288.16167638921866,
					-102.63292583725604
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 32,
			"versionNonce": 440122487,
			"isDeleted": false,
			"id": "0dxRwRKDCtnxaypg6zVWw",
			"fillStyle": "hachure",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -16.920175713338267,
			"y": -526.9668573670554,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 35.5267820205886,
			"height": 142.1071280823544,
			"seed": 654579840,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160948,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					0,
					-2.631613483006504
				],
				[
					0,
					-10.526453932026243
				],
				[
					2.631613483006504,
					-22.36871460555585
				],
				[
					7.894840449019739,
					-50.00065617712471
				],
				[
					11.842260673529609,
					-68.42195055817069
				],
				[
					15.789680898039478,
					-88.15905168071993
				],
				[
					22.36871460555585,
					-107.89615280326916
				],
				[
					28.947748313072225,
					-128.94906066732165
				],
				[
					32.895168537582094,
					-134.21228763333477
				],
				[
					34.21097527908523,
					-138.15970785784464
				],
				[
					35.5267820205886,
					-142.1071280823544
				],
				[
					35.5267820205886,
					-142.1071280823544
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 55,
			"versionNonce": 96840313,
			"isDeleted": false,
			"id": "A-1318v8gNUzmRS2HBXBK",
			"fillStyle": "hachure",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -30.446014613196667,
			"y": -59.017346369287,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 18.52774916756198,
			"height": 343.30829339894314,
			"seed": 1908170624,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160948,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					-1.0898675980918142,
					0
				],
				[
					-1.0898675980918142,
					-6.53920558855134
				],
				[
					-2.1797351961836284,
					-30.51629274657273
				],
				[
					-2.1797351961836284,
					-52.31364470841038
				],
				[
					-4.359470392367484,
					-78.47046706261563
				],
				[
					-4.359470392367484,
					-101.35768662254509
				],
				[
					-5.4493379904592985,
					-139.50305255576097
				],
				[
					-6.53920558855134,
					-166.74974250805803
				],
				[
					-7.629073186643154,
					-184.1876240775282
				],
				[
					-7.629073186643154,
					-200.53563804890643
				],
				[
					-7.629073186643154,
					-213.614049226009
				],
				[
					-7.629073186643154,
					-232.1417983935711
				],
				[
					-7.629073186643154,
					-240.86073917830618
				],
				[
					-5.4493379904592985,
					-252.84928275731681
				],
				[
					-4.359470392367484,
					-259.38848834586815
				],
				[
					-2.1797351961836284,
					-271.3770319248788
				],
				[
					0,
					-279.00610511152206
				],
				[
					1.0898675980918142,
					-283.36557550388954
				],
				[
					2.179735196183856,
					-288.81491349434896
				],
				[
					4.359470392367484,
					-294.26425148480837
				],
				[
					6.53920558855134,
					-301.8933246714515
				],
				[
					8.718940784735196,
					-304.0730598676354
				],
				[
					8.718940784735196,
					-308.43253026000286
				],
				[
					8.718940784735196,
					-311.70213305427853
				],
				[
					9.80880838282701,
					-317.15147104473795
				],
				[
					9.80880838282701,
					-319.3312062409217
				],
				[
					10.898675980918824,
					-324.7805442313811
				],
				[
					10.898675980918824,
					-326.9602794275649
				],
				[
					10.898675980918824,
					-331.3197498199324
				],
				[
					10.898675980918824,
					-335.6792202122999
				],
				[
					10.898675980918824,
					-338.9488230065756
				],
				[
					9.80880838282701,
					-340.03869060466747
				],
				[
					9.80880838282701,
					-342.21842580085126
				],
				[
					9.80880838282701,
					-343.30829339894314
				],
				[
					9.80880838282701,
					-343.30829339894314
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 39,
			"versionNonce": 1654330775,
			"isDeleted": false,
			"id": "JuuKPANn42PBSWOfN1VRS",
			"fillStyle": "hachure",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -1681.9457054593286,
			"y": 23.622189817666595,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 244.17915607206896,
			"height": 8.988189794063942,
			"seed": 723564672,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160948,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					-5.99212652937581,
					0
				],
				[
					-8.9881897940636,
					0
				],
				[
					-14.980316323439638,
					0
				],
				[
					-23.968506117503694,
					0
				],
				[
					-46.43898060266338,
					-2.9960632646880185
				],
				[
					-71.90551835251108,
					-5.992126529375923
				],
				[
					-97.37205610235878,
					-7.490158161719933
				],
				[
					-124.3366254845505,
					-7.490158161719933
				],
				[
					-155.79528976377424,
					-8.988189794063942
				],
				[
					-178.26576424893392,
					-8.988189794063942
				],
				[
					-194.74411220471757,
					-8.988189794063942
				],
				[
					-203.73230199878162,
					-8.988189794063942
				],
				[
					-217.21458668987748,
					-8.988189794063942
				],
				[
					-230.69687138097333,
					-8.988189794063942
				],
				[
					-233.69293464566135,
					-8.988189794063942
				],
				[
					-239.68506117503716,
					-8.988189794063942
				],
				[
					-242.68112443972518,
					-8.988189794063942
				],
				[
					-244.17915607206896,
					-8.988189794063942
				],
				[
					-244.17915607206896,
					-8.988189794063942
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 45,
			"versionNonce": 2021389145,
			"isDeleted": false,
			"id": "VDgcGLWwCpiMeej0G-07q",
			"fillStyle": "hachure",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -612.3511199657244,
			"y": 23.622189817666595,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 284.626010145357,
			"height": 10.486221426407837,
			"seed": 861890688,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160948,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					-2.9960632646880185,
					1.4980316323440093
				],
				[
					-8.988189794064056,
					1.4980316323440093
				],
				[
					-16.478347955783875,
					2.9960632646880185
				],
				[
					-23.968506117503694,
					2.9960632646880185
				],
				[
					-47.937012235007614,
					4.494094897031914
				],
				[
					-64.41536019079126,
					4.494094897031914
				],
				[
					-82.39173977891915,
					5.992126529375923
				],
				[
					-98.87008773470302,
					5.992126529375923
				],
				[
					-121.3405622198627,
					5.992126529375923
				],
				[
					-148.30513160205442,
					5.992126529375923
				],
				[
					-170.7756060872141,
					7.490158161719933
				],
				[
					-191.74804894003,
					7.490158161719933
				],
				[
					-208.22639689581365,
					7.490158161719933
				],
				[
					-229.19883974862955,
					8.988189794063942
				],
				[
					-238.18702954269338,
					8.988189794063942
				],
				[
					-251.66931423378924,
					8.988189794063942
				],
				[
					-257.6614407631653,
					8.988189794063942
				],
				[
					-266.6496305572291,
					10.486221426407837
				],
				[
					-272.6417570866049,
					10.486221426407837
				],
				[
					-277.13585198363694,
					10.486221426407837
				],
				[
					-278.63388361598095,
					10.486221426407837
				],
				[
					-281.62994688066897,
					10.486221426407837
				],
				[
					-283.127978513013,
					10.486221426407837
				],
				[
					-284.626010145357,
					10.486221426407837
				],
				[
					-284.626010145357,
					10.486221426407837
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 39,
			"versionNonce": 1408387767,
			"isDeleted": false,
			"id": "JCmoDV1FnDbclItd6sA3G",
			"fillStyle": "hachure",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1384.525045948804,
			"y": 100.0218030672097,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 38.94882244094356,
			"height": 242.6811244397254,
			"seed": 1931345792,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160948,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					0,
					8.988189794063942
				],
				[
					1.4980316323440093,
					14.980316323439865
				],
				[
					2.9960632646880185,
					28.46260101453572
				],
				[
					5.99212652937581,
					44.940948970319596
				],
				[
					7.490158161719819,
					67.41142345547928
				],
				[
					11.984253058751847,
					103.36418263173482
				],
				[
					19.474411220471666,
					143.8110367050224
				],
				[
					25.466537749847703,
					175.26970098424613
				],
				[
					28.46260101453572,
					194.7441122047178
				],
				[
					32.95669591156752,
					215.7165550575337
				],
				[
					34.45472754391153,
					223.20671321925352
				],
				[
					35.95275917625554,
					232.19490301331734
				],
				[
					37.45079080859955,
					235.19096627800536
				],
				[
					37.45079080859955,
					236.68899791034937
				],
				[
					37.45079080859955,
					238.18702954269338
				],
				[
					37.45079080859955,
					239.6850611750374
				],
				[
					38.94882244094356,
					241.1830928073814
				],
				[
					38.94882244094356,
					242.6811244397254
				],
				[
					38.94882244094356,
					242.6811244397254
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 32,
			"versionNonce": 1396056121,
			"isDeleted": false,
			"id": "Ra1o_tcv-PNVLEWErUz9W",
			"fillStyle": "hachure",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1508.8616714333548,
			"y": 56.57888572923423,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 173.7716693519019,
			"height": 5.992126529375923,
			"seed": 640884608,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160948,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					4.494094897032028,
					0
				],
				[
					10.48622142640761,
					0
				],
				[
					20.972442852815675,
					0
				],
				[
					37.45079080859932,
					-2.996063264687905
				],
				[
					55.42717039672743,
					-4.494094897031914
				],
				[
					91.37992957298275,
					-5.992126529375923
				],
				[
					103.36418263173482,
					-5.992126529375923
				],
				[
					125.8346571168945,
					-5.992126529375923
				],
				[
					146.80709996971018,
					-5.992126529375923
				],
				[
					167.77954282252585,
					-5.992126529375923
				],
				[
					173.7716693519019,
					-5.992126529375923
				],
				[
					173.7716693519019,
					-5.992126529375923
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 34,
			"versionNonce": 988142551,
			"isDeleted": false,
			"id": "Nf9LVEBFCe-y1yFG1NVJD",
			"fillStyle": "hachure",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1471.410880624755,
			"y": 28.11628471469851,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 250.17128260144545,
			"height": 257.66144076316505,
			"seed": 2116165504,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160948,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					2.9960632646880185,
					-2.996063264687905
				],
				[
					11.984253058751847,
					-13.482284691095856
				],
				[
					28.46260101453572,
					-31.458664279223626
				],
				[
					46.43898060266338,
					-47.93701223500739
				],
				[
					94.37599283767122,
					-95.87402447001489
				],
				[
					124.3366254845505,
					-125.8346571168945
				],
				[
					157.29332139611824,
					-154.29725813143023
				],
				[
					185.75592241065397,
					-181.26182751362194
				],
				[
					221.70868158690973,
					-220.2106499545655
				],
				[
					235.19096627800536,
					-236.68899791034926
				],
				[
					245.67718770441343,
					-248.67325096910122
				],
				[
					248.67325096910145,
					-254.66537749847714
				],
				[
					250.17128260144545,
					-257.66144076316505
				],
				[
					250.17128260144545,
					-257.66144076316505
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 58,
			"versionNonce": 869773593,
			"isDeleted": false,
			"id": "MgVjKhaPR1rt5GGvjOewA",
			"fillStyle": "hachure",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 824.2612154521544,
			"y": 29.614316347042518,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 247.1752193367572,
			"height": 5.992126529375923,
			"seed": 1228382080,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160948,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					4.4940948970318,
					0
				],
				[
					11.984253058751847,
					0
				],
				[
					20.972442852815675,
					1.4980316323440093
				],
				[
					28.46260101453572,
					1.4980316323440093
				],
				[
					38.94882244094356,
					1.4980316323440093
				],
				[
					67.41142345547928,
					1.4980316323440093
				],
				[
					82.39173977891915,
					1.4980316323440093
				],
				[
					97.37205610235878,
					1.4980316323440093
				],
				[
					119.8425305875187,
					1.4980316323440093
				],
				[
					131.82678364627054,
					1.4980316323440093
				],
				[
					146.8070999697104,
					1.4980316323440093
				],
				[
					154.29725813143023,
					1.4980316323440093
				],
				[
					161.78741629315005,
					1.4980316323440093
				],
				[
					166.28151119018207,
					1.4980316323440093
				],
				[
					172.2736377195581,
					1.4980316323440093
				],
				[
					176.7677326165899,
					1.4980316323440093
				],
				[
					179.76379588127793,
					1.4980316323440093
				],
				[
					184.25789077830996,
					1.4980316323440093
				],
				[
					187.25395404299775,
					1.4980316323440093
				],
				[
					191.74804894002978,
					1.4980316323440093
				],
				[
					194.7441122047178,
					1.4980316323440093
				],
				[
					197.7401754694058,
					2.9960632646880185
				],
				[
					199.23820710174982,
					2.9960632646880185
				],
				[
					202.2342703664376,
					2.9960632646880185
				],
				[
					205.23033363112563,
					2.9960632646880185
				],
				[
					208.22639689581365,
					2.9960632646880185
				],
				[
					211.22246016050167,
					2.9960632646880185
				],
				[
					217.21458668987748,
					2.9960632646880185
				],
				[
					220.2106499545655,
					4.494094897031914
				],
				[
					226.2027764839413,
					4.494094897031914
				],
				[
					229.19883974862933,
					4.494094897031914
				],
				[
					233.69293464566135,
					4.494094897031914
				],
				[
					238.18702954269338,
					4.494094897031914
				],
				[
					241.18309280738117,
					4.494094897031914
				],
				[
					244.1791560720692,
					5.992126529375923
				],
				[
					245.6771877044132,
					5.992126529375923
				],
				[
					247.1752193367572,
					5.992126529375923
				],
				[
					247.1752193367572,
					5.992126529375923
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 36,
			"versionNonce": 1535789303,
			"isDeleted": false,
			"id": "5xeB6GoyLSWBOVa_PtNTF",
			"fillStyle": "hachure",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -646.8058475096371,
			"y": 651.2974437697956,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 82.39173977891903,
			"height": 110.85434079345475,
			"seed": 589711488,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160948,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					0,
					2.996063264687905
				],
				[
					1.4980316323440093,
					8.988189794063828
				],
				[
					4.494094897031914,
					13.482284691095856
				],
				[
					7.490158161719933,
					19.47441122047178
				],
				[
					10.486221426407951,
					23.968506117503694
				],
				[
					19.47441122047178,
					37.45079080859955
				],
				[
					22.470474485159798,
					44.94094897031948
				],
				[
					26.964569382191712,
					50.933075499695406
				],
				[
					32.956695911567635,
					58.42323366141534
				],
				[
					41.944885705631464,
					65.91339182313527
				],
				[
					58.42323366141534,
					85.38780304360705
				],
				[
					67.41142345547917,
					95.87402447001489
				],
				[
					73.4035499848552,
					100.3681193670468
				],
				[
					77.89764488188712,
					106.36024589642273
				],
				[
					82.39173977891903,
					110.85434079345475
				],
				[
					82.39173977891903,
					110.85434079345475
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 47,
			"versionNonce": 802432505,
			"isDeleted": false,
			"id": "ntIpquorHNXIJBIBIb197",
			"fillStyle": "hachure",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -474.53220979007904,
			"y": 880.496283518425,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 164.78347955783806,
			"height": 182.75985914596606,
			"seed": 834082944,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160948,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					0,
					1.4980316323438956
				],
				[
					2.996063264687905,
					4.494094897031914
				],
				[
					7.490158161719933,
					7.490158161719819
				],
				[
					10.486221426407837,
					11.984253058751847
				],
				[
					16.47834795578376,
					17.97637958812777
				],
				[
					23.968506117503694,
					26.9645693821916
				],
				[
					37.45079080859955,
					41.94488570563158
				],
				[
					43.44291733797547,
					49.435043867351396
				],
				[
					56.92520202907133,
					64.41536019079126
				],
				[
					68.90945508782318,
					79.39567651423113
				],
				[
					88.38386630829496,
					98.87008773470279
				],
				[
					101.86615099939081,
					113.85040405814266
				],
				[
					112.35237242579865,
					124.3366254845505
				],
				[
					121.34056221986259,
					133.32481527861455
				],
				[
					127.33268874923851,
					140.81497344033437
				],
				[
					133.32481527861444,
					146.8070999697103
				],
				[
					136.32087854330246,
					151.30119486674232
				],
				[
					140.81497344033437,
					155.79528976377435
				],
				[
					143.8110367050224,
					158.79135302846237
				],
				[
					145.30906833736628,
					161.78741629314993
				],
				[
					149.8031632343983,
					166.28151119018196
				],
				[
					157.29332139611824,
					173.771669351902
				],
				[
					160.28938466080615,
					176.76773261659002
				],
				[
					161.78741629315016,
					178.26576424893403
				],
				[
					163.28544792549417,
					181.26182751362205
				],
				[
					164.78347955783806,
					182.75985914596606
				],
				[
					164.78347955783806,
					182.75985914596606
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 61,
			"versionNonce": 56889879,
			"isDeleted": false,
			"id": "8ksxjl-bFk_fa6PkrNVoj",
			"fillStyle": "hachure",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 40.790671736251056,
			"y": 1093.2167753112708,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 154.29725813143045,
			"height": 8.988189794064056,
			"seed": 73058432,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160948,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					1.4980316323440093,
					0
				],
				[
					2.9960632646880185,
					0
				],
				[
					4.494094897032028,
					0
				],
				[
					5.992126529376037,
					0
				],
				[
					8.988189794064056,
					0
				],
				[
					11.984253058751847,
					0
				],
				[
					16.478347955783875,
					0
				],
				[
					19.474411220471893,
					0
				],
				[
					26.964569382191712,
					0
				],
				[
					32.95669591156775,
					0
				],
				[
					38.94882244094356,
					0
				],
				[
					43.44291733797559,
					0
				],
				[
					53.929138764383424,
					-1.4980316323440093
				],
				[
					62.91732855844748,
					-1.4980316323440093
				],
				[
					67.41142345547928,
					-1.4980316323440093
				],
				[
					74.90158161719933,
					-2.9960632646880185
				],
				[
					77.89764488188712,
					-2.9960632646880185
				],
				[
					82.39173977891915,
					-2.9960632646880185
				],
				[
					83.88977141126315,
					-2.9960632646880185
				],
				[
					85.38780304360716,
					-2.9960632646880185
				],
				[
					88.38386630829518,
					-2.9960632646880185
				],
				[
					89.88189794063919,
					-2.9960632646880185
				],
				[
					92.87796120532698,
					-2.9960632646880185
				],
				[
					94.37599283767099,
					-2.9960632646880185
				],
				[
					97.37205610235901,
					-2.9960632646880185
				],
				[
					98.87008773470302,
					-2.9960632646880185
				],
				[
					101.86615099939104,
					-2.9960632646880185
				],
				[
					104.86221426407883,
					-2.9960632646880185
				],
				[
					107.85827752876685,
					-2.9960632646880185
				],
				[
					115.3484356904869,
					-2.9960632646880185
				],
				[
					119.8425305875187,
					-2.9960632646880185
				],
				[
					122.83859385220671,
					-2.9960632646880185
				],
				[
					128.83072038158275,
					-4.494094897032028
				],
				[
					134.82284691095856,
					-5.992126529376037
				],
				[
					137.81891017564658,
					-5.992126529376037
				],
				[
					140.8149734403346,
					-5.992126529376037
				],
				[
					146.8070999697104,
					-7.490158161720046
				],
				[
					151.30119486674243,
					-8.988189794064056
				],
				[
					152.79922649908644,
					-8.988189794064056
				],
				[
					154.29725813143045,
					-8.988189794064056
				],
				[
					154.29725813143045,
					-8.988189794064056
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 33,
			"versionNonce": 1647247065,
			"isDeleted": false,
			"id": "W4Q1KKQVzB2a7uYfuOYWP",
			"fillStyle": "hachure",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 175.61351864720962,
			"y": 901.4687263712407,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 70.4074867201673,
			"height": 98.87008773470302,
			"seed": 2142156928,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160948,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					0,
					1.4980316323440093
				],
				[
					5.992126529376037,
					7.490158161719933
				],
				[
					10.486221426407837,
					11.98425305875196
				],
				[
					14.980316323439865,
					19.474411220471893
				],
				[
					20.972442852815675,
					26.964569382191712
				],
				[
					46.438980602663605,
					53.929138764383424
				],
				[
					56.92520202907144,
					68.90945508782329
				],
				[
					64.41536019079126,
					80.89370814657514
				],
				[
					67.41142345547928,
					88.38386630829496
				],
				[
					70.4074867201673,
					94.37599283767099
				],
				[
					70.4074867201673,
					97.37205610235901
				],
				[
					70.4074867201673,
					98.87008773470302
				],
				[
					70.4074867201673,
					98.87008773470302
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 45,
			"versionNonce": 1533523767,
			"isDeleted": false,
			"id": "6ZYY-zhfCHspfuUt_g0XA",
			"fillStyle": "hachure",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -5.6483088664123215,
			"y": 923.9392008564004,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 59.92126529375935,
			"height": 130.32875201392665,
			"seed": 116461440,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160948,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					0,
					1.4980316323440093
				],
				[
					-4.494094897031914,
					7.490158161720046
				],
				[
					-8.988189794063942,
					16.478347955783875
				],
				[
					-17.97637958812777,
					32.95669591156775
				],
				[
					-23.968506117503694,
					44.940948970319596
				],
				[
					-31.458664279223626,
					62.91732855844748
				],
				[
					-35.952759176255654,
					73.40354998485532
				],
				[
					-41.94488570563158,
					88.38386630829518
				],
				[
					-44.94094897031948,
					94.37599283767099
				],
				[
					-46.43898060266349,
					98.87008773470302
				],
				[
					-49.43504386735151,
					104.86221426407894
				],
				[
					-49.43504386735151,
					107.85827752876696
				],
				[
					-52.431107132039415,
					112.35237242579899
				],
				[
					-53.929138764383424,
					115.34843569048701
				],
				[
					-53.929138764383424,
					116.84646732283102
				],
				[
					-55.42717039672743,
					119.84253058751858
				],
				[
					-56.92520202907133,
					121.34056221986259
				],
				[
					-56.92520202907133,
					122.8385938522066
				],
				[
					-56.92520202907133,
					124.33662548455061
				],
				[
					-58.42323366141534,
					125.83465711689462
				],
				[
					-58.42323366141534,
					127.33268874923863
				],
				[
					-59.92126529375935,
					128.83072038158264
				],
				[
					-59.92126529375935,
					130.32875201392665
				],
				[
					-59.92126529375935,
					130.32875201392665
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 53,
			"versionNonce": 964410297,
			"isDeleted": false,
			"id": "oy3P-1LTkE_1s_RmD_1_1",
			"fillStyle": "hachure",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 19.81822888343538,
			"y": 516.474596858837,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 10.486221426407837,
			"height": 205.23033363112575,
			"seed": 1348792192,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160948,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					1.4980316323440093,
					1.4980316323440093
				],
				[
					2.9960632646880185,
					8.988189794063942
				],
				[
					2.9960632646880185,
					17.976379588127884
				],
				[
					2.9960632646880185,
					25.466537749847703
				],
				[
					2.9960632646880185,
					32.956695911567635
				],
				[
					2.9960632646880185,
					47.9370122350075
				],
				[
					4.494094897032028,
					62.917328558447366
				],
				[
					4.494094897032028,
					71.9055183525112
				],
				[
					5.992126529376037,
					89.88189794063908
				],
				[
					7.490158161719819,
					101.86615099939092
				],
				[
					7.490158161719819,
					109.35630916111086
				],
				[
					8.988189794063828,
					122.83859385220671
				],
				[
					8.988189794063828,
					130.32875201392653
				],
				[
					10.486221426407837,
					137.81891017564647
				],
				[
					10.486221426407837,
					143.8110367050224
				],
				[
					10.486221426407837,
					154.29725813143034
				],
				[
					10.486221426407837,
					161.78741629315027
				],
				[
					10.486221426407837,
					167.7795428225262
				],
				[
					10.486221426407837,
					173.77166935190212
				],
				[
					10.486221426407837,
					179.76379588127804
				],
				[
					10.486221426407837,
					187.25395404299798
				],
				[
					10.486221426407837,
					188.75198567534187
				],
				[
					10.486221426407837,
					191.7480489400299
				],
				[
					10.486221426407837,
					193.2460805723739
				],
				[
					10.486221426407837,
					194.7441122047179
				],
				[
					10.486221426407837,
					196.2421438370618
				],
				[
					10.486221426407837,
					197.7401754694058
				],
				[
					10.486221426407837,
					200.73623873409383
				],
				[
					10.486221426407837,
					202.23427036643773
				],
				[
					10.486221426407837,
					203.73230199878174
				],
				[
					10.486221426407837,
					205.23033363112575
				],
				[
					10.486221426407837,
					205.23033363112575
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 36,
			"versionNonce": 2046408791,
			"isDeleted": false,
			"id": "b_HMW4yxbmNivxM6HuKYH",
			"fillStyle": "hachure",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -270.7999077912974,
			"y": 732.1911519163706,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 214.2185234251897,
			"height": 215.71655505753358,
			"seed": 1033625472,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160949,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					10.486221426407951,
					-11.984253058751847
				],
				[
					28.46260101453572,
					-29.960632646879617
				],
				[
					49.43504386735151,
					-52.431107132039415
				],
				[
					67.41142345547928,
					-73.40354998485509
				],
				[
					110.85434079345475,
					-113.85040405814266
				],
				[
					130.32875201392665,
					-134.82284691095845
				],
				[
					146.8070999697104,
					-149.8031632343983
				],
				[
					166.2815111901822,
					-167.77954282252608
				],
				[
					185.75592241065397,
					-185.75592241065385
				],
				[
					197.7401754694058,
					-197.7401754694057
				],
				[
					203.73230199878174,
					-203.73230199878174
				],
				[
					209.72442852815766,
					-209.72442852815766
				],
				[
					212.72049179284568,
					-212.72049179284556
				],
				[
					214.2185234251897,
					-215.71655505753358
				],
				[
					214.2185234251897,
					-215.71655505753358
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 52,
			"versionNonce": 98426009,
			"isDeleted": false,
			"id": "ZAR-JCQBn2V0iI59awVfS",
			"fillStyle": "hachure",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -152.45540883612273,
			"y": 483.51790094726937,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 350.53940196849203,
			"height": 112.35237242579876,
			"seed": 606064512,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160949,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					-7.490158161719933,
					2.9960632646880185
				],
				[
					-13.482284691095856,
					2.9960632646880185
				],
				[
					-34.45472754391153,
					10.486221426407951
				],
				[
					-53.92913876438331,
					17.976379588127884
				],
				[
					-82.39173977891903,
					26.964569382191712
				],
				[
					-106.36024589642273,
					34.454727543911645
				],
				[
					-133.32481527861444,
					43.44291733797559
				],
				[
					-169.2775744548701,
					56.92520202907144
				],
				[
					-196.2421438370618,
					65.91339182313527
				],
				[
					-208.22639689581365,
					70.4074867201673
				],
				[
					-229.19883974862944,
					77.89764488188712
				],
				[
					-253.16734586613313,
					83.88977141126315
				],
				[
					-269.6456938219169,
					88.38386630829507
				],
				[
					-277.1358519836368,
					91.37992957298297
				],
				[
					-284.62601014535676,
					92.87796120532698
				],
				[
					-290.6181366747327,
					95.874024470015
				],
				[
					-301.10435810114063,
					98.8700877347029
				],
				[
					-307.09648463051656,
					100.36811936704692
				],
				[
					-314.5866427922364,
					103.36418263173493
				],
				[
					-317.5827060569244,
					104.86221426407883
				],
				[
					-319.0807376892684,
					104.86221426407883
				],
				[
					-322.0768009539563,
					104.86221426407883
				],
				[
					-323.5748325863003,
					106.36024589642284
				],
				[
					-328.06892748333223,
					106.36024589642284
				],
				[
					-332.56302238036426,
					107.85827752876685
				],
				[
					-338.5551489097402,
					109.35630916111086
				],
				[
					-346.0453070714601,
					110.85434079345475
				],
				[
					-349.041370336148,
					110.85434079345475
				],
				[
					-350.53940196849203,
					110.85434079345475
				],
				[
					-350.53940196849203,
					112.35237242579876
				],
				[
					-350.53940196849203,
					112.35237242579876
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "freedraw",
			"version": 57,
			"versionNonce": 888051063,
			"isDeleted": false,
			"id": "67F5B-FILJiBKbOogmyjX",
			"fillStyle": "hachure",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 46.78279826562709,
			"y": 91.03361327314582,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 26.964569382191712,
			"height": 302.6023897334846,
			"seed": 171405184,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160949,
			"link": null,
			"locked": false,
			"customData": {
				"strokeOptions": {
					"highlighter": true,
					"constantPressure": true,
					"hasOutline": false,
					"outlineWidth": 1,
					"options": {
						"thinning": 1,
						"smoothing": 0.5,
						"streamline": 0.5,
						"easing": "linear",
						"start": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						},
						"end": {
							"cap": true,
							"taper": true,
							"easing": "linear"
						}
					}
				}
			},
			"points": [
				[
					0,
					0
				],
				[
					0,
					4.4940948970319425
				],
				[
					0,
					20.97244285281576
				],
				[
					0,
					28.462601014535664
				],
				[
					0,
					41.94488570563152
				],
				[
					0,
					58.42323366141534
				],
				[
					0,
					68.90945508782323
				],
				[
					0,
					95.87402447001494
				],
				[
					0,
					115.34843569048672
				],
				[
					0,
					127.33268874923857
				],
				[
					0,
					139.31694180799042
				],
				[
					-1.4980316323440093,
					164.78347955783812
				],
				[
					-2.9960632646880185,
					178.26576424893398
				],
				[
					-7.490158161720046,
					194.7441122047178
				],
				[
					-8.988189794063828,
					203.73230199878174
				],
				[
					-11.984253058751847,
					215.71655505753358
				],
				[
					-13.482284691095856,
					224.70474485159747
				],
				[
					-16.478347955783875,
					236.68899791034931
				],
				[
					-16.478347955783875,
					242.6811244397253
				],
				[
					-19.474411220471893,
					248.67325096910122
				],
				[
					-19.474411220471893,
					256.1634091308211
				],
				[
					-20.972442852815675,
					259.1594723955091
				],
				[
					-20.972442852815675,
					263.653567292541
				],
				[
					-22.470474485159684,
					266.649630557229
				],
				[
					-22.470474485159684,
					272.6417570866049
				],
				[
					-22.470474485159684,
					274.1397887189489
				],
				[
					-22.470474485159684,
					278.6338836159809
				],
				[
					-23.968506117503694,
					283.1279785130128
				],
				[
					-23.968506117503694,
					287.6220734100448
				],
				[
					-25.466537749847703,
					292.1161683070767
				],
				[
					-25.466537749847703,
					293.6141999394207
				],
				[
					-25.466537749847703,
					295.1122315717647
				],
				[
					-25.466537749847703,
					296.61026320410866
				],
				[
					-25.466537749847703,
					299.6063264687966
				],
				[
					-26.964569382191712,
					301.10435810114063
				],
				[
					-26.964569382191712,
					302.6023897334846
				],
				[
					-26.964569382191712,
					302.6023897334846
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": false,
			"pressures": [
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				1,
				0
			]
		},
		{
			"type": "text",
			"version": 166,
			"versionNonce": 1191764345,
			"isDeleted": false,
			"id": "0Sxsd4xa",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -575.5128205128206,
			"y": -17.806290064102484,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 1331.2435302734375,
			"height": 90,
			"seed": 328390784,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160949,
			"link": null,
			"locked": false,
			"fontSize": 36,
			"fontFamily": 1,
			"text": "Kann die Anwendung von Document Understanding Transformers \ndie Effizienz und Genauigkeit der Verarbeitung von Dokumenten verbessern?",
			"rawText": "Kann die Anwendung von Document Understanding Transformers \ndie Effizienz und Genauigkeit der Verarbeitung von Dokumenten verbessern?",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Kann die Anwendung von Document Understanding Transformers \ndie Effizienz und Genauigkeit der Verarbeitung von Dokumenten verbessern?",
			"lineHeight": 1.25,
			"baseline": 77
		},
		{
			"type": "text",
			"version": 61,
			"versionNonce": 318645624,
			"isDeleted": false,
			"id": "Ftfc8Y7j",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -66.66234605715522,
			"y": -485.45001163014047,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 95.64793395996094,
			"height": 35,
			"seed": 2047336320,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1711005973589,
			"link": null,
			"locked": false,
			"fontSize": 28,
			"fontFamily": 1,
			"text": "Pipeline",
			"rawText": "Pipeline",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Pipeline",
			"lineHeight": 1.25,
			"baseline": 24
		},
		{
			"type": "text",
			"version": 209,
			"versionNonce": 1065029128,
			"isDeleted": false,
			"id": "hMLVEAaB",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -1660.5642587132443,
			"y": -23.912217287832163,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 712.963623046875,
			"height": 105,
			"seed": 557875072,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1711005973589,
			"link": null,
			"locked": false,
			"fontSize": 28,
			"fontFamily": 1,
			"text": "Analyse: Wie können Donuts\nauf die Interpretation visueller/layoutbasierter\nund textueller Elemente in Docs angewandt werden?",
			"rawText": "Analyse: Wie können Donuts\nauf die Interpretation visueller/layoutbasierter\nund textueller Elemente in Docs angewandt werden?",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Analyse: Wie können Donuts\nauf die Interpretation visueller/layoutbasierter\nund textueller Elemente in Docs angewandt werden?",
			"lineHeight": 1.25,
			"baseline": 94
		},
		{
			"type": "text",
			"version": 104,
			"versionNonce": 1409988216,
			"isDeleted": false,
			"id": "F5S1SapX",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1110.4351062721353,
			"y": 21.004740339297882,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 338.9678955078125,
			"height": 35,
			"seed": 2112786304,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1711005973590,
			"link": null,
			"locked": false,
			"fontSize": 28,
			"fontFamily": 1,
			"text": "Vergleich OCR und Donut",
			"rawText": "Vergleich OCR und Donut",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Vergleich OCR und Donut",
			"lineHeight": 1.25,
			"baseline": 24
		},
		{
			"type": "text",
			"version": 143,
			"versionNonce": 744424510,
			"isDeleted": false,
			"id": "FNph8gTi",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1264.4423007128742,
			"y": 362.45665815953294,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 226.60389709472656,
			"height": 35,
			"seed": 388943744,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1712354013753,
			"link": "[[Metriken]]",
			"locked": false,
			"fontSize": 28,
			"fontFamily": 1,
			"text": "Welche Metriken?",
			"rawText": "Welche Metriken?",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Welche Metriken?",
			"lineHeight": 1.25,
			"baseline": 24
		},
		{
			"type": "text",
			"version": 125,
			"versionNonce": 1197287288,
			"isDeleted": false,
			"id": "T0LGSDBJ",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1700.0117159545707,
			"y": 34.31393045021434,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 230.8319091796875,
			"height": 35,
			"seed": 1872054400,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1711005973590,
			"link": null,
			"locked": false,
			"fontSize": 28,
			"fontFamily": 1,
			"text": "Ist Vergleichbar?",
			"rawText": "Ist Vergleichbar?",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Ist Vergleichbar?",
			"lineHeight": 1.25,
			"baseline": 24
		},
		{
			"type": "text",
			"version": 68,
			"versionNonce": 1174744072,
			"isDeleted": false,
			"id": "Fx0f99RY",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1715.4136428165607,
			"y": -323.1197983979015,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 283.38787841796875,
			"height": 35,
			"seed": 1802426496,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1711005973590,
			"link": null,
			"locked": false,
			"fontSize": 28,
			"fontFamily": 1,
			"text": "Nur kleiner Abschnitt",
			"rawText": "Nur kleiner Abschnitt",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Nur kleiner Abschnitt",
			"lineHeight": 1.25,
			"baseline": 24
		},
		{
			"type": "text",
			"version": 161,
			"versionNonce": 1765374072,
			"isDeleted": false,
			"id": "6skFYu1f",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -2287.1882559303695,
			"y": -26.643761349874808,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 337.931884765625,
			"height": 70,
			"seed": 1759018880,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1711005973590,
			"link": null,
			"locked": false,
			"fontSize": 28,
			"fontFamily": 1,
			"text": "Vergleich Donuts zu CNN\nsind sie vergleichbar?",
			"rawText": "Vergleich Donuts zu CNN\nsind sie vergleichbar?",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Vergleich Donuts zu CNN\nsind sie vergleichbar?",
			"lineHeight": 1.25,
			"baseline": 59
		},
		{
			"type": "text",
			"version": 129,
			"versionNonce": 2073193224,
			"isDeleted": false,
			"id": "4SAe5j5u",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -128.42089805901503,
			"y": 444.7543197406004,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 289.6318664550781,
			"height": 35,
			"seed": 648001664,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1711005973590,
			"link": null,
			"locked": false,
			"fontSize": 28,
			"fontFamily": 1,
			"text": "Zur Forschungsfrage:",
			"rawText": "Zur Forschungsfrage:",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Zur Forschungsfrage:",
			"lineHeight": 1.25,
			"baseline": 24
		},
		{
			"type": "text",
			"version": 102,
			"versionNonce": 224635256,
			"isDeleted": false,
			"id": "FvQFSSeG",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -817.5814535968514,
			"y": 555.4234192997806,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 284.4798889160156,
			"height": 70,
			"seed": 1646083968,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1711005973590,
			"link": null,
			"locked": false,
			"fontSize": 28,
			"fontFamily": 1,
			"text": "Was ist die Methode\nder Untersuchung?",
			"rawText": "Was ist die Methode\nder Untersuchung?",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Was ist die Methode\nder Untersuchung?",
			"lineHeight": 1.25,
			"baseline": 59
		},
		{
			"type": "text",
			"version": 90,
			"versionNonce": 723503624,
			"isDeleted": false,
			"id": "ADYkBx6f",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -616.8452148627574,
			"y": 768.1439110926261,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 329.13983154296875,
			"height": 70,
			"seed": 658153344,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1711005973590,
			"link": null,
			"locked": false,
			"fontSize": 28,
			"fontFamily": 1,
			"text": "Was heißt Effizienz und\nGenauigkeit",
			"rawText": "Was heißt Effizienz und\nGenauigkeit",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Was heißt Effizienz und\nGenauigkeit",
			"lineHeight": 1.25,
			"baseline": 59
		},
		{
			"type": "text",
			"version": 82,
			"versionNonce": 1864350328,
			"isDeleted": false,
			"id": "w60xs0BQ",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -92.53414354236338,
			"y": 775.6340692543462,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 349.411865234375,
			"height": 105,
			"seed": 936294528,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1711005973590,
			"link": null,
			"locked": false,
			"fontSize": 28,
			"fontFamily": 1,
			"text": "Was ist der Status quo?\nWie werden Dokumente\nverarbeitet?",
			"rawText": "Was ist der Status quo?\nWie werden Dokumente\nverarbeitet?",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Was ist der Status quo?\nWie werden Dokumente\nverarbeitet?",
			"lineHeight": 1.25,
			"baseline": 94
		},
		{
			"type": "text",
			"version": 97,
			"versionNonce": 44675769,
			"isDeleted": false,
			"id": "lybaiNpM",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -297.764477173489,
			"y": 1072.7502375614229,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 308.499755859375,
			"height": 25,
			"seed": 584638336,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160949,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "Wie bemesse ich das Verfahren?",
			"rawText": "Wie bemesse ich das Verfahren?",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Wie bemesse ich das Verfahren?",
			"lineHeight": 1.25,
			"baseline": 18
		},
		{
			"type": "text",
			"version": 131,
			"versionNonce": 470462807,
			"isDeleted": false,
			"id": "zDA442T9",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 201.08005639705732,
			"y": 1054.2679528703263,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 304.7397766113281,
			"height": 50,
			"seed": 502775680,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160949,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "Wie komme ich an Daten?\nWie mache ich einen Benchmark?",
			"rawText": "Wie komme ich an Daten?\nWie mache ich einen Benchmark?",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Wie komme ich an Daten?\nWie mache ich einen Benchmark?",
			"lineHeight": 1.25,
			"baseline": 43
		},
		{
			"type": "text",
			"version": 74,
			"versionNonce": 70579097,
			"isDeleted": false,
			"id": "ZI2ERpPD",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -842.9863785549041,
			"y": -879.395493316485,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 311.55975341796875,
			"height": 25,
			"seed": 41070464,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160949,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "Wie implementiere ich es in ELO?",
			"rawText": "Wie implementiere ich es in ELO?",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Wie implementiere ich es in ELO?",
			"lineHeight": 1.25,
			"baseline": 18
		},
		{
			"type": "text",
			"version": 67,
			"versionNonce": 1014525559,
			"isDeleted": false,
			"id": "1diugU5G",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -354.1377747923523,
			"y": -1028.1755031572616,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 293.09979248046875,
			"height": 25,
			"seed": 2112077696,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160949,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "Wie bleiben die Daten anonym?",
			"rawText": "Wie bleiben die Daten anonym?",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Wie bleiben die Daten anonym?",
			"lineHeight": 1.25,
			"baseline": 18
		},
		{
			"type": "text",
			"version": 83,
			"versionNonce": 946149497,
			"isDeleted": false,
			"id": "lN4r6F9b",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -178.3068540714346,
			"y": -730.6154834757085,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 299.2997741699219,
			"height": 25,
			"seed": 1732429952,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160949,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "Modelltraining -> Endanwendung",
			"rawText": "Modelltraining -> Endanwendung",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Modelltraining -> Endanwendung",
			"lineHeight": 1.25,
			"baseline": 18
		},
		{
			"type": "text",
			"version": 85,
			"versionNonce": 1047627671,
			"isDeleted": false,
			"id": "YfFs7OSH",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 132.77862105018949,
			"y": -1028.175503157262,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 248.3798065185547,
			"height": 25,
			"seed": 399935616,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160949,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "Woher kommen die Daten?",
			"rawText": "Woher kommen die Daten?",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Woher kommen die Daten?",
			"lineHeight": 1.25,
			"baseline": 18
		},
		{
			"type": "text",
			"version": 113,
			"versionNonce": 1090363737,
			"isDeleted": false,
			"id": "DtWmhxNi",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 159.643643458361,
			"y": -1189.1068745501539,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 161.63987731933594,
			"height": 25,
			"seed": 1586063488,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160949,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "Vom Unternehmen",
			"rawText": "Vom Unternehmen",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Vom Unternehmen",
			"lineHeight": 1.25,
			"baseline": 18
		},
		{
			"type": "text",
			"version": 98,
			"versionNonce": 271219895,
			"isDeleted": false,
			"id": "f1XDIw1z",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 473.1440173051417,
			"y": -1138.986125126374,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 80.73995971679688,
			"height": 25,
			"seed": 985598080,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160949,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "Von ELO",
			"rawText": "Von ELO",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Von ELO",
			"lineHeight": 1.25,
			"baseline": 18
		},
		{
			"type": "text",
			"version": 70,
			"versionNonce": 995233337,
			"isDeleted": false,
			"id": "RGhKpEUS",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 90.8504579747414,
			"y": -1332.5898042731321,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 293.31976318359375,
			"height": 25,
			"seed": 345448320,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160949,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "Um eigene Daten erweiterbar?",
			"rawText": "Um eigene Daten erweiterbar?",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Um eigene Daten erweiterbar?",
			"lineHeight": 1.25,
			"baseline": 18
		},
		{
			"type": "text",
			"version": 73,
			"versionNonce": 1699204567,
			"isDeleted": false,
			"id": "HO5myDMu",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 392.2957208941825,
			"y": -820.3917607222871,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 229.67979431152344,
			"height": 50,
			"seed": 651202432,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160949,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "Ab wie viel Input\nperformt das Ding gut?",
			"rawText": "Ab wie viel Input\nperformt das Ding gut?",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Ab wie viel Input\nperformt das Ding gut?",
			"lineHeight": 1.25,
			"baseline": 43
		},
		{
			"type": "text",
			"version": 40,
			"versionNonce": 1313201945,
			"isDeleted": false,
			"id": "k04DUpPC",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 740.9845073925519,
			"y": -815.128533756274,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 153.65988159179688,
			"height": 50,
			"seed": 85864320,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160949,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "Schätzung Nina:\n~1000",
			"rawText": "Schätzung Nina:\n~1000",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Schätzung Nina:\n~1000",
			"lineHeight": 1.25,
			"baseline": 43
		},
		{
			"type": "text",
			"version": 110,
			"versionNonce": 1604929800,
			"isDeleted": false,
			"id": "YOggx1IA",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -2133.7531882889134,
			"y": 347.38048340411285,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 373.88385009765625,
			"height": 35,
			"seed": 1909971072,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1711005973593,
			"link": null,
			"locked": false,
			"fontSize": 28,
			"fontFamily": 1,
			"text": "Was ist der BusinessCase?",
			"rawText": "Was ist der BusinessCase?",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Was ist der BusinessCase?",
			"lineHeight": 1.25,
			"baseline": 24
		},
		{
			"type": "text",
			"version": 96,
			"versionNonce": 1093774200,
			"isDeleted": false,
			"id": "gwn666Q3",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -2038.0457024991579,
			"y": -390.9906256068027,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 366.51983642578125,
			"height": 35,
			"seed": 231473024,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1711005973593,
			"link": null,
			"locked": false,
			"fontSize": 28,
			"fontFamily": 1,
			"text": "Was zeichnet Donuts aus?",
			"rawText": "Was zeichnet Donuts aus?",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Was zeichnet Donuts aus?",
			"lineHeight": 1.25,
			"baseline": 24
		},
		{
			"type": "text",
			"version": 74,
			"versionNonce": 1688922120,
			"isDeleted": false,
			"id": "Qt3INyaj",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -1411.361888546495,
			"y": -530.6603377880427,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 479.49981689453125,
			"height": 35,
			"seed": 1544900480,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1711005973593,
			"link": null,
			"locked": false,
			"fontSize": 28,
			"fontFamily": 1,
			"text": "Abgrenzung ViT <-> Donut <-> CNN",
			"rawText": "Abgrenzung ViT <-> Donut <-> CNN",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Abgrenzung ViT <-> Donut <-> CNN",
			"lineHeight": 1.25,
			"baseline": 24
		},
		{
			"type": "text",
			"version": 151,
			"versionNonce": 493464793,
			"isDeleted": false,
			"id": "VSvIjoXG",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -270.12501091904676,
			"y": -1383.3624990910043,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 253.23977661132812,
			"height": 150,
			"seed": 1842043008,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160950,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "Theoretisch\nArchitektur über\nFinetuning\n--> Weboberfläche\nwo selbst gelabelt werden\nkann",
			"rawText": "Theoretisch\nArchitektur über\nFinetuning\n--> Weboberfläche\nwo selbst gelabelt werden\nkann",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Theoretisch\nArchitektur über\nFinetuning\n--> Weboberfläche\nwo selbst gelabelt werden\nkann",
			"lineHeight": 1.25,
			"baseline": 143
		},
		{
			"type": "text",
			"version": 46,
			"versionNonce": 150399287,
			"isDeleted": false,
			"id": "SLq7IKd2",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -545.509384663936,
			"y": -1119.3096093337376,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 131.1798858642578,
			"height": 50,
			"seed": 1516318592,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160950,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "Gebaut von\nBenoit --> St",
			"rawText": "Gebaut von\nBenoit --> St",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Gebaut von\nBenoit --> St",
			"lineHeight": 1.25,
			"baseline": 43
		},
		{
			"type": "text",
			"version": 117,
			"versionNonce": 1429252537,
			"isDeleted": false,
			"id": "7pAYEmPM",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -2749.3189084734604,
			"y": -64.42360013720827,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 304.7597351074219,
			"height": 25,
			"seed": 182679680,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160950,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "Auf Encoder-Ebene vergleichbar",
			"rawText": "Auf Encoder-Ebene vergleichbar",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Auf Encoder-Ebene vergleichbar",
			"lineHeight": 1.25,
			"baseline": 18
		},
		{
			"type": "text",
			"version": 103,
			"versionNonce": 1389537879,
			"isDeleted": false,
			"id": "u0Z76VlV",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -2111.985575140127,
			"y": 517.9284859043576,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 307.0997619628906,
			"height": 50,
			"seed": 2046099328,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160950,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "ELO Finanzabteilung kriegt Doc\nMetadaten werden zugeordnet",
			"rawText": "ELO Finanzabteilung kriegt Doc\nMetadaten werden zugeordnet",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "ELO Finanzabteilung kriegt Doc\nMetadaten werden zugeordnet",
			"lineHeight": 1.25,
			"baseline": 43
		},
		{
			"type": "text",
			"version": 82,
			"versionNonce": 2026179225,
			"isDeleted": false,
			"id": "yucGVVYm",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1094.0335232515047,
			"y": 490.7835612975639,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 16.899993896484375,
			"height": 25,
			"seed": 1503974587,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160950,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "F1",
			"rawText": "F1",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "F1",
			"lineHeight": 1.25,
			"baseline": 18
		},
		{
			"type": "text",
			"version": 125,
			"versionNonce": 702105463,
			"isDeleted": false,
			"id": "itM61GGJ",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1244.6282104263864,
			"y": 546.4591054830378,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 56.11994934082031,
			"height": 50,
			"seed": 1736130389,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160950,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "Cost/\nGPUh",
			"rawText": "Cost/\nGPUh",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Cost/\nGPUh",
			"lineHeight": 1.25,
			"baseline": 43
		},
		{
			"type": "text",
			"version": 71,
			"versionNonce": 1893355385,
			"isDeleted": false,
			"id": "dR4gcCtT",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1410.726217716993,
			"y": 542.9544632369112,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 85.91993713378906,
			"height": 25,
			"seed": 1833877589,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160950,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "Accuracy",
			"rawText": "Accuracy",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Accuracy",
			"lineHeight": 1.25,
			"baseline": 18
		},
		{
			"type": "text",
			"version": 45,
			"versionNonce": 1548697751,
			"isDeleted": false,
			"id": "OAnnn6zU",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1595.055709746059,
			"y": 520.3316827499376,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 50.13996887207031,
			"height": 25,
			"seed": 6498715,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160950,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "ANLS",
			"rawText": "ANLS",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "ANLS",
			"lineHeight": 1.25,
			"baseline": 18
		},
		{
			"type": "text",
			"version": 20,
			"versionNonce": 1135867993,
			"isDeleted": false,
			"id": "ZHoU15G6",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1688.5005945451048,
			"y": 408.4769332178696,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 28.79998779296875,
			"height": 25,
			"seed": 8738043,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160950,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "EM",
			"rawText": "EM",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "EM",
			"lineHeight": 1.25,
			"baseline": 18
		},
		{
			"type": "text",
			"version": 23,
			"versionNonce": 2078873015,
			"isDeleted": false,
			"id": "u6xabILC",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 998.34839557956,
			"y": 367.28689388502414,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 61.4599609375,
			"height": 25,
			"seed": 1092913589,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160950,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "CIDEr",
			"rawText": "CIDEr",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "CIDEr",
			"lineHeight": 1.25,
			"baseline": 18
		},
		{
			"type": "text",
			"version": 21,
			"versionNonce": 1663403321,
			"isDeleted": false,
			"id": "l3NSHzyZ",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1096.0623139522133,
			"y": 266.96980105528166,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 26.67999267578125,
			"height": 25,
			"seed": 2005739861,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160950,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "RA",
			"rawText": "RA",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "RA",
			"lineHeight": 1.25,
			"baseline": 18
		},
		{
			"type": "text",
			"version": 22,
			"versionNonce": 1875592919,
			"isDeleted": false,
			"id": "YKWUOdjQ",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1631.1287200735728,
			"y": 329.1912250230578,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 36.85997009277344,
			"height": 25,
			"seed": 754983707,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160950,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "FPS",
			"rawText": "FPS",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "FPS",
			"lineHeight": 1.25,
			"baseline": 18
		},
		{
			"type": "text",
			"version": 95,
			"versionNonce": 982677017,
			"isDeleted": false,
			"id": "u0UX9Q1B",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1574.5626827637388,
			"y": 271.492910112717,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 48.539947509765625,
			"height": 25,
			"seed": 641716955,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160950,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "Flops",
			"rawText": "Flops",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Flops",
			"lineHeight": 1.25,
			"baseline": 18
		},
		{
			"type": "text",
			"version": 87,
			"versionNonce": 1183470583,
			"isDeleted": false,
			"id": "yDbQkuES",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -1205.352593983394,
			"y": 588.295331360623,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 198.41981506347656,
			"height": 25,
			"seed": 679728789,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160950,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "Methode: Experiment",
			"rawText": "Methode: Experiment",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Methode: Experiment",
			"lineHeight": 1.25,
			"baseline": 18
		},
		{
			"type": "text",
			"version": 97,
			"versionNonce": 2095991545,
			"isDeleted": false,
			"id": "WmCx6Eyx",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -974.7103272048122,
			"y": 770.9118662117924,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 116.35989379882812,
			"height": 50,
			"seed": 1525616373,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160950,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "Genauigkeit:\nAccuracy",
			"rawText": "Genauigkeit:\nAccuracy",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Genauigkeit:\nAccuracy",
			"lineHeight": 1.25,
			"baseline": 43
		},
		{
			"type": "text",
			"version": 241,
			"versionNonce": 1210760471,
			"isDeleted": false,
			"id": "LaCgdref",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -971.0782165391577,
			"y": 1001.1102679393122,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 270.43975830078125,
			"height": 200,
			"seed": 1765537717,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160950,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "Effizienz (Abseits von Acc):\n- F1\n- Cost (i.e. GPUh)\n- RA\n- CIDEr\n- FPS (vermutlich weniger\n- EM\n- ANLS",
			"rawText": "Effizienz (Abseits von Acc):\n- F1\n- Cost (i.e. GPUh)\n- RA\n- CIDEr\n- FPS (vermutlich weniger\n- EM\n- ANLS",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Effizienz (Abseits von Acc):\n- F1\n- Cost (i.e. GPUh)\n- RA\n- CIDEr\n- FPS (vermutlich weniger\n- EM\n- ANLS",
			"lineHeight": 1.25,
			"baseline": 193
		},
		{
			"type": "text",
			"version": 40,
			"versionNonce": 851215321,
			"isDeleted": false,
			"id": "sU375XuL",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 357.48860263554366,
			"y": 1241.3190880226016,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 209.079833984375,
			"height": 25,
			"seed": 2141425339,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160950,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "Händischen Labeling :(",
			"rawText": "Händischen Labeling :(",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Händischen Labeling :(",
			"lineHeight": 1.25,
			"baseline": 18
		},
		{
			"type": "ellipse",
			"version": 389,
			"versionNonce": 1210122807,
			"isDeleted": false,
			"id": "BFXaXD4llQvbLar-_iLao",
			"fillStyle": "hachure",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1840.193479109524,
			"y": -2224.1433799984934,
			"strokeColor": "#1971c2",
			"backgroundColor": "#a5d8ff",
			"width": 1941.5101909303341,
			"height": 1551.1407555142216,
			"seed": 1131597627,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1710252160950,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 136,
			"versionNonce": 135307449,
			"isDeleted": false,
			"id": "iUNxf4qO",
			"fillStyle": "hachure",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 2734.1463246271014,
			"y": -2157.3831777683554,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"width": 178.27195739746094,
			"height": 45,
			"seed": 542067061,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160950,
			"link": null,
			"locked": false,
			"fontSize": 36,
			"fontFamily": 1,
			"text": "VDU/VrDU",
			"rawText": "VDU/VrDU",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "VDU/VrDU",
			"lineHeight": 1.25,
			"baseline": 32
		},
		{
			"type": "text",
			"version": 93,
			"versionNonce": 928097111,
			"isDeleted": false,
			"id": "FMtrDmlQ",
			"fillStyle": "hachure",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 2283.5965929702347,
			"y": -1997.547831913657,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"width": 340.847900390625,
			"height": 45,
			"seed": 1987775387,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [
				{
					"id": "RvfwCi5LYjXZgQUx72A0K",
					"type": "arrow"
				}
			],
			"updated": 1710252160950,
			"link": null,
			"locked": false,
			"fontSize": 36,
			"fontFamily": 1,
			"text": "OCR + Downstream",
			"rawText": "OCR + Downstream",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "OCR + Downstream",
			"lineHeight": 1.25,
			"baseline": 32
		},
		{
			"type": "text",
			"version": 95,
			"versionNonce": 1519264153,
			"isDeleted": false,
			"id": "KALykMsh",
			"fillStyle": "hachure",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 3149.3175797940535,
			"y": -1996.1342116342037,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"width": 74.15997314453125,
			"height": 45,
			"seed": 800027573,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [
				{
					"id": "RvfwCi5LYjXZgQUx72A0K",
					"type": "arrow"
				}
			],
			"updated": 1710252160950,
			"link": null,
			"locked": false,
			"fontSize": 36,
			"fontFamily": 1,
			"text": "E2E",
			"rawText": "E2E",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "E2E",
			"lineHeight": 1.25,
			"baseline": 32
		},
		{
			"type": "arrow",
			"version": 226,
			"versionNonce": 1980833911,
			"isDeleted": false,
			"id": "RvfwCi5LYjXZgQUx72A0K",
			"fillStyle": "hachure",
			"strokeWidth": 4,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 2636.37892262229,
			"y": -1974.687038760035,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"width": 506.34383833502034,
			"height": 4.440137705947109,
			"seed": 2027991547,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1710252160950,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "FMtrDmlQ",
				"focus": 0.08168125688423519,
				"gap": 11.934429261430068
			},
			"endBinding": {
				"elementId": "KALykMsh",
				"focus": 0.25743307912348673,
				"gap": 6.594818836743343
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					506.34383833502034,
					-4.440137705947109
				]
			]
		},
		{
			"type": "rectangle",
			"version": 227,
			"versionNonce": 124290681,
			"isDeleted": false,
			"id": "-Zv2bsdsdV948EteP2jCM",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 3095.3695952966864,
			"y": -1811.8155639194413,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#b2f2bb",
			"width": 250.05510441039092,
			"height": 178.4088431103568,
			"seed": 721674491,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"type": "text",
					"id": "qeBnBXfT"
				}
			],
			"updated": 1710252160950,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 297,
			"versionNonce": 1713633687,
			"isDeleted": false,
			"id": "qeBnBXfT",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 3124.817199076589,
			"y": -1790.1111423642628,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#b2f2bb",
			"width": 191.15989685058594,
			"height": 135,
			"seed": 1015995771,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160950,
			"link": null,
			"locked": false,
			"fontSize": 36,
			"fontFamily": 1,
			"text": "Donut\n(OCR-Free)\n10.2022",
			"rawText": "Donut\n(OCR-Free)\n10.2022",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "-Zv2bsdsdV948EteP2jCM",
			"originalText": "Donut\n(OCR-Free)\n10.2022",
			"lineHeight": 1.25,
			"baseline": 122
		},
		{
			"type": "rectangle",
			"version": 398,
			"versionNonce": 2036551513,
			"isDeleted": false,
			"id": "2Y_OPew0IHA821IVyGw5o",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 2254.228164609439,
			"y": -1833.9166140153839,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#bd9d00",
			"width": 206.56292805928797,
			"height": 159.12880617120823,
			"seed": 255940347,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"type": "text",
					"id": "YRfrDvsO"
				}
			],
			"updated": 1710252160950,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 126,
			"versionNonce": 1019129527,
			"isDeleted": false,
			"id": "YRfrDvsO",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 2300.3956454847857,
			"y": -1799.3522109297796,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#bd9d00",
			"width": 114.22796630859375,
			"height": 90,
			"seed": 457185493,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160950,
			"link": null,
			"locked": false,
			"fontSize": 36,
			"fontFamily": 1,
			"text": "OCR +\nBERT",
			"rawText": "OCR + BERT",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "2Y_OPew0IHA821IVyGw5o",
			"originalText": "OCR + BERT",
			"lineHeight": 1.25,
			"baseline": 77
		},
		{
			"type": "rectangle",
			"version": 627,
			"versionNonce": 1993473081,
			"isDeleted": false,
			"id": "r77l4N9FlWZm8OyIguY42",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 2239.7912706304896,
			"y": -1326.8965124420115,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#bd9d00",
			"width": 206.56292805928797,
			"height": 159.12880617120823,
			"seed": 800174197,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"type": "text",
					"id": "uaRKhToE"
				}
			],
			"updated": 1710252160950,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 441,
			"versionNonce": 344309719,
			"isDeleted": false,
			"id": "uaRKhToE",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 2268.072803324684,
			"y": -1297.3321093564073,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#bd9d00",
			"width": 149.99986267089844,
			"height": 100,
			"seed": 661510613,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160950,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "FastStrucText\n(Hourglass)\n5.2023\n",
			"rawText": "FastStrucText\n(Hourglass)\n5.2023\n",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "r77l4N9FlWZm8OyIguY42",
			"originalText": "FastStrucText\n(Hourglass)\n5.2023\n",
			"lineHeight": 1.25,
			"baseline": 93
		},
		{
			"type": "rectangle",
			"version": 363,
			"versionNonce": 798493977,
			"isDeleted": false,
			"id": "sKt1nbzrxQEx4Azfncg9L",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 3089.934893798417,
			"y": -1131.5073433766909,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#b2f2bb",
			"width": 250.05510441039092,
			"height": 178.4088431103568,
			"seed": 290332341,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"type": "text",
					"id": "2QN8n7F6"
				}
			],
			"updated": 1710252160950,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 444,
			"versionNonce": 1066249463,
			"isDeleted": false,
			"id": "2QN8n7F6",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 3119.3824975783195,
			"y": -1109.8029218215124,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#b2f2bb",
			"width": 191.15989685058594,
			"height": 135,
			"seed": 1877114901,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160950,
			"link": null,
			"locked": false,
			"fontSize": 36,
			"fontFamily": 1,
			"text": "Dublin\n(OCR-Free)\n12.2023",
			"rawText": "Dublin\n(OCR-Free)\n12.2023",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "sKt1nbzrxQEx4Azfncg9L",
			"originalText": "Dublin\n(OCR-Free)\n12.2023",
			"lineHeight": 1.25,
			"baseline": 122
		},
		{
			"type": "rectangle",
			"version": 467,
			"versionNonce": 187236857,
			"isDeleted": false,
			"id": "W8Xx5bzJCufyaoLw3iAff",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 2240.766120053133,
			"y": -1512.2827238267046,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#bd9d00",
			"width": 206.56292805928797,
			"height": 159.12880617120823,
			"seed": 490507771,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"type": "text",
					"id": "vW8ARdTi"
				}
			],
			"updated": 1710252160950,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 210,
			"versionNonce": 1499133463,
			"isDeleted": false,
			"id": "vW8ARdTi",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 2271.0216136237923,
			"y": -1477.7183207411003,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#bd9d00",
			"width": 146.05194091796875,
			"height": 90,
			"seed": 1812928155,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160950,
			"link": null,
			"locked": false,
			"fontSize": 36,
			"fontFamily": 1,
			"text": "Ernie\n10.2022",
			"rawText": "Ernie\n10.2022",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "W8Xx5bzJCufyaoLw3iAff",
			"originalText": "Ernie\n10.2022",
			"lineHeight": 1.25,
			"baseline": 77
		},
		{
			"type": "rectangle",
			"version": 258,
			"versionNonce": 914905817,
			"isDeleted": false,
			"id": "PxIkxA3HxJM3NHe59JLzq",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 4401.738459463437,
			"y": -2026.9457518576257,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"width": 250.05510441039092,
			"height": 178.4088431103568,
			"seed": 387577397,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"type": "text",
					"id": "FQU6ZfX3"
				},
				{
					"id": "FeF0n0ohRN31ujw7tfhpg",
					"type": "arrow"
				},
				{
					"id": "60Y7j-9ueftTTQoWtJMKX",
					"type": "arrow"
				}
			],
			"updated": 1710252160950,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 342,
			"versionNonce": 417471287,
			"isDeleted": false,
			"id": "FQU6ZfX3",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 4467.420033885429,
			"y": -1982.7413303024473,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#b2f2bb",
			"width": 118.69195556640625,
			"height": 90,
			"seed": 222783381,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160951,
			"link": null,
			"locked": false,
			"fontSize": 36,
			"fontFamily": 1,
			"text": "ViT\n6.2021",
			"rawText": "ViT\n6.2021",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "PxIkxA3HxJM3NHe59JLzq",
			"originalText": "ViT\n6.2021",
			"lineHeight": 1.25,
			"baseline": 77
		},
		{
			"type": "rectangle",
			"version": 351,
			"versionNonce": 1917425593,
			"isDeleted": false,
			"id": "kQGpnNozmEDBE5hQSdmIT",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 4402.707564799906,
			"y": -1665.7863911119857,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"width": 250.05510441039092,
			"height": 178.4088431103568,
			"seed": 438679893,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"type": "text",
					"id": "ykCCNjtF"
				},
				{
					"id": "60Y7j-9ueftTTQoWtJMKX",
					"type": "arrow"
				},
				{
					"id": "GD4CAB1_Z43TmvQQw5V9L",
					"type": "arrow"
				}
			],
			"updated": 1710252160951,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 444,
			"versionNonce": 1653054551,
			"isDeleted": false,
			"id": "ykCCNjtF",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 4466.139139221898,
			"y": -1621.5819695568073,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#b2f2bb",
			"width": 123.19195556640625,
			"height": 90,
			"seed": 1009632949,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160951,
			"link": null,
			"locked": false,
			"fontSize": 36,
			"fontFamily": 1,
			"text": "Swin\n8.2021",
			"rawText": "Swin\n8.2021",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "kQGpnNozmEDBE5hQSdmIT",
			"originalText": "Swin\n8.2021",
			"lineHeight": 1.25,
			"baseline": 77
		},
		{
			"type": "rectangle",
			"version": 343,
			"versionNonce": 546322585,
			"isDeleted": false,
			"id": "6cQl_s15s-clD7WpQAuHp",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 4401.738459463437,
			"y": -1319.639340528932,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"width": 250.05510441039092,
			"height": 178.4088431103568,
			"seed": 300198261,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"type": "text",
					"id": "diuI977G"
				},
				{
					"id": "GD4CAB1_Z43TmvQQw5V9L",
					"type": "arrow"
				}
			],
			"updated": 1710252160951,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 412,
			"versionNonce": 438303095,
			"isDeleted": false,
			"id": "diuI977G",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 4431.186063243339,
			"y": -1297.9349189737536,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#b2f2bb",
			"width": 191.15989685058594,
			"height": 135,
			"seed": 450474709,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160951,
			"link": null,
			"locked": false,
			"fontSize": 36,
			"fontFamily": 1,
			"text": "Donut\n(OCR-Free)\n10.2022",
			"rawText": "Donut\n(OCR-Free)\n10.2022",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "6cQl_s15s-clD7WpQAuHp",
			"originalText": "Donut\n(OCR-Free)\n10.2022",
			"lineHeight": 1.25,
			"baseline": 122
		},
		{
			"type": "rectangle",
			"version": 151,
			"versionNonce": 319798649,
			"isDeleted": false,
			"id": "g1BC7clFlNg0P7QxjDmYa",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 3905.057561874978,
			"y": -2027.9841078420393,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 244.09983163630022,
			"height": 184.32304314724794,
			"seed": 462230229,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"type": "text",
					"id": "HjpYuqra"
				},
				{
					"id": "FeF0n0ohRN31ujw7tfhpg",
					"type": "arrow"
				}
			],
			"updated": 1710252160951,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 89,
			"versionNonce": 888124055,
			"isDeleted": false,
			"id": "HjpYuqra",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 3992.457483796644,
			"y": -1953.3225862684153,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 69.29998779296875,
			"height": 35,
			"seed": 1043217973,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160951,
			"link": null,
			"locked": false,
			"fontSize": 28,
			"fontFamily": 1,
			"text": "CNNs",
			"rawText": "CNNs",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "g1BC7clFlNg0P7QxjDmYa",
			"originalText": "CNNs",
			"lineHeight": 1.25,
			"baseline": 24
		},
		{
			"type": "arrow",
			"version": 142,
			"versionNonce": 1286244209,
			"isDeleted": false,
			"id": "FeF0n0ohRN31ujw7tfhpg",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 4164.95500767675,
			"y": -1941.0709131068247,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 219.71541338850147,
			"height": 0.4511455735018899,
			"seed": 1557849499,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1712353982025,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "g1BC7clFlNg0P7QxjDmYa",
				"gap": 15.797614165471714,
				"focus": -0.05372976589793473
			},
			"endBinding": {
				"elementId": "PxIkxA3HxJM3NHe59JLzq",
				"gap": 17.068038398185763,
				"focus": 0.0455225101771102
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					219.71541338850147,
					-0.4511455735018899
				]
			]
		},
		{
			"type": "arrow",
			"version": 99,
			"versionNonce": 1294606385,
			"isDeleted": false,
			"id": "60Y7j-9ueftTTQoWtJMKX",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 4535.736834463256,
			"y": -1823.2993611440543,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 0.3557250958201621,
			"height": 132.56912677364448,
			"seed": 1991526171,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1712353982025,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "PxIkxA3HxJM3NHe59JLzq",
				"gap": 25.23754760321458,
				"focus": -0.0691622249416006
			},
			"endBinding": {
				"elementId": "kQGpnNozmEDBE5hQSdmIT",
				"gap": 24.94384325842384,
				"focus": 0.06916222494160061
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					0.3557250958201621,
					132.56912677364448
				]
			]
		},
		{
			"type": "arrow",
			"version": 113,
			"versionNonce": 684982193,
			"isDeleted": false,
			"id": "GD4CAB1_Z43TmvQQw5V9L",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 4533.937397670664,
			"y": -1462.6460705934408,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 0.5298537362077695,
			"height": 124.34323915011987,
			"seed": 727301973,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1712353982025,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "kQGpnNozmEDBE5hQSdmIT",
				"gap": 24.731477408188084,
				"focus": -0.04558552759980929
			},
			"endBinding": {
				"elementId": "6cQl_s15s-clD7WpQAuHp",
				"gap": 18.66349091438883,
				"focus": 0.06507487452782598
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					0.5298537362077695,
					124.34323915011987
				]
			]
		},
		{
			"type": "text",
			"version": 79,
			"versionNonce": 1819752663,
			"isDeleted": false,
			"id": "5zRGmAPY",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 4686.117047011878,
			"y": -2006.4825358052,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 291.3997802734375,
			"height": 25,
			"seed": 562451099,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160951,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "Hohe Datenmenge für Training",
			"rawText": "Hohe Datenmenge für Training",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Hohe Datenmenge für Training",
			"lineHeight": 1.25,
			"baseline": 18
		},
		{
			"type": "text",
			"version": 98,
			"versionNonce": 609657881,
			"isDeleted": false,
			"id": "7VKLZQpl",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 3902.0314273654626,
			"y": -1823.654043303076,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 236.51979064941406,
			"height": 50,
			"seed": 1159225371,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160951,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "Niedrige Datenmenge für\nTraining",
			"rawText": "Niedrige Datenmenge für\nTraining",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Niedrige Datenmenge für\nTraining",
			"lineHeight": 1.25,
			"baseline": 43
		},
		{
			"type": "text",
			"version": 134,
			"versionNonce": 1037925496,
			"isDeleted": false,
			"id": "M05mtzOP",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 2166.4769535917612,
			"y": -133.39468899591827,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 355.34783935546875,
			"height": 70,
			"seed": 1048423157,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1711005973595,
			"link": null,
			"locked": false,
			"fontSize": 28,
			"fontFamily": 1,
			"text": "Auf Basis von Rechnungen\n~1000 Stück",
			"rawText": "Auf Basis von Rechnungen\n~1000 Stück",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Auf Basis von Rechnungen\n~1000 Stück",
			"lineHeight": 1.25,
			"baseline": 59
		},
		{
			"type": "text",
			"version": 25,
			"versionNonce": 908109576,
			"isDeleted": false,
			"id": "W49u9ni6",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 383.74539681218187,
			"y": 478.75060401720043,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 170.8838653564453,
			"height": 35,
			"seed": 1702919861,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1711005973595,
			"link": null,
			"locked": false,
			"fontSize": 28,
			"fontFamily": 1,
			"text": "Spezifikation",
			"rawText": "Spezifikation",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Spezifikation",
			"lineHeight": 1.25,
			"baseline": 24
		},
		{
			"type": "text",
			"version": 385,
			"versionNonce": 921120120,
			"isDeleted": false,
			"id": "5AnFcCOl",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 457.26250413415744,
			"y": 631.3345148385208,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 848.1756591796875,
			"height": 210,
			"seed": 447415797,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1711005973595,
			"link": null,
			"locked": false,
			"fontSize": 28,
			"fontFamily": 1,
			"text": "Betrachtet für den UseCase ELO Rechnungsverarbeitung\nim Vergleich zu OCR + Downstream\n- Keine Massenverarbeitung sondern Einzelverarbeitung. Daher\nFPS vermutlich weniger wichtig\n- Evtl. Austausch der OCR\n- Interessant: Wie performt es gegen heutiges SOTA?",
			"rawText": "Betrachtet für den UseCase ELO Rechnungsverarbeitung\nim Vergleich zu OCR + Downstream\n- Keine Massenverarbeitung sondern Einzelverarbeitung. Daher\nFPS vermutlich weniger wichtig\n- Evtl. Austausch der OCR\n- Interessant: Wie performt es gegen heutiges SOTA?",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Betrachtet für den UseCase ELO Rechnungsverarbeitung\nim Vergleich zu OCR + Downstream\n- Keine Massenverarbeitung sondern Einzelverarbeitung. Daher\nFPS vermutlich weniger wichtig\n- Evtl. Austausch der OCR\n- Interessant: Wie performt es gegen heutiges SOTA?",
			"lineHeight": 1.25,
			"baseline": 199
		},
		{
			"type": "text",
			"version": 230,
			"versionNonce": 1607283161,
			"isDeleted": false,
			"id": "zGx4Stj3",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 4123.69457174124,
			"y": -922.6752145939895,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 518.291748046875,
			"height": 45,
			"seed": 441554325,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160951,
			"link": null,
			"locked": false,
			"fontSize": 36,
			"fontFamily": 1,
			"text": "Architektur u. Pipeline Donut:",
			"rawText": "Architektur u. Pipeline Donut:",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Architektur u. Pipeline Donut:",
			"lineHeight": 1.25,
			"baseline": 32
		},
		{
			"type": "text",
			"version": 218,
			"versionNonce": 1887864328,
			"isDeleted": false,
			"id": "pT81dz7F",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 4696.489567255291,
			"y": -1624.2278903772951,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 729.6235961914062,
			"height": 105,
			"seed": 1610789269,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1711005973595,
			"link": null,
			"locked": false,
			"fontSize": 28,
			"fontFamily": 1,
			"text": "Interessant: Self-Attention wird mit Shifting Windows\numgesetzt. Das ganze Bild wird über übergreifende\nPanelgrenzen erzeugt",
			"rawText": "Interessant: Self-Attention wird mit Shifting Windows\numgesetzt. Das ganze Bild wird über übergreifende\nPanelgrenzen erzeugt",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Interessant: Self-Attention wird mit Shifting Windows\numgesetzt. Das ganze Bild wird über übergreifende\nPanelgrenzen erzeugt",
			"lineHeight": 1.25,
			"baseline": 94
		},
		{
			"type": "rectangle",
			"version": 388,
			"versionNonce": 1792773817,
			"isDeleted": false,
			"id": "RDWPMXnV8-MzK4U3lx2j0",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 4235.313332210273,
			"y": -789.1078592004924,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#a5d8ff",
			"width": 250.05510441039092,
			"height": 178.4088431103568,
			"seed": 2146087349,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"type": "text",
					"id": "v3sdjfYk"
				},
				{
					"id": "9pTBR2001M4ddhVsNw5ie",
					"type": "arrow"
				},
				{
					"id": "wndIB6o6ZfpIUWLfrDRbS",
					"type": "arrow"
				}
			],
			"updated": 1710252160951,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 510,
			"versionNonce": 1836356951,
			"isDeleted": false,
			"id": "v3sdjfYk",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 4252.502917496523,
			"y": -767.4034376453139,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#b2f2bb",
			"width": 215.67593383789062,
			"height": 135,
			"seed": 594850581,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160951,
			"link": null,
			"locked": false,
			"fontSize": 36,
			"fontFamily": 1,
			"text": "Encoder:\nSwin\nTransformer",
			"rawText": "Encoder:\nSwin Transformer",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "RDWPMXnV8-MzK4U3lx2j0",
			"originalText": "Encoder:\nSwin Transformer",
			"lineHeight": 1.25,
			"baseline": 122
		},
		{
			"type": "text",
			"version": 78,
			"versionNonce": 1103843225,
			"isDeleted": false,
			"id": "vgRVOvmh",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 3866.477362157181,
			"y": -716.8092642734977,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 104.14796447753906,
			"height": 45,
			"seed": 777950747,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [
				{
					"id": "9pTBR2001M4ddhVsNw5ie",
					"type": "arrow"
				}
			],
			"updated": 1710252160951,
			"link": null,
			"locked": false,
			"fontSize": 36,
			"fontFamily": 1,
			"text": "Image",
			"rawText": "Image",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Image",
			"lineHeight": 1.25,
			"baseline": 32
		},
		{
			"type": "arrow",
			"version": 201,
			"versionNonce": 1725046577,
			"isDeleted": false,
			"id": "9pTBR2001M4ddhVsNw5ie",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 3978.558369176117,
			"y": -690.689416687758,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 239.6150043517423,
			"height": 4.47499189751079,
			"seed": 303670741,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1712353982025,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "vgRVOvmh",
				"gap": 7.933042541397299,
				"focus": 0.20196059271200692
			},
			"endBinding": {
				"elementId": "RDWPMXnV8-MzK4U3lx2j0",
				"gap": 17.13995868241409,
				"focus": -0.02276552893717209
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					239.6150043517423,
					-4.47499189751079
				]
			]
		},
		{
			"type": "text",
			"version": 23,
			"versionNonce": 630374008,
			"isDeleted": false,
			"id": "NwBFTz2Y",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 4282.274016303313,
			"y": -822.3403106253049,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 160.46795654296875,
			"height": 35,
			"seed": 1979963451,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1711005973596,
			"link": null,
			"locked": false,
			"fontSize": 28,
			"fontFamily": 1,
			"text": "CNN Möglich",
			"rawText": "CNN Möglich",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "CNN Möglich",
			"lineHeight": 1.25,
			"baseline": 24
		},
		{
			"type": "rectangle",
			"version": 638,
			"versionNonce": 565341079,
			"isDeleted": false,
			"id": "pk4JtK2FPUddZ_Kt-4TKF",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 4234.318253288548,
			"y": -355.6397740855789,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 250.05510441039092,
			"height": 178.4088431103568,
			"seed": 850595125,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"type": "text",
					"id": "KmxJJkC3"
				},
				{
					"id": "wndIB6o6ZfpIUWLfrDRbS",
					"type": "arrow"
				},
				{
					"id": "YqhPvEUswAeh4G5sCXtaU",
					"type": "arrow"
				},
				{
					"id": "BxkNfR8CB8ZszogUrmW1a",
					"type": "arrow"
				}
			],
			"updated": 1710252160951,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 772,
			"versionNonce": 1504509273,
			"isDeleted": false,
			"id": "KmxJJkC3",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 4284.267840711028,
			"y": -311.4353525304005,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#b2f2bb",
			"width": 150.1559295654297,
			"height": 90,
			"seed": 598056597,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160951,
			"link": null,
			"locked": false,
			"fontSize": 36,
			"fontFamily": 1,
			"text": "Decoder:\nBART",
			"rawText": "Decoder:\nBART",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "pk4JtK2FPUddZ_Kt-4TKF",
			"originalText": "Decoder:\nBART",
			"lineHeight": 1.25,
			"baseline": 77
		},
		{
			"type": "arrow",
			"version": 82,
			"versionNonce": 453279409,
			"isDeleted": false,
			"id": "wndIB6o6ZfpIUWLfrDRbS",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 4361.371083769728,
			"y": -584.7142723473349,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 2.616472223598066,
			"height": 213.98294200915268,
			"seed": 1216418523,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "DBWZJWAH"
				}
			],
			"updated": 1712353982026,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "RDWPMXnV8-MzK4U3lx2j0",
				"gap": 25.984743742800617,
				"focus": 0.0029993578335573566
			},
			"endBinding": {
				"elementId": "pk4JtK2FPUddZ_Kt-4TKF",
				"gap": 15.091556252603354,
				"focus": 0.046916487437769085
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					2.616472223598066,
					213.98294200915268
				]
			]
		},
		{
			"type": "text",
			"version": 18,
			"versionNonce": 1035332153,
			"isDeleted": false,
			"id": "DBWZJWAH",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 4289.459349178402,
			"y": -495.2228013427586,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 146.43994140625,
			"height": 35,
			"seed": 1686718325,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160952,
			"link": null,
			"locked": false,
			"fontSize": 28,
			"fontFamily": 1,
			"text": "Embeddings",
			"rawText": "Embeddings",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "wndIB6o6ZfpIUWLfrDRbS",
			"originalText": "Embeddings",
			"lineHeight": 1.25,
			"baseline": 24
		},
		{
			"type": "arrow",
			"version": 234,
			"versionNonce": 1577535089,
			"isDeleted": false,
			"id": "YqhPvEUswAeh4G5sCXtaU",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 4505.786302339354,
			"y": -260.48715320936964,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 309.7388013063519,
			"height": 1.1231643854845856,
			"seed": 423470773,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "wX6cBUtm"
				}
			],
			"updated": 1712353982027,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "pk4JtK2FPUddZ_Kt-4TKF",
				"gap": 21.41294464041448,
				"focus": 0.06042064609391471
			},
			"endBinding": {
				"elementId": "UbrMdh5z",
				"gap": 13.117481550527373,
				"focus": -0.15899741020846717
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					309.7388013063519,
					1.1231643854845856
				]
			]
		},
		{
			"type": "text",
			"version": 27,
			"versionNonce": 265173785,
			"isDeleted": false,
			"id": "wX6cBUtm",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 4565.376057706802,
			"y": -294.449313159337,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 121.29594421386719,
			"height": 70,
			"seed": 198983989,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160952,
			"link": null,
			"locked": false,
			"fontSize": 28,
			"fontFamily": 1,
			"text": "Token\nSequence",
			"rawText": "Token\nSequence",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "YqhPvEUswAeh4G5sCXtaU",
			"originalText": "Token\nSequence",
			"lineHeight": 1.25,
			"baseline": 59
		},
		{
			"type": "text",
			"version": 77,
			"versionNonce": 1201233655,
			"isDeleted": false,
			"id": "UbrMdh5z",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 4828.642585196233,
			"y": -285.20256208275566,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 125.4599609375,
			"height": 45,
			"seed": 96326869,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [
				{
					"id": "YqhPvEUswAeh4G5sCXtaU",
					"type": "arrow"
				}
			],
			"updated": 1710252160952,
			"link": null,
			"locked": false,
			"fontSize": 36,
			"fontFamily": 1,
			"text": "Output",
			"rawText": "Output",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Output",
			"lineHeight": 1.25,
			"baseline": 32
		},
		{
			"type": "text",
			"version": 117,
			"versionNonce": 543780857,
			"isDeleted": false,
			"id": "mYrmjY95",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 3800.4700546070867,
			"y": -317.542261375523,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 254.08787536621094,
			"height": 135,
			"seed": 311133083,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [
				{
					"id": "BxkNfR8CB8ZszogUrmW1a",
					"type": "arrow"
				}
			],
			"updated": 1710252160952,
			"link": null,
			"locked": false,
			"fontSize": 36,
			"fontFamily": 1,
			"text": "Question/\nClassification/\nParsing",
			"rawText": "Question/\nClassification/\nParsing",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Question/\nClassification/\nParsing",
			"lineHeight": 1.25,
			"baseline": 122
		},
		{
			"type": "arrow",
			"version": 464,
			"versionNonce": 153118743,
			"isDeleted": false,
			"id": "7vCygrxuZ_nagXC9_84nN",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 2815.363001059742,
			"y": -2023.9137695678214,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 0.751866075648195,
			"height": 1311.7055555755962,
			"seed": 578455253,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "hTOORAQ2"
				}
			],
			"updated": 1710252160952,
			"link": null,
			"locked": false,
			"startBinding": null,
			"endBinding": null,
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					0.751866075648195,
					1311.7055555755962
				]
			]
		},
		{
			"type": "text",
			"version": 11,
			"versionNonce": 1703610585,
			"isDeleted": false,
			"id": "hTOORAQ2",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 2772.9052334187018,
			"y": -1399.7638325459557,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 100.40397644042969,
			"height": 45,
			"seed": 1208288853,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160952,
			"link": null,
			"locked": false,
			"fontSize": 36,
			"fontFamily": 1,
			"text": "TIME",
			"rawText": "TIME",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "7vCygrxuZ_nagXC9_84nN",
			"originalText": "TIME",
			"lineHeight": 1.25,
			"baseline": 32
		},
		{
			"type": "arrow",
			"version": 113,
			"versionNonce": 1766530609,
			"isDeleted": false,
			"id": "BxkNfR8CB8ZszogUrmW1a",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 4071.5551082671323,
			"y": -251.11177083362557,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 149.24645451068636,
			"height": 3.239282054998796,
			"seed": 1483663771,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1712353982027,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "mYrmjY95",
				"gap": 16.997178293834168,
				"focus": 0.02927513456173227
			},
			"endBinding": {
				"elementId": "pk4JtK2FPUddZ_Kt-4TKF",
				"gap": 13.516690510729404,
				"focus": -0.09875428156905777
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					149.24645451068636,
					-3.239282054998796
				]
			]
		},
		{
			"type": "rectangle",
			"version": 282,
			"versionNonce": 1220969913,
			"isDeleted": false,
			"id": "2ofVsJVNf4nFQ_ls5V2Dr",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 2632.952611798039,
			"y": -1785.3721581932566,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#bd9d00",
			"width": 208.67401737529872,
			"height": 156.58179870734784,
			"seed": 1839762075,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"type": "text",
					"id": "n8TpO48n"
				}
			],
			"updated": 1710252160952,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 234,
			"versionNonce": 1897434711,
			"isDeleted": false,
			"id": "n8TpO48n",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 2638.8656474021923,
			"y": -1752.0812588395827,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#bd9d00",
			"width": 196.8479461669922,
			"height": 90,
			"seed": 1615460187,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160952,
			"link": null,
			"locked": false,
			"fontSize": 36,
			"fontFamily": 1,
			"text": "LayoutLM3\n7.2022",
			"rawText": "LayoutLM3\n7.2022",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "2ofVsJVNf4nFQ_ls5V2Dr",
			"originalText": "LayoutLM3\n7.2022",
			"lineHeight": 1.25,
			"baseline": 77
		},
		{
			"type": "rectangle",
			"version": 338,
			"versionNonce": 893347481,
			"isDeleted": false,
			"id": "v7XgzXurPsoZQom9cux8L",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 2797.598479028231,
			"y": -1575.2490929463902,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#b2f2bb",
			"width": 208.67401737529872,
			"height": 156.58179870734784,
			"seed": 1447835899,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"type": "text",
					"id": "vhpTu6ZQ"
				}
			],
			"updated": 1710252160952,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 313,
			"versionNonce": 1304603511,
			"isDeleted": false,
			"id": "vhpTu6ZQ",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 2811.863519637267,
			"y": -1541.9581935927163,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#bd9d00",
			"width": 180.14393615722656,
			"height": 90,
			"seed": 1542545819,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160952,
			"link": null,
			"locked": false,
			"fontSize": 36,
			"fontFamily": 1,
			"text": "DocFormer\n",
			"rawText": "DocFormer\n",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "v7XgzXurPsoZQom9cux8L",
			"originalText": "DocFormer\n",
			"lineHeight": 1.25,
			"baseline": 77
		},
		{
			"type": "rectangle",
			"version": 553,
			"versionNonce": 1705585529,
			"isDeleted": false,
			"id": "g24LD9eBfxFf4SyOmcimP",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 2799.01205755618,
			"y": -1302.571553725326,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#b2f2bb",
			"width": 208.67401737529872,
			"height": 156.58179870734784,
			"seed": 1167618037,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"type": "text",
					"id": "5b8wj5yd"
				}
			],
			"updated": 1710252160952,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 562,
			"versionNonce": 90973335,
			"isDeleted": false,
			"id": "5b8wj5yd",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 2807.5171189171692,
			"y": -1291.7806543716522,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#bd9d00",
			"width": 191.6638946533203,
			"height": 135,
			"seed": 1632676181,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160952,
			"link": null,
			"locked": false,
			"fontSize": 36,
			"fontFamily": 1,
			"text": "Rationale \nDistillation\n11.2023",
			"rawText": "Rationale \nDistillation\n11.2023",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "g24LD9eBfxFf4SyOmcimP",
			"originalText": "Rationale \nDistillation\n11.2023",
			"lineHeight": 1.25,
			"baseline": 122
		},
		{
			"type": "text",
			"version": 77,
			"versionNonce": 1917277273,
			"isDeleted": false,
			"id": "3EKwmCYR",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 4643.528121814226,
			"y": -765.613428622108,
			"strokeColor": "#2f9e44",
			"backgroundColor": "#ffc9c9",
			"width": 493.84783935546875,
			"height": 90,
			"seed": 226475899,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160952,
			"link": null,
			"locked": false,
			"fontSize": 36,
			"fontFamily": 1,
			"text": "Hier auch die Abwägung:\nWas sind Vor- und Nachteile",
			"rawText": "Hier auch die Abwägung:\nWas sind Vor- und Nachteile",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Hier auch die Abwägung:\nWas sind Vor- und Nachteile",
			"lineHeight": 1.25,
			"baseline": 77
		},
		{
			"type": "text",
			"version": 135,
			"versionNonce": 1087931656,
			"isDeleted": false,
			"id": "j7Iky1iz",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 2423.6909525433152,
			"y": -1007.4653954864878,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 364.1640625,
			"height": 96.6,
			"seed": 1515084219,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1711005973602,
			"link": null,
			"locked": false,
			"fontSize": 28,
			"fontFamily": 2,
			"text": "Grundsätzlicher Trend:\nMit fortlaufender Zeit bessere\nModelle",
			"rawText": "Grundsätzlicher Trend:\nMit fortlaufender Zeit bessere\nModelle",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Grundsätzlicher Trend:\nMit fortlaufender Zeit bessere\nModelle",
			"lineHeight": 1.15,
			"baseline": 89
		},
		{
			"type": "text",
			"version": 78,
			"versionNonce": 518873401,
			"isDeleted": false,
			"id": "wpkgGt0g",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 3343.9419329811285,
			"y": 76.06952356866623,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 333.50390625,
			"height": 45,
			"seed": 984473979,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160952,
			"link": null,
			"locked": false,
			"fontSize": 36,
			"fontFamily": 1,
			"text": "Projektgestalltung:",
			"rawText": "Projektgestalltung:",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Projektgestalltung:",
			"lineHeight": 1.25,
			"baseline": 32
		},
		{
			"type": "text",
			"version": 53,
			"versionNonce": 436153047,
			"isDeleted": false,
			"id": "jvSjlKg0",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 2791.5633230843796,
			"y": 277.614041353375,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 224.6759033203125,
			"height": 45,
			"seed": 1656805429,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [
				{
					"id": "svjNys6CeIVxfQI4haK6H",
					"type": "arrow"
				}
			],
			"updated": 1710252160952,
			"link": null,
			"locked": false,
			"fontSize": 36,
			"fontFamily": 1,
			"text": "Daten labeln",
			"rawText": "Daten labeln",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Daten labeln",
			"lineHeight": 1.25,
			"baseline": 32
		},
		{
			"type": "text",
			"version": 100,
			"versionNonce": 1761530393,
			"isDeleted": false,
			"id": "7s8gxoce",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 3278.2511287880734,
			"y": 272.82533568394683,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 240.22787475585938,
			"height": 45,
			"seed": 2003871765,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [
				{
					"id": "FsblHk68_ohmO9GPzS9oK",
					"type": "arrow"
				},
				{
					"id": "svjNys6CeIVxfQI4haK6H",
					"type": "arrow"
				}
			],
			"updated": 1710252160952,
			"link": null,
			"locked": false,
			"fontSize": 36,
			"fontFamily": 1,
			"text": "Pipeline bauen",
			"rawText": "Pipeline bauen",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Pipeline bauen",
			"lineHeight": 1.25,
			"baseline": 32
		},
		{
			"type": "text",
			"version": 73,
			"versionNonce": 1218557943,
			"isDeleted": false,
			"id": "bdADuUFt",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 3689.0935268367452,
			"y": 263.6063230192266,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 257.39984130859375,
			"height": 45,
			"seed": 305332443,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [
				{
					"id": "FsblHk68_ohmO9GPzS9oK",
					"type": "arrow"
				},
				{
					"id": "LB59msowcTk5Uxo2b9Rfd",
					"type": "arrow"
				}
			],
			"updated": 1710252160952,
			"link": null,
			"locked": false,
			"fontSize": 36,
			"fontFamily": 1,
			"text": "Pipeline testen",
			"rawText": "Pipeline testen",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Pipeline testen",
			"lineHeight": 1.25,
			"baseline": 32
		},
		{
			"type": "text",
			"version": 62,
			"versionNonce": 1433347833,
			"isDeleted": false,
			"id": "CtXGEDip",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 4082.6213927087692,
			"y": 260.8119838888341,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 184.93191528320312,
			"height": 45,
			"seed": 990089525,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [
				{
					"id": "LB59msowcTk5Uxo2b9Rfd",
					"type": "arrow"
				},
				{
					"id": "oIzPdMSpsgvX29mba4RNm",
					"type": "arrow"
				},
				{
					"id": "NXWlWBzk5bB6Fz-hnIdJ2",
					"type": "arrow"
				}
			],
			"updated": 1710252160952,
			"link": null,
			"locked": false,
			"fontSize": 36,
			"fontFamily": 1,
			"text": "Experiment",
			"rawText": "Experiment",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Experiment",
			"lineHeight": 1.25,
			"baseline": 32
		},
		{
			"type": "text",
			"version": 287,
			"versionNonce": 1505075479,
			"isDeleted": false,
			"id": "spCg6y4Z",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 4722.120545497621,
			"y": 255.75509074150636,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 210.20391845703125,
			"height": 45,
			"seed": 727570011,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [
				{
					"id": "hbWz9-KAh17oqvglQncdB",
					"type": "arrow"
				},
				{
					"id": "NXWlWBzk5bB6Fz-hnIdJ2",
					"type": "arrow"
				},
				{
					"id": "LOjgUhyGijv8XIpMbMyyp",
					"type": "arrow"
				}
			],
			"updated": 1710252160952,
			"link": null,
			"locked": false,
			"fontSize": 36,
			"fontFamily": 1,
			"text": "Modell Swap",
			"rawText": "Modell Swap",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Modell Swap",
			"lineHeight": 1.25,
			"baseline": 32
		},
		{
			"type": "text",
			"version": 190,
			"versionNonce": 2126634969,
			"isDeleted": false,
			"id": "uCIhlCXI",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 4407.338728608096,
			"y": 252.86964477447805,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 159.5519256591797,
			"height": 45,
			"seed": 1590199451,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [
				{
					"id": "oIzPdMSpsgvX29mba4RNm",
					"type": "arrow"
				},
				{
					"id": "hbWz9-KAh17oqvglQncdB",
					"type": "arrow"
				}
			],
			"updated": 1710252160952,
			"link": null,
			"locked": false,
			"fontSize": 36,
			"fontFamily": 1,
			"text": "Ergebniss",
			"rawText": "Ergebniss",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Ergebniss",
			"lineHeight": 1.25,
			"baseline": 32
		},
		{
			"type": "arrow",
			"version": 34,
			"versionNonce": 783246903,
			"isDeleted": false,
			"id": "FsblHk68_ohmO9GPzS9oK",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 3527.6866815007875,
			"y": 290.8645003062663,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 151.54027677888735,
			"height": 5.37513906274944,
			"seed": 1719274555,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1710252160952,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "7s8gxoce",
				"focus": 0.0047161757610838274,
				"gap": 9.207677956854695
			},
			"endBinding": {
				"elementId": "bdADuUFt",
				"focus": 0.20439394071930025,
				"gap": 9.866568557070423
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					151.54027677888735,
					-5.37513906274944
				]
			]
		},
		{
			"type": "arrow",
			"version": 46,
			"versionNonce": 1661631673,
			"isDeleted": false,
			"id": "LB59msowcTk5Uxo2b9Rfd",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 3951.7605614122167,
			"y": 290.4780523997941,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 117.62947298595327,
			"height": 5.954810922457682,
			"seed": 885997781,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1710252160952,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "bdADuUFt",
				"focus": 0.3844052307420361,
				"gap": 5.267193266877712
			},
			"endBinding": {
				"elementId": "CtXGEDip",
				"focus": 0.15229441062820182,
				"gap": 13.231358310599262
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					117.62947298595327,
					-5.954810922457682
				]
			]
		},
		{
			"type": "arrow",
			"version": 61,
			"versionNonce": 108234583,
			"isDeleted": false,
			"id": "oIzPdMSpsgvX29mba4RNm",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 4274.374300060767,
			"y": 283.60103624598224,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 122.10875553824462,
			"height": 5.4805339463326845,
			"seed": 821152757,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1710252160952,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "CtXGEDip",
				"focus": 0.17805899253569227,
				"gap": 6.820992068795022
			},
			"endBinding": {
				"elementId": "uCIhlCXI",
				"focus": 0.05049389047473532,
				"gap": 10.855673009084057
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					122.10875553824462,
					-5.4805339463326845
				]
			]
		},
		{
			"type": "arrow",
			"version": 167,
			"versionNonce": 1911324057,
			"isDeleted": false,
			"id": "hbWz9-KAh17oqvglQncdB",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 4576.479950945397,
			"y": 272.1062044237958,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 140.22789260761056,
			"height": 1.5023394450463456,
			"seed": 1584596597,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1710252160952,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "uCIhlCXI",
				"focus": -0.18834934143803106,
				"gap": 9.589296678121173
			},
			"endBinding": {
				"elementId": "spCg6y4Z",
				"focus": 0.14655631500963476,
				"gap": 5.412701944613218
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					140.22789260761056,
					1.5023394450463456
				]
			]
		},
		{
			"type": "arrow",
			"version": 340,
			"versionNonce": 1331070071,
			"isDeleted": false,
			"id": "NXWlWBzk5bB6Fz-hnIdJ2",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 4822.247762844735,
			"y": 313.79667039260454,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 654.9019670628321,
			"height": 220.10238518851696,
			"seed": 1412108085,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "GmTrhxDK"
				}
			],
			"updated": 1710252160952,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "spCg6y4Z",
				"focus": -0.35609204271878087,
				"gap": 13.041579651098175
			},
			"endBinding": {
				"elementId": "CtXGEDip",
				"focus": 0.438360956456852,
				"gap": 10.001299240036758
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					-338.9998064344571,
					220.10238518851696
				],
				[
					-654.9019670628321,
					2.0166127362662998
				]
			]
		},
		{
			"type": "text",
			"version": 29,
			"versionNonce": 1520132729,
			"isDeleted": false,
			"id": "GmTrhxDK",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 4360.650010243286,
			"y": 488.8990555811215,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 245.19589233398438,
			"height": 90,
			"seed": 1755246363,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160952,
			"link": null,
			"locked": false,
			"fontSize": 36,
			"fontFamily": 1,
			"text": "Neues Modell/\nandere OCR",
			"rawText": "Neues Modell/\nandere OCR",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "NXWlWBzk5bB6Fz-hnIdJ2",
			"originalText": "Neues Modell/\nandere OCR",
			"lineHeight": 1.25,
			"baseline": 77
		},
		{
			"type": "arrow",
			"version": 79,
			"versionNonce": 958193047,
			"isDeleted": false,
			"id": "svjNys6CeIVxfQI4haK6H",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 3026.6833194805,
			"y": 295.8004940207524,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 244.41951793669023,
			"height": 0.008782906965279835,
			"seed": 1442159931,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1710252160952,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "jvSjlKg0",
				"focus": -0.19187488021411997,
				"gap": 10.444093075807814
			},
			"endBinding": {
				"elementId": "7s8gxoce",
				"focus": -0.021707580371712408,
				"gap": 7.148291370883271
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					244.41951793669023,
					0.008782906965279835
				]
			]
		},
		{
			"type": "text",
			"version": 184,
			"versionNonce": 983838584,
			"isDeleted": false,
			"id": "eVRLPXoH",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 2774.8157305504983,
			"y": 337.83936686303423,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 249.59188842773438,
			"height": 70,
			"seed": 577064923,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1711005973777,
			"link": null,
			"locked": false,
			"fontSize": 28,
			"fontFamily": 1,
			"text": "~1000 Rechnungen\nvia. Azure",
			"rawText": "~1000 Rechnungen\nvia. Azure",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "~1000 Rechnungen\nvia. Azure",
			"lineHeight": 1.25,
			"baseline": 59
		},
		{
			"type": "text",
			"version": 174,
			"versionNonce": 1418896392,
			"isDeleted": false,
			"id": "dPeJIHKM",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 3203.4401662038103,
			"y": 330.6607578207522,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 352.96783447265625,
			"height": 35,
			"seed": 1290829301,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1711005973777,
			"link": null,
			"locked": false,
			"fontSize": 28,
			"fontFamily": 1,
			"text": "- Sparrow Anpassung ELO",
			"rawText": "- Sparrow Anpassung ELO",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "- Sparrow Anpassung ELO",
			"lineHeight": 1.25,
			"baseline": 24
		},
		{
			"type": "text",
			"version": 147,
			"versionNonce": 1851752568,
			"isDeleted": false,
			"id": "StvMzI98",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 3228.799734157157,
			"y": 379.3400714500318,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 280.9798583984375,
			"height": 35,
			"seed": 2054524219,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1711005973778,
			"link": null,
			"locked": false,
			"fontSize": 28,
			"fontFamily": 1,
			"text": "- FineTuning Sparrow",
			"rawText": "- FineTuning Sparrow",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "- FineTuning Sparrow",
			"lineHeight": 1.25,
			"baseline": 24
		},
		{
			"type": "text",
			"version": 86,
			"versionNonce": 563454935,
			"isDeleted": false,
			"id": "npz1A8Vq",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 5154.731065207717,
			"y": 246.72261698660685,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 425.73583984375,
			"height": 45,
			"seed": 779186523,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [
				{
					"id": "LOjgUhyGijv8XIpMbMyyp",
					"type": "arrow"
				}
			],
			"updated": 1710252160953,
			"link": null,
			"locked": false,
			"fontSize": 36,
			"fontFamily": 1,
			"text": "Flows-Kompatibel machen",
			"rawText": "Flows-Kompatibel machen",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Flows-Kompatibel machen",
			"lineHeight": 1.25,
			"baseline": 32
		},
		{
			"type": "arrow",
			"version": 65,
			"versionNonce": 652765465,
			"isDeleted": false,
			"id": "LOjgUhyGijv8XIpMbMyyp",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 4943.755354927946,
			"y": 281.8745814951412,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 201.23032352480095,
			"height": 8.397187752493323,
			"seed": 1592846267,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1710252160953,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "spCg6y4Z",
				"focus": 0.3154940482437961,
				"gap": 11.430890973294481
			},
			"endBinding": {
				"elementId": "npz1A8Vq",
				"focus": 0.16042877077533044,
				"gap": 9.745386754969331
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					201.23032352480095,
					-8.397187752493323
				]
			]
		},
		{
			"type": "text",
			"version": 227,
			"versionNonce": 1236329224,
			"isDeleted": false,
			"id": "RTFQL0hQ",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 3281.7456010173414,
			"y": 431.39337887697843,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 152.57192993164062,
			"height": 35,
			"seed": 820481979,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1711005973780,
			"link": null,
			"locked": false,
			"fontSize": 28,
			"fontFamily": 1,
			"text": "- Inference",
			"rawText": "- Inference",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "- Inference",
			"lineHeight": 1.25,
			"baseline": 24
		},
		{
			"type": "text",
			"version": 1720,
			"versionNonce": 277393784,
			"isDeleted": false,
			"id": "kC4X6XX2",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 868.4554143664736,
			"y": 1285.7040595395806,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 1658.9991455078125,
			"height": 980,
			"seed": 515852187,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1711005973783,
			"link": null,
			"locked": false,
			"fontSize": 28,
			"fontFamily": 1,
			"text": "10 - 20 genau anschauen\nEffizienz auf 1000 prüfen --> GPUh oder Kosten betrachten\nNicht zu viele verschiedene Modelle\nEine Refferenz --> Das möchten wir haben\nDann 2-3 Aufbauten\nSchlussstrich Ende 2023\n\n1. Einleitung: Das Ziel dieser Arbeit ist: Dann Ziel der Arbeit\n2. Um dieses Ziel zu beantworten machen wir: Experiment bewertung etc. deswegen ist die Arbeit so aufgebaut:\nDann so viel einleitend wir gehen jetzt in Kapitel 2\n3. Gliederung Theorie typischerweise zu groß max. 20 S\n4. OCR wichtig, dass es da drinne ist aber keine Details (Keine 5 Seiten für OCR, nur Details die ich brauche)\n5. Arbeit so dass der Leser immer weiß wo er ist und was er liest, an die Hand nehmen und durchführen\n(Es sollen nun OCR erklärt werden..)\n6. Methodik ausformulieren\n7. In 4. und 5. ich habe gemacht --> Wegen Eigenständigen Ergebnissen\n8. Bei Ergebnissen: Nicht nur Modelle reflektieren sondern auch kritische Reflektion des Vorgehens\nWenn ich es nochmal mache, was würde ich anders/besser machen \nAuch mit dem Betreuer zusammensetzten und Fragen: Was hätten wir vor 4 Monaten besser machen können\n9. Bewertungsstil: Formalien: 4, Wir biegen es noch hin 3, Liest sich flüssig: 2, Liest sich flüssig, keine Rechtschreibfehler\nKritische Distanz zu Quellen, Experiment funzt, Schöne Auswertung, Hinterfragen von Experiment: 1\n10. Keine Internetquellen\n11. Durchlesen lassen\n\nWenn ein Teil fertig, dann schicken\nBeschreibung wie Experiment aussieht, aber nicht was\nTIKZ: Latex Plugin für Skizzen --> ChatGPT\nFür Metriken graphische Aufbereitung: TGFPlots bzw TIKZ kann auch Balkendiagramme etc. ",
			"rawText": "10 - 20 genau anschauen\nEffizienz auf 1000 prüfen --> GPUh oder Kosten betrachten\nNicht zu viele verschiedene Modelle\nEine Refferenz --> Das möchten wir haben\nDann 2-3 Aufbauten\nSchlussstrich Ende 2023\n\n1. Einleitung: Das Ziel dieser Arbeit ist: Dann Ziel der Arbeit\n2. Um dieses Ziel zu beantworten machen wir: Experiment bewertung etc. deswegen ist die Arbeit so aufgebaut:\nDann so viel einleitend wir gehen jetzt in Kapitel 2\n3. Gliederung Theorie typischerweise zu groß max. 20 S\n4. OCR wichtig, dass es da drinne ist aber keine Details (Keine 5 Seiten für OCR, nur Details die ich brauche)\n5. Arbeit so dass der Leser immer weiß wo er ist und was er liest, an die Hand nehmen und durchführen\n(Es sollen nun OCR erklärt werden..)\n6. Methodik ausformulieren\n7. In 4. und 5. ich habe gemacht --> Wegen Eigenständigen Ergebnissen\n8. Bei Ergebnissen: Nicht nur Modelle reflektieren sondern auch kritische Reflektion des Vorgehens\nWenn ich es nochmal mache, was würde ich anders/besser machen \nAuch mit dem Betreuer zusammensetzten und Fragen: Was hätten wir vor 4 Monaten besser machen können\n9. Bewertungsstil: Formalien: 4, Wir biegen es noch hin 3, Liest sich flüssig: 2, Liest sich flüssig, keine Rechtschreibfehler\nKritische Distanz zu Quellen, Experiment funzt, Schöne Auswertung, Hinterfragen von Experiment: 1\n10. Keine Internetquellen\n11. Durchlesen lassen\n\nWenn ein Teil fertig, dann schicken\nBeschreibung wie Experiment aussieht, aber nicht was\nTIKZ: Latex Plugin für Skizzen --> ChatGPT\nFür Metriken graphische Aufbereitung: TGFPlots bzw TIKZ kann auch Balkendiagramme etc. ",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "10 - 20 genau anschauen\nEffizienz auf 1000 prüfen --> GPUh oder Kosten betrachten\nNicht zu viele verschiedene Modelle\nEine Refferenz --> Das möchten wir haben\nDann 2-3 Aufbauten\nSchlussstrich Ende 2023\n\n1. Einleitung: Das Ziel dieser Arbeit ist: Dann Ziel der Arbeit\n2. Um dieses Ziel zu beantworten machen wir: Experiment bewertung etc. deswegen ist die Arbeit so aufgebaut:\nDann so viel einleitend wir gehen jetzt in Kapitel 2\n3. Gliederung Theorie typischerweise zu groß max. 20 S\n4. OCR wichtig, dass es da drinne ist aber keine Details (Keine 5 Seiten für OCR, nur Details die ich brauche)\n5. Arbeit so dass der Leser immer weiß wo er ist und was er liest, an die Hand nehmen und durchführen\n(Es sollen nun OCR erklärt werden..)\n6. Methodik ausformulieren\n7. In 4. und 5. ich habe gemacht --> Wegen Eigenständigen Ergebnissen\n8. Bei Ergebnissen: Nicht nur Modelle reflektieren sondern auch kritische Reflektion des Vorgehens\nWenn ich es nochmal mache, was würde ich anders/besser machen \nAuch mit dem Betreuer zusammensetzten und Fragen: Was hätten wir vor 4 Monaten besser machen können\n9. Bewertungsstil: Formalien: 4, Wir biegen es noch hin 3, Liest sich flüssig: 2, Liest sich flüssig, keine Rechtschreibfehler\nKritische Distanz zu Quellen, Experiment funzt, Schöne Auswertung, Hinterfragen von Experiment: 1\n10. Keine Internetquellen\n11. Durchlesen lassen\n\nWenn ein Teil fertig, dann schicken\nBeschreibung wie Experiment aussieht, aber nicht was\nTIKZ: Latex Plugin für Skizzen --> ChatGPT\nFür Metriken graphische Aufbereitung: TGFPlots bzw TIKZ kann auch Balkendiagramme etc. ",
			"lineHeight": 1.25,
			"baseline": 969
		},
		{
			"type": "text",
			"version": 116,
			"versionNonce": 514802184,
			"isDeleted": false,
			"id": "kY3fi9wB",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -2514.2089124661907,
			"y": -395.17023196132243,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 183.6239013671875,
			"height": 35,
			"seed": 963797653,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1711005973784,
			"link": null,
			"locked": false,
			"fontSize": 28,
			"fontFamily": 1,
			"text": "Classification",
			"rawText": "Classification",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Classification",
			"lineHeight": 1.25,
			"baseline": 24
		},
		{
			"type": "text",
			"version": 188,
			"versionNonce": 1482932856,
			"isDeleted": false,
			"id": "DoBWY3zE",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -2418.7532244285826,
			"y": -587.8225666479952,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 38.10798645019531,
			"height": 35,
			"seed": 1972053819,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1711005973784,
			"link": null,
			"locked": false,
			"fontSize": 28,
			"fontFamily": 1,
			"text": "QA",
			"rawText": "QA",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "QA",
			"lineHeight": 1.25,
			"baseline": 24
		},
		{
			"type": "text",
			"version": 79,
			"versionNonce": 579453192,
			"isDeleted": false,
			"id": "oPfX0jNz",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -2602.5109933183367,
			"y": -736.0845822368781,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 131.3759307861328,
			"height": 35,
			"seed": 1235639445,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1711005973784,
			"link": null,
			"locked": false,
			"fontSize": 28,
			"fontFamily": 1,
			"text": "Extraktiv",
			"rawText": "Extraktiv",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Extraktiv",
			"lineHeight": 1.25,
			"baseline": 24
		},
		{
			"type": "text",
			"version": 131,
			"versionNonce": 1957999480,
			"isDeleted": false,
			"id": "zbfCLHvA",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -2249.698717366385,
			"y": -705.077366777864,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 232.5398712158203,
			"height": 35,
			"seed": 573111835,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1711005973785,
			"link": null,
			"locked": false,
			"fontSize": 28,
			"fontFamily": 1,
			"text": "Swin-Transformer",
			"rawText": "Swin-Transformer",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Swin-Transformer",
			"lineHeight": 1.25,
			"baseline": 24
		},
		{
			"type": "text",
			"version": 123,
			"versionNonce": 1690066952,
			"isDeleted": false,
			"id": "Q7oADDsB",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -1902.5961255809148,
			"y": -776.7207014853196,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 127.595947265625,
			"height": 35,
			"seed": 718363477,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1711005973785,
			"link": null,
			"locked": false,
			"fontSize": 28,
			"fontFamily": 1,
			"text": "OCR-Free",
			"rawText": "OCR-Free",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "OCR-Free",
			"lineHeight": 1.25,
			"baseline": 24
		},
		{
			"type": "text",
			"version": 122,
			"versionNonce": 465536120,
			"isDeleted": false,
			"id": "Z1RkZv9A",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -2737.100633100756,
			"y": 80.74016463573935,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 279.60784912109375,
			"height": 105,
			"seed": 125882773,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1711005973786,
			"link": null,
			"locked": false,
			"fontSize": 28,
			"fontFamily": 1,
			"text": "Donut Paper:\nSwin kann durch CNN\nersetzt werden",
			"rawText": "Donut Paper:\nSwin kann durch CNN\nersetzt werden",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Donut Paper:\nSwin kann durch CNN\nersetzt werden",
			"lineHeight": 1.25,
			"baseline": 94
		},
		{
			"type": "text",
			"version": 130,
			"versionNonce": 625155848,
			"isDeleted": false,
			"id": "8Ddj1mKM",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 593.6532740630778,
			"y": 248.09382159625704,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 256.2279052734375,
			"height": 105,
			"seed": 59842555,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1711005973786,
			"link": null,
			"locked": false,
			"fontSize": 28,
			"fontFamily": 1,
			"text": "Limitation auf:\n1 Refferrenzmodell\n2 Vergleichsmodelle",
			"rawText": "Limitation auf:\n1 Refferrenzmodell\n2 Vergleichsmodelle",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Limitation auf:\n1 Refferrenzmodell\n2 Vergleichsmodelle",
			"lineHeight": 1.25,
			"baseline": 94
		},
		{
			"type": "text",
			"version": 38,
			"versionNonce": 547789177,
			"isDeleted": false,
			"id": "pt2kV4O2",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 866.7387159175505,
			"y": 1214.9545071821174,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 389.267822265625,
			"height": 45,
			"seed": 1776792821,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160953,
			"link": null,
			"locked": false,
			"fontSize": 36,
			"fontFamily": 1,
			"text": "Offtermatt Feedback:",
			"rawText": "Offtermatt Feedback:",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Offtermatt Feedback:",
			"lineHeight": 1.25,
			"baseline": 32
		},
		{
			"type": "text",
			"version": 200,
			"versionNonce": 457717112,
			"isDeleted": false,
			"id": "fVH5yFv9",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1152.9201046434653,
			"y": -505.4714034677073,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 735.0277099609375,
			"height": 105,
			"seed": 943623989,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1711005973787,
			"link": null,
			"locked": false,
			"fontSize": 28,
			"fontFamily": 1,
			"text": "Ist OCR+Bert nicht vielleicht schon outdated?\nEvtl. neuere Modelle? --> Grundlagenmodell, Herzstück\n--> Neues wie DUBLIN",
			"rawText": "Ist OCR+Bert nicht vielleicht schon outdated?\nEvtl. neuere Modelle? --> Grundlagenmodell, Herzstück\n--> Neues wie DUBLIN",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Ist OCR+Bert nicht vielleicht schon outdated?\nEvtl. neuere Modelle? --> Grundlagenmodell, Herzstück\n--> Neues wie DUBLIN",
			"lineHeight": 1.25,
			"baseline": 94
		},
		{
			"type": "text",
			"version": 82,
			"versionNonce": 1150942728,
			"isDeleted": false,
			"id": "rwgMZMSa",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1150.6111870555892,
			"y": -549.6331936966902,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 626.6956787109375,
			"height": 35,
			"seed": 1073982613,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1711005973788,
			"link": null,
			"locked": false,
			"fontSize": 28,
			"fontFamily": 1,
			"text": "Betrachtung der wirtschaftlichkeit von BERT",
			"rawText": "Betrachtung der wirtschaftlichkeit von BERT",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Betrachtung der wirtschaftlichkeit von BERT",
			"lineHeight": 1.25,
			"baseline": 24
		},
		{
			"type": "text",
			"version": 31,
			"versionNonce": 1754449528,
			"isDeleted": false,
			"id": "LqMd2y83",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1154.0529970138361,
			"y": -584.431191593187,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 300.411865234375,
			"height": 35,
			"seed": 1979448693,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1711005973788,
			"link": null,
			"locked": false,
			"fontSize": 28,
			"fontFamily": 1,
			"text": "Wirtschaftsseite OCR",
			"rawText": "Wirtschaftsseite OCR",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Wirtschaftsseite OCR",
			"lineHeight": 1.25,
			"baseline": 24
		},
		{
			"type": "text",
			"version": 19,
			"versionNonce": 266817337,
			"isDeleted": false,
			"id": "G3JKh93E",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 2135.3089746548,
			"y": 695.7453191944852,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 195.73194885253906,
			"height": 45,
			"seed": 733206715,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160953,
			"link": null,
			"locked": false,
			"fontSize": 36,
			"fontFamily": 1,
			"text": "Acc /= Acc",
			"rawText": "Acc /= Acc",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Acc /= Acc",
			"lineHeight": 1.25,
			"baseline": 32
		},
		{
			"type": "image",
			"version": 203,
			"versionNonce": 1080237271,
			"isDeleted": false,
			"id": "qY1aJPnnmIoEddiVSYOM3",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -218.33662392945155,
			"y": -3084.529110588932,
			"strokeColor": "transparent",
			"backgroundColor": "#ffc9c9",
			"width": 1816.8320312499998,
			"height": 1207.1973629568106,
			"seed": 2001791003,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160953,
			"link": null,
			"locked": false,
			"status": "pending",
			"fileId": "c64d24b765085d3519ee7c9c406d8490efba0bca",
			"scale": [
				1,
				1
			]
		},
		{
			"type": "text",
			"version": 70,
			"versionNonce": 1082851353,
			"isDeleted": false,
			"id": "EEMK3wnK",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 317.58439021572383,
			"y": -3157.0493829006027,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 654.5517578125,
			"height": 45,
			"seed": 2121879195,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160953,
			"link": null,
			"locked": false,
			"fontSize": 36,
			"fontFamily": 1,
			"text": "CRISP-DM als Datamining Framework",
			"rawText": "CRISP-DM als Datamining Framework",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "CRISP-DM als Datamining Framework",
			"lineHeight": 1.25,
			"baseline": 32
		},
		{
			"type": "text",
			"version": 70,
			"versionNonce": 565668343,
			"isDeleted": false,
			"id": "02kS9RHP",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1335.749297056676,
			"y": 869.042781667411,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 203.95985412597656,
			"height": 25,
			"seed": 2101681241,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160953,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "Wie messe ich GPU/h",
			"rawText": "Wie messe ich GPU/h",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Wie messe ich GPU/h",
			"lineHeight": 1.25,
			"baseline": 18
		},
		{
			"type": "text",
			"version": 90,
			"versionNonce": 122000633,
			"isDeleted": false,
			"id": "CZRxvirA",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1665.9618993642366,
			"y": 859.7047745293132,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 422.5396423339844,
			"height": 25,
			"seed": 1124097431,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160953,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "Kosten vom Training oder nur Pre-Training?",
			"rawText": "Kosten vom Training oder nur Pre-Training?",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Kosten vom Training oder nur Pre-Training?",
			"lineHeight": 1.25,
			"baseline": 18
		},
		{
			"type": "text",
			"version": 84,
			"versionNonce": 868023560,
			"isDeleted": false,
			"id": "kpEg77cn",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -40.68974455399962,
			"y": 1242.6227550636042,
			"strokeColor": "#2f9e44",
			"backgroundColor": "#ffc9c9",
			"width": 315.78387451171875,
			"height": 35,
			"seed": 412780281,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1711005973790,
			"link": null,
			"locked": false,
			"fontSize": 28,
			"fontFamily": 1,
			"text": "Evtl. mit CORD testen",
			"rawText": "Evtl. mit CORD testen",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Evtl. mit CORD testen",
			"lineHeight": 1.25,
			"baseline": 24
		},
		{
			"type": "text",
			"version": 137,
			"versionNonce": 811808632,
			"isDeleted": false,
			"id": "KGP34Je3",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 616.5928218557626,
			"y": 979.0397642905596,
			"strokeColor": "#2f9e44",
			"backgroundColor": "#ffc9c9",
			"width": 298.1158752441406,
			"height": 35,
			"seed": 1881925753,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1711005973790,
			"link": null,
			"locked": false,
			"fontSize": 28,
			"fontFamily": 1,
			"text": "Die 1000 die ich habe",
			"rawText": "Die 1000 die ich habe",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Die 1000 die ich habe",
			"lineHeight": 1.25,
			"baseline": 24
		},
		{
			"type": "text",
			"version": 76,
			"versionNonce": 1680350216,
			"isDeleted": false,
			"id": "t1s4fSqD",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 602.8495907088036,
			"y": 1108.6706157873875,
			"strokeColor": "#2f9e44",
			"backgroundColor": "#ffc9c9",
			"width": 323.2318115234375,
			"height": 35,
			"seed": 968714617,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1711005973790,
			"link": null,
			"locked": false,
			"fontSize": 28,
			"fontFamily": 1,
			"text": "Anonymisiert von Kunden",
			"rawText": "Anonymisiert von Kunden",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Anonymisiert von Kunden",
			"lineHeight": 1.25,
			"baseline": 24
		},
		{
			"type": "text",
			"version": 39,
			"versionNonce": 1727891576,
			"isDeleted": false,
			"id": "ITS51aOl",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1080.4152466011128,
			"y": 985.455117846175,
			"strokeColor": "#2f9e44",
			"backgroundColor": "#ffc9c9",
			"width": 77.64396667480469,
			"height": 35,
			"seed": 118959159,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1711005973791,
			"link": null,
			"locked": false,
			"fontSize": 28,
			"fontFamily": 1,
			"text": "Azure",
			"rawText": "Azure",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Azure",
			"lineHeight": 1.25,
			"baseline": 24
		},
		{
			"type": "text",
			"version": 38,
			"versionNonce": 1246656855,
			"isDeleted": false,
			"id": "IKkGwmwm",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -467.4654021585684,
			"y": 1258.6652733485826,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 150.63987731933594,
			"height": 25,
			"seed": 434906839,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160953,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "Welche Aufgabe",
			"rawText": "Welche Aufgabe",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Welche Aufgabe",
			"lineHeight": 1.25,
			"baseline": 18
		},
		{
			"type": "text",
			"version": 40,
			"versionNonce": 586263449,
			"isDeleted": false,
			"id": "Th9MkAuG",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -646.4992518376305,
			"y": 1305.1935138305976,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 74.27995300292969,
			"height": 25,
			"seed": 1837987895,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160953,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "DocVQA",
			"rawText": "DocVQA",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "DocVQA",
			"lineHeight": 1.25,
			"baseline": 18
		},
		{
			"type": "text",
			"version": 48,
			"versionNonce": 2130916983,
			"isDeleted": false,
			"id": "jnnNh8Kd",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -512.2499778667582,
			"y": 1382.304705973032,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 69.75993347167969,
			"height": 25,
			"seed": 1417511353,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710252160953,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "Parsing",
			"rawText": "Parsing",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Parsing",
			"lineHeight": 1.25,
			"baseline": 18
		},
		{
			"type": "text",
			"version": 35,
			"versionNonce": 272374879,
			"isDeleted": false,
			"id": "ILK4au7K",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -303.3524975019852,
			"y": 1355.4487212989457,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#ffc9c9",
			"width": 131.15992954799108,
			"height": 25,
			"seed": 1755367543,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1712211493669,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "Classification",
			"rawText": "Classification",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Classification",
			"lineHeight": 1.25,
			"baseline": 18
		}
	],
	"appState": {
		"theme": "dark",
		"viewBackgroundColor": "#ffffff",
		"currentItemStrokeColor": "#1971c2",
		"currentItemBackgroundColor": "#ffc9c9",
		"currentItemFillStyle": "solid",
		"currentItemStrokeWidth": 4,
		"currentItemStrokeStyle": "dashed",
		"currentItemRoughness": 1,
		"currentItemOpacity": 100,
		"currentItemFontFamily": 1,
		"currentItemFontSize": 20,
		"currentItemTextAlign": "left",
		"currentItemStartArrowhead": null,
		"currentItemEndArrowhead": "arrow",
		"scrollX": -33.373628797637245,
		"scrollY": 1150.1018084407465,
		"zoom": {
			"value": 0.34045840352773693
		},
		"currentItemRoundness": "round",
		"gridSize": null,
		"gridColor": {
			"Bold": "#C9C9C9FF",
			"Regular": "#EDEDEDFF"
		},
		"currentStrokeOptions": {
			"highlighter": true,
			"constantPressure": true,
			"hasOutline": false,
			"outlineWidth": 1,
			"options": {
				"thinning": 1,
				"smoothing": 0.5,
				"streamline": 0.5,
				"easing": "linear",
				"start": {
					"cap": true,
					"taper": true,
					"easing": "linear"
				},
				"end": {
					"cap": true,
					"taper": true,
					"easing": "linear"
				}
			}
		},
		"previousGridSize": null,
		"frameRendering": {
			"enabled": true,
			"clip": true,
			"name": true,
			"outline": true
		}
	},
	"files": {}
}
```
%%