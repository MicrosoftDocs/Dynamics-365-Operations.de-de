--- 
title: " POS-Berechtigungsgruppen erstellen"
description: Diese Prozedur zeigt, wie eine POS-Berechtigungsgruppe erstellt wird.
author: scott-tucker
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: b0c930e3722d1d0b1fff8efad7a785a153436b6d
ms.contentlocale: de-de
ms.lasthandoff: 07/28/2017

---
# <a name="create-pos-permission-groups"></a> POS-Berechtigungsgruppen erstellen

[!include[task guide banner](../includes/task-guide-banner.md)]

Diese Prozedur zeigt, wie eine POS-Berechtigungsgruppe erstellt wird. Das Demodatenunternehmen, das verwendet wird, um diese Aufgabe zu erstellen, ist USRT. Diese Aufgabe ist für die Rolle "Bereichsleiter (Einzelhandel)" vorgesehen.

1. Gehen Sie zu "Berechtigungsgruppen".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "POS-Berechtigungsgruppenkennung" einen Wert ein.
4. Geben Sie im Feld "Beschreibung" einen Wert ein.
5. Wählen Sie "Ja" im Feld "Zeiterfassungseinträge anzeigen" aus.
    * Sie können verschiedene Berechtigungen für Ihre POS-Berechtigungsgruppe jetzt aktivieren oder deaktivieren. Bei einigen Berechtigungen können Sie einen Wert festlegen, der verwendet wird, wenn überprüft werden soll, ob der POS-Benutzer die Aktivität ausführen kann.  Dieses Aufgabenhandbuch ermöglicht einige Berechtigungen, die einem Kassierer zugeordnet werden können.  
6. Wählen Sie "Ja" im Feld "Auftragserstellung zulassen" aus.
7. Wählen Sie "Ja" im Feld "Auftragsbearbeitung zulassen" aus.
8. Wählen Sie "Ja" im Feld "Auftragsabruf zulassen" aus.
9. Wählen Sie "Ja" im Feld "Kennwortänderung zulassen" aus.
10. Wählen Sie "Ja" im Feld "Blindschließen zulassen" aus.
11. Klicken Sie auf "Speichern".
    * Nachdem die Änderungen gespeichert sind, müssen Sie den Mitarbeiterverteilungszeitplan ausführen, um die Änderungen an Einzelhandelskanäle zu übertragen.  
12. Schließen Sie die Seite.
13. Gehen Sie zu "Einzelvorgänge".
    * Danach weisen wir die POS-Berechtigungsgruppe einem Einzelvorgang zu.  
14. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
15. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
16. Klicken Sie auf Bearbeiten.
17. Erweitern Sie den Einzelvorgangsklassifizierungs-Abschnitt.
18. Geben Sie im Feld "POS-Berechtigungsgruppe" einen Wert ein oder wählen Sie einen Wert aus.
    * Alle Arbeitskräfte in Positionen für diesen Einzelvorgang werden die Einstellungen dieser POS-Berechtigungsgruppe verwenden, es sei denn, die POS-Berechtigungen dieser Arbeitskräfte wurden in ihrer Positionsebene überschrieben.  
19. Klicken Sie auf "Speichern".
    * Nachdem die Änderungen gespeichert sind, müssen Sie den Mitarbeiterverteilungszeitplan ausführen, um die Änderungen an Einzelhandelskanäle zu übertragen.  


