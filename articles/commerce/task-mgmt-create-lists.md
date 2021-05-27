---
title: Aufgabenlisten erstellen und Aufgaben hinzufügen
description: Dieses Thema beschreibt, wie Sie Aufgabenlisten erstellen und Aufgaben in Microsoft Dynamics 365 Commerce hinzufügen können.
author: gvrmohanreddy
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: f3fcfae9f4ab458b4f14f18859f22fc25bf98623
ms.sourcegitcommit: cabd991fda2bfcabb55db84c225b24a7bb061631
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6027623"
---
# <a name="create-task-lists-and-add-tasks"></a>Aufgabenlisten erstellen und Aufgaben hinzufügen

[!include [banner](includes/banner.md)]

Dieses Thema beschreibt, wie Sie Aufgabenlisten erstellen und Aufgaben in Microsoft Dynamics 365 Commerce hinzufügen können.

Eine *Aufgabe* definiert eine bestimmte Arbeit oder eine Aktion, die jemand an oder vor einem bestimmten Fälligkeitsdatum erledigen muss. In Dynamics 365 Commerce kann eine Aufgabe detaillierte Anweisungen und Informationen über eine Kontaktperson enthalten. Sie kann auch Links zu Back-Office-Vorgängen, POS-Vorgängen oder Seiten der Website enthalten, um die Produktivität zu verbessern und den Kontext zu schaffen, den der Aufgabeninhaber zur effizienten Erledigung der Aufgabe benötigt.

Eine *Aufgabenliste* ist eine Sammlung von Aufgaben, die als Teil eines Geschäftsprozesses erledigt werden müssen. Zum Beispiel könnte es eine Aufgabenliste geben, die ein neuer Mitarbeiter während der Einarbeitung erledigen muss, eine Aufgabenliste für Kassierer, die in Abendschichten arbeiten, oder eine Aufgabenliste, die zur Vorbereitung des Geschäfts auf eine bevorstehende Urlaubssaison erledigt werden muss. Im Handel kann jede Aufgabenliste, die ein Zieldatum hat, einer beliebigen Anzahl von Filialen oder Mitarbeitern zugeordnet werden, und sie kann so konfiguriert werden, dass sie sich wiederholt.

Sowohl Manager als auch Mitarbeiter können im Backoffice des Bereichs Handel Aufgabenlisten erstellen und sie dann einer Reihe von Filialen zuordnen.

## <a name="create-a-task-list"></a>Erstellen Sie eine Aufgabenliste

Um einen Aufgabenplan zu erstellen, führen Sie folgende Schritte aus.

1. Gehen Sie zu **Retail and Commerce \> Aufgabenverwaltung \> Aufgabenverwaltung Verwaltung**.
1. Wählen Sie **Neu**, und geben Sie dann Werte in die Felder **Name**, **Beschreibung** und **Besitzer** ein.
1. Wählen Sie **Speichern**.

## <a name="add-tasks-to-a-task-list"></a>Aufgaben zu einer Aufgabenliste hinzufügen

Um einer Aufgabenliste Aufgaben hinzuzufügen, gehen Sie wie folgt vor.
 
1. Wählen Sie auf der Registerkarte **Aufgaben** einer bestehenden Aufgabenliste **Neu**, um eine Aufgabe hinzuzufügen.
1. Geben Sie im Dialogfeld **Neue Aufgabe erstellen** im Feld **Name** einen Namen für die Aufgabe ein.
1. Geben Sie in das Feld **Datenversatz vom Zieldatum** einen positiven oder negativen ganzzahligen Wert ein. Geben Sie z.B. **-2** ein, wenn die Aufgabe zwei Tage vor dem Fälligkeitsdatum der Aufgabenliste abgeschlossen sein soll.
1. Geben Sie in das Feld **Hinweise** detaillierte Anweisungen ein.
1. Geben Sie in das Feld **Ansprechpartner** den Namen eines Fachexperten ein, an den sich der Aufgabeninhaber wenden kann, wenn er Hilfe benötigt.
1. Geben Sie im Feld **Aufgabenverknüpfung** eine Verknüpfung ein, die auf der Art der Aufgabe basiert.

> [!TIP]
> Obwohl Sie das Feld **Zugeordnet zu** verwenden können, um jemandem Aufgaben zuzuweisen, während Sie eine Aufgabenliste erstellen, empfehlen wir Ihnen, die Zuweisung von Aufgaben während der Erstellung der Aufgabenliste zu vermeiden. Ordnen Sie stattdessen die Aufgaben nach der Instanziierung der Liste für einzelne Filialen zu.

## <a name="use-task-links-to-help-improve-worker-productivity"></a>Verwenden Sie Aufgabenverknüpfungen, um die Produktivität der Mitarbeiter zu verbessern.

Im Bereich Handel können Sie Aufgaben mit bestimmten POS-Operationen verknüpfen, z. B. die Ausführung eines Verkaufsberichts, die Anzeige eines Online-Schulungsvideos zur Orientierung neuer Mitarbeiter oder die Durchführung einer Back-Office-Operation. Diese Funktion hilft den Aufgabeninhabern, die Informationen zu erhalten, die sie zur effizienten Erledigung einer Aufgabe benötigen.

Um Aufgabenverknüpfungen während der Erstellung einer Aufgabe hinzuzufügen, gehen Sie wie folgt vor.

1. Wählen Sie auf der Registerkarte **Aufgaben** einer vorhandenen Aufgabenliste **Bearbeiten**.
1. Wählen Sie im Dialogfeld **Aufgabe bearbeiten** im Feld **Aufgabenverknüpfung** eine oder mehrere der folgenden Optionen:

    - Wählen Sie **Menüpunkt**, um einen Back-Office-Vorgang zu konfigurieren, z.B. „Produkt-Kits“.
    - Wählen Sie **POS-Operation**, um eine POS-Operation zu konfigurieren, wie z.B. „Verkaufsberichte“.
    - Wählen Sie **URL**, um eine absolute URL zu konfigurieren.

Die folgende Abbildung zeigt die Auswahl der Aufgabenverknüpfungen im Dialogfenster **Aufgabe bearbeiten**.

![Auswahl der Aufgabenverknüpfungen im Dialogfeld „Aufgabe bearbeiten“.](media/HQ-POS-Tasks-Linking.png)

### <a name="configure-a-pos-operation-so-that-it-can-be-linked-to-a-task"></a>Konfigurieren Sie eine POS-Operation so, dass sie mit einer Aufgabe verknüpft werden kann

Um einen POS-Vorgang so zu konfigurieren, dass er mit einer Aufgabe verknüpft werden kann, gehen Sie wie folgt vor.

1. Gehen Sie zu **Einzelhandel und Handel \> Kanaleinstellung \> POS-Einrichtung \> POS \> POS-Operationen**.
1. Wählen Sie **Bearbeiten**, suchen Sie die POS-Operation und markieren Sie dann das Kontrollkästchen **Aufgabenverwaltung aktivieren** für diese Operation.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Übersicht über die Aufgabenverwaltung](task-mgmt-overview.md)

[Aufgabenverwaltung konfigurieren](task-mgmt-configure.md)

[Arbeitspläne den Filialen oder Mitarbeitern zuweisen](task-mgmt-assign-lists.md)

[Aufgabenverwaltung in POS](task-mgmt-POS.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
