---
title: POS-Berechtigungsgruppen erstellen
description: In diesem Thema wird erläutert, wie Sie eine POS-Berechtigungsgruppe erstellen.
author: scott-tucker
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailPosPermissionGroup, HcmJob
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1d4634ec275d3d1c2a131c4c1d61cc983e485b14
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798488"
---
# <a name="create-pos-permission-groups"></a>POS-Berechtigungsgruppen erstellen

[!include [banner](../includes/banner.md)]

In diesem Thema wird erläutert, wie Sie eine POS-Berechtigungsgruppe erstellen. Das Demodatenunternehmen, das verwendet wird, um diese Aufgabe zu erstellen, ist USRT. Diese Aufgabe ist für die Rolle „Bereichsleiter (Commerce)“ vorgesehen.

1. Wechseln Sie im Navigationsbereich zu **Module > Retail and Commerce > Mitarbeiter > Berechtigungsgruppen**.
2. Wählen Sie **Neu** aus.
3. Geben Sie im Feld **POS-Berechtigungsgruppenkennung** einen Wert ein.
4. Geben Sie im Feld **Beschreibung** einen Wert ein.
5. Wählen Sie **Ja** im Feld **Zeiterfassungseinträge anzeigen** aus. Sie können verschiedene Berechtigungen für Ihre POS-Berechtigungsgruppe jetzt aktivieren oder deaktivieren. Bei einigen Berechtigungen können Sie einen Wert festlegen, der verwendet wird, wenn überprüft werden soll, ob der POS-Benutzer die Aktivität ausführen kann. Dieses Aufgabenhandbuch ermöglicht einige Berechtigungen, die einem Kassierer zugeordnet werden können.  
6. Wählen Sie **Ja** im Feld **Auftragserstellung zulassen** aus.
7. Wählen Sie **Ja** im Feld **Auftragsbearbeitung zulassen** aus.
8. Wählen Sie **Ja** im Feld **Auftragsabruf zulassen** aus.
9. Wählen Sie **Ja** im Feld **Kennwortänderung zulassen** aus.
10. Wählen Sie **Ja** im Feld **Blindschließen zulassen** aus.
11. Wählen Sie **Speichern**. Nachdem die Änderungen gespeichert sind, müssen Sie den Mitarbeiterverteilungszeitplan ausführen, um die Änderungen an Commerce-Kanäle zu übertragen. 
12. Wechseln Sie im Navigationsbereich zu **Module > Personalverwaltung > Einzelvorgänge > Einzelvorgänge**.
13. Danach weisen wir die POS-Berechtigungsgruppe einem Einzelvorgang zu. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
14. Wählen Sie **Bearbeiten** aus.
15. Erweitern Sie den Abschnitt **Einzelvorgangsklassifizierung**.
16. Geben Sie im Feld "POS-Berechtigungsgruppe" einen Wert ein oder wählen Sie einen Wert aus. Alle Arbeitskräfte in Positionen für diesen Einzelvorgang werden die Einstellungen dieser POS-Berechtigungsgruppe verwenden, es sei denn, die POS-Berechtigungen für diese Arbeitskräfte wurden in ihrer Positionsebene überschrieben.  
17. Wählen Sie **Speichern**. Nachdem die Änderungen gespeichert sind, müssen Sie den Mitarbeiterverteilungszeitplan ausführen, um die Änderungen an Kanälen zu übertragen.  



[!INCLUDE[footer-include](../../includes/footer-banner.md)]