---
title: Intercompany-Fakturierung
description: "Dieser Artikel wird Informationen sowie Beispiele zu Intergesellschaftsrechnungsstellung für Projekte in Microsoft Dynamics 365 für Arbeitsgänge festgelegt."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 94153
ms.assetid: 33e98da7-01c1-4369-923d-aa1c8326cb80
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: eb32cf1b96dfef75131b8c7541e20a93615a87f7
ms.openlocfilehash: 8a606f81e6e66390bf0add3deeeb032ab4cbd90b
ms.lasthandoff: 03/31/2017


---

# <a name="intercompany-invoicing"></a>Intercompany-Fakturierung

Dieser Artikel wird Informationen sowie Beispiele zu Intergesellschaftsrechnungsstellung für Projekte in Microsoft Dynamics 365 für Arbeitsgänge festgelegt.

Ihre Organisation verfügt möglicherweise über mehrere Abteilungen, Tochtergesellschaften und andere juristische Personen, die einander Produkte und Dienstleistungen für Projekte übertragen. Die juristische Person, die den Service durchführt, Produkt oder das *lending gültige entity* " und die juristische Person, die den Service oder das Produkt erhält), wird das *borrowing gültige entity* bezeichnet. 

Die folgende Abbildung zeigt eine Situation, in der zwei juristischen Personen, SI FR (ausleihende juristische Person) und SI USA (ausleihenden juristischen Person) gemeinsam Ressourcen für ein Projekt für Kunde A nutzen. In diesem Szenario ist SI FR vertraglich zur Durchführung der Arbeit für Kunde A verpflichtet. 

![Intergesellschaftsrechnungsstellungsbeispiel ([]. /media/interco.invoicing-01.jpg)]". /media/interco.invoicing-01.jpg) 

Die Zielsetzung besteht, Kostenkontrolle, Umsatzerkennung, Steuern, und internen Verrechnungspreis flexibleren leistungsfähigen und für die Intergesellschaftsprojektbuchungen vorzunehmen. Darüber hinaus stehen folgenden Funktionen zur Verfügung:

-   Erstellen von Kundenrechnung für ein Projekt in einer ausleihenden juristische Person mithilfe von Intercompany-Arbeitszeitnachweise, -Ausgaben und Kreditorenrechnungen in eine ausleihenden juristischen Person.
-   Unterstützung von Steuerberechnungen und indirekten Kosten
-   Verzögern der Umsatzrealisierung in einer ausleihenden juristischen Person und der Kostenrealisierung einer ausleihenden juristischen Person.
-   Antizipieren von RIF-Umsätzen in der ausleihenden juristischen Person.
-   Festlegen von Transferpreisen, die auf verschiedenen Preismodellen basieren können. Nachfolgend finden Sie einige Beispiele:
    -   **Menge** – Der Betrag, den Sie in das Feld **Preisgestaltung** eingeben, sind die Istkosten pro Menge oder Einheit.
    -   **Betrag der Belastungen** – Der Verkaufspreis/die Kosten pro Buchung plus dem Betrag der Belastungen, die Sei im Feld **Preisgestaltung** eingeben.
    -   **Prozentsatz für Belastungen** – Der Verrechnungspreis ist der Preis/die Kosten pro Buchung mit dem im Feld **Preisgestaltung** eingegeben Belastungsprozentsatz.
    -   **Prozentsatz des Verkaufspreises** – Der Prozentsatz des Verkaufspreises, der für die ausleihende juristische Person gebucht wird.
    -   **Betrag unter Verkaufspreis** – Der Betrag, den die ausleihende juristische Person vom Verkaufspreis vor der Buchung an die ausleihende juristischen Person zurückhält.
    -   **Deckungsbeitragsverhältnis** – Die Zahl, die Sie in das Feld **Preisgestaltung** eingeben, ist der Deckungsbeitrag ausgedrückt als Prozentsatz des Verkaufspreises.

## <a name="example-1-set-up-parameters-for-intercompany-invoicing"></a>Beispiel 1: Parameter für die Intercompany-Fakturierung einrichten
In diesem Beispiel ist USSI eine ausleihenden juristischen Person. Ihre Ressourcen Berichten die Zeit an die ausleihende juristische Person FRSI, die in einem Vertragsverhältnis mit dem Endkunden steht. Die Stunden und Ausgaben, die von USSI-Mitarbeiter gemeldet werden, können in die von FRSI generierte Projektfakturierung einbezogen werden. Darüber hinaus gibt es eine dritte Buchungsquelle, die von der ausleihenden juristischen Person stammen kann (in diesem Beispiel USSI) wenn diese gemeinsame Dienstleistungen für einen Kreditor für Tochtergesellschaften ((wie FRSI) bereitstellt und dann die Kosten an Projekte in diesen Tochtergesellschaften weitergibt. Alle erforderlichen Beim Steuerberechnungen und werden von Dynamics 365 für Arbeitsgänge abgeschlossen. 

In diesem Beispiel muss FRSI ein Debitor der juristischen Person USSI sein. USSI muss ein Kreditor in der juristischen Person FRSI sein. Sie können dann die Intercompany-Beziehung zwischen den zwei juristischen Personen einrichten. Das folgende Verfahren veranschaulicht die Einrichtung von Parametern für die Teilnahme beider juristischer Personen an der Intercompany-Fakturierung.

1.  Richten Sie FRSI als Debitor in der juristischen Person USSI und USSI als Kreditor in der juristische Person FRSI ein. Es gibt drei Einstiegspunkte für die für diese Aufgabe erforderlichen Schritte.
    | Schritt | Einstiegspunkt                                                                       | Beschreibung   |
    |------|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | A:    | In USSI klicken Sie ** Debitor ** &gt; ** auf Debitoren ** &gt; ** ** alle Debitoren. | Erstellen Sie einen neuen Debitorendatensatze für FRSI, und wählen Sie die Debitorengruppe aus.                                                                                                                                                                                                                           |
    | Mrd    | In FRSI klicken Sie ** Kreditor ** &gt; ** auf Kreditoren ** &gt; ** ** alle Kreditoren.        | Erstellen Sie einen neuen Kreditorendatensatz für USSI, und wählen Sie die Kreditorengruppe aus.                                                                                                                                                                                                                               |
    | C:    | Öffnen Sie in FRSI den Kreditorendatensatz, den Sie gerade erstellt haben.                            | Klicken Sie im Aktivitätsbereich auf der Registerkarte **Allgemein** und in der Gruppe **Einrichtung** auf **Intercompany**. Auf der Seite **Intercompany** legen Sie auf der Registerkarte **Handelsbeziehung** den **Aktiv**-Schieberegler auf **Ja** fest. Wählen Sie im Feld **Debitorenunternehmen** den Kundendatensatz, den Sie in Schritt A erstellt haben. |

2.  ** Auf Projektverwaltung und Buchhaltung ** &gt; ** Einstellungen ** &gt; ** Projektverwaltungsbetriebskontoparameter ** und klicken Sie dann auf die Registerkarte. ** ** Intercompany Die Einrichtung dieser Parameter hängt davon ab, ob Sie die ausleihende juristische Person oder die verleihende juristische Person sind.
    -   Wenn Sie die ausleihende juristische Person sind, wählen Sie die Beschaffungskategorie, die verwendet werden, um die automatisch generierten Vendorenrechnungen zuzuordnen.
    -   Wenn Sie die verleihende juristische Person sind, wählen Sie für jede ausleihende Person eine standardmäßige Projektkategorie für jede Buchungsart. Projektkategorien dienen der Steuerkonfiguration wenn die fakturierte Kategorie in Intercompany-Buchungen nur in der ausleihenden juristische Person vorhanden ist. Sie können die Umsatzerlöse für Intercompany-Buchungen antizipieren. Die Antizipierung wird durchgeführt wenn die Buchungen durchgeführt wird. Sie wird storniert wenn die Intercompany-Rechnung gebucht wird.

3.  ** Auf Projektverwaltung und Buchhaltung ** &gt; ** Einstellungen ** &gt; ** Preise ** &gt; ** interner Verrechnungspreis **.
4.  Wählen Sie eine Währung, eine Buchungsart und ein Internes Verrechnungspreismodell aus. Die für die Rechnung verwendete Währung ist die Währung, die im Kundendatensatz der ausleihenden juristische Person für die verleihende juristische Person konfiguriert ist. Die Währung wird zur Zuordnung von Einträgen in der Tabelle für den internen Verrechnungspreis genutzt.
5.  ** Hauptbuch auf ** &gt; ** Buchungseinstellungen ** &gt; ** Verrechnung ** und eingerichtet einer Beziehung für USSI und FRSI.

## <a name="example-2-create-and-post-an-intercompany-timesheet"></a>Beispiel 2: Erstellen und Buchen von Intercompany-Arbeitszeitnachweisen
USSI, die verleihende juristische Person, muss die Arbeitszeitnachweise für ein Projekt von FRSI, der ausleihenden juristischen Person, erstellen und buchen. Es gibt zwei Einstiegspunkte für die für diese Aufgabe erforderlichen Schritte.

| Schritt | Einstiegspunkt                                                                       | Beschreibung                                                                                                                                                                                       |
|------|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A:    | ** Projektverwaltung und Buchhaltung ** &gt; ** Arbeitszeitnachweise ** &gt; ** alle Arbeitszeitnachweise ** | Neuen Arbeitszeitnachweis erstellen. Wählen Sie in der Arbeitszeitnachweisposition im Feld **Juristische Person****FRSI** aus. Wählen Sie im Feld **Projektkennung** das Projekt in FRSI aus. Geben Sie die für jeden Wochentag die Stunden ein. |
| Mrd    | **Arbeitszeitnachweise**-Seite                                                                | Wenn der Workflows ausgeführt wird, buchen Sie den Arbeitszeitnachweis und notieren Sie die Belegnummer.                                                                                                               |

## <a name="example-3-create-and-post-an-intercompany-vendor-invoice"></a>Beispiel 3: Erstellen und Buchen von Intercompany-Kreditorenrechnungen
USSI, die verleihende juristische Person, muss die Intercompacny-Kreditorenrechnung für ein Projekt von FRSI, der ausleihenden juristischen Person, erstellen und buchen. Diese kreditorenrechnung stellt ausgelagerte Arbeit und die Ausgaben dar, die durch von USSI bezahlten Lieferanten durchgeführt wurden. Es gibt zwei Einstiegspunkte für die für diese Aufgabe erforderlichen Schritte.

| Schritt | Einstiegspunkt                                                                                      | Beschreibung                                                                                                                                                                                                                                                                          |
|------|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A:    | ** Kreditor ** &gt; ** Rechnungen ** &gt; ** offene Kreditorenrechnungen ** &gt; ** neuen Kreditorenrechnung ** | Erstellen Sie eine neue Kreditorenrechnung, und geben Sie die für das Projekt von FRSI durchgeführten Dienstleistungen an.                                                                                                                                                                                  |
| Mrd    | Die Seite **Kreditorenrechnung**                                                                      | Geben Sie Positionen für die für FRSI ausgelagerten Dienstleistungen an. Geben Sie auf dem **Positionsdetails**-Inforegister auf der **Projekt**-Registerkarte der Rechnungsposition im Feld **Projektunternehmen** den Wert **FRSI** ein. Geben Sie das Projekt und die entsprechenden Informationen ein. Buchen Sie dann die Kreditorenrechnung. |

## <a name="example-4-create-and-post-the-intercompany-invoice"></a>Beispiel 4: Erstellen und Buchen der Intercompany-Rechnung
USSI, die ausleihende juristischen Person, muss die Intercompany-Rechnung erstellen und buchen. Es gibt zwei Einstiegspunkte für die für diese Aufgabe erforderlichen Schritte.

| Schritt | Einstiegspunkt                                                                                             | Beschreibung                                                                                                                                      |
|------|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| A:    | ** Projektverwaltung und Buchhaltung ** &gt; ** Projektrechnungen ** &gt; ** Intercompany-Debitorenrechnung **  | Klicken Sie auf **Neu**, um die Seite **Intercompany-Rechnung erstellen** zu öffnen.                                                                                  |
| Mrd    | ** Projektverwaltung und Buchhaltung ** &gt; ** Projektrechnungen ** &gt; ** ** Intercompany-Debitorenrechnungen | Auf der Seite **Intercompany-Rechnung erstellen** geben Sie die juristische Person, geben die einzubeziehenden Buchungen ein, und klicken dann auf **Suche**. |
| C:    | ** Projektverwaltung und Buchhaltung ** &gt; ** Projektrechnungen ** &gt; ** ** Intercompany-Debitorenrechnungen | Wählen Sie die zu fakturierenden Buchungen oder klicken Sie auf **Alle wählen**, um alle Buchungen in der Liste zu fakturieren, und klicken Sie dann auf **OK**.                  |
| S    | Die Seite **Intercompany-Rechnung**                                                                       | Der Intercompany-Debitorenrechnungsvorschlag wird angezeigt.                                                                                             |
| E:    | Die Seite **Intercompany-Rechnung**                                                                       | Klicken Sie auf **Buchen**.                                                                                                                                  |

## <a name="example-5-post-the-vendor-invoice-and-invoice-the-customer"></a>Beispiel 5: Buchen der Kreditorenrechnung und Rechnung an den Debitor
Wenn die ausleihende juristische Person USSI die Intercompany-Debitorenrechnung stellt, wird eine entsprechende ausstehende Kreditorenrechnung in der verleihenden juristischen Person FRSI erstellt. Nachdem diese Kreditorenrechnung gebucht ist, stellt auch FRSI die von USSI angegebenen Stunden in Rechnung. Es gibt drei Einstiegspunkte für die für diese Aufgabe erforderlichen Schritte.

| Schritt | Einstiegspunkt                                                                                        | Beschreibung                                                                                                             |
|------|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| A:    | ** Kreditor ** &gt; ** Rechnungen ** &gt; ** ** für Kreditorenrechnungen                            | Überprüfen Sie die Rechnung, um sicherzustellen, dass die Arbeitszeitnachweiswerte enthalten sind, und Buchen Sie die Kreditorrechung.                  |
| Mrd    | ** Projektverwaltung und Buchhaltung ** &gt; ** Projektrechnungen ** &gt; ** ** Projektrechnungsvorschläge | Erstellen Sie eine neue Projektrechnung für das Projekt, und überprüfen Sie, ob die gebuchten Stunden angezeigt werden.            |
| C:    | Die Seite **Projektrechnung**                                                                       | Wählen Sie die Projektrechnung, und klicken Sie auf **Einzelheiten**, um die Kosten- und Umsatzbeträge anzuzeigen. Buchen sie dann die Rechnung. |




