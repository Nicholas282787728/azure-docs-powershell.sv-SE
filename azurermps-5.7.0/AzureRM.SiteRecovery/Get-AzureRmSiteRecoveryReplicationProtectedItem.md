---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 99196F44-F1DB-4219-91C0-3056624ADE5B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryReplicationProtectedItem.md
ms.openlocfilehash: 210b8ca6d8165049edc190e24e4a435046e1461e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757210"
---
# <span data-ttu-id="15528-101">Get-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="15528-101">Get-AzureRmSiteRecoveryReplicationProtectedItem</span></span>

## <span data-ttu-id="15528-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="15528-102">SYNOPSIS</span></span>
<span data-ttu-id="15528-103">Hämtar egenskaperna för skyddat Azure Site Recovery-objekt.</span><span class="sxs-lookup"><span data-stu-id="15528-103">Gets the properties of Azure Site Recovery Protected Items.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15528-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="15528-104">SYNTAX</span></span>

### <span data-ttu-id="15528-105">ByObject (standard)</span><span class="sxs-lookup"><span data-stu-id="15528-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryReplicationProtectedItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15528-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="15528-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryReplicationProtectedItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15528-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="15528-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryReplicationProtectedItem -FriendlyName <String>
 -ProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15528-108">ByProtectableItemObject</span><span class="sxs-lookup"><span data-stu-id="15528-108">ByProtectableItemObject</span></span>
```
Get-AzureRmSiteRecoveryReplicationProtectedItem -ProtectableItem <ASRProtectableItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15528-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="15528-109">DESCRIPTION</span></span>
<span data-ttu-id="15528-110">Cmdleten **Get-AzureRmSiteRecoveryReplicationProtectedItem** hämtar egenskaperna för skyddat Azure Site Recovery-objekt.</span><span class="sxs-lookup"><span data-stu-id="15528-110">The **Get-AzureRmSiteRecoveryReplicationProtectedItem** cmdlet gets the properties of Azure Site Recovery Protected Items.</span></span>

## <span data-ttu-id="15528-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="15528-111">EXAMPLES</span></span>

## <span data-ttu-id="15528-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="15528-112">PARAMETERS</span></span>

### <span data-ttu-id="15528-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15528-113">-DefaultProfile</span></span>
<span data-ttu-id="15528-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="15528-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15528-115">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="15528-115">-FriendlyName</span></span>
<span data-ttu-id="15528-116">Anger det egna namnet på det replikerade objekt som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="15528-116">Specifies the friendly name of the Replication Protected Item that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15528-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="15528-117">-Name</span></span>
<span data-ttu-id="15528-118">Anger namnet på det replikerade objekt som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="15528-118">Specifies the name of the Replication Protected Item that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15528-119">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="15528-119">-ProtectableItem</span></span>
<span data-ttu-id="15528-120">Anger det skydd bara objekt som motsvarar det replikerade objektet.</span><span class="sxs-lookup"><span data-stu-id="15528-120">Specifies the Protectable Item corresponding to the Replication Protected Item.</span></span>

```yaml
Type: ASRProtectableItem
Parameter Sets: ByProtectableItemObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15528-121">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="15528-121">-ProtectionContainer</span></span>
<span data-ttu-id="15528-122">Anger objekt för objektet för Azure Site Recovery-skyddet.</span><span class="sxs-lookup"><span data-stu-id="15528-122">Specifies the Azure Site Recovery Protection Container object.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: ByObject, ByObjectWithName, ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15528-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15528-123">CommonParameters</span></span>
<span data-ttu-id="15528-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15528-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15528-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15528-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15528-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="15528-126">INPUTS</span></span>

### <span data-ttu-id="15528-127">ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="15528-127">ASRProtectableItem</span></span>
<span data-ttu-id="15528-128">Parametern ' ProtectableItem ' godkänner värdet av typen ' ASRProtectableItem ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="15528-128">Parameter 'ProtectableItem' accepts value of type 'ASRProtectableItem' from the pipeline</span></span>

### <span data-ttu-id="15528-129">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="15528-129">ASRProtectionContainer</span></span>
<span data-ttu-id="15528-130">Parametern ' ProtectionContainer ' godkänner värdet av typen ' ASRProtectionContainer ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="15528-130">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="15528-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="15528-131">OUTPUTS</span></span>

### <span data-ttu-id="15528-132">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. SiteRecovery. ASRReplicationProtectedItem, Microsoft. Azure. commands. SiteRecovery, version = 2.0.1.0; Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="15528-132">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="15528-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="15528-133">NOTES</span></span>

## <span data-ttu-id="15528-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="15528-134">RELATED LINKS</span></span>

[<span data-ttu-id="15528-135">New-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="15528-135">New-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./New-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="15528-136">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="15528-136">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Remove-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="15528-137">Set-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="15528-137">Set-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Set-AzureRmSiteRecoveryReplicationProtectedItem.md)
