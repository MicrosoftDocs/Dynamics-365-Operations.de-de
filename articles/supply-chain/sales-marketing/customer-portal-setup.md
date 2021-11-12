---
title: Installieren, einrichten und aktualisieren Sie das Kundenportal
description: Dieses Thema enthält Lizenzdetails und Installationsanweisungen für das Kundenportal.
author: Henrikan
ms.date: 06/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: b24aa8c342a3de647acc9cf0b4ec175ca24cef43
ms.sourcegitcommit: e891a6cc0674d27b7e218fdf22ca5ba8ac3310d0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/18/2021
ms.locfileid: "7648377"
---
# <a name="install-set-up-and-update-the-customer-portal"></a>Installieren, einrichten und aktualisieren Sie das Kundenportal

[!include [banner](../includes/banner.md)]
[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="licensing-requirements"></a>Lizenzanforderungen

Um das Kundenportal zu implementieren, müssen Sie über folgende Lizenzen verfügen:

- **Power Apps Portale** – Diese Lizenz ist erforderlich, um das Kundenportal zu hosten. Portale werden je nach Nutzung lizenziert. Weitere Informationen finden Sie in den [Power Apps Portal Lizenzanforderungen](/power-platform/admin/powerapps-flow-licensing-faq#portals).
- **Duales Schreiben** – Sie müssen über die erforderlichen Lizenzen verfügen, um duales Schreiben für Supply Chain Management-Tabellen zu aktivieren. Weitere Informationen finden Sie unter [Systemanforderungen für duales Schreiben](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req.md).

## <a name="dependencies-on-dual-write-and-power-apps-portals"></a>Abhängigkeiten von dualem Schreiben und Power Apps Portalen

Das Kundenportal ist abhängig von Power Apps Portalen und dualem Schreiben, wie in der folgenden Abbildung gezeigt.

![Kundenportalabhängigkeiten.](media/customer-portal-elements.png "Kundenportalabhängigkeiten")

Im Gegensatz zu anderen Funktionen von Supply Chain Management befindet sich die Kundenportalvorlage in Power Apps Portalen. Daher ist das Kundenportal durch die bereitgestellten Funktionen und Fähigkeiten eingeschränkt, die von Power Apps Portalen und Tabellen in dualem Schreiben bereitgestellt werden.

## <a name="required-setup-to-enable-the-customer-portal"></a><a name="required-setup"></a>Erfordert Installation zum Aktivieren des Kundenportals

Nachdem Sie sichergestellt haben, dass Sie über die erforderlichen Lizenzen verfügen, können Sie duales Schreiben wie in der Beschreibung beschrieben einrichten [Anweisungen für die anfängliche Synchronisierung mit zwei Schreibvorgängen](../../fin-ops-core/dev-itpro/data-entities/dual-write/enable-entity-map.md).

Stellen Sie sicher, dass die folgenden Tabellenzuordnungen in dualem Schreiben aktiviert sind:

- Auftragskopf
- Auftragsdetails
- Konten
- Kontakte
- Produkte

Nach Abschluss dieser Einrichtung können Sie die Vorlage für das Kundenportal bereitstellen.

## <a name="provision-the-customer-portal"></a>Stellen Sie das Kundenportal bereit

Bevor Sie beginnen, stellen Sie sicher, dass Sie die [erforderliche Einrichtung](#required-setup) bereits abgeschlossen haben. Führen Sie dann die folgenden Schritte aus, um das Kundenportal bereitzustellen.

1. Gehen Sie zu [make.powerapps.com](https://make.powerapps.com/).
2. Stellen Sie sicher, dass Sie die Umgebung verwenden, in der Sie duales Schreiben aktiviert haben.
3. Auf der Registerkarte **Erstellen** scrollen Sie nach unten zum Abschnitt **Beginnen Sie mit der Vorlage** und wählen Sie die Vorlage aus, die benannt ist **Debitorenportal**.
4. Befolgen Sie die Anweisungen auf dem Bildschirm.

Nach Abschluss der Bereitstellung können Sie auf das Kundenportal im Internet zugreifen im Abschnitt **Ihre Apps** auf der Seite **Startseite**.

> [!NOTE]
> Wenn die Lösung duales Schreiben nicht in der Umgebung installiert ist, in der Sie arbeiten, wird eine Fehlermeldung angezeigt und das Kundenportal wird nicht bereitgestellt.

## <a name="update-the-customer-portal"></a>Aktualisieren Sie das Kundenportal

Weitere Funktionen werden möglicherweise später zum Kundenportal hinzugefügt. Alle Änderungen, die Microsoft an den zugrunde liegenden Lösungskomponenten vornimmt, werden automatisch in Ihrer Umgebung angezeigt. Die in Ihrer Umgebung bereitgestellte Website spiegelt jedoch nicht automatisch Änderungen wider, die an den Konfigurationsdaten vorgenommen wurden. Sie müssen diese Änderungen manuell anwenden, indem Sie den Code aus der neuen Vorlage abrufen und mit der bereitgestellten Website zusammenführen.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

Um zu erfahren, wie Sie das Kundenportal einrichten und anpassen können, lesen Sie zunächst die folgende Dokumentation zu den zugrunde liegenden Technologien:

- [Power Apps Portaldokumentation](/powerapps/maker/portals/overview)
- [Dokumentation Duales Schreiben](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md)

Um Ihre Portale effektiv verwalten zu können, müssen Sie die Power Apps Portale und Microsoft Dataverse Lifecycle verstehen. Weitere Informationen finden Sie in den folgenden Ressourcen:

- [Informationen zum Portallebenszyklus](/powerapps/maker/portals/admin/portal-lifecycle)
- [Aktualisieren Sie ein Portal](/powerapps/maker/portals/admin/upgrade-portal)
- [Portalkonfiguration migrieren](/powerapps/maker/portals/admin/migrate-portal-configuration)
- [Solution Lifecycle Management: Dynamics 365 for Customer Engagement Apps](https://www.microsoft.com/download/details.aspx?id=57777)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]