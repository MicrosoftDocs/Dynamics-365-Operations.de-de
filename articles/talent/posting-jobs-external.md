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
ms.openlocfilehash: 9c27d1810a89ed7d7a7745e41c5f118dbdfe5dda
ms.sourcegitcommit: cadce85ca3004d53caf6bc49147a524c1bfd421f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/16/2019
ms.locfileid: "1590481"
---
# <a name="post-jobs-to-external-career-sites-from-attract"></a>Stellen aus Attract auf externen Karrierewebsites veröffentlichen

[!include [banner](../includes/banner.md)]

Sie möchten die offenen Stellen für möglichst viele qualifizierten Kandidaten bekannt machen. Stellenportale wie Broadbean helfen Ihnen dabei Microsoft Dynamics 365 Talent: Mit Attract können Sie nune Stellen auf Broadbean veröffentlichen und Microsoft ist ständig daran, neue Angebote in diesem Bereich bereitzustellen.

## <a name="post-jobs-to-broadbean"></a>Stellen auf Broadbean veröffentlichen.

Bevor Stellen in Broadbean gebucht werden können, müssen Sie die Broadbean-Integration konfigurieren.

> [!NOTE]
> - Um Stellen an externen Standorten zu buchen, müssen Sie das [Umfassende Einstellungsadd-on](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring) haben.
> - Um Stellen bei Broadbean über Attract zu veröffentlichen, müssen Sie ein Broadbean-Abonnement haben.
> - Diese Funktion befindet sich derzeit in der Vorschau. Wenn Sie sie ausprobieren möchten, müssen Sie [sie in den Attract-Administratoreinstellungen aktivieren](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature) auf.

### <a name="configure-broadbean-integration"></a>Broadbean-Integration konfigurieren

1. Bei Attract als Administrator anmelden.
2. Wählen Sie die Schaltfläche **Einstellungen** (das Rad-Symbol) in der rechten oberen Ecke der Seite aus, und wählen Sie dann **Administratorcenter**.
3. In der Registerkarte **Stellenbörseeinstellungen** im Abschnitt **Broadbeanintegration aktivieren**, aktivieren Sie die Integration.
4. Broadbean kontaktieren und die Informationen in **Benutzername, Client-ID, Verschlüsselungs-Token** eingeben.

> [!WARNING]
> Ihre Broadbean-Anmeldeinformationen sind vertraulich. Daher müssen Sie diese sicher und verantwortungsvoll speichern. Alle, die eine Administratorrolle in Attract haben, können diese Anmeldeinformationen anzeigen.

> [!NOTE]
> Microsoft und Attract sind nicht involviert beim Erstellen und Verwalten dieser Werte. Es ist Ihre Verantwortung, sie in Attract auf dem neuesten Stand zu halten und mit Broabean zusammen zu arbeiten, um Probleme zu beheben, die Ihre Anmeldeinformationen umfassen.

### <a name="post-a-job-to-broadbean"></a>Eine Stelle auf Broadbean veröffentlichen

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
2. Im Abschnitt **Stelle** wählen Sie die Ellipsenschaltfläche (**...**), die Broadbean entspricht und wählen Sie dann **Ansicht** aus.

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

### <a name="troubleshoot-the-broadbean-integration"></a>Problembehandlung bei der Broadbean Integration

Wenn Sie Probleme haben, eine Stelle in Broadbean zu veröffentlichen, versuchen Sie diese Schritte.

1. Überprüfen Sie, dass die Broadbean Anmeldeinformationen, die Sie in Attract eingegeben haben, gültig und korrekt sind.
2. Wenn die Anmeldeinformationen gültig sind und korrekt sind, kontaktieren Sie den [Broadbean Support](https://www.broadbean.com/resources/support/).
3. Wenn das Problem weiterhin besteht, kontaktieren Sie den [Microsoft Support](./talent-support.md).
