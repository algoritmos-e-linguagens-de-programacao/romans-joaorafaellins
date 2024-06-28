[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/RfGTOLZs)


Repositório para os exercícios aplicados nas disciplinas relacionadas a programação.
def int_to_roman(num):
    # Mapeamento de números inteiros para numerais romanos
    val = [
        1000, 900, 500, 400,
        100, 90, 50, 40,
        10, 9, 5, 4,
        1
    ]
    syms = [
        "M", "CM", "D", "CD",
        "C", "XC", "L", "XL",
        "X", "IX", "V", "IV",
        "I"
    ]
    
    roman_numeral = ""
    i = 0
    
    while num > 0:
        for _ in range(num // val[i]):
            roman_numeral += syms[i]
            num -= val[i]
        i += 1
        
    return roman_numeral


def convert_and_print_up_to_3000():
    for num in range(1, 3001):
        print(f"{num}: {int_to_roman(num)}")


convert_and_print_up_to_3000()
