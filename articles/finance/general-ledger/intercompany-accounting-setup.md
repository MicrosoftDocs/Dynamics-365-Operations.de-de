---
title: Einrichten der Intercompany-Verrechnung
description: In diesem Thema wird erläutert, wie die Intercompany-Verrechnung eingerichtet wird, sodass Sie Intercompany-Erfassungen für Sachkonto-Zuweisungen Finanzerfassung, z. B. Tageserfassungen, Kreditorenrechnungserfassungen und Zahlungserfassungen, verwenden können.
author: kweekley
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerInterCompany
audience: Application User
ms.reviewer: roschlom
ms.custom: 15761
ms.assetid: 1362297b-7a51-4930-b822-2b204a2e3c37
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ed05b0814826442f22d4c3508c28b3c48080e8ee
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988851"
---
# <a name="intercompany-accounting-setup"></a>Einrichten der Intercompany-Verrechnung

[!include [banner](../includes/banner.md)]

In diesem Thema wird erläutert, wie die Intercompany-Verrechnung eingerichtet wird, sodass Sie Intercompany-Erfassungen für Sachkonto-Zuweisungen Finanzerfassung, z. B. Tageserfassungen, Kreditorenrechnungserfassungen und Zahlungserfassungen, verwenden können.

Intercompany-Erfassungen können in unterschiedlichen Szenarien erstellt werden, z. B. für Tageserfassungen, Sachkontozuteilungen und zentralisierte Zahlungen. Um diese Szenarien zu ermöglichen, müssen Sie die Verrechnung einrichten.

## <a name="define-main-accounts"></a>Hauptkonten definieren
Zunächst müssen Sie die Intercompany-Hauptkonten anlegen, die für die Buchhaltungseinträge "Fällig an" und "Fällig von" verwendet werden. Es wird empfohlen, eindeutige Hauptkonten für jedes Unternehmen zu verwenden, um die Abstimmung und die Löschung von Intercompany-Verrechnungseinträgen zu vereinfachen. Wenn Sie einen Handelspartner oder eine entsprechende Dimension verwenden, um die Intercompany-Partei zu identifizieren, können Sie diese Dimension als feste Dimension im Hauptkonto definieren, das in der Verrechnung festgelegt ist. Wenn Sie die Hauptkonten einrichten, sollten Sie das **Hauptkontotyp** Feld auf **Bilanz** auf der **Hauptkonten** Seite festlegen.

## <a name="define-journal-names"></a>Standardjournale definieren
Anschließend müssen Sie einen Erfassungsnamen definieren. Legen Sie das **Erfassungstyp** Feld auf **täglich** auf der **Erfasssungsnamen** Seite fest. Es wird empfohlen, einen spezifischen Erfassungsnamen für die Verrechnung zu verwenden.

## <a name="define-intercompany-accounting-setup"></a>Einrichten der Intercompany-Verrechnung
Die Seite **Intercompany-Verrechnung** wird verwendet, um die Paare von juristischen Personen erstellen, mit die einander abwickeln können. Die wird Verrechnungseinstellungen freigegeben, um die Einstellungen aus allen juristischen Personen angezeigt. Wenn Sie ein neues Paar der juristische Person erstellen, stellen Sie sicher, dass Sie berücksichtigen, welche juristische Person als das ursprüngliche Unternehmen für das Zielunternehmen definiert wird. Wenn Sie Intercompany-Verrechnung eingibt, bestimmt die Buchung, der juristischen Person ist, initiierend Zeilencode oder die Buchung. Beispielsweise wird die Intercompany-Verrechnung für USMF (Ursprungslagerort) und USSI (Ziel) eingerichtet. Wenn ein Benutzer in USSI aktiv ist und eine Intercompany-Buchung mit den USMF eingibt, wird die Buchung nicht, da die Intercompany-Verrechnung nur für USMF definiert, wird das der Ersteller gesendet. Wenn jedem Unternehmen eine Buchung auslösen kann, müssen Sie ein zweites Paar der juristischen Person für die gegenseitige Einstellungen erstellen. 

Wählen Sie **Sollkonto (fällig am)** und **Habenkonto (fällig am)** für den Ursprungslagerort und konsolidierte juristische Person enthält. Definieren Sie, welche **Erfassungsname** verwendet wird, wenn die Buchung im Zielunternehmen erstellt wird. Die Erfassung für das ursprüngliche Unternehmen bereits bekannt, da vom Benutzer festgelegt, sofern die Intercompany-Buchung erstellt hat. 

Schließlich wählen Sie, welche juristische Person die unterstützenden erklärenden Beträge erhält, z.B. Skonto oder realisierte Gewinne/Verluste für zentralisierte Zahlungen aus. 

Eine Beziehung gegenseitige kann für die **Intercompany-Verrechnung** Seite einfacher eingerichtet werden, indem die verwendet **Gegenseitige Beziehung Erstellen**-Schaltfläche, nachdem das erste Paar der juristischen Person erstellt wurde. Wenn das gegenseitige Paar erstellt wird, werden die Angaben für das Zielunternehmen zum ursprünglichen Unternehmen und umgekehrt kopiert. Die Erfassung, die für das Zielunternehmen definiert wird, bleibt. Die meisten Organisationen verwendet dieselbe Benennungskonvention für ihre Journale, damit das Journal das gleich ist. Wenn das Journal unterscheidet, wird eine Warnung in dem Feld, die Sie darüber informiert werden, dass die Erfassung nicht vorhanden ist und eine andere Erfassung ausgewählt werden kann.



