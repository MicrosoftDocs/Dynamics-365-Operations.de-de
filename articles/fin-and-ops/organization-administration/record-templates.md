---
title: Datensatzvorlagen
description: Dieser Artikel führt das Konzept der Datensatzvorlagen ein und erklärt, wie Sie verwendet werden können, um Datensätze zu erstellen, die Informationen freigeben.
author: pvillads
manager: AnnBe
ms.date: 08/18/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 16101
ms.assetid: 61ada2d8-84c3-44bc-b4c5-516b1aeac3d1
ms.search.region: Global
ms.author: pvillads
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 426fd8fafec061b649cbb31109ffe8fabc24917d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "323570"
---
# <a name="record-templates"></a>Datensatzvorlagen

[!include [banner](../includes/banner.md)]

Dieser Artikel führt das Konzept der Datensatzvorlagen ein und erklärt, wie Sie verwendet werden können, um Datensätze zu erstellen, die Informationen freigeben.

Mithilfe von Datensatzvorlagen können Sie Datensätze schneller in Microsoft Dynamics 365 for Finance and Operationserstellt werden. Datensatzvorlagen können nicht für alle Datensatztypen in Microsoft Dynamics 365 for Finance and Operations erstellt werden.

Beispiel: Stellen Sie sich vor, Sie geben Mietinformationen für eine Autovermietung mit Sitz in San Francisco ein. Da die meisten Kunden vermutlich aus dem Bereich San Francisco kommen, wäre es schön, wenn die Werte für **Bundesland**, **Land** und **Ort** auf dem Mietvertragsformular automatisch gefüllt würden.

> [!NOTE]
> Sie können Vorlagen nur auf Finance and Operations-Bereiche anwenden, auf die Sie Zugriff haben. Wenn Sie einen neuen Datensatz erstellen, können Sie und andere Benutzer jedoch alle Vorlagentitel sehen, wenn Sie Vorlagen erstellen, die für alle Benutzer verfügbar sind. Berücksichtigen Sie dies beim Benennen von Vorlagen. Vermeiden Sie z. B. Namen, in denen Begriffe wie "Provision" vorkommen, wenn die Information, dass einige Mitarbeiter des Unternehmens auf Provisionen beruhende Gehälter haben, vertraulich ist.

Wenn es für ein bestimmtes Formular eine oder mehrere Vorlagen gibt, auf die Sie zugreifen können, und Sie versuchen, einen neuen Datensatz im Formular zu erstellen, wird die Seite **Vorlage für … wählen** angezeigt. Durch Auswählen einer Vorlage aus der Liste wird der neue Datensatz mit den in der ausgewählten Vorlage festgelegten Standardinformationen versehen. Wenn Sie beim Erstellen neuer Datensätze keine Vorlagen verwenden möchten, aktivieren Sie das Kontrollkästchen **Nicht erneut fragen** im Formular **Vorlage für …** wählen. Soll das Auswahldialogfeld für Vorlagen wieder angezeigt werden, klicken Sie mit der rechten Maustaste auf **Datensatzinfo**, und klicken Sie anschließend auf **Vorlagenabschnitt anzeigen**.
