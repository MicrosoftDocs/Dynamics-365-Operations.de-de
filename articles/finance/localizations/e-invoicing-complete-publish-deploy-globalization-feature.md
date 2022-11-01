---
title: Vervollständigen, veröffentlichen und bereitstellen einer Globalisierungsfunktion
description: Dieser Artikel enthält Informationen über den Lebenszyklus von Funktionen zur Globalisierung.
author: gionoder
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 9d4a408f2169b220fefd9ab7e9f3b37217fb3cfe
ms.sourcegitcommit: 1ecfc1d8afb2201ab895ae6f93304ba2b120f14b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/21/2022
ms.locfileid: "9710834"
---
# <a name="complete-publish-and-deploy-a-globalization-feature"></a>Vervollständigen, veröffentlichen und bereitstellen einer Globalisierungsfunktion

[!include [banner](../includes/banner.md)]

## <a name="electronic-invoicing-feature-versions"></a>Versionen der Funktionen für die Elektronische Rechnungsstellung

Die Funktionen der Elektronischen Rechnungsstellung sind versioniert. Wird eine neue Version erstellt, erhöht sich automatisch die Versionsnummer.

Die Versionen der elektronischen Rechnungsfunktion folgen einem Lebenszyklus mit bis zu drei Status:

- **Entwurf** - Wenn eine Funktion diesen Status hat, können Sie ihre Konfigurationsattribute und ihre Artefakte (z.B. Dateiformatkonfigurationen) bearbeiten.
- **Vollständig** - Dieser Status zeigt an, dass Sie die Bearbeitung der Funktion abgeschlossen haben und keine weiteren Aktualisierungen vornehmen möchten. Wenn eine Funktion diesen Status hat, können Sie sie oder eine ihrer Komponenten nicht mehr bearbeiten.
- **Veröffentlicht** - Dieser Status zeigt an, dass die Version der Funktion im globalen Repository veröffentlicht wurde, das mit Ihrer Organisation verbunden ist. Wenn eine Funktion diesen Status hat, können Sie sie oder eine ihrer Komponenten nicht mehr bearbeiten.

Sie können ein **Gültig ab** Datum für eine neue Version einer Funktion der Elektronischen Rechnungsstellung angeben. Auf diese Weise können Sie eine Standardversion definieren, die verwendet werden kann oder die überschrieben werden kann, wenn die Funktion in der Umgebung des Dienstes bereitgestellt wird.

Führen Sie die folgenden Schritte aus, um den Status einer Funktion für die elektronische Rechnungsstellung zu ändern.

1. Melden Sie sich bei Ihrem RCS-Konto (Regulatory Configuration Service) an.
2. Wählen Sie im Abschnitt **Funktionen** des Arbeitsbereichs **Globalisierungsfunktion** die Kachel **Elektronische Rechnungsstellung** aus.
3. Wählen Sie auf der linken Seite der Seite **Elektronische Rechnungsstellung** die Funktion für die elektronische Rechnungsstellung.
4. Wählen Sie auf der Registerkarte **Versionen** auf der rechten Seite der Seite die Version aus.
5. Wählen Sie **Status ändern**, und wählen Sie dann **Fertig** (wenn der aktuelle Status **Entwurf** ist) oder **Veröffentlicht** (wenn der aktuelle Status **Fertig** ist).
6. Wählen Sie in der angezeigten Nachricht **Ja**, um die Anfrage zu bestätigen.

Der manuelle Wechsel vom Status **Fertig** zum Status **Veröffentlicht** ist optional. Die Versionen der Funktionen für die Elektronische Rechnungsstellung werden automatisch auf den Status **Veröffentlicht** aktualisiert, wenn sie in der Umgebung des Dienstes bereitgestellt werden.

Sie können den Status in der Spalte **Versionsstatus der Funktion** auf der Registerkarte **Versionen** verfolgen.

## <a name="deploy-feature-versions"></a>Versionen von Funktionen bereitstellen

In RCS verwenden Sie den Befehl **Bereitstellen**, um eine Version der Funktion für die elektronische Rechnungsstellung in der Umgebung des Zielservices oder der angeschlossenen Anwendung bereitzustellen.

1. Wählen Sie auf der linken Seite der Seite **Elektronische Rechnungsstellung** die Funktion für die elektronische Rechnungsstellung.
2. Wählen Sie auf der Registerkarte **Versionen** auf der rechten Seite die Version der Funktion für die elektronische Rechnungsstellung aus, die Sie in der Umgebung des Dienstes oder der verbundenen Anwendung bereitstellen möchten. Die ausgewählte Version muss einen Status von **Fertig** oder **Veröffentlicht** haben.
3. Wählen Sie **Bereitstellen**, und wählen Sie dann eine oder beide der folgenden Optionen, um das Ziel der Bereitstellung zu definieren:

    - **Verbundene Anwendung** - Dies ist optional, muss aber verwendet werden, wenn Sie möchten, dass die Konfiguration, die von der Einrichtung der Anwendung bereitgestellt wird, in die Instanz von Microsoft Dynamics 365 Finance oder Dynamics 365 Supply Chain Management geschrieben wird, die zuvor mit ihr verbunden war. Wenn Sie diese Art der Bereitstellung überspringen, müssen Sie die in der Anwendungseinrichtung von Finance oder Supply Chain Management definierten Parameter manuell konfigurieren.
    - **Serviceumgebung** - Damit wird die Funktion für die Elektronische Rechnungsstellung in der Umgebung der Servicerechnung bereitgestellt. Die Elektronische Rechnungsstellung ist nun bereit, elektronische Belege, die von Finance oder Supply Chain Management gesendet werden, zu empfangen und zu verarbeiten.

> [!NOTE]
> Normalerweise ändern Sie die Parameter der Funktion Elektronisches Reporting (ER), die in der Umgebung des Dienstes bereitgestellt werden muss. Änderungen an der angeschlossenen Anwendung werden selten sein. Sie sollten neue Versionen für die verbundene Anwendung nur bereitstellen, wenn Sie die entsprechenden Parameter Ihrer Anwendung ändern.

Um festzustellen, ob eine bestimmte Version einer Funktion für die Elektronische Rechnungsstellung in einer bestimmten Umgebung bereitgestellt wird, prüfen Sie die Informationen auf der Registerkarte **Umgebungen**.

## <a name="remove-feature-versions"></a>Entfernen von Funktionen und Versionen

In RCS können Sie **Abbrechen** wählen, um eine bestimmte Version der Funktion für die elektronische Rechnungsstellung aus einer Umgebung zu entfernen, wenn sie dort bereitgestellt wurde.

> [!IMPORTANT]
> Die Schaltfläche **Abbrechen** funktioniert nur in Umgebungen, in denen Dienstleistungen angeboten werden. Es entfernt nichts aus der verbundenen Anwendung für die aktuelle Funktion der Elektronischen Rechnungsstellung.

## <a name="rebase-electronic-invoicing-features"></a>Funktionen für die Elektronische Rechnungsstellung neu einstellen

Wenn eine Funktion der Elektronischen Rechnungsstellung von einer anderen abgeleitet ist, können Sie **Neubasis** wählen, um die abgeleitete Funktion mit den Änderungen zu aktualisieren, die in der ursprünglichen (übergeordneten) Funktion vorgenommen wurden.

Um eine abgeleitete Version einer von Ihnen erstellten Funktion zu rebasen, führen Sie diese Schritte aus.

1. Holen Sie sich die neueste Version der Funktion, indem Sie sie aus dem Global Repository importieren. Weitere Informationen finden Sie unter [Funktion aus Global Repository importieren](e-invoicing-import-feature-global-repository.md).
2. Wählen Sie in der Liste der Funktionen die Funktion aus, die neu erstellt werden soll.
3. Wählen Sie auf der Registerkarte **Versionen** die Option **Neu**, um einen Versionsentwurf zu erstellen.
4. Wählen Sie **Zurücksetzen**.
5. Wählen Sie im Dialogfeld **Rebase** die Version der Funktion aus, auf die Sie rebasen möchten.
6. Wählen Sie **OK** aus.
7. Überprüfen Sie die Funktionskomponenten und nehmen Sie alle notwendigen Änderungen vor.
8. Wählen Sie **Status ändern**, um die Funktion zurückzusetzen. Wenn die Zurücksetzung abgeschlossen ist, können Sie zusätzliche Aktionen ausführen.

## <a name="get-a-specific-version-of-electronic-invoicing-features"></a>Erhalten Sie eine bestimmte Version der Funktionen für die Elektronische Rechnungsstellung

Wenn Sie eine neue Version einer Funktion für die Elektronische Rechnungsstellung erstellen, erstellt das System eine Kopie der neuesten Version der Funktion. Um eine frühere Version der Funktion als Grundlage für eine neue Version zu verwenden, wählen Sie die Version aus und wählen Sie dann den Befehl **Diese Version holen**. Es wird eine neue Entwurfsversion der Funktion erstellt, die eine Kopie der ausgewählten Version ist.
