---
title: Berechtigungen zum Bestellen von Produkten im Auftrag einer anderen Person einrichten
description: Diese Prozedur zeigt, wie Arbeitskräften die Berechtigung erteilt wird, Bestellanforderungen im Auftrag anderer Arbeitskräfte vorzubereiten.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchReqAuthorization, HcmWorkerLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 35688d191cef06cc15251a6e10a2e8c9afb0e08b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "314807"
---
# <a name="set-up-permissions-for-ordering-products-on-behalf-of-someone-else"></a>Berechtigungen zum Bestellen von Produkten im Auftrag einer anderen Person einrichten

[!include [task guide banner](../../includes/task-guide-banner.md)]

Diese Prozedur zeigt, wie Arbeitskräften die Berechtigung erteilt wird, Bestellanforderungen im Auftrag anderer Arbeitskräfte vorzubereiten. Das bedeutet, kann eine Bestellanforderung "Antragsteller" eine Bestellanforderung für eine andere  "anfordernden Person" erstellen kann. Die Prozedur zeigt auch, wie Arbeitsberechtigungen gewährt werden, um Artikel oder Services in unterschiedlichen juristischen Personen oder Organisationseinheiten zu gewähren. Normalerweise werden diese Aufgaben von einem Einkaufsleiter ausgeführt. Sie können diese Prozedur entweder für Daten für das Demodatenunternehmen USMF oder für Ihre eigenen Daten verwenden.


## <a name="grant-permission-to-enter-purchase-requisitions-on-behalf-of-another-worker"></a>Berechtigung erteilen, um Bestellanforderungen im Auftrag einer anderen Arbeitskraft einzugeben
1. Wechseln Sie zu Beschaffung > Einstellungen > Richtlinien > Bestellanforderungsberechtigungen.
    * Stellen Sie sicher, dass das Feld "Aktuelle Ansicht" auf "Durch Antragsteller" festgelegt ist.  Die Liste im linken Bereich zeigt Personen an, denen die Berechtigung erteilt werden kann, Anforderungen im Auftrag anderer Personen vorzubereiten.  
2. Wählen Sie die Person aus, die (dem Antragsteller) die Berechtigung erteilt.
3. Klicken Sie auf Hinzufügen.
4. Suchen Sie die Person und wählen Sie sie aus, die als anfordernde Person hinzugefügt werden soll.
    * Die anfordernde Person ist die Person, in dessen Auftrag der Antragsteller Anforderungen erstellen kann.  
    * Wählen sie im Feld "Autorisierung" die Option "'Spezifisch" aus, wenn der Antragsteller in der Lage sein sollte, Bestellanforderungen im Auftrag der ausgewählten Arbeitskraft zu erstellen. Wählen Sie "Berichterstellung" aus, wenn der Antragsteller in der Lage sein soll, Bestellanforderungen im Auftrag aller Arbeitskräfte zu erstellen, die dieser Arbeitskraft unterstellt sind.  
5. Geben Sie ein Datum im Feld "Gültig" ein.
6. Geben Sie im Feld "Ablauf" ein Datum ein.

## <a name="view-preparers-who-have-permission-to-create-purchase-requisitions-for-a-selected-worker"></a>Antragsteller anzeigen, die die Berechtigung zum Erstellen von Bestellanforderungen für eine ausgewählte Arbeitskraft haben
1. Wählen Sie im Feld "Aktuelle Ansicht" die Option "Durch anfordernde Person" aus.
    * Diese Anzeige zeigt eine Liste von Antragstellern an, denen die Berechtigung zum Erstellen von Bestellanforderungen im Auftrag einer ausgewählten Arbeitskraft erteilt wurde.  
2. Verwenden Sie den Schnellfilter, um die Arbeitskraft zu suchen, die Sie soeben als anfordernde Person hinzugefügt haben.
3. Wählen Sie die anfordernde Person aus.
    * Die Antragstellerliste zeigt die Personen an, die die Berechtigung haben, Artikel im Auftrag des Antragstellers zu bestellen, der im linken Bereich ausgewählt ist.   Sie können zusätzliche Antragsteller hier hinzufügen.   In dieser Ansicht können Sie der anfordernden Person auch die Berechtigung erteilen, Anforderungen in juristischen Personen und Organisationseinheiten zu erstellen, die nicht die primäre juristische Person oder Organisationseinheit dieser Person sind.  

