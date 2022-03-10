---
title: Nachkalkulationsbögen
description: 'Durch die Einrichtung des Nachkalkulationsbogens werden zwei Ziele verfolgt: Zum einen wird das Format definiert, das zum Anzeigen von Wareneinsatzinformationen für einen produzierten Artikel oder einen Produktionsauftrag verwendet wird. Die formatierte Anzeige wird als Nachkalkulationsbogen bezeichnet. Zum anderen wird die Grundlage für die Berechnung indirekter Kosten definiert. Die Einstellungen des Nachkalkulationsbogens basieren auf der Kostengruppenfunktion für die Informationsanzeige sowie für die Berechungsformeln für indirekte Kosten. In diesem Artikel werden die beiden Ziele des Nachkalkulationsbogens beschrieben:'
author: AndersGirke
ms.date: 11/18/2021
ms.topic: article
ms.search.form: CostSheetDesigner, CostSheetCalculationFactor
audience: Application User
ms.reviewer: kamaybac
ms.custom: 53201
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 64b8a9b8b29193f25e706e52424de2af3454aec8
ms.sourcegitcommit: f11ad8d7ee8a4d2ee1a1bb601622b50e14955c4a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/18/2021
ms.locfileid: "7825357"
---
# <a name="costing-sheets"></a>Nachkalkulationsbögen

[!include [banner](../includes/banner.md)]

Durch die Einrichtung des Nachkalkulationsbogens werden zwei Ziele verfolgt: Zum einen wird das Format definiert, das zum Anzeigen von Wareneinsatzinformationen für einen produzierten Artikel oder einen Produktionsauftrag verwendet wird. Die formatierte Anzeige wird als Nachkalkulationsbogen bezeichnet. Zum anderen wird die Grundlage für die Berechnung indirekter Kosten definiert. Die Einstellungen des Nachkalkulationsbogens basieren auf der Kostengruppenfunktion für die Informationsanzeige sowie für die Berechungsformeln für indirekte Kosten. In diesem Artikel werden die beiden Ziele des Nachkalkulationsbogens beschrieben: 

In der folgenden Tabelle sind die standardmäßigen Sicherheitsrollen aufgeführt, die auf Kalkulationstabellen zugreifen können, einschließlich der Zugriffsebene, die jeder Rolle durch die Standardeinstellungen gewährt wird.

| Rolle | Zugriff
|---|---|
| Leiter Buchhaltung | Bearbeiten |
| Sachbearbeiter Bestandsbuchhaltung | Anzeigen |
| Bestandsbuchhalter | Anzeigen |

Ein Nachkalkulationsbogen ist die formatierte Anzeige von Informationen zu den Kosten von Waren, die für einen produzierten Artikel oder einen Produktionsauftrag verkauft werden. Wenn Sie einen Nachkalkulationsbogen einrichten, definieren Sie das Format für die Informationen und die Basis für die Berechnung indirekter Kosten. Die Einstellungen des Nachkalkulationsbogens basieren auf der Kostengruppenfunktion für die Informationsanzeige sowie für die Berechungsformeln für indirekte Kosten. Nachfolgend finden Sie weitere Informationen über die zwei Ziele der Einstellungen des Nachkalkulationsbogens:

- **Definieren des Formats für den Nachkalkulationsbogen.** Das benutzerdefinierte Format eines Nachkalkulationsbogens ermöglicht die Identifizierung der Segmentierung von Kosten, die den Wareneinsatz eines produzierten Artikels enthalten. Beispielsweise können die Wareneinsatzinformationen eines Artikels auf Basis von Kostengruppen in Material, Arbeit und Gemeinkosten segmentiert werden. Diese Kostengruppen werden Artikeln, Kostenkategorien für die Arbeitsgangsteuerung und Formeln zur Berechnung indirekter Kosten zugewiesen. Das Format für den Nachkalkulationsbogen erfordert in der Regel die Verwendung von Zwischensummen, wenn mehrere Kostengruppen definiert wurden. So können mehrere Kostengruppen, die Material zugeordnet sind, zusammengefasst werden. Das Definieren eines Formats für den Nachkalkulationsbogen ist optional, zur Berechnung indirekter Kosten muss es jedoch definiert werden.
- **Definieren Sie die Basis für die Berechnung indirekter Kosten.** Indirekte Kosten sind die materialbasierten Gemeinkosten, die der Produktion eines produzierten Artikels zugeordnet sind. Eine Berechnungsformel für indirekte Kosten kann als Zuschlag oder als Satz ausgedrückt werden. Bei einem Zuschlag handelt es sich um den prozentualen Anteil eines Werts, bei einem Satz handelt es sich dagegen um einen stundenbasierten Betrag für einen Arbeitsgang des Arbeitsplans. Eine Kostengruppe bildet die Grundlage für die Berechnungsformel. Das kann beispielsweise ein Zuschlag von 100 Prozent für die Kostengruppe "Arbeit" oder ein Stundensatz von EUR 50,00 für die Kostengruppe "Maschine" sein. Zum Definieren einer Berechungsformel und der entsprechenden Kostengruppengrundlage ist im Rahmen der Einrichtung des Nachkalkulationsbogens die Kennzeichnung der Kostengruppe für die Gemeinkosten erforderlich. Zudem muss ausgewählt werden, ob Zuschläge oder Sätze verwendet werden sollen.

Jede Berechnungsformel muss in Form eines Kostendatensatzes eingegeben werden. Der Kostendatensatz enthält eine angegebene Nachkalkulationsversion, einen Zuschlagsprozentsatz oder einen Satzbetrag, die Grundlage für die Kostengruppe, einen Status sowie ein Gültigkeitsdatum. Wenn ein Kostendatensatz das erste Mal eingeben wird, hat er den Status **Ausstehend** sowie ein Gültigkeitsdatum. Bei Aktivierung des Kostendatensatzes wird der aktualisiert, so dass der Datensatz der aktuell aktive Datensatz ist, und das Gültigkeitsdatum auf das Aktivierungsdatum aktualisiert wird. Der Kostendatensatz kann außerdem oder eine standortspezifische Berechnungsformel angeben. Alternativ können Sie das Feld **Standort** leer lassen, um anzugeben, dass die Berechnungsformel eine unternehmensweite Formel ist. Optional kann der Kostendatensatz aus einem angegebenen Artikel oder aus einer angegebenen Artikelgruppe bestehen, wenn die Berechnungsformel als "Pro Artikel Formel" gekennzeichnet ist. 

Der zurzeit aktive Kostendatensatz der Berechungsformeln für indirekte Kosten dient zur Vorkalkulation der Kosten für Produktionsaufträge. Er dient außerdem zur Berechnung der Istkosten, die sich auf den Istverbrauch von Zeit und Material beziehen. Die Datensätze für ausstehende Kosten werden für die Stücklistenkalkulationen eines späteren Datums verwendet. 

Anhand zweier Sperrrichtlinien für Nachkalkulationsversionen wird bestimmt, ob ausstehende Kosten verwaltet und ob die ausstehenden Kosten aktiviert werden können. Ermöglichen Sie mithilfe der Sperrrichtlinien die Verwaltung von Daten, und sperren Sie anschließend die Datenverwaltung für die Kostendaten innerhalb einer Nachkalkulationsversion. 

Nach dem Definieren des Formats für den Nachkalkulationsbogen sowie nach den Berechnungen für indirekte Kosten müssen die Informationen in einem separaten Schritt geprüft und gespeichert werden. Bei dem Nachkalkulationsbogen handelt es sich um ein unternehmensweites Format zur einheitlichen Anzeige der Wareneinsatzinformationen. 

Der Nachkalkulationsbogen wird als Teil der Seite **Artikelkosten berechnen** angezeigt. Dieses Formular wird für den Datensatz mit berechneten Kosten eines produzierten Artikels auf der Seite **Artikelpreis** oder für einen Datensatz mit auftragsspezifischen Berechnungen auf der Seite **Ergebnisse der Herstellkostenkalkulation** aufgerufen. Der Nachkalkulationsbogen kann auch als Teil der der Seite **Preiskalkulations** für einen Produktionsauftrag angezeigt.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
