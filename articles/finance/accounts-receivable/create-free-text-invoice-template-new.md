---
title: Eine Vorlage für Freitextrechnungen erstellen
description: Verwenden Sie die folgende Prozedur, um eine Vorlage für Freitext-Serienrechnungen zu erstellen.
author: abruer
ms.date: 02/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7baa29ad341bdf7ff874bd7f69cf483b7afc075a
ms.sourcegitcommit: 6102f70d4595d01b90afe5b23dfd8ec2ea030653
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/16/2022
ms.locfileid: "8182508"
---
# <a name="create-a-free-text-invoice-template"></a>Eine Vorlage für Freitextrechnungen erstellen

[!include [banner](../includes/banner.md)]

Für diese Prozedur wird das Demo-Unternehmen USMF verwendet. Die Erfassung ist für den Benutzer bestimmt, der für die Verwaltung und für die Verarbeitung von Debitorenrechnungen zuständig ist.

## <a name="create-a-template"></a>Eine Vorlage erstellen

1. Wechseln Sie zu **Debitoren > Rechnungen > Wiederkehrende Rechnungen > Vorlage für Freitextrechnungen**.
    * Mithilfe dieser Seite können Sie Freitext-Rechnungsvorlagen erstellen, die Rechnungspositionen, Belastungen, eine Buchhaltungsverteilungsvorlage und Sachkontoinformationen enthalten können.  
2. Klicken Sie auf **Neu**, um eine neue Vorlage für Freitextrechnungen zu erstellen.
3. Geben Sie im Feld **Vorlagenname** einen Wert ein.
    * "Vorlagenname" bezeichnet eindeutig eine Freitext-Rechnungsvorlage. Keine zwei Vorlagen können den gleichen "Vorlagennamen" haben.  
4. Geben Sie im Feld **Beschreibung** eine Beschreibung für die Vorlage ein.
5. Erweitern Sie die Registerkarte **Rechnungspositionen**.
6. Geben Sie im Feld **Beschreibung** eine Beschreibung der Rechnungsposition ein.
7. Wählen Sie im Feld **Hauptkonto** ein Umsatzerlöskonto aus.
    * Sie können das Gegenbuchungskonto eines Debitorenkredits für den Gesamtrechnungsbetrag auf der Seite **Kundenbuchungsprofile** auswählen.  
8. Klicken Sie im Feld **Mehrwertsteuergruppe** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
    * Die Mehrwertsteuergruppe für die aktuelle Rechnungsposition ist die standardmäßige Mehrwertsteuergruppe für das Debitorenkonto.  
9. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
10. Wählen Sie im Feld **Artikel-Mehrwertsteuergruppe** die Artikel-Mehrwertsteuergruppe für die aktuelle Rechnungsposition aus.
11. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
12. Geben Sie im Feld **Preis je Einheit** den Einzelpreis für die Rechnungsposition ein oder zeigen ihn an.
    * Dieser Betrag wird mit dem Feld **Menge** multipliziert, um den Betrag der Rechnungsposition zu ermitteln.  
13. Fügen Sie der Vorlage für Freitextrechnungen eine neue Position hinzu.
14. Geben Sie im Feld **Beschreibung** eine Beschreibung der Rechnungsposition ein.
15. Wählen Sie im Feld **Hauptkonto** ein Umsatzerlöskonto aus.
    * Sie können das Gegenbuchungskonto eines Debitorenkredits für den Gesamtrechnungsbetrag auf der Seite **Kundenbuchungsprofile** auswählen.  
16. Klicken Sie im Feld **Mehrwertsteuergruppe** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
    * Die Mehrwertsteuergruppe für die aktuelle Rechnungsposition ist die standardmäßige Mehrwertsteuergruppe für das Debitorenkonto.  
17. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
18. Klicken Sie im Feld **Artikel-Mehrwertsteuergruppe** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
    * Die Artikel-Mehrwertsteuergruppe für die aktuelle Rechnungsposition.  
19. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
20. Die Anzahl von Einheiten für die Rechnungsposition eingeben oder anzeigen.
    * Diese Zahl wird mit dem Wert im Feld "Einzelpreis" multipliziert, um den Betrag der Rechnungsposition zu ermitteln.  
21. Dient zum Eingeben oder Anzeigen des Preises je Einheit für die Rechnungsposition. 
    * Dieser Betrag wird mit dem Wert im Feld **Menge** multipliziert, um den Betrag der Rechnungsposition zu ermitteln.  
22. Zeigen Sie die Buchhaltungsverteilungen für eine einzelne Position und alle untergeordneten Positionen an und ändern Sie diese.
    * Buchhaltungsverteilungen definieren, wie ein Betrag kalkuliert wird, beispielsweise wie Umsatzerlöse, Steuern oder Zuschläge auf einer Freitextrechnung kalkuliert werden.  
23. Aktualisieren Sie die Buchhaltungsverteilungen für die ausgewählte Rechnungsposition.
24. Klicken Sie auf **Schließen**.

## <a name="save-a-free-text-invoice-as-a-template"></a>Eine Vorlage für Freitextrechnungen erstellen
Sie können eine vorhandene Freitextrechnung als Vorlage auch speichern. Wenn Sie **Speichern in Vorlage** auf der Registerkarte **Rechnung** auswählen, geben Sie einen Namen und eine Beschreibung für die Vorlage an. Wenn eine Vorlage mit dem Namen bereits vorhanden ist, sehen Sie eine Benachrichtigung, dass eine Vorlage mit diesem Namen vorhanden ist. Sie können immer noch auf **OK** klicken, um es zu ersetzen. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
