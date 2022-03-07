---
title: Verbesserungen bei der Bargeldverwaltung
description: In diesem Thema werden die Verbesserungen bei der Bargeldverwaltung in POS für Dynamics 365 Commerce beschrieben.
author: anpurush
manager: AnnBe
ms.date: 05/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-21
ms.dyn365.ops.version: ''
ms.openlocfilehash: ce75a191726fc430347f057ac511188acfbbf76e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5213161"
---
# <a name="cash-management-improvements"></a>Verbesserungen bei der Bargeldverwaltung

[!include [banner](includes/banner.md)]


Bargeldverwaltung ist eine wesentliche Funktion für Einzelhändler in physischen Läden. Einzelhändler möchten, dass ihre Läden Systeme haben, die eine vollständige Nachverfolgbarkeit und Verantwortbarkeit bei Bargeld und dessen Bewegung über verschiedene Kassen und Kassierer in einem Laden hinweg ermöglichen. Sie müssen in der Lage sein, eventuelle Differenzen abzustimmen und die Verantwortlichkeit zu bestimmen.


Microsoft Dynamics 365 Commerce verfügt über Bargeldverwaltungsfunktionen in seiner Verkaufsstellen-(POS)-Anwendung. In Versionen von Retail, die vor Version 10.0.3 liegen, ist die Bargeldverwaltungsfunktion nicht robust genug, um eine vollständige Nachverfolgbarkeit von Bargeldbewegungen in Läden zu ermöglichen. Obwohl Einzelhändler das Bargeld in einem Laden abstimmen können, können sie nicht präzise die Verantwortlichkeit bestimmen, sollte es zu Bargeldabweichungen kommen.


In Retail, Version 10.0.3 und höher, erhalten Einzelhändler die Nachverfolgbarkeit für die Bargeldhandhabung. Als Teil dieser Nachverfolgbarkeit werden Einzelhändler dazu in der Lage sein, Geldschränke zu definieren, doppelseitige Bargeldtransaktionen durchzuführen und Bargeldverwaltungstransaktionen abzustimmen.

## <a name="set-up-traceability-and-define-safes"></a>Einrichten von Nachverfolgbarkeit und Definieren von Geldschränken

Um die neuen Bargeldverwaltungsfunktionen einzurichten, führen Sie die folgenden Schritte aus um das Funktionsprofil für Läden zu konfigurieren.

1. Gehen Sie zu **Einzelhandel und Handel \> Kanaleinrichtung \> POS-Einrichtung \> POS-Profile \> Funktionsprofile**, und wählen Sie ein Funktionsprofil aus, das mit den Geschäften verknüpft ist, für die Sie die Verbesserungen für die Bargeldverwaltung zur Verfügung stellen möchten.
2. Legen Sie im Inforegister **Funktionen** des Funktionsprofils unter **Erweiterte Bargeldverwaltung** die Option **Bargeldnachverfolgbarkeit aktivieren** auf **Ja** fest.
3. Um Geldschränke einzurichten, gehen Sie zu **Einzelhandel und Handel \> Kanäle \> Geschäfte \> Alle Geschäfte**, und wählen Sie ein Geschäft aus.
4. Auf der Seite **Ladengeschäfte** im Aktivitätsbereich auf der Registerkarte **Einrichten** in der Gruppe **Einrichten** wählen Sie **Geldschränke** aus. Mit dieser Option können Sie mehrere Geldschränke für einen Laden definieren und verwalten.
4. Bevor Sie die Funktion verwenden können, müssen Sie den Verteilungszeitplan-Einzelvorgang **1070 Kanalkonfiguration** ausführen, um diese Konfigurationen mit der Kanaldatenbank zu synchronisieren.

## <a name="additional-cash-management-changes"></a>Zusätzliche Bargeldverwaltungsänderungen

In Retail, Version 10.0.3 und höher, werden die folgenden Funktionen ebenfalls bereitgestellt, die sich auf Bargeldtransaktionen beziehen:

- Ein Benutzer, der zum „Startbetrag deklarieren“ aufgefordert wird, muss die Quelle des Bargelds eingeben. Der Benutzer kann nach den verfügbaren Geldschränken suchen, die im Laden definiert sind, und den Geldschrank auswählen, aus dem das Bargeld entnommen wird, damit es in die Kasse gelegt werden kann.
- Ein Benutzer, der einen Arbeitsgang zur „Zahlungsmittelentfernung“ vornimmt, wird dazu aufgefordert, in einer Liste offener „Bareinlage“-Transaktionen die Transaktion auszuwählen, zu der dieser Arbeitsgang ausgeführt wird. Wenn die entsprechende Bareinlage im System nicht vorhanden ist, kann der Benutzer eine nicht verknüpfte Zahlungsmittelentfernungstransaktion erstellen.
- Durch einen Arbeitsgang zur „Zahlungsmittelentfernung“ wird ein Benutzer aufgefordert, in einer Liste offener „Bareinlage“-Transaktionen die Transaktion auszuwählen, zu der der Bareinlage-Arbeitsgang ausgeführt wird. Wenn die entsprechende Zahlungsmittelentfernung im System nicht vorhanden ist, kann der Benutzer eine nicht verknüpfte Bareinlage-Transaktion erstellen.
- Ein Benutzer, der eine „Ablage im Geldschrank“ vornimmt, wird dazu aufgefordert, den Geldschrank auszuwählen, in den das Bargeld gelegt wird.
- Für Geldschränke, die in einem Laden definiert sind, können Benutzer Arbeitsgänge verwalten, wie z. B. das Deklarieren des Startbetrags, das Vornehmen einer Bareinlage, die Zahlungsmittelentfernung und eine Bankeinzahlung.
- Für Benutzer, die die entsprechenden Benutzerrechte haben, zeigen Arbeitsgänge zu „Schichtverwaltung“ die Bargeldsalden aktiver, ausgesetzter und blind geschlossener Schichten an.
- Um die Bargeldtransaktionen innerhalb einer Schicht oder schichtübergreifend abzustimmen, wählen Sie die abzustimmende Schicht aus, und wählen Sie dann **Abstimmen** aus. Die Ansicht, die geöffnet ist, zeigt die Liste abgestimmter und nicht abgestimmter Transaktionen unter getrennten Registerkarten an. Von dieser Ansicht aus können Benutzer entweder nicht abgestimmte Transaktionen auswählen und sie abstimmen oder zuvor abgestimmte Transaktionen auswählen und deren Abstimmung aufheben.
- Während der Abstimmung, wenn die ausgewählte Transaktion nicht ausgeglichen werden kann, muss der Benutzer eine Beschreibung des Grunds eingeben, warum die Abstimmung keinen Saldo ergibt. Benutzer können eine einzelne Transaktion auswählen und sie mit der relevanten Ursachenbeschreibung abstimmen, wie diese benötigt wird.
- Benutzer können fortfahren, Transaktionen abzustimmen oder deren Abstimmung aufzuheben, bis die Schicht geschlossen ist. Nachdem eine Schicht abgeschlossen ist, kann die Abstimmung für die Transaktionen nicht aufgehoben werden.
- Wenn ein Benutzer beschließt, eine Schicht zu schließen, überprüft Commerce, dass es keine nicht abgestimmten Bargeldverwaltungstransaktionen in der Schicht gibt. Sind nicht abgestimmte Transaktionen vorhanden, können Benutzer eine Schicht nicht schließen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]