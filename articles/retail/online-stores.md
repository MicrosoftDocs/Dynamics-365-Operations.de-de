---
title: "Ohlineshop, Überblick"
description: "Dieser Artikel enthält Informationen zu Onlineshops und wie man sie in Microsoft Dynamics 365 for Retail einrichtet."
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailChannelManagementWorkspace, RetailOnlineStoreList
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16161
ms.assetid: 646d560c-f856-4701-b4ca-44e357ef09b8
ms.search.region: Global
ms.search.industry: Retail
ms.author: meeram
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 3814e5a4a88f439c89981f191e8896afb2ced68b
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="online-store-overview"></a>Onlineshop – Überblick

[!INCLUDE [banner](includes/banner.md)]

Dieser Artikel enthält Informationen zu Onlineshops und wie man sie in Microsoft Dynamics 365 for Retail einrichtet.

Dynamics 365 for Retail unterstützt mehrere Vertriebskanäle. Diese Vertriebskanäle umfassen Onlineshops, Callcenter und Einzelhandelsgeschäfte (auch physische Läden genannt). Onlineshops stellen für ein Einzelhandelsgeschäft eine Onlinepräsenz bereit, damit die Debitoren der Filiale Produkte aus dem Onlineshop des Einzelhändlers sowie aus dessen physischen Shops erwerben können. Wenn Debitoren Produkte des Onlineshops kaufen, können die Produkte entweder zugesendet oder vom Debitoren in einer lokalen Filiale abgeholt werden. Erstellen Sie einen Onlineshop in Dynamics 365 for Retail Client. Dieser Onlineshop wird dann über einen Onlineshop von Drittanbietern veröffentlicht, der in Dynamics 365 for Retail integriert ist. Der Drittanbieteronlineshop dient als die Ladenzeile (Benutzeroberfläche) für den Onlineshop und bietet eine Auswahl an CMS (Customer Management System)- und Benutzeroberflächen-Funktionen. Viele Integrationen dieses Typs sind für Dynamics 365 for Retail verfügbar. Die Eigenschaften, die Sie für den Onlineshop festlegen, steuern das Verhalten des Onlineshops. Definieren Sie beispielsweise die Navigationskategoriehierarchie in Dynamics 365 for Retail, und weisen Sie sie dem Onlineshop zu. Wenn Sie den Onlineshop über den Onlineshop eines Drittanbieters veröffentlichen, wird die Navigationskategoriehierarchie in der Onlineversion der Filiale angezeigt. Käufer verwenden dann die Navigationskategoriehierarchie, um den Onlineshop zu durchsuchen und nach Produkten zu suchen. Um einen Onlineshop zu erstellen, müssen Sie die Komponenten einrichten, die es ermöglichen, dass die Filiale Transaktionen verarbeiten kann. Sie müssen beispielsweise Sortimente hinzufügen, Attribute übernehmen und Zahlungsmethoden wie Versandarten einrichten. Sie können auch Preise, Aktionen, Rabatte, Handelsvereinbarungen und Versandbedingungen festlegen, die für den Onlineshop spezifisch sind. Nachdem Sie den Onlineshop über den Onlineshop des Drittanbieters veröffentlicht haben, können Sie Einzelhandelsproduktkataloge für den Onlineshop erstellen. Die Produkte im Katalog werden Produktlisten im Onlineshop. Wenn ein Käufer Produkte aus dem Onlineshop kauft, wird der verfügbare Lagerbestand im Client aktualisiert und synchronisiert. Zudem werden Aufträge für die Einkäufe generiert und an den Client zur Auftragserfüllung und Verarbeitung gesendet.

## <a name="set-up-an-online-store"></a>Onlineshop einrichten
Zum Einrichten eines Onlineshops müssen folgende Aufgaben ausgeführt werden.

1.  Erstellen Sie den Onlineshop.
2.  Fügen Sie den Onlineshop den entsprechenden Organisationshierarchien hinzu.
3.  Fügen Sie Sortimente hinzu, die die Produkte enthalten, die im Onlineshop verfügbar sind.
4.  Weisen Sie Preisgruppen für den Onlineshop zu oder erstellen Sie diese.
5.  Richten Sie die für den Onlineshop verfügbaren Lieferarten ein.
6.  Weisen Sie die Zahlungsmethoden zu, die für den Onlineshop akzeptiert werden.
7.  Wenn Sie es Käufern ermöglichen, Produkte online zu bestellen und in einem lokalen Shop abzuholen, weisen Sie dem Onlineshop Shoplokatorgruppen zu.
8.  Weisen Sie dem Onlineshop Attribute für Kanäle, Produkte und Aufträge zu. Kanalattribute gelten für den gesamten Onlineshop, Produktattribute gelten für die Produkte, die im Onlineshop angeboten werden, und Auftragsattribute gelten für Aufträge, die vom Onlineshop generiert werden.
9.  Ordnen Sie Attribute zu, um die Eigenschaften zu definieren, die bestimmen, wie sich die Attribute im Onlineshop verhalten. So können Sie festlegen, dass die Attribute erforderlich oder suchbar sein sollen.
10. Veröffentlichen Sie den Onlineshop, um die Shopstruktur beim gewählten Onlineshop des Drittanbieters zu generieren. **Wichtig:** Bevor Sie den Onlineshop veröffentlichen, müssen Sie ein Vertriebsort für den Onlineshop einrichten.

## <a name="retail-channel-navigation-hierarchies"></a>Navigationshierarchien – Retail Channel
Bevor Sie einen Onlineshop erstellen, müssen Sie die Navigationshierarchie für Vertriebsweg definieren, die Sie im Onlineshop verwenden möchten. Die Kalnavigationshierarchie für Vertriebsweg stellt die Kategoriehierarchie dar, die im Onlineshop angezeigt wird, nachdem der Filiale veröffentlicht ist. Wenn Sie Einzelhandelsproduktkataloge im Onlineshop veröffentlichen, sind die Produkte im Katalog den Kategorien in der Navigationshierarchie für Vertriebsweg zugeordnet. Die Hierarchie wird auch von den Käufern verwendet, um im Onlineshop zu navigieren.

## <a name="organization-hierarchies"></a>Organisationshierarchien
Organisationshierarchien werden verwendet, um Einzelhandelskanäle zu strukturieren. Organisationshierarchien stellen die Beziehungen zwischen den Organisationen dar, aus denen das Unternehmen besteht. Wenn Sie Onlineshops einrichten, können Sie diese einer Organisationshierarchie hinzufügen. Die Shops teilen dann Daten, die für Sortimente, Auffüllung und Berichterstellung verwendet werden. Wenn Sie eine Organisationshierarchie erstellen, müssen Sie einen Kostenträger zuweisen. Der Kostenträger gibt an, wie die Hierarchie in der Struktur des Unternehmens verwendet wird. Sie können eine Organisationshierarchie für die Filialenarbeitsgänge erstellen und diese Hierarchie für Sortimente, Auffüllung und Berichte verwenden. Sie können auch eine separate Organisationshierarchie für jeden Kostenträger erstellen. Sie können auch mehrere Hierarchien mit demselben Kostenträger erstellen und diesen je einen separaten Kanal zuweisen. Wenn Sie Einzelhandelsproduktkataloge im Onlineshop veröffentlichen möchten, sollten Sie mindestens den Onlineshop einer Organisationshierarchie für Sortimente hinzufügen. Die Produkte in einem Katalog werden von den Sortimenten ausgewählt, die dem Onlineshop zugewiesen sind. Wenn der Katalog veröffentlicht wird, vergleicht der Veröffentlichungsprozess die Gültigkeitsdaten für das Sortiment, das dem Onlineshop für die Produkte zugewiesen ist, die im Katalog enthalten sind, um zu bestimmen, welche Produkte im Onlineshop verfügbar gemacht werden.




