---
title: Verarbeitung von eingehenden elektronischen Belegen
description: Dieser Artikel bietet einen Überblick über die Verarbeitung von eingehenden elektronischen Belegen.
author: gionoder
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 554bc8fde3b2135eb878d885541c76ecd6d66493
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277300"
---
# <a name="processing-of-incoming-electronic-documents"></a>Verarbeitung von eingehenden elektronischen Belegen

[!include [banner](../includes/banner.md)]

Eingehende elektronische Belege, wie z.B. elektronische Rechnungen von Lieferanten, können auf zwei Arten importiert und verarbeitet werden:

- Dateien werden von externen Kanälen abgerufen und direkt an Ihre verbundene Anwendung weitergeleitet. Dort werden sie einer zusätzlichen Transformation unterzogen und dann in die Datenbank importiert.
- Die Dateien werden im Dienst für die elektronische Rechnungsstellung vorverarbeitet und dann an Ihre angeschlossene Anwendung weitergeleitet.

Die Elektronische Rechnungsstellung unterstützt zwei Kanäle für eingehende Belege: E-Mail und Microsoft SharePoint-Ordner.

Es gibt zwei Einrichtungsarten, mit denen Sie festlegen können, ob Dokumente einer Vorverarbeitung unterzogen oder direkt an Ihre verbundene Anwendung weitergeleitet werden:

- **Datenkanal** - Das System wird das Dokument direkt an die angeschlossene Anwendung weiterleiten.
- **Datenkanal mit Verarbeitungspipeline** - Sie können zusätzliche Aktionen festlegen, die ausgeführt werden, bevor das Dokument an die verbundene Anwendung übergeben wird.

Informationen darüber, wie Sie die Szenarien für die Verarbeitung eingehender elektronischer Belege für die verschiedenen Kanäle festlegen, finden Sie unter [Konfigurieren eines E-Mail-Kanals](e-invoicing-configure-email.md) und [Konfigurieren eines SharePoint-Kanals](e-invoicing-configure-sharepoint-channel.md).
