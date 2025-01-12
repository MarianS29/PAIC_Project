# PAIC_Project
Script that eliminates noise from infrared images.
It eliminated 2 types of noise: gaussian and impulsive (salt & pepper)

-> It uses 3x3 window to determine which category is the center pixel (gaussian noise, impulsive noise or detail point)
-> If it's gaussian noise point => apply a self-weighted mean filter
-> If it's impulsive noise point => apply a self-weighted median filter
-> If it's detail point it stays the same
-> self-weighted - to preserve image details while eliminating unwanted noise

Results are tested with MSE/NMSE/PSNR for more images with more noise types.

######################################################################################################
######################################################################################################

-> proiect PAIC ----------------- Deadine: 21 ianuarie 23:59 (tema 24)

-> implementarea + testarea unui algoritm de fitrare de zgomot pe imagini color
-> articol cu imagini grayscale -> extindere pe color prin aplicare pe fiecare plan RGB
-> rezultate:
	-> reducere de zgomot pt imagini cu continut diferit
	-> mai multe tipuri de zgomot
	-> mai multe intensitati ale zgomotului

-> set minim de testare:
	-> 5 img cu zgomot aditiv gaussian, deviatie standard 10 + 10% zgomot impulsiv
	-> 2 img pt testare a intensitatilor de zgomot (minim 3 intensitati per imagine => minim 6 img)

-> comparare performante cu filtrul MEDIE ARITMETICA si filtrul MEDIAN
	-> implementate pe vec 3x3 si aplicate pe fiecare plan RGB
	-> obs susbiectiva: pastrarea detaliilor, contururi, artefacte etc.
	-> obs obiective: mimim 2 masuri (SNR/PSNR, MAE, SSIM etc.)

-> document scris cu:
	-> descrierea filtrului cu cuvintele noastre (!)
	-> descrierea modului de implementare
	-> experimente
	-> concluzii
	-> comentarii personale
	-> referinte bibliografice
	
-> predare 2 fisiere:
	-> pdf cu documentul
	-> zip cu codul sursa

-> orice idee preluata -> CITARE
