---
title: Berechtigungen zum Bestellen von Produkten im Auftrag einer anderen Person einrichten
description: In diesem Artikel wird erläutert, wie Sie den Mitarbeitern die Erlaubnis erteilen, Bestellanforderungen im Namen anderer Mitarbeiter zu erstellen.
author: GalynaFedorova
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchReqAuthorization, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3053f28fdf97637b1da5f644f64676bfd10fb6a0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8854209"
---
# <a name="set-up-permissions-for-ordering-products-on-behalf-of-someone-else"></a>Berechtigungen zum Bestellen von Produkten im Auftrag einer anderen Person einrichten

[!include [banner](../../includes/banner.md)]

In diesem Artikel wird erläutert, wie Sie den Mitarbeitern die Erlaubnis erteilen, Bestellanforderungen im Namen anderer Mitarbeiter zu erstellen. Das bedeutet, dass eine Bestellanforderung Antragsteller eine Bestellanforderung für eine andere anfordernden Person erstellen kann. Die Prozedur zeigt auch, wie Arbeitsberechtigungen gewährt werden, um Artikel oder Services in unterschiedlichen juristischen Personen oder Organisationseinheiten zu gewähren. Normalerweise werden diese Aufgaben von einem Einkaufsleiter ausgeführt. Sie können diese Prozedur entweder für Daten für das Demodatenunternehmen USMF oder für Ihre eigenen Daten verwenden.


## <a name="grant-permission-to-enter-purchase-requisitions-on-behalf-of-another-worker"></a>Berechtigung erteilen, um Bestellanforderungen im Auftrag einer anderen Arbeitskraft einzugeben
1. Gehen Sie im Navigationsbereich zu **Module > Beschaffung und Sourcing > Einrichtung > Richtpositionen > Berechtigungen für Bestellanforderungen**. Stellen Sie sicher, dass das Feld **Aktuelle Ansicht** auf **Durch Präparator** gesetzt ist. Die Liste im linken Bereich zeigt Personen an, denen die Berechtigung erteilt werden kann, Anforderungen im Auftrag anderer Personen vorzubereiten.  
2. Wählen Sie die Person aus, die (dem Antragsteller) die Berechtigung erteilt.
3. Wählen Sie **Hinzufügen** aus.
4. Suchen Sie die Person und wählen Sie sie aus, die als anfordernde Person hinzugefügt werden soll.
    - Die anfordernde Person ist die Person, in dessen Auftrag der Antragsteller Anforderungen erstellen kann.  
    - Wählen Sie im Feld **Berechtigung** **Spezifisch**, wenn der Vorbereiter Bestellanforderungen für den ausgewählten Mitarbeiter erstellen können soll. Wählen Sie **Berichterstattung**, wenn der Vorbereiter auch Bestellanforderungen für alle Mitarbeiter erstellen können soll, die an diesen Mitarbeiter berichten.  
5. Geben Sie im Feld **Effektiv** ein Datum ein.
6. Geben Sie im Feld **Ablauf** ein Datum ein.

## <a name="view-preparers-who-have-permission-to-create-purchase-requisitions-for-a-selected-worker"></a>Antragsteller anzeigen, die die Berechtigung zum Erstellen von Bestellanforderungen für eine ausgewählte Arbeitskraft haben
1. Wählen Sie im Feld **Aktuelle Ansicht** **Durch Antragsteller**. Diese Anzeige zeigt eine Liste von Antragstellern an, denen die Berechtigung zum Erstellen von Bestellanforderungen im Auftrag einer ausgewählten Arbeitskraft erteilt wurde.  
2. Verwenden Sie den Schnellfilter, um die Arbeitskraft zu suchen, die Sie soeben als anfordernde Person hinzugefügt haben.
3. Wählen Sie die anfordernde Person aus. Die Antragstellerliste zeigt die Personen an, die die Berechtigung haben, Artikel im Auftrag des Antragstellers zu bestellen, der im linken Bereich ausgewählt ist.  Sie können zusätzliche Antragsteller hier hinzufügen. In dieser Ansicht können Sie der anfordernden Person auch die Berechtigung erteilen, Anforderungen in juristischen Personen und Organisationseinheiten zu erstellen, die nicht die primäre juristische Person oder Organisationseinheit dieser Person sind.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]