---
title: Zeitpunkt für das Zurücksetzen eines Data Mart
description: In diesem Thema werden die Umstände aufgeführt, die durch das Zurücksetzen eines Data Mart verbessert werden könnten, und die Umstände, unter denen das Zurücksetzen Ihres Data Mart wahrscheinlich nicht hilfreich ist.
author: jinniew
ms.date: 05/06/2021
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
ms.openlocfilehash: bc2c4ee490f3bebd6e7c91609a06f8dfedfcb628
ms.sourcegitcommit: 5916ea2a94ab9af7aac21f0fc44e194d5ce82917
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2021
ms.locfileid: "5988991"
---
# <a name="when-to-reset-a-data-mart"></a>Zeitpunkt für das Zurücksetzen eines Data Mart

Das Zurücksetzen eines Data Mart kann zeitaufwändig sein. Abhängig von den Umständen ist diese Aktion möglicherweise nicht die passende Lösung. In diesem Thema werden die Umstände aufgeführt, die durch das Zurücksetzen eines Data Mart verbessert werden könnten, sowie die Umstände, unter denen das Zurücksetzen Ihres Data Mart wahrscheinlich nicht hilfreich ist.  

## <a name="when-do-i-need-to-do-a-data-mart-reset"></a>Wann muss ich einen Data Mart zurücksetzen?
Stellen Sie sich die folgenden Fragen, bevor Sie einen Data Mart zurücksetzen. Wenn Sie eine oder mehrere Fragen mit „Ja“ beantworten, kann dies darauf hinweisen, dass Ihre Organisation vom Zurücksetzen des Data Mart profitieren kann.

- Wurde die Anwendungsdatenbank wiederhergestellt?
- Wenn Sie einen Support-Vorfall eröffnet haben und ein Support-Techniker Sie angewiesen hat, den Data Mart im Rahmen einer Problembehandlung zurückzusetzen?
 
## <a name="when-is-it-not-appropriate-to-reset-a-data-mart"></a>Wann ist es nicht angebracht, einen Data Mart zurückzusetzen?
Unter bestimmten Umständen empfehlen wir nicht, einen Data Mart zurückzusetzen. Im Folgenden finden sind einige Beispiele für solche Umstände. 

- Bei Ihnen treten Leistungsprobleme auf, die mit einer Datensynchronisierung zusammenhängen. 
- Aus einem der folgenden Gründe kommt es zum Zurücksetzen mit einem sich wiederholenden Muster: 
  - **Fehlende Daten** 
  - **Hängengebliebener Integrationszustand** 
  - **Veraltete Datensätze** – Veraltete Datensätze allein rechtfertigen nicht unbedingt das Zurücksetzen des Data Mart. Bei großen Datasets kann das Zurücksetzen einige Zeit dauern. Es ist jedoch unwahrscheinlich, dass es dadurch zu einer Verbesserung kommt.
 
## <a name="what-is-a-data-mart-reset"></a>Was ist das Zurücksetzen eines Data Marts?
- Das Zurücksetzen wird erst gestartet, wenn vorhandene Aufgaben abgeschlossen sind. Dadurch wird sichergestellt, dass keine alten Daten eingefügt werden. Zu diesem Zeitpunkt wird möglicherweise die folgende Meldung angezeigt: „Das Zurücksetzen des Data Mart konnte aufgrund einer aktiven Aufgabe nicht verarbeitet werden. Bitte versuchen Sie es später erneut.“
- Durch das Zurücksetzen werden die Integrationsaufgaben deaktiviert und alle Data-Mart-Daten gelöscht. Die Integration wird erneut aktiviert.

## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a>Verliere ich Berichte, die ich bereits erstellt habe, wenn ich den Data Mart zurücksetze? 
Nein, Ihre Berichte werden in SQL-Tabellen gespeichert, die von einem Zurücksetzen des Data Mart nicht betroffen sind. Wenn Sie sich Sorgen machen, von Ihnen erstellte Berichte zu verlieren, können Sie eine Sicherungskopien der Designs erstellen, die Sie nicht verlieren möchten. Öffnen Sie dazu den Berichts-Designer und gehen Sie zu **Unternehmen > Unternehmen > Bausteine > Export**.
 
## <a name="is-it-necessary-for-all-users-to-exit-the-system-to-reset-the-data-mart"></a>Müssen alle Benutzer das System verlassen, um den Data Mart zurückzusetzen?
Nein, Benutzer können während des Zurücksetzens des Data Mart weiter im System arbeiten. Sie können jedoch erst dann auf Berichte zugreifen, die mit Financial Reporter erstellt wurden, wenn das Zurücksetzen abgeschlossen ist. 

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
