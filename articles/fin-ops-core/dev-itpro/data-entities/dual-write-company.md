---
title: Unternehmenskonzept in Common Data Service
description: In diesem Thema wird die Integration von Unternehmensdaten zwischen Finance and Operations und Common Data Service beschrieben.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: aa4d54fd7b3ab407751ad6ca1032d742c23eed41
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184530"
---
## <a name="company-concept-in-common-data-service"></a>Unternehmenskonzept in Common Data Service

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

In Finance and Operations ist das Konzept *Unternehmen* sowohl ein juristisches als auch ein unternehmerisches Konstrukt. Es ist außerdem ein Sicherheits- und Sichtbarkeitsgrenze für Daten. Benutzer arbeiten immer im Kontext eines einzelnen Unternehmens, und die meisten Daten werden von dem Unternehmen gekennzeichnet.

Common Data Service hat kein entsprechendes Konzept. Das nächste Konzept ist *Unternehmenseinheit*, das in erster Linie eine Sicherheits- und Sichtbarkeitsgrenze für Benutzerdaten ist. Dieses Konzept besitzt nicht die gleichen rechten oder geschäftlichen Auswirkungen wie das Unternehmenskonzept.

Da Unternehmenseinheit und Unternehmen keine entsprechenden Konzepte sind, ist es nicht möglich, eine 1:1-Zuordnung zum Zwecke der Common Data Service-Integration zu erzwingen. Da Benutzer aber standardmäßig in der Lage sein müssen, dieselben Datensätze in der Anwendung und in Common Data Service anzuzeigen, hat Microsoft hat eine neue Entität in Common Data Service mit dem Namen „cdm\_Company“ eingeführt. Diese Entität entspricht der Unternehmensentität in der Anwendung. Um sicherzustellen, dass die Sichtbarkeit von Datensätzen in der Anwendung und Common Data Service standardmäßig äquivalent ist, empfehlen wir die folgende Einstellung für Daten in Common Data Service:

+ Für jeden Unternehmensdatensatz in Finance and Operations, für den duales Schreiben aktiviert ist, wird ein zugehöriger cdm\_Company-Datensatz erstellt.
+ Wenn ein cdm\_Company-Datensatz erstellt und für duales Schreiben aktiviert wird, wird eine Standardgeschäftseinheit mit demselben Namen erstellt. Es wird zwar automatisch ein Standardteam für diese Geschäftseinheit erstellt, die Geschäftseinheit wird aber nicht verwendet.
+ Ein separates Eigentümerteam wird erstellt, das denselben Namen hat. Es wird ebenfalls der Geschäftseinheit zugeordnet.
+ Standardmäßig wird der Eigentümer eines beliebigen Datensatzes, der erstellt und in Common Data Service dualgeschrieben wird, auf das Team „DW-Eigentümer“ festgelegt, das mit der zugehörigen Geschäftseinheit verknüpft ist.

Die folgende Abbildung zeigt ein Beispiel für diese Dateneinreichtung in Common Data Service.

![Dateneinrichtung in Common Data Service](media/dual-write-company-1.png)

Aufgrund dieser Konfiguration ist jeder Datensatz, der mit dem USMF-Unternehmen verknüpft ist, im Besitz eines Teams, das mit der USFM-Geschäftseinheit in Common Data Service verknüpft ist. Daher kann jeder Benutzer, der Zugriff auf diese Geschäftseinheit über eine Sicherheitsrolle hat, die auf Sichtbarkeit auf Geschäftseinheitsebene festgelegt ist, diese Datensätze nun anzeigen. Das folgende Beispiel veranschaulicht, wie Teams verwendet werden können, um den richtigen Zugang zu diesen Datensätzen bereitzustellen.

+ Die Rolle „Vertriebsmanager“ ist Mitgliedern des Teams „USMF-Vertrieb“ zugewiesen.
+ Benutzer mit der Rolle „Vertriebsmanager“ können auf beliebige Kontodatensätze zugreifen, die Mitglieder derselben Geschäftseinheit wie sie sind.
+ Das Team „USMF-Vertrieb“ wird mit der zuvor erwähnten USMF-Geschäftseinheit verknüpft.
+ Daher können Mitglieder des Teams „USMF-Vertrieb“ ein beliebiges Konto sehen, das im Besitz des Benutzers „USMF DW“ ist, der von der USMF-Unternehmenseinheit in Finance and Operations stammt.

![Wie Teams verwendet werden können](media/dual-write-company-2.png)

Wie in der vorherigen Abbildung dargestellt, ist diese 1:1-Zuordnung zwischen Geschäftseinheit, Unternehmen und Team nur ein Anfangspunkt. In diesem Beispiel wird eine neue Geschäftseinheit „Europa“ manuell in Common Data Service als übergeordnetes Element für DEMF und ESMF erstellt. Diese neue Stammgeschäftseinheit ist nicht mit dem dualen Schreiben verknüpft. Sie kann allerdings verwendet werden, um Mitgliedern des Teams „EUR-Vertrieb“ Zugriff auf Kontodaten sowohl in DEMF als auch in ESMF zu gewähren, indem die Datensichtbarkeit in der zugehörigen Sicherheitsrolle auf **Übergeordnete/untergeordnete Geschäftseinheit** festgelegt wird.

Ein abschließendes Thema ist, wie durch das duale Schreiben bestimmt wird, welchem Eigentümerteam Datensätze zugewiesen werden sollen. Dieses Verhalten wird vom Feld **Standardeigentümerteam** im Datensatz cdm\_Company gesteuert. Wenn ein cdm\_Company-Datensatz für duales Schreiben aktiviert ist, erstellt ein Plug-In automatisch die zugewiesene Geschäftseinheit und das Eigentümerteam (wenn nicht bereits vorhanden) und legt das Feld **Standardeigentümerteam** fest. Der Administrator kann das Feld in einen anderen Wert ändern. Allerdings kann der Administrator das Feld nicht deaktivieren, sofern die Entität für duales Schreiben aktiviert ist.

![Feld „Standardeigentümerteam“](media/dual-write-default-owning-team.jpg)

## <a name="company-striping-and-bootstrapping"></a>Unternehmensstriping und Bootstrapping

Die Common Data Service-Integration bringt Unternehmensparität durch Verwendung eines Unternehmensbezeichners zum Kennzeichen von Daten. Wie in der folgenden Abbildung dargestellt, werden alle unternehmensspezifischen Entitäten so erweitert, dass sie eine Viele-zu-Eins-Beziehung (N:1) mit der cdm\_Company-Entität haben.

![N:1-Beziehung zwischen einer unternehmensspezifischen Entität und der cdm_Company-Entität](media/dual-write-bootstrapping.png)

+ Für Datensätze wird der Wert schreibgeschützt, nachdem ein Unternehmen hinzugefügt und gespeichert wird. Daher sollten Benutzer sicherstellen, dass Sie das korrekte Unternehmen auswählen.
+ Nur Datensätze mit Unternehmensdaten kommen für duales Schreiben zwischen der Anwendung und Common Data Service infrage.
+ Für vorhandene Common Data Service-Daten wird in Kürze eine vom Administrator geführte Bootstrapping-Erfahrung verfügbar sein.
