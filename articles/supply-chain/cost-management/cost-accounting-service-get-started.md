---
title: Erste Schritte mit dem Kostenrechnungsdienst (private Vorschau)
description: Dieses Thema enthält Lizenzdetails und Installationsanweisungen für den Kostenrechnungsdienst.
author: AndersGirke
manager: tfehr
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 1f602116edabc424b6cbee541e268df017912d3c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5011846"
---
# <a name="get-started-with-the-cost-accounting-service-private-preview"></a>Erste Schritte mit dem Kostenrechnungsdienst (private Vorschau)

[!INCLUDE [banner](../includes/banner.md)]

> [!IMPORTANT]
> Die in diesem Abschnitt genannten Funktionen stehen im Rahmen einer privaten Vorschauversion zur Verfügung. Der Inhalt dieses Themas und die darin beschriebenen Funktionen können sich ändern. Weitere Informationen zu Vorschauversionen finden Sie in den [FAQ zu Dienstupdates für eine Version](../../fin-ops-core/fin-ops/get-started/one-version.md).

Mit dem Kostenrechnungsservice können Sie mehrere Bestandsbuchungen in den von Ihnen eingerichteten Kostenrechnungsbüchern durchführen. Sie verknüpfen jedes Kostenrechnungsbuch mit einer *Konvention*. Eine Konvention ist eine Sammlung der folgenden Arten von Rechnungslegungsgrundsätzen:

- Kostenobjekt
- Messungsgrundlage für Eingabe
- Kostenflussannahme
- Kostenelement

> [!NOTE]
> Auch nach dem Aktivieren des Kostenrechnungsdienstes können Sie die Bestandsabrechnung in Microsoft Dynamics 365 Supply Chain Management wie gewöhnlich durchführen.

Der Kostenrechnungsdienst ist ein Add-In. Um seine Funktionen verfügbar zu machen, müssen Sie es über Microsoft Dynamics Lifecycle Services (LCS) installieren. Daher können Sie es in einer Testumgebung auswerten, bevor Sie es für Produktionsumgebungen aktivieren.

Der Kostenrechnungsdienst unterstützt derzeit nicht alle integrierten Kostenmanagementfunktionen von Dynamics 365 Supply Chain Management. Daher ist es wichtig, dass Sie prüfen, ob der derzeit verfügbare Funktionsumfang Ihren Anforderungen entspricht.

## <a name="how-to-get-the-cost-accounting-service-private-preview"></a><a name="sign-up"></a>Abrufen des Kostenrechnungsdiensts (private Vorschau)

> [!IMPORTANT]
> Um den Kostenrechnungsdienst nutzen zu können, müssen Sie über eine LCS-fähige Hochverfügbarkeitsumgebung (keine OneBox-Umgebung) verfügen und Dynamics 365 Supply Chain Management in der Version 10.0.11 oder höher muss ausgeführt werden.

Um sich für die private Vorschau des Kostenrechnungsdiensts anzumelden, senden Sie bitte Ihre LCS-Umgebungs-ID per E-Mail an [Kostenrechnungsdienst (private Vorschau)](mailto:aevengir@microsoft.com?subject=Cost%20accounting%20service%20%28private%20preview%29). Nach der Genehmigung für das Programm senden wir Ihnen eine Folge-E-Mail mit einem Beta-Schlüssel für den Kostenrechnungsservice. Nach Erhalt des Beta-Schlüssels können Sie fortfahren, indem Sie das [Add-In installieren](#install).

## <a name="licensing"></a>Lizenzierung

Der Kostenrechnungsdienst wird zusammen mit den Standardfunktionen der Bestandsbuchhaltung lizenziert, die für das Supply Chain Management verfügbar sind. Sie müssen keine zusätzliche Lizenz erwerben, um den Kostenrechnungsdienst nutzen zu können.

## <a name="install-the-add-in"></a><a name="install"></a>Installieren des Add-Ins

Um den Kostenrechnungsdienst zu verwenden, installieren Sie das Kostenrechnungsdienst-Add-In für Supply Chain Management wie im folgenden Verfahren beschrieben.

1. [Anmelden](#sign-up) für den Kostenrechnungsdiensts (private Vorschau).

1. Melden Sie sich bei LCS an.

1. Navigieren Sie zu **Verwaltung von Vorschaufunktionen**.

1. Wählen Sie das Pluszeichen (**+**).

1. Im Feld **Code** geben Sie Ihren Add-In-Beta-Schlüssel für den Kostenrechnungsdienst ein. (Sie sollten Ihren Schlüssel per E-Mail erhalten haben.)

1. Wählen Sie **Entsperren** aus.

1. Öffnen Sie die LCS-Umgebung, in der Sie den Dienst hinzufügen möchten.

1. Gehen Sie zu **Vollständige Details**.

1. Scrollen Sie zum Inforegister **Umgebungs-Add-Ins**.

1. Wählen Sie **Installieren Sie ein neues Add-In**.

1. Wählen Sie **Kostenrechnungsdienst**.

1. Befolgen Sie die Installationsanleitung und erklären Sie sich mit den Allgemeinen Geschäftsbedingungen einverstanden.

1. Wählen Sie **Installieren**.

1. Auf dem Inforegister **Umgebungs-Add-Ins** sollten Sie sehen, dass der Kostenrechnungsdienst installiert wird. Nach einigen Minuten sollte sich der Status von **Installieren** in **Installiert** ändern. (Möglicherweise müssen Sie die Seite aktualisieren, um diese Änderung zu sehen.) Zu diesem Zeitpunkt ist der Kostenrechnungsdienst einsatzbereit.

## <a name="set-up-the-integration"></a>Einrichten der Integration

Einrichten der Integration zwischen dem Kostenrechnungsdienst und Dynamics 365 Supply Chain Management:

1. Gehen Sie zu **Systemverwaltung > Funktionsverwaltung**.

1. Wählen Sie **Nach Updates suchen**.

1. Öffnen Sie die Registerkarte **Alle** und suchen Sie nach der genannten Funktion *Kostenrechnungsdienst*.

1. Wählen Sie **Jetzt aktivieren**.

1. Gehen Sie zu **Kostenverwaltung > Kostenrechnungsdienst > Setup > Kostenrechnungsdienstparameter > Integrationsparameter**.

1. Im Feld **Anwendungs-ID** geben Sie den folgenden Code ein:<br> 08231eb2-a501-4edb-b3c5-aede5e5e0c3f

1. Im Feld **Datendienst-Endpunkt** geben Sie die folgende URL ein:<br>https://operationsdataservice.operations365.dynamics.com/

1. Im Feld **Kostenrechnungsdienst-Endpunkt** geben Sie die folgende URL ein:<br>https://costaccountingservice.operations365.dynamics.com/

1. Der Kostenrechnungsdienst ist jetzt einsatzbereit.

## <a name="related-resources"></a>Zugehörige Ressourcen

[Startseite für den Kostenrechnungsdienst](cost-accounting-service-home.md)
