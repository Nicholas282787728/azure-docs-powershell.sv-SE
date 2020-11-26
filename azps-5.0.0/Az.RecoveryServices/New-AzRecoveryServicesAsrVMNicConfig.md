---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrvmnicconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrVMNicConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrVMNicConfig.md
ms.openlocfilehash: 658a0cfa66abd71a63edc67ab2615713ac815bcd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270272"
---
# <span data-ttu-id="6611e-101">New-AzRecoveryServicesAsrVMNicConfig</span><span class="sxs-lookup"><span data-stu-id="6611e-101">New-AzRecoveryServicesAsrVMNicConfig</span></span>

## <span data-ttu-id="6611e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6611e-102">SYNOPSIS</span></span>
<span data-ttu-id="6611e-103">Skapar en ASR NIC-konfiguration som innehåller redundans-och testredundans-relaterade konfigurations uppgifter.</span><span class="sxs-lookup"><span data-stu-id="6611e-103">Creates an ASR NIC config that contains the failover and test failover related configuration details.</span></span>

## <span data-ttu-id="6611e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6611e-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrVMNicConfig -NicId <String> -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-RecoveryVMNetworkId <String>] [-RecoveryNicName <String>] [-RecoveryNicResourceGroupName <String>]
 [-ReuseExistingNic] [-RecoveryVMSubnetName <String>] [-RecoveryNetworkSecurityGroupId <String>]
 [-EnableAcceleratedNetworkingOnRecovery] [-RecoveryNicStaticIPAddress <String>]
 [-RecoveryPublicIPAddressId <String>] [-RecoveryLBBackendAddressPoolId <String[]>] [-TfoVMNetworkId <String>]
 [-TfoNicName <String>] [-TfoNicResourceGroupName <String>] [-TfoReuseExistingNic] [-TfoVMSubnetName <String>]
 [-TfoNetworkSecurityGroupId <String>] [-EnableAcceleratedNetworkingOnTfo] [-TfoNicStaticIPAddress <String>]
 [-TfoPublicIPAddressId <String>] [-TfoLBBackendAddressPoolId <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6611e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6611e-105">DESCRIPTION</span></span>
<span data-ttu-id="6611e-106">Cmdleten **New-AzRecoveryServicesAsrVMNicConfig** skapar ett ASR NIC-konfigurationsobjekt som innehåller information om redundans och testning av redundans.</span><span class="sxs-lookup"><span data-stu-id="6611e-106">The **New-AzRecoveryServicesAsrVMNicConfig** cmdlet creates an ASR NIC config object that contains the failover and test failover related details.</span></span> <span data-ttu-id="6611e-107">Om ingen information skickas, sparas motsvarande värden från det replikerade objektet för att undvika att dessa värden uppdateras till null.</span><span class="sxs-lookup"><span data-stu-id="6611e-107">In case any information is not passed, the corresponding values are picked from the replication protected item to avoid these values being updated to null.</span></span>

## <span data-ttu-id="6611e-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6611e-108">EXAMPLES</span></span>

### <span data-ttu-id="6611e-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6611e-109">Example 1</span></span>
```powershell
PS C:\> $nicConfig = New-AzRecoveryServicesAsrVMNicConfig -NicId $AsrNicGuid -ReplicationProtectedItem $Rpi -RecoveryVMNetworkId $recoveryNetworkId -RecoveryVMSubnetName $recoverySubnetName -RecoveryNicStaticIPAddress "10.0.0.1" `
    -TfoVMNetworkId $tfoNetworkId -TfoVMSubnetName $tfoSubnetName -TfoNicStaticIPAddress "10.0.1.1"
```

<span data-ttu-id="6611e-110">Skapar ett ASRVmNicConfig-objekt med inställningarna för failover och test faiover nätverks inställningar som har kon figurer ATS för NÄTVERKSKORTet.</span><span class="sxs-lookup"><span data-stu-id="6611e-110">Creates an ASRVmNicConfig object with the failover and test faiover networking settings configured for the NIC.</span></span> <span data-ttu-id="6611e-111">Eventuella egenskaper som inte skickades ovan hämtas från det skyddade objektet.</span><span class="sxs-lookup"><span data-stu-id="6611e-111">Any property that's not passed above is fetched from the protected item passed.</span></span>

### <span data-ttu-id="6611e-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="6611e-112">Example 2</span></span>
```powershell
PS C:\> $nicConfig = New-AzRecoveryServicesAsrVMNicConfig -NicId $AsrNicGuid -ReplicationProtectedItem $Rpi -TfoNicName $TfoNicName -TfoNicResourceGroupName $TfoNicRgName -TfoReuseExistingNic
```

<span data-ttu-id="6611e-113">Skapar ett ASRVmNicConfig-objekt med test faiover nätverks inställningar som har kon figurer ATS för att byta namn på NÄTVERKSKORTet.</span><span class="sxs-lookup"><span data-stu-id="6611e-113">Creates an ASRVmNicConfig object with the test faiover networking settings configured for the NIC renaming.</span></span> <span data-ttu-id="6611e-114">Eventuella egenskaper som inte skickades ovan hämtas från det skyddade objektet.</span><span class="sxs-lookup"><span data-stu-id="6611e-114">Any property that's not passed above is fetched from the protected item passed.</span></span>


### <span data-ttu-id="6611e-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="6611e-115">Example 3</span></span>

<span data-ttu-id="6611e-116">Skapar en ASR NIC-konfiguration som innehåller redundans-och testredundans-relaterade konfigurations uppgifter.</span><span class="sxs-lookup"><span data-stu-id="6611e-116">Creates an ASR NIC config that contains the failover and test failover related configuration details.</span></span> <span data-ttu-id="6611e-117">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="6611e-117">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzRecoveryServicesAsrVMNicConfig -NicId $AsrNicGuid -RecoveryNetworkSecurityGroupId <String> -RecoveryNicStaticIPAddress '10.0.0.1' -RecoveryVMNetworkId $recoveryNetworkId -RecoveryVMSubnetName $recoverySubnetName -ReplicationProtectedItem $Rpi -TfoNetworkSecurityGroupId <String> -TfoNicStaticIPAddress <String> -TfoVMNetworkId <String> -TfoVMSubnetName <String>
```

## <span data-ttu-id="6611e-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6611e-118">PARAMETERS</span></span>

### <span data-ttu-id="6611e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6611e-119">-DefaultProfile</span></span>
<span data-ttu-id="6611e-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6611e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6611e-121">-EnableAcceleratedNetworkingOnRecovery</span><span class="sxs-lookup"><span data-stu-id="6611e-121">-EnableAcceleratedNetworkingOnRecovery</span></span>
<span data-ttu-id="6611e-122">Anger om accelererade nätverk är aktiverat på Recovery NIC.</span><span class="sxs-lookup"><span data-stu-id="6611e-122">Specifies whether accelerated networking is enabled on recovery NIC.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6611e-123">-EnableAcceleratedNetworkingOnTfo</span><span class="sxs-lookup"><span data-stu-id="6611e-123">-EnableAcceleratedNetworkingOnTfo</span></span>
<span data-ttu-id="6611e-124">Anger om snabb anslutning är aktiverat för testa redundans-NIC.</span><span class="sxs-lookup"><span data-stu-id="6611e-124">Specifies whether accelerated networking is enabled on test failover NIC.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6611e-125">-NicId</span><span class="sxs-lookup"><span data-stu-id="6611e-125">-NicId</span></span>
<span data-ttu-id="6611e-126">Ange GUID för ASR-NÄTVERKSKORTet.</span><span class="sxs-lookup"><span data-stu-id="6611e-126">Specify the ASR NIC GUID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6611e-127">-RecoveryLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="6611e-127">-RecoveryLBBackendAddressPoolId</span></span>
<span data-ttu-id="6611e-128">Anger ID-numren för backend-adresspoolen för Recovery-NÄTVERKSKORTet.</span><span class="sxs-lookup"><span data-stu-id="6611e-128">Specifies the IDs of backend address pools for the recovery NIC.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6611e-129">-RecoveryNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="6611e-129">-RecoveryNetworkSecurityGroupId</span></span>
<span data-ttu-id="6611e-130">Anger ID för det NSG som är kopplat till återställnings kortet.</span><span class="sxs-lookup"><span data-stu-id="6611e-130">Specifies the ID of the NSG associated with recovery NIC.</span></span>

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

### <span data-ttu-id="6611e-131">-RecoveryNicName</span><span class="sxs-lookup"><span data-stu-id="6611e-131">-RecoveryNicName</span></span>
<span data-ttu-id="6611e-132">Anger namnet på återställnings kortet.</span><span class="sxs-lookup"><span data-stu-id="6611e-132">Specifies the name of the recovery NIC.</span></span>

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

### <span data-ttu-id="6611e-133">-RecoveryNicResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6611e-133">-RecoveryNicResourceGroupName</span></span>
<span data-ttu-id="6611e-134">Anger namnet på resurs gruppen för Recovery NIC.</span><span class="sxs-lookup"><span data-stu-id="6611e-134">Specifies the name of the recovery NIC resource group.</span></span>

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

### <span data-ttu-id="6611e-135">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="6611e-135">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="6611e-136">Anger IP-adressen för återställnings kortet.</span><span class="sxs-lookup"><span data-stu-id="6611e-136">Specifies the IP address of the recovery NIC.</span></span>

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

### <span data-ttu-id="6611e-137">-RecoveryPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="6611e-137">-RecoveryPublicIPAddressId</span></span>
<span data-ttu-id="6611e-138">Anger ID: t för den offentliga IP-adress som är kopplad till återställnings kortet.</span><span class="sxs-lookup"><span data-stu-id="6611e-138">Specifies the ID of the public IP address associated with recovery NIC.</span></span>

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

### <span data-ttu-id="6611e-139">-RecoveryVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="6611e-139">-RecoveryVMNetworkId</span></span>
<span data-ttu-id="6611e-140">Anger ID för det virtuella återställnings nätverket.</span><span class="sxs-lookup"><span data-stu-id="6611e-140">Specifies the ID of the recovery virtual network.</span></span>

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

### <span data-ttu-id="6611e-141">-RecoveryVMSubnetName</span><span class="sxs-lookup"><span data-stu-id="6611e-141">-RecoveryVMSubnetName</span></span>
<span data-ttu-id="6611e-142">Anger namnet på återställnings nätet.</span><span class="sxs-lookup"><span data-stu-id="6611e-142">Specifies the name of the recovery subnet.</span></span>

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

### <span data-ttu-id="6611e-143">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="6611e-143">-ReplicationProtectedItem</span></span>
<span data-ttu-id="6611e-144">Ange skyddat objekt för ASR-replikering.</span><span class="sxs-lookup"><span data-stu-id="6611e-144">Specify the ASR Replication Protected Item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6611e-145">-ReuseExistingNic</span><span class="sxs-lookup"><span data-stu-id="6611e-145">-ReuseExistingNic</span></span>
<span data-ttu-id="6611e-146">Anger om ett befintligt nätverkskort kan användas under redundans.</span><span class="sxs-lookup"><span data-stu-id="6611e-146">Specifies whether an existing NIC can be used during failover.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6611e-147">-TfoLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="6611e-147">-TfoLBBackendAddressPoolId</span></span>
<span data-ttu-id="6611e-148">Anger ID-numren för backend-adresspoolen för Recovery-NÄTVERKSKORTet.</span><span class="sxs-lookup"><span data-stu-id="6611e-148">Specifies the IDs of backend address pools for the recovery NIC.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6611e-149">-TfoNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="6611e-149">-TfoNetworkSecurityGroupId</span></span>
<span data-ttu-id="6611e-150">Anger ID för det NSG som är kopplat till testa redundans-NIC.</span><span class="sxs-lookup"><span data-stu-id="6611e-150">Specifies the ID of the NSG associated with test failover NIC.</span></span>

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

### <span data-ttu-id="6611e-151">-TfoNicName</span><span class="sxs-lookup"><span data-stu-id="6611e-151">-TfoNicName</span></span>
<span data-ttu-id="6611e-152">Anger namnet på testredundans NIC.</span><span class="sxs-lookup"><span data-stu-id="6611e-152">Specifies the name of the test failover NIC.</span></span>

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

### <span data-ttu-id="6611e-153">-TfoNicResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6611e-153">-TfoNicResourceGroupName</span></span>
<span data-ttu-id="6611e-154">Anger namnet på resursen för testa redundans-NIC.</span><span class="sxs-lookup"><span data-stu-id="6611e-154">Specifies the name of the test failover NIC resource group.</span></span>

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

### <span data-ttu-id="6611e-155">-TfoNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="6611e-155">-TfoNicStaticIPAddress</span></span>
<span data-ttu-id="6611e-156">Anger IP-adressen för testredundans-NIC.</span><span class="sxs-lookup"><span data-stu-id="6611e-156">Specifies the IP address of the test failover NIC.</span></span>

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

### <span data-ttu-id="6611e-157">-TfoPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="6611e-157">-TfoPublicIPAddressId</span></span>
<span data-ttu-id="6611e-158">Anger ID: t för den offentliga IP-adressen som är kopplad till redundanstestning för testning av redundans.</span><span class="sxs-lookup"><span data-stu-id="6611e-158">Specifies the ID of the public IP address associated with test failover NIC.</span></span>

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

### <span data-ttu-id="6611e-159">-TfoReuseExistingNic</span><span class="sxs-lookup"><span data-stu-id="6611e-159">-TfoReuseExistingNic</span></span>
<span data-ttu-id="6611e-160">Anger om ett befintligt nätverkskort kan användas under testning av redundans.</span><span class="sxs-lookup"><span data-stu-id="6611e-160">Specifies whether an existing NIC can be used during test failover.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6611e-161">-TfoVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="6611e-161">-TfoVMNetworkId</span></span>
<span data-ttu-id="6611e-162">Anger ID för det virtuella nätverket för redundanstest.</span><span class="sxs-lookup"><span data-stu-id="6611e-162">Specifies the ID of the test failover virtual network.</span></span>

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

### <span data-ttu-id="6611e-163">-TfoVMSubnetName</span><span class="sxs-lookup"><span data-stu-id="6611e-163">-TfoVMSubnetName</span></span>
<span data-ttu-id="6611e-164">Anger namnet på redundanstestning för redundanstest.</span><span class="sxs-lookup"><span data-stu-id="6611e-164">Specifies the name of the test failover subnet.</span></span>

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

### <span data-ttu-id="6611e-165">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6611e-165">-Confirm</span></span>
<span data-ttu-id="6611e-166">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6611e-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6611e-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6611e-167">-WhatIf</span></span>
<span data-ttu-id="6611e-168">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6611e-168">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6611e-169">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6611e-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6611e-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6611e-170">CommonParameters</span></span>
<span data-ttu-id="6611e-171">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6611e-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6611e-172">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6611e-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6611e-173">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6611e-173">INPUTS</span></span>

### <span data-ttu-id="6611e-174">Ingen</span><span class="sxs-lookup"><span data-stu-id="6611e-174">None</span></span>

## <span data-ttu-id="6611e-175">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6611e-175">OUTPUTS</span></span>

### <span data-ttu-id="6611e-176">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRVMNicConfig</span><span class="sxs-lookup"><span data-stu-id="6611e-176">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMNicConfig</span></span>

## <span data-ttu-id="6611e-177">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6611e-177">NOTES</span></span>

## <span data-ttu-id="6611e-178">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6611e-178">RELATED LINKS</span></span>