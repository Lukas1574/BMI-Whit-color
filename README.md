#__________________________________________________________________________________________________________________#

from colorama import Fore, Style, init
init()

#__________________________________________________________________________________________________________________#

# BMI Informations Eingaben #

gewicht = float(input("Geben Sie Ihr Gewicht in kg ein: "))
groesse = float(input("Geben Sie Ihre Größe in Metern ein: "))
bmi = gewicht / (groesse ** 2)

#__________________________________________________________________________________________________________________#

# BMI Ausgabe #

if bmi < 16.5:
    print(f"{Fore.BLUE}Dein BMI beträgt {bmi:.1f}. Damit bist du stark untergewichtig.{Style.RESET_ALL}")
    print(f"{Fore.YELLOW}Wir Empfhelen dir Ausreichende Kalorienzufuhr und regelmäßige Mahlzeiten")
elif bmi < 18.5:
    print(f"{Fore.CYAN}Dein BMI beträgt {bmi:.1f}. Damit bist du untergewichtig.{Style.RESET_ALL}")
    print(f"{Fore.YELLOW}Wir Empfhelen dir Ausreichende Kalorienzufuhr und regelmäßige Mahlzeiten")
elif bmi < 25:
    print(f"{Fore.GREEN}Dein BMI beträgt {bmi:.1f}. Damit liegst du im Normalgewicht.{Style.RESET_ALL}")
    print(f"{Fore.YELLOW}Wir Empfhelen dir dein Gewicht zuhalten und ausgewogene Ernährung")
elif bmi < 30:
    print(f"{Fore.YELLOW}Dein BMI beträgt {bmi:.1f}. Damit hast du Übergewicht.{Style.RESET_ALL}")
    print(f"{Fore.YELLOW}Wir Empfhelen dir Kalorienreduzierte Ernährung und mehr Bewegung")
else:
    print(f"{Fore.RED}Dein BMI beträgt {bmi:.1f}. Damit leidest du an Adipositas.{Style.RESET_ALL}")
    print(f"{Fore.YELLOW}Wir Empfhelen dir einen Arztbesuch für professionelle Unterstützung")
    
#__________________________________________________________________________________________________________________#

ideal = 21.7 * (groesse ** 2) 

print(f"{Fore.YELLOW}Dein Ideal Gewicht beträgt {Fore.GREEN}{ideal:.2f} Kg {Style.RESET_ALL}")

#__________________________________________________________________________________________________________________#


if gewicht > ideal:
    differenz = gewicht - ideal
    print(f"{Fore.RED}Du solltest ca. {differenz:.2f} kg abnehmen.")
elif gewicht < ideal:
    differenz = ideal - gewicht
    print(f"{Fore.BLUE}Du solltest ca. {differenz:.2f} kg zunehmen.")
else:
    print(f"{Fore.GREEN}Du hast genau dein Idealgewicht erreicht!")
    
#__________________________________________________________________________________________________________________#
