---
title: Parameter für die Vorteilsverwaltung je Unternehmen konfigurieren
description: Konfigurieren Sie Parameter für die Vorteilsverwaltung je Unternehmen in Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2943d0095e4c9421725b90e579b7cbb841038ab7
ms.sourcegitcommit: fd097f6f76f0d8428038fa3655b3188bf093b517
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "4692744"
---
# <a name="configure-benefits-management-parameters-per-company"></a>Parameter für die Vorteilsverwaltung je Unternehmen konfigurieren

Für jede Organisation, die Vorteile bereitstellt, müssen Sie Einstellungen für E-Mails zur Vorteilsbestätigung konfigurieren.

## <a name="configure-confirmation-email-settings"></a>Einstellungen für Bestätigungs-E-Mail konfigurieren

1. Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Setup** die Option **Personalverwaltungsparameter**.

2. Definieren Sie auf der Registerkarte **Vergütungsverwaltung** die Werte für die folgenden Felder: 

   | Feld | Beschreibung |
   | --- | --- |
   | **Bestätigungs-E-Mail senden** | Wenn diese Funktion aktiviert ist, wird eine Bestätigungs-E-Mail an die Mitarbeiter gesendet, wenn sie sich aus der Umgebung zur Vorteilsregistrierung im Mitarbeiter-Self-Service abmelden. |
   | **E-Mail-Vorlage für Bestätigung** | Wählen Sie die E-Mail-Vorlage der Organisation aus, die beim Senden der Anmeldebestätigung verwendet werden soll. Wenn Sie keine Vorlage auswählen, wird die folgende allgemeine E-Mail gesendet:<br><br>%EmployeeFirstName%,<br><br>herzlichen Glückwunsch! Sie haben sich erfolgreich für Vorteile angemeldet.<br><br>Vielen Dank,<br>Vorteil <Name des Unternehmens/der Organisation>. |
   | **Standard-E-Mail-Adresse des Absenders** | Die E-Mail-Adresse, die beim Senden der Bestätigungs-E-Mail verwendet werden soll. |

3. Wählen Sie **Speichern** aus.