---
title: Auftragssuchmodul
description: Dieses Thema behandelt das Auftragssuchmodul und erläutert, wie es in Microsoft Dynamics 365 Commerce konfiguriert wird.
author: stuharg
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2021-08-15
ms.dyn365.ops.version: Release 10.0.22
ms.openlocfilehash: fa61a20ffd9a31f800c48b71832be7547952119f
ms.sourcegitcommit: d420b96d37093c26f0e99c548f036eb49a15ec30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/03/2021
ms.locfileid: "7472613"
---
# <a name="order-lookup-module"></a>Auftragssuchmodul

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Dieses Thema behandelt das Auftragssuchmodul und erläutert, wie es in Microsoft Dynamics 365 Commerce konfiguriert wird.

Das Auftragssuchmodul stellt ein Formular bereit, mit dem Kunden Bestellungen suchen können, die sie auf einer E-Commerce-Site aufgegeben haben. Es wird als Teil der [Auftragssuche für Gastbezahlvorgänge aktivieren](order-lookup-guest.md)-Funktion. Das Auftragssuchmodul kann verwendet werden, um Bestellungen nachzuschlagen, die über eine E-Commerce-Site, die Einzelhandelsverkaufsstelle (POS) oder ein Callcenter übermittelt wurden. Das Formular kann Bestellungen abrufen, die sowohl von Gastbenutzern als auch von registrierten Benutzern eingereicht wurden.

Die folgende Abbildung zeigt ein Beispiel für das Formular, das vom Auftragssuchmodul gerendert wird. Wenn Kunden das Formular ausfüllen und **Ihre Bestellung suchen** auswählen, werden sie auf die Seite mit den Bestelldetails weitergeleitet.

![Formular für das Auftragssuchmodul auf einer Seite.](./media/OrderLookup_module.PNG)

## <a name="order-lookup-module-properties"></a>Eigenschaften des Auftragssuchmoduls

| Eigenschaftenname     | Wert     | Beschreibung |
|-------------------|-----------|-------------|
| Überschrift           | Text      | Die Überschrift, die oben im Formular angezeigt wird (z. B. „Bestellung finden“). |
| Rich Text         | Rich Text | Optionaler erläuternder Text, der unter der Überschrift angezeigt wird. |
| Auftragsstatustyp | Enum      | <p>Wählen Sie die Art der Informationen aus, die das Formular zusätzlich zur Bestellbestätigungs-ID vom Kunden anfordert. Die folgenden Werte werden derzeit unterstützt:</p><ul><li><b>E-Mail</b> – das Formular enthält ein Feld, in das Kunden die E-Mail-Adresse eingeben können, die sie bei der Bestellung verwendet haben.</li><li><b>Keine</b> – das Formular fordert außer der Bestellbestätigungs-ID keine weiteren Informationen an.</li></ul> |

## <a name="add-an-order-lookup-module-to-a-page"></a>Ein Auftragssuchmodul einer Seite hinzufügen

Das Auftragssuchmodul kann dem Hauptteil jeder Seite Ihrer E-Commerce-Site hinzugefügt werden. Wenn Sie das Auftragssuchmodul verwenden möchten, um die Auftragssuche für Gastbezahlvorgänge zu aktivieren, stellen Sie sicher, dass Sie es einer Seite hinzufügen, auf der der Benutzer nicht angemeldet sein muss. Um die Einstellung **Anmeldung erforderlich?** einer Seite zu finden, wählen Sie in der Baumansicht des Commerce Site Builder den Slot **Standardseite (erforderlich)** aus, und sehen sich den unteren Teil des rechten Fensters an.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Auftragssuche für Gast-Checkouts aktivieren](order-lookup-guest.md)

[Informationen zur Modulbibliothek](starter-kit-overview.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
