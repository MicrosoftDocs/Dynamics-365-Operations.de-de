---
title: Erstellen und Verwalten von Kundenportalbenutzern (enthält Video)
description: In diesem Artikel wird erläutert, wie Sie Kundenportal-Benutzerkonten erstellen und Berechtigungen für diese festlegen.
author: Henrikan
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: ec4f20daac39e1728ab46db159059e51a0cae0a6
ms.sourcegitcommit: 12b3dbee905f8b2eb2e6c383c822a0fc9fccf063
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2022
ms.locfileid: "9103769"
---
# <a name="create-and-manage-customer-portal-users"></a>Erstellen und Verwalten von Kundenportalbenutzern

[!include [banner](../includes/banner.md)]


In der Out-of-Box-Implementierung können sich Benutzer nicht selbst für Websites registrieren, die mithilfe des Kundenportals erstellt wurden. Um sich anzumelden und eine Website zu nutzen, müssen Benutzer vom Administrator eingeladen werden. Microsoft hat absichtlich die Möglichkeit der Benutzer blockiert, sich selbst zu registrieren.

Bevor ein Benutzer eine Website verwenden kann, muss für diesen Benutzer ein Kontaktdatensatz erstellt werden. Dieser Datensatz gibt an, zu welchem Kundenkonto und zu welcher juristischen Person der Benutzer gehört. Diese Informationen sind wichtig, um sicherzustellen, dass der Benutzer Kundenaufträge erstellen und anzeigen kann.

Wenn sich Benutzer selbst registrieren, werden automatisch Kontaktdatensätze für sie erstellt. Daher können Sie nicht sicherstellen, dass ein Benutzer das richtige Kundenkonto und die richtige juristische Person auswählt. Andererseits kann ein Administrator beim Einladungsprozess dem Kontaktdatensatz das richtige Kundenkonto und die richtige juristische Person zuweisen, bevor eine Einladung gesendet wird. Wenn Sie die Lösung so anpassen möchten, dass sich Benutzer selbst registrieren können, sollten Sie die möglichen Konsequenzen berücksichtigen.

## <a name="video"></a>-Video
> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4ADkI]

Das Video [Laden Sie Kunden ein, sich zu registrieren und Ihr Kundenportal zu nutzen](https://youtu.be/drGUYHX9QIQ) (oben gezeigt) ist in der Wiedergabeliste [Finanzen und Vorgänge](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) enthalten, die auf YouTube verfügbar ist.

## <a name="prerequisite-setup"></a>Voraussetzungen für die Einrichtung

Kontakte in Power Apps Portal werden als Datensätze in der Tabelle **Kontakte** in Microsoft Dataverse gespeichert. Duales Schreiben synchronisiert diese Datensätze dann mit Microsoft Dynamics 365 Supply Chain Management wie erforderlich.

![Systemdiagramm für Kundenportal-Kontakte.](media/customer-portal-contacts.png "Systemdiagramm für Kundenportal-Kontakte")

Stellen Sie vor dem Einladen neuer Kunden sicher, dass Sie die Tabellenzuordnung **Kontakt** in dualem Schreiben aktiviert haben.

## <a name="the-invitation-process"></a>Der Einladungsprozess

Führen Sie die folgenden Schritte aus, um einen vorhandenen Kontakt zum Kundenportal einzuladen [Laden Sie Kontakte zu Ihren Portalen ein](/powerapps/maker/portals/configure/invite-contacts) in der Power Apps Portaldokumentation.

Stellen Sie vor dem Einladen eines Kunden zum Kundenportal sicher, dass der [Kontaktdatensatz](/powerapps/maker/portals/configure/configure-contacts) des Kunden verfügbar ist und wie folgt eingerichtet ist:

1. Legen Sie das Feld **Unternehmen** auf die juristische Person fest, zu der der Kunde in Supply Chain Management gehören soll.
2. Legen Sie das Feld **Kontonummer** auf die Kontonummer des Kunden fest, zu der der Kunde in Supply Chain Management gehören soll.

Nachdem ein Kontakt erstellt wurde, sollte er im Supply Chain Management angezeigt werden können.

Weitere Informationen finden Sie unter [Konfigurieren Sie einen Kontakt für die Verwendung in einem Portal](/powerapps/maker/portals/configure/configure-contacts) in der Power Apps Portaldokumentation.

## <a name="out-of-box-web-roles-and-table-permissions"></a>Out-of-Box-Webrollen und Tabellenberechtigungen

Benutzerrollen in Power Apps Portalen sind definiert durch [Webrollen](/powerapps/maker/portals/configure/create-web-roles) und [Tabellenberechtigungen](/powerapps/maker/portals/configure/assign-entity-permissions). Für das Kundenportal sind sofort einige Rollen definiert. Sie können neue Rollen erstellen und vorhandene Rollen ändern oder entfernen.

### <a name="out-of-box-web-roles"></a>Out-of-Box-Webrollen

In diesem Abschnitt werden die Webrollen beschrieben, die mit dem Kundenportal bereitgestellt werden.

Weitere Informationen zum Ändern der Standardbenutzerrollen finden Sie unter [Erstellen Sie Webrollen für Portale](/powerapps/maker/portals/configure/create-web-roles) und [Fügen Sie datensatzbasierte Sicherheit hinzu, indem Sie Tabellenberechtigungen für Portale verwenden](/powerapps/maker/portals/configure/assign-entity-permissions) in der Power Apps Portaldokumentation.

#### <a name="administrator"></a>Administrator

Der Administrator überwacht und pflegt die Website. Diese Person wird das Kundenportal bereitstellen und einrichten. Der Administrator verwaltet die IT- und Sicherheitsaspekte des Portals und stellt sicher, dass alles reibungslos funktioniert. Der Administrator kann das Portal auch anpassen und/oder ändern, indem er neue Funktionen hinzufügt, neue Rollen erstellt und vieles mehr.

#### <a name="customer-representative"></a>Kundenvertreter

Ein Kundenvertreter arbeitet für ein Kundenunternehmen und ist für die Verwaltung der Bestellungen verantwortlich, die das Unternehmen aufgibt. Der Kundenvertreter kann alle Bestellungen sehen, die für das Unternehmen und die Benutzer, die sie aufgegeben haben, aufgegeben wurden. Darüber hinaus kann der Kundenvertreter Informationen zum Gesamtkonto anzeigen und sehen, welche Kontakte im Namen dieses Kontos Bestellungen aufgeben können.

#### <a name="authorized-users"></a>Autorisierte Benutzer

Autorisierte Benutzer können Bestellungen aufgeben und den Status der Bestellungen anzeigen, die sie aufgegeben haben. Sie können jedoch nicht den Status von Bestellungen anzeigen, die andere Benutzer in ihrem Unternehmen aufgegeben haben.

#### <a name="unauthorized-users"></a>Nicht autorisierte Benutzer

Nicht autorisierte Benutzer können keine Daten anzeigen. Sie können nur öffentliche Informationen wie Geschäftsbedingungen und Details zu dem Unternehmen anzeigen, das das Kundenportal betreibt.

#### <a name="example"></a>Beispiel

Die folgende Tabelle zeigt, welche Kundenaufträge die Benutzer in jeder Webrolle im System sehen können.

| Auftrag | Administrator | Kundenvertreter für Kunde&nbsp;X | Autorisierter Benutzer: Jane | Autorisierter Benutzer: Sam | Nicht autorisierte Benutzer: May |
|---|---|---|---|---|---|
| Kunde&nbsp;X Besteller:&nbsp;Jane | Ja | Ja | Ja | Nein | Nein |
| Kunde&nbsp;X Besteller:&nbsp;Sam | Ja | Ja | Nein | Ja | Nein |
| Kunde&nbsp;Y Besteller:&nbsp;May | Ja | Nein | Nein | Nein | Nein |

> [!NOTE]
> Obwohl sowohl Sam als auch Jane Kontakte sind, die für Kunde X arbeiten, können sie nur die Bestellungen sehen, die sie selbst aufgegeben haben, und sonst nichts. Obwohl May eine Bestellung im System hat, kann sie diese Bestellung nicht im Kundenportal sehen, da sie eine nicht autorisierte Benutzerin ist. (Außerdem muss sie die Bestellung über einen anderen Kanal als das Kundenportal aufgegeben haben.)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
