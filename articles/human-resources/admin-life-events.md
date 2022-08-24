---
title: Administratorrechte für Lebensereignisse festlegen
description: In diesem Artikel wird erläutert, wie Sie Administratorrechte für Lebensereignisse in Microsoft Dynamics 365 Human Resources konfigurieren.
author: twheeloc
ms.date: 08/01/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9deed240977394667cee8b107397267b182d960b
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2022
ms.locfileid: "9229899"
---
# <a name="set-administrator-rights-for-life-events"></a>Administratorrechte für Lebensereignisse festlegen

[!include [banner](../includes/preview-banner.md)]

Administratoren können Lebensereignisoptionen je nach Konfigurationseinstellungen aktualisieren. Auf der Seite **Personalverwaltungsparameter** können Sie Parameter konfigurieren, die es Administratoren ermöglichen, Änderungen an Planauswahlen vorzunehmen. Sie können Administratoren auch vollständig daran hindern, Änderungen vorzunehmen.

Auf der Seite **Personalverwaltungsparameter** können Sie Planänderungsbeschränkungen für bestätigte Pläne und Optionen für Lebensereignisse einrichten.

Wenn die Option **Bestätigte Pläne** ausgewählt ist, können Änderungen nur vorgenommen werden, wenn ein Anmeldezeitraum aktiv ist. (Beispiele für Registrierungszeiträume sind offene Registrierungszeiträume, Registrierungszeiträume für neu eingestellte Mitarbeiter und Registrierungszeiträume für Lebensereignisse.) Wenn diese Option nicht ausgewählt ist, können jederzeit Änderungen vorgenommen werden.

Wenn die Option **Lebensereignisoptionen** nicht ausgewählt ist, werden Planänderungen während eines Lebensereignisses durch die Lebensereignisoptionen eingeschränkt, die für den Plantyp festgelegt sind. Wenn diese Option nicht ausgewählt ist, können Planauswahlen während eines Lebensereignisses geändert werden.

## <a name="set-plan-change-restrictions"></a>Planänderungsbeschränkungen festlegen

Auf der Seite **Personalverwaltungsparameter** auf der Registerkarte **Leistungsmanagement** die folgenden Felder verfügbar.

| Feld | Description |
|-------|-------------|
| Bestätigte Pläne | Wählen Sie diese Option, wenn Änderungen an einem Plan nur zulässig sind, wenn ein Registrierungszeitraum aktiv ist. Wenn diese Option nicht ausgewählt ist, können Änderungen jederzeit vorgenommen werden. |
| Lebensereignisoptionen | Wählen Sie diese Option, wenn Planänderungen während eines Lebensereignisses durch die Lebensereignisoptionen eingeschränkt sind, die für den Plantyp festgelegt sind. Wenn diese Option nicht ausgewählt ist, können Planauswahlen während eines Lebensereignisses geändert werden. |
