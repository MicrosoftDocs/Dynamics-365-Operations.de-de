---
title: Massen-Finanzperiodenabschluss
description: Dieses Thema zeigt, wie Sie einen Zeitraum zurückstellen oder dauerhaft schließen können, oder wie Sie mehr als eine juristische Person auf einmal.
author: aprilolson
manager: AnnBe
ms.date: 08/16/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerCalendar, LedgerPeriodModuleAccessControlUpdate, SysLookupPicklist, LedgerFiscalCalendarPeriodStatus
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a149b35c6964166207effc799a02cd4c59bbb843
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144981"
---
# <a name="mass-financial-period-close"></a>Massen-Finanzperiodenabschluss

[!include [banner](../../includes/banner.md)]

Dieses Thema zeigt, wie Sie einen Zeitraum zurückstellen oder dauerhaft schließen können, oder wie Sie mehr als eine juristische Person auf einmal. Darüber hinaus zeigt die Aufgabe, wie die Benutzergruppenbuchun auf bestimmte Module beschränkt wird.

1. Gehen Sie im Navigationsbereich zu **Module > Hauptbuch > Periodenabschluss > Sachkonto-Kalender**. Beachten Sie, dass die Liste der angezeigten juristischen Personen vom auf der Seite ausgewählten Steuerkalender abhängig ist. Nur juristischen Personen, die den ausgewählten Steuerkalender verwenden, werden angezeigt.
2. Wählen Sie **Bearbeiten** aus.
3. Wählen Sie den Zeitraum aus, für den Sie den Status ändern möchten.
4. Wählen Sie die juristischen Personen aus, für den Sie den Status aktualisieren möchten. Sie können alle Rechtspersonen schnell auswählen, indem Sie das Häkchen oben links im Raster markieren.  
5. Wählen Sie **Aktualisierungsmodulzugriff**, um den Buchungszugriff auf ein ausgewähltes Modul zu definieren. Der Modulstatus kann auch einzeln aktualisiert werden, indem die Datensätze des Rasters bearbeitet werden. Die Schaltfläche ist hilfreich, wenn Sie mehrere Datensätze der juristischen Person schnell aktualisieren möchten.  
6. Wählen Sie im Modul **Anwendung** das Modul aus, für das Sie den Status aktualisieren möchten. Klicken Sie auf **Auswählen**.
7. Wählen Sie in der Ebene **Zugang** **Alle**, **Keine** oder eine bestimmte Benutzergruppe. Klicken Sie auf **Auswählen**. "Alle" legt fest, dass alle Benutzer mit Bearbeitungszugriff auf das Modul buchen können wenn die Periode offen ist. "Keine" legt fest, dass Benutzer nicht im Modul buchen können, wenn die Periode offen ist. Eine bestimmte Benutzergruppe gibt an, das nur Benutzer der Gruppe im Modul buchen dürfen, wenn die Periode geöffnet ist.  
8. Wählen Sie **Aktualisieren**.
9. Wählen Sie eine andere Periode aus, um den Status zu aktualisieren.
10. Wählen Sie die juristischen Personen aus, für den Sie die Periode aktualisieren möchten.
11. Wählen Sie **Periodenstatus aktualisieren** und setzen Sie den Status von **Ein Halten**, **Öffnen** oder **Dauerhaft geschlossen**. **Offen** zeigt an, dass der Zeitraum gebucht werden kann, sofern der Benutzer Zugriff hat. **Einbehalten** bedeutet, dass die Periode nicht bebucht werden kann, aber die Periode wieder geöffnet werden kann. **Dauerhaft geschlossen** bedeutet, dass die Periode geschlossen ist und nie geöffnet werden kann. Regulierungen können nicht gebucht werden. Wir empfehlen nicht, einen Zeitraum auf **Dauerhaft geschlossen** zu setzen, bis alle Anpassungen und Audits abgeschlossen sind.  
12. Wählen Sie **Aktualisieren**.

