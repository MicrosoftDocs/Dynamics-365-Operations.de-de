---
title: Integrierte Masterdaten von Kreditoren
description: In diesem Thema wird die Integration von Kreditorendaten zwischen Finance and Operations und Common Data Service beschrieben.
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
ms.openlocfilehash: 45808bc35aba04df6fcaf6b1cbfcc2461b0b65cb
ms.sourcegitcommit: 02c223b44ac7196df675afac61c6783f467d1983
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/24/2019
ms.locfileid: "1789190"
---
## <a name="integrated-vendor-master"></a>Integrierte Masterdaten von Kreditoren

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

Der Begriff *Kreditor* bezieht sich auf eine Lieferantenorganisation oder einen Einzelunternehmer, der Teil des Lieferkettenprozesses ist und der Waren an das Unternehmen liefert. Der Begriff*Kreditor* ist zwar in Microsoft Dynamics 365 for Finance and Operations ein etabliertes Konzept, ist Dynamics 365 for Customer Engagement gibt es dieses Konzept aber nicht. Stattdessen überladen einige Unternehmen die Kontoentität, um sowohl Debitoreninformationen als auch Kreditoreninformationen zu speichern. Andere Unternehmen verwenden ein benutzerdefiniertes Kreditorenkonzept. Die Common Data Service-Integration unterstützt beide Entwürfe. Daher können Sie, je nach Ihrem Unternehmensszenario, einen der beiden Entwürfe aktivieren.

Durch die Integration von Kreditorendaten zwischen Finance and Operations and Customer Engagement können für die Daten einen Multimaster ausführen. Unabhängig davon, woher die Kreditorendaten stammen, werden diese im Hintergrund über Anwendungsgrenzen und Infrastrukturunterschiede hinweg integriert. 

### <a name="vendor-data-flow"></a>Kreditorendatenfluss

Wenn Sie Customer Engagement für das Kreditoren-Mastering verwenden und Sie die Kreditoreninformationen von den Debitoreninformationen isolieren möchten, können Sie das neue Kreditorendesign verwenden.

![Kreditorendatenfluss](media/dual-write-vendor-data-flow.png)

Wenn Sie Customer Engagement für das Kreditoren-Mastering verwenden und Sie weiterhin die Kontoentität zum Speichern der Kreditoreninformationen verwenden möchten, können Sie das neue erweiterte Kreditorendesign verwenden. In diesem Entwurf werden erweiterte Kreditordaten, z. B. das Kreditorengruppen- und das Kreditorenbuchungsprofil, in den Kreditorendetails gespeichert.

![Erweiterter Kreditorendatenfluss](media/dual-write-vendor-detail.jpg)

Die Kontaktinformationen des Kreditors ähneln den Kontaktinformationen des Debitors. Im Hintergrund werden die Informationen der Kontaktperson in den gleichen Entitäten gespeichert und aus den gleichen Entitäten abgerufen.

## <a name="templates"></a>Vorlagen

Kreditorendaten enthalten alle Informationen über den Kreditor, z. B. die Kreditorengruppe, Adressen, Kontaktinformationen, das Zahlungsprofil und das Rechnungsprofil. Eine Sammlung von Entitätszuordnungen arbeitet während der Interaktion der Kreditorendaten zusammen, wie in der folgenden Tabelle dargestellt.

Finance and Operations  | Customer Engagement-Anwendung
------------------------|---------------------------------
Kreditor V2               | Konto
Kreditor V2               | Msdyn\_vendors
CDS-Kontakte V2         | Kontakt
Kreditorengruppen           | Msdyn\_vendorgroups
Kreditorzahlungsmethode   | Msdyn\_vendorpaymentmethods
Zahlungszeitplan        | Msdyn\_paymentschedules
Zahlungszeitplan        | Msdyn\_paymentschedulelines
Zahlungstag CDS         | Msdyn\_paymentdays
Zahlungstagpositionen CDS   | Msdyn\_paymentdaylines
Zahlungsbedingungen        | Msdyn\_paymentterms
Namensaffixe            | Msdyn\_nameaffixes

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="vendor-v2-and-account"></a>Kreditor V2 und Konto 

Unternehmen, die die Kontoentität verwenden, um Kreditorendaten speichern, können diese weiterhin auf die gleiche Weise verwenden. Sie können auch die explizite Kreditorenfunktion nutzen, die dank der Finance and Operations-Integration zur Verfügung stehen.

## <a name="vendor-v2-and-msdyn_vendors"></a>Kreditor V2 und Msdyn\_vendors

Unternehmen, die eine benutzerdefinierte Lösung für Kreditoren verwenden, können das vordefinierte Kreditorenkonzept nutzen, das in Common Data Service durch die Finance and Operations-Integration eingeführt wird. 

<!-- ![vendor mappings](media/dual-write-vendors-1.png) -->

<!-- ![vendor mappings](media/dual-write-vendors-2.png) -->

<!-- ![vendor mappings](media/dual-write-vendors-3.png) -->

Quellfeld | Zuordnungstyp | Zielfeld
---|---|---
VENDORACCOUNTNUMBER | = | msdyn\_vendoraccountnumber
VENDORGROUPID | = | msdyn\_vendorgroupid.msdyn\_vendorgroup
VENDORORGANIZATIONNAME | = | msdyn\_name
VENDORPARTYTYPE | \>\< | msdyn\_isperson
PERSONFIRSTNAME | = | msdyn\_firstname
PERSONLASTNAME | = | msdyn\_lastname
CREDITLIMIT | = | msdyn\_vendorcreditlimit
ISFOREIGNENTITY | \>\< | msdyn\_isforeignentity
ISONETIMEVENDOR | \>\< | msdyn\_isonetimevendor
ADDRESSBUILDINGCOMPLIMENT | = | msdyn\_addressbuildingcompliment
PERSONCHILDRENNAMES | = | msdyn\_childrennames
ADDRESSCITY | = | msdyn\_addresscity
ADDRESSCOUNTRYREGIONID | = | msdyn\_addresscountryregionid
ADDRESSCOUNTRYREGIONISOCODE | = | msdyn\_addresscountryregionisocode
ADDRESSCOUNTYID | = | msdyn\_addresscountyid
CREDITRATING | = | msdyn\_creditrating
ADDRESSDESCRIPTION | = | msdyn\_addressdescription
ADDRESSDISTRICTNAME | = | msdyn\_addressdistrictname
DUNSNUMBER | = | msdyn\_dunsnumber
ETHNICORIGINID | = | msdyn\_ethnicorigin
FORMATTEDPRIMARYADDRESS | = | msdyn\_formattedprimaryaddress
PERSONHOBBIES | = | msdyn\_hobbies
PERSONINITIALS | = | msdyn\_initials
LANGUAGEID | = | msdyn\_languageid
PERSONLASTNAMEPREFIX | = | msdyn\_lastnameprefix
PERSONMIDDLENAME | = | msdyn\_middlename
ORGANIZATIONNUMBER | = | msdyn\_organizationnumber
OURACCOUNTNUMBER | = | msdyn\_ourvendoraccountnumber
PAYMENTID | = | msdyn\_paymentid
PERSONPHONETICFIRSTNAME | = | msdyn\_phoneticfirstname
PERSONPHONETICMIDDLENAME | = | msdyn\_phoneticmiddlename
PERSONPHONETICLASTNAME | = | msdyn\_phoneticlastname
ORGANIZATIONPHONETICNAME | = | msdyn\_organizationphoneticname
ADDRESSPOSTBOX | = | msdyn\_addresspostbox
PRIMARYURL | = | msdyn\_primarycontacturl
PRIMARYEMAILADDRESS | = | msdyn\_primaryemailaddress
PRIMARYEMAILADDRESSDESCRIPTION | = | msdyn\_primaryemailaddressdescription
PRIMARYFACEBOOK | = | msdyn\_primaryfacebook
PRIMARYFACEBOOKDESCRIPTION | = | msdyn\_primaryfacebookdescription
PRIMARYFAXNUMBER | = | msdyn\_primaryfaxnumber
PRIMARYFAXNUMBERDESCRIPTION | = | msdyn\_primaryfaxnumberdescription
PRIMARYFAXNUMBEREXTENSION | = | msdyn\_primaryfaxnumberextension
PRIMARYLINKEDIN | = | msdyn\_primarylinkedin
PRIMARYLINKEDINDESCRIPTION | = | msdyn\_primarylinkedindescription
PRIMARYPHONENUMBER | = | msdyn\_pimaryphonenumber
PRIMARYPHONENUMBERDESCRIPTION | = | msdyn\_primaryphonenumberdescription
PRIMARYPHONENUMBEREXTENSION | = | msdyn\_primaryphonenumberextension
PRIMARYTELEX | = | msdyn\_primarytelex
PRIMARYTELEXDESCRIPTION | = | msdyn\_primarytelexdescription
PRIMARYTWITTER | = | msdyn\_primarytwitter
PRIMARYTWITTERDESCRIPTION | = | msdyn\_primarytwitterdescription
PRIMARYURLDESCRIPTION | = | msdyn\_primaryurldescription
PERSONPROFESSIONALSUFFIX | = | msdyn\_professionalsuffix
PERSONPROFESSIONALTITLE | = | msdyn\_professionatitle
ADDRESSSTATEID | = | msdyn\_addressstateid
ADDRESSSTREET | = | msdyn\_addressstreet
ADDRESSSTREETNUMBER | = | msdyn\_addressstreetnumber
VENDORKNOWNASNAME | = | msdyn\_vendorknownasname
ADDRESSZIPCODE | = | msdyn\_addresszipcode
DEFAULTPAYMENTDAYNAME | = | msdyn\_defaultpaymentdayname.msdyn\_name
DEFAULTPAYMENTSCHEDULENAME | = | msdyn\_paymentschedule.msdyn\_name
DEFAULTPAYMENTTERMSNAME | = | msdyn\_paymentterms.msdyn\_name
HASONLYTAKENBIDS | \>\< | msdyn\_hasonlytakenbids
ISMINORITYOWNED | \>\< | msdyn\_isminorityowned
ISVENDORLOCALLYOWNED | \>\< | msdyn\_isvendorlocallyowned
ISSERVICEVETERANOWNED | \>\< | msdyn\_isserviceveteranowned
ISOWNERDISABLED | \>\< | msdyn\_ownerisdisabled
ISWOMANOWNER | \>\< | msdyn\_womanowner
PERSONANNIVERSARYDAY | = | msdyn\_personanniversaryday
PERSONANNIVERSARYYEAR | = | msdyn\_anniversaryyear
PERSONBIRTHDAY | = | msdyn\_birthday
PERSONBIRTHYEAR | = | msdyn\_birthyear
ORGANIZATIONEMPLOYEEAMOUNT | = | msdyn\_numberofemployees
VENDORHOLDRELEASEDATE | = | msdyn\_vendoronholdreleasedate
VENDORPARTYNUMBER | = | msdyn\_vendorpartynumber
ADDRESSLOCATIONID | = | msdyn\_addresslocationid
PERSONANNIVERSARYMONTH | = | msdyn\_vendorpersonanniversarymonth
PERSONBIRTHMONTH | = | msdyn\_vendorpersonbirthmonth
PERSONMARITALSTATUS | \>\< | msdyn\_maritalstatus
ADDRESSLATITUDE | \>\> | msdyn\_addresslatitude
ADDRESSLONGITUDE | \>\> | msdyn\_addresslongitude
ONHOLDSTATUS | \>\< | msdyn\_onholdstatus
CURRENCYCODE | = | msdyn\_currencycode.isocurrencycode
ISVENDORLOCATEDINHUBZONE | \>\< | msdyn\_isvendorlocatedinhubzone
DEFAULTVENDORPAYMENTMETHODNAME | = | msdyn\_vendorpaymentmethod.msdyn\_name
INVOICEVENDORACCOUNTNUMBER | = | msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber
PERSONGENDER | \>\< | msdyn\_gender
AREPRICESINCLUDINGSALESTAX | \>\< | msdyn\_priceincludessalestax
SALESTAXGROUPCODE | = | msdyn\_taxgroup.msdyn\_name
VENDORPRICETOLERANCEGROUPID | = | msdyn\_pricetolerancegroup.msdyn\_groupid

## <a name="contacts"></a>Kontakte

Diese Vorlage synchronisiert alle primären, sekundären und tertiären Kontaktinformationen, sowohl für Debitoren als auch für Kreditoren, zwischen Finance and Operations und Customer Engagement. Informationen zur Entitätszuordnung finden Sie in den [Integrierten Masterdaten von Debitoren](dual-write-customer.md#contacts).

## <a name="vendor-groups"></a>Kreditorengruppen

Diese Vorlage synchronisiert Kreditorengruppeninformationen zwischen Finance and Operations und Customer Engagement.

<!-- ![vendor groups mappings](media/dual-write-vendor-groups.png) -->

Quellfeld | Zuordnungstyp | Zielfeld
---|---|---
DEFAULTPAYMENTTERMNAME | = | msdyn\_paymentterms.msdyn\_name
BESCHREIBUNG | = | msdyn\_description
VENDORGROUPID | = | msdyn\_vendorgroup
CLEARINGPERIODPAYMENTTERMNAME | = | msdyn\_clearingperiodpaymentpermname.msdyn\_name

### <a name="vendor-payment-method"></a>Kreditorzahlungsmethode

Diese Vorlage synchronisiert Informationen für die Kreditorenzahlungsmethode zwischen Finance and Operations und Customer Engagement.

<!-- ![vendor payment method mappings](media/dual-write-vendor-payment-method.png) -->

Quellfeld | Zuordnungstyp | Zielfeld
---|---|---
NAME | = | msdyn\_name
BESCHREIBUNG | = | msdyn\_description
SUMBYPERIOD | \>\< | msdyn\_sumbyperiod
DISCOUNTGRACEPERIODDAYS | = | msdyn\_discountgraceperioddays
PAYMENTSTATUS | \>\< | msdyn\_paymentstatus
ALLOWPAYMENTCOPIES | \>\< | msdyn\_allowpaymentcopies
PAYMENTTYPE | \>\< | msdyn\_paymenttype
LASTFILENUMBER | = | msdyn\_lastfilenumber
LASTFILENUMBERTODAY | = | msdyn\_lastfilenumbertoday
ACCOUNTTYPE | \>\< | msdyn\_accounttype
BRIDGINGPOSTINGENABLED | \>\< | msdyn\_bridgingposting
ENABLEPOSTDATEDCHECKCLEARINGPOSTING | \>\< | msdyn\_postdatedcheckclearingposting
PROMISSORYNOTEDRAFTTYPE | \>\< | msdyn\_promissorynotedrafttype
DIRECTDEBIT | \>\< | msdyn\_directdebit

