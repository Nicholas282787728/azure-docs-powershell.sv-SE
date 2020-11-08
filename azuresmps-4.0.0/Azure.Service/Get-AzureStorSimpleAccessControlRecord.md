---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 71302FB6-7E2B-4972-A743-AB537AC7CD79
online version: ''
schema: 2.0.0
ms.openlocfilehash: 79e194e0f8dda4392dec191881702c680bf172ac
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099782"
---
# <span data-ttu-id="9a88b-101">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="9a88b-101">Get-AzureStorSimpleAccessControlRecord</span></span>

## <span data-ttu-id="9a88b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9a88b-102">SYNOPSIS</span></span>
<span data-ttu-id="9a88b-103">Hämtar åtkomst kontroll poster i en tjänst konfiguration.</span><span class="sxs-lookup"><span data-stu-id="9a88b-103">Gets access control records in a service configuration.</span></span>

## <span data-ttu-id="9a88b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9a88b-104">SYNTAX</span></span>

```
Get-AzureStorSimpleAccessControlRecord [-ACRName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9a88b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9a88b-105">DESCRIPTION</span></span>
<span data-ttu-id="9a88b-106">Cmdleten **Get-AzureStorSimpleAccessControlRecord** hämtar åtkomst kontroll poster i StorSimple Manager-tjänstens konfiguration.</span><span class="sxs-lookup"><span data-stu-id="9a88b-106">The **Get-AzureStorSimpleAccessControlRecord** cmdlet gets access control records in the StorSimple Manager service configuration.</span></span>
<span data-ttu-id="9a88b-107">Denna cmdlet hämtar alla poster eller en namngiven post.</span><span class="sxs-lookup"><span data-stu-id="9a88b-107">This cmdlet gets all records or a named record.</span></span>

<span data-ttu-id="9a88b-108">Åtkomst kontroll poster är behållare för iSCSI Initiator-parametrar.</span><span class="sxs-lookup"><span data-stu-id="9a88b-108">Access control records are containers of iSCSI initiator parameters.</span></span>
<span data-ttu-id="9a88b-109">Dessa parametrar anger vilka initierare som kan komma åt en volym.</span><span class="sxs-lookup"><span data-stu-id="9a88b-109">These parameters specify which initiators can access a volume.</span></span>
<span data-ttu-id="9a88b-110">När en iSCSI-initieraren försöker ansluta till en volym kontrollerar din enhet vilka åtkomst kontroll poster som har tilldelats till volymen.</span><span class="sxs-lookup"><span data-stu-id="9a88b-110">When an iSCSI initiator attempts to connect to a volume, your appliance checks the access control records assigned to that volume.</span></span>
<span data-ttu-id="9a88b-111">Om parametrarna för iSCSI-initieraren matchar en av posterna i en åtkomst kontroll post som mappats till den volymen kan iSCSI-initieraren ansluta.</span><span class="sxs-lookup"><span data-stu-id="9a88b-111">If the iSCSI initiator parameters match one of the entries in an access control record mapped to that volume, the iSCSI initiator can connect.</span></span>

## <span data-ttu-id="9a88b-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9a88b-112">EXAMPLES</span></span>

### <span data-ttu-id="9a88b-113">Exempel 1: Hämta alla åtkomst kontroll poster</span><span class="sxs-lookup"><span data-stu-id="9a88b-113">Example 1: Get all access control records</span></span>
```
PS C:\>Get-AzureStorSimpleAccessControlRecord
InstanceId                           Name                        InitiatorName               VolumeCount
----------                           ----                        -------------               -----------
01a31aa5-14de-4b77-b926-2842577f540e Windows_XYUSFL718-RV_ACR    iqn.1991-05.com.microsof... 3
071c282d-0cd2-4c5f-b687-48966037ba48 Linux_XYUSFL719_ACR         iqn.1994-05.com.redhat:a... 3
4600eade-71f8-4d04-baec-0e7cf1d1e8fb Windows_XYUSFL720_ACR       iqn.1991-05.com.microsof... 9
d508d6f0-fcda-4624-b223-c0b307d6113e Linux_XYUSFL350_ACR         iqn.1991-05.com.microsof... 9
```

<span data-ttu-id="9a88b-114">Det här kommandot får alla åtkomst kontroll poster.</span><span class="sxs-lookup"><span data-stu-id="9a88b-114">This command gets all access control records.</span></span>

### <span data-ttu-id="9a88b-115">Exempel 2: Hämta en specifik åtkomst kontroll post</span><span class="sxs-lookup"><span data-stu-id="9a88b-115">Example 2: Get a specific access control record</span></span>
```
PS C:\>Get-AzureStorSimpleAccessControlRecord -ACRName "Acr11"
VERBOSE: ClientRequestId: 61f261c7-acd3-4bcc-922a-ddfd85eb767b_PS
VERBOSE: ClientRequestId: 49c6a4c7-d299-46fd-a553-034c52b47487_PS

GlobalId            : 
InitiatorName       : iqn-contoso63
InstanceId          : 55f24643-ab3a-4098-ade2-aa2b1a3ab18c
Name                : Acr11
OperationInProgress : None
VolumeCount         : 6

VERBOSE: Access Control Record with given name Acr11 is found!
```

<span data-ttu-id="9a88b-116">Det här kommandot får åtkomst kontroll posten med namnet Acr11.</span><span class="sxs-lookup"><span data-stu-id="9a88b-116">This command gets the access control record named Acr11.</span></span>

## <span data-ttu-id="9a88b-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9a88b-117">PARAMETERS</span></span>

### <span data-ttu-id="9a88b-118">-ACRName</span><span class="sxs-lookup"><span data-stu-id="9a88b-118">-ACRName</span></span>
<span data-ttu-id="9a88b-119">Anger namnet på en åtkomst kontroll post som ska visas.</span><span class="sxs-lookup"><span data-stu-id="9a88b-119">Specifies the name of an access control record to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a88b-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="9a88b-120">-Profile</span></span>
<span data-ttu-id="9a88b-121">Anger en Azure-profil.</span><span class="sxs-lookup"><span data-stu-id="9a88b-121">Specifies an Azure profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a88b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a88b-122">CommonParameters</span></span>
<span data-ttu-id="9a88b-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a88b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a88b-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a88b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a88b-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9a88b-125">INPUTS</span></span>

### <span data-ttu-id="9a88b-126">Ingen</span><span class="sxs-lookup"><span data-stu-id="9a88b-126">None</span></span>

## <span data-ttu-id="9a88b-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9a88b-127">OUTPUTS</span></span>

### <span data-ttu-id="9a88b-128">AccessControlRecord, IList\<AccessControlRecord\></span><span class="sxs-lookup"><span data-stu-id="9a88b-128">AccessControlRecord, IList\<AccessControlRecord\></span></span>
<span data-ttu-id="9a88b-129">Denna cmdlet returnerar ett **AccessControlRecord** -objekt eller **ett \<AccessControlRecord\> ilist** -objekt.</span><span class="sxs-lookup"><span data-stu-id="9a88b-129">This cmdlet returns an **AccessControlRecord** object or an **IList\<AccessControlRecord\>** object.</span></span>
<span data-ttu-id="9a88b-130">Ett **AccessControlRecord** -objekt innehåller följande fält:</span><span class="sxs-lookup"><span data-stu-id="9a88b-130">An **AccessControlRecord** object contains the following fields:</span></span> 

- <span data-ttu-id="9a88b-131">**GlobalId** ( **sträng** )</span><span class="sxs-lookup"><span data-stu-id="9a88b-131">**GlobalId** ( **String** )</span></span> 
- <span data-ttu-id="9a88b-132">**InitiatorName** ( **sträng** )</span><span class="sxs-lookup"><span data-stu-id="9a88b-132">**InitiatorName** ( **String** )</span></span> 
- <span data-ttu-id="9a88b-133">**InstanceID** ( **sträng** )</span><span class="sxs-lookup"><span data-stu-id="9a88b-133">**InstanceId** ( **String** )</span></span> 
- <span data-ttu-id="9a88b-134">**Namn** ( **sträng** )</span><span class="sxs-lookup"><span data-stu-id="9a88b-134">**Name** ( **String** )</span></span> 
- <span data-ttu-id="9a88b-135">**OperationInProgress** ( **OperationInProgress** )</span><span class="sxs-lookup"><span data-stu-id="9a88b-135">**OperationInProgress** ( **OperationInProgress** )</span></span> 
- <span data-ttu-id="9a88b-136">**VolumeCount** ( **int** )</span><span class="sxs-lookup"><span data-stu-id="9a88b-136">**VolumeCount** ( **int** )</span></span>

## <span data-ttu-id="9a88b-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9a88b-137">NOTES</span></span>

## <span data-ttu-id="9a88b-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9a88b-138">RELATED LINKS</span></span>

[<span data-ttu-id="9a88b-139">New-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="9a88b-139">New-AzureStorSimpleAccessControlRecord</span></span>](./New-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="9a88b-140">Remove-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="9a88b-140">Remove-AzureStorSimpleAccessControlRecord</span></span>](./Remove-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="9a88b-141">Set-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="9a88b-141">Set-AzureStorSimpleAccessControlRecord</span></span>](./Set-AzureStorSimpleAccessControlRecord.md)


