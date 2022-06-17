---
title: Häufig gestellte Fragen zum Financial Reporting
description: Dieser Artikel gibt Antwort auf einige häufig gestellte Fragen zur Finanzberichterstellung.
author: jinniew
ms.date: 07/07/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 5981946a4bba2c58402f4cf566bfa008de67363b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901369"
---
# <a name="financial-reporting-faq"></a>Häufig gestellte Fragen zum Financial Reporting

Dieser Artikel gibt Antwort auf einige häufig gestellte Fragen zu Financial reporting.

## <a name="how-do-i-restrict-access-to-a-report-by-using-tree-security"></a>Wie beschränke ich den Zugriff auf einen Bericht mithilfe der Baumstruktursicherheit?

Das folgende Beispiel zeigt, wie der Zugriff auf einen Bericht mithilfe der Baumstruktursicherheit eingeschränkt werden kann.

Auf den **Bilanzbericht** des USMF-Demounternehmens sollen nicht alle Benutzer der Finanzberichterstellung zugreifen dürfen. Mithilfe der Baumstruktursicherheit können Sie den Zugriff auf einzelne Berichte so einschränken, damit nur bestimmte Benutzer Zugriff erhalten.

1. Melden Sie sich bei Financial Reporter Report Designer an.
2. Wählen Sie **Datei \> Neu \> Baumdefinition** aus, um eine neue Baumdefinition zu erstellen.
3. Doppeltippen oder -klicken Sie in der Spalte **Einheitssicherheit** auf **Zusammenfassung**.
4. Wählen Sie **Benutzer und Gruppen** aus.
5. Wählen Sie die Benutzer oder Gruppen aus, die auf diesen Bericht zugreifen müssen.
6. Wählen Sie **Speichern** aus.
7. Ergänzen Sie die neue Baumdefinition in der Berichtsdefinition.
8. Wählen Sie in der Baumdefinition **Einstellung** aus. Wählen Sie dann unter **Auswahl der Berichtseinheit** die Option **Alle Einheiten einschließen** aus.

## <a name="how-do-i-identify-which-accounts-dont-match-my-balances"></a>Wie finde ich heraus, welche Konten nicht mit meinen Salden übereinstimmen?

Bei einem Bericht, in dem die Salden nicht übereinstimmen, verwenden Sie die folgenden Verfahren, um die einzelnen Konten und Abweichungen zu ermitteln.

### <a name="in-financial-reporter-report-designer"></a>In Financial Reporter Report Designer

1. Erstellen Sie eine neue Zeilendefinition.
2. Wählen Sie **Bearbeiten \> Zeilen aus Dimensionen einfügen** aus.
3. Wählen Sie **MainAccount** aus.
4. Wählen Sie **OK** aus.
5. Speichern Sie die Zeilendefinition.
6. Erstellen Sie eine neue Spaltendefinition.
7. Erstellen Sie eine neue Berichtsdefinition.
8. Wählen Sie **Einstellungen** aus, und deaktivieren Sie diese Option.
9. Erstellen Sie den Bericht. 
10. Exportieren Sie den Bericht in Microsoft Excel.

### <a name="in-dynamics-365-finance"></a>In Dynamics 365 Finance

1. Wechseln Sie zu **Hauptbuch \> Anfragen und Berichte \> Zwischenbilanz**.
2. Stellen Sie die folgenden Felder ein:

    - **Ab Datum** – Geben Sie das Startdatum des Geschäftsjahres ein.
    - **Bis Datum** – Geben Sie das Datum ein, zu dem der Bericht erstellt wird.
    - **Finanzdimension** – Setzen Sie dieses Feld auf **Hauptkonto festgelegt**.

3. Wählen Sie **Berechnen** aus.
4. Exportieren Sie den Bericht in Excel.

Nun sollten sich die Daten aus dem Excel-Bericht in Financial Reporter in den Bericht zur **Zwischenbilanz** kopieren lassen, damit Sie die Spalten zur **Abschlussbilanz** vergleichen können.

## <a name="when-i-design-a-report-in-report-designer-or-when-i-generate-a-financial-report-i-received-the-following-message-the-operation-could-not-be-completed-due-to-a-problem-in-the-data-provider-framework-how-should-i-respond"></a>Beim Entwerfen eines Berichts im Report Designer oder beim Generieren eines Finanzberichts erhalten ich die folgende Meldung: „Der Vorgang konnte aufgrund eines Problems im Datenanbieter-Framework nicht abgeschlossen werden.“ Wie soll ich reagieren?

Die Nachricht weist darauf hin, dass ein Fehler aufgetreten ist, als das System versucht hat, Finanzmetadaten aus dem Data Mart abzurufen, während Sie die Finanzberichterstellung verwendet haben. Es gibt zwei Möglichkeiten, auf dieses Problem zu reagieren:

- Überprüfen Sie den Integrationsstatus der Daten, indem Sie in Report Designer zu **Extras \> Integrationsstatus** wechseln. Wenn die Integration unvollständig ist, warten Sie, bis sie abgeschlossen ist. Wiederholen Sie dann den Vorgang, bei dem Sie die Nachricht erhalten haben.
- Wenden Sie sich an den Support, um das Problem zu identifizieren und zu beheben. Möglicherweise sind inkonsistente Daten im System vorhanden. Supporttechniker können Ihnen helfen, das Problem auf dem Server zu ermitteln und die Daten zu finden, die ggf. aktualisiert werden müssen.

## <a name="how-does-the-selection-of-historical-rate-translation-affect-report-performance"></a>Wie wirkt sich die Auswahl der Umrechnung historischer Kurse auf die Leistung bei der Berichterstellung aus?

Historische Kurse werden in der Regel bei Konten im Zusammenhang mit einbehaltenen Gewinnen, Liegenschaften, Werken und Maschinen sowie Eigenkapital verwendet. Je nach den Richtlinien des US-amerikanischen Financial Accounting Standards Board (FASB) oder den US-amerikanischen Rechnungslegungsvorschriften (US-GAAP) können historische Kurse erforderlich sein. Weitere Informationen finden Sie unter [Währungsfunktionen in der Finanzberichterstellung](financial-reporting-currency-capability.md).

## <a name="how-many-types-of-currency-rate-are-there"></a>Wie viele Währungskurstypen gibt es?

Es gibt drei Typen:

- **Aktueller Kurs**: Dieser Typ wird üblicherweise bei Bilanzkonten verwendet. Er ist auch als *Devisenkassakurs* bekannt und kann der Kurs am letzten Tag des Monats oder der Kurs zu einem anderen vorab festgelegten Datum sein.
- **Durchschnittskurs**: Dieser Typ wird üblicherweise bei Gewinn- und Verlustkonten verwendet. Der Durchschnittskurs kann entweder als einfacher Durchschnitt oder gewichteter Durchschnitt festgelegt werden.
- **Historischer Kurs**: Dieser wird in der Regel bei Konten im Zusammenhang mit einbehaltenen Gewinnen, Liegenschaften, Werken und Maschinen sowie Eigenkapital verwendet. Diese Konten können je nach den Richtlinien von FASB oder US-GAAP erforderlich sein.

## <a name="how-does-historical-currency-translation-work"></a>Wie funktioniert die historische Währungsumrechnung?

Kurse hängen vom Transaktionsdatum ab. Das heißt, jede Transaktion wird individuell anhand des nächsten Wechselkurses umgerechnet.

Bei der historischen Währungsumrechnung können anstelle individueller Transaktionsangaben die vorab berechneten Periodensalden verwendet werden. Diese Funktionsweise unterscheidet sich von der Umrechnung aktueller Kurse.

## <a name="how-does-historical-currency-translation-affect-performance"></a>Wie wirkt sich die historische Währungsumrechnung auf die Leistung aus?

Bei der Aktualisierung von Berichtsdaten kann es zu Verzögerungen kommen, weil die Beträge durch Überprüfung der Transaktionsangaben erneut berechnet werden müssen. Diese Verzögerung tritt immer dann auf, wenn Kurse aktualisiert oder weitere Transaktionen gebucht werden. Werden beispielsweise tausende Konten mehrmals am Tag zur historischen Umrechnung eingerichtet, kann es zu einer Verzögerung von bis zu einer Stunde kommen, bevor die Berichtsdaten aktualisiert werden. Bei weniger Konten dauert die Verarbeitung von Änderungen im Bericht mitunter nur wenige Minuten.

Auch bei der Erstellung von Berichten mithilfe der Währungsumrechnung bei Konten mit historischem Typ kommt es zu zusätzlichen Berechnungen pro Transaktion. Je nach Anzahl der Konten kann die Berichterstellung doppelt so lange dauern.

## <a name="what-are-the-estimated-data-mart-integration-intervals"></a>Was sind die geschätzten Data Mart-Integrationsintervalle?

Financial Reporter kopiert mithilfe von 16 Vorgängen Daten aus Dynamics 365 Finance in die Datenbank von Financial Reporter. Die folgende Tabelle enthält diese 16 Aufgaben sowie das Intervall, das angibt, wie oft jeder Vorgang ausgeführt wird. Die Intervalle können nicht geändert werden.

| Name                                                       | Intervall | Intervallzeitmessung |
|------------------------------------------------------------|----------|-----------------|
| AX 2012 Kontokategorien nach Kontokategorie            | 41       | Minuten         |
| AX 2012-Konten nach Konto                                | 7        | Minuten         |
| AX 2012-Unternehmen nach Unternehmen                               | 300      | Sekunden         |
| AX 2012-Unternehmen nach Organisation                          | 23       | Minuten         |
| AX 2012-Dimensionskombinationen nach Dimensionskombination    | 1        | Minuten         |
| AX 2012-Dimensionswerte nach Dimensionswert                | 11       | Minuten         |
| AX 2012-Dimensionen nach Dimension                            | 31       | Minuten         |
| AX 2012-Wechselkurse nach Wechselkurs                    | 17       | Minuten         |
| AX 2012-Geschäftsjahr nach Geschäftsjahr                        | 13       | Minuten         |
| AX 2012-Hauptbuchtransaktionen nach Fakt                | 1        | Minuten         |
| AX 2012-Organisationshierarchien nach Struktur                   | 3.600    | Sekunden         |
| AX 2012-Szenarien nach Szenario                              | 29       | Minuten         |
| AX 2012-Transaktionstyp-Qualifizierer nach Faktentyp-Qualifizierer | 19       | Minuten         |
| Wartungsaufgabe                                           | 1        | Minuten         |
| MR-Berichtsdefinitionen nach AX7-Finanzberichten             | 45       | Sekunden         |
| MR-Berichtsversionen nach AX-Finanzberichtsversionen         | 45       | Sekunden         |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
