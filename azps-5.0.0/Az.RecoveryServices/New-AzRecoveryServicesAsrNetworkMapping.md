---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: dca68a4f6315ee124c927d0efb0ff0eb95bf1663
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322176"
---
# <span data-ttu-id="28f15-101">New-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="28f15-101">New-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="28f15-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="28f15-102">SYNOPSIS</span></span>
<span data-ttu-id="28f15-103">Skapar en nätverks mappning för automatisk system återställning mellan två nätverk.</span><span class="sxs-lookup"><span data-stu-id="28f15-103">Creates an ASR network mapping between two networks.</span></span>

## <span data-ttu-id="28f15-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="28f15-104">SYNTAX</span></span>

### <span data-ttu-id="28f15-105">EnterpriseToEnterprise (standard)</span><span class="sxs-lookup"><span data-stu-id="28f15-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryNetwork <ASRNetwork> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="28f15-106">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="28f15-106">AzureToAzure</span></span>
```
New-AzRecoveryServicesAsrNetworkMapping [-AzureToAzure] -Name <String> -PrimaryFabric <ASRFabric>
 -PrimaryAzureNetworkId <String> -RecoveryFabric <ASRFabric> -RecoveryAzureNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28f15-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="28f15-107">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryAzureNetworkId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="28f15-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="28f15-108">DESCRIPTION</span></span>
<span data-ttu-id="28f15-109">**New-AzRecoveryServicesAsrNetworkMapping-** cmdleten startar åtgärden att skapa en ASR-nätverks mappning mellan två nätverk och returnerar ASR-jobbet för det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="28f15-109">The **New-AzRecoveryServicesAsrNetworkMapping** cmdlet starts the operation of creating an ASR network mapping between two networks and returns the ASR job object for the ASR job used to track the operation.</span></span>

## <span data-ttu-id="28f15-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="28f15-110">EXAMPLES</span></span>

### <span data-ttu-id="28f15-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="28f15-111">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrNetworkMapping -Name $NetworkMapName -PrimaryNetwork $PrimaryNetwork -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="28f15-112">Startar åtgärden för att skapa nätverks mappning med angivet namn, primärt och återställnings nätverk och returnerar ett ASR-jobb för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="28f15-112">Starts the network mapping creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation.</span></span>

### <span data-ttu-id="28f15-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="28f15-113">Example 2</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrNetworkMapping -AzureToAzure -Name "mappingName" -PrimaryFabric $AzureFabric `
 -PrimaryAzureNetworkId $AzureNetworkId -RecoveryFabric $RecoveryAzureFabric -RecoveryAzureNetworkId $RecoveryNetworkId
```

<span data-ttu-id="28f15-114">Startar nätverks mappningen för att skapa en åtgärd med hjälp av angivet namn, primärt och återställnings nätverk och returnerar ett ASR-jobb för att spåra åtgärden (Azure to Azure-scenariot).</span><span class="sxs-lookup"><span data-stu-id="28f15-114">Starts the network mapping for creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation(Azure to Azure scenario).</span></span>

## <span data-ttu-id="28f15-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="28f15-115">PARAMETERS</span></span>

### <span data-ttu-id="28f15-116">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="28f15-116">-AzureToAzure</span></span>
<span data-ttu-id="28f15-117">Flagga för att skapa AzureToAzure-scenario.</span><span class="sxs-lookup"><span data-stu-id="28f15-117">Flag to create AzureToAzure scenario.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28f15-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28f15-118">-DefaultProfile</span></span>
<span data-ttu-id="28f15-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="28f15-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="28f15-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="28f15-120">-Name</span></span>
<span data-ttu-id="28f15-121">Namn på den nätverks mappning för automatisk system återställning som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="28f15-121">Name of the ASR network mapping to create.</span></span>

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

### <span data-ttu-id="28f15-122">-PrimaryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="28f15-122">-PrimaryAzureNetworkId</span></span>
<span data-ttu-id="28f15-123">Anger det primära nätverkets virtuella Azure-nätverks-ID.</span><span class="sxs-lookup"><span data-stu-id="28f15-123">Specifies the Azure virtual network ID of the primary network for the mapping.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28f15-124">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="28f15-124">-PrimaryFabric</span></span>
<span data-ttu-id="28f15-125">Anger ASR-fabricen där mappning ska skapas.</span><span class="sxs-lookup"><span data-stu-id="28f15-125">Specifies the ASR fabric where mapping should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28f15-126">-PrimaryNetwork</span><span class="sxs-lookup"><span data-stu-id="28f15-126">-PrimaryNetwork</span></span>
<span data-ttu-id="28f15-127">Anger det primära nätverks objekt för automatisk nätverks mappning.</span><span class="sxs-lookup"><span data-stu-id="28f15-127">Specifies the primary network object for the ASR network mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28f15-128">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="28f15-128">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="28f15-129">Anger återställnings-nätverks-ID för nätverks mappningen.</span><span class="sxs-lookup"><span data-stu-id="28f15-129">Specifies the recovery azure network ID for the network mapping.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28f15-130">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="28f15-130">-RecoveryFabric</span></span>
<span data-ttu-id="28f15-131">Det Fabric-objekt för Azure Site Recovery som motsvarar återställnings-Azure-regionen.</span><span class="sxs-lookup"><span data-stu-id="28f15-131">The Azure Site Recovery fabric object corresponding to the recovery Azure region.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28f15-132">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="28f15-132">-RecoveryNetwork</span></span>
<span data-ttu-id="28f15-133">Anger återställnings nätverks objekt för automatisk nätverks mappning.</span><span class="sxs-lookup"><span data-stu-id="28f15-133">Specifies the recovery network object for the ASR network mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28f15-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="28f15-134">-Confirm</span></span>
<span data-ttu-id="28f15-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="28f15-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28f15-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28f15-136">-WhatIf</span></span>
<span data-ttu-id="28f15-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="28f15-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="28f15-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="28f15-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28f15-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28f15-139">CommonParameters</span></span>
<span data-ttu-id="28f15-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28f15-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28f15-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="28f15-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28f15-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="28f15-142">INPUTS</span></span>

### <span data-ttu-id="28f15-143">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="28f15-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

## <span data-ttu-id="28f15-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="28f15-144">OUTPUTS</span></span>

### <span data-ttu-id="28f15-145">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="28f15-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="28f15-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="28f15-146">NOTES</span></span>

## <span data-ttu-id="28f15-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="28f15-147">RELATED LINKS</span></span>

[<span data-ttu-id="28f15-148">Get-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="28f15-148">Get-AzRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="28f15-149">Remove-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="28f15-149">Remove-AzRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzRecoveryServicesAsrNetworkMapping.md)
