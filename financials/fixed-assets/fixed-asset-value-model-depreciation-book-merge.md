---
title: "Anlagewertmodel und Abschreibungsbuchzusammenführung"
description: "In älteren Versionen die aus zwei Bewertungskonzepte für Anlagen - Wertmodelle und Abschreibungsbücher. In Microsoft Dynamics 365 zur Freigabe der Arbeitsgänge 1611, werden die Wertmodellfunktionen und die funktionen Abschreibungsbuch in ein einzelnes Konzept zusammengeführt wurde, als das Buch bezeichnet."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 221564
ms.assetid: 7c68eb7c-8b1a-4dd9-afb8-04b4040e305e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 6c8c005c7f5ede54ce0b6c8114cac69e2551d467
ms.lasthandoff: 03/31/2017


---

# <a name="fixed-asset-value-model-and-depreciation-book-merge"></a>Anlagewertmodel und Abschreibungsbuchzusammenführung

In älteren Versionen die aus zwei Bewertungskonzepte für Anlagen - Wertmodelle und Abschreibungsbücher. In Microsoft Dynamics 365 zur Freigabe der Arbeitsgänge 1611, werden die Wertmodellfunktionen und die funktionen Abschreibungsbuch in ein einzelnes Konzept zusammengeführt wurde, als das Buch bezeichnet.

Die neue Buchfunktionalität basiert auf einer früheren Wertmodellfunktionalität, aber sie umfasst auch die gesamte Funktionalität, die zuvor nur in Abschreibungsbüchern bereitgestellt wurde. [![als Buch Zusammenführung aus Wertmodell und Abschreibungsbuchfunktionen]" . /media/fixed-assets.png)]". /media/fixed-assets.png) Verwalten, deswegen Sie können einen einzelnen Satz Seiten, Abfragen und Berichten für alle Ihre Anlagenprozesse nun können zusammen verwendet werden. Die Tabellen in diesem Thema beschrieben die vorhergehende Funktionalität für Abschreibungsbücher und Wertmodelle, zusammen mit der neuen Funktionalität für Bücher.

## <a name="setup"></a>Einstellung
Standardmäßig buchen Bücher sowohl in das Hauptbuch als auch in das untergeordnete Anlagensachkonto. Bücher haben eine neue Option **Ins Hauptbuch buchen**. Mit ihr können Sie Buchungen in das Hauptbuch deaktivieren und nur in das untergeordnete Anlagensachkonto buchen. Diese Funktionalität ähnelt dem früheren Buchungsverhalten für Abschreibungsbücher. Das Erfassungsnamenssetup hat eine neue Buchungsebene mit der Bezeichnung „Keine”. Diese Buchungsebene wurde speziell für Anlagenbuchungen hinzugefügt. Um Buchungen für Bücher zu buchen die nicht auf das Hauptkonto buchen, müssen Sie einen Erfassungsnamen verwenden, bei dem die Buchungsebene auf **Keine** festgelegt ist.

|                                                  |                                 |                                 |                                                         |
|--------------------------------------------------|---------------------------------|---------------------------------|---------------------------------------------------------|
|                                                  | Abschreibungsbuch               | Wertmodell                     | Buch (neu)                                              |
| Zum Hauptbuch buchen                                   | Nie                           | Immer                          | Option, zum Hauptbuch zu buchen                                |
| Buchungsebenen                                   | Nicht zutreffend                  | 3: Aktuell, Vorgänge und Steuer | 11: Aktuell, Vorgänge, Steuern, 7 benutzerdefinierte Ebenen und Keine |
| Journale                                    | Abschreibungsbuch-Journale | Hauptbuch – Erfassungsnamen              | Hauptbuch – Erfassungsnamen                                      |
| Abgeleitete Bücher                                    | Nicht zulässig                     | Zulässig                         | Zulässig                                                 |
| Abschreibungsprofilaußerkraftsetzung auf der Anlagenebene | Zulässig                         | Nicht zulässig                     | Zulässig                                                 |

## <a name="processes"></a>Prozesse
Prozesse verwenden jetzt eine gemeinsame Seite. Einige Prozesse sind nur zulässig, wenn die Option **Ins Hauptbuch buchen** in den Bucheinstellungen auf **Nein** festgelegt ist.

|                                |                           |                     |                                          |
|--------------------------------|---------------------------|---------------------|------------------------------------------|
|                                | Abschreibungsbuch         | Wertmodell         | Buch (neu)                               |
| Buchungseintrag              | Abschreibungsbuch-Journal | Anlagenerfassung | Anlagenerfassung                      |
| Vorzeitige Abschreibung             | Zulässig                   | Nicht zulässig         | Zulässig                                  |
| Historische Buchungen löschen | Zulässig                   | Nicht zulässig         | Zulässig, es sei denn, Sie buchen zum Hauptbuch |
| Massenaktualisierung                    | Zulässig                   | Nicht zulässig         | Zulässig, es sei denn, Sie buchen zum Hauptbuch |

## <a name="inquiries-and-reports"></a>Abfragen und Berichte
Abfragen und Berichte unterstützen alle Bücher. Berichte, die in der folgenden Tabelle nicht einbezogen sind, unterstützten zuvor beide Abschreibungsbücher und Wertmodelle und unterstützen jetzt weiterhin alle Buchtypen. Das Feld **Buchungsebene** ist auch Berichten hinzugefügt worden, sodass Sie die Transaktionsbuchungen leichter identifizieren können.

|                                       |                                |                          |                          |
|---------------------------------------|--------------------------------|--------------------------|--------------------------|
|                                       | Abschreibungsbuch              | Wertmodell              | Buch (neu)               |
| Abfragen                             | Abschreibungsbuchbuchungen | Anlagenbuchungen | Anlagenbuchungen |
| Anlagenspiegel                 | Nicht zulässig                    | Zulässig                  | Zulässig                  |
| Anlagenbasis                     | Zulässig                        | Nicht zulässig              | Zulässig                  |
| Anwendbarkeit in Quartalsmitte für Anlagen | Zulässig                        | Nicht zulässig              | Zulässig                  |

## <a name="upgrade"></a>Upgrade durchführen
Durch den Upgradeprozess werden Ihre vorhandenen Einstellungen und alle Ihre vorhandenen Transaktionen zur neuen Buchstruktur verschoben. Wertmodelle bleiben, wie sie zurzeit sind, als Buch, das zum Hauptbuch bucht. Allerdings werden Abschreibungsbücher zu einem Buch verschoben, bei dem die Option **Ins Hauptbuch buchen** auf **Nein** festgelegt ist. Abschreibungsbuch-Erfassungsnamen werden zu einem Hauptbuch-Erfassungsnamen verschoben, bei dem die Buchungsebene auf **Keine** festgelegt ist.


