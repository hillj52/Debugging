# Debugging

Craps Game
-Found bug that allowed 11 to become the point on come out roll
-Fixed bug by properly making a come out roll of 11 a winner

if (cr.isFrontlineWinner()) {
				//Roll is a frontline winner 7 or 11!
				System.out.println("Frontline Winner " + cr.getTotal() + "!");
				br.winner(cr.getTotal());
				frontlineWinner = true;
