---
title: Häufig gestellte Fragen zur Finanzberichterstellung
description: Dieser Artikel gibt Antwort auf einige häufig gestellte Fragen zur Finanzberichterstellung.
author: jiwo
ms.date: 01/13/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e1b67f86446403933005008a9a1e2cc6739dc516
ms.sourcegitcommit: ecabf43282a3e55f1db40341aa3f3c7950b9e94c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/16/2021
ms.locfileid: "6266632"
---
# <a name="financial-reporting-faq"></a>Häufig gestellte Fragen zur Finanzberichterstellung

Dieser Artikel gibt Antwort auf häufig gestellte Fragen zur Finanzberichterstellung.

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

### <a name="in-dynamics-365-finance"></a>In Dynamics 365 Finance

1. Wechseln Sie zu **Hauptbuch \> Anfragen und Berichte \> Zwischenbilanz** aus.
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
- Wenden Sie sich an den Support, um das Problem zu identifizieren und zu beheben. Möglicherweise sind inkonsistente Daten im System vorhanden. Supporttechniker können Ihnen helfen, dieses Problem auf dem Server zu identifizieren und die spezifischen Daten zu finden, die möglicherweise aktualisiert werden müssen.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
