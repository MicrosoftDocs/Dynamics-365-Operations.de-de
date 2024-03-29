---
title: Filialen oder Mitarbeitern Aufgabenlisten zuweisen
description: In diesem Artikel wird beschrieben, wie Sie den Filialen oder Mitarbeitern in Microsoft Dynamics 365 Commerce Aufgabenlisten zuweisen.
author: gvrmohanreddy
ms.date: 11/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.search.industry: ''
ms.openlocfilehash: faff772051738f624b86fd23fb6bf29173e909ea
ms.sourcegitcommit: 9e2e54ff7d15aa51e58309da3eb52366328e199d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2022
ms.locfileid: "9746193"
---
# <a name="assign-task-lists-to-stores-or-employees"></a>Filialen oder Mitarbeitern Aufgabenlisten zuweisen

[!include [banner](includes/banner.md)]

In diesem Artikel wird beschrieben, wie Sie den Filialen oder Mitarbeitern in Microsoft Dynamics 365 Commerce Aufgabenlisten zuweisen.

Mit der Aufgabenverwaltung in Dynamics 365 Commerce können Sie eine Aufgabenliste mehreren Filialen oder Mitarbeitern oder einer Kombination aus Filialen und Mitarbeitern zuweisen. Beispielsweise könnte ein Regionalmanager für 20 Filialen allen 20 Filialen die Aufgabenliste **Feiertagssaisonvorbereitung** zuweisen wollen.

## <a name="start-the-task-list-assignment-process"></a>Starten Sie den Prozess der Aufgabenlistenzuweisung

Bevor Sie mit dem Zuweisen von Aufgaben beginnen, vergewissern Sie sich, dass Sie eine Aufgabenliste erstellt haben, indem Sie den Schritten in Artikel [Erstellen Sie Aufgabenlisten und fügen Sie Aufgaben hinzu](task-mgmt-create-lists.md) folgen. Um den Prozess der Zuweisung eines Aufgabenplans zu beginnen, führen Sie die folgenden Schritte aus.

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

![Eingabe von Häufigkeitskriterien im Dialogfenster „Wiederholung definieren“.](media/HQ-Assign-Tasks-Lists-Recurrently.png)

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
