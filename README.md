# Debugging

Craps Game

-Found bug that allowed 11 to become the point on come out roll
 -Fixed bug by properly making a come out roll of 11 a winner

if (cr.isFrontlineWinner()) { 
	//Roll is a frontline winner 7 or 11! 
	System.out.println("Frontline Winner " + cr.getTotal() + "!"); 
	br.winner(cr.getTotal()); 
	frontlineWinner = true; 
}

Craps Game

-Found bug that caused the program to bomb faster than the Bengals in the playoffs if user input a non-numeric value for pass line or odds bet.
 -Fixed by verifying input is numeric before calling Integer.parseInt.

private static int readBetIn(Scanner scan) {
	 String input = scan.nextLine(); 
	while (!input.matches("\d+$")) { 
		System.out.println("Invalid bet, try again");
		 input = scan.nextLine(); 
	} 
	return Integer.parseInt(input);
 }

Craps Game

-Found bug that allowed user to input odds bet in excess of the maximum odds

-Fixed the bug by comparing the odds bet to the original line bet and re-asking the user if over max

if (bet > cash || bet < 0 || bet > (this.passLineBet * this.maxOdds))
