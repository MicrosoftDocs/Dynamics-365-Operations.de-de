---
title: Verarbeitung von eingehenden elektronischen Belegen
description: Dieser Artikel bietet einen Überblick über die Verarbeitung von eingehenden elektronischen Belegen.
author: dkalyuzh
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: dec4c16c8ba9f0ba55f30f3944eff172cf9db724
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910007"
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
