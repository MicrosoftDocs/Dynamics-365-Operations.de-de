---
title: Intrastat (Polen)
description: Dieser Artikel enthält Informationen zur Intrastat-Meldung in Polen.
author: AdamTrukawka
ms.date: 11/09/2021
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: ''
ms.openlocfilehash: 473581fa4f3f1e8cac06d5748f28116e6615215e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281641"
---
# <a name="polish-intrastat"></a>Intrastat (Polen)

[!include[banner](../includes/banner.md)]

Die **Intrastaz** Seite wird verwendet, um Informationen zum Handel zwischen EU-Ländern/Regionen generieren und melden. Die polnische Intrastat-Meldung enthält Informationen über die Inzahlungnahme von Waren zur Meldung.

Die folgenden Felder sind in der polnischen Intrastat-Meldung enthalten. Alle Felder sind bei Wareneingängen und beim Versand enthalten, außer **RodzajTransportu** (der Transportmodus) und **KrajPochodzenia** (das Herkunftsland oder die Herkunftsregion), die beim Versand nicht enthalten sind, und **IdKontrahenta** (die ausländische Umsatzsteuer-Identifikationsnummer des Kunden), die beim Wareneingang nicht enthalten ist.

| Feldname | Description |
|-------------------------|-------------------------|
| Deklaracja Data | Das Erstellungsdatum des Dokuments. |
| Miesiac | Der Referenzmonat der Erklärung. |
| Rok | Das Referenzjahr der Erklärung. |
| Numer | Die Nummer der Meldung im Referenzzeitraum. |
| Wersja | Die Versionsnummer der Erklärung. |
| NrWlasny | Der Bezeichner der Erklärung. Der Wert wird automatisch generiert. |
| Typ | Die Berichtsrichtung.</br><li>Bei Wareneingängen wird „P“ gedruckt.</li><li>Beim Versand wird „W“ gedruckt.</li> |
| Rodzaj | Der Typ der Erklärung. Der Wert gibt an, ob es sich bei der Meldung um die Originalmeldung oder eine korrigierende Meldung handelt. |
| UC | Der Einheitencode, an den die Intrastat-Meldung adressiert ist. Der Wert ist im Feld **Steuerbefreiungsnummer** im Abschnitt **Mehrwertsteuer** der Registerkarte **Agent** auf der Seite **Außenhandelsparameter** angegeben. |
| Nazwa | Der Name des Unternehmens. |
| Miejscowosc, UlicaNumer, KodPocztowy | Die vollständige Adresse der juristischen Person. |
| Nip | Die polnische Steuernummer (Umsatzsteuer-ID, USt-IdNr.). |
| Regon | Die polnische statistische Identifikationsnummer (Unternehmensnummer). |
| LacznaWartoscFaktur | Die Summe der Rechnungswerte. |
| LacznaWartoscStatystyczna | Die Summe der statistischen Werte. |
| LacznaLiczbaPozycji | Die Gesamtzahl der Waren oder Artikel. |
| PozId | Die fortlaufende Nummer eines bestimmten Artikels. |
| OpisTowaru | Der Handelsname der Ware. |
| KrajPochodzeniaWysylki | Code für das Land oder die Region der Gegenpartei, der von der International Organisation für Normung (ISO) verwendet wird. |
| WarunkiDostawy | Der Intrastat-Code für die Lieferbedingungen. |
| RodzajTransakcji | Der Code, der die Art der Transaktion angibt. Polnische Unternehmen verwenden zweistellige Transaktionscodes. |
| KodTowarowy | Der achtstellige Warencode gemäß der kombinierten Nomenklatur. |
| RodzajTransportu | Der Intrastat-Code für den Transportmodus. |
| KrajPochodzenia | Der ISO-Code für das Land oder die Region, in dem die Waren produziert oder hergestellt wurden. |
| MasaNetto | Die Nettomasse in vollen Kilogramm. |
| IloscUzupelniajacaJm | Die Menge in der zusätzlichen Maßeinheit in ganzen Zahlen. |
| WartoscFaktury | Der Rechnungswert aller Transaktionen, die von einem Artikel abgedeckt werden. |
| WartoscStatystyczna | Der statistische Wert. |
| Wypelniajacy: NazwiskoImie, Telefon, Faks, Email | Vor- und Nachname, Telefonnummer, Faxnummer und E-Mail-Adresse der Person, die die Erklärung abgibt. |
| IdKontrahenta | Die ausländische Mehrwertsteuernummer des Kunden in einem EU-Mitgliedstaat. |


## <a name="set-up-intrastat"></a>Einrichten von Intrastat

Importieren Sie vom globalen Repository aus die neueste Version der folgenden Konfigurationen für die elektronische Berichterstellung (EB).

   - Intrastat-Modell
   - Intrastat-Bericht
   - Intrastat (PL)

Weitere Informationen finden Sie unter [Herunterladen von ER-Konfigurationen aus dem Global Repository des Konfigurationsdienstes](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md).

## <a name="set-up-a-vat-id-and-an-enterprise-number-for-your-company"></a>Eine USt-IdNr. und eine Unternehmensnummer für Ihr Unternehmen einrichten

### <a name="create-registration-types-for-company-codes"></a>Registrierungsarten für Unternehmenscodes erstellen

Für Unternehmenscodes müssen Sie zwei Registrierungsarten anlegen: eine für die USt-IdNr. (NIP-Code) und eine für die Unternehmensnummer (Regon-Code).

1. Navigieren Sie zur **Organisationsverwaltung** > **Globales Adressbuch** > **Registrierungstypen** > **Registrierungstypen**.
2. Wählen Sie im Aktivitätsbereich die Option **Neu** aus, um einen Registrierungstyp für die USt-IdNr. zu erstellen.
3. Geben Sie im Dialogfeld **Details zu Registrierungstypen eingeben** im Feld **Name** einen Namen für den neuen Registrierungstyp ein. Geben Sie beispielsweise **NIP** ein.
4. Wählen Sie im Feld **Land/Region** **POL** aus.
5. Wählen Sie **Erstellen** aus.
6. Wählen Sie im Aktivitätsbereich die Option **Neu** aus, um einen Registrierungstyp für die Unternehmensnummer zu erstellen.
7. Geben Sie im Dialogfeld **Details zu Registrierungstypen eingeben** im Feld **Name** einen Namen für den neuen Registrierungstyp ein. Geben Sie beispielsweise **Regon** ein.
8. Wählen Sie im Feld **Land/Region** **POL** aus.
9. Wählen Sie **Erstellen** aus.

### <a name="match-the-registration-types-with-registration-categories"></a>Die Registrierungstypen den Registrierungskategorien zuordnen

1. Navigieren Sie zu **Organisationsverwaltung** > **Globales Adressbuch** > **Registrierungstypen** > **Registrierungskategorien**.
2. Wählen Sie im Aktivitätsbereich **Neu** aus, um eine Verknüpfung zwischen den einzelnen von Ihnen erstellten Registrierungstypen und einer Registrierungskategorie zu erstellen.

    - Wählen Sie für den Registrierungstyp für die USt-IdNr. (NIP-Code) die Registrierungskategorie **USt-IdNr.**.
    - Wählen Sie für den Registrierungstyp für die Unternehmensnummer (Regon-Code) die Registrierungskategorie **Enterprise-ID (COID)** aus.

### <a name="set-up-a-vat-id-and-an-enterprise-number-for-your-company"></a>Eine USt-IdNr. und eine Unternehmensnummer für Ihr Unternehmen einrichten

1. Gehen Sie zu **Organisationsverwaltung** > **Organisationen** > **Juristische Personen**.
2. Wählen Sie im Raster Ihr Unternehmen aus.
3. Wählen Sie im Aktivitätsbereich **Registrierungs-ID** aus.
4. Wählen Sie im Inforegister **Registrierungskennung** die Option **Hinzufügen** aus.
5. Wählen Sie im Feld **Registrierungstyp** einen der Registrierungstypen aus, die Sie vorher erstellt haben.
6. Geben Sie die USt-IdNr. (NIP-Code) oder die Unternehmensnummer (Regon-Code) Ihres Unternehmens ein, je nachdem, welchen Registrierungstyp Sie im vorherigen Schritt ausgewählt haben.
7. Wiederholen Sie die Schritte 4 bis 6 für den anderen Registrierungstyp, den Sie zuvor erstellt haben.

## <a name="set-up-a-company-address"></a>Unternehmensadresse einrichten

1. Gehen Sie zu **Organisationsverwaltung** > **Organisationen** > **Juristische Personen**.
2. Wählen Sie im Raster Ihr Unternehmen aus.
3. Wählen Sie auf der Registerkarte **Adressen** die Option **Bearbeiten** aus.
4. Wählen Sie im Dialogfeld **Adresse bearbeiten** unter **Postleitzahl** die Postleitzahl Ihres Unternehmens aus.
5. Geben Sie im Feld **Straße** Ihre Adresse ein.
6. Wählen Sie im Feld **Stadt** Ihre Stadt aus.

## <a name="set-up-foreign-trade-parameters"></a>Außenhandelsparameter einrichten

1. Wechseln Sie zu **Steuer** > **Einstellungen** > **Außenhandelsparameter**.
2. Wählen Sie auf der Registerkarte **Intrastat** das Inforegister **Elektronische Berichterstellung** und dann im Feld **Dateiformatzuordnung** **Intrastat (PL)** aus.
3. Im Feld **Berichtformatzuordnung** **Intrastatbericht** auswählen.
4. Auf dem Inforegister **Warencodehierarchie** im Feld **Kategoriehierarchie** wählen Sie **Intrastat**.
5. Wählen Sie im Feld **Art des Geschäfts** die Art des Geschäfts für Eigentumsübertragungen aus. Sie verwenden diesen Code für Transaktionen, die tatsächliche oder geplante Eigentumsübertragungen gegen Vergütung (finanziell oder anderweitig) zur Folge haben. Sie verwenden ihn auch für Korrekturen. Unternehmen in Polen verwenden zweistellige Transaktionscodes.
6. Wählen Sie im Feld **Gutschrift** die Art des Geschäfts für die Warenrücksendung aus.
7. Auf der Registerkarte **Länder-/Regionseigenschaften** führen Sie im Feld **Land/Region** alle Länder oder Regionen auf, mit denen Ihre Unternehmen Geschäfte macht. Wählen Sie für jedes Land, das Teil der EU ist, im Feld **Länder-/Regionsart** die Option **EU**, damit das Land in Ihrem Intrastat-Bericht erscheint. Wählen Sie für Polen im Feld **Länder-/Regionsart** die Option **Inland** aus.
8. Wählen Sie auf der Registerkarte **Agent** das Inforegister **Agent**, den Abschnitt **Mehrwertsteuer**, das Feld **Steuerbefreiungsummer** aus und geben Sie **420000** ein, um den Einheitencode anzugeben, an den die Intrastat-Erklärung gerichtet ist.
9. Geben Sie in der Registerkarte **Kontakt** den Vor- und Nachnamen, die Telefonnummer, Faxnummer und E-Mail-Adresse der Person, die die Erklärung abgibt.
10. Geben Sie in der Registerkarte **Nummernkreis** im Feld **Nummernkreiscode** Feld einen nicht fortlaufenden Nummernkreis mit maximal neun Zeichen als Referenz für die **XML-Dateinummer** ein. Dieses Feld wird verwendet, um automatisch einen Wert für das Feld **Bezeichner der Erklärung** im Intrastat-Bericht zu generieren.

## <a name="set-up-product-parameters-for-the-intrastat-declaration"></a>Die Produktparameter für die Intrastat-Meldung festlegen

1. Wechseln Sie zu **Produktinformationsverwaltung** > **Produkte** > **Freigegebene Produkte** aus.
2. Wählen Sie im Raster ein Produkt aus.
3. Auf der Registerkarte **Außenhandel** Inforegister, im Abschnitt **Intrastat**, im Feld **Ware**, wählen Sie die Warennummer. Der Name der Ware wird im Feld **Beschreibung der Waren** im Intrastat-Bericht eingetragen.
4. Wählen Sie im Abschnitt **Ursprung** im Feld **Land/Region** das Ursprungsland oder die Ursprungsregion des Produkts aus.
5. Auf der Registerkarte **Lagerbestand verwalten** Inforegister, im Feld **Nettogewicht**, geben Sie das Gewicht des Produkts in Kilogramm ein.

## <a name="set-up-compression-of-intrastat"></a>Komprimierung von Intrastat einrichten

-   Gehen Sie zu **Steuer** > **Einstellungen** > **Außenhandel** > **Komprimierung von Intrastat** und wählen Sie die Felder aus, die verglichen werden sollen, wenn Intrastat-Informationen zusammengefasst werden. Wählen Sie für das polnische Intrastat die folgenden Felder aus:

    - Warencode
    - Art des Geschäftes
    - Herkunftsland/-region
    - Transport
    - Lieferbedingungen
    - Land/Region des Absenders
    - Land/Region
    - Berichtigung
    - Steuerbefreiungsnummer
    - Planungsrichtung
    - Rechnung

## <a name="set-up-the-transport-method-and-delivery-terms"></a>Die Transportmethode und Lieferbedingungen festlegen

1.  Legen Sie Transportcodes fest.

    1. Gehen Sie zu **Steuer** > **Einrichtung** > **Außenhandel** > **Transportmethode**.
    2. Wählen Sie im Aktivitätsbereich **Neu** aus.
    3. Geben Sie im Feld **Transport** einen eindeutigen Wert ein. Polnische Unternehmen verwenden einstellige Transportcodes.

2.  Legen Sie Intrastat-Codes für die Lieferart fest.

    1. Gehen Sie zu **Beschaffung** > **Einstellungen** > **Vertrieb** > **Lieferbedingungen**.
    2. Wählen Sie im Raster Lieferbedingungen aus.
    3. Geben Sie auf dem Inforegister **Allgemein** im Feld **Intrastat-Code** den eindeutigen Code ein.

## <a name="intrastat-transfer"></a>Intrastat-Übertragung

Auf der Seite **Intrastat** im Aktivitätsbereich können Sie **Überweisen** auswählen, um die Informationen über den innergemeinschaftlichen Handel aus Ihren Verkaufsaufträgen, Freitextrechnungen, Bestellungen, Lieferantenrechnungen, Lieferantenprodukteingängen, Projektrechnungen und Transferaufträgen automatisch zu übertragen. Es werden nur Dokumente übermittelt, die ein EU-Land als Bestimmungsland oder -region bzw. Sendungsland oder -region haben.

Sie können Transaktionen auch manuell eingeben, indem Sie **Neu** im Aktionsbereich auswählen.

### <a name="generate-an-intrastat-report"></a>Generieren eines Intrastat-Berichts

1. Wechseln Sie zu **Steuer** > **Meldungen** > **Außenhandel** > **Intrastat**.
2. Wählen Sie im Aktivitätsbereich **Ausgabe** &gt; **Bericht**.
3. Im angezeigten Dialogfeld **Intrastat-Bericht** legen Sie die folgenden Felder fest.

    | Feld | Description |
    |-------------------------|-------------------------|
    | Startdatum | Wählen Sie das Startdatum für den Bericht. |
    | Datei generieren | Legen Sie diese Option auf **Ja** fest, um eine .xml-Datei für Ihren Intrastat-Bericht zu erzeugen. |
    | Dateiname | Geben Sie den Namen der .xml-Datei ein. |
    | Bericht generieren | Legen Sie diese Option auf **Ja** fest, um eine .xlsx-Datei für Ihren Intrastat-Bericht zu generieren. |
    | Berichtdateiname | Geben Sie den Namen der .xlsx-Datei ein. |
    | Planungsrichtung | **Eingang** für einen Bericht über die innergemeinschaftlichen Eingänge auswählen.</br>**Versand** für einen Bericht über innergemeinschaftliche Versendungen auswählen. |
    | Bezeichner der Erklärung | Die Dokument-ID wird automatisch generiert und kann aktualisiert werden. |
    | Meldungsart | Wählen Sie **Erklärung** für eine Originalerklärung aus.</br>Wählen Sie **Erklärungskorrektur – Ersatz** für eine korrigierte Erklärung, die eine bestehende, bereits eingereichte Original- oder korrigierte Erklärung vollständig ersetzen soll. |
    | Stadt der Dokumenterstellung | Geben Sie den Wert ein, der im Feld **Miejscowosc** der Intrastat-Meldung eingetragen werden soll. |
    | Datum der Dokumenterstellung | Geben Sie den Wert ein, der im Feld **Deklaracja Data** der Intrastat-Meldung eingetragen werden soll. |
    | Dokumentnr. | Geben Sie den Wert ein, der im Feld **Numer** der Intrastat-Meldung eingetragen werden soll. |
    | Belegversion | Geben Sie den Wert ein, der im Feld **Wersja** der Intrastat-Meldung eingetragen werden soll. |

4. Wählen Sie **OK**, und überprüfen Sie die generierten Berichte.

## <a name="example"></a>Beispiel

Dieses Beispiel zeigt, wie Sie Eingänge und Versendungen für Intrastat mithilfe der juristischen Person **DEMF** buchen.

### <a name="preliminary-setup"></a>Vorläufige Einstellungen

Importieren Sie die neueste Version der folgenden ER-Konfigurationen:

   - Intrastat-Modell
   - Intrastat-Bericht
   - Intrastat (PL)

### <a name="set-up-a-company-address"></a>Unternehmensadresse einrichten

1. Gehen Sie zu **Organisationsverwaltung** > **Globales Adressbuch** > **Adressen** > **Adresseinstellungen**.
2. Wählen Sie auf der Registerkarte **Stadt** **Neu** aus.
3. Wählen Sie im Feld **Land/Region** **POL** aus.
4. Geben Sie im Feld **Stadt** den Wert **Warschau (Warszawa)** ein.
5. Wählen Sie auf der Registerkarte **Postleitzahl** **Neu** aus.
6. Wählen Sie im Feld **Land/Region** **POL** aus.
7. Wählen Sie im Feld **Stadt** **Warschau (Warszawa)**.
8. Geben Sie im Feld **Postleitzahl** **00-844** ein.
9. Gehen Sie zu **Organisationsverwaltung** > **Organisation** > **Juristische Entitäten**, und wählen Sie die juristische Entität **DEMF**.
10. Wählen Sie auf der Inforegisterkarte **Adressen** die Option **Bearbeiten**.
11. Wählen Sie im Feld **Land/Region** **POL** aus.
12. Wählen Sie im Feld **Postleitzahl** **31-111** aus.
13. Geben Sie im Feld **Straße** **Statystyczna 22/1** ein.
14. Wählen Sie im Feld **Stadt** **Warschau (Warszawa)**.
15. Wählen Sie **OK** aus.

## <a name="set-up-a-vat-id-and-an-enterprise-number-code-for-your-company"></a>Eine USt-IdNr. und einen Unternehmensnummerncode für Ihr Unternehmen einrichten

### <a name="create-registration-types-for-company-codes"></a>Registrierungsarten für Unternehmenscodes erstellen

1. Navigieren Sie zur **Organisationsverwaltung** > **Globales Adressbuch** > **Registrierungstypen** > **Registrierungstypen**.
2. Wählen Sie im Aktivitätsbereich die Option **Neu** aus, um einen Registrierungstyp für die USt-IdNr. (NIP-Code) zu erstellen.
3. Geben Sie im Dialogfeld **Details zu Registrierungstypen eingeben** im Feld **Name** **NIP** ein.
4. Wählen Sie im Feld **Land/Region** **POL** aus.
5. Wählen Sie **Erstellen** aus.
6. Wählen Sie im Aktivitätsbereich die Option **Neu** aus, um einen Registrierungstyp für die Unternehmensnummer (Regon-Code) zu erstellen.
7. Geben Sie im Dialogfeld **Details zu Registrierungstypen eingeben** im Feld **Name** **Regon** ein.
8. Wählen Sie im Feld **Land/Region** **POL** aus.
9. Wählen Sie **Erstellen** aus.

### <a name="match-the-registration-types-with-registration-categories"></a>Die Registrierungstypen den Registrierungskategorien zuordnen

1. Navigieren Sie zu **Organisationsverwaltung** > **Globales Adressbuch** > **Registrierungstypen** > **Registrierungskategorien**.
2. Wählen Sie im Aktivitätsbereich **Neu** aus, um eine Verknüpfung zwischen den einzelnen von Ihnen erstellten Registrierungstypen und einer Registrierungskategorie zu erstellen.

    - Wählen Sie für den Registrierungstyp **NIP** die Registrierungskategorie **USt-IdNr.** aus.
    - Wählen Sie für den Registrierungstyp **Regon** die Registrierungskategorie **Enterprise-ID (COID)** aus.

### <a name="set-up-a-vat-id-and-an-enterprise-number-for-your-company"></a>Eine USt-IdNr. und eine Unternehmensnummer für Ihr Unternehmen einrichten

1. Gehen Sie zu **Organisationsverwaltung** > **Organisationen** > **Juristische Personen**.
2. Wählen Sie im Raster **DEMF** aus.
3. Wählen Sie im Aktivitätsbereich **Registrierungs-ID** aus.
4. Wählen Sie im Inforegister **Registrierungskennung** die Option **Hinzufügen** aus.
5. Wählen Sie im Feld **Registrierungstyp** **NIP** aus.
6. Geben Sie in das Feld **Registrierungsnummer** **1234567890** ein.
7. Wählen Sie **Hinzufügen** aus.
8. Wählen Sie im Feld **Registrierungstyp** **Regon** aus.
9. Geben Sie in das Feld **Registrierungsnummer** **12345678901234** ein.

### <a name="set-up-a-number-sequence-code"></a>Einrichten eines Nummernkreiscodes

1. Gehen Sie zu **Organisationsverwaltung** > **Nummernkreise** > **Nummernkreise**.
2. Wählen Sie im Aktivitätsbereich, auf der Registerkarte **Nummernkreis** in der Gruppe **Neu** die Option **Nummernkreis**.
3. Geben Sie im Inforegister **Kennung** im Feld **Nummernkreiscode** **XML\_Datei** ein.
4. Wählen Sie im Inforegister **Bereichsparameter** im Feld **Bereich** **Unternehmen** aus.
5. Wählen Sie im Feld **Unternehmen** **DEMF**.
6. Wählen Sie im Inforegister **Segmente** das Feld **Länge** und geben Sie dann im Segment **Alphanumerisch** **4** ein.
7. Auf der Registerkarte **Allgemein** Inforegister, im Abschnitt **Einrichtung**, legen Sie die Option **Kontinuierlich** auf **Nein** fest.
8. Geben Sie im Abschnitt **Nummerzuordnung** im Feld **Größte** **9999** ein.

### <a name="set-up-foreign-trade-parameters"></a>Außenhandelsparameter einrichten

1. Gehen Sie zu **Steuer** > **Einstellungen** > **Außenhandel** > **Außenhandelsparameter**.
2. Auf der Registerkarte **Intrastat** wählen Sie auf dem Inforegister **Allgemein** im Feld **Art** **des Geschäfts** **11** aus.
3. Wählen Sie auf der Registerkarte **Elektronisches Berichtswesen** Inforegister, im Feld **Dateiformatzuordnung**, **Intrastat (PL)**.
4. Wählen Sie im Feld **Berichtformatzuordnung** **Intrastatbericht** aus.
5. Stellen Sie sicher, dass Sie im Inforegister **Warencodehierarchie** im Feld **Kategoriehierarchie** **Intrastat** ausgewählt ist.
6. Wählen Sie auf der Registerkarte **Länder-/Regionseigenschaften** **Neu** aus.
7. Wählen Sie im Feld **Land/Region der Partei** **POL** aus. Wählen Sie dann im Feld **Land/Regionstyp** die Option **Inland**.
8. Wählen Sie im Feld **Land/Region der Partei** **DEU** aus. Wählen Sie dann im Feld **Länder-/Regionsart** die Option **EU** aus.
9. Wählen Sie in der Registerkarte **Agent** das Inforegister **Agent**, den Abschnitt **Mehrwertsteuer** und das Feld **Umsatzsteuernummer** aus. Geben Sie dort **420000** ein.
10. Geben Sie auf der Registerkarte **Kontakt** im Feld **Name** **Manish Chopra** ein.
11. Geben Sie im Feld **Telefon** den Wert **425-555-5068** ein.
12. Geben Sie im Feld **Faxnummer** den Wert **425-555-5049** ein.
13. Geben Sie im Feld **E-Mail** **manishc@contoso.com** ein.
14. Wählen Sie auf der Registerkarte **Nummernkreise** im Feld **Nummernkreiscode** für die Referenz **XML-Dateinummer** **XML\_Datei** aus.

### <a name="set-up-product-information"></a>Produktinformation festlegen

1. Gehen Sie zu **Produktinformationsverwaltung** > **Produkte** > **Freigegebene** **Produkte**.
2. Wählen Sie im Raster **D0001** aus.
3. Auf dem Inforegister **Außenhandel** wählen Sie im Abschnitt **Intrastat** im Feld **Ware** **100 200 30** aus.
4. Wählen Sie im Inforegister **Bestand verwalten** im Abschnitt **Gewichtsmessungen** im Feld **Nettogewicht** **2** ein.
5. Wählen Sie im Aktionsbereich **Speichern** aus.
6. Wählen Sie im Raster **D0003** aus.
7. Auf dem Inforegister **Außenhandel** wählen Sie im Abschnitt **Intrastat** im Feld **Ware** **100 200 30** aus.
8. Wählen Sie im Abschnitt **Herkunft** im Feld **Land/Region** **DEU** aus.
9. Wählen Sie im Inforegister **Bestand verwalten** im Abschnitt **Gewichtsmessungen** im Feld **Nettogewicht** **5** ein.
10. Wählen Sie im Aktionsbereich **Speichern** aus.

### <a name="change-the-site-address"></a>Ändern Sie die Standortadresse

1. Gehen Sie zu **Lagerortverwaltung** > **Einrichtung** > **Lager** > **Standorte**.
2. Wählen Sie im Raster **1** aus.
3. Wählen Sie auf der Inforegisterkarte **Adressen** die Option **Bearbeiten**.
4. Wählen Sie im Dialogfeld **Adresse bearbeiten** im Feld **Land/Region** die Option **POL**.
5. Wählen Sie **OK** aus.

### <a name="set-up-a-transport-method"></a>Eine Transportmethode festlegen

1. Erstellen Sie eine Transportmethode.

    1. Gehen Sie zu **Steuer** > **Einrichtung** > **Außenhandel** > **Transportmethode**.
    2. Wählen Sie im Aktivitätsbereich **Neu** aus.
    3. Geben Sie im Feld **Transport** den Wert **3** ein.
    4. Geben Sie im Feld **Beschreibung** **Straßentransport** ein.

2. Weisen Sie eine neue Transportmethode einer Lieferart zu. Auf diese Weise legen Sie die Standartwerte fest, die bei Auswahl der entsprechenden Lieferart für die Transportmethode verwendet werden.

    1. Gehen Sie zu **Beschaffung** > **Einstellungen** > **Vertrieb** > **Liefermodus**.
    2. Wählen Sie im Raster **10** aus.
    3. Wählen Sie auf dem Inforegister **Außenhandel** im Feld **Transport** die Option **3** aus.

3. Wählen Sie die Standardlieferart für einen Kunden aus.

    1. Gehen Sie zu **Debitoren** > **Kunden** > **Alle Kunden**.
    2. Wählen Sie im Raster **DE-016** aus.
    3. Wählen Sie im Inforegister **Rechnung und Lieferung** im Feld **Liefermodus** den Wert **10**.

4. Wählen Sie die Standardlieferart für einen Kreditor aus.

    1. Gehen Sie zu **Kreditorenkonten** > **Kreditoren** > **Alle Kreditoren** aus.
    2. Wählen Sie im Raster **DE-001** aus.
    3. Wählen Sie im Inforegister **Rechnung und Lieferung** im Feld **Liefermodus** den Wert **10**.

### <a name="set-up-codes-for-terms-of-delivery"></a>Die Codes für Lieferbedingungen festlegen

1. Richten Sie einen Intrastat-Code für die Lieferbedingungen ein.

    1. Gehen Sie zu **Beschaffung** > **Einstellungen** > **Vertrieb** > **Lieferbedingungen**.
    2. Wählen Sie im Raster **CIF** aus.
    3. Auf dem Inforegister **Allgemein** geben Sie im Feld **Intrastat-Code** **CIF** ein.

2. Wählen Sie die Standardlieferbedingungen für einen Kunden aus.

    1. Gehen Sie zu **Debitoren** > **Kunden** > **Alle Kunden**.
    2. Wählen Sie im Raster **DE-016** aus.
    3. Wählen Sie im Inforegister **Rechnung und Lieferung** im Feld **Lieferbedingungen** den Wert **CIF**.

3. Wählen Sie die Standardlieferbedingungen für einen Kreditor aus.

    1. Gehen Sie zu **Kreditorenkonten** > **Kreditoren** > **Alle Kreditoren** aus.
    2. Wählen Sie im Raster **DE-001** aus.
    3. Wählen Sie im Inforegister **Rechnung und Lieferung** im Feld **Lieferbedingungen** den Wert **CIF**.

### <a name="verify-an-eu-customers-tax-exempt-number-code"></a>Den Umsatzsteuernummer eines EU-Debitors bestätigen

1. Gehen Sie zu **Debitoren** > **Kunden** > **Alle Kunden**.
2. Wählen Sie im Raster **DE-016** aus.
3. Gehen Sie sicher, dass im **Rechnung und Lieferung**-Inforegister im Feld **Mehrwertsteuer** die **Umsatzsteuernummer** **DE9012** lautet.

### <a name="create-a-sales-order-with-an-eu-customer"></a>Erzeugen eines Verkaufsauftrags mit einem EU-Kunden

1. Gehen Sie zu **Debitoren** > **Aufträge** > **Alle Aufträge**.
2. Wählen Sie im Aktivitätsbereich **Neu** aus.
3. Wählen Sie im Dialogfeld **Auftrag erstellen** im Inforegister **Debitor** im Abschnitt **Debitor** im Feld **Debitorenkonto** **DE-016** aus.
4. Wählen Sie im Inforegister **Allgemein** im Abschnitt **Lagerdimensionen** im Feld **Standort** **1**.
5. Im Feld **Lagerort** wählen Sie **11** aus.
6. Gehen Sie sicher, dass in der Registerkarte **Adresse** das Feld **Adresse** **Teichgasse 12, Kiel, 24103, DEU** lautet, da der Kunde aus Deutschland kommt.
7. Wählen Sie **OK** aus.
8. Überprüfen Sie, ob auf der Registerkarte **Header** im Inforegister **Lieferung** das Feld **Lieferbedingungen** auf **CIF** und das Feld **Liefermodus** auf **10** gesetzt ist.
9. Wählen Sie auf der Registerkarte **Zeilen**, auf dem Inforegister **Kundenauftragszeilen**, im Feld **Positionsnummer**, **D0001**. Geben Sie dann im Feld **Menge** den Wert **8** ein.
10. Überprüfen Sie, ob im Inforegister **Positionsdetails** auf der Registerkarte **Außenhandel**, ob das Feld **Transaktionscode** auf **11**, das Feld **Ware** auf **100 200 30** und das Feld **Ursprungsland/-region** auf **POL** gesetzt sind.
11. Wählen Sie im Aktionsbereich **Speichern** aus.
12. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Rechnung** in der Gruppe **Generieren** **Rechnung** aus.
13. Im **Rechnung buchen** Dialogfeld, auf dem **Parameter** Inforegiser im **Parameter** Abschnitt, im **Menge** Feld, wählen Sie **Alle**.
14. Wählen Sie im Inforegister **Setup** im Feld **Verkaufsdatum** **18.10.2021** (18. Oktober 2021) aus.
15. Klicken Sie auf **OK**, um die Rechnung zu buchen.

### <a name="transfer-the-transaction-to-the-intrastat-journal-and-review-the-result"></a>Übertragen Sie die Transaktion in das Intrastat-Buch.-Blatt und überprüfen Sie das Ergebnis

1. Wechseln Sie zu **Steuer** > **Meldungen** > **Außenhandel** > **Intrastat**.
2. Wählen Sie im Aktivitätsbereich **Übertragung**.
3. Im **Intrastat (Übertragung)** Dialogfeld, im **Parameter** Abschnitt, legen Sie die **Kundenrechnung** Option auf **Ja** fest.
4. Wählen Sie **Filter** aus.
5. Wählen Sie im Dialogfeld **Intrastat-Filter** in der Registerkarte **Bereich** die erste Zeile aus und überprüfen Sie, ob das Feld **Feld** auf **Datum** gesetzt ist.
6. Wählen Sie im Feld **Kriterien** das aktuelle Datum aus.
7. Wählen Sie **OK** aus, um das Dialogfeld **Intrastat-Filter** zu schließen.
8. Wählen Sie **OK**, um das Dialogfeld **Intrastat (Übertragung)** zu schließen und überprüfen Sie das Ergebnis. Die Position stellt den Auftrag dar, den Sie früher erstellt haben.

    ![Position, die den Auftrag auf der Intrastat-Seite darstellt](media/intrastat_pl_1.png)

9. Wählen Sie die Transaktionsposition aus, und wählen Sie dann die Registerkarte **Allgemein**, um weitere Details anzuzeigen.

    ![Auftragsdetails auf der Registerkarte „Allgemein“ der Intrastat-Seite](media/intrastat_pl_2.png)

10. Wählen Sie im Aktivitätsbereich **Ausgabe** > **Bericht**.
11. Wählen Sie im Dialogfeld **Intrastat-Bericht**, das Inforegister **Parameter**, den Abschnitt **Datum**, das Feld **Von-Datum** aus und geben Sie den ersten Tag des derzeitigen Monats ein.
12. Im Abschnitt **Exportoptionen** legen Sie die Option **Generieren** auf **Ja** fest. Geben Sie dann im Feld **Dateiname** den gewünschten Namen ein.
13. Legen Sie die Option **Bericht generieren** auf **Ja** fest. Geben Sie dann in das Feld **Berichtsdateiname** den gewünschten Namen ein.
14. Wählen Sie im Feld **Richtung** die Option **Versand**.
15. Überprüfen Sie, ob im Abschnitt **Dateiformatzuordnung** das Feld **Meldungsart** auf **Erklärung** gesetzt ist.
16. Geben Sie im Feld **Stadt der Dokumenterstellung** **Krakau** ein.
17. Wählen Sie im Feld **Stadt der Dokumenterstellung** **19.10.2021** (19. Oktober 2021) aus.
18. Geben Sie im Feld **Dokumentnr.** **11** ein.
19. Geben Sie im Feld **Dokumentversion** **22** ein.
20. Wählen Sie **OK** und prüfen Sie den erzeugten Bericht im XML-Format. Die folgende Tabelle zeigt die Werte in dem Beispielbericht.

    <table>
    <tbody>
    <tr>
    <td>
    <p><strong>Feldname</strong></p>
    </td>
    <td>
    <p><strong>Feldbeschreibung</strong></p>
    </td>
    <td>
    <p><strong>Wert</strong></p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p><strong>Informationen über das Dokument</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Deklaracja Data</p>
    </td>
    <td>
    <p>Das Erstellungsdatum des Dokuments.</p>
    </td>
    <td>
    <p>19.10.2021</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Miejscowosc</p>
    </td>
    <td>
    <p>Die Stadt, in der das Dokument erstellt wurde.</p>
    </td>
    <td>
    <p>Krakau</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LacznaLiczbaPozycji</p>
    </td>
    <td>
    <p>Gesamtzahl der Artikel.</p>
    </td>
    <td>
    <p>1</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LacznaWartoscStatystyczna</p>
    </td>
    <td>
    <p>Der statistische Gesamtwert.</p>
    </td>
    <td>
    <p>2632</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LacznaWartoscFaktur</p>
    </td>
    <td>
    <p>Der Gesamtwert der Rechnung.</p>
    </td>
    <td>
    <p>2632</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>UC</p>
    </td>
    <td>
    <p>Der Einheitencode.</p>
    </td>
    <td>
    <p>420000</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Rodzaj</p>
    </td>
    <td>
    <p>Der Typ der Erklärung.</p>
    </td>
    <td>
    <p>S</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Wersja</p>
    </td>
    <td>
    <p>Die Dokumentenversion.</p>
    </td>
    <td>
    <p>22</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Numer</p>
    </td>
    <td>
    <p>Die Dokumentennummer.</p>
    </td>
    <td>
    <p>11</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Miesiac</p>
    </td>
    <td width="330">
    <p>Der Referenzmonat.</p>
    </td>
    <td>
    <p>10</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Rok</p>
    </td>
    <td width="330">
    <p>Das Referenzjahr.</p>
    </td>
    <td>
    <p>2021</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Typ</p>
    </td>
    <td width="330">
    <p>Die Berichtsrichtung.</p>
    </td>
    <td>
    <p>Mi</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>NrWlasny</p>
    </td>
    <td width="330">
    <p>Der Bezeichner der Erklärung.</p>
    </td>
    <td>
    <p>21ISTDEMF-0001</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p><strong>Informationen über das Unternehmen</strong></p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Miejscowosc</p>
    </td>
    <td width="330">
    <p>Der Ort, an dem sich das Unternehmen befindet.</p>
    </td>
    <td>
    <p>Warschau (Warszawa)</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Regon</p>
    </td>
    <td width="330">
    <p>Der Regon-Code des Unternehmens.</p>
    </td>
    <td>
    <p>12345678901234</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Nip</p>
    </td>
    <td>
    <p>Der NIP-Code des Unternehmens.</p>
    </td>
    <td>
    <p>1234567890</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KodPocztowy</p>
    </td>
    <td>
    <p>Die Postleitzahl des Unternehmens.</p>
    </td>
    <td>
    <p>31-111</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>UlicaNumer</p>
    </td>
    <td>
    <p>Die Straße, in der sich das Unternehmen befindet.</p>
    </td>
    <td>
    <p>Statystyczna 22/1</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Nazwa</p>
    </td>
    <td>
    <p>Der Name des Unternehmens.</p>
    </td>
    <td>
    <p>Contoso Entertainment System Germany</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p><strong>Informationen über die Ware</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>WartoscStatystyczna</p>
    </td>
    <td>
    <p>Der statistische Wert.</p>
    </td>
    <td>
    <p>2632</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>WartoscFaktury</p>
    </td>
    <td>
    <p>Der Rechnungswert.</p>
    </td>
    <td>
    <p>2632</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>MasaNetto</p>
    </td>
    <td>
    <p>Die Nettomasse.</p>
    </td>
    <td>
    <p>16</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>IdKontrahenta</p>
    </td>
    <td>
    <p>Die MwSt.-Nummer des Debitoren.</p>
    </td>
    <td>
    <p>DE9012</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KodTowarowy</p>
    </td>
    <td>
    <p>Der Warencode.</p>
    </td>
    <td>
    <p>10020030</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>RodzajTransakcji</p>
    </td>
    <td>
    <p>Der Buchungscode.</p>
    </td>
    <td>
    <p>11</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>WarunkiDostawy</p>
    </td>
    <td>
    <p>Die Bedingungen des Liefermodus.</p>
    </td>
    <td>
    <p>Kosten, Versicherung und Fracht</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KrajPochodzeniaWysylki</p>
    </td>
    <td>
    <p>Der Code für das Versand-/Zielland oder die Region.</p>
    </td>
    <td>
    <p>DE</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>OpisTowaru</p>
    </td>
    <td>
    <p>Eine Beschreibung der Waren.</p>
    </td>
    <td>
    <p>Hardware</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>PozId</p>
    </td>
    <td>
    <p>Die Nummer des Artikels.</p>
    </td>
    <td>
    <p>1</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p><strong>Kontaktinformationen</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>E-Mail-Adresse</p>
    </td>
    <td>
    <p>Die E-Mail-Adresse des Übermittlers.</p>
    </td>
    <td>
    <p>manishc@contoso.com</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Faks</p>
    </td>
    <td>
    <p>Die Faxnummer des Übermittlers.</p>
    </td>
    <td>
    <p>425-555-5049</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Telefon</p>
    </td>
    <td>
    <p>Die Telefonnummer des Übermittlers.</p>
    </td>
    <td>
    <p>425-555-5068</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>NazwiskoImie</p>
    </td>
    <td>
    <p>Der Name des Übermittlers.</p>
    </td>
    <td>
    <p>Manish Chopra</p>
    </td>
    </tr>
    </tbody>
    </table>

21. Prüfen Sie den erzeugten Bericht im Excel-Format.

    ![Intrastat-Bericht über Sendungen](media/intrastat_pl_3.png)

### <a name="create-a-purchase-order"></a>Eine Bestellung erstellen

1. Gehen Sie zu **Kreditoren** > **Bestellungen** > **Alle Bestellungen**.
2. Wählen Sie im Aktivitätsbereich **Neu** aus.
3. Wählen Sie im Dialogfeld **Bestellung erstellen** im Feld **Kreditorenkonto** **DE-001**.
4. Im Feld **Standort** wählen Sie **1** aus.
5. Im Feld **Lagerort** wählen Sie **11** aus.
6. Wählen Sie **OK** aus.
7. Überprüfen Sie, ob auf der Registerkarte **Header** im Inforegister **Lieferung** das Feld **Liefermodus** auf **10** und das Feld **Lieferbedingungen** auf **CIF** gesetzt ist.
8. Wählen Sie auf der Registerkarte **Zeilen** auf dem Inforegister **Bestellzeilen** im Feld **Positionsnummer** den Wert **D0003**. Geben Sie dann im Feld **Menge** den Wert **6** ein.
9. Überprüfen Sie, ob im Inforegister **Positionsdetails** auf der Registerkarte **Außenhandel** der **Transaktionscode** auf **11**, das Feld **Transport** auf **3**, das Feld **Ware** auf **100 200 30** und das Feld **Ursprungsland/-region** auf **DEU** gesetzt sind.
10. Wählen Sie im Aktionsbereich, auf der Registerkarte **Kauf**, in der Gruppe **Aktionen** den Eintrag **Bestätigen**.
11. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Rechnung** in der Gruppe **Generieren** **Rechnung** aus.
12. Wählen Sie im Aktivitätsbereich **Standard von** und dann im Feld **Standardmenge für Positionen** **Bestellmenge** aus. Wählen Sie dann **OK** aus.
13. Geben Sie auf dem Inforegister **Kreditor Rechnungskopf** im Abschnitt **Rechnungsidentifikation** im Feld **Nummer** **00010** ein.
14. Wählen Sie im Abschnitt **Rechnungsdaten** im Feld **Rechnungsdatum** das aktuelle Datum aus. Dieses Datum wird für die Intrastat-Übertragung verwendet.
15. Wählen Sie im Feld **Empfangsdatum des Dokuments** **18.10.2021** (18. Oktober 2021) aus.
16. Wählen Sie im Aktionsbereich **Buchen**, um die Rechnung zu buchen.

### <a name="create-an-intrastat-declaration-for-arrivals"></a>Erzeugen einer Intrastat-Meldung für Eingänge

1. Wechseln Sie zu **Steuer** > **Meldungen** > **Außenhandel** > **Intrastat**.
2. Wählen Sie im Aktivitätsbereich **Übertragung**.
3. Legen Sie im Dialogfeld **Intrastat (Übertragung)** die Option **Kreditor-Rechnung** auf **Ja** fest.
4. Wählen Sie **OK**, um die Transaktionen zu übertragen, und überprüfen Sie dann das Intrastat-Buch.-Blatt.

    ![Position, die die Bestellung auf der Intrastat-Seite darstellt](media/intrastat_pl_4.png)

5. Überprüfen Sie die Informationen auf der Registerkarte **Allgemein** für die Bestellung.

    ![Bestellungsdetails auf der Registerkarte „Allgemein“ der Intrastat-Seite](media/intrastat_pl_5.png)

6. Wählen Sie im Aktivitätsbereich **Ausgabe** > **Bericht**.
7. Wählen Sie im Dialogfeld **Intrastat-Bericht**, das Inforegister **Parameter**, den Abschnitt **Datum**, das Feld **Von-Datum** aus und geben Sie den ersten Tag des derzeitigen Monats ein.
8. Im Abschnitt **Exportoptionen** legen Sie die Option **Generieren** auf **Ja** fest. Geben Sie dann im Feld **Dateiname** den gewünschten Namen ein.
9. Legen Sie die Option **Bericht generieren** auf **Ja** fest. Geben Sie dann in das Feld **Berichtsdateiname** den gewünschten Namen ein.
10. Wählen Sie im Feld **Richtung** die Option **Eingänge**.
11. Überprüfen Sie, ob im Abschnitt **Dateiformatzuordnung** das Feld **Meldungsart** auf **Erklärung** gesetzt ist.
12. Geben Sie im Feld **Stadt der Dokumenterstellung** **Krakau** ein.
13. Wählen Sie im Feld **Stadt der Dokumenterstellung** **19.10.2021** (19. Oktober 2021) aus.
14. Geben Sie im Feld **Dokumentnr.** **11** ein.
15. Geben Sie im Feld **Dokumentversion** **22** ein.
16. Wählen Sie **OK** und prüfen Sie den erzeugten Bericht im XML-Format. Die folgende Tabelle zeigt die Werte in dem Beispielbericht.

    <table>
    <tbody>
    <tr>
    <td>
    <p><strong>Feldname</strong></p>
    </td>
    <td>
    <p><strong>Feldbeschreibung</strong></p>
    </td>
    <td>
    <p><strong>Wert</strong></p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p align=center><strong>Informationen über das Dokument</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Deklaracja Data</p>
    </td>
    <td>
    <p>Das Erstellungsdatum des Dokuments.</p>
    </td>
    <td>
    <p>19.10.2021</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Miejscowosc</p>
    </td>
    <td>
    <p>Die Stadt, in der das Dokument erstellt wurde.</p>
    </td>
    <td>
    <p>Krakau</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LacznaLiczbaPozycji</p>
    </td>
    <td>
    <p>Gesamtzahl der Artikel.</p>
    </td>
    <td>
    <p>1</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LacznaWartoscStatystyczna</p>
    </td>
    <td>
    <p>Der statistische Gesamtwert.</p>
    </td>
    <td>
    <p>965</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LacznaWartoscFaktur</p>
    </td>
    <td>
    <p>Der Gesamtwert der Rechnung.</p>
    </td>
    <td>
    <p>965</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>UC</p>
    </td>
    <td>
    <p>Der Einheitencode.</p>
    </td>
    <td>
    <p>420000</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Rodzaj</p>
    </td>
    <td>
    <p>Der Typ der Erklärung.</p>
    </td>
    <td>
    <p>S</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Wersja</p>
    </td>
    <td>
    <p>Die Dokumentenversion.</p>
    </td>
    <td>
    <p>22</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Numer</p>
    </td>
    <td>
    <p>Die Dokumentennummer.</p>
    </td>
    <td>
    <p>11</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Miesiac</p>
    </td>
    <td width="332">
    <p>Der Referenzmonat.</p>
    </td>
    <td>
    <p>10</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Rok</p>
    </td>
    <td width="332">
    <p>Das Referenzjahr.</p>
    </td>
    <td>
    <p>2021</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Typ</p>
    </td>
    <td width="332">
    <p>Die Berichtsrichtung.</p>
    </td>
    <td>
    <p>P</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>NrWlasny</p>
    </td>
    <td width="332">
    <p>Der Bezeichner der Erklärung.</p>
    </td>
    <td>
    <p>21ISTDEMF-0002</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p align=center><strong>Informationen über das Unternehmen</strong></p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Miejscowosc</p>
    </td>
    <td width="332">
    <p>Der Ort, an dem sich das Unternehmen befindet.</p>
    </td>
    <td>
    <p>Warschau (Warszawa)</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Regon</p>
    </td>
    <td width="332">
    <p>Der Regon-Code des Unternehmens.</p>
    </td>
    <td>
    <p>12345678901234</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Nip</p>
    </td>
    <td>
    <p>Der NIP-Code des Unternehmens.</p>
    </td>
    <td>
    <p>1234567890</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KodPocztowy</p>
    </td>
    <td>
    <p>Die Postleitzahl des Unternehmens.</p>
    </td>
    <td>
    <p>31-111</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>UlicaNumer</p>
    </td>
    <td>
    <p>Die Straße, in der sich das Unternehmen befindet.</p>
    </td>
    <td>
    <p>Statystyczna 22/1</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Nazwa</p>
    </td>
    <td>
    <p>Der Name des Unternehmens.</p>
    </td>
    <td>
    <p>Contoso Entertainment System Germany</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p align=center><strong>Informationen über die Ware</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>WartoscStatystyczna</p>
    </td>
    <td>
    <p>Der statistische Wert.</p>
    </td>
    <td>
    <p>965</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>WartoscFaktury</p>
    </td>
    <td>
    <p>Der Rechnungswert.</p>
    </td>
    <td>
    <p>965</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>MasaNetto</p>
    </td>
    <td>
    <p>Die Nettomasse.</p>
    </td>
    <td>
    <p>30</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KrajPochodzenia</p>
    </td>
    <td>
    <p>Der Code für das Ursprungsland oder die Ursprungsregion.</p>
    </td>
    <td>
    <p>DE</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>RodzajTransportu</p>
    </td>
    <td>
    <p>Der Modus des Transportcodes.</p>
    </td>
    <td>
    <p>3</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KodTowarowy</p>
    </td>
    <td>
    <p>Der Warencode.</p>
    </td>
    <td>
    <p>10020030</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>RodzajTransakcji</p>
    </td>
    <td>
    <p>Der Buchungscode.</p>
    </td>
    <td>
    <p>11</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>WarunkiDostawy</p>
    </td>
    <td>
    <p>Die Bedingungen des Liefermodus.</p>
    </td>
    <td>
    <p>Kosten, Versicherung und Fracht</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KrajPochodzeniaWysylki</p>
    </td>
    <td>
    <p>Der Code für das Versand-/Zielland oder die Region.</p>
    </td>
    <td>
    <p>DE</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>OpisTowaru</p>
    </td>
    <td>
    <p>Eine Beschreibung der Waren.</p>
    </td>
    <td>
    <p>Hardware</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>PozId</p>
    </td>
    <td>
    <p>Die Nummer des Artikels.</p>
    </td>
    <td>
    <p>1</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p align=center><strong>Kontaktinformationen</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>E-Mail-Adresse</p>
    </td>
    <td>
    <p>Die E-Mail-Adresse des Übermittlers.</p>
    </td>
    <td>
    <p>manishc@contoso.com</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Faks</p>
    </td>
    <td>
    <p>Die Faxnummer des Übermittlers.</p>
    </td>
    <td>
    <p>425-555-5049</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Telefon</p>
    </td>
    <td>
    <p>Die Telefonnummer des Übermittlers.</p>
    </td>
    <td>
    <p>425-555-5068</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>NazwiskoImie</p>
    </td>
    <td>
    <p>Der Name des Übermittlers.</p>
    </td>
    <td>
    <p>Manish Chopra</p>
    </td>
    </tr>
    </tbody>
    </table>

17. Prüfen Sie den erzeugten Bericht im Excel-Format.

    ![Intrastat-Bericht zu Wareneingängen](media/intrastat_pl_6.png)
