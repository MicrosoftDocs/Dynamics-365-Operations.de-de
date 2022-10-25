---
title: Synchronisation von Kundenvorgängen in der Zentrale überwachen
description: In diesem Artikel wird erläutert, wie Sie die Synchronisierung von Kundenvorgängen in Microsoft Dynamics 365 Commerce Headquarters prüfen, um bei der Behebung von Problemen mit Websitebenutzern zu helfen.
author: gvrmohanreddy
ms.date: 10/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-09-28
ms.openlocfilehash: c615b0b436e01a1423b5611a72f0056b5b14f8e8
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691087"
---
# <a name="audit-synchronization-of-customer-operations-in-headquarters"></a>Synchronisation von Kundenvorgängen in der Zentrale überwachen

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

In diesem Artikel wird erläutert, wie Sie die Synchronisierung von Kundenvorgängen in Microsoft Dynamics 365 Commerce Headquarters prüfen, um bei der Behebung von Problemen mit Websitebenutzern zu helfen.

Da Unternehmen damit beginnen, Kunden asynchron zu erstellen und zu bearbeiten, benötigen Site-Administratoren eine Möglichkeit, Vorgänge basierend auf Site-Benutzeranfragen oder Prozessfehlern anzuzeigen und Fehler zu beheben. In diesen Szenarien sollten Site-Administratoren in der Lage sein, Kundenerstellungs- und -bearbeitungsvorgänge zu überwachen und alle Fehler mithilfe eines Self-Service-Modells zu beheben.

## <a name="customer-synchronization-status"></a>Status der Debitorensynchronisierung

Wenn Sie sich für den asynchronen Modus der Kundenverwaltung und der dazugehörigen Funktionen anmelden, müssen Administratoren der Commerce headquarters ungeachtet Ihrer Auswahl bei der Ersteller synchroner und asynchroner Debitoren wiederkehrenden Stapelverarbeitungsauftrag für den **P-Einzelvorgang**, den Einzelvorgang **Debitoren und Geschäftspartner im asynchronen Modus synchronisieren** und den Einzelvorgang **1010** erstellen und planen, sodass alle asynchrone Debitoren im Commerce headquarters in synchrone Debitoren konvertiert werden. Die Synchronisierung von Kundenverwaltungsvorgängen erfolgt immer dann, wenn diese Jobs ausgeführt werden. Weitere Informationen finden Sie unter [Asynchroner Kundenerstellungsmodus](async-customer-mode.md).

Als Geschäftsinhaber können Sie die folgenden Vorgänge ausführen:

- Zeigen Sie alle Erstellungs-/Bearbeitungsvorgänge von Sitebenutzern an. Zu den Details gehören der Status und ein Zeitstempel.
- Filtern Sie Vorgänge, indem Sie beliebige Felder und Werte der Kundentabelle verwenden, um das Prüfprotokoll einzugrenzen.
- Zeigen Sie kurze Beschreibungen von Änderungen zusammen mit den Statusdetails an, um Vorgänge auf hoher Ebene zu verstehen.
- Bearbeiten und beheben Sie bei Fehlern problematische Felder und speichern und synchronisieren Sie dann bestimmte Kundenvorgänge.

### <a name="elements-on-the-customer-synchronization-status-page"></a>Elemente auf der Statusseite der Kundensynchronisierung

Um eine Liste aller Synchronisationsvorgänge anzuzeigen, gehen Sie in Commerce Headquarters zu **Handel und Einzelhandel \> Kunden \> Kundensynchronisierungsstatus**. Die folgende Abbildung zeigt ein Beispiel der Seite **Status der Debitorensynchronisierung**.

![Statusseite der Kundensynchronisierung im Commerce Headquarters.](media/D365-Commerce-Customer-Mgmt-Audi-Async-Operations.png)

Standardmäßig enthält die Liste der Kundensynchronisierungsvorgänge auf der linken Seite der Seite **Status der Debitorensynchronisierung** die folgenden Spalten:

- Kanalname
- Kundenkonto
- Konto des asynchronen Debitors
- Vorgangszeitstempel
- Status der Debitorensynchronisierung

Oben rechts auf der Seite werden Kundenkontodetails angezeigt, z. B. **Kundenkonto**, **Asynchroner Einzelhandelsbetrieb**, **Kundensynchronisierungsstatus**, und **Letzter bekannter Fehler** Werte.

Der Abschnitt **Beschreibung ändern** enthält eine Beschreibung des Typs des ausgeführten Kundenverwaltungsvorgangs (z. B. Kundenerstellung, Kontoaktualisierung oder Synchronisierungsfehler mit Details).

Der Abschnitt **Kundenattribute** enthält ein Raster, das alle Kundenattribute zusammen mit alten und neuen Werten anzeigt. Sie können diesen Abschnitt bearbeiten, wenn Sie Ihre Kundenattributwerte ändern möchten, um Fehler zu beheben, und dann erneut synchronisieren.
