---
title: Betriebliche Erkenntnisse einrichten
description: Dieser Artikel beschreibt, wie Sie die Funktion Betriebliche Einblicke in Microsoft Dynamics 365 Commerce einrichten und verwenden.
author: ashishMSFT
ms.date: 12/07/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: ca0d31e403275d6131fa6d53f0a7b46a7ddb651d
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2022
ms.locfileid: "9832126"
---
# <a name="set-up-operational-insights"></a>Betriebliche Erkenntnisse einrichten

[!include [banner](../includes/banner.md)]

Dieser Artikel beschreibt, wie Sie die Funktion Betriebliche Einblicke in Microsoft Dynamics 365 Commerce einrichten und verwenden.

Operational Insights ist eine Dynamics 365 Commerce Funktion, die Kunden einen besseren Einblick in ihren Dienstzustand und ihre Geschäftsfunktionen geben soll, indem Telemetriedaten direkt an ein kundeneigenes Application Insights Konto gesendet werden.

Indem Sie Operational Insights für Ihre Umgebungen im Commerce headquarters aktivieren, können Sie eine kuratierte Liste von Ereignissen sowohl von Commerce Scale Unit (CSU) als auch von Ihren Point-of-Sale (POS)-Geräten sammeln. Diese Ereignisse können Ihnen dabei helfen, die Leistung Ihrer Systeme besser zu verstehen, und sie ermöglichen Ihnen die Überwachung wichtiger technischer und geschäftlicher Kennzahlen.

Auch wenn Sie diese Telemetriedaten nicht ständig erfassen möchten, können Sie davon profitieren, indem Sie die Erfassung für bestimmte Umgebungen schnell aktivieren oder deaktivieren. Auf diese Weise kann Ihnen die Telemetrie bei der Fehlerbehebung oder beim Debuggen während der Entwicklung oder in der Produktion helfen.

## <a name="access-logs-in-application-insights"></a>Zugriffsprotokolle in Application Insights

Führen Sie die Verfahren in diesem Abschnitt aus, um über Application Insights auf Diagnoseereignisprotokolle für Commerce CSU- und POS-Komponenten zuzugreifen.

### <a name="minimum-version-requirements-for-csu"></a>Minimale Versionsanforderungen für CSU

CSU hat die folgenden Mindestversionsanforderungen:

- 10.0.23 (Retail Server-Version 9.33.22062.15 und höher)
- 10.0.24 (Retail Server-Version 9.34.22062.14 und höher)
- 10.0.25 (Retail Server-Version 9.35.22062.13 und höher)
- 10.0.26 und höher (alle Versionen)

### <a name="enable-diagnostic-events-in-application-insights"></a>Aktivieren Sie Diagnoseereignisse in Application Insights

> [!IMPORTANT]
> Wenn Sie zuvor eine Vorschauversion von Operational Insights verwendet haben, müssen Sie das folgende Verfahren verwenden, um Operational Insights zu aktivieren. So stellen Sie sicher, dass weiterhin ein zuverlässiger und sicherer Zugriff auf Veranstaltungen möglich ist.

Um Diagnoseereignisse der Commerce-Komponente zu aktivieren, müssen Sie über ein Application Insights Konto verfügen. Sie können ein vorhandenes Konto verwenden oder [ein neues Konto erstellen](/azure/azure-monitor/app/create-workspace-resource#create-workspace-based-resource). Aus Datenschutzgründen empfehlen wir Ihnen, separate Application Insights Konten für Produktions-, Sandbox- und Entwicklungsumgebungen zu verwenden. Nachdem Sie ein Konto erstellt haben, müssen Sie die Funktion **Operational Insights** in der Zentrale aktivieren.

Führen Sie die folgenden Schritte aus, um Diagnoseereignisse in Application Insights zu aktivieren.

1. Öffnen Sie in headquarters den Arbeitsbereich **Funktionsverwaltung** und aktivieren Sie die Funktion **Betriebseinblicke**.
1. Gehen Sie zu **Systemverwaltung \> Einrichten \> Betriebliche Einblicke**.
1. Setzen Sie auf der Registerkarte **Konfigurieren** die Option **Commerce-Kanalereignisse** auf **Ja**.
1. Geben Sie auf der Registerkarte **Umgebungen** Werte für **LCS-Umgebungs-ID** and **Umgebungsmodus** für jede Umgebung ein, in der Sie Application Insights verwenden möchten. Sie finden die Umgebungs-ID jeder Umgebung auf der Seite **Umgebungsdetails** für diese Umgebung in Microsoft Dynamics Lifecycle Services. Dieser Schritt ist erforderlich, um zu verhindern, dass Diagnoseereignisse versehentlich an eine falsche Umgebung gesendet werden, wenn Datenbankkopiervorgänge durchgeführt werden.
1. Geben Sie auf der REgisterkarte **Application Insights Registrierung** den Application Insights **Instrumentierungsschlüssel** Wert und den entsprechenden **Umgebungsmodus** Wert der Umgebungen, in denen Sie die einzelne Application Insights Konten verwenden möchten.
1. Nachdem Sie die vorherige Konfiguration abgeschlossen haben, müssen Sie den Job **CDX-Job 1110** ausführen. Sie können warten, bis dieser Job gemäß seinem eigenen Zeitplan ausgeführt wird, oder Sie können ihn manuell ausführen.
1. Gehen Sie in Lifecycle Services zu **Umgebungsdetails \> Commerce \> Verwalten**, wählen Sie eine CSU-Instanz und dann **Neu starten**. Wiederholen Sie diesen Schritt für jede CSU.
1. Wiederholen Sie die vorherigen Schritte für jede Umgebung, in der Sie Application Insights verwenden möchten.

> [!NOTE]
> - Die Telemetrieereignisse in Operational Insights können sich ändern. Wir empfehlen, dass Sie Operational Insights-Ereignisse verwenden, um selbst vorläufige Analysen und Fehlerbehebungen durchzuführen, und nicht, um Dashboards oder Warnungen zu definieren. Wenn Sie Ereignisse für Zwecke verwenden, die über die Self-Service-Fehlerbehebung hinausgehen, empfehlen wir Ihnen, Ihre Abfragen nach jeder CSU/POS-Version zu validieren und zu aktualisieren.
> - Ab Commerce-Version 10.0.29 ermöglichen die Verfahren in diesem Abschnitt auch das Streamen von POS Operational Insights-Ereignissen zu Ihrem Application Insights Konto. Weitere Informationen finden Sie unter [Operational Insights for POS – Ereignisse und Abfragen](https://download.microsoft.com/download/9/2/b/92be35b0-0e24-4a4d-940d-6f4db29791c0/Operational-Insights-Commerce-POS-events-queries.pdf).

#### <a name="use-the-dllhostexeconfig-file-to-control-pos-operational-insights-events"></a>Verwenden Sie die Datei DLLHost.exe.config, um POS Operational Insights-Ereignisse zu steuern

Verwenden Sie diese Schritte, um die Datei DLLHost.exe.config, um POS Operational Insights-Ereignisse zu steuern

1. Öffnen Sie in einem Texteditor die Datei **DLLHost.exe.config** unter **C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\Retail Modern POS\\ClientBroker**.
1. Entfernen Sie im Abschnitt **diagnosticsSection** das Sink-XML Element mit dem Klassennamen **Microsoft.Dynamics.Retail.Diagnostics.OperationalInsights.OperationalInsightsLogger**.
1. Speichern Sie die Datei.

### <a name="disable-diagnostic-events-in-application-insights"></a>Deaktivieren Sie Diagnoseereignisse in Application Insights

> [!IMPORTANT]
> Wenn Sie Diagnoseereignisse deaktivieren und nicht mehr an Application Insights senden möchten, müssen Sie das folgende Verfahren ausführen. Sie können diese Vorschaufunktion unter Funktionsverwaltung nicht einfach deaktivieren.

Führen Sie die folgenden Schritte aus, um Diagnoseereignisse in Application Insights zu deaktivieren.

1. Gehen Sie in headquarters zu **Systemverwaltung \> Betriebliche Einblicke**.
1. Setzen Sie auf der Registerkarte **Konfigurieren** die Option **Commerce-Kanalereignisse** auf **Nein**.
1. Nachdem Sie die vorherige Konfiguration abgeschlossen haben, müssen Sie den Job **CDX-Job 1110** ausführen. Sie können warten, bis dieser Job gemäß seinem eigenen Zeitplan ausgeführt wird, oder Sie können den Job manuell ausführen.
1. Gehen Sie in Lifecycle Services zu **Umgebungsdetails \> Commerce \> Verwalten**, wählen Sie eine CSU-Instanz und dann **Neu starten**. Wiederholen Sie diesen Schritt für jede CSU.
1. Wiederholen Sie die vorherigen Schritte für jede Umgebung, in der Sie Application Insights deaktivieren möchten.

Um Diagnoseereignisse für eine einzelne Umgebung zu deaktivieren, löschen Sie den Instrumentierungsschlüssel auf der Registerkarte **Application Insights Registrierung** der Seite **Betriebliche Einblicke**. Führen Sie dann die Schritte 3 und 4 des vorherigen Verfahrens aus.

> [!NOTE]
> In Commerce-Version 10.0.29 und höher deaktivieren die Schritte in diesem Abschnitt auch das Streamen von POS Operational Insights-Ereignissen zu Ihrem Application Insights Konto. 
