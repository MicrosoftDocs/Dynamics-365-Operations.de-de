---
title: Geben Sie Fähigkeiten ein
description: Werke und Manager können Fähigkeiten in Dynamics 365 Human Resources eingeben.
author: andreabichsel
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: b24d37292a2e9749fb2fde06b9f03fcd13db0bbe
ms.sourcegitcommit: 48528233e0f02dbd47e96e030254ef65f2bb899e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/20/2021
ms.locfileid: "6076594"
---
# <a name="enter-skills"></a>Geben Sie Fähigkeiten ein

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Sie können Zielqualifikationen oder tatsächliche Qualifikationen für Arbeitskräfte, Bewerber oder Kontakte in Dynamics 365 Human Resources eingeben. Eine Zielqualifikation ist eine Qualifikation, die eine Person plant zu erreichen. Eine tatsächliche Qualifikation ist eine Qualifikation, die eine Person derzeit hat.

## <a name="create-a-workflow-to-auto-approve-skills"></a>Erstellen Sie einen Workflow, um Fähigkeiten automatisch zu genehmigen

Um Fähigkeiten einzugeben, ohne dass eine Genehmigung erforderlich ist, müssen Sie einen Workflow erstellen, um Fähigkeiten automatisch zu genehmigen.

> [!NOTE]
> Von Arbeitskräften eingegebene Fähigkeiten erfordern immer die Zustimmung des Managers. Dieser Workflow genehmigt nur automatisch Fähigkeiten, die von Managern im Namen ihrer Mitarbeiter eingegeben wurden.

1. Wählen Sie im Arbeitsbereich **Personalverwaltung** die Registerkarte **Links** aus.

2. Unter **Einrichtung** wählen Sie **Personalressourcen-Workflows**.

3. Wählen Sie **Neu** aus.

4. In dem Bereich **Workflow erstellen** wählen Sie **Qualifikationen Arbeitskräfte**.

   [![Wählen Sie Workflow für Arbeitskräfte-Qualifikationen aus](media/hr-develop-skills-new-workflow.png)](media/hr-develop-skills-new-workflow.png)

5. In dem Dialog **Diese Datei öffnen?** wählen Sie **Öffnen**. Geben Sie Ihre Anmeldeinformationen ein, wenn Sie dazu aufgefordert werden.

6. Wählen Sie im Workflow-Editor das Workflowelement **Qualifikationen genehmigen** und ziehen Sie es auf den Canvas.

   [![Wählen Sie das Workflowelement Qualifikationen genehmigen aus](media/hr-develop-skills-element.png)](media/hr-develop-skills-element.png)

7. Verbinden Sie das Element **Start** mit dem Element **Qualifikationen genehmigen 1** und verbinden Sie dann das Element **Fähigkeiten genehmigen 1** mit dem Element **Ende**. Möglicherweise müssen Sie nach unten scrollen, um das Element **Ende** zu sehen. Sie können es näher an die anderen Elemente ziehen.

   [![Workflow-Elemente verbinden](media/hr-develop-skills-connect-elements.png)](media/hr-develop-skills-connect-elements.png)

8. Doppelklicken Sie auf das Workflowelement **Qualifikationen 1 genehmigen** und klicken Sie dann mit der rechten Maustaste auf das Element **Schritt 1**. Klicken Sie mit der rechten Maustaste auf das Element **Schritt 1**, und klicken Sie anschließend auf **Eigenschaften**.

9. In dem **Eigenschaften** Fenster wählen Sie **Bedingung** auf der linken Navigationsleiste.

10. Wählen Sie die Option **Diesen Schritt nur ausführen, wenn folgende Bedingungen erfüllt sind**.

11. Wählen Sie **Bedingung hinzufügen**. Nach **Wo** wählen Sie **Self-Service-Fähigkeiten der Mitarbeiter** und dann **Mitarbeiter Self-Service-Fähigkeiten.Person**. Nach **ist** wählen Sie **Feld** und dann **Benutzer-zu-Person-Beziehung.Person**.

    [![Bedingung angeben](media/hr-develop-skills-condition.png)](media/hr-develop-skills-condition.png)

12. Wählen Sie **Zuweisung** auf der linken Navigationsleiste.

13. Auf der Registerkarte **Zuweisungstyp** wählen Sie **Hierarchie**.

14. Auf der Registerkarte **Hierarchieauswahl** im Feld **Hierarchietyp:** wählen Sie **Führungshierarchie** aus.

    [![Geben Sie die Führungshierarchie an](media/hr-develop-skills-hierarchy.png)](media/hr-develop-skills-hierarchy.png)

15. Wählen Sie **Schließen** und wählen Sie **Workflow** im Canvas Breadcrumb, und wählen Sie dann **Speichern und schließen**.

Weitere Informationen über das Erstellen von Workflows finden Sie unter [Workflow-Systemübersicht](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/overview-workflow-system?toc=/dynamics365/human-resources/toc.json).

## <a name="enter-skills-for-a-worker"></a>Geben Sie Fähigkeiten für eine Arbeitskraft ein

1. Hier können Sie eine Arbeitskraft auswählen.

2. In der Aktionsleiste der Seite **Arbeitskraft** wählen Sie **Person** und dann **Qualifikationen**.

3. Auf der Seite **Qualifikationen** füllen Sie die folgenden Felder für jede Fertigkeit aus:

   - **Qualifikation**: Wählen Sie eine Qualifikation aus.
   - **Ebenentyp**: Wählen Sie **Tatsächlich** für eine Qualifikation aus, die die Arbeitskraft bereits hat, oder wählen Sie **Ziel** für eine Qualifikation, auf die die Arbeitskraft hinarbeitet.
   - **Ebene**: Wählen Sie eine Ebene für die Qualifikation der Arbeitskraft aus.
   - **Ebenendatum**: Wählen Sie ein Datum im Kalender aus.
   - **Prüfer**: Wählen Sie gegebenenfalls einen Prüfer aus der Liste aus. Sie können Ihre Suche filtern.
   - **Anzahl Jahre Erfahrung**: Geben Sie Anzahl Jahre für die Erfahrung ein.
   - **Verifiziert**: Wenn die Fähigkeit überprüft wurde, aktivieren Sie das Kontrollkästchen.
   - **Geprüft von**: Geben Sie den Namen des Prüfers ein.

4. Wenn Sie mit der Eingabe von Qualifikationen fertig sind, wählen Sie **speichern**.

## <a name="see-also"></a>Siehe auch

[Fähigkeiten konfigurieren](hr-develop-skills.md)<br>
[Qualifikationen aufzeichnen](hr-develop-map-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]