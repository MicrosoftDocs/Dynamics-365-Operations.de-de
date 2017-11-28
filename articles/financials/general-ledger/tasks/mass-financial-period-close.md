--- 
title: Massen-Finanzperiodenabschluss
description: "Dieses Verfahren zeigt, wie eine Periode als \"Gesperrt\" oder \"Permanent geschlossen\" oder für mehrere juristische Person auf einmal festgelegt wird."
author: aprilolson
manager: AnnBe
ms.date: 10/25/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ef3cad6538d9efbd1c1881f4b7d771382d9b1ba8
ms.openlocfilehash: 1954bfdf4807e91d275e3a1ba80f959bdf9464a8
ms.contentlocale: de-de
ms.lasthandoff: 10/26/2017

---
# <a name="mass-financial-period-close"></a>Massen-Finanzperiodenabschluss

[!include[task guide banner](../../includes/task-guide-banner.md)]

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


