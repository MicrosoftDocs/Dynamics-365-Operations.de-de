---
title: Zurücksetzen von Data Marts FAQ
description: In diesem Thema finden Sie Antworten auf einige häufig gestellte Fragen zum Zurücksetzen des Data Marts.
author: jinniew
ms.date: 06/09/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-05-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 7cd96c7bc698986ef1ef07ca88479a3d49f22924
ms.sourcegitcommit: ecabf43282a3e55f1db40341aa3f3c7950b9e94c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/16/2021
ms.locfileid: "6266608"
---
# <a name="data-mart-resets-faq"></a>Zurücksetzen von Data Marts FAQ

In diesem Thema finden Sie Antworten auf einige häufig gestellte Fragen zum Zurücksetzen des Data Marts. Ein Zurücksetzen des Data Mart kann ein zeitaufwändiger Prozess sein und ist je nach den Umständen möglicherweise nicht die Lösung, die benötigt wird. Daher enthält dieses Thema Informationen über Umstände, unter denen ein Data Mart-Reset hilfreich sein kann, und auch über Umstände, unter denen es unwahrscheinlich ist, dass es hilft.

## <a name="what-is-a-data-mart-reset"></a>Was ist das Zurücksetzen eines Data Marts?

Bei einem Data Mart-Reset werden die Integrationsaufgaben deaktiviert, alle Data Mart-Daten gelöscht und anschließend die Integration wieder aktiviert.

Um sicherzustellen, dass keine alten Daten eingefügt werden, kann ein Data Mart-Reset erst dann gestartet werden, wenn bestehende Aufgaben abgeschlossen sind. Wenn Sie versuchen, den Data Mart zurückzusetzen, bevor alle Aufgaben abgeschlossen sind, erhalten Sie möglicherweise eine Nachricht wie „Das Zurücksetzen des Data Mart konnte aufgrund einer aktiven Aufgabe nicht verarbeitet werden. Bitte versuchen Sie es später erneut.“

## <a name="when-do-i-have-to-do-a-data-mart-reset"></a>Wann muss ich ein Data Mart-Reset durchführen?

Wenn eine oder mehrere der folgenden Aussagen auf Ihre Situation zutreffen, kann Ihre Organisation von einem Data Mart-Reset profitieren:

- Die Anwendungsdatenbank wurde wiederhergestellt.
- Sie haben ein Support-Ticket geöffnet, und ein Support-Techniker hat Sie angewiesen, den Data Mart als Teil einer Fehlerbehebung zurückzusetzen.
 
## <a name="when-is-a-data-mart-reset-inappropriate"></a>Wann ist ein Data Mart-Reset unangebracht?

Im Folgenden sind einige der Umstände aufgeführt, unter denen wir nicht empfehlen, den Data Mart zurückzusetzen:

- Sie haben Leistungsprobleme, die mit der Datensynchronisierung zusammenhängen.
- Sie haben ein wiederkehrendes Rücksetzungsmuster aus einem der folgenden Gründe:

    - **Fehlende Daten** – Wenn Sie feststellen, dass Daten fehlen, eröffnen Sie ein Support-Ticket bei Microsoft, um Ihr Berichtsformat und mögliche Probleme bei der Datensynchronisation zu überprüfen.
    - **Hängengebliebener Integrationszustand**
    - **Veraltete Datensätze** – Veraltete Datensätze allein rechtfertigen nicht unbedingt einen Data Mart Reset. Wenn Sie ein großes Dataset haben, dauert es einige Zeit, bis der Rücksetzungsprozess ausgeführt wird, aber es ist unwahrscheinlich, dass er zu einer Verbesserung führt.

## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a>Verliere ich Berichte, die ich bereits erstellt habe, wenn ich den Data Mart zurücksetze?

Nein. Ihre Berichte sind in SQL-Tabellen gespeichert, die von einem Data Mart-Reset nicht betroffen sind. Wenn Sie befürchten, dass von Ihnen entworfene Berichte verloren gehen, können Sie die Entwürfe, die Sie nicht verlieren möchten, sichern. Um Designs zu sichern, öffnen Sie den Report Designer und gehen Sie zu **Firma \> Firmen \> Bausteine \> Export**.
 
## <a name="do-all-users-have-to-exit-the-system-before-i-can-reset-the-data-mart"></a>Müssen alle Benutzer das System verlassen, bevor ich den Data Mart zurücksetzen kann?

Nein. Die Benutzer können während eines Data Mart-Resets weiter im System arbeiten. Bis das Zurücksetzen abgeschlossen ist, können die Benutzer jedoch nicht auf Berichte zugreifen, die mit Financial Reporter erstellt wurden.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
