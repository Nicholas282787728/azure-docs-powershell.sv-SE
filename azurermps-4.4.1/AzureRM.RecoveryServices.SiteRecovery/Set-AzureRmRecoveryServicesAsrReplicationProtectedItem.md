---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 5627b94f87d69fab6b760bf05f1e22566992048b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756883"
---
# <span data-ttu-id="4698f-101">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="4698f-101">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="4698f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4698f-102">SYNOPSIS</span></span>
<span data-ttu-id="4698f-103">Anger återställnings egenskaper som mål nätverk och virtuell dator storlek för det angivna replikerade objektet.</span><span class="sxs-lookup"><span data-stu-id="4698f-103">Sets recovery properties such as target network and virtual machine size for the specified replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4698f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4698f-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem>
 [-Name <String>] [-Size <String>] [-PrimaryNic <String>] [-RecoveryNetworkId <String>]
 [-RecoveryNicSubnetName <String>] [-RecoveryNicStaticIPAddress <String>] [-NicSelectionType <String>]
 [-RecoveryResourceGroupId <String>] [-LicenseType <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4698f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4698f-105">DESCRIPTION</span></span>
<span data-ttu-id="4698f-106">Cmdleten **set-AzureRmRecoveryServicesAsrReplicationProtectedItem** anger återställnings egenskaper för ett replikerat objekt.</span><span class="sxs-lookup"><span data-stu-id="4698f-106">The **Set-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet sets the recovery properties for a Replication Protected Item.</span></span>

## <span data-ttu-id="4698f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4698f-107">EXAMPLES</span></span>

### <span data-ttu-id="4698f-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4698f-108">Example 1</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $RPI -PrimaryNic $NicId -RecoveryNetworkId $AzureNetworkID -RecoveryNicSubnetName $subnetName
```

<span data-ttu-id="4698f-109">Startar åtgärden att uppdatera inställningarna för att skydda objekt med de angivna parametrarna och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="4698f-109">Starts the operation of updating the replication protect item settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="4698f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4698f-110">PARAMETERS</span></span>

### <span data-ttu-id="4698f-111">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4698f-111">-InputObject</span></span>
<span data-ttu-id="4698f-112">Indatavärdet till cmdleten: objektet skyddat objekt för ASR som motsvarar det replikerade objekt som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="4698f-112">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item to update.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4698f-113">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="4698f-113">-LicenseType</span></span>
<span data-ttu-id="4698f-114">Ange licens typs valet för virtuella datorer med Windows Server.</span><span class="sxs-lookup"><span data-stu-id="4698f-114">Specifiy the license type selection to be used for Windows Server virtual machines.</span></span> <span data-ttu-id="4698f-115">Om du har rätt att använda användnings förmånen för Azure Hybrid (hubb) för migreringar och vill ange att nav-inställningen ska användas när det här skyddade objektet inte används, ställer du in licens typen på WindowsServer.</span><span class="sxs-lookup"><span data-stu-id="4698f-115">If you are entitled to use the Azure Hybrid Use Benefit (HUB) for migrations and would like to specify that the HUB setting be used while failing over this protected item set the license type to be WindowsServer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: NoLicenseType, WindowsServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4698f-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="4698f-116">-Name</span></span>
<span data-ttu-id="4698f-117">Anger namnet på den virtuella återställnings datorn som kommer att skapas på redundans.</span><span class="sxs-lookup"><span data-stu-id="4698f-117">Specifies the name of the recovery virtual machine that will be created on failover.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4698f-118">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="4698f-118">-NicSelectionType</span></span>
<span data-ttu-id="4698f-119">Anger de nätverkskort-egenskaper som anges av användaren eller som standard.</span><span class="sxs-lookup"><span data-stu-id="4698f-119">Specifies the network interface card (NIC) properties set by user or set by default.</span></span>
<span data-ttu-id="4698f-120">Du kan ange NotSelected för att återgå till standardvärdena.</span><span class="sxs-lookup"><span data-stu-id="4698f-120">You can specify NotSelected to go back to the default values.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: NotSelected, SelectedByUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4698f-121">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="4698f-121">-PrimaryNic</span></span>
<span data-ttu-id="4698f-122">Anger NÄTVERKSKORTet för den virtuella dator för vilken denna cmdlet ställer in egenskapen för återställnings nätverk.</span><span class="sxs-lookup"><span data-stu-id="4698f-122">Specifies the NIC of the virtual machine for which this cmdlet sets the recovery network property.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4698f-123">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="4698f-123">-RecoveryNetworkId</span></span>
<span data-ttu-id="4698f-124">Anger ID för det Azure Virtual Network som det skyddade objektet ska flyttas över.</span><span class="sxs-lookup"><span data-stu-id="4698f-124">Specifies the ID of the Azure virtual network to which the protected item should be failed over.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4698f-125">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="4698f-125">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="4698f-126">Anger den statiska IP-adressen som ska kopplas till primär NIC vid återställning.</span><span class="sxs-lookup"><span data-stu-id="4698f-126">Specifies the static IP address that should be assigned to primary NIC on recovery.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4698f-127">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="4698f-127">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="4698f-128">Anger namnet på under nätet i det virtuella Azure-nätverk som det här NÄTVERKSKORTet i det skyddade objektet ska anslutas till vid redundans.</span><span class="sxs-lookup"><span data-stu-id="4698f-128">Specifies the name of the subnet on the recovery Azure virtual network to which this NIC of the protected item should be connected to on failover.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4698f-129">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="4698f-129">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="4698f-130">ID för Azure-adressresursen i det återställnings område där det skyddade objektet återställs på redundans.</span><span class="sxs-lookup"><span data-stu-id="4698f-130">The ID of the Azure resource group in the recovery region in which the protected item will be recovered on failover.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4698f-131">-Storlek</span><span class="sxs-lookup"><span data-stu-id="4698f-131">-Size</span></span>
<span data-ttu-id="4698f-132">Anger storleken på den virtuella återställnings datorn.</span><span class="sxs-lookup"><span data-stu-id="4698f-132">Specifies the recovery virtual machine size.</span></span>
<span data-ttu-id="4698f-133">Värdet ska vara från den uppsättning storlekar som stöds av virtuella Azure-datorer.</span><span class="sxs-lookup"><span data-stu-id="4698f-133">The value should be from the set of sizes supported by Azure virtual machines.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4698f-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4698f-134">-Confirm</span></span>
<span data-ttu-id="4698f-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4698f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4698f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4698f-136">-WhatIf</span></span>
<span data-ttu-id="4698f-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4698f-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4698f-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4698f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4698f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4698f-139">CommonParameters</span></span>
<span data-ttu-id="4698f-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4698f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4698f-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4698f-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4698f-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4698f-142">INPUTS</span></span>

### <span data-ttu-id="4698f-143">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="4698f-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="4698f-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4698f-144">OUTPUTS</span></span>

### <span data-ttu-id="4698f-145">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="4698f-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="4698f-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4698f-146">NOTES</span></span>

## <span data-ttu-id="4698f-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4698f-147">RELATED LINKS</span></span>

[<span data-ttu-id="4698f-148">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="4698f-148">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="4698f-149">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="4698f-149">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="4698f-150">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="4698f-150">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
