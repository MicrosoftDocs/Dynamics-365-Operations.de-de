---
title: Lebensereignisse verarbeiten
description: Während des Mitarbeiterlebenszyklus in Microsoft Dynamics 365 Human Resources kann es bei jedem Mitarbeiter zu verschiedenen Änderungen von Lebensereignissen kommen.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitLifeEventTypes, BenefitEligibilityProcessResultViewer
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: beac0d6666055a278cab0be9080e49c51885671d
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6057813"
---
# <a name="process-life-events"></a>Lebensereignisse verarbeiten

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Während des Mitarbeiterlebenszyklus in Microsoft Dynamics 365 Human Resources kann es bei jedem Mitarbeiter zu verschiedenen Änderungen von Lebensereignissen kommen. Beispiel: Ehe, Wechsel der Beschäftigung oder Wechsel von Unterhaltsberechtigten/Begünstigten. Um Lebensereignisse zu verwenden, müssen Sie Lebensereignisse im Formular „Vorteilparameter“ aktivieren, Lebensereignistypen einrichten und Lebensereignisoptionen für Plantypen einrichten.

Bevor Sie Lebensereignisse verarbeiten können, müssen Sie mindestens einmal während einer Einstellungsperiode eine offene Registrierung durchgeführt haben. In den USA erfolgt die offene Registrierung in der Regel einmal pro Jahr. Außerhalb der USA kann eine offene Registrierung zum Zeitpunkt der Einstellung durchgeführt werden. Eine Arbeitskraft muss keinen Vorteilsplan auswählen, damit Lebensereignisse verarbeitet werden können, sie muss jedoch in die offene Registrierungsverarbeitung einbezogen worden sein. 

Verwenden Sie die Lebensereignisverarbeitung, wenn Sie Arbeitskräfte haben, deren Lebensereignisse zu einem späteren Zeitpunkt stattfinden. Dieses Ereignis verarbeitet alle nicht verarbeiteten Lebensereignisse (wie zukünftige Lebensereignisse oder hinzugefügte Lebensereignisse, die sich nicht auf eine bestimmte Arbeitskraft beziehen – ein Beispiel wäre ein neuer Vorteil). Echtzeitereignisse sind ausgeblendet.

Wenn beispielsweise heute der 1. Februar ist und die Arbeitskraft Joe Smith am 14. Februar juristische Personen wechseln soll, verarbeitet das System alle Ereignisse bis zum 15. Februar, wenn Sie die Verarbeitung von Lebensereignissen für den 15. Februar ausführen. 

1. Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Bearbeitung** die Option **Verarbeitung von Lebensereignissen**.

2. Geben Sie im Dialogfeld **Verarbeitung von Lebensereignissen ausführen** Werte für die folgenden Felder ein:

   | Feld | Beschreibung |
   | --- | --- |
   | **Registrierungsperiode** | Die Registrierungsperiode, für die die Lebensereignisse verarbeitet werden. |
   | **Juristische Person** | Die juristische Person, für die die Lebensereignisse verarbeitet werden. |
   | **Datum des Lebensereignisses** | Das System verarbeitet alle Ereignisse während der Registrierungsperiode, die bis zu diesem Datum auftreten. |
   | **Arbeitskraft** | Die Arbeitskraft, für die die Lebensereignisse verarbeitet werden. Wenn Sie dieses Feld leer lassen, werden Lebensereignisse für alle Arbeitskräfte verarbeitet. |

3. Wenn Sie den Prozess im Hintergrund ausführen möchten, wählen Sie **Im Hintergrund ausführen** und führen Sie die folgenden Aufgaben aus:

   1. Geben Sie Informationen für den Prozess ein.

   2. Um eine wiederkehrende Stelle einzurichten, wählen Sie **Wiederholung**, geben Sie die Wiederholungsinformationen ein und wählen Sie **OK**.

   3. Um eine Stellenbenachrichtigung einzurichten, wählen Sie **Benachrichtigungen**, wählen Sie die zu empfangenden Benachrichtigungen und wählen Sie dann **OK**.

   4. Wählen Sie **OK**. Der Prozess wird mit den von Ihnen festgelegten Parametern ausgeführt.

4. Wählen Sie **OK**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]