---
title: Adressänderungen anzeigen und verwalten
description: In diesem Thema wird erläutert, wie Sie Adressänderungen in Dynamics 365 Human Resources anzeigen und verwalten können.
author: andreabichsel
manager: AnnBe
ms.date: 08/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-08-07
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: a69d723b45e834b022491c8eaf2a7fb580e54f1d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4418620"
---
# <a name="view-and-manage-address-changes"></a>Adressänderungen anzeigen und verwalten

In diesem Thema wird erläutert, wie Sie Adressänderungen auf der Mitarbeiter-Self-Service-Seite **Persönliche Daten bearbeiten** oder der Detailseite **Arbeitskraft** in Dynamics 365 Human Resources anzeigen und verwalten können.

Viele Unternehmen möchten, dass Mitarbeiter ihre persönlichen Daten über einen Self-Service verwalten. Sie können Benutzern erlauben, ihre Adresse im Arbeitsbereich **Mitarbeiter-Self-Service** zu aktualisieren. Sie können diese Änderungen dann im Arbeitsbereich **Personalverwaltung** überwachen. Sie müssen die Anzahl der Tage angeben, an denen Sie Änderungen auf der Seite **Personalverwaltungsparameter** anzeigen möchten, um diese Funktion nutzen zu können.

## <a name="configure-address-change-parameters"></a>Adressänderungsparameter konfigurieren

Führen Sie die folgenden Schritte aus, um die Anzahl der Tage, an denen Adressänderungen im Arbeitsbereich **Personalverwaltung** konfiguriert werden sollen, zu konfigurieren:

1. Wählen Sie im Navigationsbereich **Personalverwaltung** aus.

2. Wählen Sie **Links** aus.

3. Wählen Sie **Personalverwaltungsparameter** aus.

4. Geben Sie im Feld **Anzahl der Tage** unter **Adressänderung** die Anzahl der Tage ein, an denen Adressänderungen im Arbeitsbereich **Personalverwaltung** angezeigt werden sollen.

5. Schließen Sie die Seite.

## <a name="create-or-change-an-employee-address"></a>Eine Mitarbeiteradresse erstellen oder ändern

Mitarbeiter können ihre eigene Adresse im Arbeitsbereich **Mitarbeiter-Self-Service** aktualisieren. Gehen Sie folgendermaßen vor, um eine Adresse zu erstellen oder zu ändern:

1. Wählen Sie auf Ihrer Startseite die Kachel **Mitarbeiter-Self-Service** aus.

2. Wählen Sie **Persönliche Daten bearbeiten** aus.

3. Wählen Sie **Hinzufügen** aus, um eine Adresse hinzuzufügen. Um eine vorhandene Adresse zu aktualisieren, wählen Sie die Adresse aus der Liste aus, und klicken Sie dann auf **Bearbeiten**.

4. Geben Sie den **Namen oder die Beschreibung** ein.

5. Wählen Sie das Dropdownfeld **Zweck** und dann den Adresstyp aus.

6. Füllen Sie **Land/Region** aus.

7. Geben Sie die **Postleitzahl** ein.

8. Geben Sie die **Straße** ein.

9. Geben Sie die **Stadt**, den **Staat** und den **Bezirk** ein. In der Regel werden diese Felder automatisch basierend auf dem Feld **Postleitzahl** ausgefüllt.

10. Wählen Sie optional das Feld **Primär** aus, um anzugeben, dass es sich um eine primäre Adresse handelt. Es kann nur eine Adresse als primäre Adresse markiert werden. Wenn bereits eine andere Adresse als primäre Adresse markiert ist, müssen Sie bestätigen, dass Sie diese Adresse als primäre Adresse verwenden möchten.

11. Wählen Sie optional das Feld **Privat** aus, um anzugeben, dass es sich um eine private Adresse handelt. Nur Benutzer mit ausdrücklicher Berechtigung zum Anzeigen privater Adressinformationen können diese Adresse anzeigen.

12. Wählen Sie **OK**.

## <a name="create-or-change-a-worker-address"></a>Eine Arbeitskraftadresse erstellen oder ändern

Sie können eine Adresse im Arbeitsbereich **Personalverwaltung** aktualisieren. Gehen Sie folgendermaßen vor, um eine Adresse zu erstellen oder zu ändern:

1. Wählen Sie im Arbeitsbereich **Personalverwaltung** **Links** und dann **Arbeitskräfte** aus.

3. Wählen Sie die Arbeitskraft aus, und klicken Sie anschließend auf **Adressen**.

3. Wählen Sie **Hinzufügen** aus, um eine Adresse hinzuzufügen. Um eine vorhandene Adresse zu aktualisieren, wählen Sie die Adresse aus der Liste aus, und klicken Sie dann auf **Bearbeiten**.

4. Geben Sie den **Namen oder die Beschreibung** ein.

5. Wählen Sie das Dropdownfeld **Zweck** und dann den Adresstyp aus.

6. Füllen Sie **Land/Region** aus.

7. Geben Sie die **Postleitzahl** ein.

8. Geben Sie die **Straße** ein.

9. Geben Sie die **Stadt**, den **Staat** und den **Bezirk** ein. In der Regel werden diese Felder automatisch basierend auf dem Feld **Postleitzahl** ausgefüllt.

10. Wählen Sie optional das Feld **Primär** aus, um anzugeben, dass es sich um eine primäre Adresse handelt. Es kann nur eine Adresse als primäre Adresse markiert werden. Wenn bereits eine andere Adresse als primäre Adresse markiert ist, müssen Sie bestätigen, dass Sie diese Adresse als primäre Adresse verwenden möchten.

11. Wählen Sie optional das Feld **Privat** aus, um anzugeben, dass es sich um eine private Adresse handelt. Nur Benutzer mit ausdrücklicher Berechtigung zum Anzeigen privater Adressinformationen können diese Adresse anzeigen.

12. Wählen Sie **OK**.
 
## <a name="create-a-future-change-for-an-address"></a>Eine zukünftige Änderung für eine Adresse erstellen

In einigen Fällen möchten Sie möglicherweise eine Adresse aktualisieren, um sie in Zukunft zu ändern. Dies wäre beispielsweise nützlich, wenn ein Mitarbeiter am 15. des folgenden Monats umzieht.

1. Öffnen Sie die Seite **Adressen verwalten**, indem Sie **Weitere Optionen > Erweitert** aus einem beliebigen Adressraster auswählen.

2. Wählen Sie **Neu** aus, um eine neue Adresse zu erstellen.

3. Geben Sie die Details der Adresse ein.

4. Wählen Sie das Inforegister **Allgemein** aus.

5. Wählen Sie im Feld **Gültigkeitsdatum** das Datum aus, an dem die neue Adresse wirksam werden soll.

6. Wählen Sie im Feld **Ablaufdatum** optional aus, wann die Adresse nicht mehr aktuell sein wird.

7. Schließen Sie die Seiten.

## <a name="view-and-monitor-address-changes"></a>Adressänderungen anzeigen und überwachen

HR-Mitarbeiter können Adressänderungen über den Arbeitsbereich **Personalverwaltung** anzeigen und überwachen. Öffnen Sie die Kachel **Personalverwaltung** auf der Seite **Home**, um die Adressänderungen anzuzeigen. Die Adressänderungen werden auf einer Kachel in der oberen rechten Ecke angezeigt. Die Nummer über **Adressänderungen** zeigt an, wie viele Adressänderungen in der in der angegebenen Anzahl von Tagen auf der Seite **Personalverwaltungsparameter** vorgenommen wurden. 

Wenn Sie die Kachel **Adressänderungen** auswählen, werden auf einer neuen Seite die Details aller Adressänderungen angezeigt. Sie können optional **Zukünftige Adressänderungen einschließen** in der oberen rechten Ecke auswählen, um Adressänderungen mit einem Datum in der Zukunft anzuzeigen.

> [!NOTE]
> Wenn Sie eine Warnung oder E-Mail über diese Adressänderungen erhalten möchten, können Sie eine neue Warnregel auf der Registerkarte **Optionen** im Aktionsbereich erstellen. Weitere Informationen zum Erstellen von Warnregeln finden Sie unter [Warnregeln erstellen](/fin-ops-core/fin-ops/get-started/create-alert-rules.md).<br><br>

> Wenn Sie einen Workflow für die Adressänderungen konfigurieren möchten, können Sie die auswählen Option **Extern senden** für Ihre Warnregel auswählen und dann Power Automate verwenden, um das Geschäftsereignis auszulösen und einen Workflow zu konfigurieren. Weitere Informationen finden Sie unter [Warnungen als Geschäftsereignisse](/fin-ops-core/dev-itpro/business-events/alerts-business-events.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]