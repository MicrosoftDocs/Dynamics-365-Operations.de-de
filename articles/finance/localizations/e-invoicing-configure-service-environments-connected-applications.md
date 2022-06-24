---
title: Konfigurieren Sie die Umgebungen der Dienste und der verbundenen Anwendungen
description: In diesem Artikel erfahren Sie, wie Sie Ihre Umgebung und die damit verbundenen Anwendungen konfigurieren.
author: dkalyuzh
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: c1bb3f784148f04c01223ac4e280a18bacfe0e51
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853221"
---
# <a name="configure-service-environments-and-connected-applications"></a>Konfigurieren Sie die Umgebungen der Dienste und der verbundenen Anwendungen

[!include [banner](../includes/banner.md)]

In diesem Artikel erfahren Sie, wie Sie Ihre Umgebung und die damit verbundenen Anwendungen konfigurieren. Dieser Prozess besteht aus drei Schritten. Schritt 1 ist obligatorisch, die Schritte 2 und 3 sind optional.

## <a name="step-1-create-a-service-environment"></a>Schritt 1: Erstellen Sie eine Service-Umgebung

Wenn Sie Ihre Umgebung erstellen, definieren Sie die Liste der Benutzer, die Globalisierungsfunktionen bereitstellen können. Optional können Sie für einige der Szenarien die Liste der externen Anwendungen definieren, die mit dem Dienst für die elektronische Rechnungsstellung kommunizieren können. Legen Sie Nummernkreise fest, wenn Sie diese in Ihren Szenarien verwenden werden.

Um diesen Schritt abzuschließen, siehe [Dienstumgebungen](e-invoicing-service-environments.md).

## <a name="step-2-add-certificates-and-secrets"></a>Schritt 2: Hinzufügen von Zertifikaten und Geheimnissen

Fügen Sie einen Verweis auf den Key Vault Microsoft Azure und die Geheimnisse hinzu, um sie in Ihren Szenarien zu verwenden. Dieser Schritt ist obligatorisch, wenn Aktionen in den Verarbeitungs-Pipelines Zertifikate und Geheimnisse für die digitale Unterzeichnung oder die Kommunikation mit externen Webdiensten verwenden.

Um diesen Schritt abzuschließen, siehe [Kundenzertifikate und Geheimnisse](e-invoicing-customer-certificates-secrets.md).

## <a name="step-3-configure-connected-applications"></a>Schritt 3: Konfigurieren Sie die verbundenen Anwendungen.

Um die Kommunikation zwischen den Anwendungen Dynamics 365 Finance oder Dynamics 365 Supply Chain Management und der Elektronischen Rechnungsstellung einzurichten, müssen Sie Finance oder Supply Chain Management so konfigurieren, dass sie den Aufruf des Dienstes für die elektronische Rechnungsstellung aufbauen und die Geschäftsdaten in einer einheitlichen Struktur vorbereiten, die in das gewünschte elektronische Format umgewandelt werden kann. Die Anwendungen müssen auch die Antworten des Dienstes korrekt verarbeiten. Sie können diese Konfiguration direkt in Ihrer Finance oder Supply Chain Management Umgebung vornehmen, oder Sie können sie im Regulatory Configuration Service (RCS) vornehmen. Wenn Sie die Konfiguration in RCS abgeschlossen haben, können Sie es anschließend in Ihrer Umgebung für Finance oder Supply Chain Management bereitstellen. In diesem Schritt registrieren Sie die verbundene Anwendung für die Bereitstellung von Parametern.

Um diesen Schritt auszuführen, siehe [Verbundene Anwendungen](e-invoicing-connected-applications.md).
