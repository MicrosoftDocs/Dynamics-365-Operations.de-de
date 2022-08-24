---
title: Anleitung zum Einrichten des dualen Schreibens
description: In diesem Artikel werden die Szenarien beschrieben, die für die Dual-Write-Einrichtung unterstützt werden.
author: RamaKrishnamoorthy
ms.date: 06/28/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: b27cabf495448fcd82edd374bb59e6e5a664c7e9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289743"
---
# <a name="guidance-for-dual-write-setup"></a>Anleitung zum Einrichten des dualen Schreibens

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]



Sie können eine Dual-write Verbindung zwischen einer Finanz- und Betriebs-Umgebung und einer Dataverse Umgebung festlegen.

+ Eine **Umgebung für Finanzen und Vorgänge** bietet die zugrundeliegende Plattform für **Finanz- und Betriebs-Apps** (zum Beispiel Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce und Dynamics 365 Human Resources).
+ Eine **Dataverse-Umgebung** bietet die zugrunde liegende Plattform für **Kundenbindungs-Apps** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Column Service, Dynamics 365 Marketing und Dynamics 365 Project Service Automation).


> [!IMPORTANT]
> Das Modul „Personalressourcen“ in Dynamics 365 Finance unterstützt Verbindungen für duales Schreiben, die Dynamics 365 Human Resources-App jedoch nicht.

Der Einrichtungsmechanismus variiert je nach Ihrem Abonnement und der Umgebung:

+ Für neue Instanzen von Finanz- und Betriebs-Apps beginnt die Einrichtung einer Dual-write Verbindung in Microsoft Dynamics Lifecycle Services (LCS). Wenn Sie eine Lizenz für Microsoft Power Platform haben, erhalten Sie eine neue Dataverse-Umgebung, wenn Ihr Mandant keine hat.
+ Bei bestehenden Instanzen von Finanz- und Betriebs-Apps beginnt die Einrichtung einer Dual-write-Verbindung in der Finanz- und Betriebs-Umgebung.

Bevor Sie Dual-write für eine Entität starten, können Sie eine erste Synchronisierung ausführen, um die vorhandenen Daten auf beiden Seiten zu bearbeiten: Finanz- und Betriebs-Apps und Customer-Engagement-Apps. Sie können diese erste Synchronisierung überspringen, wenn Sie keine Daten zwischen den beiden Umgebungen synchronisieren müssen.

Bei einer ersten Synchronisierung können Sie vorhandene Daten bidirektional von einer App in eine andere kopieren. Es gibt verschiedene Einrichtungsszenarien, je nachdem, welche Umgebungen Sie bereits verwenden und welche Art von Daten sich in den Umgebungen befinden.

Die folgenden Einrichtungsszenarien werden unterstützt:

+ [Eine neue Finanz- und Betriebs-App-Instanz und eine neue Customer-Engagement-App-Instanz](#new-new)
+ [Eine neue Finanz- und Betriebs-App-Instanz und eine bestehende Customer-Engagement-App-Instanz](#new-existing)
+ [Eine neue Instanz einer Finanz- und Betriebs-App, die Daten enthält, und eine neue Instanz einer Customer-Engagement-App](#new-data-new)
+ [Eine neue Instanz einer Finanz- und Betriebs-App, die über Daten verfügt, und eine bestehende Instanz einer Customer-Engagement-App](#new-data-existing)
+ [Eine bestehende Finanz- und Betriebs-App-Instanz und eine neue Customer-Engagement-App-Instanz](#existing-new)
+ [Eine bestehende Finanz- und Betriebs-App-Instanz und eine bestehende Customer-Engagement-App-Instanz](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="new-new"></a>Eine neue Finanz- und Betriebs-App-Instanz und eine neue Customer-Engagement-App-Instanz

Um eine Dual-write-Verbindung zwischen einer neuen Instanz einer Finanz- und Betriebs-App, die keine Daten hat, und einer neuen Instanz einer Customer-Engagement-App festzulegen, folgen Sie den Schritten unter [Dual-write-Einrichtung von Lifecycle Services](lcs-setup.md). Wenn der Verbindungsaufbau abgeschlossen ist, werden die folgenden Aktionen automatisch ausgeführt:

- Eine neue, leere Finanz- und Betriebs-Umgebung wird bereitgestellt.
- Es wird eine neue, leere Instanz einer Customer Engagement Anwendung bereitgestellt, in der die CRM-Prime-Lösung installiert wird.
- Eine Dual-Write-Verbindung wird für DAT-Firmendaten hergestellt.
- Tabellenzuordnungen werden für die Live-Synchronisierung aktiviert.

Beide Umgebungen sind dann für die Live-Datensynchronisierung bereit.

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a>Eine neue Finanz- und Betriebs-App-Instanz und eine bestehende Customer-Engagement-App-Instanz

Um eine Dual-write-Verbindung zwischen einer neuen Instanz einer Finanz- und Betriebs-App, die keine Daten hat, und einer vorhandenen Instanz einer Customer-Engagement-App festzulegen, folgen Sie den Schritten in [Dual-write-Einrichtung von Lifecycle Services](lcs-setup.md). Wenn der Verbindungsaufbau abgeschlossen ist, werden die folgenden Aktionen automatisch ausgeführt:

- Eine neue, leere Finanz- und Betriebs-Umgebung wird bereitgestellt.
- Eine Dual-Write-Verbindung wird für DAT-Firmendaten hergestellt.
- Tabellenzuordnungen werden für die Live-Synchronisierung aktiviert.

Beide Umgebungen sind dann für die Live-Datensynchronisierung bereit.

Um die vorhandenen Dataverse-Daten mit der Finanz- und Betriebs-App zu synchronisieren, gehen Sie folgendermaßen vor.

1. Erstellen Sie eine neue Firma in der Finanz- und Betriebs-App.
2. Fügen Sie das Unternehmen zum Dual-Write-Verbindungsaufbau hinzu.
3. [Bootstrap](bootstrap-company-data.md) die Dataverse-Daten unter Verwendung eines aus drei Buchstaben bestehenden Buchungscodees der International Organization for Standardization (ISO).
4. Führen Sie die Funktion **Erstsynchronisierung** für die Tabellen aus, für die Sie Daten synchronisieren möchten.

Links zu einem Beispiel und einem alternativen Ansatz finden Sie im Abschnitt [Beispiel](#example) später in diesem Artikel.

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a>Eine neue Instanz einer Finanz- und Betriebs-App, die Daten enthält, und eine neue Instanz einer Customer-Engagement-App

Um eine Dual-write-Verbindung zwischen einer neuen Instanz einer Finanz- und Betriebs-App, die Daten enthält, und einer neuen Instanz einer Customer-Engagement-App festzulegen, folgen Sie den Schritten im Abschnitt [Eine neue Instanz einer Finanz- und Betriebs-App und eine neue Instanz einer Customer-Engagement-App](#new-new) weiter oben in diesem Artikel. Wenn der Verbindungsaufbau abgeschlossen ist und Sie die Demodaten mit der Customer Engagement Anwendung synchronisieren möchten, folgen Sie diesen Schritten.

1. Öffnen Sie die App Finanzen und Vorgänge von der LCS Seite aus, melden Sie sich an und gehen Sie dann auf **Datenverwaltung \> Dual-write**.
2. Führen Sie die Funktion **Erstsynchronisierung** für die Tabellen aus, für die Sie Daten synchronisieren möchten.

Links zu einem Beispiel und einem alternativen Ansatz finden Sie im Abschnitt [Beispiel](#example).

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a>Eine neue Instanz einer Finanz- und Betriebs-App, die über Daten verfügt, und eine bestehende Instanz einer Customer-Engagement-App

Um eine Dual-write-Verbindung zwischen einer neuen Instanz einer Finanz- und Betriebs-App, die über Daten verfügt, und einer bestehenden Instanz einer Customer-Engagement-App einzurichten, folgen Sie den Schritten im Abschnitt [Eine neue Instanz einer Finanz- und Betriebs-App und eine bestehende Instanz einer Customer-Engagement-App](#new-existing) weiter oben in diesem Artikel. Wenn der Verbindungsaufbau abgeschlossen ist und Sie die Demodaten mit der Customer Engagement Anwendung synchronisieren möchten, folgen Sie diesen Schritten.

1. Öffnen Sie die App Finanzen und Vorgänge von der LCS Seite aus, melden Sie sich an und gehen Sie dann auf **Datenverwaltung \> Dual-write**.
2. Führen Sie die Funktion **Erstsynchronisierung** für die Tabellen aus, für die Sie Daten synchronisieren möchten.

Um die vorhandenen Dataverse-Daten mit der Finanz- und Betriebs-App zu synchronisieren, gehen Sie folgendermaßen vor.

1. Erstellen Sie eine neue Firma in der Finanz- und Betriebs-App.
2. Fügen Sie das Unternehmen zum Dual-Write-Verbindungsaufbau hinzu.
3. [Bootstrap](bootstrap-company-data.md) der Dataverse-Daten unter Verwendung eines dreibuchstabigen ISO-Buchungscodees.
4. Führen Sie die Funktion **Erstsynchronisierung** für die Tabellen aus, für die Sie Daten synchronisieren möchten.

Links zu einem Beispiel und einem alternativen Ansatz finden Sie im Abschnitt [Beispiel](#example).

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a>Eine bestehende Finanz- und Betriebs-App-Instanz und eine neue Customer-Engagement-App-Instanz

Die Einrichtung einer Dual-write-Verbindung zwischen einer bestehenden Instanz einer Finanz- und Betriebs-App und einer neuen Instanz einer Customer-Engagement-App erfolgt in der Umgebung Finance and Operation.

1. [Verbindung von der Finanz- und Betriebs-App festlegen](enable-dual-write.md).
2. Führen Sie die Funktion **Erstsynchronisierung** für die Tabellen aus, für die Sie Daten synchronisieren möchten.

Links zu einem Beispiel und einem alternativen Ansatz finden Sie im Abschnitt [Beispiel](#example).

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a>Eine bestehende Instanz einer Finanz- und Betriebs-App und eine bestehende Instanz einer Customer-Engagement-App

Die Einrichtung einer Dual-write-Verbindung zwischen einer bestehenden Instanz einer Finanz- und Betriebs-App und einer bestehenden Instanz einer Customer-Engagement-App erfolgt in der Umgebung Finance and Operation.

1. [Verbindung von der Finanz- und Betriebs-App festlegen](enable-dual-write.md).
2. Um die vorhandenen Dataverse-Daten mit der Finanz- und Betriebs-App zu synchronisieren, [booten](bootstrap-company-data.md) Sie die Dataverse-Daten, indem Sie einen dreibuchstabigen ISO-Firmencode verwenden.
3. Führen Sie die Funktion **Erstsynchronisierung** für die Tabellen aus, für die Sie Daten synchronisieren möchten.

Links zu einem Beispiel und einem alternativen Ansatz finden Sie im Abschnitt [Beispiel](#example).

## <a name="example"></a>Beispiel

Ein Beispiel finden Sie unter [Aktivieren der Tabellenzuordnung für Kunden V3 – Kontakte](enable-entity-map.md#enable-table-map).

Einen alternativen Ansatz basierend auf den Datenmengen in jeder Entität, für die eine Erstsynchronisierung ausgeführt werden muss, finden Sie unter [Überlegungen zur Erstsynchronisierung](initial-sync-guidance.md).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
