---
title: Schwellenwert und Ausnahmeschwellenwert
description: Dieses Thema beschreibt die Schwellenwerte und Ausnahmeschwellenwerte für die Quellenbesteuerung (TDS).
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 1bf0d3a01ede559d288581d3b58b3777d0e608dc
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023262"
---
# <a name="threshold-limit-and-exception-threshold-limit"></a>Schwellenwert und Ausnahmeschwellenwert

[!include [banner](../includes/banner.md)]

Dieses Thema beschreibt die Schwellenwerte und Ausnahmeschwellenwerte für die Quellenbesteuerung (TDS). Die TDS für Rechnungen und Zahlungen wird immer unter Berücksichtigung des Schwellenwerts und des Ausnahmeschwellenwerts berechnet, die für die TDS-Steuerkomponenten auf der Seite **Quellensteuerkomponenten** festgelegt sind. Die TDS-Steuerkomponenten sind den TDS-Steuercodes zugeordnet, die in den TDS-Steuergruppen enthalten sind. Die TDS-Steuergruppen sind Kreditoren und Debitoren zugeordnet, um TDS auf Rechnungs- oder Zahlungsebene zu berechnen.

Die TDS wird berechnet, wenn der Betrag für eine Buchung oder die kumulierten Buchungen, die mit einer bestimmten TDS-Gruppe für einen Kreditor gebucht wurden, den auf der Seite **Quellensteuerkomponenten** festgelegten Schwellenwert überschreitet. Die TDS wird erst berechnet, wenn der kumulierte Buchungsbetrag den angegebenen Schwellenwert überschreitet.

Wenn ein Ausnahmeschwellenwert sowie der Schwellenwert für eine TDS-Komponente angegeben wird, wird die TDS berechnet, wenn ein bestimmter Buchungsbetrag den Ausnahmeschwellenwert überschreitet, auch wenn der kumulierte Buchungsbetrag den angegebenen Schwellenwert nicht überschreitet.

### <a name="example"></a>Beispiel
Eine Steuerkomponente namens TDS wird eingerichtet und einer TDS-Steuergruppe namens Auftragnehmer zugeordnet. Der Schwellenwert wurde für die TDS-Steuerkomponente auf 50.000 und der Ausnahmeschwellenwert auf 20.000 festgelegt. Der Auftragnehmer der TDS-Gruppe ist als Standard-TDS-Gruppe für Kreditor 1 definiert.

Eine Einkaufsrechnung 001 wird für 10.000 für Kreditor 1 gebucht. Die TDS wird für die Rechnung nicht berechnet, da der Rechnungsbetrag den Schwellenwert bzw. den Ausnahmeschwellenwert nicht überschreitet. Eine Einkaufsrechnung 002 wird für 25.000 für Kreditor 1 gebucht. Die TDS wird für die Rechnung berechnet, da der Rechnungsbetrag den Ausnahmeschwellenwert überschreitet. Eine Einkaufsrechnung 003 wird für 20.000 für Kreditor 1 gebucht. Die TDS wird für die Rechnung berechnet, da der Gesamtrechnungsbetrag der drei Rechnungen, die für den Kreditor ausgestellt wurden, den Schwellenwert überschreitet. Die TDS wird für alle Rechnungen berechnet, die für den Kreditor ausgestellt wurden, für den die TDS nicht bereits berechnet wurde. Daher wird die TDS für 30.000 berechnet, was dem Gesamtrechnungsbetrag der Rechnungen 001 und 003 entspricht.

Der Schwellenwert und der Ausnahmeschwellenwert werden für die TDS-Berechnung nicht berechnet, wenn die Option **Schwellenwert übersehen** für TDS-Steuercodes in der TDS-Gruppe ausgewählt ist, die der Buchung zugeordnet ist. Der Schwellenwert wird in den TDS-Steuercodes in der TDS-Gruppe nicht verwendet, für die **Schwellenwert übersehen** aktiviert ist.

Wenn das Kontrollkästchen **Schwellenwert übersehen** für eine bestimmte TDS-Gruppe für einige Rechnungen aktiviert ist, für andere Rechnungen, die für einen bestimmten Kunden/Debitor erstellt wurden, jedoch nicht aktiviert ist, erfolgt die TDS-Berechnung für einige Rechnungen ohne Übersehen des Schwellenwerts, wobei der kumulierte Betrag für alle Rechnungen berücksichtigt wird, für die die TDS noch nicht berechnet wurde.

Beispiel: Der Schlwellenwert liegt bei 25.000. Für Kreditor A werden die folgenden Rechnungen erstellt.

- Rechnung 1 – 20.000 – (Kontrollkästchen **Schwellenwert übersehen** ist nicht aktiviert): TDS wird nicht berechnet.

- Rechnung 2 – 4.000 – (Kontrollkästchen **Schwellenwert übersehen** ist aktiviert): TDS wird für 4.000 berechnet.

- Rechnung 2 – 3.000 – (Kontrollkästchen **Schwellenwert übersehen** ist nicht aktiviert): Die TDS wird berechnet, da der kumulierte Rechnungsbetrag, d. h. 27.000 (20.000 + 4.000 + 3.000), den Schwellenwert überschreitet. Die TDS wird auf der Grundlage des kumulierten Rechnungsbetrags berechnet, für den die TDS nicht bereits berechnet wurde, also 23.000 (20.000 + 3.000).
