---
title: Übersicht über Add-In Bestandstransparenz
description: Dieses Thema erklärt, was Inventory Visibility ist und beschreibt seine Funktionen.
author: yufeihuang
ms.date: 03/18/2022
ms.topic: overview
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 9eb8a135d2415c867c746a1c40a80cdb84819c0e
ms.sourcegitcommit: d475dea4cf13eae2f0ce517542c5173bb9d52c1c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/05/2022
ms.locfileid: "8547900"
---
# <a name="inventory-visibility-add-in-overview"></a>Übersicht über das Bestandsanzeige-Add-In

[!include [banner](../includes/banner.md)]

Das Bestandssichtbarkeits-Add-In (auch *Bestandssichtbarkeitsdienst* genannt) ist ein unabhängiger und hochgradig skalierbarer Microservice, der es ermöglicht, Lagerbestandsänderungen in Echtzeit zu verbuchen und die Sichtbarkeit über alle Ihre Datenquellen und Kanäle hinweg zu verfolgen. Es bietet eine Plattform, mit der Sie Ihren globalen Bestand verwalten können, indem Sie Funktionen nutzen, die die folgende Liste umfassen (aber nicht darauf beschränkt sind):

- Verfolgen Sie zentral den aktuellen Lagerbestand (wie z.B. vorhanden, bestellt, gekauft, unterwegs, zurückgegeben und unter Quarantäne gestellt) über alle Ihre Datenquellen, Lager und Standorte hinweg, indem Sie Ihre Supply Chain Management- oder Logistikdatenquellen von Drittanbietern (wie z.B. Auftragsverwaltungssysteme, Enterprise Resource Planning-Systeme von Drittanbietern \[ERP \], Point of Sale-Systeme \[POS \] und Lagerverwaltungssysteme) mit dem Inventory Visibility-Service verbinden.
- Fragen Sie die Verfügbarkeit von Lagerbeständen und Fehlmengen ab und erhalten Sie sofortige Antworten, indem Sie den Dienst Inventory Visibility direkt aufrufen.
- Vermeiden Sie ein Überangebot, insbesondere wenn Ihr Bedarf aus verschiedenen Kanälen stammt, indem Sie im Dienst Inventory Visibility Soft-Reservierungen in Echtzeit vornehmen.
- Verwalten Sie versprochene Bestellungen und Kundenerwartungen besser, indem Sie genaue aktuelle oder nächstverfügbare Daten bereitstellen, so dass die Funktion „Omnichannel Available-to-Promise“ (ATP) die voraussichtlichen Termine für die Auftragserfüllung berechnen kann.

## <a name="extensibility"></a>Erweiterbarkeit

Der Inventory Visibility-Dienst ist in hohem Maße erweiterbar, da die Dateneingabe und -ausgabe nicht auf Microsoft-Anwendungen beschränkt ist. Externe Systeme können über RESTful Application Programming Interfaces (APIs) auf den Dienst zugreifen. Zusätzlich zu den Out-of-Box-Zuordnungen, die für die Datenquelle und die Dimensionen des Supply Chain Managements bereitgestellt werden, können Sie Inventory Visibility mit mehreren Systemen von Drittanbietern integrieren, indem Sie über die Konfigurations-App zusätzliche Datenquellen, Kennzahlen für den Lagerbestand (im Supply Chain Management-Service als *physikalische Kennzahlen* bezeichnet) und Bestandsdimensionen festlegen. Auf diese Weise können Sie Ihre verschiedenen Datenquellen und vordefinierten Bestandsdimensionen flexibel abfragen und ändern.

Da Inventory Visibility auf Microsoft Dataverse aufbaut, können seine Daten außerdem für die Erstellung und Integration von Power Apps verwendet werden. Sie können auch Power BI verwenden, um angepasste Dashboards zu erstellen, die Ihren geschäftlichen Anforderungen entsprechen.

## <a name="scalability"></a>Skalierbarkeit

Der Inventory Visibility Service kann je nach Datenvolumen nach oben oder unten skaliert werden. Die Skalierbarkeit erfolgt größtenteils nahtlos und wird vom Microsoft Plattformteam auf der Grundlage einer automatischen Erkennung und Bewertung Ihres Transaktionsdatenvolumens durchgeführt.

## <a name="feature-highlights"></a>Besondere Funktionen

### <a name="get-a-global-view-of-real-time-inventory"></a>Globale Ansicht des Bestands in Echtzeit abrufen

Inventory Visibility stellt sicher, dass Sie jederzeit Zugriff auf die aktuellsten Bestandsmengen haben, und zwar über alle Ihre Kanäle, Standorte und Lager hinweg. Sie werden am meisten davon profitieren, wenn Sie es zur Unterstützung Ihres täglichen operativen Geschäfts einsetzen, wann immer Sie Datensätze über Bestände erhalten müssen. Physischer Lagerbestand, verkaufte Mengen und gekaufte Mengen sind sofort verfügbar. Sie können auch andere Messungen des physischen Bestands (z.B. zurückgegebene, unter Quarantäne gestellte und gebuchte Daten) nach Bedarf konfigurieren, um diese Details in Echtzeit zu erhalten. Inventory Visibility kann Millionen von Bestandsänderungsbuchungen effizient verarbeiten. Diese Daten können aggregiert werden und in den neuesten Bestandsmengen im Service sofort, pro Sekunde oder pro Minute berücksichtigt werden, je nachdem, in welchem Intervall die Daten gepostet werden. Weitere Informationen finden Sie unter [Inventory Visibility öffentliche APIs](inventory-visibility-api.md).

### <a name="soft-reservation-to-avoid-overselling-across-all-order-channels"></a>Weiche Reservierung zur Vermeidung von Overselling über alle Bestellkanäle hinweg

Mit einer *Soft-Reservierung* können Sie bestimmte Mengen zuweisen oder kennzeichnen, um einen Auftrag oder Bedarf zu erfüllen. Eine Soft-Reservierung wirkt sich nicht auf den physischen Bestand aus, aber sie zieht von der *zur Reservierung verfügbaren* Bestandsmenge ab und stellt eine aktualisierte Menge für die zukünftige Auftragserfüllung bereit. Diese Funktion ist nützlich, wenn Verkaufsanfragen oder Aufträge aus einem oder mehreren Kanälen oder Datensätzen in Ihr Unternehmen kommen, die nicht in Ihrem ERP-System (Enterprise Resource Planning) gespeichert sind.

Wenn Sie im Service Inventory Visibility keine Soft-Reservierungen verwenden, müssen Sie warten, bis der Auftrag mit Ihrem ERP-System synchronisiert und verarbeitet wurde, um eine Aktualisierung der physischen Bestandsmenge zu erhalten. Dieser Prozess hat normalerweise eine enorme Latenzzeit. Soft-Reservierungen werden jedoch jedes Mal sofort wirksam, wenn eine Verkaufsanfrage oder ein Auftrag in Ihren Vertriebskanälen generiert wird. Sie helfen also dabei, Überverkäufe zu vermeiden, indem sie sicherstellen, dass sich Ihre Omnichannel-Bestellungen nicht gegenseitig behindern, wenn sie schließlich im ERP-System ankommen. Soft-Reservierungen stellen außerdem sicher, dass Sie alle versprochenen Bestellungen erfüllen können. Sie helfen Ihnen also, die Erwartungen Ihrer Kunden zu erfüllen und sie an sich zu binden. Weitere Informationen finden Sie unter [Reservierungen in Inventory Visibility](inventory-visibility-reservations.md).

### <a name="immediate-response-of-atp-dates-confirmation"></a>Sofortige Rückmeldung der ATP-Datenbestätigung

Die Einsicht in Ihren für die nahe Zukunft prognostizierten Bestand (einschließlich Angaben zu Vorrat, Bedarf und prognostiziertem Lagerbestand) ist wichtig, denn sie hilft Ihrer Firma, die folgenden Ziele zu erreichen:

- Minimieren Sie die Bestände, um die Kosten für die Kalkulation zu senken.
- Erleichtern Sie die interne Verarbeitung von Bestellungen, damit Verkäufer Versand- und Liefertermine auf der Grundlage der Verfügbarkeit der bestellten Produkte berechnen können.
- Bieten Sie Transparenz darüber, wann Kunden erwarten können, dass ein vergriffenes Element wieder verfügbar ist, indem Sie das Datum der nächsten Verfügbarkeit angeben.

Die ATP Funktion lässt sich leicht in Ihren täglichen Auftragsabwicklungsprozess adaptieren. Am wichtigsten ist, dass die ATP Funktion wie andere Inventory Visibility Angebote *global und in Echtzeit* ist. Daher können Sie mehrere ATP-Berechnungsformeln festlegen, um vollständige Abfragen zur Bestandsverfügbarkeit zu erhalten, die alle Ihre Geschäftskanäle und Datenquellen abdecken. Weitere Informationen finden Sie unter [Inventory Visibility Lagerbestand Änderungspläne und verfügbar zu versprechen](inventory-visibility-available-to-promise.md).

### <a name="compatibility-with-advanced-warehouse-management-items"></a>Kompatibilität mit Elementen der erweiterten Lagerverwaltung

Microsoft strebt eine Out-of-Box-Integration mit der erweiterten Lagerverwaltung (WHS) an, damit auch WHS-Kunden in den Genuss der Vorteile des Dienstes Inventory Visibility kommen. In der Version 2022 Wave 1 (öffentliche Vorschau im März) unterstützt der Bestandsservice WHS-Abfragen zum Lagerbestand und ATP. Die Funktion der weichen Reservierung und Zuweisung wird für WHS-Kunden in der nächsten Welle unterstützt. Weitere Informationen finden Sie unter [Inventory Visibility-Unterstützung für WHS-Artikel](inventory-visibility-whs-support.md).

## <a name="licensing"></a>Lizenzierung

Der Inventory Visibility Service ist in den folgenden Versionen verfügbar:

- **Inventory Visibility-Add-In für Microsoft Dynamics 365 Supply Chain Management** - Für Unternehmen, die über eine gültige Supply Chain Management-Lizenz verfügen, ist Inventory Visibility ohne zusätzliche Lizenzkosten verfügbar. Sie können noch heute damit beginnen, ihn zu prüfen. Einzelheiten zur Installation finden Sie unter [Installation und Festlegen von Inventory Visibility](inventory-visibility-setup.md).
- **Inventory Visibility Service als Bestandteil von IOM** - Diese Version ist entweder für Kunden von Intelligent Order Management (IOM) oder für Firmen, die Supply Chain Management nicht als ERP-System einsetzen. Die Lizenz ist in dem IOM-Bündel enthalten. Weitere Informationen finden Sie unter [Intelligent Order Management Überblick](/dynamics365/intelligent-order-management/overview).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
