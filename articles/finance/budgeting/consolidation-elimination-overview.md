---
title: Konsolidierungs- und Löschungsüberblick
description: Dieser Artikel enthält allgemeine Informationen zum Konsolidierungs- und Beseitigungsprozess. Er enthält Antworten auf mehrere häufig gestellten Fragen.
author: aprilolson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerConsolidate
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13151
ms.assetid: 9d8f55cb-b2cf-4e01-89cf-0e21f5c8ae1f
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 566b1ecef3f9e540c651fe214accadcf32f4fbed
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772052"
---
# <a name="consolidation-and-elimination-overview"></a>Konsolidierungs- und Löschungsüberblick

[!include [banner](../includes/banner.md)]

Dieser Artikel enthält allgemeine Informationen zum Konsolidierungs- und Beseitigungsprozess. Er enthält Antworten auf mehrere häufig gestellten Fragen.

Wenn Sie Daten konsolidieren, werden die finanziellen Ergebnisse mehrerer Unternehmen vom Typ Tochtergesellschaft in Ergebnisse für nur ein konsolidiertes Unternehmen zusammengefasst. Tochtergesellschaften können ggf. auf verschiedenen Versionen oder Systemen laufen, sie sind ggf. kein vollständiges Eigentum und verwenden unterschiedliche Währungen. Es gibt mehrere Optionen für das Konsolidieren von Daten:

-   **Online konsolidieren** - Diese Option konsolidiert Tagessalden nach den ausgewählten Konten und Dimensionen und speichert sie in einem Konsolidierungsunternehmen.
-   **Finanzberichterstellung** - Diese Option ermöglicht die Konsolidierung von Transaktionen und Salden und kann jederzeit generiert werden. Mehrere Ebenen von Hierarchien können erstellt werden, und mehrere Berichtswährungen können angezeigt werden.
-   **Mit Import konsolidieren** - Diese Option importiert Salden in einem Konsolidierungsunternehmen.
-   **Unternehmenssalden exportieren** - Diese Option stellt eine Exportdatei von Unternehmenssalden bereit. Die Datei kann dann in andere Instanzen oder in Systeme importiert werden. Eine Finanzberichterstellung kann auch verwendet werden, um die Salden nach einer Microsoft Excel-Datei zu exportieren.

Löschungen können auf mehrere Arten gemeldet werden:

-   Löschungsregeln können im System eingerichtet und dann während des Konsolidierungsprozesses oder einen Löschungsvorschlag verarbeitet werden. Die Regeln können für ein beliebiges Unternehmen gebucht werden, das **Für finanziellen Löschungsprozess verwenden** in den Einstellungen für die juristische Person ausgewählt hat.
-   Ein separates Unternehmen kann erstellt und verwendet werden, um Löschtransaktionen manuell zu bestimmen und zu buchen. Dieses Unternehmen kann im Konsolidierungsprozess oder in der Finanzberichterstellung verwendet werden.
-   Die Konten und Finanzdimensionen, die verwendet werden, um Intercompany-Aktivität zu bestimmen, können auf einer Zeilendefinition oder einer Spaltendefinition in der Finanzberichterstellung gefiltert werden und vollständige Drilldownfunktion können verwendet werden. Eine berechnete Spalte oder Zeile kann dann verwendet werden, um die Konten und Finanzdimensionen aus der konsolidierten Summe zu entfernen.

Es gibt viele Konsolidierungsszenarien, und mit jeder Methode können die Szenarien auf verschiedene Weise behandelt werden.

## <a name="frequently-asked-questions"></a>Häufig gestellte Fragen
1.  Ich ziehe es vor, Löschungen in einer Datenbank zu buchen. Welcher Optionen habe ich?

Sie haben mehrere Optionen. Sie können die Option **Online konsolidieren** verwenden und Löschungen während des Prozesses oder als Vorschlag einschließen. Die Transaktionen werden im Konsolidierungsunternehmen gebucht. Alternativ können Sie über ein gesondertes Unternehmen verfügen, in dem Sie die Löschungen manuell erstellen und das sie dann in der Finanzberichterstellung oder im Konsolidierungsprozess verwenden.

2.  Wir benötigen unsere konsolidierten Ergebnisse in mehreren Berichtswährungen.

Die Option **Finanzberichterstellung** hat unbegrenzte Berichtswährungen. Die Daten werden während der Berichterstellung basierend auf dem Wechselkurstyp sowie der Umrechnungsmethode übersetzt, die im Hauptkonto festgelegt werden. Da die Option **Online konsolidieren** allerdings nur über eine Berichtswährung verfügt, muss für jede Berichtswährung ein konsolidiertes Unternehmen erforderlich, wenn Sie diese Option verwenden. Die Option **Finanzberichterstellung** ist die empfohlene Methode.

3.  Ich möchte für jedes Unternehmen Details auf Transaktionsebene sehen.

Die Option **Finanzberichterstellung** ist die Lösung, da Detail auf Transaktionsebene für so viele Unternehmen angezeigt werden kann, wie in der Berichtsbaumstruktur-Definition enthalten sind.

4.  Wir verwenden Budgetplanung oder Budgetsteuerung, und sie muss konsolidiert werden.
Die Option **Finanzberichterstellung** ist die Lösung, um alle Budgetplanungs- oder Budgetsteuerungsdaten zu konsolidieren.

5.  Wir haben Tochtergesellschaften weltweit, und wir haben mehrere Kontenpläne. Was ist die beste Methode für das Konsolidieren unserer Daten?

Sie haben mehrere Optionen, wenn Sie mehrere Kontenpläne behandeln müssen. Sie können die Option **Online konsolidieren** verwenden, und dann auswählen, entweder das Konsolidierungskonto zu verwenden, das im Hauptkonto definiert ist, oder einer Konsolidierungskontengruppe. Sie können auch die Option **Finanzberichterstellung** verwenden, mehrere Links zu den Finanzdimensionen in der Zeilendefinition einbeziehen und die Konten zuordnen.

6.  Wir benötigen mehrere Konsolidierungsebenen. Das bedeutet, wir konsolidieren zunächst unsere europäischen Tochtergesellschaften in das britischen Pfund (GBP). Dann übersetzen wir den konsolidierten Betrag dieser Daten in US-Dollar. Wie erreichen wir das?

Wenn mehrere Konsolidierungsebenen erforderlich sind und verschiedene Währungen in jeder Ebene verwendet werden, müssen Sie die Option **Online konsolidieren** verwenden. Mehrere Konsolidierungsunternehmen müssen erstellt werden, die sich in ihren Buchhaltungs- und Berichtswährungen unterscheiden. Die Konsolidierung muss dann mehrmals ausgeführt werden. Die Option **Finanzberichterstellung** übersetzt immer aus der Buchhaltungswährung jedes Quellunternehmens in die ausgewählte Währung.

7.  Es haben Tochtergesellschaften mit einem anderen System. Wie können wir sie konsolidieren?

Verwenden Sie die Option **Mit Import konsolidieren**, um Salden in ein Konsolidierungsunternehmen zu bringen.

8.  Einige unserer Tochtergesellschaften sind kein vollständiges Eigentum. Was ist die beste Methode, um sie zu konsolidieren?

Sie haben mehrere Optionen für Tochtergesellschaften mit teilweisem Eigentum. Wenn Sie die Option **Finanzberichterstellung** verwenden, können Sie eine Berichtsbaumstruktur-Definition und den Besitz definieren. Sie können auch eine berechnete Zeile oder Spalte verwenden, um den teilweise besessenen Betrag darzustellen. Sie können die Minderheitsbeteiligung auch als eigene Zeile in einem Bericht anzeigen. Sie können auch die **Online konsolidieren** Option verwenden. Die **Juristische Personen**-Registerkarte enthält eine **Besitz**-Spalte, in der Sie den Prozentsatz definieren können, der dem übergeordneten Unternehmen angehört.

9.  Unsere Organisation muss Konsolidierungen nach Unternehmenseinheit anzeigen oder möchte die Organisationshierarchien verwenden.

Die Option **Finanzberichterstellung** ist die Lösung. Organisationshierarchien mit juristischen Personen oder Finanzdimensionen können in der Finanzberichterstellung gemeldet werden. Sie können auch eigene mehrstufige Hierarchien erstellen, indem Sie eine Berichtsbaumstruktur-Definition verwenden, die eine Kombination von juristischen Personen und Dimensionswerten aufweist.

10. Wir haben mehrere Instanzen des Systems.

Wenn Sie die Option **Unternehmenssalden exportieren** verwenden, um von einer Instanz zu exportieren, und anschließend die Option **Mit Import konsolidieren** auf der anderen Instanz verwenden, können Sie die Daten konsolidieren.


Weitere Informationen finden Sie unter [Neubewertung der Währung in einem Konsolidierungsunternehmen](../general-ledger/currency-revaluation-consolidation-company.md).


