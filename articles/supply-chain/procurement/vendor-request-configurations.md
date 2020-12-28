---
title: Konfigurationen für Kreditorenanforderungen
description: In diesem Thema werden die Felder beschrieben, deren Auffüllung in einer neuen Kreditorenanforderung erforderlich ist.
author: mkirknel
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendProspectiveVendorRegistrationConfig
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: d78aa7c14ed2a2a5097f6f80c946c6ae4ed8bb94
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428917"
---
# <a name="vendor-request-configurations"></a>Konfigurationen für Kreditorenanforderungen
[!include [banner](../includes/banner.md)]

Um eine Kreditorenanforderung abzuschließen, muss eine Kontaktperson des Kreditors den Registrierungs-Assistenten des künftigen Kreditors abschließen.

Im Formular **Kreditorenanforderungskonfigurationen** können Sie Profile erstellen, die erforderliche Felder und sichtbare Felder im Registrierungs-Assistenten des künftigen Kreditors angeben.

Der Kreditorenregistrierungs-Assistent beginnt, indem er den künftigen Kreditorbenutzer fragt, in welchem Land/Region der Kreditor geschäftliche tätig ist. Diese Information bestimmt die anzuwendende Konfiguration. Wenn keine bestimmte Konfiguration für ein Land/eine Region definiert wird, wird eine Standardkonfiguration verwendet.

### <a name="set-up-a-vendor-request-configuration"></a>Eine Kreditorenanforderungskonfiguration einrichten

Standardmäßig ist eine Kreditorenkonfiguration im Kreditorenanforderungskonfigurationsformular verfügbar.

Es ist nicht möglich, Länder/Regionen für die Standardkonfiguration auszuwählen, somit kann der Abschnitt **Länder/Regionen** nicht geändert werden.

1. Klicken Sie auf **Beschaffung** > **Einstellungen** > **Kreditoren**, und klicken Sie dann auf **Kreditorenanforderungskonfiguration**.
2. Klicken Sie auf die Registerkarte **Felder**, um den Status der aufgeführten Felder festzulegen.
3. Ausgeblendet (Nicht sichtbar)
4. Angezeigt (Sichtbar, aber nicht obligatorisch)
5. Erorderlich (Sichbar und obligatorisch)
6. Klicken Sie auf die Registerkarte **Inhalt**, um anzugeben, ob Text im Assistenten angezeigt wird und ob es eine Bestätigung geben soll, dass der künftige Kreditorenbenutzer diesen bestätigen muss, bevor er zum nächsten Schritt im Assistenten wechselt. Die Bestätigung wird für alle Bedingungen angefordert, die der Benutzer akzeptieren muss, um den Vorgang fortzusetzen.

Sie können auch eine Bestätigungsmeldung eingeben, die angezeigt wird, wenn der Assistent abgeschlossen ist, und Sie können einen oder mehrere Fragebögen hinzufügen.

### <a name="create-a-vendor-configuration-for-a-specific-countryregion"></a>Erstellen einer Kreditorenkonfiguration für ein bestimmtes Land/Region
1.  Klicken Sie auf **Beschaffung** > **Einstellungen** > **Kreditoren**, und klicken Sie dann auf **Kreditorenanforderungskonfiguration**.
2.  Klicken Sie auf **Neu**, um eine neue Konfiguration zu erstellen, und geben Sie einen Namen für die Konfiguration an.
3.  Klicken Sie auf **Speichern**.
4.  Öffnen Sie die Registerkarte **Land/Regionen**, um das Land/die Region auszuwählen, für das/die die Konfiguration verwendet werden soll.
5.  Schließen Sie die Konfiguration ab, indem Sie die für Richtlinien die Standardkonfiguration befolgen.

