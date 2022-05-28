---
title: Leasingbuchungskonten einrichten
description: In diesem Thema werden die Buchungskonten aufgelistet, die für Anlagenleasing-Transaktionen erforderlich sind, und es wird erläutert, wie Buchungskonten auf der Seite „Leasingbuchungsparameter“ definiert werden.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePostingAccounts
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 147d8cd93f9664039b2004b878dcaff96c8b6ce6
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2022
ms.locfileid: "8726377"
---
# <a name="set-up-lease-posting-accounts"></a>Leasingbuchungskonten einrichten

[!include [banner](../includes/banner.md)]

In diesem Thema werden die Buchungskonten aufgelistet, die für Anlagenleasing-Transaktionen erforderlich sind, und es wird erläutert, wie Buchungskonten auf der Seite **Leasingbuchungsparameter** definiert werden.

Um den Themen 842 zur Kodifizierung von Rechnungslegungsstandards (ASC 842) und dem International Financial Reporting Standard 16 (IFRS 16) zu entsprechen, müssen Sie möglicherweise Konten in Ihrem Kontenplan erstellen. Konten, die Sie zur Einhaltung der ASC- und IFRS-Standards erstellen, sind jedoch keine Anlagenkonten. Gemäß ASC 842 wird eine Analge für das Nutzungsrecht am Leasingobjekt sowohl für Finanzierungsleasing als auch für Ausrüstungs-Leasingverträge erfasst. Diese Mietverträge sind vom Anlagevermögen getrennt. (Sie können ein Nutzungsrecht am Leasingobjekt weiterhin mithilfe des Anlagevermögens verwalten.)

Informationen zum Erstellen von Kontostrukturen finden Sie unter [Erstellen von Kontostrukturen](../general-ledger/tasks/create-account-structures.md). Informationen zum Erstellen eines Hauptkontos finden Sie unter [Erstellen eines Hauptkontos](../general-ledger/tasks/create-main-account.md).

Die folgende Tabelle zeigt Beispiele für Konten, die Sie für Transaktionen mit Leasingobjekten erstellen müssen, sofern diese noch nicht erstellt wurden. Nach IFRS 16 werden die Ausrüstungs-Leasingvertragsbeziehungen weiterhin für geringwertige und kurzfristige Mietverträge verwendet.

| Sachkontonummer | Kontenart  | Kontoname                                          |
|-----------------------|---------------|-------------------------------------------------------|
| 180150                | Anlage         | Nutzungsrecht am Leasingobjekt für Fahrzeuge                                     |
| 180160                | Anlage         | Nutzungsrecht am Leasingobjekt für Gebäude                                    |
| 180250                | Anlage         | Kumulierte Abschreibung – Fahrzeuge                   |
| 180260                | Anlage         | Haben: Kumulierte Abschreibung – Gebäude                  |
| 222300                | Passivposten     | Kurzfristige Verpflichtung – Finanzierungsleasing                |
| 222310                | Bilanz | Kurzfristige Verpflichtung – Ausrüstungs-Leasingverträge              |
| 250200                | Passivposten     | Wechselverbindlichkeiten                                         |
| 250601                | Bilanz | Langfristige Verpflichtung – Finanzierungsleasing                 |
| 250602                | Bilanz | Langfristige Verpflichtung – Ausrüstungs-Leasingverträge               |
| 250606                | Bilanz | Zurückgestellter Mietaufwand                                         |
| 300160                | Bilanz | Nicht ausgeschüttete Gewinne                                     |
| 604500                | Spesen       | Mietsausgaben                                         |
| 604501                | Spesen       | Ausgaben für Ausrüstungs-Leasingverträge von Fahrzeugen – Zinszuwachs  |
| 604502                | Spesen       | Ausgaben für Ausrüstungs-Leasingverträge von Fahrzeugen – Amortisierung        |
| 605200                | Spesen       | Ausgaben für Ausrüstungs-Leasingverträge von Gebäuden – Zinszuwachs |
| 605201                | Spesen       | Ausgaben für Ausrüstungs-Leasingverträge von Gebäuden – Amortisierung       |
| 607101                | Spesen       | Ausgaben für Amortisierung von Fahrzeugleasing                    |
| 607102                | Spesen       | Ausgaben für die Amortisierung von Gebäudemiete                   |
| 607103                | Spesen       | Wertminderungsaufwand – Finanzierungsleasing                   |
| 607104                | Spesen       | Wertminderungsaufwand – Ausrüstungs-Leasingverträge                 |
| 618910                | Spesen       | Mietsaufwand – Finanzierungsleasing                        |
| 618920                | Spesen       | Variable Zahlungen – Finanzierungsleasing                    |
| 618930                | Spesen       | Variable Zahlungen – Ausrüstungs-Leasingverträge                  |
| 800600                | Spesen       | Ausgaben für Mietzins von Fahrzeugen                        |
| 800601                | Spesen       | Ausgaben für Mietzins von Gebäuden                       |
| 801201                | Bilanz | Gewinn und Verlust – Änderung des Mietvertrags                      |

## <a name="configure-posting-accounts"></a>Buchungskonten konfigurieren

Um den erstellten Leasingbüchern und Gruppen Konten zuzuweisen, müssen Sie Parameter für das Anlagenleasing konfigurieren.

1. Wechseln Sie zu **Anlagenleasing \> Einrichtung \> Leasingbuchungsparameter**.
2. Öffnen Sie auf der Registerkarte **Konten** das Inforegister **Leasingkonten**. Bestimmen Sie die Hauptkonten für Finanzierungsleasing- und Ausrüstungs-Leasingverträge entsprechend der **Buchungsart**. Die vorstehende Tabelle zeigt die Konten, die sich auf Ausrüstungs-Leasingverträge und Finanzierungsleasing beziehen.

    > [!NOTE]
    > Für diesen Schritt müssen Sie für jede Buchungsart außer Konten separate Konten für Ausrüstungs-Leasingverträge und Finanzierungsleasing einrichten **Mietaufwand verrechnen** und **Leasing erhöhen/verringern**. Unternehmen, die den Rechnungslegungsrahmen von IFRS 16 einhalten, müssen ein Hauptkonto für Ausrüstungs-Leasingverträge hinzufügen. Das System wird dieses Konto jedoch nicht verwenden, obwohl es ein Pflichtfeld ist, da alle Mietverträge nach IFRS 16 als Finanzierungsleasing klassifiziert sind.
    >[!NOTE]
    > **Leasing erhöhen/verringern** wird als Buchungsart für zusätzliche Anlagenüberlegungen verwendet, einschließlich **Anfängliche direkte Kosten, Mietanreize, Mietvorauszahlungen und Demontagekosten**, aber auf das Hauptkonto des Nutzungsrechts am Leasingobjekt buchen, für das standardmäßig **Leasingobjekt** verwendet wird.        
    
3. Um eine bestimmte Mietgruppe auszuwählen, die dem Hauptkonto entspricht, klicken Sie auf das **Kontocode**-Feld und wählen **Gruppe** aus. Wählen Sie dann im Feld **Konto-/Gruppennummer** die Mietvertragsgruppe aus, die dem Hauptkonto zugewiesen werden soll.
4. Um den im System eingerichteten Verwaltungskosten Kontocodes zuzuweisen, klicken Sie auf das Inforegister **Nebenkosten beim Leasing** im **Kostenart**-Feld und wählen Sie eine Ausgabe aus. Weisen Sie dann die Finanz- und Betriebskonten zu, die für jedes Buch verwendet werden sollen.

    > [!NOTE]
    > Das ausgewählte Finanz- oder Betriebskonto wird belastet, wenn die Rechnung für den geplanten Aufwand gebucht wird.
    > **Mietaufwand verrechnen** wird als Buchungsart für Transaktionen für Nebenkosten beim Leasing verwendet, aber auf ein definiertes **Gegenkonto** in den **Zahlungsplanzeilen der Nebenkosten beim Leasing** in Mietvertragsdetails oder dem Leasingbuchformular gebucht.   


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
