import unittest
from calculator import add, subtract, multiply, divide

class TestAdvancedCalculator(unittest.TestCase):

    def test_addition_logic(self):
        """Проверка корректности операции сложения чисел."""
        self.assertEqual(add(10, 5), 15)
        self.assertEqual(add(-1, 1), 0)

    def test_subtraction_logic(self):
        """Проверка корректности операции вычитания чисел."""
        self.assertEqual(subtract(10, 5), 5)
        self.assertEqual(subtract(0, 5), -5)

    def test_multiplication_logic(self):
        """Проверка корректности операции умножения чисел."""
        self.assertEqual(multiply(10, 5), 50)
        self.assertEqual(multiply(-2, 3), -6)

    def test_division_logic(self):
        """Проверка корректности операции деления и вызова исключений."""
        self.assertEqual(divide(10, 2), 5)
        with self.assertRaises(ValueError):
            divide(10, 0)

if __name__ == "__main__":
    unittest.main()
