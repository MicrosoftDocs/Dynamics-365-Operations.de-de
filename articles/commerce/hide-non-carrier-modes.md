---
title: Ausblenden der Nicht-Spediteurlieferarten aus den Lieferoptionen in POS
description: In diesem Artikel wird eine Konfigurationsoption beschrieben, die verhindert, dass Nicht-Spediteurlieferarten zur Auswahl angezeigt werden, wenn Lieferungsaufträge in der Verkaufsstelle (POS)-Anwendung erstellt werden.
author: hhainesms
ms.date: 10/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 469e6ebb8afed26a6bf25f4c9c3ab8f7f4ac78ba
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897004"
---
# <a name="hide-non-carrier-delivery-modes-from-the-shipping-options-in-pos"></a>Ausblenden der Nicht-Spediteurlieferarten aus den Lieferoptionen in POS


[!include [banner](includes/banner.md)]

In diesem Artikel wird eine Konfigurationsoption beschrieben, die für die Verkaufsstelle (POS)-Anwendung verfügbar ist. Die Konfigurationsoption ändert das Verhalten für die Auswahl einer Lieferart, wenn Lieferungsaufträge in POS erstellt werden.

Wenn Benutzer Debitorenlieferungsaufträge in POS erstellen, können sie eine Lieferart für die Lieferung auswählen. Diese Funktionen sind verfügbar unabhängig davon, ob der gesamte Auftrag oder nur ausgewählte Positionen versendet werden.

Standardmäßig zeigt das Dialogfeld, in dem eine Lieferart ausgewählt wird, alle gültigen Lieferarten für die Kombination eines Kanals, eines Artikels und einer Lieferadresse an. Diese Lieferarten werden auf der Seite **Lieferarten** in der Zentralverwaltung (**Vertrieb und Marketing \> Einstellungen \> Verteilung \> Lieferarten**) definiert. „Nicht-Spediteur“-Lieferarten wie **Takeaway** oder **Entnahme** werden möglicherweise auch zur Auswahl im Dialogfeld angezeigt.

Jedoch wurde eine Funktion hinzugefügt, mit der Sie Nicht-Spediteurlieferarten im Dialogfeld ausblenden können. Um diese Funktion zu aktivieren, legen Sie auf der Seite für **Commerce-Parameter** auf der Registerkarte **Debitorenaufträge** die Option **Nur Spediteurmodusoptionen für Lieferungsaufträge anzeigen** auf **Ja** fest. Nachdem Sie diese Funktion aktiviert und die entsprechenden Verteilungseinzelvorgänge ausgeführt haben, um die Informationen mit der Kanaldatenbank zu synchronisieren, werden Nicht-Spediteurlieferarten beim Erstellen der Lieferungsaufträge in POS nicht für die Auswahl angezeigt.


[!INCLUDE[footer-include](../includes/footer-banner.md)]