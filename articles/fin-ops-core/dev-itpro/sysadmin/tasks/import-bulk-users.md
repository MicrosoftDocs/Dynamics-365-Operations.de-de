---
title: Benutzer aus Azure Active Directory importieren
description: Diese Prozedur kann von Systemadministratoren verwendet werden, um ausgewählte Benutzer manuell oder viele Benutzer aus Azure Active Directory zu importieren.
author: peakerbl
manager: AnnBe
ms.date: 07/07/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 56b6666310309817ff30ccb3902721880b829ee0
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679813"
---
# <a name="import-users-from-azure-active-directory"></a>Benutzer aus Azure Active Directory importieren

[!include [banner](../../includes/banner.md)]

## <a name="import-select-users"></a>Ausgewählte Benutzer importieren

Diese Prozedur kann von Systemadministratoren verwendet werden, um ausgewählte Benutzer aus Azure Active Directory (Azure AD) zu importieren.

1. Der Benutzer wird mit dem aktuellen Sitzungsunternehmen als Standardunternehmen importiert. Ändern Sie gegebenenfalls das aktuelle Unternehmen, bevor Sie Benutzer importieren.
2. Wechseln Sie zu **Systemverwaltung > Benutzer > Benutzer**.
3. Klicken Sie auf **Benutzer importieren**.
4. Wählen Sie die Benutzer aus, die importiert werden sollen, und wählen Sie dann **Benutzer importieren** aus.

Nach Abschluss des Imports müssen den Benutzern Rollen zugewiesen werden.

## <a name="import-users-in-bulk"></a>Massenimport von Benutzern

Diese Prozedur kann von Systemadministratoren verwendet werden, um viele Benutzer aus Azure Active Directory zu importieren.
Beachten Sie, dass bei Verwendung der Stapelimportoption keine Benutzer ausgewählt werden können.

## <a name="run-the-import-as-a-batch-job"></a>Import als Stapelverarbeitungslauf ausühren
1. Der Benutzer wird mit dem aktuellen Sitzungsunternehmen als Standardunternehmen importiert. Ändern Sie gegebenenfalls das aktuelle Unternehmen, bevor Sie Benutzer importieren.
2. Wechseln Sie zu **Systemverwaltung > Benutzer > Benutzer**.
3. Klicken Sie auf **Stapelimport**.
4. Erweitern Sie den Abschnitt **Im Hintergrund ausführen**.
4. Wählen Sie „Ja“ im Feld **Stapelverarbeitung** aus.
6. Geben Sie im Feld **Stapelverarbeitungsgruppe** einen Wert ein oder wählen Sie einen Wert aus. Dieser Schritt ist optional.  
7. Wählen Sie **Ja** im Feld **Privat** aus. Dieser Schritt ist optional.  
8. Wählen Sie **Ja** im Feld **Kritische Aufgabe** aus. Dieser Schritt ist optional.  
9. Wählen Sie im Feld „Kategorie überwachen“ eine Option aus.
10. Klicken Sie auf **OK**.

Nach Abschluss des Imports müssen den Benutzern Rollen zugewiesen werden.

## <a name="run-in-a-sandbox-environment"></a>Eine Sandkastenumgebung ausführen
1. Wählen Sie **Stapelimport** aus.
2. Wählen Sie **OK**.
