---
title: Beendigungsvorschlag des Leasingvertrags
description: In diesem Thema wird erläutert, wie Sie einen Mietvertrag zur Kündigung vorschlagen.
author: moaamer
manager: Ann Beebe
ms.date: 1/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetLease
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2021-1-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 144559b14878a44afd8a77648bb5ce1d3ba17832
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2021
ms.locfileid: "5131286"
---
# <a name="propose-a-lease-for-termination"></a>Einen Mietvertrag zur Kündigung vorschlagen

[!include [banner](../includes/banner.md)]

Wenn ein Mietvertag vorzeitig gekündigt wird, kann das Anlagenleasing einen Journaleintrag Eintrag erfassen, um die Leasingverbindlichkeit, das Nutzungsrecht (ROU) und die kumulierten Abschreibungen abzuschreiben und einen Gewinn oder Verlust zu verbuchen. Der Prozess der vorzeitigen Kündigung eines Mietvertrags und die zugehörigen Leasingbücher. Einzelne Leasingbücher werden nicht beendet. In diesem Thema wird die Funktionalität beschrieben, mit der Sie einen Mietvertrag zur Kündigung vorschlagen und den Journaleintrag für die Kündigung des Mietvertrags verarbeiten können.

Wenn ein Mietvertrag nicht als Leasingverhältnis mit zurückgestelltem Mietaufwand eingestuft wird und nicht mit einem Anlagevermögen verbunden ist, erstellt das Assetleasing den folgenden Kündigungsjournaleintrag.

| Transaktion                           | Soll (S) | Haben (H) |
|---------------------------------------|-------------|--------------|
| S Leasingverbindlichkeit                   | X           |              |
| Soll – kumulierte Abschreibung          | X           |              |
| S Gewinn (Verlust) bei Änderung des Mietvertrags | X           |              |
| H Leasingobjekt                       |             | X            |
| H Gewinn (Verlust) bei Änderung des Mietvertrags |             | X            |

Wenn das Leasingbuch als Buch für zurückgestellten Mietaufwand eingestuft ist, schreibt der Eintrag die Bilanz des zurückgestellten Mietaufwands vor der Kündigung in das Gewinn- oder Verlustkonto, wie hier gezeigt.

| Transaktion                           | Soll (S) | Haben (H) | 
|---------------------------------------|-------------|--------------|
| S Zurückgestellter Mietaufwand                     | X           |              |
| H Gewinn (Verlust) bei Änderung des Mietvertrags |             | X            |
| H Zurückgestellter Mietaufwand                     |             | X            |
| S Gewinn (Verlust) bei Änderung des Mietvertrags | X           |              |

Wenn das Leasingbuch mit einem Anlagevermögen verbunden ist, wird das Nutzungsrecht am Leasingobjekt im Anlagevermögen erfasst. Diese Buchhaltung umfasst die Buchhaltung für vorzeitige Kündigungen. Assetleasing erstellt den folgenden Journaleintrag, um die Leasingverbindlichkeit abzuschreiben.

| Transaktion                           | Soll (S) | Haben (H) |
|---------------------------------------|-------------|--------------|
| S Leasingverbindlichkeit                   | X           |              |
| H Gewinn (Verlust) bei Änderung des Mietvertrags |             | X            |

Informationen zur korrekten Entsorgung eines Nutzungsrechts am Leasingobjekt finden Sie unter [Entsorgen eines Anlagevermögens als Ausschuss](../fixed-assets/dispose-of-a-fixed-asset-as-scrap.md).

## <a name="propose-a-lease-for-termination"></a>Einen Mietvertrag zur Kündigung vorschlagen

1. Wechseln Sie zu dem Mietvertrag, der gekündigt werden muss, und wählen Sie im Aktionsbereich die Option **Kündigungsvorschlag**.

    > [!NOTE]
    > Die **Kündigungsvorschlag**-Schaltfläche ist nicht verfügbar, wenn für ein Buch nicht veröffentlichte Journaleinträge vorhanden sind. Bevor Sie den Mietvertrag kündigen können, müssen Sie alle Journaleinträge veröffentlichen oder löschen, die für den Mietvertrag erstellt wurden.

2. Legen Sie im angezeigten Dialogfeld die Felder **Gültigkeitsdatum** und **Buchungsdatum** für den Kündigungsjournaleintrag fest.
3. Wählen Sie **Kündigungsvorschlag**, um den Mietvertrag zur Kündigung vorzuschlagen.
4. Wählen Sie **Mietvertragskündigung buchen**, um den Journaleintrag für die Mietvertragskündigung automatisch zu buchen.
5. Wählen Sie auf der Seite **Mietvertragskündigungen** die Leasing-ID des Mietvertrags aus, das Sie zur Kündigung vorgeschlagen haben, um die Kündigungszeilen anzuzeigen. Die Kündigungszeilen zeigen die Buchwerte des Nutzungsrechts am Leasingobjekt, der Leasingverbindlichkeit, der kumulierten Abschreibungen, des zurückgestellten Mietaufwands (falls zutreffend) und des Gewinns oder Verlusts, die bei Beendigung des Mietvertrags erfasst werden müssen.

Der Mietvertrag kann jetzt gekündigt werden. Der Wert des **Kündigungsstatus**-Felds für das Leasingbuch wird in **Bereit zur Kündigung** geändert. Ab diesem Zeitpunkt können Sie keine Journaleinträge mehr für den Mietvertrag buchen oder ihn anpassen oder beeinträchtigen. 

## <a name="process-leases-that-are-ready-for-termination"></a>Mietverträge verarbeiten, die zur Kündigung bereit sind

Führen Sie die folgenden Schritte aus, um kündigungsbereite Mietverträge zu verarbeiten und den Kündigungsjournaleintrag zu buchen.

1. Wählen Sie auf der Seite **Mietvertragskündigungen** den zu verarbeitenden Mietvertrag und dann **Kündigen** aus.
2. Im angezeigten Dialogfeld wählen Sie **OK** aus.

Das System bucht den Kündigungsjournaleintrag. Das **Leasingstatus**-Feld für das Leasingbuch wird auf **Gekünsigt** festgelegt, und das **Status des Kündigungsvorschlags**-Feld wird auf **Abgeschlossen** festgelegt.

## <a name="reverse-a-lease-termination"></a>Kündigung eines Mietvertrags rückgängig machen

Führen Sie den folgenden Schritt aus, um einen Journaleintrag für die Beendigung eines Mietvertrags rückgängig zu machen und einen gekündigten Mietvertrag zu öffnen.

- Wählen Sie auf der Seite **Mietvertragskündigungen** den rückgängig zu machenden beendeten Mietvertrag und dann **Kündigung rückgängig machen** aus.

Das System macht den Kündigungsjournaleintrag rückgängig. Das **Leasingstatus**-Feld für das Leasingbuch wird auf **Öffnen** festgelegt. Der Mietvertrag erscheint nicht mehr auf der **Mietvertragskündigungen**-Seite und kann erneut zur Kündigung vorgeschlagen werden.

## <a name="example-of-a-lease-termination"></a>Beispiel für eine Kündigung des Mietvertrags

In diesem Beispiel ist der Mietvertrag einer nicht spezialisierte Anlage zugeordnet, und es werden weder das Eigentum der Anlage noch dem Mieter die Option zum Kauf der Anlage gewährt.

### <a name="setup"></a>Einstellung

Die folgenden Tabellen zeigen die Werte, die auf den Registerkarten **Allgemeines** und **Zahlungspläne** für die Mietverträge festgelegt sind, die in dem Beispiel verwendet werden.

**Registerkarte „Allgemeines“**

| Feld                      | Wert            |
|----------------------------|------------------|
| Zeitwert der Anlage    | 600,000          |
| Währung                   | USD              |
| Anfängliche direkte Kosten       | 1.000            |
| Zinssatz für Neukredit | 7 %               |
| Aufzinsungsintervall       | Jährlich         |
| Nutzungsdauer für Anlagen (Monate) | 600              |
| Annuitätstyp               | Normale Annuität |
| Anfangsdatum          | 01.01.2019         |

**Registerkarte „Zahlungsplanpositionen“**

| Feld             | Wert      |
|-------------------|------------|
| Startdatum        | 01.01.2019   |
| Periodenintervall   | Monatlich    |
| Perioden           | 120        |
| Enddatum          | 31.12.2028 |
| Zahlungshäufigkeit | Jährlich   |
| Zahlungsbetrag    | 10,000     |

### <a name="steps-for-terminating-the-lease"></a>Schritte zur Kündigung des Mietvertrags

1. Nachdem Sie den Mietvertrag wie oben in diesem Thema beschrieben erstellt haben, gehen Sie zum Leasingbuch und bestätigen Sie den Zahlungsplan. Buchen Sie dann den Journaleintrag der erstmaligen Erfassung . Das anfängliche Nutzungsrecht am Leasingobjekt ist 71.235,81 USD und die Leasingverbindlichkeit sollte 70.235,81 USD sein. In diesem Beispiel wurde der Mietvertrag gemäß ASC 842 als Ausrüstungs-Leasingvertrag unter Thema 842 zur zur Kodifizierung von Rechnungslegungsstandards (ASC 842) klassifiziert.
2. Führen Sie den Batch für Erfassungen dreimal aus, um den Ablauf von drei Jahren für die Mietzahlungen, Zinsaufwendungen und Abschreibungskosten zu simulieren.
3. Nachdem Sie alle drei Batch-Aufträge ausgeführt haben, kehren Sie zum Leasingbuch zurück und öffnen Sie die Tabellen für Verbindlichkeiten und Anlagentransaktionen, um den aktuellen Buchwert des Nutzungsrechts am Leasingobjekt und der Leasingverbindlichkeit anzuzeigen. Nach drei Jahren sollte der Anlagenwert ungefähr -53.893,00 USD betragen, und der Wert des Vermögenswerts sollte ungefähr 54.593,00 USD betragen.

    Nach Ablauf der drei Jahre vereinbaren das Unternehmen und der Vermieter einvernehmlich, den Mietvertrag zu kündigen. Daher müssen Sie jetzt den Mietvertrag kündigen.

4. Wechseln Sie zu dem Mietvertrag, der gekündigt werden muss, und wählen Sie im Aktionsbereich die Option **Kündigungsvorschlag**. 
5. Geben Sie in dem Dialogfeld, das angezeigt wird, in den Feldern **Gültigkeitsdatum** und **Buchungsdatum** **01.01.2021** ein.
6. Wählen Sie **Kündigungsvorschlag**, um den Mietvertrag zur Kündigung vorzuschlagen.

    Die **Mietvertragskündigungen**-Seite erscheint und zeigt den Mietvertrag, der gekündigt wird.

7. Um die Kündigungszeilen anzuzeigen, wählen Sie die Leasing-ID des Mietvertrags aus, den Sie zur Kündigung vorgeschlagen haben. Die Kündigungszeilen zeigen die Buchwerte des Mietvertrags. Die folgende Tabelle zeigt, wie diese Werte für dieses Beispiel lauten sollten. 

    | Feld                                                 | Wert      |
    |-------------------------------------------------------|------------|
    | Buchungsbilanz der Verbindlichkeit in Transaktionswährung | 53.892,89 USD |
    | Nutzungsrecht am Leasingobjekt in Transaktionswährung            | 71.235,81 USD |
    | Kumulierte Abschreibung in Transaktionswährung      | 16.642,92 USD |
    | Gewinn (Verlust) in Transaktionswährung                   | -700,00 USD   |

8. Um den Kündigungsjournaleintrag zu buchen, wählen Sie auf der Seite **Mietvertragskündigungen** **Kündigung** aus.
9. Im angezeigten Dialogfeld wählen Sie **OK** aus.
10. Um den Kündigungsjournaleintrag anzuzeigen, der erstellt und gebucht wurde, rufen Sie das Leasingjournal der Anlage im Leasingbuch auf. Die folgende Tabelle zeigt, wie dieser Eintrag für dieses Beispiel lauten sollten.

    | Transaktion                           | Soll (S) | Haben (H) |
    |---------------------------------------|-------------|--------------|
    | S Leasingverbindlichkeit                   | 53,892.89   |              |
    | Soll – kumulierte Abschreibung          | 16,642.92   |              |
    | S Gewinn (Verlust) bei Änderung des Mietvertrags | 700.00      |              |
    | H Leasingobjekt                       |             | 71,235.81    |

11. Um den Nettoeffekt der Kündigung anzuzeigen, bei dem das Nutzungsrecht am Leasingobjekt und die Leasingverbindlichkeit 0 (Null) betragen, öffnen Sie die Transaktionstabellen für Verbindlichkeiten und Anlagen.

Der Leasingstatus sollte jetzt **Gekündigt** sein. Für diesen Mietvertrag werden keine zusätzlichen Journaleinträge gebucht, es sei denn, die Kündigung wird rückgängig gemacht.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]