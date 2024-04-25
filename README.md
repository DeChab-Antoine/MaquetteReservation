########### ITER1 ##############

## welcome.java :

package ilu2;

public class Welcome {
	
	public String welcome(String input) {
		
        return nomPropre(input);
    }
	
	private String nomPropre(String input) {
		
		StringBuilder chaine = new StringBuilder();
		chaine.append("Hello, ");
    	chaine.append(input.substring(0, 1).toUpperCase());
   		chaine.append(input.substring(1));
	    
	    return chaine.toString();
    }
}




## welcomeTest.java : 

package ilu2;

import static org.junit.jupiter.api.Assertions.*;

import org.junit.jupiter.api.BeforeEach;
import org.junit.jupiter.api.Test;

class WelcomeTest {
	
	Welcome welcome;
	
	@BeforeEach
	void init() {
        welcome = new Welcome();
	}
	

	@Test
	void testIter1() {
        assertEquals("Hello, Bob", welcome.welcome("bob"));
        assertNotEquals("Hello, bob", welcome.welcome("bob"));
        assertNotEquals("Hello, BOB", welcome.welcome("bob"));

    }

}


## commandes git : 

git add . 
git commit -m "ITER_1"


########### ITER2 ##############

## welcome.java :

package ilu2;

public class Welcome {
	
	public String welcome(String input) {
		if (input.toUpperCase().equals(input)) {
			return nomPropreMaj(input);
		}
		
        return nomPropre(input);
    }
	
	private String nomPropre(String input) {
		
		StringBuilder chaine = new StringBuilder();
		chaine.append("Hello, ");
    	chaine.append(input.substring(0, 1).toUpperCase());
   		chaine.append(input.substring(1));
	    
	    return chaine.toString();
    }
	
	private String nomPropreMaj(String input) {
		
		StringBuilder chaine = new StringBuilder();
		chaine.append("HELLO, ");
    	chaine.append(input);
   		chaine.append(" !");
	    
	    return chaine.toString();
    }
}

## welcomeTest.java : 

package ilu2;

import static org.junit.jupiter.api.Assertions.*;

import org.junit.jupiter.api.BeforeEach;
import org.junit.jupiter.api.Test;

class WelcomeTest {
	
	Welcome welcome;
	
	@BeforeEach
	void init() {
        welcome = new Welcome();
	}
	

	@Test
	void testIter1() {
        assertEquals("Hello, Bob", welcome.welcome("bob"));
        assertNotEquals("Hello, bob", welcome.welcome("bob"));
        assertNotEquals("Hello, BOB", welcome.welcome("bob"));

    }
	
	@Test
	void testIter2() {
        assertEquals("HELLO, JERRY !", welcome.welcome("JERRY"));
        assertNotEquals("Hello, JERRY !", welcome.welcome("JERRY"));
        assertNotEquals("HELLO, Jerry !", welcome.welcome("JERRY"));
        assertNotEquals("HELLO, JERRY", welcome.welcome("JERRY"));
    }
	
	

}


## commandes git : 

git add . 
git commit -m "ITER_2"


########### ITER3 ##############

## welcome.java :

package ilu2;

public class Welcome {
	
	public String welcome(String input) {
		if (input == null || input.trim().isEmpty()) {
			return "Hello, my friend";
		}
		
		if (input.toUpperCase().equals(input)) {
			return nomPropreMaj(input);
		}
		
        return nomPropre(input);
    }
	
	private String nomPropre(String input) {
		
		StringBuilder chaine = new StringBuilder();
		chaine.append("Hello, ");
    	chaine.append(input.substring(0, 1).toUpperCase());
   		chaine.append(input.substring(1));
	    
	    return chaine.toString();
    }
	
	private String nomPropreMaj(String input) {
		
		StringBuilder chaine = new StringBuilder();
		chaine.append("HELLO, ");
    	chaine.append(input);
   		chaine.append(" !");
	    
	    return chaine.toString();
    }
	
}

## welcomeTest.java : 

package ilu2;

import static org.junit.jupiter.api.Assertions.*;

import org.junit.jupiter.api.BeforeEach;
import org.junit.jupiter.api.Test;

class WelcomeTest {
	
	Welcome welcome;
	
	@BeforeEach
	void init() {
        welcome = new Welcome();
	}
	

	@Test
	void testIter1() {
        assertEquals("Hello, Bob", welcome.welcome("bob"));
        assertNotEquals("Hello, bob", welcome.welcome("bob"));
        assertNotEquals("Hello, BOB", welcome.welcome("bob"));

    }
	
	@Test
	void testIter2() {
        assertEquals("HELLO, JERRY !", welcome.welcome("JERRY"));
        assertNotEquals("Hello, JERRY !", welcome.welcome("JERRY"));
        assertNotEquals("HELLO, Jerry !", welcome.welcome("JERRY"));
        assertNotEquals("HELLO, JERRY", welcome.welcome("JERRY"));
    }
	
	@Test
	void testIter3() {
        assertEquals("Hello, my friend", welcome.welcome(""));
        assertEquals("Hello, my friend", welcome.welcome(null));
        assertEquals("Hello, my friend", welcome.welcome("      "));
    }
	
	
	
	

}


## commandes git : 

git add . 
git commit -m "ITER_3"


########### ITER4 ##############

## welcome.java :

package ilu2;

public class Welcome {
	
	public String welcome(String input) {
		if (input == null || input.trim().isEmpty()) {
			return "Hello, my friend";
		}
		
		input = input.trim();
		
		if (input.toUpperCase().equals(input)) {
			return nomPropreMaj(input);
		}
		
        return nomPropre(input);
    }
	
	private String nomPropre(String input) {
		
		StringBuilder chaine = new StringBuilder();
		chaine.append("Hello, ");
    	chaine.append(input.substring(0, 1).toUpperCase());
   		chaine.append(input.substring(1));
	    
	    return chaine.toString();
    }
	
	private String nomPropreMaj(String input) {
		
		StringBuilder chaine = new StringBuilder();
		chaine.append("HELLO, ");
    	chaine.append(input);
   		chaine.append(" !");
	    
	    return chaine.toString();
    }
	
}

## welcomeTest.java : 

package ilu2;

import static org.junit.jupiter.api.Assertions.*;

import org.junit.jupiter.api.BeforeEach;
import org.junit.jupiter.api.Test;

class WelcomeTest {
	
	Welcome welcome;
	
	@BeforeEach
	void init() {
        welcome = new Welcome();
	}
	

	@Test
	void testIter1() {
        assertEquals("Hello, Bob", welcome.welcome("bob"));
        assertNotEquals("Hello, bob", welcome.welcome("bob"));
        assertNotEquals("Hello, BOB", welcome.welcome("bob"));

    }
	
	@Test
	void testIter2() {
        assertEquals("HELLO, JERRY !", welcome.welcome("JERRY"));
        assertNotEquals("Hello, JERRY !", welcome.welcome("JERRY"));
        assertNotEquals("HELLO, Jerry !", welcome.welcome("JERRY"));
        assertNotEquals("HELLO, JERRY", welcome.welcome("JERRY"));
    }
	
	@Test
	void testIter3() {
        assertEquals("Hello, my friend", welcome.welcome(""));
        assertEquals("Hello, my friend", welcome.welcome(null));
        assertEquals("Hello, my friend", welcome.welcome("      "));
    }
	
	@Test
	void testIter4() {
        assertEquals("Hello, Bob", welcome.welcome("bob     "));
        assertEquals("Hello, Bob", welcome.welcome("    bob"));
        assertNotEquals("Hello,  Bob ", welcome.welcome(" bob "));
	}
	

}


## commandes git : 

git add . 
git commit -m "ITER_4"


########### ITER5 ##############

## welcome.java :

package ilu2;

public class Welcome {
	
	public String welcome(String input) {
		if (input == null || input.trim().isEmpty()) {
			return "Hello, my friend";
		}
		
		input = input.trim();
		
		if (input.contains(",")) {
            return deuxNoms(input.split(","));
        }
		
		if (input.toUpperCase().equals(input)) {
			return nomPropreMaj(input);
		}
		
        return nomPropre(input);
    }
	
	private String nomPropre(String input) {
		
		StringBuilder chaine = new StringBuilder();
		chaine.append("Hello, ");
    	chaine.append(input.substring(0, 1).toUpperCase());
    	chaine.append(input.substring(1));
	    
	    return chaine.toString();
    }
	
	private String nomPropreMaj(String input) {
		
		StringBuilder chaine = new StringBuilder();
		chaine.append("HELLO, ");
    	chaine.append(input);
   		chaine.append(" !");
	    
	    return chaine.toString();
    }
	
	private String deuxNoms(String[] noms) {
		StringBuilder chaine = new StringBuilder();
		chaine.append("Hello, ");
    	chaine.append(noms[0].substring(0, 1).toUpperCase());
    	chaine.append(noms[0].substring(1));
    	chaine.append(", ");
    	chaine.append(noms[1].substring(0, 1).toUpperCase());
    	chaine.append(noms[1].substring(1));
		return chaine.toString();
	}
	
}

## welcomeTest.java : 

package ilu2;

import static org.junit.jupiter.api.Assertions.*;

import org.junit.jupiter.api.BeforeEach;
import org.junit.jupiter.api.Test;

class WelcomeTest {
	
	Welcome welcome;
	
	@BeforeEach
	void init() {
        welcome = new Welcome();
	}
	

	@Test
	void testIter1() {
        assertEquals("Hello, Bob", welcome.welcome("bob"));
        assertNotEquals("Hello, bob", welcome.welcome("bob"));
        assertNotEquals("Hello, BOB", welcome.welcome("bob"));

    }
	
	@Test
	void testIter2() {
        assertEquals("HELLO, JERRY !", welcome.welcome("JERRY"));
        assertNotEquals("Hello, JERRY !", welcome.welcome("JERRY"));
        assertNotEquals("HELLO, Jerry !", welcome.welcome("JERRY"));
        assertNotEquals("HELLO, JERRY", welcome.welcome("JERRY"));
    }
	
	@Test
	void testIter3() {
        assertEquals("Hello, my friend", welcome.welcome(""));
        assertEquals("Hello, my friend", welcome.welcome(null));
        assertEquals("Hello, my friend", welcome.welcome("      "));
    }
	
	@Test
	void testIter4() {
        assertEquals("Hello, Bob", welcome.welcome("bob     "));
        assertEquals("Hello, Bob", welcome.welcome("    bob"));
        assertNotEquals("Hello,  Bob ", welcome.welcome(" bob "));
	}
	
	@Test
	void testIter5() {
        assertEquals("Hello, Amy, Bob", welcome.welcome("amy,bob"));
        assertNotEquals("Hello, Amy", welcome.welcome("amy,bob"));
        assertNotEquals("Hello, Bob", welcome.welcome("amy,bob"));
	}
	
	

}


## commandes git : 

git add . 
git commit -m "ITER_5"


########### ITER6 ##############

## welcome.java :

package ilu2;

public class Welcome {
	
	public String welcome(String input) {
		if (input == null || input.trim().isEmpty()) {
			return "Hello, my friend";
		}
		
		input = input.trim();
		
		if (input.contains(",")) {
            return plusieursNoms(input.split(","));
        }
		
		if (input.toUpperCase().equals(input)) {
			return nomPropreMaj(input);
		}
		
        return nomPropre(input);
    }
	
	private String nomPropre(String input) {
		
		StringBuilder chaine = new StringBuilder();
		chaine.append("Hello, ");
    	chaine.append(input.substring(0, 1).toUpperCase());
    	chaine.append(input.substring(1));
	    
	    return chaine.toString();
    }
	
	private String nomPropreMaj(String input) {
		
		StringBuilder chaine = new StringBuilder();
		chaine.append("HELLO, ");
    	chaine.append(input);
   		chaine.append(" !");
	    
	    return chaine.toString();
    }
	
	private String plusieursNoms(String[] noms) {
		StringBuilder chaine = new StringBuilder();
		chaine.append("Hello");
		for (String nom : noms) {
			chaine.append(", ");
			nom = nom.trim();
			chaine.append(nom.substring(0, 1).toUpperCase());
	    	chaine.append(nom.substring(1));
	    }
		
		return chaine.toString();
	}
	
}

## welcomeTest.java : 

package ilu2;

import static org.junit.jupiter.api.Assertions.*;

import org.junit.jupiter.api.BeforeEach;
import org.junit.jupiter.api.Test;

class WelcomeTest {
	
	Welcome welcome;
	
	@BeforeEach
	void init() {
        welcome = new Welcome();
	}
	

	@Test
	void testIter1() {
        assertEquals("Hello, Bob", welcome.welcome("bob"));
        assertNotEquals("Hello, bob", welcome.welcome("bob"));
        assertNotEquals("Hello, BOB", welcome.welcome("bob"));

    }
	
	@Test
	void testIter2() {
        assertEquals("HELLO, JERRY !", welcome.welcome("JERRY"));
        assertNotEquals("Hello, JERRY !", welcome.welcome("JERRY"));
        assertNotEquals("HELLO, Jerry !", welcome.welcome("JERRY"));
        assertNotEquals("HELLO, JERRY", welcome.welcome("JERRY"));
    }
	
	@Test
	void testIter3() {
        assertEquals("Hello, my friend", welcome.welcome(""));
        assertEquals("Hello, my friend", welcome.welcome(null));
        assertEquals("Hello, my friend", welcome.welcome("      "));
    }
	
	@Test
	void testIter4() {
        assertEquals("Hello, Bob", welcome.welcome("bob     "));
        assertEquals("Hello, Bob", welcome.welcome("    bob"));
        assertNotEquals("Hello,  Bob ", welcome.welcome(" bob "));
	}
	
	@Test
	void testIter5() {
        assertEquals("Hello, Amy, Bob", welcome.welcome("amy,bob"));
        assertNotEquals("Hello, Amy", welcome.welcome("amy,bob"));
        assertNotEquals("Hello, Bob", welcome.welcome("amy,bob"));
	}
	
	@Test
	void testIter6() {
        assertEquals("Hello, Amy, Bob, Jerry", welcome.welcome("amy, bob,jerry"));
        assertNotEquals("Hello, Amy", welcome.welcome("amy, bob,jerry"));
        assertNotEquals("Hello, Bob", welcome.welcome("amy, bob,jerry"));
        assertNotEquals("Hello, Jerry", welcome.welcome("amy, bob,jerry"));
	}
	
	

}


## commandes git : 

git add . 
git commit -m "ITER6"


########### ITER7 ##############

## welcome.java :

package ilu2;

public class Welcome {
	
	public String welcome(String input) {
		if (input == null || input.trim().isEmpty()) {
			return "Hello, my friend";
		}
		
		input = input.trim();
		
		if (input.contains(",")) {
            return plusieursNoms(input.split(","));
        }
		
		if (input.toUpperCase().equals(input)) {
			return nomPropreMaj(input);
		}
		
        return nomPropre(input);
    }
	
	private String nomPropre(String input) {
		
		StringBuilder chaine = new StringBuilder();
		chaine.append("Hello, ");
    	chaine.append(input.substring(0, 1).toUpperCase());
    	chaine.append(input.substring(1));
	    
	    return chaine.toString();
    }
	
	private String nomPropreMaj(String input) {
		
		StringBuilder chaine = new StringBuilder();
		chaine.append("HELLO, ");
    	chaine.append(input);
   		chaine.append(" !");
	    
	    return chaine.toString();
    }
	
	private String plusieursNoms(String[] noms) {
		StringBuilder chaine = new StringBuilder();
		int nombreNomsMin = compterNombreNomsMinMaj(noms)[0];
		String[] nomsMin = new String[nombreNomsMin];
	    int nombreNomsMaj = compterNombreNomsMinMaj(noms)[1];
		String[] nomsMaj = new String[nombreNomsMaj];
		int indMin = 0;
		int indMaj = 0;
	    for (String nom : noms) {
	    	if (nom.equals(nom.toUpperCase())) {
	    		nomsMaj[indMaj] = nom;
	    		indMaj += 1;
	        } else {
	        	nomsMin[indMin] = nom;
	    		indMin += 1;
	        }
	    }
	    if (nomsMin.length > 0) {
	    	chaine.append(plusieursNomsMinus(nomsMin));
		}
		if (nomsMaj.length > 0) {
	    	chaine.append(plusieursNomsMaj(nomsMaj));
		}
		return chaine.toString();
	}
	
	private int[] compterNombreNomsMinMaj(String[] noms) {
		int[] tuple = {0, 0};
	    
	    for (String nom : noms) {
	    	if (nom.equals(nom.toUpperCase())) {
	    		tuple[1] += 1;
	        } else {
	        	tuple[0] += 1;
	        }
	    }
	    
	    return tuple;
	}
	
	private String plusieursNomsMinus(String[] nomsMin) {
		StringBuilder chaine = new StringBuilder();
		chaine.append("Hello");

		for (String nom : nomsMin) {
			if (nom != null) {
				chaine.append(", ");
				nom = nom.trim();
				chaine.append(nom.substring(0, 1).toUpperCase());
		    	chaine.append(nom.substring(1));
			}
	    } 
		
		return chaine.toString();
	}
	
	private String plusieursNomsMaj(String[] nomsMaj) {
		StringBuilder chaine = new StringBuilder();
		chaine.append(". AND HELLO");

		for (String nom : nomsMaj) {
			if (nom != null && !nom.trim().isEmpty()) {
				chaine.append(", ");
				nom = nom.trim();
				chaine.append(nom.toUpperCase());
			}
	    }
		
    	chaine.append(" !");

		return chaine.toString();
	}
	
}

## welcomeTest.java : 

package ilu2;

import static org.junit.jupiter.api.Assertions.*;

import org.junit.jupiter.api.BeforeEach;
import org.junit.jupiter.api.Test;

class WelcomeTest {
	
	Welcome welcome;
	
	@BeforeEach
	void init() {
        welcome = new Welcome();
	}
	

	@Test
	void testIter1() {
        assertEquals("Hello, Bob", welcome.welcome("bob"));
        assertNotEquals("Hello, bob", welcome.welcome("bob"));
        assertNotEquals("Hello, BOB", welcome.welcome("bob"));

    }
	
	@Test
	void testIter2() {
        assertEquals("HELLO, JERRY !", welcome.welcome("JERRY"));
        assertNotEquals("Hello, JERRY !", welcome.welcome("JERRY"));
        assertNotEquals("HELLO, Jerry !", welcome.welcome("JERRY"));
        assertNotEquals("HELLO, JERRY", welcome.welcome("JERRY"));
    }
	
	@Test
	void testIter3() {
        assertEquals("Hello, my friend", welcome.welcome(""));
        assertEquals("Hello, my friend", welcome.welcome(null));
        assertEquals("Hello, my friend", welcome.welcome("      "));
    }
	
	@Test
	void testIter4() {
        assertEquals("Hello, Bob", welcome.welcome("bob     "));
        assertEquals("Hello, Bob", welcome.welcome("    bob"));
        assertNotEquals("Hello,  Bob ", welcome.welcome(" bob "));
	}
	
	@Test
	void testIter5() {
        assertEquals("Hello, Amy, Bob", welcome.welcome("amy,bob"));
        assertNotEquals("Hello, Amy", welcome.welcome("amy,bob"));
        assertNotEquals("Hello, Bob", welcome.welcome("amy,bob"));
	}
	
	@Test
	void testIter6() {
        assertEquals("Hello, Amy, Bob, Jerry", welcome.welcome("amy, bob,jerry"));
        assertNotEquals("Hello, Amy", welcome.welcome("amy, bob,jerry"));
        assertNotEquals("Hello, Bob", welcome.welcome("amy, bob,jerry"));
        assertNotEquals("Hello, Jerry", welcome.welcome("amy, bob,jerry"));
	}
	
	@Test
	void testIter7() {
        assertEquals("Hello, Amy, Jerry. AND HELLO, BOB !", welcome.welcome("amy, BOB, jerry"));
        assertNotEquals("Hello, Amy, Bob, Jerry", welcome.welcome("amy, BOB, jerry"));
	}
	

}


## commandes git : 

git add . 
git commit -m "ITER_7"


########### ITER8 ##############

## welcome.java :

package ilu2;

public class Welcome {
	
	public String welcome(String input) {
		if (input == null || input.trim().isEmpty()) {
			return "Hello, my friend";
		}
		
		input = input.trim();
		
		if (input.contains(",")) {
            return plusieursNoms(input.split(","));
        }
		
		if (input.toUpperCase().equals(input)) {
			return nomPropreMaj(input);
		}
		
        return nomPropre(input);
    }
	
	private String nomPropre(String input) {
		
		StringBuilder chaine = new StringBuilder();
		chaine.append("Hello, ");
    	chaine.append(input.substring(0, 1).toUpperCase());
    	chaine.append(input.substring(1));
	    
	    return chaine.toString();
    }
	
	private String nomPropreMaj(String input) {
		
		StringBuilder chaine = new StringBuilder();
		chaine.append("HELLO, ");
    	chaine.append(input);
   		chaine.append(" !");
	    
	    return chaine.toString();
    }
	
	private String plusieursNoms(String[] noms) {
		StringBuilder chaine = new StringBuilder();
		int nombreNomsMin = compterNombreNomsMinMaj(noms)[0];
		String[] nomsMin = new String[nombreNomsMin];
	    int nombreNomsMaj = compterNombreNomsMinMaj(noms)[1];
		String[] nomsMaj = new String[nombreNomsMaj];
		int indMin = 0;
		int indMaj = 0;
	    for (String nom : noms) {
	    	if (nom.equals(nom.toUpperCase())) {
	    		nomsMaj[indMaj] = nom;
	    		indMaj += 1;
	        } else {
	        	nomsMin[indMin] = nom;
	    		indMin += 1;
	        }
	    }
	    if (nomsMin.length > 0) {
	    	chaine.append(plusieursNomsMinus(nomsMin));
		}
		if (nomsMaj.length > 0) {
	    	chaine.append(plusieursNomsMaj(nomsMaj));
		}
		return chaine.toString();
	}
	
	private int[] compterNombreNomsMinMaj(String[] noms) {
		int[] tuple = {0, 0};
	    
	    for (String nom : noms) {
	    	if (nom.equals(nom.toUpperCase())) {
	    		tuple[1] += 1;
	        } else {
	        	tuple[0] += 1;
	        }
	    }
	    
	    return tuple;
	}
	
	private String plusieursNomsMinus(String[] nomsMin) {
		StringBuilder chaine = new StringBuilder();
		chaine.append("Hello");

		for (int i = 0; i < nomsMin.length; i++) {
	        if (nomsMin[i] != null) {
	        	if (i == nomsMin.length - 1) {
	                chaine.append(" and ");
	            } else {
	            	chaine.append(", ");
	            }   
	        	nomsMin[i] = nomsMin[i].trim();
	            chaine.append(nomsMin[i].substring(0, 1).toUpperCase());
	            chaine.append(nomsMin[i].substring(1));
	        }
	    }
		
		return chaine.toString();
	}
	
	private String plusieursNomsMaj(String[] nomsMaj) {
		StringBuilder chaine = new StringBuilder();
		chaine.append(". AND HELLO");
		
		for (int i = 0; i < nomsMaj.length; i++) {
			if (nomsMaj[i] != null) {
				if (i == nomsMaj.length - 1) {
	                chaine.append(" AND ");
	            } else {
	            	chaine.append(", ");
	            } 
				nomsMaj[i] = nomsMaj[i].trim();
				chaine.append(nomsMaj[i].toUpperCase());
			}
	    }
		
    	chaine.append(" !");

		return chaine.toString();
	}
	
}

## welcomeTest.java : 

package ilu2;

import static org.junit.jupiter.api.Assertions.*;

import org.junit.jupiter.api.BeforeEach;
import org.junit.jupiter.api.Test;

class WelcomeTest {
	
	Welcome welcome;
	
	@BeforeEach
	void init() {
        welcome = new Welcome();
	}
	

	@Test
	void testIter1() {
        assertEquals("Hello, Bob", welcome.welcome("bob"));
        assertNotEquals("Hello, bob", welcome.welcome("bob"));
        assertNotEquals("Hello, BOB", welcome.welcome("bob"));

    }
	
	@Test
	void testIter2() {
        assertEquals("HELLO, JERRY !", welcome.welcome("JERRY"));
        assertNotEquals("Hello, JERRY !", welcome.welcome("JERRY"));
        assertNotEquals("HELLO, Jerry !", welcome.welcome("JERRY"));
        assertNotEquals("HELLO, JERRY", welcome.welcome("JERRY"));
    }
	
	@Test
	void testIter3() {
        assertEquals("Hello, my friend", welcome.welcome(""));
        assertEquals("Hello, my friend", welcome.welcome(null));
        assertEquals("Hello, my friend", welcome.welcome("      "));
    }
	
	@Test
	void testIter4() {
        assertEquals("Hello, Bob", welcome.welcome("bob     "));
        assertEquals("Hello, Bob", welcome.welcome("    bob"));
        assertNotEquals("Hello,  Bob ", welcome.welcome(" bob "));
	}
	
	@Test
	void testIter5() {
        assertEquals("Hello, Amy, Bob", welcome.welcome("amy,bob"));
        assertNotEquals("Hello, Amy", welcome.welcome("amy,bob"));
        assertNotEquals("Hello, Bob", welcome.welcome("amy,bob"));
	}
	
	@Test
	void testIter6() {
        assertEquals("Hello, Amy, Bob, Jerry", welcome.welcome("amy, bob,jerry"));
        assertNotEquals("Hello, Amy", welcome.welcome("amy, bob,jerry"));
        assertNotEquals("Hello, Bob", welcome.welcome("amy, bob,jerry"));
        assertNotEquals("Hello, Jerry", welcome.welcome("amy, bob,jerry"));
	}
	
	@Test
	void testIter7() {
        assertEquals("Hello, Amy, Jerry. AND HELLO, BOB !", welcome.welcome("amy, BOB, jerry"));
        assertNotEquals("Hello, Amy, Bob, Jerry", welcome.welcome("amy, BOB, jerry"));
	}
	
	@Test
	void testIter8() {
        assertEquals("Hello, Bob, Amy and Jerry", welcome.welcome("bob, amy, jerry"));
        assertEquals("Hello, Bob and Jerry. AND HELLO, AMY AND JACK !", welcome.welcome("bob, AMY, jerry, JACK"));
	}
	

}


## commandes git : 

git add . 
git commit -m "ITER_8"


########### ITER9 ##############

## welcome.java :



## welcomeTest.java : 



## commandes git : 

git add . 
git commit -m "ITER_9"


########### ITER10 ##############

## welcome.java :



## welcomeTest.java : 



## commandes git : 

git add . 
git commit -m "ITER_10"

## une fois tout finis 

git add . 
git commit -m "Finish"
git tag v1.0.0 && git push origin v1.0.0


































































