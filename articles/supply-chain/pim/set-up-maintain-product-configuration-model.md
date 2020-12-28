---
title: Einrichten eines Produktkonfigurationsmodells
description: Dieser Artikel beschreibt die Schritte zum Einrichten und Erstellen eines Produktkonfigurationsmodells.
author: cvocph
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PCProductConfigurationModelListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 4051
ms.assetid: 00df5537-b148-4e32-a248-3e35876ad4e1
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7af9aaa01d89da909f2b30089c17d67d377d9e78
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428805"
---
# <a name="set-up-a-product-configuration-model"></a>Einrichten eines Produktkonfigurationsmodells

[!include [banner](../includes/banner.md)]

Dieser Artikel beschreibt die Schritte zum Einrichten und Erstellen eines Produktkonfigurationsmodells.

| Aufgabe                                                        | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Erstellen Sie einen Produktmaster.                                    | Erstellen Sie einen Produktmaster aus der Liste **Produktmaster**. Geben Sie den Produktmaster den entsprechenden Unternehmen frei. Für einen Produktmaster, der als Version für ein Produktkonfigurationsmodell oder als Unterkomponente verwendet wird, muss **Einschränkungsbasierte Konfiguration** ausgewählt werden, und die Konfigurationsdimension darf nur für die Produktdimensionsgruppe ausgewählt werden. |
| Erstellen Sie Komponenten.                                          | Erstellen Sie Komponenten auf der Seite **Komponenten**. Komponenten sind die Bausteine eines Produktkonfigurationsmodells und können in mehreren Produktkonfigurationsmodellen wiederverwendet werden.                                                                                                                                                                                                                      |
| Erstellen Sie Attributtypen.                                     | Erstellen Sie Attributtypen auf der Seite **Attributtypen**. Attributtypen geben den Satz von Datentypen für alle Attribute an, die in Produktkonfigurationsmodellen verwendet werden. Attribute von **Boolesch**, **Text** mit einer festen Liste und **Ganzzahl** mit Bereichstypen führen den Satz von Werten auf, die verfügbar sind, wenn Sie eine Produktvariante, basierend auf einem Produktkonfigurationsmodell, konfigurieren.       |
| Erstellen Sie ein Produktkonfigurationsmodell.                       | Erstellen Sie ein Produktkonfigurationsmodell auf der Seite **Neues Produktkonfigurationsmodell**.                                                                                                                                                                                                                                                                                                              |
| Fügen Sie Attribute zu einem Produktkonfigurationsmodell hinzu.            | Erstellen Sie ein Attribut auf dem Inforegister **Attributes** auf der Seite **Details zum einschränkungsbasierten Produktkonfigurationsmodell**. Attribute beschreiben die Funktionen des Produktkonfigurationsmodells.                                                                                                                                                                                                       |
| Fügen Sie Einschränkungen zu einem Produktkonfigurationsmodell hinzu.           | Erstellen Sie Einschränkungen auf dem Inforegister **Einschränkungen** auf der Seite **Details zum einschränkungsbasierten Produktkonfigurationsmodell**. Einschränkungen sind Begrenzungen, die ein Produktkonfigurationsmodell erfüllen muss. Einschränkungen sind entweder Ausdruckseinschränkungen oder Tabelleneinschränkungen.                                                                                                                                 |
| Fügen Sie einem Produktkonfigurationsmodell Unterkomponenten hinzu.         | Erstellen Sie Unterkomponenten auf dem Inforegister **Unterkomponenten** auf der Seite **Details zum einschränkungsbasierten Produktkonfigurationsmodell**. Unterkomponenten sind Komponenten zugeordnet und sie werden mit Artikeln verknüpft, die die Unterkomponente darstellen.                                                                                                                                                                       |
| Fügen Sie Benutzeranforderungen zu einem Produktkonfigurationsmodell hinzu.     | Benutzeranforderungen ähneln Unterkomponenten, aber sie verweisen nicht auf einen Artikel. Sie können sich Benutzeranforderungen als Phantomstücklisten vorstellen. Alle Stücklistenpositionen oder Arbeitsplan-Arbeitsgänge, die direkt unter die Benutzeranforderung platziert werden, werden in die übergeordnete Komponente reduziert.                                                                                                                       |
| Fügen Sie Stücklistenpositionen zu einem Produktkonfigurationsmodell hinzu.             | Erstellen Sie Stücklistenpositionen auf dem Inforegister **Stücklistenpositionen** auf der Seite **Details zum einschränkungsbasierten Produktkonfigurationsmodell**. Stücklistenpositionen stellen einen Teil dar, der erforderlich ist, um eine Variante des Produkts zu erstellen.                                                                                                                                                                                                 |
| Fügen Sie Arbeitsplan-Arbeitsgängen zu einem Produktkonfigurationsmodell hinzu.      | Erstellen Sie Arbeitsplan-Arbeitsgänge auf dem Inforegister **Arbeitsplan-Arbeitsgänge** auf der Seite **Details zum einschränkungsbasierten Produktkonfigurationsmodell**. Arbeitsplan-Arbeitsgänge stellen einen Schritt in einer Reihenfolge von Schritten dar, die ausgeführt werden, um eine Variante des Produkts zu erstellen.                                                                                                                                                    |
| Erstellen Sie eine aktiven Version für ein Produktkonfigurationsmodell. | Erstellen Sie eine aktive Version des Produktkonfigurationsmodells auf der Seite **Versionen**. Eine Version ist die Beziehung zwischen einem Produktkonfigurationsmodell und einem Produktmaster. Ein Produktkonfigurationsmodell, das eine aktive Version aufweist, kann aus einem Auftrag, einem Verkaufsangebot, einer Bestellung oder einem Produktionsauftrag heraus konfiguriert werden.                                                               |
| Testen Sie ein Produktkonfigurationsmodell.                         | Testen Sie das Produktkonfigurationsmodell, entweder von der Seite **Details zum einschränkungsbasierten Produktkonfigurationsmodell** oder der Seite **Liste der Produktkonfigurationsmodelle** aus. Beim Testen der Produktkonfigurationsmodelle wird der Produktmodellkonfigurationsprozess simuliert, der während der Auftragsbehandlung abläuft.                                                                                                |
| Erstellen Sie ein Produktkonfigurationsmodell-Vorlage.                | Erstellen Sie eine Produktkonfigurationsmodell-Vorlage auf der Seite **Konfigurationsvorlage**. Eine Konfigurationsvorlage enthält Werte für Attribute im Produktkonfigurationsmodell. Wählen Sie die Attributwerte auf der Seite **Position konfigurieren** aus. Sie können auswählen, eine Produktmodell-Konfigurationsvorlage während der Produktmodellkonfiguration zu laden.                                                   |
| Konfigurieren Sie einen Artikel.                                          | Produktkonfigurationsmodelle können aus einem Auftrag, einem Verkaufsangebot, einer Bestellung oder einem Produktionsauftrag heraus konfiguriert werden.                                                                                                                                                                                                                                                                           |





