---
title: Abwesenheitserfassung in "Zeit und Anwesenheit"
description: "In diesem Thema wird erläutert, wie Sie Abwesenheitserfassungen in Zeit und Anwesenheit behandeln."
author: johanhoffmann
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JMGParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 477724e6211a084638e8a0b7133f60edef07b3ad
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="absence-registration-in-time-and-attendance"></a>Abwesenheitserfassung in "Zeit und Anwesenheit"

[!include [banner](../includes/banner.md)]

In diesem Thema werden die Konzepte für Abwesenheit und erläutert, wie Abwesenheiten in Zeit und Anwesenheit behandelt.

## <a name="absence-that-is-based-on-regular-work-hours"></a>Abwesenheit, die auf Grundlage regulärer Arbeitsstunden ist

Arbeitskräfte gelten als abwesend alle Stunden, die sie nicht während der normalen Arbeitsstunden arbeiten. Reguläre Arbeitsstunden werden im Standardzeitprofil einer Arbeitskraft definiert.

Beispielsweise arbeitet eine Arbeitskraft an einem Tagprofil, die Einstempeln um 7:00 Uhr und Ausstempeln um 3:00 Uhr hat. Wenn die Arbeitskraft am Morgen 9:00 einstempelt, wird sie als Abwesenheit von 7:00 bis 9:00 an diesem Tag angesehen.

In diesem Fall werden Arbeitskräfte aufgefordert, einen Grund für die Abwesenheit einzugeben. Sie können einen Grund angeben, indem ein Abwesenheitscode ausgewählt wird.

## <a name="absence-codes"></a>Abwesenheitscodes

Abwesenheitscodes definieren die verschiedenen Arten der Abwesenheit. Abwesenheitscodes werden durch das Unternehmen definiert.

Verschiedene Regeln können auf diese Codes angewendet werden. So kann ein Abwesenheitscode konfiguriert werden, um Lohn abzuziehen oder zu erteilen.

Beispielsweise ein Unternehmen definiert einen Abwesenheitscode **Verspätet**, den Arbeitskräfte verwenden, wenn sie überfällig und eintreffen ohne triftigen Grund ist. Das Unternehmen definiert auch **Interner Kurs** einen Abwesenheitscode, den Arbeitskräfte für Zeit verwendet werden, der sie das die Teilnahme an interne Kurse ausgeben. Diese Abwesenheitscodes können eingerichtet werden, sodass **Verspätet** vom Lohn der Arbeitskraft, aber nicht verarbeitet **Interner Kurs** vom Lohn der Arbeitskraft abzieht.

Sie können in automatische Abwesenheitscodes einrichten. Diese Abwesenheitscodes können verwendet werden, um die Zeit einer Arbeitskraft zu berechnen, wenn keine Abwesenheit erfasst wird. Das Zeitprofil der Arbeitskraft abhängig, ob der Abwesenheitscode für Standardzeit oder Gleitzeit verwendet wird.

### <a name="set-up-standard-time-and-flex-time"></a>Einstellungsstandardzeit und -Gleitzeit

- Konfigurieren Sie die Parameter für Standardzeit und Gleitzeit, indem Sie die Optionen **Automatische Einfügung von Abwesenheit** und **Automatisches Einfügen Gleitzeit-** auf der Seite **Zeit- und Anwesenheitsparameter**.

## <a name="absence-groups"></a>Abwesenheitsgruppen

Abwesenheitscodes sind logische Gruppen von Abwesenheitscodes. Mithilfe von Abwesenheitsgruppen können Sie Abwesenheitscodes gruppieren, die gemeinsame Merkmale haben. Hierzu gehören Abwesenheitscodes für eine zulässige Abwesenheit oder Abwesenheit aufgrund eines Arzttermins, der Jury-Pflicht oder eines kranken Kinds.

## <a name="planned-absence"></a>Geplante Abwesenheit

Wenn Sie wissen, dass eine Arbeitskraft während einer Periode ein, z. B. bevorstehenden Urlaub abwesend ist, können Sie eine geplante Abwesenheit verwenden. Sie richten geplante Abwesenheit ein, indem Sie den Abwesenheitscode so konfigurieren, dass er die geplante Abwesenheit berücksichtigt. Wenn Sie eine geplante Abwesenheit einrichten, werden Sie nicht für einen Abwesenheitscode für die Abwesenheitsperiode aufgefordert, wenn Benutzerzeiterfassungen berechnet werden. Geplante Abwesenheit kann für einzelne Arbeitskräfte definiert werden, oder Sie können einen Stapelverarbeitungsauftrag definieren, um Aktualisierung der geplante Abwesenheit für Arbeitskräfte zu aktualisieren.

### <a name="set-up-planned-absence"></a>Geplante Abwesenheit einrichten

1. Wählen Sie **Personalverwaltung** &gt; **Arbeitskräfte** &gt; **Mitarbeiter** aus, und wählen Sie einen Mitarbeiter aus.
2. Wählen Sie **Zeit** &gt; **Zeit-Zuweisungen** &gt; **Zeit-Abwesenheitserfassung** aus, und richten Sie die geplante Abwesenheit.

## <a name="interrupted-planned-absence"></a>Unterbrochene geplante Abwesenheit

Wenn Sie die Option **Unterbrechen** anwenden, wenn Sie eine geplante Abwesenheit einrichten, wird die geplante Abwesenheit unterbrochen, wenn die Arbeitskraft während der geplanten Abwesenheitsperiode sich anmeldet. Die geplante Abwesenheit wird als **Unterbrochen** markiert und hat keine Auswirkung auf zukünftige Berechnungen.

### <a name="set-up-a-planned-absence-for-interruption"></a>Hier können Sie eine geplante Unterbrechung für Abwesenheit einrichten

1. Öffnen Sie die Seite **Zeit-Abwesenheitserfassung**, wie in der Prozedur zum Installieren der geplante Abwesenheit erläutert.
2. Wählen Sie **Unterbrechen** aus.

Die Option **Unterbrechen** wird angewendet, wenn die Zeit durch das Shop-Terminal oder das Shop-Gerät erfasst wird. Die Option gilt nicht, wenn die Erfassungen für die Berechnungs- und Genehmigungsseiten eingegeben werden, oder auf der **Elektronische Zeitkarte**-Seite.

## <a name="examples-of-the-use-of-absence-in-a-flex-profile"></a>Beispiele für Gebrauchs von Abwesenheit in einem Gleitzeitprofil

Die drei folgenden Beispiele zeigen, wie Abwesenheit in einem Profil berechnet wird, das Gleitzeitperioden hat.

In den folgenden Beispielen wird folgendes Profil verwendet:

| Einstempeln | Standardzeit    | Pause             | Standardzeit | Gleitzeit-        | Ausstempeln | Gleitzeit+        |
|----------|------------------|-------------------|---------------|--------------|-----------|--------------|
| 8:00     | 9 bis 11:30 | 11:30 bis bis 12 PM | 12 PM bis 3 PM | 3 PM bis 4 PM | 4 nachmittags      | 4 PM bis 6 PM |

### <a name="example-1-signing-out-during-a-flex--period"></a>Beispiel 1: Abmelden während einer Flexperiode

Die Arbeitskraft stempelt um 8:00 Uhr ein und stempelt um 3:30 Uhr aus. In diesem Fall, da die Arbeitskraft in einer Flexperiode ausstempelt, wird keine Abwesenheit berechnet, und eine halbe Stunde wird vom Gleitzeitsaldo der Arbeitskraft abgezogen.

### <a name="example-2-signing-out-in-during-standard-time-period"></a>Beispiel 2: Abmelden während des Standardzeitraums

Die Arbeitskraft stempelt um 8:00 Uhr ein und stempelt um 2:30 Uhr aus. In diesem Fall, da die Arbeitskraft im Standardzeitzeitraum ausstempelt, Abwesenheit wird von 2:30 Uhr zu 4 PM berechnet, und eine der Abwesenheitsperiode 1,5 Stunden wird erfasst. Ein Abwesenheitscode ist für diese Periode erforderlich.

### <a name="example-3-signing-out-during-a-flex-period"></a>Beispiel 3: Abmelden während einer Flex+-Periode

Die Arbeitskraft stempelt um 8:00 Uhr ein und stempelt um 4:30 Uhr aus. In diesem Fall, da die Arbeitskraft in einer Flex+-Periode ausstempelt, wird keine Abwesenheit berechnet, und eine halbe Stunde wird zum Gleitzeitsaldo der Arbeitskraft addiert.

## <a name="absence-in-the-calculation-and-approval-process"></a>Abwesenheit im Berechnungs- und Genehmigungsprozess

Arbeitskraftzeiterfassungen müssen berechnet und genehmigt werden, damit sie einem Lohnbuchhaltungssystem als Lohnelemente übertragen werden können.

Eine genehmigende Person kann die Zeiterfassungen einer Arbeitskraft ändern. Der Genehmiger kann jede Abwesenheit auch ändern, die die Arbeitskraft registriert hat. Wenn der Genehmiger manuell eine Zeitperiode eingibt, die einen Abwesenheitscode hat, wird der Abwesenheitscode für diese Periode nicht durch den Standardabwesenheitscode anhand von Zeit- und Anwesenheitsparametern überschrieben.

Beispielsweise stempelt eine Arbeitskraft um 10 ein und wählt einen Abwesenheitscode aus, der angibt, dass sie sich verspätet. Später informiert die Arbeitskraft ihren Supervisor, dass sie einen Arzttermin von 8 bis zu 10 einen Arzttermin hatte. Ein Arzttermin sollte keinen Abzug im Lohn der Arbeitskraft verursachen. Daher in diesem Fall kann der Supervisor die zwei Stunden der Abwesenheit von 8 bis auf 10 am Morgen regulieren, indem er manuell einem Abwesenheitscode eingibt, und Krankheit für diese zwei Stunden angibt.

### <a name="calculate-and-approve-absence"></a>Berechnen und Genehmigen von Abwesenheit

- Wählen Sie **Zeitanwesenheit** &gt; **Prüfen und Genehmigen** &gt; **Genehmigen oder Berechnen Sie** aus.

