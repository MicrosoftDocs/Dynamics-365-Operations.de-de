---
title: Übersicht über Add-In Bestandstransparenz
description: Dieses Thema erklärt, was Inventory Visibility ist und beschreibt seine Funktionen.
author: yufeihuang
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 1ea1d8c1b0e8c996ead8461005960fa756ce6ca7
ms.sourcegitcommit: 1e5a46271bf7fae2f958d2b1b666a8d2583e04a8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2021
ms.locfileid: "7678908"
---
# <a name="inventory-visibility-add-in-overview"></a>Übersicht über Add-In Bestandstransparenz

[!include [banner](../includes/banner.md)]

Das Bestandssichtbarkeits-Add-In (auch *Bestandssichtbarkeit* genannt) ist ein unabhängiger und hoch skalierbarer Microservice, der die Verfolgung des Lagerbestands in Echtzeit ermöglicht. Daher bietet es eine globale Sicht auf den Bestand.

Externe Systeme greifen über RESTful-APIs auf den Dienst zu. Auf diese Weise können sie entweder Lagerbestandsinformationen zu vorgegebenen Sets von Dimensionen abfragen oder Änderungen an Ihrem Bestand in verschiedenen angepassten Datenquellen vornehmen.

Als Microservice, der auf Microsoft Dataverse aufgebaut ist, bietet Inventory Visibility Erweiterbarkeit. Sie können Power Apps verwenden, um Apps zu erstellen. Sie können Power BI auch anwenden, um angepasste Funktionalität bereitzustellen, die Ihren geschäftlichen Anforderungen entspricht.

Sie können Inventory Visibility mit mehreren Systemen von Drittanbietern integrieren, indem Sie Konfigurationsoptionen für standardisierte Bestandsdimensionen festlegen und Transaktionstypen einrichten. Inventory Visibility unterstützt auch angepasste Erweiterbarkeit durch konfigurierbare berechnete Mengen.

## <a name="inventory-visibility-integration-with-dynamics-365-supply-chain-management"></a>Inventory Visibility-Integration mit Dynamics 365 Supply Chain Management

Die integrierte Lösung zieht Bestandsdaten von Dynamics 365 Supply Chain Management und verfolgt kontinuierlich Bestandsänderungen. Weitere Informationen finden Sie unter [Bestandsanzeige installieren und einrichten](inventory-visibility-setup.md) und [Bestandsanzeige konfigurieren](inventory-visibility-configuration.md).

## <a name="get-a-global-view-of-inventory"></a>Globale Ansicht des Bestands erhalten

Mit der integrierten Lösung können Sie Ihre eigenen Datenquellen definieren und die Bestandsdaten zentralisieren. Weitere Informationen finden Sie unter [Bestandsanzeige konfigurieren](inventory-visibility-configuration.md).

Es gibt zwei Ansätze, um Ihren Bestand einzusehen:

- Senden Sie eine Abfrage über die Hochleistungs-API. Diese API kann Bestandsdaten nahezu in Echtzeit direkt von einer zwischengespeicherten Instanz zurückgeben. Verträge und Beispiele finden Sie unter [Öffentliche APIs für Inventory Visibility](inventory-visibility-api.md).
- Zeigen Sie die rohe Lagerbestandsliste an. Diese Liste wird periodisch von einer zwischenspeichernden Instanz synchronisiert und ist in Bestand in Dataverse zu sehen. Weitere Informationen finden Sie unter [Inventory Visibility App](inventory-visibility-power-platform.md).

## <a name="soft-reservations"></a>Soft-Reservierungen

Soft-Reservierungen werden angewendet, wenn ein Unternehmen eine bestimmte Menge an Produkten reservieren muss, um z. B. die Erfüllung von Verkaufsaufträgen zu unterstützen, die einen Überverkauf vermeiden. Wenn ein Verkaufsauftrag im Supply Chain Management oder anderen Auftragsverwaltungssystemen erstellt und bestätigt wird, wird eine Anfrage zur Reservierung der Menge an Inventory Visibility gesendet. Mit Inventory Visibility können Sie Produkte reservieren, die Details zu Dimensionen und bestimmten Bestandstransaktionen haben. (Weitere Informationen finden Sie unter [Inventory Visibility App](inventory-visibility-power-platform.md).) Nachdem die Menge erfolgreich reserviert wurde, wird eine Reservierungs-ID zurückgegeben. Sie können diese Reservierungs-ID verwenden, um im Supply Chain Management oder in anderen Auftragsverwaltungssystemen eine Verknüpfung zurück zur ursprünglichen Bestellung herzustellen.

Die Funktionalität ist so ausgelegt, dass eine Reservierung in Inventory Visibility nicht die Gesamtmenge verändert. Stattdessen wird nur die reservierte Menge geflaggt. (Aus diesem Grund wird sie als *Soft-Reservierung* bezeichnet.) Die soft-reservierte Menge kann ausgeglichen werden, wenn die Produkte im Supply Chain Management oder einem System eines Drittanbieters verbraucht werden, indem die API erneut aufgerufen wird, um einen Mengenabzug vorzunehmen und die Gesamtmenge in Inventory Visibility zu aktualisieren. Weitere Informationen finden Sie unter [Reservierungen in Inventory Visibility](inventory-visibility-reservations.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
