---
title: Partei und globales Adressbuch
description: In diesem Thema wird die Partei- und globale Adressbuchfunktionalität von Duales Schreiben beschrieben.
author: RamaKrishnamoorthy
ms.date: 02/22/2021
ms.topic: article
ms.service: dynamics-ax-applications
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-02-22
ms.openlocfilehash: e7bec58f8094a1448017822e7d8840368cc482b8
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750787"
---
# <a name="party-and-global-address-book"></a>Partei und globales Adressbuch

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Partei und globales Adressbuch sind Konzepte in Finance and Operations-Anwendungen. Eine Partei kann eine Person oder eine Organisation sein. Es ist bequem, Eigenschaften von einer **Partei**, wie Name, Sprache, Kontakte und Adressen, global zu speichern und zu verwalten. Wenn sich ein Eigenschaftswert an einer Stelle ändert, wird er an allen Stellen angezeigt, an denen die **Partei** involviert ist.

## <a name="party"></a>Partei

Eine *Partei* ist eine Person oder Organisation, die am Geschäft beteiligt ist. Durch die Verwendung des Partei-Konzepts kann eine Person oder Organisation mehr als eine Rolle (Mitarbeiter, Kunde, Lieferant oder Kontakt) in einem Unternehmen spielen. Die Rolle basiert auf dem Kontext und dem Zweck. Hier einige Beispiele von zwei fiktiven Unternehmen, Contoso und Fabrikam.

+ **Arbeitskraft**: Ein Mitarbeiter. Zum Beispiel ein Mitarbeiter von Contoso.
+ **Lieferant**: Eine Lieferantenorganisation oder ein Einzelunternehmer, der Waren oder Dienstleistungen an ein Unternehmen liefert. Wenn Fabrikam beispielsweise Lieferungen an Contoso verkauft, übernimmt Fabrikam die Rolle des Lieferanten.
+ **Kontakt**: Eine Kontaktperson. Wenn Contoso beispielsweise Verbrauchsmaterialien von Fabrikam kauft, kontaktiert ein Mitarbeiter von Contoso den Kontakt von Fabrikam.
+ **Kunde**: Ein Kunde ist eine Person oder Firma, die Dinge von einer Firma kauft. Wenn Contoso beispielsweise Verbrauchsmaterialien von Fabrikam kauft, ist Contoso ein Kunde von Fabrikam.

Das Parteimodell wird häufig verwendet, um mittlere bis komplexe Beziehungen zwischen Organisationen und Personen darzustellen, insbesondere wenn eine Partei mehr als eine Rolle spielt. Im Folgenden finden Sie einige allgemeine Beispiele hierfür:

+ Eine Partei kann sowohl Kunde als auch Verkäufer sein. In Nordamerika verkauft Fabrikam beispielsweise elektrische Kabel an Contoso und kauft montierte Lautsprecher von Contoso. In Europa verkauft Fabrikam Teile an Contoso, kauft aber nichts von Contoso.
+ Eine Partei kann sowohl Mitarbeiter als auch Kunde sein. Beispielsweise kauft ein Mitarbeiter von Contoso Elektronik von Contoso für den persönlichen Gebrauch.
+ Es kann eine Viele-zu-Viele-Beziehung zwischen einer Person und einer Organisation geben. Beispielsweise liefert Fabrikam Service-Spezialisten und beschäftigt einen Vermittlungskoordinator. Der Koordinator ordnet die Service-Spezialisten den Arbeitsanforderungen mehrerer Kunden von Fabrikam zu. Contoso ist eines der Kundenkonten. Wenn Contoso einen Spezialisten benötigt, kontaktiert Contoso den Koordinator, der dann die Anfrage unterstützt. Der Koordinator bearbeitet Anfragen für alle Kunden und schafft so eine Viele-zu-Viele-Beziehung.

Das folgende Bild zeigt das Datenmodell für Partei:

![Datenmodell für Partei](media/party-gab-image1.png)

> [!Tip]
> Wenn Sie versuchen, einen neuen Kontodatensatz zu erstellen, verwenden Sie das Feld „Partei“, um nach dem Datensatz nach Namen zu suchen. Wenn Sie den Datensatz finden, müssen Sie nur den Datensatz auswählen. Das System füllt automatisch alle Daten der Partei. Sie müssen nicht alle erforderlichen Felder manuell eingeben. Dieses Verhalten kann auf Konto-, Kontakt- und Lieferantenformularen gefunden werden, die standardmäßig ausgeliefert werden.

Nicht alle Parteirollen von Finance and Operations-Apps werden von Duales Schreiben unterstützt. Eine vollständige Liste der Parteirollen finden Sie unter [Überblick über globale Adressbücher](../../../fin-ops/organization-administration/overview-global-address-book.md).

### <a name="global-address-book"></a>Globales Adressbuch

Das globale Adressbuch ist ein Verzeichnis mit postalischen und elektronischen Adressen der Organisationen und Einzelpersonen, die an einem Unternehmen teilnehmen.

Das globale Adressbuch speichert und verarbeitet so viele Postanschriften und elektronische Adressen wie nötig. Angenommen, Fabrikam verfügt über Tankstellen an 50 Standorten. Jeder Standort hat eine andere Postanschrift, E-Mail-Adresse und Telefonnummer. Alle geschäftlichen Einkäufe werden der Haupttankstelle in Rechnung gestellt, aber die Einkäufe werden direkt an die spezifische Tankstelle geliefert, an der der Kauf angefordert wurde. Das globale Adressbuch speichert die Haupttankstelle als Rechnungsadresse und jede Tankstelle als Lieferadresse für Fabrikam. Die Adressen können einmal gespeichert und bei Bedarf für Angebote und Bestellungen abgerufen werden.

Eine Person oder Organisation kann je nach Geschäftskontext mehr als eine Rolle spielen. Wenn sie dies tun, können ihre Postanschriften und elektronischen Adressen identisch sein. In diesem Fall sollte eine Adressänderung in einer Rolle in der anderen Rolle erfolgen und umgekehrt. Das globale Adressbuch speichert und verarbeitet Adressen global.

![Datenmodell für globales Adressbuch](media/party-gab-image2.png)

## <a name="contacts"></a>Kontakte

In Kundenbindungs-Apps ist ein *Kontakt* eine Person. Die Tabelle **Kontakt** wurde jedoch überladen, um eine Person, einen Portalbenutzer, einen B2C-Kunden oder einen Lieferanten darzustellen. Die Darstellung ist implizit und Sie können den Unterschied nicht erkennen, ohne die zugehörigen Transaktionen zu untersuchen. Die Tabelle **Kontakt** wurde auf eine 1:1-Beziehung mit der **Konto**-Tabelle beschränkt. Als Teil des Partei- und globalen Adressbuchmodells führt Duales Schreiben explizite Eigenschaften für die Klassifizierung ein und Duales Schreiben ermöglicht N:N-Beziehungen zwischen einer **Kontakt**-Person und einer Organisation (Kontoentität oder Lieferantenentität).

Es gibt zwei Typen von **Kontakt**-Zeilen:

+ Zusammengefasster Kontakt – Kontaktzeile mit einem obligatorischen Wert im Feld **Unternehmen**.
+ Nicht zusammengefasster Kontakt – Kontaktzeile mit leerem Feld **Unternehmen**.

Die Tabelle **Kontakt** kann diese Arten von Zeilen speichern:

Zeilentyp | Beschreibung
---|---
Eine Person, die Kunde ist, beispielsweise ein verkaufbarer Kontakt oder ein B2C-Kunde. | Ein zusammengefasster Kontaktdatensatz, in dem das Feld **Unternehmen** nicht leer und das Feld **Ist Kunde** auf **Ja** gesetzt ist.
Eine Person, die ein Verkäufer ist, zum Beispiel ein Einzelunternehmer wie ein Verkäufer. | Ein zusammengefasster Kontaktdatensatz, in dem das Feld **Unternehmen** nicht leer und das Feld **Ist Lieferant** auf **Ja** gesetzt ist.
Eine Partei, die sowohl Kunde als auch Verkäufer ist. | Ein zusammengefasster Kontaktdatensatz, in dem das Feld **Unternehmen** nicht leer und das Feld **Ist Kunde** auf **Ja** und das Feld **Ist Lieferant** auf **Ja** gesetzt ist. Eine Person kann sowohl Produzent für ein Produkt als auch Verbraucher für ein anderes Produkt sein. Beide, Finance and Operations-Apps und Duales Schreiben, unterstützen diese Beziehung.
Eine Person, die eine Kontaktperson für eine Organisation ist, aber weder Kunde noch Verkäufer. | Ein nicht zusammengefasster Kontaktdatensatz, in dem das Feld **Unternehmen** leer und das Feld **Ist Kunde** auf **Nein** und das Feld **Ist Lieferant** auf **Nein** gesetzt ist.

## <a name="contact-for-party"></a>Kontakt für Partei

**Kontakt für Partei** speichert und verarbeitet N:N-Beziehungen zwischen **Konto**-Zeilen und **Kontakt**-Zeilen. Es kann die zusammengefassten **Kontakt**-Zeilen aus nicht zusammengefassten Zeilen herausfiltern und nur die nicht zusammengefassten **Kontakt**-Zeilen zu **Konto**- oder **Lieferant**-Zeilen zuordnen.

Zum Beispiel sind Natasha Jones und Miguel Reyes Tierärzte, die Farmen in ihren Gebieten versorgen. Natasha bedient die Region Seattle und Miguel die Region Kent. In der Kundenbindungs-App werden die Farmen als Kunden dargestellt und die Tierärzte sind Kontaktpersonen. Ein einziger **Kontakt**-Datensatz für Natasha ist allen Farmen zugeordnet, mit denen Natasha zusammenarbeitet. Ebenso ist ein einziger **Kontakt**-Datensatz für Miguel allen Farmen zugeordnet, mit denen Miguel zusammenarbeitet.

Diese Beziehungen werden in der Tabelle **Kontakt für Partei** gespeichert. Sie finden die Informationen in den Standardformularen:

+ Wenn Sie im **Konto**-Formular sind, gibt es eine Registerkarte mit dem Namen **Zugeordnete Kontakte**. Verwenden Sie diese Registerkarte, um einen oder mehrere Kontakte der Zeile **Konto** zuzuordnen. In diesem Formular weisen Sie eine Kontaktperson für eine Organisation zu. Nachdem Sie Kontakte zugewiesen haben, können Sie einen als primären Kontakt für dieses Konto auswählen. Bei Verwendung des Formulars **Schnellerstellung** können Sie nur eine Kontaktperson auswählen. Das Verhalten ist das Gleiche, wenn Sie das Formular **Lieferant** verwenden und der Datensatztyp **Organisation** ist.
+ Wenn Sie im Formular **Kontakt** sind und die Zeile ein Kunde oder Lieferant oder beides ist (ein zusammengefasster Kontakt), gibt es eine Registerkarte mit dem Namen **Zugeordnete Kontakte**. Verwenden Sie diese Registerkarte, um einen oder mehrere Kontakte zuzuordnen. In diesem Formular weisen Sie eine Kontaktperson für den B2C-Kunden oder Lieferanten zu. Nachdem Sie Kontakte zugewiesen haben, können Sie einen als primären Kontakt auswählen. Bei Verwendung des Formulars **Schnellerstellung** können Sie nur eine Kontaktperson auswählen.
+ Wenn Sie im Formular **Kontakt** sind und die Zeile eine Kontaktperson ist (ein nicht zusammengefasster Kontakt), gibt es eine Registerkarte mit dem Namen **Zugeordnete Organisationen**. Verwenden Sie diese Registerkarte, um einen oder mehrere Kunden oder Lieferanten zuzuordnen. In diesem Formular weisen Sie einen Kunden oder Lieferanten der zugrunde liegenden Kontaktperson zu. Der Kunde oder Lieferant kann eine Organisation, eine Person oder beides sein. Sie können jeweils nur einen Wert aus den vier Feldern auswählen.

    ![Registerkarte „Zugeordnete Organisationen“](media/party-gab-image3.png)

    + Wenn Sie **Partei-ID** auswählen, wird der zugrunde liegende Kontakt allen Rollen der ausgewählten Partei zugewiesen.
    + Wenn Sie **Zugeordneter Kontakt** auswählen, dann wählen Sie den zusammengefassten Kontakt vom Typ „Person“ aus.
    + Wenn Sie **Zugeordnetes Konto** oder **Lieferant** auswählen, dann wählen Sie eine Organisation aus.

    Unabhängig von Ihrer Wahl wird die Zuordnung auf Parteiebene erstellt und gilt für alle Rollen der Partei. Sie wird in der Entität „Kontakt für Partei“ gespeichert.

> [!Note]
> Der Anzeigename für die Tabelle **Kontakt für Partei** in der Kundenbindungs-App ist **Kontakt für Debitor/Kreditor**.

Wenn Sie eine **Kontakt**-Zeile öffnen, wo **Ist Kunde** **Nein** und **Ist Lieferant** **Nein** ist, werden Sie die Registerkarte **Zugeordnete Organisationen** sehen. Auf dieser Registerkarte können Sie dem Kontakt eine oder mehrere Kunden- oder Lieferantenorganisationen zuordnen.

Wenn Sie eine **Kontakt**-Zeile öffnen, wo **Ist Kunde** **Ja** oder **Ist Lieferant** **Ja** ist, werden Sie die Registerkarte **Zugeordnete Kontakte** sehen. Auf dieser Registerkarte können Sie einen oder mehrere Kontakte zuordnen.

## <a name="postal-address"></a>Postadresse

Eine neue Registerkarte mit dem Namen **Adressen** wurde in den Formularen **Konto**, **Kontakt** und **Lieferant** eingeführt. Die **Adressen** für die Unterstützung von N Adressen mithilfe eines Rasters, wie in diesem Bild gezeigt:

![Raster für Postanschrift](media/party-gab-image4.png)

+ In der Spalte **Rollen der Postanschrift** wird der Zweck der Adresse aufgeführt.
+ Die Spalte **Ist primär** listet die primäre Adresse auf.
+ Die Spalte **Adressnummer** listet die Adressreihenfolge auf.
+ Mit der Schaltfläche **+ Neue Adresse** können Sie eine neue Adresse erstellen. Sie können so viele Adressen erstellen, wie Sie wollen.

Die Felder **Adresse 1** und **Adresse 2** auf der **Zusammenfassung**-Registerkarte des **Konto**-Formulars entsprechen den Adressen für **Lieferung** bzw. **Rechnung**.

![Registerkarte „Zusammenfassung“ für die Postanschrift](media/party-gab-image5.png)

Die Felder **Adresse 1**, **Adresse 2** und **Adresse 3** auf der **Zusammenfassung**-Registerkarte des **Kontakt**-Formulars entsprechen den Adressen für **Unternehmen**, **Lieferung** bzw. **Rechnung**.

## <a name="electronic-address"></a>Elektronische Adresse

Eine neue Registerkarte mit dem Namen **Elektronische Adressen** wurde in den Formularen **Konto**, **Kontakt** und **Lieferant** eingeführt. Die **Adressen** für die Unterstützung von N Adressen mithilfe eines Rasters, wie in diesem Bild gezeigt:

![Raster für elektronische Adresse](media/party-gab-image6.png)

+ Die Spalte **Typ** listet den Typ der Adresse auf.
+ Die Spalte **Ist primär** listet die primäre Adresse auf.
+ In der Spalte **Zweck** wird der Zweck der elektronischen Adresse aufgeführt.
+ Mit der Schaltfläche **+ Neue elektronische Adresse** können Sie eine neue Adresse erstellen. Sie können so viele Adressen erstellen, wie Sie wollen.

Elektronische Adressen sind nur in diesem Raster verfügbar. In zukünftigen Versionen werden alle elektronischen und postalischen Adressfelder von anderen Registerkarten entfernt, z. B. den Registerkarten **Zusammenfassung** und **Details**.

## <a name="setup-instructions"></a>Setupanweisungen

Wenn Sie bereits Kunde von Duales Schreiben sind, sind die folgenden Anweisungen zur Einrichtung erforderlich. Andernfalls können Sie diesen Abschnitt überspringen.

1. Stoppen Sie die folgenden Zuordnungen, da sie nicht mehr benötigt werden. Führen Sie stattdessen die Zuordnung „Kontakte V2“ (msdyn_contactforparties) aus.

    + CDS-Kontakte V2 und Kontakte (bezieht sich auf Kundenkontakte)
    + CDS-Kontakte V2 und Kontakte (bezieht sich auf Lieferantenkontakte)

2. Die folgenden Entitätszuordnungen werden für die Partei-Funktionalität aktualisiert, daher muss die neueste Version auf diese Zuordnungen angewendet werden.

Zuordnen | Update auf diese Version | Änderungen
---|---|---
Debitoren V3 (Konten) | 1.0.0.5 |Die PartyNumber und andere parteibezogene Felder wie Name, persönliche Daten, Postanschriftfelder, elektronische Kontaktadressfelder usw. wurden entfernt.
Kunde V3 (Kontakte) | 1.0.0.5 | Die PartyNumber und andere parteibezogene Felder wie Name, persönliche Daten, Postanschriftfelder, elektronische Kontaktadressfelder usw. wurden entfernt.
Kreditoren V2 (msdyn_vendors) | 1.0.0.6 | Die PartyNumber und andere parteibezogene Felder wie Name, persönliche Daten, Postanschriftfelder, elektronische Kontaktadressfelder usw. wurden entfernt.
CDS-Verkaufsangebotskopfzeilen (Angebote) | 1.0.0.6 | Die Kontaktperson wurde durch die ContactforParty-Referenz ersetzt.
Verkaufsrechnungskopfzeilen V2 (Rechnungen) | 1.0.0.4 | Die Kontaktperson wurde durch die ContactforParty-Referenz ersetzt.
CDS-Auftragskopfzeilen (salesorders) | 1.0.0.5 | Die Kontaktperson wurde durch die ContactforParty-Referenz ersetzt.
Kontakte V2 (msdyn_contactforparties) | 1.0.0.2 | Dies ist eine neue Zuordnung. Wenn Sie eine frühere Version der Parteilösung haben, müssen Sie diese Zuordnung wie erwähnt auf die neueste Version aktualisieren.
Postanschriften der CDS-Partei (msdyn_partypostaladdresses) | 1.0.0.1  | Dies ist eine neue Zuordnung, die im Rahmen der vorherigen Partei-Vorschauversion hinzugefügt wurde.
CDS-Postadressverlauf V2 (msdyn_postaladdresses) | | Dies ist eine neue Zuordnung, die im Rahmen der vorherigen Partei-Vorschauversion hinzugefügt wurde.
CDS-Postanschriften (msdyn_postaladdresscollections) | | Dies ist eine neue Zuordnung, die im Rahmen der vorherigen Partei-Vorschauversion hinzugefügt wurde.
Parteikontakte V3 (msdyn_partyelectronicaddresses) | | Dies ist eine neue Zuordnung, die im Rahmen dieses Releases hinzugefügt wurde.

## <a name="templates"></a>Vorlagen

Eine Sammlung von Tabellenzuordnungen arbeitet für die Interaktion von Partei und globalem Adressbuch zusammen, wie in der folgenden Tabelle dargestellt.

Finance and Operations-App | Customer Engagement-App     | Beschreibung
----------------------------|-----------------------------|------------
[Titel von Kontaktpersonen](mapping-reference.md#223) | msdyn_salescontactpersontitles |
[Debitoren V3](mapping-reference.md#101) | Konten |
[Debitoren V3](mapping-reference.md#116) | Kontakte |
[CDS-Parteien](mapping-reference.md#220) | msdyn_parties |
[CDS Postadressorte der Partei](mapping-reference.md#233) | msdyn_partypostaladdresses |
[CDS-Verlauf der Postanschrift V2](mapping-reference.md#235) | msdyn_postaladdresses |
[CDS Postadressorte](mapping-reference.md#234) | msdyn_postaladdresscollections |
[CDS-Verkaufsangebotskopf](mapping-reference.md#215) | Angebote |
[Auftragskopfzeilen CDS](mapping-reference.md#217) | salesorders |
[Schlussformeln](mapping-reference.md#222) | msdyn_complimentaryclosings |
[Kontakte V2](mapping-reference.md#221) | msdyn_contactforparties |
[Entscheidungsfunktionen](mapping-reference.md#224) | msdyn_decisionmakingroles |
[Stellenfunktionen](mapping-reference.md#225) | msdyn_employmentjobfunctions |
[Treueebenen](mapping-reference.md#226) | msdyn_loyaltylevels |
[Parteikontakte V3](mapping-reference.md#236) | msdyn_partyelectronicaddresses |
[Arten von Persönlichkeitsmerkmalen](mapping-reference.md#227) | msdyn_personalcharactertypes |
[Verkaufsrechnungskopfzeilen V2](mapping-reference.md#118) | Rechnungen |
[Anreden](mapping-reference.md#228) | msdyn_salutations |
[Kreditoren V2](mapping-reference.md#202) | msdyn_vendors |

Weitere Informationen finden Sie unter [Referenz für die Zuordnung von dualem Schreiben](mapping-reference.md).
