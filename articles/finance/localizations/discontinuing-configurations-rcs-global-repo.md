---
title: Konfigurationen im RCS Global-Repository einstellen
description: In diesem Artikel wird beschrieben, wie Sie Konfigurationen im RCS Global-Repository beenden.
author: gionoder
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2021-02-02
ms.dyn365.ops.version: AX 10.0.14
ms.custom: 97423
ms.assetid: ''
ms.search.form: ERSolutionTable, ERWorkspace
ms.openlocfilehash: b0605f56058e3c93ea088ee8386ba26c4ce2b65a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272335"
---
# <a name="discontinue-configurations-in-the-rcs-global-repository"></a>Konfigurationen im RCS Global-Repository einstellen

[!include [banner](../includes/banner.md)]

In diesem Artikel wird beschrieben, wie Sie die Konfiguration im RCS Global-Repository beenden. Bisher konnten nur nicht mehr benötigte Konfigurationen gelöscht werden. Jetzt können Sie jedoch eine freigegebene Konfiguration im RCS Global-Repository als **Eingestellt** markieren. Darüber hinaus können Sie mit dieser Funktion auch Folgendes durchführen: 
 
 - Stellen Sie im Voraus Benachrichtigungen bereit, wenn die Einstellung einer Konfiguration geplant ist.
 - Geben Sie die entsprechenden Details zur Ersatzkonfiguration an.
 - Legen Sie ein **Unterstützt bis**-Datum für die spezifische Konfiguration fest, um den Benutzer darüber zu informieren, wann sie eingestellt wird.

Wenn Sie eine Konfigurationsversion beenden, können Sie die folgenden optionalen Informationen angeben:

  - **Ersatzkonfiguration**
  - **Ersatzkonfigurationsversion**
  - **Freitextnotiz**: Verwenden Sie dieses Feld, um Dokumentationslinks oder Referenzen bereitzustellen
  - **Unterstützt bis**: Dieses Feld enthält das vorgeschlagene Datum, bis zu dem die aktuelle Konfiguration/Version unterstützt wird. Dieses Datum muss manuell aktualisiert werden.
  
Führen Sie die folgenden Schritte aus, um die Konfiguration einzustellen. 

1. Wählen Sie aus, ob Sie eine einzelne Version oder alle Versionen mit denselben Einstellungen in einem Vorgang beenden möchten, indem Sie **Alle Versionen** auf **Ja** festlegen. 
2. Stellen Sie den Parameter **Nicht fortsetzen** auf **Ja**.
3. Wählen Sie **OK** aus, um die Konfigurationen abzubrechen. Das Feld **Aufgabedatum** wird ausgefüllt, wenn Sie die Änderungen speichern.

![Konfigurationsinformationen beenden.](media/Discontinue-details-2.png)
  
Sie können die Konfiguration auf **Freigegeben** zurücksetzen oder die Abbruchinformationen jederzeit anpassen. Wenn Sie eine Konfiguration freigeben, geben Sie das Datum **Unterstützt bis** und alle anderen Informationen im Zusammenhang mit der Einstellung an, um Ihre Pläne für eine zukünftige Einstellung anzuzeigen.

Wenn Sie Informationen über eine geplante Einstellung teilen möchten, bevor Sie die Konfiguration tatsächlich einstellen, kann der Benutzer alle Felder im Zusammenhang mit dem Ersetzen vorab ausfüllen, aber den Parameter **Nicht fortsetzen** auf **Nein** belassen.

> [!NOTE]
> Die Einstellung schränkt Vorgänge mit Konfigurationen nicht ein. Sie können die Konfigurationen weiterhin importieren, ausführen oder ableiten. Diese Felder dienen nur zur Information.

## <a name="finance-supports-displaying-this-information-starting-in-version-10014"></a>Finance unterstützt die Anzeige dieser Informationen ab Version 10.0.14

Dynamics 365 Finance unterstützt die Anzeige von Einstellungsinformationen ab Version 10.0.14. Auf der Seite **Globales Repository** können Sie aktuelle Informationen zur Einstellung anzeigen. Standardmäßig werden nicht mehr verfügbare Konfigurationen herausgefiltert.
  
Auf der Seite **Importierte Konfigurationen** (ERSolutionTable) werden Konfigurationen angezeigt, die beim Import bereits eingestellt wurden. Für die Konfigurationen, die nach dem Import eingestellt wurden, können die Abbruchinformationen durch Ausführen von **Konfigurationsaktualisierungen importieren** synchronisiert werden.


