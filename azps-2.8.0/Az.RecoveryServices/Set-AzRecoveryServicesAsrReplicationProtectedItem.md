---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 11598952da67d7f3b3ec94f6c64b71c80bbad12c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920193"
---
# <span data-ttu-id="2c14f-101">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="2c14f-101">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="2c14f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2c14f-102">SYNOPSIS</span></span>
<span data-ttu-id="2c14f-103">Anger återställnings egenskaper som mål nätverk och virtuell dator storlek för det angivna replikerade objektet.</span><span class="sxs-lookup"><span data-stu-id="2c14f-103">Sets recovery properties such as target network and virtual machine size for the specified replication protected item.</span></span>

## <span data-ttu-id="2c14f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2c14f-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem> [-Name <String>]
 [-Size <String>] [-PrimaryNic <String>] [-RecoveryNetworkId <String>] [-RecoveryCloudServiceId <String>]
 [-RecoveryNicSubnetName <String>] [-RecoveryNicStaticIPAddress <String>] [-NicSelectionType <String>]
 [-RecoveryResourceGroupId <String>] [-LicenseType <String>] [-RecoveryAvailabilitySet <String>]
 [-RecoveryBootDiagStorageAccountId <String>]
 [-AzureToAzureUpdateReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]>]
 [-UseManagedDisk <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2c14f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2c14f-105">DESCRIPTION</span></span>
<span data-ttu-id="2c14f-106">Cmdleten **set-AzRecoveryServicesAsrReplicationProtectedItem** anger återställnings egenskaper för ett replikerat objekt.</span><span class="sxs-lookup"><span data-stu-id="2c14f-106">The **Set-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet sets the recovery properties for a Replication Protected Item.</span></span>

## <span data-ttu-id="2c14f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2c14f-107">EXAMPLES</span></span>

### <span data-ttu-id="2c14f-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2c14f-108">Example 1</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $RPI -PrimaryNic $NicId -RecoveryNetworkId $AzureNetworkID -RecoveryNicSubnetName $subnetName
```

<span data-ttu-id="2c14f-109">Startar åtgärden att uppdatera inställningarna för att skydda objekt med de angivna parametrarna och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="2c14f-109">Starts the operation of updating the replication protect item settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="2c14f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2c14f-110">PARAMETERS</span></span>

### <span data-ttu-id="2c14f-111">-AzureToAzureUpdateReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="2c14f-111">-AzureToAzureUpdateReplicationConfiguration</span></span>
<span data-ttu-id="2c14f-112">{{Fill AzureToAzureUpdateReplicationConfiguration Description}}</span><span class="sxs-lookup"><span data-stu-id="2c14f-112">{{Fill AzureToAzureUpdateReplicationConfiguration Description}}</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c14f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c14f-113">-DefaultProfile</span></span>
<span data-ttu-id="2c14f-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2c14f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c14f-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2c14f-115">-InputObject</span></span>
<span data-ttu-id="2c14f-116">Indatavärdet till cmdleten: objektet skyddat objekt för ASR som motsvarar det replikerade objekt som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="2c14f-116">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c14f-117">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="2c14f-117">-LicenseType</span></span>
<span data-ttu-id="2c14f-118">Ange licens typs valet för virtuella datorer med Windows Server.</span><span class="sxs-lookup"><span data-stu-id="2c14f-118">Specifiy the license type selection to be used for Windows Server virtual machines.</span></span> <span data-ttu-id="2c14f-119">Om du har rätt att använda användnings förmånen för Azure Hybrid (hubb) för migreringar och vill ange att nav-inställningen ska användas när det här skyddade objektet inte används, ställer du in licens typen på WindowsServer.</span><span class="sxs-lookup"><span data-stu-id="2c14f-119">If you are entitled to use the Azure Hybrid Use Benefit (HUB) for migrations and would like to specify that the HUB setting be used while failing over this protected item set the license type to be WindowsServer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NoLicenseType, WindowsServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c14f-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="2c14f-120">-Name</span></span>
<span data-ttu-id="2c14f-121">Anger namnet på den virtuella återställnings datorn som kommer att skapas på redundans.</span><span class="sxs-lookup"><span data-stu-id="2c14f-121">Specifies the name of the recovery virtual machine that will be created on failover.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c14f-122">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="2c14f-122">-NicSelectionType</span></span>
<span data-ttu-id="2c14f-123">Anger de nätverkskort-egenskaper som anges av användaren eller som standard.</span><span class="sxs-lookup"><span data-stu-id="2c14f-123">Specifies the network interface card (NIC) properties set by user or set by default.</span></span>
<span data-ttu-id="2c14f-124">Du kan ange NotSelected för att återgå till standardvärdena.</span><span class="sxs-lookup"><span data-stu-id="2c14f-124">You can specify NotSelected to go back to the default values.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NotSelected, SelectedByUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c14f-125">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="2c14f-125">-PrimaryNic</span></span>
<span data-ttu-id="2c14f-126">Anger NÄTVERKSKORTet för den virtuella dator för vilken denna cmdlet ställer in egenskapen för återställnings nätverk.</span><span class="sxs-lookup"><span data-stu-id="2c14f-126">Specifies the NIC of the virtual machine for which this cmdlet sets the recovery network property.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c14f-127">-RecoveryAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="2c14f-127">-RecoveryAvailabilitySet</span></span>
<span data-ttu-id="2c14f-128">Tillgänglighets uppsättning för replikerat skyddat objekt efter redundans.</span><span class="sxs-lookup"><span data-stu-id="2c14f-128">Availability set for replication protected item after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c14f-129">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="2c14f-129">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="2c14f-130">Anger lagrings konto för startdiagnostik för återställning av Azure VM.</span><span class="sxs-lookup"><span data-stu-id="2c14f-130">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c14f-131">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="2c14f-131">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="2c14f-132">Resurs-ID för återställnings moln tjänsten för att redundansväxla den här virtuella datorn till.</span><span class="sxs-lookup"><span data-stu-id="2c14f-132">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c14f-133">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="2c14f-133">-RecoveryNetworkId</span></span>
<span data-ttu-id="2c14f-134">Anger ID för det Azure Virtual Network som det skyddade objektet ska flyttas över.</span><span class="sxs-lookup"><span data-stu-id="2c14f-134">Specifies the ID of the Azure virtual network to which the protected item should be failed over.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c14f-135">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="2c14f-135">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="2c14f-136">Anger den statiska IP-adressen som ska kopplas till primär NIC vid återställning.</span><span class="sxs-lookup"><span data-stu-id="2c14f-136">Specifies the static IP address that should be assigned to primary NIC on recovery.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c14f-137">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="2c14f-137">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="2c14f-138">Anger namnet på under nätet i det virtuella Azure-nätverk som det här NÄTVERKSKORTet i det skyddade objektet ska anslutas till vid redundans.</span><span class="sxs-lookup"><span data-stu-id="2c14f-138">Specifies the name of the subnet on the recovery Azure virtual network to which this NIC of the protected item should be connected to on failover.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c14f-139">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="2c14f-139">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="2c14f-140">ID för Azure-adressresursen i det återställnings område där det skyddade objektet återställs på redundans.</span><span class="sxs-lookup"><span data-stu-id="2c14f-140">The ID of the Azure resource group in the recovery region in which the protected item will be recovered on failover.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c14f-141">-Storlek</span><span class="sxs-lookup"><span data-stu-id="2c14f-141">-Size</span></span>
<span data-ttu-id="2c14f-142">Anger storleken på den virtuella återställnings datorn.</span><span class="sxs-lookup"><span data-stu-id="2c14f-142">Specifies the recovery virtual machine size.</span></span>
<span data-ttu-id="2c14f-143">Värdet ska vara från den uppsättning storlekar som stöds av virtuella Azure-datorer.</span><span class="sxs-lookup"><span data-stu-id="2c14f-143">The value should be from the set of sizes supported by Azure virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c14f-144">-UseManagedDisk</span><span class="sxs-lookup"><span data-stu-id="2c14f-144">-UseManagedDisk</span></span>
<span data-ttu-id="2c14f-145">Anger om den virtuella Azure-datorn som skapas på redundans ska använda hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="2c14f-145">Specifies if the Azure virtual machine that is created on failover should use managed disks.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: True, False

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c14f-146">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2c14f-146">-Confirm</span></span>
<span data-ttu-id="2c14f-147">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2c14f-147">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c14f-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c14f-148">-WhatIf</span></span>
<span data-ttu-id="2c14f-149">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2c14f-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2c14f-150">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2c14f-150">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c14f-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c14f-151">CommonParameters</span></span>
<span data-ttu-id="2c14f-152">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c14f-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c14f-153">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c14f-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c14f-154">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2c14f-154">INPUTS</span></span>

### <span data-ttu-id="2c14f-155">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="2c14f-155">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="2c14f-156">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2c14f-156">OUTPUTS</span></span>

### <span data-ttu-id="2c14f-157">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="2c14f-157">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="2c14f-158">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2c14f-158">NOTES</span></span>

## <span data-ttu-id="2c14f-159">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2c14f-159">RELATED LINKS</span></span>

[<span data-ttu-id="2c14f-160">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="2c14f-160">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="2c14f-161">New-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="2c14f-161">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="2c14f-162">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="2c14f-162">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)
