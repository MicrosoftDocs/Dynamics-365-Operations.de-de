---
title: Juristische Personen erstellen
description: In diesem Artikel wird beschrieben, wie Sie juristische Personen in Microsoft Dynamics 365 Commerce erstellen, die erstellt und konfiguriert werden müssen, bevor Kanäle erstellt werden.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: e99536d3706c842d69060136f23508208b16b461
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276318"
---
# <a name="create-legal-entities"></a>Juristische Personen erstellen

[!include [banner](includes/banner.md)]

In diesem Artikel wird beschrieben, wie Sie juristische Personen in Microsoft Dynamics 365 Commerce erstellen, die erstellt und konfiguriert werden müssen, bevor Kanäle erstellt werden.

Eine juristische Person ist eine Organisation mit einer registrierten oder eingetragenen Rechtsform. Juristische Personen können Verträge abschließen und sind verpflichtet, Finanzaufstellungen zum Erstellen eines Berichts über ihre Vermögens-, Finanz- und Ertragslage vorzubereiten.

Ein Unternehmen ist eine Art von juristischer Person. Derzeit sind Unternehmen die einzige Art von juristischer Person, die Sie erstellen können, und jeder juristischen Person ist eine Unternehmenskennung zugeordnet. Diese Zuordnung ist notwendig, da einige Funktionsbereiche im Programm eine Unternehmenskennung (oder *DataAreaId*) in den Datenmodellen verwenden. In diesen Funktionsbereichen werden Unternehmen als Grenze für die Datensicherheit verwendet. Benutzer können nur auf Daten für das Unternehmen zugreifen, bei dem sie derzeit angemeldet sind. 

Beim Erstellen eines Kanals müssen Sie angeben, zu welcher juristischen Person dieser Kanal gehört.

## <a name="create-a-new-legal-entity"></a>Eine neue juristische Person erstellen

Gehen Sie folgendermaßen vor, um eine neue juristische Person in Dynamics 365 Commerce zu erstellen.

1. Gehen Sie im Navigationsbereich zu **Module \> Hauptsitz einrichten \> Juristische Personen**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus. Das Fenster **Neue juristische Person** wird rechts angezeigt.
1. Geben Sie im Feld **Name** einen Wert ein.
1. Geben Sie im Feld **Unternehmen** einen Wert ein.
1. Wählen Sie im Feld **Land/Region** einen Wert aus, oder geben Sie einen Wert ein.
1. Wählen Sie **OK** aus. 

   ![Erstellung einer juristischen Person.](media/legal-entities.png)

1. Stellen Sie im Abschnitt **Allgemein** die folgenden allgemeinen Informationen zur juristischen Person bereit: 
   1. Geben Sie einen Suchbegriff ein, falls erforderlich. Ein Suchbegriff ist ein alternativer Name, der verwendet werden kann, um nach dieser juristischen Person zu suchen. 
   1. Wählen Sie aus, ob diese juristische Person als Konsolidierungsunternehmen verwendet werden soll.
   1. Wählen Sie aus, ob diese juristische Person als Unternehmen mit Löschungseinträgen verwendet werden soll. 
   1. Wählen Sie die **Standardsprache** für die Entität aus. 
   1. Wählen Sie die **Zeitzone** für die Entität aus.
1. Wählen Sie im Abschnitt **Adressen** die Option **Bearbeiten**, um die Adressinformationen wie die Straße und Hausnummer, die Postleitzahl und den Ort einzugeben.
1. Geben Sie im Abschnitt **Kontaktinformationen** Informationen zu den Kommunikationsmethoden ein, wie beispielsweise E-Mail-Adressen, URLs und Telefonnummern.
1. Geben Sie im Abschnitt **Offenlegungspflicht** die Registrierungsnummern ein, die für die Offenlegungspflicht verwendet werden.
1. Geben Sie im Abschnitt **Registrierungsnummern** alle Informationen ein, die für die juristische Person erforderlich sind.
1. Geben Sie im Abschnitt **Bankkontinformationen** die Bankkonten und Bankleitzahlen für die juristische Person ein.
1. Geben Sie im Abschnitt **Außenhandel und Logistik** die Versandinformationen für die juristische Person ein.
1. Im Abschnitt **Nummernkreise** können Sie die Nummernkreise anzeigen, die der juristischen Person zugeordnet sind. Dies ist zunächst leer.
1. Im Abschnitt **Dashboardbild** zeigen Sie das Logo und/oder Dashboardbild an, das der juristischen Person zugeordnet ist, oder ändern Sie es.
1. Geben Sie im Abschnitt **Steuerregistrierung** die Registrierungsnummern ein, die für die Meldung bei Steuerbehörden verwendet werden.
1. Geben Sie im Abschnitt **Steuererklärung (US 1099)** die Informationen zur Steuererklärung (US 1099) für die juristische Person ein.
1. Geben Sie im Abschnitt **Steuerinformation** die Steuerinformation für die juristische Person ein.
1. Wählen Sie **Speichern**.

Das folgende Bild zeigt die Details eines Beispiels für eine juristische Person.

![Allgemeiner Teil der juristischen Person.](media/legal-entities-general.png)
   
## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Organisationen und Organisationshierarchien – Übersicht](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[Planen Ihrer Organisationshierarchie](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[Organisationshierarchien](channels-org-hierarchies.md)

[Kanalübersicht](channels-overview.md)

[Voraussetzungen der Kanaleinrichtung](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
