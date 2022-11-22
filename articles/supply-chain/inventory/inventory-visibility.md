---
title: Übersicht über das Inventory Visibility-Add-In
description: Dieser Artikel erklärt, was Inventory Visibility ist und beschreibt seine Funktionen.
author: yufeihuang
ms.date: 11/04/2022
ms.topic: overview
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: dd790bcaada0c1a05e46b4edacaa31fc4e15be92
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762806"
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

Die folgende Abbildung zeigt die Bestandsanzeige-Architektur.

[<img src="media/inventory-visibility-architecture.png" alt="Inventory Visibility architecture." title="Bestandsanzeige-Architektur" width="720" />](media/inventory-visibility-architecture.png)

## <a name="feature-highlights"></a>Besondere Funktionen

### <a name="get-a-global-view-of-real-time-inventory"></a>Globale Ansicht des Bestands in Echtzeit abrufen

Inventory Visibility stellt sicher, dass Sie jederzeit Zugriff auf die aktuellsten Bestandsmengen haben, und zwar über alle Ihre Kanäle, Standorte und Lager hinweg. Sie werden am meisten davon profitieren, wenn Sie es zur Unterstützung Ihres täglichen operativen Geschäfts einsetzen, wann immer Sie Datensätze über Bestände erhalten müssen. Physischer Lagerbestand, verkaufte Mengen und gekaufte Mengen sind sofort verfügbar. Sie können auch andere Messungen des physischen Bestands (z.B. zurückgegebene, unter Quarantäne gestellte und gebuchte Daten) nach Bedarf konfigurieren, um diese Details in Echtzeit zu erhalten. Inventory Visibility kann Millionen von Bestandsänderungsbuchungen effizient verarbeiten. Diese Daten können aggregiert werden und in den neuesten Bestandsmengen im Service sofort, pro Sekunde oder pro Minute berücksichtigt werden, je nachdem, in welchem Intervall die Daten gepostet werden. Weitere Informationen finden Sie unter [Inventory Visibility öffentliche APIs](inventory-visibility-api.md).

### <a name="central-inventory-adjustment"></a>Zentrale Bestandsanpassung

Bestandsanzeige ermöglicht es externen Systemen, ihre API aufzurufen, um Bestandsänderungen zu veröffentlichen. Die Änderungen werden sofort in der Bestandsanzeige wirksam. Daher wird der verfügbare Lagerbestand sofort abgeführt.

### <a name="soft-reservation-to-avoid-overselling-across-all-order-channels"></a>Weiche Reservierung zur Vermeidung von Overselling über alle Bestellkanäle hinweg

Mit einer *Soft-Reservierung* können Sie bestimmte Mengen zuweisen oder kennzeichnen, um einen Auftrag oder Bedarf zu erfüllen. Eine Soft-Reservierung wirkt sich nicht auf den physischen Bestand aus, aber sie zieht von der *zur Reservierung verfügbaren* Bestandsmenge ab und stellt eine aktualisierte Menge für die zukünftige Auftragserfüllung bereit. Diese Funktion ist nützlich, wenn Verkaufsanfragen oder Aufträge aus einem oder mehreren Kanälen oder Datensätzen in Ihr Unternehmen kommen, die nicht in Ihrem ERP-System (Enterprise Resource Planning) gespeichert sind.

Wenn Sie im Service Inventory Visibility keine Soft-Reservierungen verwenden, müssen Sie warten, bis der Auftrag mit Ihrem ERP-System synchronisiert und verarbeitet wurde, um eine Aktualisierung der physischen Bestandsmenge zu erhalten. Dieser Prozess hat normalerweise eine enorme Latenzzeit. Soft-Reservierungen werden jedoch jedes Mal sofort wirksam, wenn eine Verkaufsanfrage oder ein Auftrag in Ihren Vertriebskanälen generiert wird. Sie helfen also dabei, Überverkäufe zu vermeiden, indem sie sicherstellen, dass sich Ihre Omnichannel-Bestellungen nicht gegenseitig behindern, wenn sie schließlich im ERP-System ankommen. Soft-Reservierungen stellen außerdem sicher, dass Sie alle versprochenen Bestellungen erfüllen können. Sie helfen Ihnen also, die Erwartungen Ihrer Kunden zu erfüllen und sie an sich zu binden. Weitere Informationen finden Sie unter [Reservierungen in Inventory Visibility](inventory-visibility-reservations.md).

### <a name="immediate-response-of-atp-quantity-and-dates"></a>Sofortige Rückmeldung der ATP-Menge und Daten

Die Einsicht in Ihren für die nahe Zukunft prognostizierten Bestand (einschließlich Angaben zu Vorrat, Bedarf und prognostiziertem Lagerbestand) ist wichtig, denn sie hilft Ihrer Firma, die folgenden Ziele zu erreichen:

- Minimieren Sie die Bestände, um die Kosten für die Lagerverwaltung zu senken.
- Erleichtern Sie die interne Verarbeitung von Bestellungen, damit Verkäufer Versand- und Liefertermine auf der Grundlage der Verfügbarkeit der bestellten Produkte berechnen können.
- Bieten Sie Transparenz darüber, wann Kunden erwarten können, dass ein vergriffenes Element wieder verfügbar ist, indem Sie das Datum der nächsten Verfügbarkeit angeben.

Die ATP Funktion lässt sich leicht in Ihren täglichen Auftragsabwicklungsprozess adaptieren. Am wichtigsten ist, dass die ATP Funktion wie andere Inventory Visibility Angebote *global und in Echtzeit* ist. Daher können Sie mehrere ATP-Berechnungsformeln festlegen, um vollständige Abfragen zur Bestandsverfügbarkeit zu erhalten, die alle Ihre Geschäftskanäle und Datenquellen abdecken. Weitere Informationen finden Sie unter [Inventory Visibility Lagerbestand Änderungspläne und verfügbar zu versprechen](inventory-visibility-available-to-promise.md).

### <a name="preallocate-your-stock-to-important-channels-or-customers-with-inventory-allocation"></a>Ordnen Sie Ihren Bestand mit Bestandszuteilung wichtigen Kanälen oder Kunden vor

Mit der Bestandsanzeige-Zuordnungsfunktion können Sie Ihren wertvollen Lagerbestand für wichtige Kanäle, Kundengruppen oder Standorte schützen und abgrenzen. Nachdem der Bestand zugeteilt wurde, wird der Bestandsverbrauch auf den zugeteilten Pool beschränkt, und die im Pool verbleibenden Mengen werden nahezu in Echtzeit abgezogen, um die Menge widerzuspiegeln, die noch für den Verbrauch verfügbar ist. Weitere Informationen finden Sie unter [Bestandszuordnung für Bestandsichtbarkeit](inventory-visibility-allocation.md)

### <a name="compatibility-with-wms-items"></a>Kompatibilität mit WMS-Artikeln

Microsoft strebt eine standardmäßige Integration mit den Prozessen der Lagerverwaltung (WMS) an, sodass auch WMS-Kunden von den Vorteilen des Dienstes Inventory Visibility profitieren können. In der Version 2022 Wave 1 (öffentliche Vorschau im März) unterstützt der Bestandsservice WMS-Abfragen zum Lagerbestand und ATP. Die Funktion der weichen Reservierung und Zuweisung wird für WMS-Kunden in der nächsten Welle unterstützt. Weitere Informationen finden Sie unter [Inventory Visibility-Unterstützung für WMS-Artikel](inventory-visibility-whs-support.md).

Die folgende Abbildung zeigt eine allgemeine Zusammenfassung vorhandener Funktionen und wie sie im Datenfluss positioniert werden können.

[<img src="media/inventory-visibility-feature-overview.png" alt="Inventory Visibility feature overview." title="Übersicht über die Bestandsanzeige-Funktion" width="720" />](media/inventory-visibility-feature-overview.png)

## <a name="licensing"></a>Lizenzierung

Der Inventory Visibility Service ist in den folgenden Versionen verfügbar:

- **Inventory Visibility-Add-In für Microsoft Dynamics 365 Supply Chain Management** - Für Unternehmen, die über eine gültige Supply Chain Management-Lizenz verfügen, ist Inventory Visibility ohne zusätzliche Kosten verfügbar. Denn Bestandsanzeige basiert auf Microsoft Power Platform, es unterliegt Microsoft Power Platform Speicherkapazität und API-Limits. Ihre Supply Chain Management-Lizenz sollte Standardspeicher- und API-Kapazität beinhalten. Wenn Sie mehr Speicher- und API-Kapazität benötigen, können Sie eine Professional-Lizenz erwerben. Einzelheiten zur standardmäßigen API-Zuweisung und zur Professional-Lizenz finden Sie unter [Limits und Zuweisungen anfordern](/power-platform/admin/api-request-limits-allocations) und [Lizenzübersicht für Microsoft Power Platform](/power-platform/admin/pricing-billing-skus). Mit den standardmäßigen Speicher- und API-Zuweisungen können Sie noch heute damit beginnen, das Bestandsanzeige-Add-In auszuprobieren. Einzelheiten zur Installation finden Sie unter [Installation und Festlegen von Inventory Visibility](inventory-visibility-setup.md). Wenn Ihre geschätzte API- und Speichernutzung die Standardzuweisung überschreitet, können Sie sich an Ihren Vertriebsmitarbeiter wenden und ihn bitten, sich wegen einer Ausnahme an das Plattformteam zu wenden.
- **Inventory Visibility Service als Bestandteil von IOM** - Diese Version ist entweder für Kunden von Intelligent Order Management (IOM) oder für Firmen, die Supply Chain Management nicht als ERP-System einsetzen. Die Lizenz ist im Intelligent Order Management Bundle enthalten. Weitere Informationen finden Sie unter [Intelligent Order Management Überblick](/dynamics365/intelligent-order-management/overview).

## <a name="inventory-visibility-terminology"></a>Bestandsanzeige-Terminologie

Es ist wichtig, dass Sie die folgenden Konzepte und Begriffe verstehen, wenn Sie mit der Bestandsanzeige-Add-In arbeiten:

- **Datenquelle** – Eine Datenquelle steht für das System, aus dem Ihre Daten stammen.
- **Abmessungen** – Abmessungen kennzeichnen Produkteigenschaften. Dies können Lagerabmessungen (z. B. Standort oder Lager) oder Produktabmessungen (z. B. Farbe, Größe oder Stil) sein.
- **Physikalische Messungen** – Physische Maße sind Mengen, die verschiedene Bestandsstatus messen, z. B. verfügbar, gekauft, bestellt oder verkauft.
- **Berechnete Maße** – Berechnete Maße sind quantitative Maße, die aus einer Menge physikalischer Maße berechnet werden. Zum Beispiel die *Insgesamt verfügbar* berechnetes Maß wird berechnet als *Verfügbar* + *Gekauft* – *Auf Bestellung* – *Verkauft*.
- **Partition** – Eine Partition definiert eine Hierarchie, wie die Bestandsanzeige empfangene Daten verteilt. Derzeit ist die Standardpartition Standort und Lagerort.
- **Indexhierarchie** – Eine Indexhierarchie definiert weiter, wie Sie das Inventar abfragen und Ergebnisse mit größerer Granularität erhalten möchten.

Weitere Informationen zu diesen Bedingungen und Konzepten finden Sie unter [Bestandsanzeige konfigurieren](inventory-visibility-configuration.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
