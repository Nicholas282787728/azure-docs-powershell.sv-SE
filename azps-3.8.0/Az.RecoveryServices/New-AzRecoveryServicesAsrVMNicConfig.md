---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrvmnicconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrVMNicConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrVMNicConfig.md
ms.openlocfilehash: f7b6cd7171b6f50ed0f239e733ca98f0ecd5c05a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090412"
---
# <span data-ttu-id="1ecbe-101">New-AzRecoveryServicesAsrVMNicConfig</span><span class="sxs-lookup"><span data-stu-id="1ecbe-101">New-AzRecoveryServicesAsrVMNicConfig</span></span>

## <span data-ttu-id="1ecbe-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1ecbe-102">SYNOPSIS</span></span>
<span data-ttu-id="1ecbe-103">Skapar en ASR NIC-konfiguration som innehåller redundans-och testredundans-relaterade konfigurations uppgifter.</span><span class="sxs-lookup"><span data-stu-id="1ecbe-103">Creates an ASR NIC config that contains the failover and test failover related configuration details.</span></span>

## <span data-ttu-id="1ecbe-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1ecbe-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrVMNicConfig -NicId <String> -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-RecoveryVMNetworkId <String>] [-RecoveryVMSubnetName <String>] [-RecoveryNetworkSecurityGroupId <String>]
 [-EnableAcceleratedNetworkingOnRecovery] [-RecoveryNicStaticIPAddress <String>]
 [-RecoveryPublicIPAddressId <String>] [-RecoveryLBBackendAddressPoolId <String[]>] [-TfoVMNetworkId <String>]
 [-TfoVMSubnetName <String>] [-TfoNetworkSecurityGroupId <String>] [-EnableAcceleratedNetworkingOnTfo]
 [-TfoNicStaticIPAddress <String>] [-TfoPublicIPAddressId <String>] [-TfoLBBackendAddressPoolId <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ecbe-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1ecbe-105">DESCRIPTION</span></span>
<span data-ttu-id="1ecbe-106">Cmdleten **New-AzRecoveryServicesAsrVMNicConfig** skapar ett ASR NIC-konfigurationsobjekt som innehåller information om redundans och testning av redundans.</span><span class="sxs-lookup"><span data-stu-id="1ecbe-106">The **New-AzRecoveryServicesAsrVMNicConfig** cmdlet creates an ASR NIC config object that contains the failover and test failover related details.</span></span> <span data-ttu-id="1ecbe-107">Om ingen information skickas, sparas motsvarande värden från det replikerade objektet för att undvika att dessa värden uppdateras till null.</span><span class="sxs-lookup"><span data-stu-id="1ecbe-107">In case any information is not passed, the corresponding values are picked from the replication protected item to avoid these values being updated to null.</span></span>

## <span data-ttu-id="1ecbe-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1ecbe-108">EXAMPLES</span></span>

### <span data-ttu-id="1ecbe-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1ecbe-109">Example 1</span></span>
```powershell
PS C:\> $nicConfig = New-AzRecoveryServicesAsrVMNicConfig -NicId $AsrNicGuid -ReplicationProtectedItem $Rpi -RecoveryVMNetworkId $recoveryNetworkId -RecoveryVMSubnetName $recoverySubnetName -RecoveryNicStaticIPAddress "10.0.0.1" `
    -TfoVMNetworkId $tfoNetworkId -TfoVMSubnetName $tfoSubnetName -TfoNicStaticIPAddress "10.0.1.1"
```

<span data-ttu-id="1ecbe-110">Skapar ett ASRVmNicConfig-objekt med inställningarna för failover och test faiover nätverks inställningar som har kon figurer ATS för NÄTVERKSKORTet.</span><span class="sxs-lookup"><span data-stu-id="1ecbe-110">Creates an ASRVmNicConfig object with the failover and test faiover networking settings configured for the NIC.</span></span> <span data-ttu-id="1ecbe-111">Eventuella egenskaper som inte skickades ovan hämtas från det skyddade objektet.</span><span class="sxs-lookup"><span data-stu-id="1ecbe-111">Any property that's not passed above is fetched from the protected item passed.</span></span>

## <span data-ttu-id="1ecbe-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1ecbe-112">PARAMETERS</span></span>

### <span data-ttu-id="1ecbe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ecbe-113">-DefaultProfile</span></span>
<span data-ttu-id="1ecbe-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1ecbe-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ecbe-115">-EnableAcceleratedNetworkingOnRecovery</span><span class="sxs-lookup"><span data-stu-id="1ecbe-115">-EnableAcceleratedNetworkingOnRecovery</span></span>
<span data-ttu-id="1ecbe-116">Anger om accelererade nätverk är aktiverat på Recovery NIC.</span><span class="sxs-lookup"><span data-stu-id="1ecbe-116">Specifies whether accelerated networking is enabled on recovery NIC.</span></span>

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

### <span data-ttu-id="1ecbe-117">-EnableAcceleratedNetworkingOnTfo</span><span class="sxs-lookup"><span data-stu-id="1ecbe-117">-EnableAcceleratedNetworkingOnTfo</span></span>
<span data-ttu-id="1ecbe-118">Anger om snabb anslutning är aktiverat för testa redundans-NIC.</span><span class="sxs-lookup"><span data-stu-id="1ecbe-118">Specifies whether accelerated networking is enabled on test failover NIC.</span></span>

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

### <span data-ttu-id="1ecbe-119">-NicId</span><span class="sxs-lookup"><span data-stu-id="1ecbe-119">-NicId</span></span>
<span data-ttu-id="1ecbe-120">Ange GUID för ASR-NÄTVERKSKORTet.</span><span class="sxs-lookup"><span data-stu-id="1ecbe-120">Specify the ASR NIC GUID.</span></span>

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

### <span data-ttu-id="1ecbe-121">-RecoveryLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="1ecbe-121">-RecoveryLBBackendAddressPoolId</span></span>
<span data-ttu-id="1ecbe-122">Anger ID-numren för backend-adresspoolen för Recovery-NÄTVERKSKORTet.</span><span class="sxs-lookup"><span data-stu-id="1ecbe-122">Specifies the IDs of backend address pools for the recovery NIC.</span></span>

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

### <span data-ttu-id="1ecbe-123">-RecoveryNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="1ecbe-123">-RecoveryNetworkSecurityGroupId</span></span>
<span data-ttu-id="1ecbe-124">Anger ID för det NSG som är kopplat till återställnings kortet.</span><span class="sxs-lookup"><span data-stu-id="1ecbe-124">Specifies the ID of the NSG associated with recovery NIC.</span></span>

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

### <span data-ttu-id="1ecbe-125">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="1ecbe-125">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="1ecbe-126">Anger IP-adressen för återställnings kortet.</span><span class="sxs-lookup"><span data-stu-id="1ecbe-126">Specifies the IP address of the recovery NIC.</span></span>

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

### <span data-ttu-id="1ecbe-127">-RecoveryPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="1ecbe-127">-RecoveryPublicIPAddressId</span></span>
<span data-ttu-id="1ecbe-128">Anger ID: t för den offentliga IP-adress som är kopplad till återställnings kortet.</span><span class="sxs-lookup"><span data-stu-id="1ecbe-128">Specifies the ID of the public IP address associated with recovery NIC.</span></span>

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

### <span data-ttu-id="1ecbe-129">-RecoveryVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="1ecbe-129">-RecoveryVMNetworkId</span></span>
<span data-ttu-id="1ecbe-130">Anger ID för det virtuella återställnings nätverket.</span><span class="sxs-lookup"><span data-stu-id="1ecbe-130">Specifies the ID of the recovery virtual network.</span></span>

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

### <span data-ttu-id="1ecbe-131">-RecoveryVMSubnetName</span><span class="sxs-lookup"><span data-stu-id="1ecbe-131">-RecoveryVMSubnetName</span></span>
<span data-ttu-id="1ecbe-132">Anger namnet på återställnings nätet.</span><span class="sxs-lookup"><span data-stu-id="1ecbe-132">Specifies the name of the recovery subnet.</span></span>

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

### <span data-ttu-id="1ecbe-133">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1ecbe-133">-ReplicationProtectedItem</span></span>
<span data-ttu-id="1ecbe-134">Ange skyddat objekt för ASR-replikering.</span><span class="sxs-lookup"><span data-stu-id="1ecbe-134">Specify the ASR Replication Protected Item.</span></span>

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

### <span data-ttu-id="1ecbe-135">-TfoLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="1ecbe-135">-TfoLBBackendAddressPoolId</span></span>
<span data-ttu-id="1ecbe-136">Anger ID-numren för backend-adresspoolen för Recovery-NÄTVERKSKORTet.</span><span class="sxs-lookup"><span data-stu-id="1ecbe-136">Specifies the IDs of backend address pools for the recovery NIC.</span></span>

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

### <span data-ttu-id="1ecbe-137">-TfoNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="1ecbe-137">-TfoNetworkSecurityGroupId</span></span>
<span data-ttu-id="1ecbe-138">Anger ID för det NSG som är kopplat till testa redundans-NIC.</span><span class="sxs-lookup"><span data-stu-id="1ecbe-138">Specifies the ID of the NSG associated with test failover NIC.</span></span>

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

### <span data-ttu-id="1ecbe-139">-TfoNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="1ecbe-139">-TfoNicStaticIPAddress</span></span>
<span data-ttu-id="1ecbe-140">Anger IP-adressen för testredundans-NIC.</span><span class="sxs-lookup"><span data-stu-id="1ecbe-140">Specifies the IP address of the test failover NIC.</span></span>

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

### <span data-ttu-id="1ecbe-141">-TfoPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="1ecbe-141">-TfoPublicIPAddressId</span></span>
<span data-ttu-id="1ecbe-142">Anger ID: t för den offentliga IP-adressen som är kopplad till redundanstestning för testning av redundans.</span><span class="sxs-lookup"><span data-stu-id="1ecbe-142">Specifies the ID of the public IP address associated with test failover NIC.</span></span>

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

### <span data-ttu-id="1ecbe-143">-TfoVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="1ecbe-143">-TfoVMNetworkId</span></span>
<span data-ttu-id="1ecbe-144">Anger ID för det virtuella nätverket för redundanstest.</span><span class="sxs-lookup"><span data-stu-id="1ecbe-144">Specifies the ID of the test failover virtual network.</span></span>

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

### <span data-ttu-id="1ecbe-145">-TfoVMSubnetName</span><span class="sxs-lookup"><span data-stu-id="1ecbe-145">-TfoVMSubnetName</span></span>
<span data-ttu-id="1ecbe-146">Anger namnet på redundanstestning för redundanstest.</span><span class="sxs-lookup"><span data-stu-id="1ecbe-146">Specifies the name of the test failover subnet.</span></span>

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

### <span data-ttu-id="1ecbe-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ecbe-147">CommonParameters</span></span>
<span data-ttu-id="1ecbe-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ecbe-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ecbe-149">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1ecbe-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ecbe-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1ecbe-150">INPUTS</span></span>

### <span data-ttu-id="1ecbe-151">Ingen</span><span class="sxs-lookup"><span data-stu-id="1ecbe-151">None</span></span>

## <span data-ttu-id="1ecbe-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1ecbe-152">OUTPUTS</span></span>

### <span data-ttu-id="1ecbe-153">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRVMNicConfig</span><span class="sxs-lookup"><span data-stu-id="1ecbe-153">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMNicConfig</span></span>

## <span data-ttu-id="1ecbe-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1ecbe-154">NOTES</span></span>

## <span data-ttu-id="1ecbe-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1ecbe-155">RELATED LINKS</span></span>
