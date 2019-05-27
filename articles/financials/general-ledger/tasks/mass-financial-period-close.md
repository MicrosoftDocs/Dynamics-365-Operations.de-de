---
title: Massen-Finanzperiodenabschluss
description: Dieses Verfahren zeigt, wie eine Periode als "Gesperrt" oder "Permanent geschlossen" oder für mehrere juristische Person auf einmal festgelegt wird.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerCalendar, LedgerPeriodModuleAccessControlUpdate, SysLookupPicklist, LedgerFiscalCalendarPeriodStatus
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a2988b7ab0837cc9a3e4f1c4eaf3fe6e219fa721
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564480"
---
# <a name="mass-financial-period-close"></a>Massen-Finanzperiodenabschluss

[!include [task guide banner](../../includes/task-guide-banner.md)]

Dieses Verfahren zeigt, wie eine Periode als "Gesperrt" oder "Permanent geschlossen" oder für mehrere juristische Person auf einmal festgelegt wird. Darüber hinaus zeigt die Aufgabe, wie die Benutzergruppenbuchun auf bestimmte Module beschränkt wird.

1. Wechseln Sie zu Hauptbuch > Zeitraum geschlossen > Hauptbuch.
    * Beachten Sie, dass die Liste der angezeigten juristischen Personen vom auf der Seite ausgewählten Steuerkalender abhängig ist. Nur juristischen Personen, die den ausgewählten Steuerkalender verwenden, werden angezeigt.  
2. Klicken Sie auf "Bearbeiten".
3. Wählen Sie den Zeitraum aus, für den Sie den Status ändern möchten.
4. Wählen Sie die juristischen Personen aus, für den Sie den Status aktualisieren möchten.
    * Sie können schnell alle juristischen Personen auswählen, indem Sie das Kontrollkästchen in der oberen linken Seite des Formulars auswählen.  
5. Wählen Sie "Modulzugriff aktualisieren" aus, um den Buchungszugriff mit einem bestimmten Modul zu definieren.
    * Der Modulstatus kann auch einzeln aktualisiert werden, indem die Datensätze des Rasters bearbeitet werden. Die Schaltfläche ist hilfreich, wenn Sie mehrere Datensätze der juristischen Person schnell aktualisieren möchten.  
6. Wählen Sie im Feld Anwendungsmodul das Modul aus, für das Sie den Status aktualisieren möchten. Klicken Sie auf Auswählen.
7. Wählen Sie in Zugriffsebene aus Alle, Keine oder eine bestimmte Benutzergruppe aus. Klicken Sie auf Auswählen.
    * "Alle" legt fest, dass alle Benutzer mit Bearbeitungszugriff auf das Modul buchen können wenn die Periode offen ist. "Keine" legt fest, dass Benutzer nicht im Modul buchen können, wenn die Periode offen ist. Eine bestimmte Benutzergruppe gibt an, das nur Benutzer der Gruppe im Modul buchen dürfen, wenn die Periode geöffnet ist.  
8. Klicken Sie auf Aktualisieren.
9. Wählen Sie eine andere Periode aus, um den Status zu aktualisieren.
10. Wählen Sie die juristischen Personen aus, für den Sie die Periode aktualisieren möchten.
11. Wählen Sie "Periodenstatus Aktualisierung" aus und legen Sie den Status auf "Gesperrt", "Offen" oder "Permanent geschlossen" fest.
    * "Offen" legt fest, das für die Periode gebucht werden kann, vorausgesetzt der Benutzer hat Zugriff. "Gesperrt" bedeutet, dass nicht in den Zeitraum gebucht werden kann, aber der Zeitraum erneut geöffnet werden kann. "Permanent geschlossen" bedeutet, das der Zeitraum abgeschlossen ist und nicht geöffnet werden kann. Regulierungen können nicht gebucht werden. Wir empfehlen nicht, einen Zeitraum auf "Permanent geschlossen" festzulegen, bis alle Anpassungen und Audits abgeschlossen wurden.  
12. Klicken Sie auf Aktualisieren.

