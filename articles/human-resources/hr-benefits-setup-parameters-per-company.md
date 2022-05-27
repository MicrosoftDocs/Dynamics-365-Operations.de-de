---
title: Vorteilsverwaltungsparameter pro Unternehmen konfigurieren
description: In diesem Thema wird beschrieben, wie Sie die Parameter für die Verwaltung der Vorteile pro Firma in Microsoft Dynamics 365 Human Resources konfigurieren.
author: twheeloc
ms.date: 8/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3c5e53d3dec4c6fc8be573b8a1ad3ba8fb01b490
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8689943"
---
# <a name="configure-benefits-management-parameters-per-company"></a>Parameter für die Vorteilsverwaltung je Unternehmen konfigurieren


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Für jede Organisation, die Vorteile bereitstellt, müssen Sie Einstellungen für E-Mails zur Vorteilsbestätigung konfigurieren.

## <a name="configure-confirmation-email-settings"></a>Einstellungen für Bestätigungs-E-Mail konfigurieren

1. Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Setup** die Option **Personalverwaltungsparameter**.

2. Definieren Sie auf der Registerkarte **Vergütungsverwaltung** die Werte für die folgenden Felder: 

   | Feld | Beschreibung |
   | --- | --- |
   | **Bestätigungs-E-Mail senden** | Wenn diese Funktion aktiviert ist, wird eine Bestätigungs-E-Mail an die Mitarbeiter gesendet, wenn sie sich von der Anmeldung für die Vorteile in **Mitarbeiter-Self-Service** abmelden. |
   | **E-Mail-Vorlage für Bestätigung** | Wählen Sie die E-Mail-Vorlage der Organisation aus, die beim Senden der Anmeldebestätigung verwendet werden soll. Wenn Sie keine Vorlage auswählen, wird die folgende allgemeine E-Mail gesendet:<br><br>%EmployeeFirstName%,<br><br>Herzlichen Glückwunsch! Sie haben sich erfolgreich für Vorteile angemeldet.<br><br>Vielen Dank,<br>Vorteil <Name des Unternehmens/der Organisation>. |
   | **Standard-E-Mail-Adresse des Absenders** | Die E-Mail-Adresse, die beim Senden der Bestätigungs-E-Mail verwendet werden soll. |

3. Wählen Sie **Speichern** aus.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
