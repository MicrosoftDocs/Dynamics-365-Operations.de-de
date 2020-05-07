---
title: Projektzuschüsse
description: In diesem Thema wird erläutert, wie Sie einen Zuschuss erstellen oder ändern.
author: RadhikaRS
manager: AnnBe
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: f4f7d347dab9f02fc474656e2f4cfba8e374480d
ms.sourcegitcommit: dfef2faf881b2db1bd0f016df36e2b838105312b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2020
ms.locfileid: "3282828"
---
# <a name="project-grants"></a>Projektzuschüsse

[!include [banner](../includes/banner.md)]

Ein Zuschuss stellt eine monetäre Zuwendung für einen bestimmten Zweck oder ein Projekt dar. Die Verwendung von Zuschüssen unterliegt in der Regel Beschränkungen. Unter "Projektverwaltung und Buchhaltung" können Zuschüsse eingegeben und nachverfolgt sowie deren Beziehungen zu Projekten und Projektverträgen definiert werden. So können Sie etwa die folgenden Aufgaben durchführen:

- Zuordnen von Zuschüssen zu Projekten und Finanzierungsquellen, indem Sie Links zu den Seiten **Projekt** und **Projektvertragsdetails** verwenden.
- Eingeben und Nachverfolgen von Änderungen an Zuschüssen bei einem Statuswechsel.
- Eingeben und Nachverfolgen von Kosten, angeforderten Beträgen und vergebenen Beträgen.
- Erstellen von Hauptzuschüssen und Zuordnen von entsprechenden untergeordneten Zuschüssen.

Sie können einen Zuschuss erstellen, indem Sie alle Details in einen neuen Datensatz eingeben, oder Sie können die Details aus einem vorhandenen Zuschuss kopieren und dann überarbeiten.

## <a name="create-a-new-grant"></a>Neuen Zuschuss erstellen

1. Wechseln Sie zu **Projektverwaltung und Buchhaltung** \> **Zuschüsse** \> **Zuschüsse**.
2. Wählen Sie **Neu** \> **Zuschüsse** aus.
3. Geben Sie auf der Seite "Zuschussdetails" im Inforegister **Allgemein** in das Feld **Zuschuss-ID** einen alphanumerischen Bezeichner für den Zuschuss ein.
4. Geben Sie in das Feld **Zuschussname** einen Namen für den Zuschuss ein.
5. Fügen Sie im Feld **Beschreibung** Details zum neuen Zuschuss hinzu.

    Die meisten anderen Felder auf der Seite sind optional und die Informationen können nach Bedarf eingegeben werden.

    In der folgenden Liste werden die Informationen beschrieben, die in jedem Inforegister der Seite "Zuschussdetails" angegeben sind:

    - **Allgemein** – Geben Sie Name, Status, Beschreibung, Zweck und Betrag des Zuschusses ein.
    - **Kontaktdaten** – Geben Sie Details zu Mitarbeitern, zur für die Zuschussverwaltung zuständigen Abteilung sowie zum Zuschussdebitor bzw. der Organisation ein, von der der Zuschuss stammt. Sie können auch angeben, ob Ihre Organisation als Vermittler fungiert, der den Zuschuss entgegennimmt und an einen anderen Empfänger weiterleitet. Wählen Sie **Hinzufügen** aus, um Kontaktdaten wie Telefonnummern und E-Mail-Adressen der Organisation hinzuzufügen, die den Zuschuss vergibt.
    - **Stichtage und Fristen** – Geben Sie die für den Zuschuss und den Zuschussantrag relevanten Datumsangaben ein. Beispiele hierfür sind der Stichtag für den Antrag, das Einreichungsdatum und das Datum, an dem der Zuschuss genehmigt oder abgelehnt wird.
    - **Zugeordnete Projekte und Projektverträge** – In dieses Inforegister können Sie Informationen nur dann eingeben, wenn das Feld **Zuschuss gewähren** im Inforegister **Allgemein** auf **Aktiv**oder **Ausgezeichnet** festgelegt ist. Wählen Sie eine der folgenden Optionen aus, um die zugehörige Aufgabe abzuschließen:

        - **Finanzierungsquelle hinzufügen** – Fügen Sie eine neue Finanzierungsquelle für den Zuschuss hinzu. Sie können dabei entweder alle Details sofort eingeben oder die Standardinformationen übernehmen und diese später ändern.
        - **Projektvertrag hinzufügen** – Fügen Sie Projektvertragsinformationen hinzu oder aktualisieren Sie sie.
        - **Projekt hinzufügen** – Fügen Sie Projektdetails hinzu oder aktualisieren Sie sie.

    - **Einrichtung** – Geben Sie Details zu passenden Fonds ein, falls diese Informationen erforderlich sind. Viele Organisationen, die Zuschüsse vergeben, machen es den Empfängern zur Auflage, einen bestimmten, dem bewilligten Zuschuss entsprechenden Betrag ihrer eigenen Mittel oder Ressourcen aufzuwenden. In das Feld **Kennung für lokales Projekt oder Überwachungskennung** können Sie eine Kennung eingeben, die sich von der Projektkennung unterscheidet.

        > [!NOTE]
        > Wenn ein Teil des Zuschusses an eine andere Organisation vergeben wird, legen Sie die Option **Untergeordneter Geber** auf **Ja** fest. Bei in den Vereinigten Staaten vergebenen Zuschüssen können Sie angeben, ob der Zuschuss von einem Bundesstaat oder vom Bund geregelt wird.

    - **Details zur Inanspruchnahme** – Geben Sie Informationen zur Häufigkeit ein, mit der Zuschussmittel entnommen, abgerechnet oder ausgegeben werden können (oder aktualisieren Sie die Informationen).

## <a name="create-a-new-grant-from-a-copy"></a>Erstellen eines neuen Zuschusses aus einer Kopie

1. Wechseln Sie zu **Projektverwaltung und Buchhaltung** \> **Zuschüsse** \> **Zuschüsse**.
2. Wählen Sie **Neu** \> **Aus Zuschuss kopieren** aus.
3. Geben Sie einen alphanumerischen Bezeichner und einen Namen für den neuen Zuschuss ein und wählen Sie dann **OK** aus.
4. Überprüfen Sie auf der Seite "Zuschussdetails" die Details des kopierten Zuschusses und nehmen Sie alle notwendigen Änderungen vor. Die meisten Felder auf der Seite sind optional.

## <a name="view-or-modify-grant-details"></a>Anzeigen oder Ändern von Zuschussdetails

1. Wechseln Sie zu **Projektverwaltung und Buchhaltung** \> **Zuschüsse** \> **Zuschüsse**.
2. Wählen Sie den Zuschuss aus, der geändert werden soll.
3. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Zuschuss** in der Gruppe **Verwalten** auf **Bearbeiten**.
4. Überprüfen Sie die Zuschussdetails und nehmen Sie alle notwendigen Änderungen vor.
