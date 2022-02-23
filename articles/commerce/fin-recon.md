---
title: Finanzielle Abstimmung in Einzelhandelsgeschäften
description: In diesem Thema wird die finanzielle Abstimmung in Einzelhandelsgeschäften für POS für Microsoft Dynamics 365 Commerce beschrieben.
author: anpurush
manager: AnnBe
ms.date: 06/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-21
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8ddefcdc2b2bbb5fe25e9a87396802cbbbfef72c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965076"
---
# <a name="financial-reconciliation-in-retail-stores"></a>Finanzielle Abstimmung in Einzelhandelsgeschäften

[!include [banner](includes/banner.md)]

In Microsoft Dynamics 365 Commerce Version 10.0.10 und früher können Ladenangestellte und Filialleiter mit den vom POS-Client (Point of Sale, Verkaufsstelle) für Tagesendgeschäftsprozesse in Einzelhandelsgeschäften bereitgestellten Funktionen entsprechende Vorgänge durchführen. Beispielsweise können sie Kassenstürze durchführen, Schichten blind schließen, Schichttransaktionen abstimmen und Schichten schließen. POS bietet jedoch keine Möglichkeit, um die Finanzdaten für Schichten zu finalisieren, und kann somit zum Buchen der Finanzdaten in der Commerce-Zentrale verwendet werden. In der Regel sind die Filialleiter für diese Aufgabe verantwortlich. Bevor sie sich von einer Schicht abmelden können, müssen sie die Informationen überprüfen, erforderliche Korrekturen vornehmen und die Gesamtsummen für diese Schicht finalisieren. Die finalisierten Summen sollten dann in Finanzmodulen in der Commerce-Zentrale veröffentlicht werden.

Darüber hinaus können Filialleiter in Commerce Version 10.0.10 und früher die Auszugspositionen in der Commerce-Zentrale überprüfen und einige Anpassungen vornehmen. Die Funktionen sind jedoch begrenzt und Filialleiter haben selten Zugriff auf den Client der Commerce-Zentrale. Darüber hinaus kann die Überprüfung und Anpassung von Finanzaufstellungen im Einzelhandel nur dann erfolgen, wenn sie in der Commerce-Zentrale erstellt werden. Dieser Prozess läuft jedoch üblicherweise nachts ab. Daher müssen Filialleiter auf die Abmeldung von der Schicht warten, wenn Finanzaufstellungen für den Einzelhandel in der Commerce-Zentrale erstellt werden.

In Commerce Version 10.0.11 und höher können Filialleiter ihre Schichten im POS-Client selbst überprüfen, anpassen und finalisieren. Diese Daten werden dann verwendet, um Finanzaufstellungen für den Einzelhandel in der Commerce-Zentrale zu erstellen und zu veröffentlichen.

> [!NOTE]
> Die Funktionen, die sich auf die finanzielle Abstimmung in Einzelhandelsgeschäften beziehen, funktionieren nur, wenn die Auftragserstellung per Einzelzulauf aktiviert ist. Weitere Informationen finden Sie unter [Auftragserstellung per Einzelzulauf für Einzelhandelsgeschäftbuchungen](trickle-feed.md).

## <a name="set-up-financial-reconciliation"></a>Einrichten der finanziellen Abstimmung

Gehen Sie folgendermaßen vor, um die finanzielle Abstimmung zu verwenden.

1. Aktivieren Sie im Arbeitsbereich **Funktionsverwaltung** die Funktion **Einzelhandelsaufstellungen – Einzelzulauf**.
1. Legen Sie im POS-Funktionsprofil für das entsprechende Geschäft die Option **Finanzielle Abstimmung im Geschäft aktivieren** auf **Ja** fest.

## <a name="more-information-about-financial-reconciliation"></a>Weitere Informationen zur finanziellen Abstimmung

Wenn die finanzielle Abstimmung aktiviert ist, werden einige der Parameter, die auf dem Inforegister **Auszug/Abschluss** der Seite **Einzelhandelsgeschäfte** in der Commerce-Zentrale aktiviert sind, mit der Kanaldatenbank synchronisiert. Der gleiche Satz von Berechnungskriterien und Betragsschwellenwerten, der für Einzelhandelsaufstellungen verwendet wird, wird erzwungen.

Wenn der Vorgang **Schicht schließen** aufgerufen wird, überprüft das System, ob die vom System berechneten Beträge und die deklarierten Beträge übereinstimmen. Wenn sie sich unterscheiden und die Differenz die definierten Schwellenwerte überschreitet, wird der Benutzer aufgefordert, die erforderlichen Anpassungen vorzunehmen.

Anpassungen können für jede Auszugsposition vorgenommen werden. Wenn eine Auszugsposition ausgewählt wird, kann der Benutzer die Summen für verschiedene Transaktionstypen anzeigen und die Summen für einen bestimmten Transaktionstyp bearbeiten. Während der Bearbeitung zeigt das System den ursprünglich berechneten Betrag und den überschriebenen Betrag für diesen Transaktionstyp an. Der Benutzer kann im Rahmen des Bearbeitungsprozesses auch Notizen erfassen. Notizen können zu Prüfungszwecken verwendet werden.

Benutzer können die Validierungsaufforderungen und -meldungen ignorieren und die Schicht schließen. Wenn ein Benutzer die Validierungsaufforderungen jedoch ignoriert, treten dieselben Probleme auf und müssen behoben werden, wenn die Schicht Finanzaufstellungen in der Commerce-Zentrale veröffentlicht.

Der Vorgang **Schicht schließen** in POS überprüft außerdem, ob alle Transaktionen in der Offline-Datenbank mit der Kanaldatenbank synchronisiert werden. Wenn Transaktionen nicht synchronisiert werden, erhält der Benutzer eine Warnmeldung, da dieser Umstand dazu führen kann, dass die Systembeträge falsch berechnet werden. Der Benutzer kann den Vorgang **Schicht schließen** abbrechen und versuchen, die Offline-Transaktionen mit der Kanaldatenbank zu synchronisieren. Alternativ kann der Benutzer die vom System berechneten Beträge manuell anpassen, um die nicht synchronisierten Transaktionen zu berücksichtigen, sodass der richtige Satz von Finanzkennzahlen finalisiert und gebucht wird. 

Wenn die Buchung von Aufstellungen auf Basis von Einzelzuläufen verwendet wird, sodass die Buchung von Transaktionen von der Buchung von Finanzdaten getrennt ist, können Sie die vom System berechneten Beträge für fehlende Offline-Transaktionen anpassen. Auf diese Weise stellen Sie sicher, dass Finanzdaten unabhängig von fehlenden Transaktionen immer korrekt erfasst und gebucht werden. Offline-Transaktionen können mit der Kanaldatenbank und der Commerce-Zentrale synchronisiert und später getrennt von den Finanzbuchungen gebucht werden.

Details der finanziellen Abstimmung für eine Schicht werden mithilfe des P-Jobs mit der Commerce-Zentrale synchronisiert.

Finanzaufstellungen für den Einzelhandel in der Commerce-Zentrale berechnen keine Summen, um die Details in den Auszugspositionen anzuzeigen. Stattdessen werden die finalisierten Beträge im POS-Client zum Erstellen und Buchen von Finanzaufstellungen für den Einzelhandel verwendet.
