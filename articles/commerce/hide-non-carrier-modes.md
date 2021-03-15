---
title: Ausblenden der Nicht-Spediteurlieferarten aus den Lieferoptionen in POS
description: In diesem Thema wird eine Konfigurationsoption beschrieben, die verhindert, dass Nicht-Spediteurlieferarten zur Auswahl angezeigt werden, wenn Lieferungsaufträge in der Verkaufsstelle (POS)-Anwendung erstellt werden.
author: hhainesms
manager: annbe
ms.date: 10/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: fcacb4243e78607d19d2c57aff5debe04d85d6f2
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009720"
---
# <a name="hide-non-carrier-delivery-modes-from-the-shipping-options-in-pos"></a>Ausblenden der Nicht-Spediteurlieferarten aus den Lieferoptionen in POS


[!include [banner](includes/banner.md)]

In diesem Thema wird eine Konfigurationsoption beschrieben, die für die Verkaufsstelle (POS)-Anwendung verfügbar ist. Die Konfigurationsoption ändert das Verhalten für die Auswahl einer Lieferart, wenn Lieferungsaufträge in POS erstellt werden.

Wenn Benutzer Debitorenlieferungsaufträge in POS erstellen, können sie eine Lieferart für die Lieferung auswählen. Diese Funktionen sind verfügbar unabhängig davon, ob der gesamte Auftrag oder nur ausgewählte Positionen versendet werden.

Standardmäßig zeigt das Dialogfeld, in dem eine Lieferart ausgewählt wird, alle gültigen Lieferarten für die Kombination eines Kanals, eines Artikels und einer Lieferadresse an. Diese Lieferarten werden auf der Seite **Lieferarten** in der Zentralverwaltung (**Vertrieb und Marketing \> Einstellungen \> Verteilung \> Lieferarten**) definiert. „Nicht-Spediteur“-Lieferarten wie **Takeaway** oder **Entnahme** werden möglicherweise auch zur Auswahl im Dialogfeld angezeigt.

Jedoch wurde eine Funktion hinzugefügt, mit der Sie Nicht-Spediteurlieferarten im Dialogfeld ausblenden können. Um diese Funktion zu aktivieren, legen Sie auf der Seite für **Commerce-Parameter** auf der Registerkarte **Debitorenaufträge** die Option **Nur Spediteurmodusoptionen für Lieferungsaufträge anzeigen** auf **Ja** fest. Nachdem Sie diese Funktion aktiviert und die entsprechenden Verteilungseinzelvorgänge ausgeführt haben, um die Informationen mit der Kanaldatenbank zu synchronisieren, werden Nicht-Spediteurlieferarten beim Erstellen der Lieferungsaufträge in POS nicht für die Auswahl angezeigt.


[!INCLUDE[footer-include](../includes/footer-banner.md)]