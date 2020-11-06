---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: a989b93b2c2ac2a1c292b736275da5cb91c7042d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579472"
---
# <span data-ttu-id="cbc6a-101">New-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="cbc6a-101">New-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="cbc6a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cbc6a-102">SYNOPSIS</span></span>
<span data-ttu-id="cbc6a-103">Skapar en nätverks mappning för automatisk system återställning mellan två nätverk.</span><span class="sxs-lookup"><span data-stu-id="cbc6a-103">Creates an ASR network mapping between two networks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cbc6a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cbc6a-104">SYNTAX</span></span>

### <span data-ttu-id="cbc6a-105">EnterpriseToEnterprise (standard)</span><span class="sxs-lookup"><span data-stu-id="cbc6a-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryNetwork <ASRNetwork> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cbc6a-106">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="cbc6a-106">AzureToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrNetworkMapping [-AzureToAzure] -Name <String> -PrimaryFabric <ASRFabric>
 -PrimaryAzureNetworkId <String> -RecoveryFabric <ASRFabric> -RecoveryAzureNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbc6a-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="cbc6a-107">EnterpriseToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryAzureNetworkId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cbc6a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cbc6a-108">DESCRIPTION</span></span>
<span data-ttu-id="cbc6a-109">**New-AzureRmRecoveryServicesAsrNetworkMapping-** cmdleten startar åtgärden att skapa en ASR-nätverks mappning mellan två nätverk och returnerar ASR-jobbet för det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="cbc6a-109">The **New-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet starts the operation of creating an ASR network mapping between two networks and returns the ASR job object for the ASR job used to track the operation.</span></span>

## <span data-ttu-id="cbc6a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cbc6a-110">EXAMPLES</span></span>

### <span data-ttu-id="cbc6a-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="cbc6a-111">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrNetworkMapping -Name $NetworkMapName -PrimaryNetwork $PrimaryNetwork -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="cbc6a-112">Startar åtgärden för att skapa nätverks mappning med angivet namn, primärt och återställnings nätverk och returnerar ett ASR-jobb för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="cbc6a-112">Starts the network mapping creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation.</span></span>

### <span data-ttu-id="cbc6a-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="cbc6a-113">Example 2</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrNetworkMapping -AzureToAzure -Name "mappingName" -PrimaryFabric $AzureFabric `
 -PrimaryAzureNetworkId $AzureNetworkId -RecoveryFabric $RecoveryAzureFabric -RecoveryAzureNetworkId $RecoveryNetworkId
```

<span data-ttu-id="cbc6a-114">Startar nätverks mappningen för att skapa en åtgärd med hjälp av angivet namn, primärt och återställnings nätverk och returnerar ett ASR-jobb för att spåra åtgärden (Azure to Azure-scenariot).</span><span class="sxs-lookup"><span data-stu-id="cbc6a-114">Starts the network mapping for creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation(Azure to Azure scenario).</span></span>

## <span data-ttu-id="cbc6a-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cbc6a-115">PARAMETERS</span></span>

### <span data-ttu-id="cbc6a-116">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="cbc6a-116">-AzureToAzure</span></span>
<span data-ttu-id="cbc6a-117">Switch parameter anger att nätverks mappningen som skapas ska användas för replikerade Azure Virtual-datorer mellan två Azure-regioner.</span><span class="sxs-lookup"><span data-stu-id="cbc6a-117">Switch parameter specifying that the network mapping being created will be used to replicated Azure virtual machines between two Azure regions.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbc6a-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cbc6a-118">-Confirm</span></span>
<span data-ttu-id="cbc6a-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cbc6a-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbc6a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbc6a-120">-DefaultProfile</span></span>
<span data-ttu-id="cbc6a-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cbc6a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="cbc6a-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="cbc6a-122">-Name</span></span>
<span data-ttu-id="cbc6a-123">Namn på den nätverks mappning för automatisk system återställning som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="cbc6a-123">Name of the ASR network mapping to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbc6a-124">-PrimaryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="cbc6a-124">-PrimaryAzureNetworkId</span></span>
<span data-ttu-id="cbc6a-125">Anger det primära nätverkets virtuella Azure-nätverks-ID.</span><span class="sxs-lookup"><span data-stu-id="cbc6a-125">Specifies the Azure virtual network ID of the primary network for the mapping.</span></span>

```yaml
Type: String
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbc6a-126">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="cbc6a-126">-PrimaryFabric</span></span>
<span data-ttu-id="cbc6a-127">Specifes ASR Fabric där mappning ska skapas.</span><span class="sxs-lookup"><span data-stu-id="cbc6a-127">Specifes the ASR fabric where mapping should be created.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbc6a-128">-PrimaryNetwork</span><span class="sxs-lookup"><span data-stu-id="cbc6a-128">-PrimaryNetwork</span></span>
<span data-ttu-id="cbc6a-129">Anger det primära nätverks objekt för automatisk nätverks mappning.</span><span class="sxs-lookup"><span data-stu-id="cbc6a-129">Specifies the primary network object for the ASR network mapping.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cbc6a-130">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="cbc6a-130">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="cbc6a-131">Anger återställnings-nätverks-ID för nätverks mappningen.</span><span class="sxs-lookup"><span data-stu-id="cbc6a-131">Specifies the recovery azure network ID for the network mapping.</span></span>

```yaml
Type: String
Parameter Sets: AzureToAzure, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbc6a-132">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="cbc6a-132">-RecoveryFabric</span></span>
<span data-ttu-id="cbc6a-133">Det Fabric-objekt för Azure Site Recovery som motsvarar återställnings-Azure-regionen.</span><span class="sxs-lookup"><span data-stu-id="cbc6a-133">The Azure Site Recovery fabric object corresponding to the recovery Azure region.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbc6a-134">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="cbc6a-134">-RecoveryNetwork</span></span>
<span data-ttu-id="cbc6a-135">Anger återställnings nätverks objekt för automatisk nätverks mappning.</span><span class="sxs-lookup"><span data-stu-id="cbc6a-135">Specifies the recovery network object for the ASR network mapping.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbc6a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbc6a-136">-WhatIf</span></span>
<span data-ttu-id="cbc6a-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cbc6a-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cbc6a-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cbc6a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbc6a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbc6a-139">CommonParameters</span></span>
<span data-ttu-id="cbc6a-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbc6a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbc6a-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbc6a-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbc6a-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cbc6a-142">INPUTS</span></span>

### <span data-ttu-id="cbc6a-143">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="cbc6a-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

## <span data-ttu-id="cbc6a-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cbc6a-144">OUTPUTS</span></span>

### <span data-ttu-id="cbc6a-145">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="cbc6a-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="cbc6a-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cbc6a-146">NOTES</span></span>

## <span data-ttu-id="cbc6a-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cbc6a-147">RELATED LINKS</span></span>

[<span data-ttu-id="cbc6a-148">Get-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="cbc6a-148">Get-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzureRmRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="cbc6a-149">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="cbc6a-149">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrNetworkMapping.md)
