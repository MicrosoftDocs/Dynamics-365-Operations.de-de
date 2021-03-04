---
title: Dual-Schreiben von Lifecycle Services einrichten
description: In diesem Thema wird erläutert, wie Sie eine Dual-Schreib-Verbindung zwischen einer neuen Finance and Operations Umgebung und einer neuen Dataverse Umgebung aus Microsoft Dynamics Lifecycle Services (LCS) einrichten.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 25db9c58c3d09e44dcf11b48cae1a9eda4241c35
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683523"
---
# <a name="dual-write-setup-from-lifecycle-services"></a>Dual-Schreiben von Lifecycle Services einrichten

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

In diesem Thema wird erläutert, wie Sie eine Dual-Schreib-Verbindung zwischen einer neuen Finance and Operations Umgebung und einer neuen Dataverse Umgebung aus Microsoft Dynamics Lifecycle Services (LCS) einrichten.

## <a name="prerequisites"></a>Voraussetzungen

Sie müssen ein Administrator sein, um eine Dual-Schreib-Verbindung einzurichten.

+ Sie müssen Zugriff auf den Mandant besitzen.
+ Sie müssen in beiden Bereichen Administrator sein, in Finance and Operations Umgebungen und Dataverse Umgebungen.

## <a name="set-up-a-dual-write-connection"></a>Richten Sie eine Dual-Schreib-Verbindung ein

Folgen Sie diesen Schritten, um eine Dual-Schreib-Verbindung einzurichten.

1. In LCS gehen Sie zu Ihrem Projekt.
2. Wählen Sie **Konfigurieren**, um eine neue Umgebung bereitzustellen.
3. Wählen Sie die Version. 
4. Wählen Sie die Topologie aus. Wenn nur eine Topologie verfügbar ist, wird diese automatisch ausgewählt.
5. Führen Sie die ersten Schritte im Assistent **Bereitstellungseinstellungen** aus.
6. Folgen Sie einem dieser Schritte auf der Registerkarte **Dataverse**:

    - Wenn eine Dataverse Umgebung bereits für Ihren Mandanten bereitgestellt ist, können sie sie auswählen.

        1. Legen Sie die Option **Dataverse Konfigurieren** auf **Ja** fest.
        2. In dem Feld **Verfügbare Umgebungen** wählen Sie im Feld die Umgebung aus, die in Ihre Finance and Operations Daten integriert werden soll. Die Liste enthält alle Umgebungen, in denen Sie über Administratorrechte verfügen.
        3. Wähle Sie das Kontrollkästchen **Zustimmen**, um anzuzeigen, dass Sie den Nutzungsbedingungen zustimmen.

        ![Dataverse Registerkarte, wenn eine Dataverse Umgebung bereits für Ihren Mandanten bereitgestellt ist](../dual-write/media/lcs_setup_1.png)

    - Wenn Ihr Mandant noch keine Dataverse Umgebung hat, wird eine neue Umgebung bereitgestellt.

        1. Legen Sie die Option **Dataverse Konfigurieren** auf **Ja** fest.
        2. Einen Namen für die Dataverse Umgebung eingeben.
        3. Wählen Sie die Region aus, in der die Umgebung bereitgestellt werden soll.
        4. Wählen Sie die Standardsprache und -währung für die Umgebung aus.

            > [!NOTE]
            > Sie können die Sprache und Währung später nicht mehr ändern.

        5. Wähle Sie das Kontrollkästchen **Zustimmen**, um anzuzeigen, dass Sie den Nutzungsbedingungen zustimmen.

        ![Dataverse Registerkarte, wenn Ihr Mandant noch keine Dataverse Umgebung hat](../dual-write/media/lcs_setup_2.png)

7. Führen Sie die verbleibenden Schritte im Assistent **Bereitstellungseinstellungen** aus.
8. Nachdem die Umgebung den Status **Bereitgestellt** hat, öffnen Sie die Seite mit den Umgebungsdetails. Der Abschnitt **Dataverse Umgebungsinformationen** zeigt die Namen der Finance and Operations Umgebung und die Dataverse Umgebung, die verknüpft sind.

    ![Dataverse Abschnitt mit Umgebungsinformationen](../dual-write/media/lcs_setup_3.png)

9. Ein Administrator der Finance and Operations Umgebung muss sich bei LCS anmelden und **Verknüpfung zu CDS für Apps** auswählen, um den Link vervollständigen. Auf der Seite mit den Umgebungsdetails werden die Kontaktinformationen des Administrators angezeigt.

    Nach Abschluss der Verknüpfung wird der Status auf **Umgebungsverknüpfung erfolgreich abgeschlossen** aktualisiert.

10. Zum Öffnen des **Datenintegration** Arbeitsbereichs in der Finance and Operations wählen Sie die Umgebung aus und steuern Sie die verfügbaren Vorlagen und wählen Sie **Link zu CDS für Apps**.

    ![Link zur Schaltfläche CDS für Apps im Abschnitt Dataverse Umgebungsinformationen](../dual-write/media/lcs_setup_4.png)

> [!NOTE]
> Sie können die Verknüpfung von Umgebungen mit LCS nicht aufheben. Um die Verknüpfung einer Umgebung aufzuheben, öffnen Sie den **Datenintegration** Arbeitsbereich in der Finance and Operations Umgebung und wählen Sie dann **Verknüpfung aufheben**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]