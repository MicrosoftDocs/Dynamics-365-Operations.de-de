---
title: Fehlerbehebung bei der Prozessfertigung
description: Dieses Thema beschreibt, wie Sie Probleme beheben können, die bei der Arbeit mit der Prozessfertigung auftreten können.
author: SmithaNataraj
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 13eb50ef634de211a864a3f27defe2276cb66f411480e2074693c8b8972a284b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6726704"
---
# <a name="troubleshoot-process-manufacturing"></a>Fehlersuche in der Prozessfertigung

Dieses Thema beschreibt, wie Sie Probleme beheben können, die bei der Arbeit mit der Prozessfertigung auftreten können.

## <a name="when-i-use-the-job-card-device-to-report-a-partial-quantity-on-the-last-job-in-a-production-order-all-the-previous-jobs-on-that-order-that-have-a-status-of-in-progress-are-automatically-ended"></a>Wenn ich das Jobkartengerät verwende, um eine Teilmenge für den letzten Auftrag in einem Produktionsauftrag zu melden, werden alle vorherigen Aufträge in diesem Auftrag, die den Status „In Bearbeitung“ haben, automatisch beendet.

Dieses Verhalten ist beabsichtigt. Auf der Seite **Produktionsauftragsvorgaben** gibt es auf der Registerkarte **Als beendet melden** eine Option, die **Arbeitsplan beenden** heißt. Wenn dieses Thema auf *Ja* festgelegt ist, wird eine Erfassung für den Arbeitsplan erstellt, wenn eine Arbeitskraft das Jobkartengerät oder das Jobkartenterminal verwendet, um den letzten Vorgang zu melden. Diese Erfassung kennzeichnet alle Vorgänge als abgeschlossen und beendet alle Produktionsaufträge. Wenn die Option **Arbeitsplan als beendet markieren** auf *Ja* festgelegt ist, berücksichtigt das System nicht den Auftragsstatus, den die Arbeitskraft ausgewählt hat, als sie den letzten Vorgang meldete. Das System berücksichtigt auch nicht, ob die Arbeitskraft eine volle oder eine Teilmenge meldet.

## <a name="when-i-attempt-a-stock-closing-i-receive-the-following-warning-message-no-execution-of-backflush-costing-calculation-with-a-date-1-matching-period-end-has-been-registered"></a>Wenn ich versuche, einen Lagerabschluss zu machen, erhalte ich die folgende Warnmeldung: „Es wurde keine Ausführung der Nachkalkulation mit einem Datum %1, das mit dem Periodenende übereinstimmt, registriert.“

In Versionen vor 10.0.13 erhalten Sie beim Bestandsabschluss die folgende fehlerhafte Warnmeldung, wenn Sie nicht den Lean Production Costing Flow verwenden:

> Sie sind dabei, einen Bestandsabschluss mit einem Datum %1 auszuführen. Es wurde keine Ausführung einer Nachkalkulation mit einem Datum %1 registriert, das dem Periodenende entspricht. Bitte denken Sie daran, eine Nachkalkulation mit einem Datum %1 auszuführen, das dem Periodenende entspricht. Die Bewertung der Bestände, der Selbstkosten und der Abweichungen ist möglicherweise im Nebenbuch oder im Hauptbuch nicht korrekt, bis dies ausgeführt wurde.

Dieses Problem wurde in Version 10.0.13 und später behoben. Weitere Informationen finden Sie in [KB 4582468](https://fix.lcs.dynamics.com/Issue/Details?kb=4582468&bugId=468844&dbType=3&qc=fcd64080446a27382cfde3e4c3bdcfb714279185932259cd11ceb0d500617296).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]