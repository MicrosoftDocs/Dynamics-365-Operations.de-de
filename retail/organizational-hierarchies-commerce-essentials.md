---
title: Arbeiten mit Organisationen und Organisationshierarchien (Grundlagen zum Handel)
description: "Handelsgrundlagen hat drei Typen interne Organisationen, die Sie definieren können, die eine Organisation zu unterstützen, einen Geschäftsprozess durchzuführen oder ein Ziel zu erreichen."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 21251
ms.assetid: 2bfc6bfe-784b-42e8-8bf0-116e9f0a558e
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6b1f91f863c8da35362ebb3036e76aa10d95ba65
ms.openlocfilehash: 50d29b6552cf7af5f2d9296b1d70b838a8edd637
ms.contentlocale: de-de
ms.lasthandoff: 04/26/2017


---

# <a name="organizations-and-organizational-hierarchies-commerce-essentials"></a>Arbeiten mit Organisationen und Organisationshierarchien (Grundlagen zum Handel)

[!include[banner](includes/banner.md)]


Handelsgrundlagen hat drei Typen interne Organisationen, die Sie definieren können, die eine Organisation zu unterstützen, einen Geschäftsprozess durchzuführen oder ein Ziel zu erreichen. 

Eine Organisation ist eine Gruppe von Personen, die zusammenarbeiten, um einen Geschäftsprozess durchzuführen oder ein Ziel zu erreichen. Eine Organisationshierarchie stellt die Beziehungen zwischen den Unternehmenseinheiten dar, aus denen Ihre Organisation besteht.

## <a name="organizations"></a>Organisation
In "Grundlagen zum Handel" können Sie drei Typen von internen Organisationen definieren: juristische Personen, Organisationseinheiten und Teams. In Microsoft Dynamics AX sind alle internen Organisationen Typen der Entität "Partei". Daher verwenden diese Organisationen ein Adressbuch, um Adressen und andere Kontaktinformationen zu speichern. Eine Partei kann entweder eine Person oder Organisation sein und sie kann mindestens einem Adressbuch zugeordnet sein.
### <a name="legal-entities"></a>Juristische Personen

Eine juristische Person ist eine Organisation mit einer registrierten oder eingetragenen Rechtsform. Juristische Personen können Verträge abschließen und sind verpflichtet, Finanzaufstellungen zum Erstellen eines Berichts über ihre Vermögens-, Finanz- und Ertragslage vorzubereiten. Ein Unternehmen ist ein Typ von juristischer Person in Microsoft Dynamics AX, und jede juristische Person ist einer Unternehmenskennung zugeordnet. Diese Zuordnung existiert, da eine Unternehmenskennung oder DataAreaId in manchen Datenmodellen verwendet wird, in denen Unternehmen als Grenze für die Datensicherheit verwendet werden. Benutzer können nur auf Daten für das Unternehmen zugreifen, bei dem sie derzeit angemeldet sind.

### <a name="operating-units"></a>Organisationseinheiten

Eine Organisationseinheit ist eine Organisation, die dazu dient, die Kontrolle über wirtschaftliche Ressourcen und Betriebsprozesse in einem Unternehmen aufzuteilen. Die Personen in einer Organisationseinheit sind verpflichtet, die Nutzung knapper Ressourcen zu maximieren, die Prozesse zu verbessern und Rechenschaft über ihre Leistung abzulegen. In "Grundlagen zum Handel" umfassen die Arten von Unternehmenseinheiten Kostenstellen, Unternehmenseinheiten, Wertströme, Abteilungen und Vertriebskanäle. Die folgende Tabelle enthält weitere Informationen zu jedem Organisationseinheitstyp.
|                         |                                                                                         |                                                                                                                                             |
|-------------------------|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| **Typ der Organisationseinheit** | **Beschreibung**                                                                         | **Verwendungszweck**                                                                                                                                 |
| Unternehmenseinheit           | Eine halbautomatische Organisationseinheit, die zum Erreichen strategischer Unternehmensziele erstellt wird. | Verwenden Sie Unternehmenseinheiten zur Finanzberichterstattung, die auf Branchen oder Produktlinien basiert, die die Organisation unabhängig von juristischen Personen bedient. |
| Retail Channel          | Eine Unternehmenseinheit, die einen physischen Laden darstellt.                             | Verwenden Sie diese, um eine oder mehrere Läden innerhalb oder über mehrere juristische Personen hinweg zu verwalten und zu steuern.                                                               |

## <a name="organizational-hierarchies"></a>Organisationshierarchien
In "Grundlagen zum Handel" wird jeder Hierarchie ein Zweck zugewiesen. Der Zweck der Hierarchie bestimmt die Organisationstypen, die der Hierarchie hinzugefügt werden können. Der Zweck definiert auch die Anwendungsszenarien, in denen die Hierarchie verwendet werden kann. Beispielsweise kann eine Einzelhandelshierarchie verwendet werden, um in einem auf Shop Lagermanagement Produkte zu kaufen und verkaufen zu. Organisationen in einer Hierarchie können Parameter, Richtlinien und Buchungen gemeinsam nutzen. Eine Organisation kann die Parameter der übergeordneten Organisation erben oder überschreiben. Gemeinsam genutzte Masterdaten, z. B. Produkte und Adressbücher, betreffen jedoch die gesamte Organisation und können für einzelne Organisationen nicht überschrieben werden.
### <a name="best-practices-for-setting-up-an-organization-in-a-hierarchy"></a>Optimale Verfahren zum Einrichten einer Organisation in einer Hierarchie

Berücksichtigen Sie die folgenden optimalen Verfahren bei der Implementierung einer Organisationshierarchie:
-   Erstellen Sie eine Abteilung, um die Schnittstelle zwischen einer juristischen Person und einer Unternehmenseinheit anzugeben. Anschließend lassen sich Daten von einer Abteilung zu einer juristischen Person für gesetzlich vorgeschriebene Berichte und von einer Abteilung zu einer Unternehmenseinheit für interne Berichte aufschlüsseln.
-   Legen Sie in einer einzelnen juristischen Person nicht mehrere Hierarchien für den gleichen Hierarchiezweck fest.
-   Erstellen Sie nicht für jeden Zweck eine Hierarchie. In der Regel können Sie eine Hierarchie für mehrere Zwecke verwenden. Beispielsweise kann eine Hierarchie mit Organisationseinheiten allen richtlinienbezogenen Zwecken zugewiesen werden.
-   Erstellen Sie ausgeglichene Hierarchien. In einer Hierarchie werden alle Knoten mit derselben Entfernung zum Stammknoten als Ebene definiert. In einer ausgeglichenen Hierarchie kann nur ein Organisationseinheitstyp pro Ebene vorhanden sein, und die Entfernung zum Stammknoten von jeder Ebene ist einheitlich. Sind Zwischenebenen zwischen einer Abteilung und einer juristischen Person bzw. einer Unternehmenseinheit vorhanden, sind u. U. Platzhalterorganisationen erforderlich, um eine ausgeglichene Hierarchie erstellen zu können.
-   Richten Sie keine separate Hierarchie von Organisationseinheiten ein, falls die Struktur für juristische Personen auch Ihrer Organisationsstruktur entspricht. Eine gemischte Hierarchie mit juristischen Personen und Organisationseinheiten kann beide Zwecke erfüllen.
-   Verwenden Sie vor dem Einrichten von umfassenden Neustrukturierungsszenarien die Gültigkeitsdaten der Hierarchie, um eine Auswirkungsanalyse und einen Validierungstest durchzuführen.
-   Speichern Sie eine Hierarchie als Entwurf, wenn Sie möglicherweise eine Hierarchie ändern, bevor Sie diese veröffentlichen.
-   Begrenzen Sie die Anzahl der Personen, die zum Hinzufügen oder Entfernen von Organisationen von einer Hierarchie in einer Produktionsumgebung berechtigt sind. Durch eine kleinere Anzahl verringert sich die Wahrscheinlichkeit für kostspielige Fehler und Korrekturen.

## <a name="retail-store-management"></a>Einzelhandelsshopleitung
In der folgenden Tabelle werden die Szenarien von "Grundlagen zum Handel" aufgeführt, in denen Organisationshierarchien verwendet werden können.
| Aufgabe                                                                           | Beschreibung                                                                                                                                                                                                                                                                                                | Hierarchiezweck    |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| Einzelhandelssortimente verwalten                                                      | Identifizieren Sie die Produkte, die in jedem Ladengeschäft verfügbar sind.                                                                                                                                                                                                                                             | Einzelhandelssortiment    |
| Einzelhandelsauffüllung verwalten                                                    | Gruppieren Sie Filialen, um Lagerbestand auf der Grundlage von Auffüllregeln wiederzubeschaffen.                                                                                                                                                                                                                                          | Einzelhandel-Auffüllung |
| Daten für Filialen berichten                                                         | Gruppieren Sie Shops für Berichterstellung.                                                                                                                                                                                                                                                                                | Berichterstellung im Einzelhandel     |
| Buchen von Bestand, Berechnen von Aufstellungen oder Buchen von Auszügen für eine Gruppe von Shops | Erstellen Sie eine Gruppe von Shops, die einem Stapelverarbeitungsauftrag zugewiesen werden können. Wenn Sie einen Batchauftrag zum Buchen von Lagerbestand, zum Berechnen von Aufstellungen oder zum Buchen von Auszügen festlegen, können Sie angeben, für welche Hierarchie der Auftrag gilt. Wenn Shops der Hierarchie hinzugefügt oder aus ihr entfernt werden, müssen Sie den Batchauftrag nicht ändern. | Retail POS-Buchung   |






