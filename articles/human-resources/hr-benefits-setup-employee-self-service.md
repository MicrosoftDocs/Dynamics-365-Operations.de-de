---
title: Mitarbeiter-Self-Service konfigurieren
description: In Microsoft Dynamics 365 Human Resources können Sie Kacheln für die Navigation auf oberster Ebene in Mitarbeiter-Self-Service konfigurieren.
author: twheeloc
ms.date: 12/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: cdc82c23635cc99c37aa770b996d9d2df43f5059
ms.sourcegitcommit: 66d129874635d34a8b29c57762ecf1564e4dc233
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2022
ms.locfileid: "9324637"
---
# <a name="configure-employee-self-service"></a>Mitarbeiter-Self-Service konfigurieren

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In Microsoft Dynamics 365 Human Resources können Sie Kacheln für die Navigation auf oberster Ebene im **Mitarbeiter-Self-Service** konfigurieren. Vorteilsplan-Kacheln führen Benutzer zu Vorteilsplänen, auf die Sie Anrecht haben.

## <a name="set-up-a-benefit-plans-tile"></a>Vorteilsplan-Kachel einrichten

1. Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Einstellung** die Option **Mitarbeiter-Self-Service-Parameter**.

2. Wählen Sie die Registerkarte **Vorteilsplan-Kachel einrichten** und dann **Neu** aus.

3. Geben Sie Werte für die folgenden Felder an.

   | Feld | Description |
   | --- | --- |
   | **Code des Plantyps** | Der Plantyp, der angezeigt wird, wenn diese Kachel in **Self-Service für Leistungen** ausgewählt wird. |
   | **Kachelkennung** | Der eindeutige Bezeichner für die Kachel. |
   | **Beschriftungstext für Kacheln** | Der Text, der für die Kachel in **Self-Service für Leistungen** erscheinen soll. |
   | **Beschreibung** | Eine Beschreibung der Kachel. |
   | **Kachelhintergrundbild** | Die URL des Bildes, das für die Kachel verwendet werden soll (optional). |
   | **Offene Registrierung verfolgen** | Wählen Sie diese Option aus, um den Fortschritt der offenen Registrierung für diesen Plantyp zu verfolgen. Sie haben beispielsweise Pläne erstellt, für die Folgendes gilt: **Plantyp = Sonstiges**. Bei diesen Plänen kann es sich um optionale Pläne handeln, für die Sie den Registrierungsfortschritt nicht verfolgen möchten. Wenn Sie diesen Plantyp nicht auswählen, wird dieser Plantyp beim Verfolgen des Registrierungsfortschritts oder Registrierungsabschlusses auf der Registerkarte **Registrierung öffnen** ignoriert. Diese Einstellung gilt für den Plantyp, der für alle Perioden und juristischen Personen ausgewählt wird. |

4. Wählen Sie **Speichern** aus.

## <a name="set-up-a-flex-credit-plan-tile"></a>Flexguthabenplan-Kachel einrichten

1. Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Einstellung** die Option **Mitarbeiter-Self-Service-Parameter**.

2. Wählen Sie die Registerkarte **Flexguthabenplan-Kachel einrichten** und dann **Neu** aus.

3. Geben Sie Werte für die folgenden Felder an.

   | Feld | Description |
   | --- | --- |
   | **Vergütungsgutschriftenkennung** | Der Flexguthabenprogrammplan, der angezeigt wird, wenn diese Kachel in **Self-Service für Leistungen** ausgewählt wird. |
   | **Kachelkennung** | Der eindeutige Bezeichner für die Kachel. |
   | **Beschriftungstext für Kacheln** | Der Text, der für die Kachel in **Self-Service für Leistungen** erscheinen soll. |
   | **Beschreibung** | Eine Beschreibung der Kachel. |
   | **Kachelhintergrundbild** | Die URL des Bildes, das für die Kachel verwendet werden soll (optional). |
   | **Offene Registrierung verfolgen** | Wählen Sie diese Option aus, um den Fortschritt der offenen Registrierung für diesen Plantyp zu verfolgen. Sie haben beispielsweise Pläne erstellt, für die Folgendes gilt: **Plantyp = Sonstiges**. Bei diesen Plänen kann es sich um optionale Pläne handeln, für die Sie den Registrierungsfortschritt nicht verfolgen möchten. Wenn Sie diesen Plantyp nicht auswählen, wird dieser Plantyp beim Verfolgen des Registrierungsfortschritts oder Registrierungsabschlusses auf der Registerkarte **Registrierung öffnen** ignoriert. Diese Einstellung gilt für den Plantyp, der für alle Perioden und juristischen Personen ausgewählt wird. |

4. Wählen Sie **Speichern** aus.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
