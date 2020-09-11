---
title: Unterstützte Szenarien für die Dual-Write-Einrichtung
description: In diesem Thema werden die Szenarien beschrieben, die für die Dual-Write-Einrichtung unterstützt werden.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 08/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 275d24d8f32fd1d2d15356d14c5c6591e8503c65
ms.sourcegitcommit: ec4df354602c20f48f8581bfe5be0c04c66d2927
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "3706251"
---
# <a name="supported-scenarios-for-dual-write-setup"></a>Unterstützte Szenarien für die Dual-Write-Einrichtung

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

Sie können eine Dual-Write-Verbindung zwischen einer Finance and Operations-Umgebung und einer Common Data Service-Umgebung einrichten.

+ Eine **Finance and Operations-Umgebung** bietet die zugrunde liegende Plattform für **Finance and Operations-Apps** (z.B. Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management und Dynamics 365 Retail).
+ Eine **Common Data Service-Umgebung** bietet die zugrunde liegende Plattform für **modellgesteuerte Anwendungen in Dynamics 365** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing und Dynamics 365 Project Service Automation).

>[!IMPORTANT]
>Human Resources in Finance and Operations unterstützt Verbindungen für duales Schreiben, aber die Dynamics 365 Human Resources-App nicht.

Der Einrichtungsmechanismus variiert je nach Ihrem Abonnement und der Umgebung.

+ Bei neuen Instanzen von Finance and Operations Anwendungen beginnt die Einrichtung einer Dual-Write-Verbindung in Microsoft Dynamics Lifecycle Services (LCS). Wenn Sie eine Lizenz für Microsoft Power Platform haben, erhalten Sie eine neue Common Data Service-Umgebung, wenn Ihr Mandant keine hat.
+ Für bestehende Instanzen von Finance and Operations-Anwendungen beginnt die Einrichtung einer Dual-Write-Verbindung in der Finance and Operations-Umgebung.

Die folgenden Einrichtungsszenarien werden unterstützt:

+ [Eine neue Finance and Operations-Anwendungsinstanz und eine neue modellgesteuerte Anwendungsinstanz](#new-new)
+ [Eine neue Finance and Operations App-Instanz und eine bestehende modellgetriebene App-Instanz](#new-existing)
+ [Eine neue Finance and Operations-Anwendungsinstanz, die über Demodaten und eine neue modellgesteuerte Anwendungsinstanz verfügt](#new-demo-new)
+ [Eine neue Finance and Operations App-Instanz, die über Demodaten verfügt, und eine bestehende modellgetriebene App-Instanz](#new-demo-existing)
+ [Eine bestehende Finance and Operations App-Instanz und eine neue oder bestehende modellgetriebene App-Instanz](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-model-driven-app-instance"></a><a id="new-new"></a>Eine neue Finance and Operations App-Instanz und eine neue modellgetriebene App-Instanz

Um eine Dual-Write-Verbindung zwischen einer neuen Instanz einer Finance and Operations-Anwendung, die keine Daten hat, und einer neuen Instanz einer modellgesteuerten Anwendung in Dynamics 365 einzurichten, folgen Sie den Schritten in [Dual-Write-Setup von Lifecycle Services](lcs-setup.md). Wenn der Verbindungsaufbau abgeschlossen ist, werden die folgenden Aktionen automatisch ausgeführt:

- Eine neue, leere Finance and Operations-Umgebung wird bereitgestellt.
- Es wird eine neue, leere Instanz einer modellgesteuerten Anwendung bereitgestellt, in der die CRM-Prime-Lösung installiert wird.
- Eine Dual-Write-Verbindung wird für DAT-Firmendaten hergestellt.
- Entitätszuordnungen werden für die Live-Synchronisierung aktiviert.

Beide Umgebungen sind dann für die Live-Datensynchronisierung bereit.

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-model-driven-app-instance"></a><a id="new-existing"></a>Eine neue Finance and Operations-Anwendungsinstanz und eine vorhandene modellgesteuerte Anwendungsinstanz

Um eine Dual-Write-Verbindung zwischen einer neuen Instanz einer Finance and Operations-Anwendung, die keine Daten hat, und einer bestehenden Instanz einer modellgesteuerten Anwendung in Dynamics 365 einzurichten, folgen Sie den Schritten in [Dual-Write-Setup von Lifecycle Services](lcs-setup.md). Wenn der Verbindungsaufbau abgeschlossen ist, werden die folgenden Aktionen automatisch ausgeführt:

- Eine neue, leere Finance and Operations-Umgebung wird bereitgestellt.
- Eine Dual-Write-Verbindung wird für DAT-Firmendaten hergestellt.
- Entitätszuordnungen werden für die Live-Synchronisierung aktiviert.

Beide Umgebungen sind dann für die Live-Datensynchronisierung bereit.

Um die vorhandenen Common Data Service-Daten mit der Finance and Operations-Anwendung zu synchronisieren, folgen Sie diesen Schritten.

1. Erstellen Sie ein neues Unternehmen in der Finance and Operations-Anwendung.
2. Fügen Sie das Unternehmen zum Dual-Write-Verbindungsaufbau hinzu.
3. [Bootstrap](bootstrap-company-data.md) die Common Data Service-Daten unter Verwendung eines aus drei Buchstaben bestehenden Buchungscodees der International Organization for Standardization (ISO).

Da sich Dual-Write im Live-Synchronisationsmodus befindet, beginnen die Daten von Common Data Service automatisch in die Finance and Operations-Anwendung zu fließen.

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-a-new-model-driven-app-instance"></a><a id="new-demo-new"></a>Eine neue Finance and Operations-Anwendungsinstanz, die über Demodaten und eine neue modellgesteuerte Anwendungsinstanz verfügt.

Um eine Dual-Write-Verbindung zwischen einer neuen Instanz einer Finance and Operations-Anwendung, die über Demodaten verfügt, und einer neuen Instanz einer modellgesteuerten Anwendung in Dynamics 365 einzurichten, folgen Sie den Schritten im Abschnitt [Eine neue Finance and Operations-Anwendungsinstanz und eine neue modellgesteuerte Anwendungsinstanz](#new-new) weiter oben in diesem Thema. Wenn der Verbindungsaufbau abgeschlossen ist und Sie die Demodaten mit der modellgesteuerten Anwendung synchronisieren möchten, folgen Sie diesen Schritten.

1. Öffnen Sie die Anwendung Finance and Operations von der LCS-Seite, melden Sie sich an und gehen Sie dann zu **Datenverwaltung \> Dual-write**.
2. Führen Sie die Funktionalität **Initiale Synchronisation** für die Entitäten aus, für die Sie Daten synchronisieren möchten.

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-an-existing-model-driven-app-instance"></a><a id="new-demo-existing"></a>Eine neue Finance and Operations-Anwendungsinstanz, die über Demodaten und eine bestehende modellgesteuerte Anwendungsinstanz verfügt.

Um eine Dual-Write-Verbindung zwischen einer neuen Instanz einer Finance and Operations-Anwendung, die über Demodaten verfügt, und einer bestehenden Instanz einer modellgesteuerten Anwendung in Dynamics 365 herzustellen, folgen Sie den Schritten im Abschnitt [Eine neue Finance and Operations-Anwendungsinstanz und eine bestehende modellgesteuerte Anwendungsinstanz](#new-existing) weiter oben in diesem Thema. Wenn der Verbindungsaufbau abgeschlossen ist und Sie die Demodaten mit der modellgesteuerten Anwendung synchronisieren möchten, folgen Sie diesen Schritten.

1. Öffnen Sie die Anwendung Finance and Operations von der LCS-Seite, melden Sie sich an und gehen Sie dann zu **Datenverwaltung \> Dual-write**.
2. Führen Sie die Funktionalität **Initiale Synchronisation** für die Entitäten aus, für die Sie Daten synchronisieren möchten.

Um die vorhandenen Common Data Service-Daten mit der Finance and Operations-Anwendung zu synchronisieren, folgen Sie diesen Schritten.

1. Erstellen Sie ein neues Unternehmen in der Finance and Operations-Anwendung.
2. Fügen Sie das Unternehmen zum Dual-Write-Verbindungsaufbau hinzu.
3. [Bootstrap](bootstrap-company-data.md) der Common Data Service-Daten unter Verwendung eines dreibuchstabigen ISO-Buchungscodees.

Da sich Dual-Write im Live-Synchronisationsmodus befindet, beginnen die Daten von Common Data Service automatisch in die Finance and Operations-Anwendung zu fließen.

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-or-existing-model-driven-app-instance"></a><a id="existing-existing"></a>Eine bestehende Finance and Operations-Anwendungsinstanz und eine neue oder bestehende modellgetriebene Anwendungsinstanz

Die Einrichtung einer Dual-Write-Verbindung zwischen einer bestehenden Instanz einer Finance and Operations-Anwendung und einer neuen oder bestehenden Instanz einer modellgesteuerten Anwendung in Dynamics 365 erfolgt in der Finance and Operation-Umgebung.

1. Richten Sie die Verbindung von der Finance and Operations-Anwendung aus ein.
2. Um die vorhandenen Common Data Service-Daten mit der Finance and Operations-Anwendung zu synchronisieren, [Bootstrap](bootstrap-company-data.md) die Common Data Service-Daten unter Verwendung eines dreibuchstabigen ISO-Buchungskreises.

Da sich Dual-Write im Live-Synchronisationsmodus befindet, beginnen die Daten von Common Data Service automatisch in die Finance and Operations-Anwendung zu fließen.
