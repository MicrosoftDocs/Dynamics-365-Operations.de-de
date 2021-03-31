---
title: Leasingbenutzerrollen zuweisen
description: In diesem Thema werden die Sicherheitsrollen beschrieben, die in Anlagenleasing verwendet werden. Außerdem wird erläutert, wie Benutzer diesen Rollen zugewiesen werden.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 09d80e9629b60144665441989d9d63d7f6be3c60
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5207278"
---
# <a name="assign-lease-user-roles"></a>Leasingbenutzerrollen zuweisen

[!include [banner](../includes/banner.md)]

In diesem Thema werden die Sicherheitsrollen beschrieben, die in Anlagenleasing verwendet werden. Außerdem wird erläutert, wie Benutzer diesen Rollen zugewiesen werden.

Drei Benutzerrollen unterscheiden den Zugriff beim Anlagenleasing. Eine Rolle ist für die Aufrechterhaltung von Mietverträgen geeignet, eine für die Anzeige von Mietverträgen und eine für die Erfüllung der Aufgaben eines Mietvertragsbearbeiter. Jede Rolle verfügt über spezifische Berechtigungen für alle Mietvertragsseiten. Mit jeder Rolle können Benutzer Mietverträge entsprechend ihren Aufgaben anzeigen, erstellen, bearbeiten oder löschen.

| Rolle           | Beschreibung |
|----------------|-------------|
| Mietvertrag verwalten | Benutzer in dieser Rolle können Mietverträge hinzufügen, bearbeiten, löschen und anzeigen. Diese Rolle richtet sich an tägliche Benutzer, deren Aufgaben das Erstellen und Buchen monatlicher Journaleinträge sowie das Hinzufügen neuer Mietverträge umfassen. Diese Rolle ermöglicht den Zugriff auf alle Anlagenleasing-Funktionen. |
| Mietvertrag anzeigen     | Benutzer in dieser Rolle können nur Mietvertragsdatensätze und Zeitpläne anzeigen und Berichte ausführen. Sie können keine neuen Mietverträge erstellen, keine vorhandenen Mietverträge bearbeiten und keine Journaleinträge für Mietverträge erstellen. Die Rolle richtet sich an Benutzer, die nur Mietverträge, Leasingpläne und die Transaktionen anzeigen müssen, die für diese Mietverträge ausgeführt werden. |
| Mietvertragssachbearbeiter    | Benutzer in dieser Rolle können nur neue Mietverträge erstellen. Sie können vorhandene Mietverträge nicht bearbeiten oder löschen, keine Leasingpläne anzeigen oder Leasingjournaleinträge buchen. Diese Rolle ist für Benutzer gedacht, die mit Dateneingabe arbeiten. |

Führen Sie die folgenden Schritte aus, um Benutzer den Rollen zuzuweisen, die beim Anlagenleasing verwendet werden.

1. Wechseln Sie zu **Systemverwaltung \> Sicherheit \> Benutzer zu Rollen zuweisen**.
2. Wählen Sie **Mietvertrag verwalten**, **Mietvertragsbearbeiter** oder die **Mietvertrag anzeigen**-Rolle und dann **Benutzer manuell zuweisen/ausschließen**.
3. Wählen Sie den Benutzer aus, der der Rolle zugewiesen werden soll, und wählen Sie dann **Rolle zuweisen**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]