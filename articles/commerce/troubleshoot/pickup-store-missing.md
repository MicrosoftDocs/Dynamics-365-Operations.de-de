---
title: Einzelhandelsshop wird nicht in der Liste an Shops angezeigt, in denen abgeholt werden kann
description: Dieser Artikel enthält Anleitungen zur Fehlerbehebung, die hilfreich sein können, wenn ein Einzelhandelsshop nicht in der Liste der Shops aufgeführt ist, in denen Artikel abgeholt werden können.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: b6cec3d9d598be221516506388e4797ad579a610
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286751"
---
# <a name="retail-store-doesnt-appear-in-the-list-of-stores-to-pick-up-from"></a>Einzelhandelsshop wird nicht in der Liste an Shops angezeigt, in denen abgeholt werden kann

[!include [banner](../../includes/banner.md)]

Dieser Artikel enthält Anleitungen zur Fehlerbehebung, die hilfreich sein können, wenn ein Einzelhandelsshop nicht in der Liste der Shops aufgeführt ist, in denen Artikel abgeholt werden können.

## <a name="description"></a>Beschreibung

Ein Einzelhandelsshop wird nicht in der Liste der Shops angezeigt, in denen Artikel abgeholt werden können.

## <a name="resolution"></a>Lösung

### <a name="configure-the-longitude-and-latitude-for-the-store-address-in-commerce-headquarters"></a>Den Längen- und Breitengrad für die Shopadresse in der Commerce-Zentralverwaltung konfigurieren

Befolgen Sie diese Schritte, um den Längen- und Breitengrad für die Shopadresse in der Commerce-Zentralverwaltung zu konfigurieren.

1. Rufen Sie **Retail und Commerce \> Kanäle \> Shops \> Alle Shops** auf.
1. Suchen Sie das Geschäft, das in den Abholoptionen auf der E-Commerce-Website angezeigt werden soll. Notieren Sie sich den Wert seiner **Organisationseinheit**.
1. Rufen Sie **Organisationsverwaltung \> Organisationen \> Organisationseinheiten** auf.
1. Suchen Sie nach der Nummer der Organisationseinheit, die Sie zuvor notiert haben, und wählen Sie dann die Organisationseinheit in den Suchergebnissen aus.
1. Wählen Sie im Inforegister **Adressen** **Weitere Optionen** und anschließend **Erweitert** aus.
1. Vergewissern Sie sich, dass im Inforegister **Allgemein** die Felder **Längengrad** und **Breitengrad** korrekt eingestellt sind. Vergewissern Sie sich, dass im Rahmen dieses Schritts die Werte korrekt als positive oder negative Zahlen angegeben sind.

### <a name="configure-fulfillment-groups-in-commerce-headquarters"></a>Erfüllungsgruppen in der Commerce-Zentralverwaltung konfigurieren

Befolgen Sie diese Schritte, um Erfüllungsgruppen in der Commerce-Zentralverwaltung zu konfigurieren.

1. Rufen Sie **Retail und Commerce \> Kanäle \> Onlineshops** auf.
1. Wählen Sie den zu konfigurierenden Onlineshop aus.
1. Wählen Sie im Aktionsbereich die Option **Einrichten** und anschließend **Erfüllungsgruppenzuweisung** aus.
1. Wählen Sie auf der Seite **Erfüllungsgruppenzuweisung** die Erfüllungsgruppe für den Onlineshop aus.
1. Vergewissern Sie sich, dass das Einzelhandelsgeschäft unter **Einrichtung** korrekt für die Erfüllungsgruppe konfiguriert ist.

## <a name="additional-resources"></a>Zusätzliche Ressourcen 

[Erstellen einer Organisationseinheit](../../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md)

[Einen Onlinechannel einrichten](../channel-setup-online.md)
