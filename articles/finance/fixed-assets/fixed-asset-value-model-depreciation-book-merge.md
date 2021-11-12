---
title: Anlagewertmodel und Abschreibungsbuchzusammenführung
description: 'In älteren Versionen gab es zwei Bewertungskonzepte für Anlagen: Wertmodelle und Abschreibungsbücher. In der Microsoft Dynamics 365 for Operations-Version 1611 wurden die Wertmodellfunktionalität und die Abschreibungsbuchfunktionalität zu einem einzigen Konzept zusammengeführt, das als Buch bekannt ist.'
author: moaamer
ms.date: 10/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 221564
ms.assetid: 7c68eb7c-8b1a-4dd9-afb8-04b4040e305e
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 9b11edcbf03b0917e35d9cef03834629b7b67fad
ms.sourcegitcommit: 1707cf45217db6801df260ff60f4648bd9a4bb68
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/23/2021
ms.locfileid: "7674925"
---
# <a name="fixed-asset-value-model-and-depreciation-book-merge"></a>Anlagewertmodell und Abschreibungsbuchzusammenführung

[!include [banner](../includes/banner.md)]

In diesem Thema wird die aktuelle Buchfunktion in Anlagen beschrieben. Diese neue Buchfunktionalität basiert auf der Wertmodellfunktionalität, die in früheren Versionen verfügbar war, aber sie umfasst auch die gesamte Funktionalität, die zuvor nur in Abschreibungsbüchern bereitgestellt wurde.

Mit der Buchfunktion können Sie einen einzigen Satz von Seiten, Abfragen und Berichten für alle Anlageprozesse Ihres Unternehmens verwenden. Die Tabellen in diesem Thema beschrieben die vorhergehende Funktionalität für Abschreibungsbücher und Wertmodelle, zusammen mit der aktuellen Funktionalität für Bücher.

## <a name="setup"></a>Einrichtung
Standardmäßig buchen Bücher sowohl in das Hauptbuch als auch in das untergeordnete Anlagensachkonto. Bücher haben eine neue Option **Ins Hauptbuch buchen**. Mit ihr können Sie Buchungen in das Hauptbuch deaktivieren und nur in das untergeordnete Anlagensachkonto buchen. Diese Funktionalität ähnelt dem früheren Buchungsverhalten für Abschreibungsbücher. Das Erfassungsnamenssetup hat eine neue Buchungsebene mit der Bezeichnung „Keine”. Diese Buchungsebene wurde speziell für Anlagenbuchungen hinzugefügt. Um Buchungen für Bücher zu buchen die nicht auf das Hauptkonto buchen, müssen Sie einen Erfassungsnamen verwenden, bei dem die Buchungsebene auf **Keine** festgelegt ist.


| &nbsp;                                           | Abschreibungsbuch               | Wertmodell                     | Buch (neu)                                              |
|--------------------------------------------------|---------------------------------|---------------------------------|---------------------------------------------------------|
| In Hauptbuch buchen                                   | Nie                           | Immer                          | Option zum Buchen ins Hauptbuch                                |
| Buchungsebenen                                   | Nicht zutreffend                  | 3: Aktuell, Vorgänge und Steuer | 11: Aktuell, Vorgänge, Steuern, 7 benutzerdefinierte Ebenen und Keine |
| Journale                                    | Abschreibungsbuch-Journale | Hauptbuch – Erfassungsnamen              | Hauptbuch – Erfassungsnamen                                      |
| Abgeleitete Bücher                                    | Nicht zulässig                     | Zulässig                         | Zulässig                                                 |
| Abschreibungsprofilaußerkraftsetzung auf der Anlagenebene | Zulässig                         | Nicht zulässig                     | Zulässig                                                 |

## <a name="processes"></a>Prozesse
Prozesse verwenden jetzt eine gemeinsame Seite. Einige Prozesse sind nur zulässig, wenn die Option **Ins Hauptbuch buchen** in den Bucheinstellungen auf **Nein** festgelegt ist.

| &nbsp;                                           | Abschreibungsbuch               | Wertmodell                     | Buch (neu)                                              |
|--------------------------------|---------------------------|---------------------|------------------------------------------|
| Buchungseintrag              | Abschreibungsbuch-Journal | Anlagenerfassung | Anlagenerfassung                      |
| Vorzeitige Abschreibung             | Zulässig                   | Nicht zulässig         | Zulässig                                  |
| Historische Buchungen löschen | Zulässig                   | Nicht zulässig         | Zulässig, es sei denn, Sie buchen zum Hauptbuch |
| Massenaktualisierung                    | Zulässig                   | Nicht zulässig         | Zulässig, es sei denn, Sie buchen zum Hauptbuch |

## <a name="inquiries-and-reports"></a>Abfragen und Berichte
Abfragen und Berichte unterstützen alle Bücher. Berichte, die in der folgenden Tabelle nicht einbezogen sind, unterstützten zuvor beide Abschreibungsbücher und Wertmodelle und unterstützen jetzt weiterhin alle Buchtypen. Das Feld **Buchungsebene** ist auch Berichten hinzugefügt worden, sodass Sie die Transaktionsbuchungen leichter identifizieren können.

| &nbsp;                                           | Abschreibungsbuch               | Wertmodell                     | Buch (neu)                                              |
|---------------------------------------|--------------------------------|--------------------------|--------------------------|
| Abfragen                             | Abschreibungsbuchbuchungen | Anlagenbuchungen | Anlagenbuchungen |
| Anlagenspiegel                 | Nicht zulässig                    | Zulässig                  | Zulässig                  |
| Anlagenbasis                     | Zulässig                        | Nicht zulässig              | Zulässig                  |
| Anwendbarkeit in Quartalsmitte für Anlagen | Zulässig                        | Nicht zulässig              | Zulässig                  |

## <a name="upgrade"></a>Upgrade durchführen
Durch den Upgradeprozess werden Ihre vorhandenen Einstellungen und alle Ihre vorhandenen Transaktionen zur neuen Buchstruktur verschoben. Wertmodelle bleiben, wie sie zurzeit sind, als Buch, das zum Hauptbuch bucht. Allerdings werden Abschreibungsbücher zu einem Buch verschoben, bei dem die Option **Ins Hauptbuch buchen** auf **Nein** festgelegt ist. Abschreibungsbuch-Erfassungsnamen werden zu einem Hauptbuch-Erfassungsnamen verschoben, bei dem die Buchungsebene auf **Keine** festgelegt ist.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
