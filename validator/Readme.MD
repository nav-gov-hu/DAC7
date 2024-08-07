# DAC7 Validator

A DAC7Validátor egy C#-ban készült keret program, amely segítségével a felhasználó ellenőrizheti az általa elkészített DPI_HU XML állományokat.

# Funkcionalitás
- XSD validáció az alábbi XSD-re: <br />
-- DPIXML_20231019.xsd <br />
import  oecddpitypes_v1.0.xsd <br />
import isodpitypes_v1.0.xsd <br />
- Logolás állományba

## Futtatás ,Telepítés

A program legalább Windows 10-es operációs rendszeren fut.
A program az Online Invoice Tool plugin binárisát használja a validációhoz, amely egy exe-be csomagolt java program. A program futtatásához Java 1.8-as verzió szükséges. 
Bővebb információ itt található:
[Dokumentációk | Online számla (gov.hu)](https://onlineszamla.nav.gov.hu/dokumentaciok) <br />
[Grafikus segédprogram leírás (22. Fejezet Konzolos segédprogram) | Online számla (gov.hu)](https://onlineszamla.nav.gov.hu/api/files/container/download/Online%20Sz%C3%A1mla_fejleszt%C3%A9si_seg%C3%A9deszk%C3%B6z_GUI_v2.0.pdf) 

**Futtatás**
1.) A zip állomány tartalmát csomagolja ki egy könyvtárba <br />
2.) Futtassa a Dac7Tester.exe-t <br />
3.) A DPI XML path inputbox-ba adja meg az ellenőrizendő XML elérési útját vagy tallózza ki. <br />
4.) Kattintson a Valide gombra <br />
5.) Olvassa el a megjelenő üzenetet. <br />

**Parancssori futtatás**
A program felületén már előre meg vannak adva a input adatok kivéve az XML elérési útját. Ezek az adatok azonban tetszőlegesen módosíthatók.
Az XSD validáció parancssorból is meghívható az alábbiak szerint, amennyiben az állományokat a c:\DAC7validator mappába csomagolta ki

**c:\DAC7validator\OnlineInvoiceTool_v1.1.exe -xmlvalidate -xmlfile=C:\Temp\dac7\hibas.xml -xsdfile=DPIXML_20231019.xsd**
