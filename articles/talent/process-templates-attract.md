---
title: Erstellen einer Prozessvorlage in Attract
description: "Dieses Thema enthält informationabout, wie eine Prozeßvorlage in Attract erstellt wird."
author: hasrivas
manager: AnnBe
ms.date: 10/15/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Talent
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: hasrivas
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: AX 8.1
ms.translationtype: HT
ms.sourcegitcommit: e890e32049e930b70c2d0aac8aa8206ab999418a
ms.openlocfilehash: 54c80f3d785ba7a7e0158c51201468f45796c193
ms.contentlocale: de-de
ms.lasthandoff: 10/22/2018

---

# <a name="create-a-process-template-in-attract"></a>Erstellen einer Prozessvorlage in Attract

[!include [banner](includes/banner.md)]

Eine *Einstellungs-Prozessvorlage* enthält alle Aktivitäten, die im Rahmen des Einrichtungsprozesses für einen Stelle einbezogen werden sollen. In diesem Thema werden die Elemente in einer Prozeßvorlage in Microsoft Dynamics 365 for Talent beschrieben: Attract. Es wird auch erklärt, wie eine Vorlage erstellt wird.

> [!NOTE]
> Vorlagenerstellung ist Teil des umfassenden Add-On für Neueinstellungen für Attract.

## <a name="template-management"></a>Vorlagenverwaltung

Organisationen können entscheiden, ob nur Administratoren oder auch Teammitglieder Prozeßvorlagen  erstellen können. Um die Vorlagenverwaltung zu konfigurieren, wechseln Sie zu **Administrator-Center** \> **Vorlagenverwaltung** Damit Teammitglieder eigene Vorlagen erstellen können, aktivieren Sie die Vorlagenverwaltung. Wenn Sie sie nicht aktivieren, können nur Administratoren Vorlagen erstellen.

## <a name="default-template"></a>Standardvorlage

Nur Administratoren können Standardvorlagen festlegen. Die Standardvorlage wird verwendet, wenn eine Vorlage nicht aktiviert ist, wenn ein Auftrag erstellt wird. Um die Standard-Vorlage zu konfigurieren, wechseln Sie zu **Administrator-Center** \> **Vorlagenverwaltung**. Auf der Karte für die Vorlage, die die Standardvorlage werden soll, markieren Sie die Schaltfläche (**...**) und wählen Sie dann **Als Standard festlegen** aus.

## <a name="create-a-process-template"></a>Erstellen einer Prozessvorlage

Administratoren, Personalverantwortliche und Manager können Prozessvorlagen erstellen. Eine Prozessvorlage besteht aus *Phasen* und *Aktivitäten*. Gruppieren Sie Phasen in eine oder mehrere Aktionen. Standardmäßig hat jede Prozessvorlage Interessenten, Anwendungen und Angebotsaktivitäten. Die Phasen, die diese Aktivitäten enthalten, können umbenannt werden. Sie können mehrere Phasen hinzufügen, indem Sie **+ Neue Phase** auswählen. Sie können Aktivitäten in einer Phase entweder durch ziehen oder doppelklicken einer Aktivitätenliste zuweisen.

> [!NOTE]
> Phasennamen sind für Kandidaten auf der Seite **Bewerbungsstatus** sichtbar. Sie sollten diesen Tatsache berücksichtigen, wenn Sie Namen für Phasen auswählen.

Weitere Informationen über Aktivitäten finden Sie unter [Einstelungsaktivitäten in Attract](./activities-attract.md).

Folgen Sie diesen Schritten, um eine Einstellungsvorlage zu erstellen.

1. Gehen Sie zu **Vorlagen**.
2. Wählen Sie **Neu** aus.
3. Geben Sie im Feld **Vorlagenname** einen Namen für die Vorlage ein, und wählen Sie dann **Erstellen** aus.
4. In der Liste **Wählen Sie den gewünschten Genehmigungsprozess**wählen Sie **Standard**, um die Genehmigung für eine Stelle anzugeben.
5. Wählen Sie aus, um Interessenten zu aktivieren oder zu deaktivieren.
6. Optional: Hinzufügen oder Entfernen von Phasen.

    - Um eine Phase hinzufügen, wählen Sie **+ Neue Phase** aus.
    - Um eine Phase zu entfernen, zeigen Sie mit dem Mauszeiger auf die Phase, und wählen Sie dann die Abfalleimerschaltfläche aus, die angezeigt wird.

        > [!NOTE]
        > Interessenten-, Bewerbungs- und Angebotphasen können nicht entfernt werden, jedoch können sie umbenannt werden.

7. Optional: Hinzufügen oder Entfernen von Aktivitäten.

    - Wenn Sie eine Aktivität hinzufügen möchten, ziehen Sie sie aus der Aktivitätsliste auf der rechten Seite in die entsprechende Phase. Alternativ doppelklicken Sie auf die Aktivität, und wählen Sie dann zum Hinzufügen die aus Phase aus.
    - Um eine Aktion zu entfernen, erweitern Sie sie und wählen Sie dann die Abfalleimerschaltfläche im Feld Aktivitätskopf aus.

8. Wählen Sie **Speichern**.

