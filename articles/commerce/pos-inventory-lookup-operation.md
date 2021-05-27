---
title: Bestandssuchvorgänge in POS
description: In diesem Thema wird beschrieben, wie Sie den Bestandssuchvorgang in Dynamics 365 Commerce Point of Sale (POS) verwenden, um die Verfügbarkeit von Produkten in den Filialen und Lagerorten anzuzeigen.
author: boycezhu
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2018-03-30
ms.dyn365.ops.version: Application update 5, AX 8.0
ms.openlocfilehash: 873c6413c14d2ee8315c149ee9c495bb59dbd930
ms.sourcegitcommit: 11ca5863175150b6c39f47a9322caa2186727a26
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6025447"
---
# <a name="inventory-lookup-operation-in-pos"></a>Bestandssuchvorgänge in POS

[!include [banner](includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie den Bestandssuchvorgang in Dynamics 365 Commerce Point of Sale (POS) verwenden, um die Verfügbarkeit von Produkten in den Filialen und Lagerorten anzuzeigen.

Mithilfe einer genauen Bestandsanzeige in einer gesamten Organisation können Filialmitarbeiter einen rechtzeitigen, effektiven Kundenservice bieten. Am wichtigsten ist der Augenblick, an dem ein Debitor bereit ist, eine Kaufentscheidung zu treffen. Es ist wichtig, dass Kassierer in einem Einzelhandelsgeschäft Bestandsinformationen in Echtzeit oder Quasi-Echtzeit zur Hand haben, sodass sie eine Produktlieferung und -abholung genau zusagen können.

Der Bestandssuchvorgang in Commerce POS hilft Einzelhändlern dabei, operative Exzellenz zu erzielen und Erkenntnisse zu gewinnen, indem Filialen mit der Commerce-Zentralverwaltung verbunden werden. Diese Funktion bietet eine Ansicht der Verfügbarkeit von Produkten in Filialen und Lagerorten. Einzelhändler werden zudem darin unterstützt, zusätzliche Effektivität und Kosteneinsparungen zu erreichen, indem sie die Bestandsplanung in Echtzeit verbessern.

Wenn der Bestandssuchvorgang über die POS-Anwendung gestartet wird, gibt der POS-Kassierer über die Zifferntastatur eine Produktnummer ein, um seine Bestandsinformationen abzufragen. Wenn das eingegebene Produkt Varianten hat, kann der Kassierer optional Abmessungen oder andere Werte auswählen, um die Bestandsinformationen einer bestimmten Produktvariante zu überprüfen.

## <a name="inventory-lookup-list-view-for-individual-products"></a>Listenansicht der Bestandssuche für einzelne Produkte

Für ein einzelnes Produkt bietet der Bestandssuchvorgang eine Listenansicht für die Bestandssuche mit den folgenden Produktinformationen für eine Liste der Standorte:

- **Bestand**: Bezieht sich auf die „verfügbare physische“ Menge eines Produkts.
- **Reserviert**: Bezieht sich auf die „physisch reservierte“ Menge, die von der Zentralverwaltung abgerufen wurde.
- **Bestellt**: Bezieht sich auf die „insgesamt bestellte“ Menge, die von der Zentralverwaltung abgerufen wurde.
- **Einheit**: Bezieht sich auf die in der Zentralverwaltung konfigurierte Maßeinheit des Bestands.

Die Listenansicht der Standorte enthält alle Filialen und Lagerorte, die in den Erfüllungsgruppen konfiguriert sind, mit denen die aktuelle Filiale verknüpft ist, wie im folgenden Beispielbild dargestellt.

![Listenansicht Bestandssuchvorgänge](media/inventory-lookup-list-view.png)

Die folgenden Aktionen sind in der Leiste der POS-App verfügbar:

- **Sortieren**: Mit dieser Aktion kann der POS-Benutzer die Daten in der Listenansicht nach verschiedenen Kriterien sortieren. Standardmäßig ist die Sortierung nach Standort eingestellt. 
  - **Geografischer Standort** (vom nächstgelegenen zum am weitesten entfernten Standort im Vergleich zur aktuellen Filiale)
  - **Name** (in aufsteigender oder absteigender Reihenfolge)
  - **Filialnummer** (in aufsteigender oder absteigender Reihenfolge)
  - **Bestand** (in absteigender Reihenfolge)
  - **Reserviert** (in absteigender Reihenfolge)
  - **Bestellt** (in absteigender Reihenfolge)
- **Filter**: Mit dieser Aktion kann der POS-Benutzer gefilterte Daten für einen bestimmten Standort anzeigen.
- **Verfügbarkeit in Filiale anzeigen**: Mit dieser Aktion kann der POS-Benutzer die für eine Zusage verfügbaren Mengen (ATP-Mengen) für ein Produkt in der ausgewählten Filiale anzeigen.
- **Filialstandort anzeigen**: Diese Aktion öffnet eine separate Seite mit der Kartenansicht, der Adresse und den Öffnungszeiten der ausgewählten Filiale.
- **Abholung im Shop**: Diese Aktion erstellt einen Debitorenauftrag für das Produkt, das von der ausgewählten Filiale abgeholt wird, und leitet den Benutzer zum Transaktionsbildschirm weiter.
- **Produkt versenden**: Diese Aktion erstellt einen Debitorenauftrag für das Produkt, das von der ausgewählten Filiale versandt wird, und leitet den Benutzer zum Transaktionsbildschirm weiter.
- **Alle Varianten anzeigen**: Bei einem Produkt mit Varianten wechselt diese Aktion von einer Listenansicht zu einer Matrixansicht, in der Bestandsinformationen für alle Produktvarianten angezeigt werden.
- **Zur Transaktion hinzufügen**: Diese Aktion fügt das Produkt dem Warenkorb hinzu und leitet den Benutzer zum Transaktionsbildschirm weiter.

> [!NOTE]
> Bei einer Sortierung nach Standort wird die Entfernung zwischen einem Standort und der aktuellen Filiale durch die Koordinaten (Breiten- und Längengrad) bestimmt, die in der Commerce-Zentralverwaltung festgelegt sind. Für eine Filiale werden die Standortinformationen in der primären Adresse der der Filiale zugeordneten Organisationseinheit festgelegt. Bei einem Lagerort, bei dem es sich nicht um eine Filiale handelt, werden die Standortinformationen in der Lagerortadresse festgelegt. Wenn für die aktuelle Filiale keine korrekten Koordinaten festgelegt sind, zeigt die Sortieroption nach Standort die aktuelle Filiale oben in der Liste an und sortiert dann andere Standorte nach Namen.

> [!NOTE]
> Die Aktionen **Verfügbarkeit in Filiale anzeigen**, **Filialstandort anzeigen**, **Abholung im Shop** und **Produkt versenden** sind für Standorte, bei denen es sich nicht um eine Filiale handelt, nicht verfügbar.

## <a name="inventory-lookup-matrix-view-for-variants"></a>Matrixansicht der Bestandssuche für Varianten

Für ein Masterprodukt mit Varianten bietet der Bestandssuchvorgang auch eine Matrixansicht auf Basis der Abmessungen, in der Informationen zur Bestandsverfügbarkeit für alle Varianten des Masterprodukts an einem ausgewählten Standort angezeigt werden. Standardmäßig zeigt die Matrixansicht Daten für die aktuelle Filiale an. Sie können die Aktion **Filiale** in der App-Leiste nutzen, um Bestandsinformationen für andere Filialen abzurufen, die in den Erfüllungsgruppen konfiguriert sind, mit denen die aktuelle Filiale verknüpft ist.

Das folgende Beispielbild zeigt die Matrixansicht der Bestandssuche in POS.

![Matrixansicht Bestandssuchvorgänge](media/inventory-lookup-matrix-view.png)

In der Matrixansicht stellt jede Zelle eine einzelne Variante dar und zeigt einen verfügbaren Bestand (physisch verfügbar) in der unteren rechten Ecke sowie Werte für **reserviert** (physisch reserviert) und **bestellt** (insgesamt bestellt) in der oberen linken Ecke an. In der folgenden Tabelle wird die Bedeutung der verschiedenen Werte für verfügbare Bestände erklärt.

| Verfügbarer Wert                            | Beschreibung |
|------------------------------------------|-------------|
| Numerischer Wert der größer als 0 (null) ist | Eine Variante ist für den ausgewählten Lagerplatz freigegeben worden, und Sie können zusätzliche Aktivitäten in der Zelle ausführen. |
| **0** (null)                             | Eine Variante ist für den ausgewählten Lagerplatz freigegeben worden, aber der Artikel ist am ausgewählten Standort nicht verfügbar. Sie können zusätzliche Aktionen in der Zelle ausführen. |
| **n/v** oder eine inaktive Zelle              | Eine Variante ist für den ausgewählten Lagerplatz nicht freigegeben worden, und Sie können keine zusätzlichen Aktivitäten in der Zelle ausführen. |

Die Anzeigereihenfolge der Abmessungswerte in der Matrixansicht basiert auf der Konfiguration für die Reihenfolge der Abmessungsanzeige in der Commerce-Zentralverwaltung. Sie können die Konfiguration für die Reihenfolge der Abmessungsanzeige ändern, indem Sie eine neue zu verwendende Abmessung auswählen. 

Die folgenden Aktionen sind in der Zelle Matrixansicht verfügbar:

- **Jetzt verkaufen**: Diese Aktion fügt die ausgewählte Variante dem Warenkorb hinzu und leitet den Benutzer zum Transaktionsbildschirm weiter.
- **Abholung im Shop**: Diese Aktion erstellt einen Debitorenauftrag für die ausgewählte Variante, das von der ausgewählten Filiale abgeholt wird, und leitet den Benutzer zum Transaktionsbildschirm weiter.
- **Produkt versenden**: Diese Aktion erstellt einen Debitorenauftrag für die ausgewählte Variante, das von der ausgewählten Filiale versandt wird, und leitet den Benutzer zum Transaktionsbildschirm weiter.
- **Verfügbarkeit**: Diese Aktion leitet den Benutzer zu einer separaten Seite weiter, auf der die ATP-Mengen für die ausgewählte Variante in der ausgewählten Filiale angezeigt werden.
- **Alle Standorte anzeigen**: Diese Aktion wechselt zur Standardansicht der Bestandsverfügbarkeitsliste, in der die Bestandsinformationen für die ausgewählte Variante angezeigt werden.
- **Produktdetails anzeigen**: Diese Aktion leitet den Benutzer zur Produktdetailseite (PDP) der ausgewählten Variante weiter.

## <a name="access-inventory-lookup-from-other-pages-in-pos"></a>Von anderen Seiten im POS auf die Bestandssuche zugreifen

POS-Benutzer können von anderen Seiten im POS auf die Bestandssuche zugreifen.

Das folgende Beispielbild zeigt die Ergebnisse der Bestandssuche von einer PDP in POS.

![Bestandssuche von der Produktdetailseite aus](media/inventory-lookup-from-product-details-page.png)

Auf der PDP eines Masterprodukts können Sie die Aktion **Alle Varianten anzeigen** in der App-Leiste verwenden, um die Matrixansicht der Bestandssuche zu starten, in der Informationen zur Verfügbarkeit aller Varianten eines Produkts in der aktuellen Filiale angezeigt werden. Bei einem einzelnen Produkt zeigt die PDP den verfügbaren Bestand (physisch verfügbar) dieses Produkts für die aktuelle Filiale an. Zusätzlich können Sie den Link **Bestand in anderen Filialen** zum Starten der Bestandssuche auswählen, um die Verfügbarkeit eines Produkts in anderen Filialen oder Lagerorten zu überprüfen.

> [!NOTE]
> Die Schaltfläche **Alle Varianten anzeigen** auf der PDP ist nur für Masterprodukte verfügbar, die Produktvarianten haben. Sie ist nicht für spezifische Produkte oder Sets verfügbar.

Sie können die Bestandssuche so konfigurieren, dass sie als Link im Schaltflächenraster des POS-Transaktionsbildschirms angezeigt wird. Wenn der Benutzer nach der Konfiguration eine Warenkorbposition und dann die **Bestandssuche** auswählt, wird die Listenansicht der Bestandssuche für das ausgewählte Produkt angezeigt. Weitere Informationen zum Konfigurieren von Schaltflächenrastern mit dem Designertool für das POS-Bildschirmlayout finden Sie unter [Visuelle Konfigurationen der POS-Benutzeroberfläche](pos-screen-layouts.md).

## <a name="inventory-lookup-with-channel-side-calculation"></a>Bestandssuche mit kanalseitiger Berechnung

In der Commerce-Version 10.0.9 und früheren Versionen wird der Wert **physisch verfügbar** in der Bestandssuche über einen Echtzeit-Serviceaufruf von der Commerce-Zentralverwaltung abgerufen. Ab Commerce-Version 10.0.10 können Sie den POS-Bestandssuchvorgang so konfigurieren, dass die kanalseitige Berechnung auf dem Commerce-Server verwendet wird, um den verfügbaren physischen Wert zu ermitteln, wodurch eine zuverlässigere und genauere Schätzung des verfügbaren Bestands bereitgestellt werden kann, indem noch nicht mit der Zentralverwaltung synchronisierte Transaktionsdaten berücksichtigt werden. Weitere Informationen zur kanalseitigen Bestandsberechnung und der zugehörigen POS-Konfiguration in der Zentralverwaltung finden Sie unter [Lagerverfügbarkeit für Retail Channels berechnen](calculated-inventory-retail-channels.md).

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Visuelle Konfigurationen der POS-Benutzeroberfläche](pos-screen-layouts.md)

[Lagerverfügbarkeit für Retail Channels berechnen](calculated-inventory-retail-channels.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
