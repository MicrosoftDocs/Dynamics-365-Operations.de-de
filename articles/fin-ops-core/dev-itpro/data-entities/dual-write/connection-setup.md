---
title: Anleitung zum Einrichten des dualen Schreibens
description: In diesem Thema werden die Szenarien beschrieben, die für die Dual-Write-Einrichtung unterstützt werden.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 10/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 47c07dd0e2f311b61297340a48a5a31cb1de3903
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685664"
---
# <a name="guidance-for-dual-write-setup"></a>Anleitung zum Einrichten des dualen Schreibens

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Sie können eine Dual-Write-Verbindung zwischen einer Finance and Operations-Umgebung und einer Dataverse-Umgebung einrichten.

+ Eine **Finance and Operations-Umgebung** bietet die zugrunde liegende Plattform für **Finance and Operations-Anwendungen** (z.B. Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce und Dynamics 365 Human Resources).
+ Eine **Dataverse-Umgebung** bietet die zugrunde liegende Plattform für **Kundenbindungs-Apps** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing und Dynamics 365 Project Service Automation).

> [!IMPORTANT]
> Das Modul „Personalressourcen“ in Dynamics 365 Finance unterstützt Verbindungen für duales Schreiben, die Dynamics 365 Human Resources-App jedoch nicht.

Der Einrichtungsmechanismus variiert je nach Ihrem Abonnement und der Umgebung:

+ Bei neuen Instanzen von Finance and Operations Anwendungen beginnt die Einrichtung einer Dual-Write-Verbindung in Microsoft Dynamics Lifecycle Services (LCS). Wenn Sie eine Lizenz für Microsoft Power Platform haben, erhalten Sie eine neue Dataverse-Umgebung, wenn Ihr Mandant keine hat.
+ Für bestehende Instanzen von Finance and Operations-Anwendungen beginnt die Einrichtung einer Dual-Write-Verbindung in der Finance and Operations-Umgebung.

Bevor Sie mit dem dualen Schreiben für eine Entität beginnen, können Sie eine erste Synchronisierung ausführen, um vorhandene Daten auf beiden Seiten, also auf der Seite der Finance and Operations-Apps und der Seite der Customer Engagement-Apps, zu verarbeiten. Sie können diese erste Synchronisierung überspringen, wenn Sie keine Daten zwischen den beiden Umgebungen synchronisieren müssen.

Bei einer ersten Synchronisierung können Sie vorhandene Daten bidirektional von einer App in eine andere kopieren. Es gibt verschiedene Einrichtungsszenarien, je nachdem, welche Umgebungen Sie bereits verwenden und welche Art von Daten sich in den Umgebungen befinden.

Die folgenden Einrichtungsszenarien werden unterstützt:

+ [Eine neue Finance and Operations Anwendungsinstanz und eine neue Customer Engagement Anwendungsinstanz](#new-new)
+ [Eine neue Finance and Operations Anwendungsinstanz und eine bestehende Customer Engagement Anwendungsinstanz](#new-existing)
+ [Eine neue Finance and Operations-Anwendungsinstanz, die über Demodaten und eine neue Customer Engagement Anwendungsinstanz verfügt](#new-data-new)
+ [Eine neue Finance and Operations App-Instanz, die über Demodaten verfügt, und eine bestehende Customer Engagement App-Instanz](#new-data-existing)
+ [Eine bestehende Finance and Operations Anwendungsinstanz und eine neue Customer Engagement Anwendungsinstanz](#existing-new)
+ [Eine bestehende Finance and Operations Anwendungsinstanz und eine bestehende Customer Engagement Anwendungsinstanz](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="new-new"></a>Eine neue Finance and Operations Anwendungsinstanz und eine neue Customer Engagement Anwendungsinstanz

Um eine Verbindung duales Schreiben zwischen einer neuen Instanz einer Finance and Operations-Anwendung, die keine Daten hat, und einer neuen Instanz einer Customer Engagement Anwendung einzurichten, folgen Sie den Schritten in [Duales Schreiben einrichten von Lifecycle Services](lcs-setup.md). Wenn der Verbindungsaufbau abgeschlossen ist, werden die folgenden Aktionen automatisch ausgeführt:

- Eine neue, leere Finance and Operations-Umgebung wird bereitgestellt.
- Es wird eine neue, leere Instanz einer Customer Engagement Anwendung bereitgestellt, in der die CRM-Prime-Lösung installiert wird.
- Eine Dual-Write-Verbindung wird für DAT-Firmendaten hergestellt.
- Tabellenzuordnungen werden für die Live-Synchronisierung aktiviert.

Beide Umgebungen sind dann für die Live-Datensynchronisierung bereit.

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a>Eine neue Finance and Operations Anwendungsinstanz und eine bestehende Customer Engagement Anwendungsinstanz

Um eine Verbindung duales Schreiben zwischen einer neuen Instanz einer Finance and Operations-Anwendung, die keine Daten hat, und einer bestehenden Instanz einer Customer Engagement Anwendung einzurichten, folgen Sie den Schritten in [Duales Schreiben einrichten von Lifecycle Services](lcs-setup.md). Wenn der Verbindungsaufbau abgeschlossen ist, werden die folgenden Aktionen automatisch ausgeführt:

- Eine neue, leere Finance and Operations-Umgebung wird bereitgestellt.
- Eine Dual-Write-Verbindung wird für DAT-Firmendaten hergestellt.
- Tabellenzuordnungen werden für die Live-Synchronisierung aktiviert.

Beide Umgebungen sind dann für die Live-Datensynchronisierung bereit.

Um die vorhandenen Dataverse-Daten mit der Finance and Operations-Anwendung zu synchronisieren, folgen Sie diesen Schritten.

1. Erstellen Sie ein neues Unternehmen in der Finance and Operations-Anwendung.
2. Fügen Sie das Unternehmen zum Dual-Write-Verbindungsaufbau hinzu.
3. [Bootstrap](bootstrap-company-data.md) die Dataverse-Daten unter Verwendung eines aus drei Buchstaben bestehenden Buchungscodees der International Organization for Standardization (ISO).
4. Führen Sie die Funktion **Erstsynchronisierung** für die Tabellen aus, für die Sie Daten synchronisieren möchten.

Links zu einem Beispiel und einem alternativen Ansatz finden Sie im Abschnitt [Beispiel](#example) später in diesem Thema.

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a>Eine neue Finance and Operations Anwendungsinstanz, die über Demodaten und eine neue Customer Engagement Anwendungsinstanz verfügt

Um eine Verbindung duales Schreiben zwischen einer neuen Instanz einer Finance and Operations-Anwendung, die über Demodaten verfügt, und einer neuen Instanz einer Customer Engagement Anwendung einzurichten, folgen Sie den Schritten im Abschnitt [Eine neue Finance and Operations-Anwendungsinstanz und eine neue Customer Engagement Anwendungsinstanz](#new-new) weiter oben in diesem Thema. Wenn der Verbindungsaufbau abgeschlossen ist und Sie die Demodaten mit der Customer Engagement Anwendung synchronisieren möchten, folgen Sie diesen Schritten.

1. Öffnen Sie die Anwendung Finance and Operations von der LCS-Seite, melden Sie sich an und gehen Sie dann zu **Datenverwaltung \> Dual-write**.
2. Führen Sie die Funktion **Erstsynchronisierung** für die Tabellen aus, für die Sie Daten synchronisieren möchten.

Links zu einem Beispiel und einem alternativen Ansatz finden Sie im Abschnitt [Beispiel](#example).

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a>Eine neue Finance and Operations App-Instanz, die über Demodaten verfügt, und eine bestehende Customer Engagement App-Instanz

Um eine Verbindung duales Schreiben zwischen einer neuen Instanz einer Finance and Operations-Anwendung, die über Demodaten verfügt, und einer bestehenden Instanz einer Customer Engagement Anwendung einzurichten, folgen Sie den Schritten im Abschnitt [Eine neue Finance and Operations-Anwendungsinstanz und eine neue Customer Engagement Anwendungsinstanz](#new-existing) weiter oben in diesem Thema. Wenn der Verbindungsaufbau abgeschlossen ist und Sie die Demodaten mit der Customer Engagement Anwendung synchronisieren möchten, folgen Sie diesen Schritten.

1. Öffnen Sie die Anwendung Finance and Operations von der LCS-Seite, melden Sie sich an und gehen Sie dann zu **Datenverwaltung \> Dual-write**.
2. Führen Sie die Funktion **Erstsynchronisierung** für die Tabellen aus, für die Sie Daten synchronisieren möchten.

Um die vorhandenen Dataverse-Daten mit der Finance and Operations-Anwendung zu synchronisieren, folgen Sie diesen Schritten.

1. Erstellen Sie ein neues Unternehmen in der Finance and Operations-Anwendung.
2. Fügen Sie das Unternehmen zum Dual-Write-Verbindungsaufbau hinzu.
3. [Bootstrap](bootstrap-company-data.md) der Dataverse-Daten unter Verwendung eines dreibuchstabigen ISO-Buchungscodees.
4. Führen Sie die Funktion **Erstsynchronisierung** für die Tabellen aus, für die Sie Daten synchronisieren möchten.

Links zu einem Beispiel und einem alternativen Ansatz finden Sie im Abschnitt [Beispiel](#example).

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a>Eine bestehende Finance and Operations Anwendungsinstanz und eine neue Customer Engagement Anwendungsinstanz

Die Einrichtung einer Verbindung duales Schreiben zwischen einer bestehenden Instanz einer Finance and Operations-Anwendung und einer neuen Instanz einer Customer Engagement Anwendung erfolgt in der Finance and Operation-Umgebung.

1. [Richten Sie die Verbindung von der Finance and Operations-Anwendung aus ein](enable-dual-write.md).
2. Führen Sie die Funktion **Erstsynchronisierung** für die Tabellen aus, für die Sie Daten synchronisieren möchten.

Links zu einem Beispiel und einem alternativen Ansatz finden Sie im Abschnitt [Beispiel](#example).

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a>Eine bestehende Finance and Operations Anwendungsinstanz und eine bestehende Customer Engagement Anwendungsinstanz

Die Einrichtung einer Verbindung für duales Schreiben zwischen einer bestehenden Instanz einer Finance and Operations-App und einer bestehenden Instanz einer Customer Engagement-App erfolgt in der Finance and Operation-Umgebung.

1. [Richten Sie die Verbindung von der Finance and Operations-Anwendung aus ein](enable-dual-write.md).
2. Um die vorhandenen Dataverse-Daten mit der Finance and Operations-Anwendung zu synchronisieren, [Bootstrap](bootstrap-company-data.md) die Dataverse-Daten unter Verwendung eines dreibuchstabigen ISO-Buchungskreises.
3. Führen Sie die Funktion **Erstsynchronisierung** für die Tabellen aus, für die Sie Daten synchronisieren möchten.

Links zu einem Beispiel und einem alternativen Ansatz finden Sie im Abschnitt [Beispiel](#example).

## <a name="example"></a>Beispiel

Ein Beispiel finden Sie unter [Aktivieren der Tabellenzuordnung für Kunden V3 – Kontakte](enable-entity-map.md#enable-table-map).

Einen alternativen Ansatz basierend auf den Datenmengen in jeder Entität, für die eine Erstsynchronisierung ausgeführt werden muss, finden Sie unter [Überlegungen zur Erstsynchronisierung](initial-sync-guidance.md).
