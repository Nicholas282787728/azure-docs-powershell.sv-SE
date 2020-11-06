---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: cec626d48e5daebe04ad33b13713b56c96e27b17
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575896"
---
# <span data-ttu-id="7fae4-101">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7fae4-101">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="7fae4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7fae4-102">SYNOPSIS</span></span>
<span data-ttu-id="7fae4-103">Aktiverar replikering för ett skrivskyddat ASR-objekt genom att skapa ett replikerat objekt</span><span class="sxs-lookup"><span data-stu-id="7fae4-103">Enables replication for an ASR protectable item by creating a replication protected item</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7fae4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7fae4-104">SYNTAX</span></span>

### <span data-ttu-id="7fae4-105">Avaktiverare (standard)</span><span class="sxs-lookup"><span data-stu-id="7fae4-105">DisableDR (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-WaitForCompletion] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7fae4-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="7fae4-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-WaitForCompletion] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7fae4-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="7fae4-107">EnterpriseToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -RecoveryAzureStorageAccountId <String>
 -RecoveryResourceGroupId <String> [-WaitForCompletion] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fae4-108">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="7fae4-108">HyperVSiteToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -RecoveryAzureStorageAccountId <String>
 -OSDiskName <String> -OS <String> -RecoveryResourceGroupId <String> [-WaitForCompletion] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7fae4-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7fae4-109">DESCRIPTION</span></span>
<span data-ttu-id="7fae4-110">Cmdleten **New-AzureRmRecoveryServicesAsrReplicationProtectedItem** skapar ett nytt replikerat objekt.</span><span class="sxs-lookup"><span data-stu-id="7fae4-110">The **New-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet creates a new replication protected item.</span></span>
<span data-ttu-id="7fae4-111">Använd denna cmdlet för att aktivera replikering för ett skrivskyddat objekt i ASR.</span><span class="sxs-lookup"><span data-stu-id="7fae4-111">Use this cmdlet to enable replication for an ASR protectable item.</span></span>

## <span data-ttu-id="7fae4-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7fae4-112">EXAMPLES</span></span>

### <span data-ttu-id="7fae4-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7fae4-113">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem $VM -Name $VM.Name -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="7fae4-114">Startar åtgärden för att skapa replikerat objekt för det angivna ASR-objektet och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="7fae4-114">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="7fae4-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7fae4-115">PARAMETERS</span></span>

### <span data-ttu-id="7fae4-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="7fae4-116">-Name</span></span>
<span data-ttu-id="7fae4-117">Anger ett namn för det skyddade objektet för ASR-replikering.</span><span class="sxs-lookup"><span data-stu-id="7fae4-117">Specifies a name for the ASR replication protected item.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fae4-118">-OS</span><span class="sxs-lookup"><span data-stu-id="7fae4-118">-OS</span></span>
<span data-ttu-id="7fae4-119">Anger operativ system familjen.</span><span class="sxs-lookup"><span data-stu-id="7fae4-119">Specifies the operating system family.</span></span>
<span data-ttu-id="7fae4-120">De acceptabla värdena för denna parameter är: Windows eller Linux.</span><span class="sxs-lookup"><span data-stu-id="7fae4-120">The acceptable values for this parameter are: Windows or Linux.</span></span>

```yaml
Type: String
Parameter Sets: HyperVSiteToAzure
Aliases: 
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fae4-121">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="7fae4-121">-OSDiskName</span></span>
<span data-ttu-id="7fae4-122">Anger namnet på operativ system disken.</span><span class="sxs-lookup"><span data-stu-id="7fae4-122">Specifies the name of the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fae4-123">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="7fae4-123">-ProtectableItem</span></span>
<span data-ttu-id="7fae4-124">Anger objektet för skyddad ASR-objekt där replikering aktive ras.</span><span class="sxs-lookup"><span data-stu-id="7fae4-124">Specifies the ASR protectable item object for which replication is being enabled.</span></span>

```yaml
Type: ASRProtectableItem
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7fae4-125">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="7fae4-125">-ProtectionContainerMapping</span></span>
<span data-ttu-id="7fae4-126">Anger det mappnings objekt för ASR-skyddsagenten som motsvarar den replikeringsprincip som ska användas för replikering.</span><span class="sxs-lookup"><span data-stu-id="7fae4-126">Specifies the ASR protection container mapping object corresponding to the replication policy to be used for replication.</span></span>

```yaml
Type: ASRProtectionContainerMapping
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fae4-127">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="7fae4-127">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="7fae4-128">Anger ID för det Azure Storage-konto som ska replikeras till.</span><span class="sxs-lookup"><span data-stu-id="7fae4-128">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fae4-129">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="7fae4-129">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="7fae4-130">Anger ARM-identifieraren för den resurs grupp i vilken den virtuella datorn ska skapas i händelse av en failover.</span><span class="sxs-lookup"><span data-stu-id="7fae4-130">Specifies the ARM identifier of the resource group in which the virtual machine will be created in the event of a failover.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fae4-131">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="7fae4-131">-WaitForCompletion</span></span>
<span data-ttu-id="7fae4-132">Anger att cmdleten ska vänta på att åtgärden slutförs innan den returneras.</span><span class="sxs-lookup"><span data-stu-id="7fae4-132">Specifies that the cmdlet should wait for completion of the operation before returning.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fae4-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7fae4-133">-Confirm</span></span>
<span data-ttu-id="7fae4-134">Uppmaningar om att bekräfta innan operationen startas.</span><span class="sxs-lookup"><span data-stu-id="7fae4-134">Prompts  for confirmation before starting the operation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fae4-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fae4-135">-WhatIf</span></span>
<span data-ttu-id="7fae4-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7fae4-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7fae4-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7fae4-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fae4-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fae4-138">CommonParameters</span></span>
<span data-ttu-id="7fae4-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fae4-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fae4-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fae4-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fae4-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7fae4-141">INPUTS</span></span>

### <span data-ttu-id="7fae4-142">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="7fae4-142">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="7fae4-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7fae4-143">OUTPUTS</span></span>

### <span data-ttu-id="7fae4-144">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="7fae4-144">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="7fae4-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7fae4-145">NOTES</span></span>

## <span data-ttu-id="7fae4-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7fae4-146">RELATED LINKS</span></span>

[<span data-ttu-id="7fae4-147">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7fae4-147">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="7fae4-148">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7fae4-148">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="7fae4-149">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7fae4-149">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
