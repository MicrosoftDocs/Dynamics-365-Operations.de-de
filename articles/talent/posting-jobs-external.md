---
title: Stellen aus Attract auf externen Karrierewebsites veröffentlichen
description: In diesem Thema wird erläutert, wie Dynamics 365 for Talent - Attract verwendet wird, um Stelle auf externe Stellenportalen zu veröffentlichen
author: pganapmsft
manager: AnnBe
ms.date: 05/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-03-19
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 936ff85a4dabb715cb83b875a5c58c9fb7a0ac26
ms.sourcegitcommit: 7c49475402632069685df714546770d30804af7f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/11/2019
ms.locfileid: "1739816"
---
# <a name="post-jobs-to-broadbean"></a>Stellen auf Broadbean veröffentlichen

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 for Talent: Attract hilft Ihnen, die Talente zu finden, die Sie brauchen, indem Sie Ihre Stellen direkt von Attract in Broadbean veröffentlichen. Nachdem Sie eine [Stelle erstellt haben](./creating-jobs-attract.md), müssen Sie nur auf eine Schaltfläche klicken, um die Stelle für alle möglichen Stellenbewerber auf Broadbean bereitzustellen.

Das Veröffentlichen von Stellen auf Broadbean erfordert eine entsprechende Broadbeanlizenz. Broadbean bietet verschiedene Produkte und Plänen an. Weitere Informationen zur Broadbeanlizenzierung und den Preise erhalten Sie, indem Sie [Broadbean kontaktieren](https://www.broadbean.com/contact-us/).

Wenn Sie ein Administrator sind, der mehr Informationen zur Konfiguration der Broadbeanintegration mit Attract benötigt, gehen Sie zu [Einstellungen für externe Stellenbörsen eingeben](./attract-admin-job-board-settings.md).

## <a name="post-jobs-to-broadbean"></a>Stellen auf Broadbean veröffentlichen

Nachdem Broadbean aktiviert wurde, können Personaleschaffungsmanager und Administratoren Stellen darauf veröffentlichen. Sie müssen eine URL für die Stelle verwenden.

1. Öffnen Sie in Attract die Stelle, die Sie in Broadbean veröffentlichen möchten.
2. Im Abschnitt **Veröfffentlichungen** wählen Sie die Schaltfläche **Jetzt veröffentlichen** aus, die Broadbean entspricht.
3. Folgen Sie den Anweisunge im Broadbea Fenster.

Attract leitet folgenden Informationen an Broadbean weiter:

- Anforderungskennung
- Stellenbezeichnung
- Einzelvorgangsbeschreibung
- Arbeitsort
- URL anwenden
- Informationen zum Personalbeschaffungsmitarbeiter

Nachdem Broadbean die Veröffentlichung erfolgreich abgeschlossen hat, zeigt der Abschnitt **Veröffentlichung** der Stelle in Attract den Broadbean Status als **veröffentlicht**.

> [!NOTE]
> - Broadbean erfordert das Feld **Branche**. Zurzeit ist dieses Feld standardmäßig auf **IT** festgelegt. Sie können den Wert jedoch im Fenster für die Broadbean Stellenveröffentlichung auf die richtige Branche anpassen.
> - Es dauert einige Zeit, bis Broadbean die Veröffentlichung Ihrer Stelle in allen Stellenportalen, die Sie ausgewählt haben, abgeschlossen hat. Daher kann es möglicherweise eine geringfügige Verzögerung geben, bevor Attract eine Statusaktualisierung für die Stelle bereitstellt.

### <a name="view-a-broadbean-job-posting"></a>Eine Broadbean Stellenausschreibung anzeigen.

Nachdem Sie eine Stelle in Broadbean veröffentlich haben, können Sie diese über Attract ansehen.

1. Öffnen Sie in Attract die Stelle, die Sie in Broadbean anzeigen möchten.
2. Auf der Registerkarte **Stelle** wählen Sie die Ellipsenschaltfläche (**...**), die Broadbean entspricht und wählen Sie dann **Ansicht** aus.

Die Broadbean Stellenausschreibung wird in einem neuen Fenster angezeigt.

### <a name="update-a-broadbean-job-posting"></a>Eine Broadbean Stellenausschreibung aktualisieren.

Sie können eine Broadbean Stellenausschreibung auf zwei Arten aktualisieren.

1. In Attract öffnen Sie die Stelle, die Sie anzeigen möchten.
2. Im Abschnitt **Veröfffentlichungen** wählen Sie die Schaltfläche **Veröffentlichung aktualisieren**, die Broadbean entspricht.
3. Bearbeiten Sie die Veröffentlichung im Fenster Broadbean.

- oder -

1. Öffnen Sie in Attract die Stelle, die Sie in Broadbean anzeigen möchten.
2. Im Abschnitt **Stelle** wählen Sie die Ellipsenschaltfläche (**...**), die Broadbean entspricht und wählen Sie dann **Ansicht** aus.
3. Im Fenster Broadbean bearbeiten Sie die Stellendetails und veröffentlichen die Stelle erneut. Die Stellendetails in Attract sind unverändert.

### <a name="remove-a-broadbean-job-posting"></a>Entfernen einer Broadbean Stellenausschreibung

Sie können eine Stellenausschreibung aus Broadbean wieder entfernen.

1. In Attract öffnen Sie die Stelle, die Sie entfernen möchten.
2. Im Abschnitt **Stelle** wählen Sie die Ellipsenschaltfläche (**...**), die Broadbean entspricht und wählen Sie dann **Stelle entfernen** aus.

Nachdem Broadbean die Stelle entfernt hat, hat das Broadbean Element in Attact eine Schaltfläche **Jetzt veröffentlichen**. Das Vorhandensein dieser Schaltfläche gibt an, dass die Stelle entfernt wurde und erneut gebucht werden kann.

### <a name="troubleshoot-job-posting-to-broadbean"></a>Beheben Sie Probleme mit der Veröffentlichung von Stellen in Broadbean

Wenn Sie Probleme haben, eine Stelle in Broadbean zu veröffentlichen, versuchen Sie diese Schritte.

1. Überprüfen Sie, dass die Broadbean Anmeldeinformationen, die Sie in Attract eingegeben haben, gültig und korrekt sind.
2. Wenn die Anmeldeinformationen gültig sind und korrekt sind, kontaktieren Sie den [Broadbean Support](https://www.broadbean.com/resources/support/).
3. Wenn das Problem weiterhin besteht, kontaktieren Sie den [Microsoft Support](./talent-support.md).

## <a name="see-also"></a>Siehe auch

[Stelle erstellen](./creating-jobs-attract.md)

[Geben Sie Einstellungen für externe Stellenbörsen ein](./attract-admin-job-board-settings.md)
