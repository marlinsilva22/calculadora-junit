# calculadora-junit

import static org.junit.jupiter.api.Assertions.*;
import org.junit.jupiter.api.Test;

public class CalculadoraTeste {

    Calculadora calc = new Calculadora();

    @Test
    public void testSomar() {
        assertEquals(15, calc.somar(10, 5));
    }

    @Test
    public void testSubtrair() {
        assertEquals(5, calc.subtrair(10, 5));
    }

    @Test
    public void testMultiplicar() {
        assertEquals(50, calc.multiplicar(10, 5));
    }

    @Test
    public void testDividir() {
        assertEquals(2, calc.dividir(10, 5));
    }

    @Test
    public void testDividirPorZero() {
        assertThrows(ArithmeticException.class, () -> calc.dividir(10, 0));
    }

    @Test
    public void testPotenciar() {
        assertEquals(8, calc.potenciar(2, 3));
    }
}
