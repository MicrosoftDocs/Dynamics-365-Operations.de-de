---
title: Transportverwaltungsmodule
description: "Transportverwaltungsmodule definieren die Logik, die verwendet wird, um Transportsätze in der Transportverwaltung zu generieren und zu verarbeiten."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: TMSFreightBillType, TMSGenericEngine, TMSMileageEngine, TMSRateEngine, TMSTransitTimeEngine, TMSZoneEngine
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 12234
ms.assetid: b878478c-0e04-4a1e-a037-6fdbb345a9a3
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: c65f7e44459478cac7663575abe588ad057f18e0
ms.contentlocale: de-de
ms.lasthandoff: 04/25/2017


---

# <a name="transportation-management-engines"></a>Transportverwaltungsmodule

[!include[banner](../includes/banner.md)]


Transportverwaltungsmodule definieren die Logik, die verwendet wird, um Transportsätze in der Transportverwaltung zu generieren und zu verarbeiten. 

Ein Transportverwaltungsmodul berechnet Aufgaben wie z. B. den Transportsatz des Spediteurs. Mit dem Modulsystem können Sie Berechnungsstrategien zur Laufzeit ändern, basierend auf Daten in Microsoft Dynamics 365 for Operations. Ein Transportverwaltungsmodul ähnelt einem Plug-In, das einem bestimmten Spediteursvertrag zugeordnet ist.

## <a name="what-engines-are-available"></a>Welche Module sind verfügbar?
Die folgende Tabelle zeigt die Transportverwaltungsmodule, die in Microsoft Dynamics 365 for Operations verfügbar sind.

| Transportverwaltungsmodul | Beschreibung                                                                                                                                                                                                                                                                                                                 |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Satzmodul**                  | Berechnet Sätze.                                                                                                                                                                                                                                                                                                           |
| **Allgemeines Modul**               | Einfache Hilfsmodule, die von anderen Modulen verwendet werden, die keine Daten aus Microsoft Dynamics 365 for Operations benötigen, beispielsweise ein Umlagenmodul. Umlagenmodule werden verwendet, um die Endkosten des Transports für bestimmte Aufträge und Positionen zu reduzieren, basierend auf Dimensionen wie Volumen und Gewicht. |
| **Kilometerleistungsmodul**               | Berechnet die Transportentfernung.                                                                                                                                                                                                                                                                                     |
| **Transitzeitmodul**          | Berechnet die Zeit, die erforderlich ist, um vom Start- zum Zielort zu gelangen.                                                                                                                                                                                                                                       |
| **Zonenmodul**                  | Berechnet die Zone basierend auf der aktuellen Adresse und berechnet die Anzahl der Zonen, die durchquert werden müssen, um von Adresse A nach Adresse B zu gelangen.                                                                                                                                                                    |
| **Frachtbrieftyp**            | Standardisiert die Frachtrechnungs- und Frachtbriefpositionen und wird für den automatischen Frachtbriefabgleich verwendet.                                                                                                                                                                                                                |

 
<a name="what-engines-must-be-configured-to-rate-a-shipment"></a>Welche Module müssen konfiguriert werden, um eine Lieferung zu bewerten?
---------------------------------------------------

Um eine Lieferung mithilfe eines bestimmten Spediteurs zu bewerten, müssen Sie mehrere Transportverwaltungsmodule konfigurieren. Das **Tarifmodul** ist erforderlich, möglicherweise jedoch auch andere Transportverwaltungsmodule, um das **Tarifmodul** zu unterstützen. So kann das **Tarifmodul** beispielsweise verwendet werden, um Daten aus dem **Kilometerleistungsmodul** abzurufen und den Satz anhand der Kilometerleistung zwischen den Start und Ziel zu berechnen.

## <a name="whats-required-to-initialize-a-transportation-management-engine"></a>Was ist erforderlich, um ein Transportverwaltungsmodul zu initialisieren?
Ein Transportverwaltungsmodul erfordert, dass Sie Initialisierungsdaten einrichten, um auf eine bestimmte Art funktionieren zu können. Die Einrichtung kann die folgenden Datentypen umfassen:
-   Referenzen zu anderen Transportverwaltungsmodulen. Einzelheiten finden Sie im Konfigurationsbeispiel in diesem Abschnitt.
-   Referenzen zu .NET-Typen, die vom Transportverwaltungsmodul verwendet werden.
-   Einfache Konfigurationsdaten.

In den meisten Fällen können Sie auf die Schaltfläche **Parameter** in den Einrichtungsformularen des Transportverwaltungsmoduls klicken, um die Initialisierungsdaten zu konfigurieren. **Beispiel für die Konfiguration eines Tarifmoduls, das auf ein Kilometerleistungsmodul verweist** Im folgenden Beispiel werden die Einstellungen gezeigt, die für ein Tarifmodul erforderlich sind, das auf dem .NET-Modultyp Microsoft.Dynamics.Ax.Tms.Bll.MileageRateEngine basiert und auf ein Kilometerleistungsmodul verweist.
| Parameter             | Beschreibung                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *RateBaseAssigner*    | Der .NET-Typ, der die Satz-Basiszuweisungsdaten für ein bestimmtes Schema interpretiert. Die Syntax des Parameterwerts besteht aus zwei Segmenten, getrennt durch einen senkrechten Strich (|) generiert. Das erste Segment enthält den Assemblynamen, der den Typ „assigner“ definiert. Das zweite Segment definiert den vollqualifizierten Namen des Typs „assigner“. Dazu gehört der Namespace des Typs. |
| *MileageEngineCode*   | Code des Kilometerleistungsmoduls, der den Datensatz des Kilometerleistungsmoduls in der Microsoft Dynamics 365 for Operations Datenbank kennzeichnet.                                                                                                                                                                                                                                                             |
| *ApportionmentEngine* | Allgemeiner Modulcode, der das Umlagenmodul in der Microsoft Dynamics 365 for Operations Datenbank kennzeichnet.                                                                                                                                                                                                                                                              |

 
<a name="how-is-metadata-used-in-transportation-management-engines"></a>Wie werden Metadaten in den Transportverwaltungsmodulen verwendet?
----------------------------------------------------------

Transportverwaltungsmodule, die auf Daten beruhen, die in Dynamics 365 for Operations definiert sind, können verschiedene Datenschemas verwenden. Das Transportverwaltungssystem ermöglicht verschiedenen Transportverwaltungsmodulen die Verwendung der gleichen allgemeinen physischen Datenbanktabellen. Um sicherzustellen, dass die Laufzeitinterpretation der Moduldaten korrekt ist, können Sie Metadaten für die Datenbanktabellen definieren. Dies reduziert die Kosten für die Erstellung neuer Transportverwaltungsmodule, da in Operations keine zusätzlichen Tabellen und Formularstrukturen erforderlich sind.

## <a name="what-can-be-used-as-search-data-in-rate-calculations"></a>Welche Daten können als Suchdaten in den Satzberechnungen verwendet werden?
Die Daten, die Sie verwenden, wenn Sie Sätze in Microsoft Dynamics 365 for Operations berechnen, werden durch die Metadatenkonfiguration gesteuert. Wenn Sie beispielsweise nach Sätzen auf der Basis von Postleitzahlen suchen möchten, müssen Sie Metadaten basierend auf dem Nachschlagetyp einer Postleitzahl einrichten.

## <a name="do-all-engine-configurations-require-metadata"></a>Erfordern alle Modulkonfigurationen Metadaten?
Nein. Transportverwaltungsmodule, die verwendet werden, um die Daten abzurufen, die für die Satzberechnung aus externen Systemen erforderlich sind, benötigen keine Metadaten. Die Satzdaten für diese Module können aus externen Transportanbietersystemen abgerufen werden, in der Regel über einen Webdienst. So können Sie beispielsweise ein Kilometerleistungsmodul verwenden, das Daten direkt aus Bing Maps abruft, sodass Sie keine Metadaten für dieses Modul benötigen.
| **Hinweis**                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Die Transportverwaltungsmodule, die mit Microsoft Dynamics 365 for Operations bereitgestellt werden, nutzen Daten, die aus der Anwendung abgerufen werden. Module, die mit externen Systemen verbunden sind, sind nicht in Operations enthalten. Mit dem modulbasierten Erweiterungsmodell können Sie jedoch Erweiterungen mithilfe von Microsoft Dynamics 365 for Operations Visual Studio-Tools erstellen. |

## <a name="how-do-i-configure-metadata-for-a-transportation-management-engine"></a>Wie konfiguriere ich Metadaten für ein Transportverwaltungsmodul?
Metadaten für Transportverwaltungsmodule werden für die verschiedenen Arten von Modulen unterschiedlich konfiguriert.

| Transportverwaltungsmodul               | Metadatenkonfiguration                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Satzmodul**                                | Erfordert einen **Satzbasistyp**. Der Satzbasistyp enthält Metadaten für die Satzbasisdaten und die Satz-Basiszuweisungsdaten. Die Struktur von Satzbasismetadaten wird durch den Typ des Tarifmoduls bestimmt. Die Struktur der Satz-Basiszuweisungsmetadaten wird durch den Typ des Satzubasiszuweisers bestimmt, der diesem Tarifmodul zugeordnet ist. Sie richten den Satzbasistyp eines Tarifmoduls auf den Seiten **Tarifmodul** und **Satzmaster** ein. |
| **Zonenmodul**                                | Erfordert Metadaten, die direkt auf dem Zonenmaster eingerichtet werden.                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Transitzeitmodul** und **Kilometerleistungsmodul** | Ruft die Metadaten direkt aus dem Formular für die Konfigurationseinrichtung des Kilometerleistungsmoduls ab.                                                                                                                                                                                                                                                                                                                                                                                  |

  **Beispiel für Metadaten für ein Tarifmodul** Das Transportverwaltungsmodul erfordert die Kennung der Ursprungsadresse, des Zielstaats und des Ziellands/der Zielregion sowie des Ausgangs-und Endpunkts der Lieferung. Wenn Sie diese Anforderungen verwenden, würden die Metadaten wie die Daten in der folgenden Tabelle aussehen. Die Tabelle enthält auch Informationen zum Typ der Eingabedaten, der erforderlich ist.
-   Definieren Sie diese Informationen unter **Transportverwaltung** &gt; **Einstellungen** auf der Seite **Satzbasistyp**.

| Sequenz | Name                          | Feldtyp | Datentyp | Suchtyp    | Obligatorisch |
|----------|-------------------------------|------------|-----------|----------------|-----------|
| 1        | Ursprungspostleitzahl            | Zuweisung | Zeichenfolge    | Postleitzahl    | Ausgewählt  |
| 2        | Zielstaat             | Zuweisung | Zeichenfolge    | Staat          |           |
| 3        | Zielstartpostleitzahl | Zuweisung | Zeichenfolge    | Postleitzahl    | Ausgewählt  |
| 4        | Zielendepostleitzahl   | Zuweisung | Zeichenfolge    | Postleitzahl    | Ausgewählt  |
| 5        | Zielland           | Zuweisung | Zeichenfolge    | Land/Region |           |






