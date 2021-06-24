---
title: Erstellen von Konsolidierungskontengruppen und zusätzlicher Konsolidierungskonten
description: Dieses Thema enthält Informationen zu Konsolidierungskontogruppen und zusätzliche Konsolidierungskontos und erläutert, wie sie in Microsoft Dynamics 365 Finance verwendet werden.
author: aprilolson
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerConsolidateAccountGroup
audience: Application User
ms.reviewer: roschlom
ms.custom: 265544
ms.assetid: 71c31df7-b655-46a8-8844-4f92a8bd71b0
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 245b61c8cb85ab1282a921ac99b9ac7c2efbadc5
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "6189420"
---
# <a name="consolidation-account-groups-and-additional-consolidation-accounts"></a>Erstellen von Konsolidierungskontengruppen und zusätzlicher Konsolidierungskonten

[!include [banner](../includes/banner.md)]

Dieses Thema enthält Informationen zu Konsolidierungskontogruppen und zusätzliche Konsolidierungskontos und erläutert, wie sie in Microsoft Dynamics 365 Finance verwendet werden.

## <a name="consolidation-account-groups"></a>Konsolidierungskontengruppen

Mit Konsolidierungskontogruppen können Sie Gruppen von Konten erstellen, die Sie verwenden möchten, um Daten konsolidieren zu können. Meistens stellt eine Konsolidierungskontogruppe einen von Behörden vorgegebenen Kontenplan dar oder führt Konten in einer Gruppe zusammen, die vom Hauptsitz des Unternehmens definiert wird. Sie finden die Konsolidierungskontogruppen im Bereich **Einstellungen** im Modul **Konsolidierungen**. Wenn Sie eine neue Gruppe hinzufügen, geben Sie eine eindeutige Kennung für die Kontengruppe und einen Namen ein.

## <a name="additional-consolidation-accounts"></a>Zusätzliche Konsolidierungskonten
Zusätzliche Konsolidierungskonten können einem Konto aus einem vorhandenen Kontenplan einer Konsolidierungskontogruppe zugewiesen werden. Sie können einen Konsolidierungskontowert und dann einen Namen angeben. 

Sie finden die zusätzlichen Konsolidierungskontogruppen im Bereich **Einstellungen** im Modul **Konsolidierungen**. Wenn Sie ein neues Konsolidierungskonto erstellen, müssen Sie die folgenden Informationen angeben:

-   **Hauptkonto** – Dieses Feld ist ein Suchfeld, das alle Hauptkonten anzeigt, die auf dem Kontenplan basieren, den Sie auf der Seite ausgewählt haben. Wenn Sie ein Konto auswählen, wird der Name automatisch im Feld **Name des Hauptkontos** eingegeben.
-   **Konsolidierungskontogruppe** – Verwenden Sie dieses Feld, um die Gruppe anzugeben, der das Konto zugewiesen werden soll. Wenn Sie auf zwei unterschiedliche Arten konsolidieren, müssen Sie dasselbe Konto allen vier Konsolidierungskontogruppen hinzufügen.
-   **Konsolidierungskonto** – Geben Sie den Wert des Konsolidierungskontos ein. Dieser Wert muss kein Konto in einem Kontenplan. sein Es kann jeder Wert sein, den Sie benötigen.
-   **Konsolidierungskontoname**– Geben Sie den Namen des Kontos an, das auf Anfragen und Berichten angezeigt werden soll.
-   **Sat-Ebene**– Dieses Feld wird verwendet, um Kontoauszüge der mexikanischen Steuerbehörde zu melden. 

Wenn Sie mit dem Erstellen der Konsolidierungskontogruppen und der zusätzlichen Konsolidierungskonten fertig sind, können Sie die Gruppe im Oline-Konsolidierungsprozess auswählen.


Weitere Informationen finden Sie unter [Konsolidierungsgruppen und zusätzliche Konsolidierungskonten erstellen](../general-ledger/tasks/create-consolidation-groups.md) 





[!INCLUDE[footer-include](../../includes/footer-banner.md)]