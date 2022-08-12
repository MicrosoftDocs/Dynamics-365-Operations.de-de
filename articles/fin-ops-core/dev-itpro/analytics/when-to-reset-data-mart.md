---
title: Zurücksetzen von Data Marts FAQ
description: In diesem Artikel finden Sie Antworten auf einige häufig gestellte Fragen zum Zurücksetzen des Data Marts.
author: jinniew
ms.date: 03/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-05-06
ms.dyn365.ops.version: 10.0.15
ms.search.form: ''
ms.openlocfilehash: 6cb418c331f0ad260f0c370b87404028e5a953f1
ms.sourcegitcommit: 3c4dd125ed321af8a983e89bcb5bd6e5ed04a762
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/28/2022
ms.locfileid: "9205825"
---
# <a name="data-mart-resets-faq"></a>Zurücksetzen von Data Marts FAQ

In diesem Artikel finden Sie Antworten auf einige häufig gestellte Fragen zum Zurücksetzen des Data Marts. Ein Zurücksetzen des Data Mart kann ein zeitaufwändiger Prozess sein und ist je nach den Umständen möglicherweise nicht die Lösung, die benötigt wird. Daher enthält dieser Artikel Informationen über Umstände, unter denen ein Data Mart-Reset hilfreich sein kann, und auch über Umstände, unter denen es unwahrscheinlich ist, dass es hilft.

## <a name="what-is-a-data-mart-reset"></a>Was ist das Zurücksetzen eines Data Marts?

Bei einem Data Mart-Reset werden die Integrationsaufgaben deaktiviert, alle Data Mart-Daten gelöscht und anschließend die Integration wieder aktiviert.

Um sicherzustellen, dass keine alten Daten eingefügt werden, kann ein Data Mart-Reset erst dann gestartet werden, wenn bestehende Aufgaben abgeschlossen sind. Wenn Sie versuchen, den Data Mart zurückzusetzen, bevor alle Aufgaben abgeschlossen sind, erhalten Sie möglicherweise eine Nachricht wie „Das Zurücksetzen des Data Mart konnte aufgrund einer aktiven Aufgabe nicht verarbeitet werden. Bitte versuchen Sie es später erneut.“

## <a name="when-do-i-have-to-do-a-data-mart-reset"></a>Wann muss ich ein Data Mart-Reset durchführen?

Wenn eine oder mehrere der folgenden Aussagen auf Ihre Situation zutreffen, kann Ihre Organisation von einem Data Mart-Reset profitieren:

- **Die Anwendungsdatenbank wurde wiederhergestellt**
- **Sie haben ein Support-Ticket geöffnet**: Ein Support-Techniker hat Sie angewiesen, den Data Mart im Rahmen einer Problembehebung zurückzusetzen.
- **Großer Prozentsatz veralteter Datensätze**: Veraltete Datensätze allein rechtfertigen nicht unbedingt, einen Data Mart zurückzusetzen. Ein hoher Prozentsatz an veralteten Daten kann die Gesamtleistung der Berichtgenerierung und Integration beeinträchtigen und zusätzlichen Speicherplatz in der Datenbank beanspruchen. Wir empfehlen, dass Sie einen Data Mart zurücksetzen, um die veralteten Daten zu entfernen, wenn mehr als 80 % veraltete Daten im Data Mart vorhanden sind.
 
> [!NOTE]
> Der Vorgang des Zurücksetzens eines Data Mart wird von der Anzahl der Hauptbuch- und Budgetbuchungen in Ihrer Datenbank beeinflusst. Abhängig von der Anzahl der Transaktionen in Ihrem System kann ein Zurücksetzen des Data Mart in nur 15 Minuten abgeschlossen sein oder bis zu vier Stunden dauern. Sollte Ihr Zurücksetzen jedoch länger als vier Stunden dauern, empfehlen wir Ihnen, sich an den Support zu wenden.
 
## <a name="when-is-a-data-mart-reset-inappropriate"></a>Wann ist ein Data Mart-Reset unangebracht?

Im Folgenden sind einige der Umstände aufgeführt, unter denen wir nicht empfehlen, den Data Mart zurückzusetzen:

- Sie haben Leistungsprobleme bei der Datenintegration.
- Ihre Financial Reporter Integration ist nicht aktiviert. 

    - Dies bedeutet, dass die Daten des Hauptbuchs nicht mehr mit Ihrem Financial Reporting Datamart synchronisiert werden. Ihr Financial Reporter erhält möglicherweise keine aktuellen Zahlen für Ihre Finanzberichte. Dies tritt typischerweise auf, wenn Sie Financial Reporter längere Zeit nicht mehr verwendet haben.
    - Sie werden aufgefordert, die Integration zu aktivieren, indem Sie den Data Mart zurücksetzen. Sie können fortfahren, indem Sie **Ja** wählen. Sie haben auch die Möglichkeit, den Data Mart zu einem späteren Zeitpunkt zurückzusetzen. Nachdem die Integration aktiviert wurde, werden die Daten Ihres Hauptbuchs in Financial Reporter erneut synchronisiert. 
- Sie haben ein wiederkehrendes Rücksetzungsmuster aus einem der folgenden Gründe:

    - **Fehlende oder unerwartete Daten im Bericht**: Wenn Sie feststellen, dass Daten fehlen, eröffnen Sie ein Support-Ticket bei Microsoft, um Ihr Berichtsformat und mögliche Probleme bei der Datensynchronisation zu überprüfen.
    - **Stau im Status der Integration** - Wenn Sie bemerken, dass der Status der Integration im Ausführen stecken bleibt, kann dies an einem großen Volumen an Transaktionen im System liegen. Dieser Status wird sich selbst auflösen. Wenn Sie jedoch bemerken, dass der Integrationsstatus länger als vier Stunden festhängt, eröffnen Sie ein Support-Ticket bei Microsoft. 
   
## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a>Verliere ich Berichte, die ich bereits erstellt habe, wenn ich den Data Mart zurücksetze?

Nein. Ihre Berichte sind in SQL-Tabellen gespeichert, die von einem Data Mart-Reset nicht betroffen sind. Wenn Sie befürchten, dass von Ihnen entworfene Berichte verloren gehen, können Sie die Entwürfe, die Sie nicht verlieren möchten, sichern. Um Designs zu sichern, öffnen Sie den Report Designer und gehen Sie zu **Firma \> Firmen \> Bausteine \> Export**.
 
## <a name="do-all-users-have-to-exit-the-system-before-i-can-reset-the-data-mart"></a>Müssen alle Benutzer das System verlassen, bevor ich den Data Mart zurücksetzen kann?

Nein. Die Benutzer können während eines Data Mart-Resets weiter im System arbeiten. Bis das Zurücksetzen abgeschlossen ist, können die Benutzer jedoch nicht auf Berichte zugreifen, die mit Financial Reporter erstellt wurden.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
