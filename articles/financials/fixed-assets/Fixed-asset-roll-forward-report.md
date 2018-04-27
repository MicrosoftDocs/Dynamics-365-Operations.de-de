---
title: "Rollforwardbericht für Anlagen"
description: "In diesem Thema wird erläutert, wie Sie den Rollforwardbericht für Anlagen verwenden."
author: saraschi2
manager: 
ms.date: 01/08/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 23021
ms.assetid: d7e86f72-95db-4423-9b04-761e9536a959
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-12-20
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 16f7c199fb4c9905c465e5d4596d3eaa90104b83
ms.contentlocale: de-de
ms.lasthandoff: 04/13/2018

---
# <a name="fixed-assets-roll-forward-report"></a>Rollforwardbericht für Anlagen

[!INCLUDE [banner](../includes/banner.md)]

Der Bericht **Rollforward für Anlagen** bietet ein einfach zu lesendes Microsoft Excel-Format, die detaillierten Anlagedaten, die Sie für den Periodenabschluss, für Finanzaufstellungen und die Steuererklärung benötigen. Der Bericht umfasst Start- und Endsalden für Anlagen zusammen mit Bewertungsbewegungen für die Periode und sämtlicher neuer Anlagenanschaffungen und -abgänge, die sich während der Periode ereigneten. Daten werden für einzelne Anlagen gemeldet, und Werte werden auch für Anlagengruppen und die juristische Person zusammengefasst.

Der Bericht **Rollforward für Anlagen** verwendet das Framework für die elektronische Berichterstellung (EB). Bevor Sie den Bericht ausführen können, müssen die Rollforwardkonfigurationen für Anlagenmodell und Anlagen aus Microsoft Dynamics Lifecycle Services (LCS) importiert werden. Weitere Informationen finden Sie unter [Elektronische Berichtskonfigurationen aus Lifecycle Services herunterladen](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs).

Dieser Bericht ist in Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3, oder als Hotfix für Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (Juli 2017), verfügbar. Drei Hotfixes müssen auf Umgebungen angewendet werden, die die Version von Juli 2017 haben:

- **KB 4041754:** Konfiguration der elektronischen Berichterstellung (EB) kann nicht von LCS heruntergeladen werden, da sie für die aktuelle Anwendungsversion nicht anwendbar ist, nachdem das Plattformupdatepaket angewendet wurde.
- **KB 4056107:** Elektronische Berichterstellung (GER) kumulatives Update 5
- **KB 4056353:** Aufstellungs- und Hinweisberichte für Anlagen erfüllen nicht die Anforderungen in GAAP and IFRS

In der folgenden Tabelle werden die Felder beschrieben, die im Bericht zur Verfügung stehen.


|                    Feld                    |                                                                                                                                Beschreibung                                                                                                                                |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|              Salden: Eröffnung              |                                                                                           Der Anlagennettobuchwert ab dem Datum „Von”, das im Bericht angegeben wird.                                                                                           |
|              Salden: Abschluss              |                                                                                            Der Anlagennettobuchwert ab dem Datum „Bis”, das im Bericht angegeben wird.                                                                                            |
|         Anschaffungen: Eröffnungswert         |                                                 Die Summe aller Transaktionen der Typen <strong>Anschaffung</strong> und <strong>Anschaffungsregulierung</strong> bis zum Datum „Von”, das im Bericht angegeben wird.                                                  |
|      Anschaffungen: Periodenanschaffungen      |                                                 Die Summe aller Transaktionen der Typen <strong>Anschaffung</strong> und <strong>Anschaffungsregulierung</strong>, die während des Datumsbereichs für den Bericht gebucht wurden.                                                  |
|       Anschaffungen: Periodenabgänge        |                                                                        Die Summe aller Anschaffungsumkehrungen, die gebucht wurden, die eine Abgangstransaktion während des Datumsbereichs für den Bericht hatten.                                                                        |
|         Anschaffungen: Abschlusswert         |                                                  Die Summe aller Transaktionen der Typen <strong>Anschaffung</strong> und <strong>Anschaffungsregulierung</strong> bis zum Datum „Bis”, das im Bericht angegeben wird.                                                   |
|        Abschreibungen: Eröffnungswert         | Die Summe aller Transaktionen der Typen <strong>Abschreibung</strong>, <strong>Abschreibungsregulierung</strong>, <strong>Sonderabschreibung</strong> und <strong>Außerordentliche Abschreibung</strong> bis zum Datum „Von”, das im Bericht angegeben ist. |
|     Abschreibungen: Periodenabschreibungen     |                         Die Summe aller Transaktionen der Typen <strong>Abschreibung</strong>, <strong>Abschreibungsregulierung</strong> und <strong>Außerordentliche Abschreibung</strong>, die während des Datumsbereichs für den Bericht gebucht wurden.                          |
| Abschreibungen: Periodensonderabschreibungen |                                                              Die Summe aller Transaktionen des Typs <strong>Sonderabschreibung</strong>, die während des Datumsbereichs für den Bericht gebucht wurden.                                                               |
|       Abschreibungen: Periodenabgänge       |                                                                       Die Summe aller Abschreibungsumkehrungen, die gebucht wurden, die eine Abgangstransaktion während des Datumsbereichs für den Bericht hatten.                                                                        |
|        Abschreibungen: Abschlusswert         |  Die Summe aller Transaktionen der Typen <strong>Abschreibung</strong>, <strong>Abschreibungsregulierung</strong>, <strong>Sonderabschreibung</strong> und <strong>Außerordentliche Abschreibung</strong> bis zum Datum „Bis”, das im Bericht angegeben ist.  |
|    Höherbewertungen/Niedrigerbewertungen: Eröffnungswert     |                              Die Summe aller Transaktionen der Typen <strong>Höherbewertungsregulierung</strong>, <strong>Niedrigerbewertungsregulierung</strong> und <strong>Neubewertung</strong> bis zum Datum „Von”, das im Bericht angegeben wird.                               |
|   Höherbewertungen/Niedrigerbewertungen: Periodenhöherbewertungen   |                                                                    Die Summe aller Transaktionen des Typs <strong>Höherbewertungsregulierung</strong>, die während des Datumsbereichs für den Bericht gebucht wurden.                                                                    |
|  Höherbewertungen/Niedrigerbewertungen: Periodenniedrigerbewertungen  |                                                                   Die Summe aller Transaktionen des Typs <strong>Niedrigerbewertungsregulierung</strong>, die während des Datumsbereichs für den Bericht gebucht wurden.                                                                   |
| Höherbewertungen/Niedrigerbewertungen: Periodenneubewertungen  |                                                                        Die Summe aller Transaktionen des Typs <strong>Neubewertung</strong>, die während des Datumsbereichs für den Bericht gebucht wurden.                                                                        |
|   Höherbewertungen/Niedrigerbewertungen: Periodenabgänge   |                                                           Die Summe aller Höherbewertungs-, Niedrigerbewertungs- und Neubewertungsumkehrungen, die gebucht wurden, die eine Abgangstransaktion während des Datumsbereichs für den Bericht hatten.                                                           |
|    Höherbewertungen/Niedrigerbewertungen: Abschlusswert     |                               Die Summe aller Transaktionen der Typen <strong>Höherbewertungsregulierung</strong>, <strong>Niedrigerbewertungsregulierung</strong> und <strong>Neubewertung</strong> bis zum Datum „Bis”, das im Bericht angegeben wird.                                |
|          Abgänge: Abgangsdatum           |                                                                                                                Das Abgangsdatum für das Anlagenbuch.                                                                                                                |
|    Abgänge: Nettobuchwert bei Abgang    |                                                                                                    Der Nettobuchwert des Anlagenbuches zum Zeitpunkt des Abgangs.                                                                                                    |
|            Abgänge: Verkaufswert            |                                                                                               Der Verkaufswert für das Anlagenbuch mit einem Abgang – Verkaufstransaktion.                                                                                                |
|           Abgänge: Verschrottungswert            |                                                                                               Der Verschrottungswert für das Anlagenbuch mit einem Abgang – Verschrottungstransaktion.                                                                                               |
|           Abgänge: Gewinn/Verlust            |                                                                                 Der Gewinn- oder Verlustwert, der als Teil der Abgangstransaktion für das Anlagenbuch berechnet wird.                                                                                 |


