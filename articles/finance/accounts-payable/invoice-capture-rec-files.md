---
title: Empfangene Dateien zu Invoice Capture
description: In diesem Artikel wird erläutert, wie Sie Rechnungsdateien aus verschiedenen Quellen in Invoice Capture sammeln.
author: sunfzam
ms.date: 10/13/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3c55540d11a67d4d4c4c8477d51cb6f1f5777767
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690134"
---
# <a name="invoice-capture-received-files"></a>Empfangene Dateien zu Invoice Capture

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

In Invoice Capture ist die **Empfangene Dateien** ein zentraler Ort, an dem Rechnungsdateien aus verschiedenen Quellen empfangen werden.

## <a name="upload-invoice-files"></a>Rechnungsdateien hochladen

Sachbearbeiter in der Kreditorenbuchhaltung können Rechnungsbilder hochladen, indem sie **Eine Datei hochladen** auswählen, um das Dialogfeld **Hochladen** zu öffnen. Nachdem ein Kreditorenbuchhalter eine Datei ausgewählt hat, wird die Schaltfläche **Hochladen** verfügbar.

## <a name="include-or-obsolete-invoice-files"></a>Rechnungsdateien einbeziehen oder veraltet sein

Benutzer können Rechnungen mit Fehlern oder Warnungen auswählen und die Rechnungen dann entweder einbeziehen oder veralten, indem sie die entsprechende Schaltfläche im Aktivitätsbereich auswählen. Eine als veraltet markierte Rechnung erscheint nicht in der Ansicht **Empfangene Dateien (veraltet)**.

## <a name="view-captured-invoices"></a>Erfasste Rechnungen anzeigen

Nachdem eine empfangene Datei erfolgreich erkannt wurde, werden die Informationen der erfassten Rechnung vom KI-Modell zurückgegeben und in Microsoft Dataverse eingegeben. Der Kreditorenbuchhalter kann dann die Rechnungsdetails durch Auswählen von **Erfasste Rechnung anzeigen** überprüfen. Benutzer können die Originalrechnungsdatei nach Bedarf herunterladen.
