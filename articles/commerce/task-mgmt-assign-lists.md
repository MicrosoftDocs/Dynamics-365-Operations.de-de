---
title: Aufgabenlisten zu Filialen oder Mitarbeitern zuordnen
description: In diesem Thema wird beschrieben, wie Sie den Filialen oder Mitarbeitern in Microsoft Dynamics 365 Commerce Aufgabenlisten zuweisen.
author: gvrmohanreddy
manager: annbe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: ee924f5bf95d47814e7ca09b392a3d10b5e9b9dc
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006259"
---
# <a name="assign-task-lists-to-stores-or-employees"></a>Aufgabenlisten zu Filialen oder Mitarbeitern zuordnen

[!include [banner](includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie den Filialen oder Mitarbeitern in Microsoft Dynamics 365 Commerce Aufgabenlisten zuweisen.

## <a name="overview"></a>Übersicht

Mit der Aufgabenverwaltung in Dynamics 365 Commerce können Sie eine Aufgabenliste mehreren Filialen oder Mitarbeitern oder einer Kombination aus Filialen und Mitarbeitern zuweisen. Beispielsweise könnte ein Regionalmanager für 20 Filialen allen 20 Filialen die Aufgabenliste **Feiertagssaisonvorbereitung** zuweisen wollen.

## <a name="start-the-task-list-assignment-process"></a>Starten Sie den Prozess der Aufgabenlistenzuweisung

Um den Prozess der Zuweisung eines Aufgabenplans zu beginnen, führen Sie die folgenden Schritte aus.

1. Gehen Sie zu **Retail and Commerce \> Aufgabenverwaltung \> Aufgabenverwaltung Verwaltung**.
1. Wählen Sie die Aufgabenliste, die Sie zuweisen möchten.
1. Wählen Sie **Prozess starten**.
1. Geben Sie im Dialogfeld **Prozess starten** auf der Registerkarte **Allgemein** im Feld **Prozessname** einen Namen ein (z.B. **Ostliche Region speichert**).
1. Geben Sie im Feld **Zieldatum** ein Datum ein.
1. Um die Aufgabenliste den Filialen zuzuordnen, verwenden Sie auf der Registerkarte **Filialen** den Filter **Organisationshierarchie**, um die Filialen zu finden und auszuwählen.

    Um die Aufgabenliste den Mitarbeitern zuzuordnen, suchen und wählen Sie auf der Registerkarte **Arbeiter** die Mitarbeiter aus.

1. Wählen Sie **OK**, um den Prozess zu starten. Die Aufgabenliste wird den ausgewählten Filialen oder Mitarbeitern zugeordnet.

Die folgende Abbildung zeigt ein Beispiel für die Suche und Auswahl von Filialen im Dialogfenster **Prozess starten**.

![Suchen und Auswählen von Filialen im Dialogfeld „Prozess starten“.](media/HQ-Assign-Tasks-Lists.png)

## <a name="assign-task-lists-on-a-recurring-basis"></a>Aufgabenlisten auf wiederkehrender Basis zuweisen

Einzelhändler haben manchmal wiederkehrende Aufgaben, wie z.B. „Checkliste für den Donnerstagabschluss“ oder „Checkliste für den ersten Tag des Monats“. Daher möchten sie die Aufgabenliste möglicherweise auf einer wiederkehrenden Basis zuweisen.

1. Gehen Sie zu **Retail and Commerce \> Aufgabenverwaltung \> Aufgabenverwaltung Verwaltung**.
1. Wählen Sie die Aufgabenliste, die Sie zuweisen möchten.
1. Wählen Sie **Prozess starten**.
1. Geben Sie im Dialogfenster **Prozess starten** auf der Registerkarte **Allgemein** im Feld **Prozessname** einen Namen ein.
1. Setzen Sie die Option **Wiederholung** auf **Ja**.
1. Geben Sie im Feld **Wiederholungszieldatumverschiebung in Tagen** eine Anzahl von Tagen ein. Wenn Sie z.B. **4** eingeben, ist das Zieldatum das Wiederholungsdatum plus vier Tage.
1. Wählen Sie auf der Registerkarte **Im Hintergrund ausführen** **Wiederholung**.
1. Geben Sie im Dialogfenster **Wiederholung definieren** die Häufigkeitskriterien ein und wählen Sie **OK**.

Die folgende Abbildung zeigt ein Beispiel für die Eingabe von Häufigkeitskriterien im Dialogfenster **Rezidivierung definieren**.

![Eingabe von Häufigkeitskriterien im Dialogfenster Rekursion definieren](media/HQ-Assign-Tasks-Lists-Recurrently.png)

## <a name="track-task-list-status"></a>Verfolgen Sie den Status der Aufgabenliste

Wenn Sie ein Regionalleiter oder Filialleiter sind, möchten Sie vielleicht den Status von Aufgabenlisten verfolgen, die mehreren Filialen oder Mitarbeitern zugeordnet wurden. Sie können dann die Filialen oder Mitarbeiter nachverfolgen, die die ihnen zugewiesenen Aufgaben nicht rechtzeitig erledigt haben. Im Backoffice des Handels können Sie den Status von Aufgabenlisten anzeigen, Aufgaben neu zuweisen oder den Status einer Aufgabe ändern.

Um den Aufgabenlistenstatus für alle Aufgaben zu verfolgen, führen Sie die folgenden Schritte aus.

1. Gehen Sie zu **Retail and Commerce \> Aufgabenverwaltung \> Aufgabenverwaltungsprozesse**.
1. Wählen Sie die Registerkarte **Alle Aufgabenlisten**, um den Status aller Aufgabenlisten anzuzeigen, die verschiedenen Geschäften zugeordnet sind.

Um den Aufgabenlistenstatus für alle Ihnen zugewiesenen Aufgaben zu verfolgen, führen Sie die folgenden Schritte aus.

1. Gehen Sie zu **Retail and Commerce \> Aufgabenverwaltung \> Aufgabenverwaltungsprozesse**.
1. Wählen Sie die Registerkarte **Meine Aufgaben** oder **Alle Aufgaben**, um den Status der Ihnen zugewiesenen Aufgaben anzuzeigen oder zu aktualisieren.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Übersicht über die Aufgabenverwaltung](task-mgmt-overview.md)

[Aufgabenverwaltung konfigurieren](task-mgmt-configure.md)

[Aufgabenlisten erstellen und Aufgaben hinzufügen](task-mgmt-create-lists.md)

[Aufgabenverwaltung in POS](task-mgmt-POS.md)
