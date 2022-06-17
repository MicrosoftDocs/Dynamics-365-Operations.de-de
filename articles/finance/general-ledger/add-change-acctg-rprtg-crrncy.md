---
title: Buchhaltungs- oder Berichtswährung ändern
description: In diesem Artikel wird erläutert, wie Sie die Buchhaltungs- oder Berichtswährung ändern oder der Einrichtung eines Sachkontos eine Berichtswährung hinzufügen.
author: kweekley
ms.date: 05/05/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-05-05
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: b02432c8e0bdf52c2a588f67a581b78e682b1bf8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904613"
---
# <a name="change-the-accounting-or-reporting-currency"></a>Buchhaltungs- oder Berichtswährung ändern

[!include [banner](../includes/banner.md)]

In diesem Artikel wird erläutert, wie Sie die Buchhaltungs- oder Berichtswährung ändern oder der Einrichtung eines Sachkontos eine Berichtswährung hinzufügen.

## <a name="symptom"></a>Symptom

Sie möchten die Buchhaltungs- oder Berichtswährung ändern oder der Einrichtung eines Sachkontos eine Berichtswährung hinzufügen. Dies tritt normalerweise in den folgenden Szenarien auf:

- Bei der Einrichtung einer juristischen Person wurde die falsche Buchhaltungs- oder Berichtswährung angegeben. Sie möchten diese Währung jetzt ändern.
- Bei der Einrichtung einer juristischen Person wurde eine Berichtswährung angegeben, aber die Organisation möchte die Berichtswährung jetzt entfernen.
- Die Organisation aktualisiert auf oder migriert zu Microsoft Dynamics 365 Finance und möchte die Buchhaltungs- oder Berichtswährung ändern.

Eine Organisation, die die Funktion „Doppelte Währung“ zuvor nicht verwendet hat, möchte sie jetzt nutzen. Dieses Problem tritt normalerweise in den folgenden Szenarien auf.

- Bei der Einrichtung einer juristischen Person wurde keine Berichtswährung angegeben. (Eine Berichtswährung ist optional.) Sie möchten jetzt eine Berichtswährung hinzufügen.

## <a name="resolution"></a>Lösung

Die wichtigste Überlegung ist, ob Buchungen (tatsächliche oder budgetierte) in der juristischen Person für die Einrichtung des Sachkontos gebucht wurden. **Sie können die Buchhaltungs- oder Berichtswährung nicht ändern oder eine Berichtswährung hinzufügen, wenn Buchungen (tatsächliche oder budgetierte) in der juristischen Person gebucht wurden.** Befolgen Sie die Schritte in einem der folgenden Abschnitte, je nachdem, ob Buchungen gebucht wurden.

### <a name="no-transactions-have-been-posted"></a>Es wurden keine Buchungen gebucht

1. Gehen Sie in der juristischen Person, für die Sie Währungen aktualisieren, zu **Hauptbuch \> Einrichten des Hauptbuchs \> Sachkonto**.
2. Wählen Sie auf der Seite **Sachkonto** die Option **Bearbeiten** aus.
3. Wählen Sie auf dem Inforegister **Währung** die Buchhaltungs- und Berichtswährung aus, die für die juristische Person verwendet werden soll.
4. Wählen Sie **Speichern** aus.

Wenn die Felder für die Buchhaltungswährung und die Berichtswährung auf der Seite **Sachkonto** nicht verfügbar sind, wurde mindestens eine Buchung (tatsächliche oder budgetierte) in der juristischen Person gebucht. Daher können die Währungen nicht geändert werden. Befolgen Sie in diesem Fall die Schritte im nächsten Abschnitt.

### <a name="transactions-have-been-posted"></a>Buchungen wurden gebucht

**Wenn Buchungen in der juristischen Person gebucht wurden, besteht die einzige Möglichkeit, Buchhaltungs- und Berichtswährungen zu ändern oder hinzuzufügen, darin, eine neue juristische Person mit den richtigen Währungen zu erstellen.** Um diesen Prozess zu vereinfachen, können Sie mit der Datenverwaltung im System Einrichtungs- und Masterdatensätze aus der aktuellen juristischen Person in eine neue juristische Person kopieren.

Die Änderungen an den Buchhaltungs- und Berichtswährungen sind tiefgreifend. Sie betreffen nicht nur das Hauptbuch, sondern auch alle untergeordneten Sachkonten (Debitorenbuchhaltung, Kreditorenbuchhaltung, Lagerbestand, Projekt usw.), alle unabhängigen Softwareanbieterlösungen (ISVs) und alle vorgenommenen Erweiterungen, um Beträge zu speichern.

Die Suche und Umrechnung der einzelnen Beträge in eine andere Währung ist fehlerbehaftet. Daher wird das Technikteam kein Skript genehmigen, mit dem Buchhaltungs- und Berichtswährungen geändert oder hinzugefügt werden. Es gab zwar früher ein verfügbares Tool für Microsoft Dynamics AX 2012, mit dem Sie Buchhaltungs- und Berichtswährungen ändern oder hinzufügen konnten. Dieses Tool wurde jedoch für AX 2012 R3 und Finance außer Kraft gesetzt.

Befolgen Sie diese Schritte, um die Einrichtungs- und Masterdaten aus der aktuellen juristischen Person in eine neue juristische Person zu kopieren.

1. Wechseln Sie zu **Arbeitsbereiche \> Datenverwaltung**.
2. Wählen Sie unter der Gruppe **Importieren/Exportieren** die Option **Vorlagen** aus.
3. Stellen Sie sicher, dass Vorlagen verfügbar sind. Wenn keine Vorlagen verfügbar sind, wählen Sie **Standardvorlagen laden** aus, und warten Sie, bis die Vorlagen generiert wurden.
4. Wechseln Sie zurück zum Arbeitsbereich **Datenverwaltung**.
5. Wählen Sie **In juristische Person kopieren** aus.
6. Geben Sie einen Namen für die Gruppe und eine Beschreibung ein.
7. Wählen Sie im Feld **Juristische Person der Quelle** die juristische Person aus, von der Daten kopiert werden sollen.
8. Wählen Sie auf dem Inforegister **Juristische Person des Ziels** die Option **Juristische Personen erstellen** aus, um eine neue juristische Person zu erstellen, in die Sie die Quelldaten der juristischen Person kopieren können. Wählen Sie **Vorhandene auswählen** aus, um Daten in eine bestehende juristische Person zu kopieren.
9. Optional: Legen Sie das Feld **Nummernkreise kopieren** auf **Ja** fest. (Dieser Schritt wird empfohlen, wenn Sie Daten kopieren.)
10. Wählen Sie im Bereich **Ausgewählte Entitäten** die Option **Vorlage hinzufügen** aus.
11. Wählen Sie die zu verwendenden Vorlagen aus. Vorgeschlagene Vorlagen für eine neue juristische Person lauten: **025 – Hauptbuch** und **Finanzen**. Wir empfehlen Ihnen, auch alle anderen verfügbaren Vorlagen zu prüfen, um festzustellen, ob eine davon Ihren Anforderungen entspricht.
12. Wählen Sie **In juristische Person kopieren** aus, um einen Stapelverarbeitungsvorgang zu starten, bei dem die ausgewählten Entitäten erstellt und in die juristische Zielentität kopiert werden.
13. Wechseln Sie nach Abschluss des Vorgangs, jedoch bevor eine Buchung gebucht wird, zum Hauptbuch, und aktualisieren Sie die Buchhaltungs- und Berichtswährungen, wie weiter oben in diesem Artikel beschrieben.

Wenn Sie eine neue juristische Person erstellt haben, damit Sie die Buchhaltungs- oder Berichtswährung ändern können, stellen Sie sicher, dass die Anfangssalden von den Währungen der früheren juristischen Person in die neuen Währungen umgerechnet werden.

Ein Video mit den vorhergehenden Schritten finden Sie unter [In juristische Person kopieren](https://community.dynamics.com/365/b/techtalks/posts/copy-into-legal-entity-october-24-2017).
