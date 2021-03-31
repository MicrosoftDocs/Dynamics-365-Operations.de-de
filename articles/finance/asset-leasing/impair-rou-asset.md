---
title: Wertminderung bei Nutzungsrechten an Leasingobjekten
description: In diesem Thema wird die Funktionalität beschrieben, mit der eine Wertminderung erfasst und der Zeitplan für die Abschreibung von Anlagen eines Ausrüstungs-Leasingverhältnisses des Themas 842 zur Kodifizierung von Rechnungslegungsstandards (ASC 842) angepasst wird.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 3b648075a681fb01720149aac4f479dccf963489
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5229525"
---
# <a name="impair-right-of-use-assets"></a>Wertminderung bei Nutzungsrechten an Leasingobjekten

[!include [banner](../includes/banner.md)]

Wenn der Buchwert eines Nutzungsrechts am Leasingobjekt nicht erzielbar ist, müssen Sie möglicherweise prüfen, ob die Anlage wertgemindert ist. Wenn Sie feststellen, dass der Vermögenswert wertgemindert ist, kann Analgenleasing die Wertminderung erfassen und den Abschreibungsplan entsprechend anpassen. In diesem Thema wird die Funktionalität beschrieben, mit der eine Wertminderung erfasst und der Zeitplan für die Abschreibung eines Ausrüstungs-Leasingverhältnisses des Themas 842 zur Kodifizierung von Rechnungslegungsstandards (ASC 842) angepasst wird. Die gleiche Methode gilt auch für Mietverträge nach dem International Financial Reporting Standard 16 (IFRS 16).

Der verbleibende Restbetrag des Nutzungsrecht am Leasingobjekt wird linear für die Anzahl der verbleibenden Perioden abgeschrieben, unabhängig davon, ob der Mietvertrag nach IFRS 16 als Finanzierungsleasing oder nach ASC 842 als Operating-Leasing klassifiziert wurde.

## <a name="impair-an-rou-asset"></a>Wertminderung eines ROU-Vermögenswerts

1. Gehen Sie zum wertgeminderten Mietvertrag und wählen Sie **Bücher**.
2. Wählen Sie im Aktivitätsbereich **Dauerhafte Wertminderung** aus.
3. In dem Dialogfeld, das angezeigt wird, geben Sie in das Feld **Wertminderungsbetrag** den Betrag der Wertminderung der Anlage ein. Um das Nutzungsrecht am Leasingobjekt zu verringern, sollten Sie einen positiven Wert eingeben.
4. In dem Feld **Transaktionsdatum** geben Sie das Datum ein, an dem die Wertminderungsbuchung gebucht werden soll.
5. In dem Feld **Verbleibende Zeiträume** geben Sie die verbleibende Anzahl der zu amortisierenden Monate ein.
6. Aktivieren Sie den **Buchen**-Parameter, wenn das System den Journaleintrag für den Wertminderungsaufwand automatisch buchen soll. Wenn Sie diesen Parameter deaktiviert lassen, erstellt das System den Eintrag, bucht ihn jedoch nicht. Sie können dann den Eintrag aus der Seite **Anlagenleasingerfassungen** buchen.
7. Stellen Sie die **Vorschau vor der Buchung**-Option auf **Ja**, um den vorgeschlagenen Eintrag anzuzeigen, bevor er erstellt oder gebucht wird.
8. Stellen Sie die **Buch schließen**-Option auf **Ja**, um das Leasingbuch zu schließen. Sie können diese Aktion nicht rückgängig machen. Einträge können nicht für geschlossene Mietverträge gebucht werden, und geschlossene Mietverträge können nicht angepasst werden.
9. Wählen Sie **OK**, um den Wertminderungseintrag zu erstellen oder zu buchen.
10. Um den wertgeminderten Anlagenabschreibungsplan anzuzeigen, öffnen Sie die Seite Anlagenabschreibungsplan für dieses Mietvertragsbuch. Die Anlage wird nun linear über die Anzahl der Monate abgeschrieben, die Sie im Feld **Verbleibende Zeiträume** eingegeben haben.
11. Um den Journaleintrag für den Wertminderungsaufwand anzuzeigen, wählen Sie **Anlagenleasingerfassung** im Aktionsbereich des wertgeminderten Mietvertragsbuchs aus. Das System erstellt einen Journaleintrag, der das Buchungskonto für Wertminderungsaufwendungen belastet und das Buchungskonto für Mietanlagen gutschreibt.
12. Um den neuen Buchwert des Nutzungsrechts am Leasingobjekt anzuzeigen, wählen Sie **Anlagentransaktionen** im Aktionsbereich des Mietvertragsbuchs aus.

## <a name="example-of-rou-asset-impairment"></a>Beispiel für eine Wertminderung des Nutzungsrechts am Leasingobjekt

In diesem Beispiel handelt es sich bei dem Mietvertrag um eine nicht spezialisierte Anlage, die weder das Eigentum überträgt noch dem Mieter die Kaufoption gewährt.

### <a name="setup"></a>Einstellung

Die folgenden Tabellen zeigen die Werte, die auf den Registerkarten **Allgemeines** und **Zahlungspläne** für die Mietverträge festgelegt sind, die in dem Beispiel verwendet werden.

**Registerkarte „Allgemeines“**

| Feld                      | Wert            |
|----------------------------|------------------|
| Zeitwert der Anlage    | 600,000          |
| Zinssatz für Neukredit | 7 %               |
| Aufzinsungsintervall       | Jährlich         |
| Nutzungsdauer für Anlagen (Monate) | 600              |
| Annuitätstyp               | Normale Annuität |
| Anfangsdatum          | 01.01.2019       |

**Registerkarte „Zahlungsplanpositionen“**

| Feld             | Wert      |
|-------------------|------------|
| Startdatum        | 01.01.2019   |
| Periodenintervall   | Monatlich    |
| Perioden           | 120        |
| Enddatum          | 31.12.2028 |
| Zahlungshäufigkeit | Jährlich   |
| Zahlungsbetrag    | 10,000     |

### <a name="steps"></a>Schritte

1. Nachdem Sie den Mietvertrag wie oben in diesem Thema beschrieben erstellt haben, gehen Sie zum Leasingbuch und bestätigen Sie den Zahlungsplan. Buchen Sie dann den Journaleintrag der erstmaligen Erfassung . Das anfängliche Nutzungsrecht am Leasingobjekt und Leasingverbindlichkeit sollte 70.235,81 USD sein. In diesem Beispiel wurde der Mietvertrag gemäß ASC 842 als Ausrüstungs-Leasingvertrag klassifiziert.
2. Führen Sie den Batch für Erfassungen dreimal aus, um den Ablauf von drei Jahren für die Mietzahlungen, Zinsaufwendungen und Abschreibungskosten zu simulieren.
3. Nachdem Sie alle drei Batch-Aufträge ausgeführt haben, kehren Sie zum Leasingbuch zurück und öffnen Sie die Tabellen für Verbindlichkeiten und Anlagentransaktionen, um den aktuellen Buchwert des Nutzungsrechts am Leasingobjekt und der Leasingverbindlichkeit anzuzeigen. Nach drei Jahren sollte der Anlagenwert ungefähr -53.893,00 USD betragen, und der Wert des Vermögenswerts sollte ungefähr 53.893,00 USD betragen. 

    Nach drei Jahren führt das Unternehmen Wertminderungstests durch und stellt fest, dass das Nutzungsrecht am Leasingobjekt eine Wertminderung von 35.000 USD aufweist. Sie müssen diese Wertminderung jetzt erfassen.
    
4. Gehen Sie zum Leasingbuch und wählen Sie dann im Aktionsbereich **Wertminderung**.
5. Geben Sie auf der **Wertminderungsparameter**-Seite die folgenden Details ein.

    | Feld                  | Wert    |
    |------------------------|----------|
    | Betrag der dauerhaften Wertminderung      | 35,000   |
    | Transaktionsdatum       | 01.01.2022 |
    | Verbleibende Perioden      | 84       |
    | Buchen                   | Ja      |
    | Vorschau vor dem Buchen anzeigen | Nr.       |
    | Buch schließen             | Nr.       |

6. Ein Journaleintrag für Wertminderungsaufwand wurde erstellt und gebucht. Um diesen anzuzeigen, gehen Sie zur Leasingerfassung der Anlage im Leasingbuch. Beachten Sie, dass der Betrag der Wertminderung dem Buchungskonto für Wertminderungsaufwendungen belastet und das Buchungskonto für Nutzungsrecht am Leasingobjekt gutgeschrieben wurde.
7. Um den Nettoeffekt der Wertminderung anzuzeigen, gehen Sie zu den Tabellen für Verbindlichkeiten und Anlagentransaktionen. Beachten Sie, dass der Wertminderungsaufwand das Nutzungsrecht am Leasingobjekt verringert hat, der Buchwert der Leasingverbindlichkeit sich jedoch nicht geändert hat.

Die Wertminderung hat einen weiteren Effekt, den Sie berücksichtigen sollten. Da der Betrag des Nutzungsrechts am Leasingobjekt jetzt viel geringer ist als die Leasingverbindlichkeit, muss der Betrag anders als zuvor abgeschrieben werden. Insbesondere wird die Anlage jetzt während der verbleibenden 84 Monate des Mietvertrags ab dem Transaktionsdatum linear abgeschrieben.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]