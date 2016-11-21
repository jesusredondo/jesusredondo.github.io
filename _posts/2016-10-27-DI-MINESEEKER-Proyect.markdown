---
layout: post
title:  "MineSeeker [DI]"
date:   2016-10-27 18:23:00 +0100
categories: teaching
tags: DI github Swing java
---
After seeying the main components in the Swing library it was time to develop a full project. Moreover it was a perfect opportunity to learn the very basics of git. So I prepared [these slides](http://www.slideshare.net/JessRedondoGarca/git-i-fork-commit-pull-push) and a [base project in github](https://github.com/jesusredondo/Ejercicio35-Base).

The base project used 2 classes to detach the logic from the visuals. The MVC is not 100% used because the View acts as controller (listerners). The model is 100% detached, but it is not observable.

The base project & documentation can be found clicking in the following image:

[![Mineseeker screen](/images/mineseeker.png)](https://github.com/jesusredondo/Ejercicio35-Base).

The controller was represented by:

```java
	private final static int MINA = -1;
	final int MINAS_INICIALES = 20;
	final int LADO_TABLERO = 10;

	private int [][] tablero;
	private int puntuacion;
```

To initialitlice the board it was necessary to place ```MINAS_INICIALES```mines in the ```tablero```(board):

```java
	/**Método para generar un nuevo tablero de partida:
	 * @pre: La estructura del tablero debe existir 
	 * @post: Al final el tablero se habrá inicializado con tantas minas como marque la variable MINAS_INICIALES. 
	 * 			El resto de posiciones que no son minas guardan en el entero cuántas minas hay alrededor de la celda
	 */
	public void inicializarPartida(){
		

		//Borro del tablero la información que pudiera haber anteriormente (los pongo todos a cero):
		for (int i = 0; i < tablero.length; i++) {
			for (int j = 0; j < tablero[i].length; j++) {
				tablero[i][j] = 0;
			}
		}
		
		//Me creo LADO_TABLERO*LADO_TABLERO números en un array list, uno para cada una de las posiciones del tablero:
		ArrayList<Integer> posicionesMina = new ArrayList<Integer>();
		for (int i = 0; i < (LADO_TABLERO*LADO_TABLERO); i++) {
			posicionesMina.add(i);
		}
		
		//Saco 20 posiciones sin repetir del array y les coloco una mina en el tablero:
		Random rd = new Random();
		for (int i = 0; i < MINAS_INICIALES; i++) {
			int iPosElegida = rd.nextInt(posicionesMina.size());
			int posElegida = posicionesMina.get(iPosElegida);
			posicionesMina.remove(iPosElegida);
			//Meto una mina en esa posición:
			tablero[posElegida/LADO_TABLERO][posElegida%LADO_TABLERO] = MINA;
		}
		
		//Calculo para todas las posiciones que no tienen minas, cuántas minas hay alrededor.
		for (int i = 0; i < tablero.length; i++) {
			for (int j = 0; j < tablero[i].length; j++) {
				if (tablero[i][j] != MINA){
					tablero[i][j] = calculoMinasAdjuntas(i,j);
				}
			}
		}
		
		//Pongo la puntuación a cero:
		puntuacion = 0;
		
	}
```

They had some problems with the logic of the game. Especially the chunks in which they had to figure out how many mines there were around a cell:

```java
	/**Cálculo de las minas adjuntas:
	 * Para calcular el número de minas tenemos que tener en cuenta que no nos salimos nunca del tablero.
	 * Por lo tanto, como mucho la i y la j valdrán LADO_TABLERO-1.
	 * Por lo tanto, como mucho la i y la j valdrán como poco 0.
	 * @param i: posición verticalmente de la casilla a rellenar
	 * @param j: posición horizontalmente de la casilla a rellenar
	 * @return : El número de minas que hay alrededor de la casilla [i][j]
	 */
	private int calculoMinasAdjuntas(int i, int j){
		int iInicial = Math.max(0, i-1) ;
		int iFinal = Math.min(LADO_TABLERO-1, i+1);
		int jInicial = Math.max(0, j-1);
		int jFinal = Math.min(LADO_TABLERO-1, j+1);
		
		
		int acumuladorMinas = 0;
		for (int indI = iInicial; indI <= iFinal; indI++) {
			for (int indJ = jInicial; indJ <= jFinal; indJ++) {
				if(tablero[indI][indJ] == MINA){
					acumuladorMinas++;
				}
			}
		}
			
		return acumuladorMinas;
	}
```

