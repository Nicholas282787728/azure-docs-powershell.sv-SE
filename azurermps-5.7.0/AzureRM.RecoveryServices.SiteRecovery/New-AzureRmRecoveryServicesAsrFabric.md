---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrFabric.md
ms.openlocfilehash: 53398a882ff513443f8eae336539858f7fe34ce4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579475"
---
# <span data-ttu-id="3b2c3-101">New-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="3b2c3-101">New-AzureRmRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="3b2c3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3b2c3-102">SYNOPSIS</span></span>
<span data-ttu-id="3b2c3-103">Skapar en Azure Site Recovery-Fabric.</span><span class="sxs-lookup"><span data-stu-id="3b2c3-103">Creates an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b2c3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3b2c3-104">SYNTAX</span></span>

### <span data-ttu-id="3b2c3-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="3b2c3-105">Default (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrFabric -Name <String> [-Type <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b2c3-106">Azure</span><span class="sxs-lookup"><span data-stu-id="3b2c3-106">Azure</span></span>
```
New-AzureRmRecoveryServicesAsrFabric [-Azure] -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b2c3-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3b2c3-107">DESCRIPTION</span></span>
<span data-ttu-id="3b2c3-108">Cmdleten **New-AzureRmRecoveryServicesAsrFabric** skapar en Azure Site Recovery-Fabric av den angivna typen.</span><span class="sxs-lookup"><span data-stu-id="3b2c3-108">The **New-AzureRmRecoveryServicesAsrFabric** cmdlet creates an Azure Site Recovery Fabric of the specified type.</span></span>

## <span data-ttu-id="3b2c3-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3b2c3-109">EXAMPLES</span></span>

### <span data-ttu-id="3b2c3-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3b2c3-110">Example 1</span></span>
```
PS C:\>  $currentJob = New-AzureRmRecoveryServicesAsrFabric -Name $FabricName
```

<span data-ttu-id="3b2c3-111">Startar Fabric-skapandet med det passerade namnet och returnerar det ASR-jobb som används för att spåra åtgärden för att skapa infrastrukturen.</span><span class="sxs-lookup"><span data-stu-id="3b2c3-111">Starts the fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

### <span data-ttu-id="3b2c3-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="3b2c3-112">Example 2</span></span>
```
PS C:\>  $currentJob = New-AzureRmRecoveryServicesAsrFabric -Azure -Name $fabricName -Location "eastus"
PS C:\>  Get-ASRJob -name $currentJob.id
```

<span data-ttu-id="3b2c3-113">Startar Azure Fabric-skapande med det namn som har passerat och returnerar det ASR-jobb som används för att spåra åtgärden för att skapa infrastrukturen.</span><span class="sxs-lookup"><span data-stu-id="3b2c3-113">Starts the azure fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

## <span data-ttu-id="3b2c3-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3b2c3-114">PARAMETERS</span></span>

### <span data-ttu-id="3b2c3-115">-Azure</span><span class="sxs-lookup"><span data-stu-id="3b2c3-115">-Azure</span></span>
<span data-ttu-id="3b2c3-116">Switch parameter anger att Azure Fabric skapas.</span><span class="sxs-lookup"><span data-stu-id="3b2c3-116">Switch parameter indicates creation of azure fabric.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Azure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b2c3-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3b2c3-117">-Confirm</span></span>
<span data-ttu-id="3b2c3-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3b2c3-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b2c3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b2c3-119">-DefaultProfile</span></span>
<span data-ttu-id="3b2c3-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3b2c3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="3b2c3-121">-Plats</span><span class="sxs-lookup"><span data-stu-id="3b2c3-121">-Location</span></span>
<span data-ttu-id="3b2c3-122">Anger den Azure-region som motsvarar det Fabric-objekt som skapas.</span><span class="sxs-lookup"><span data-stu-id="3b2c3-122">Specifies the Azure region corresponding to the Fabric object being created.</span></span> <span data-ttu-id="3b2c3-123">Objektet Azure Site Recovery Fabric representerar en region.</span><span class="sxs-lookup"><span data-stu-id="3b2c3-123">The Azure Site Recovery fabric object represents a region.</span></span> <span data-ttu-id="3b2c3-124">För att virtuella datorer ska replikeras mellan två Azure regioner representerar det primära Azure-området och återställnings infrastrukturen.</span><span class="sxs-lookup"><span data-stu-id="3b2c3-124">For virtual machines being replicated between two Azure regions  a primary fabric represents the primary Azure region and the recovery fabric .</span></span>

```yaml
Type: String
Parameter Sets: Azure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b2c3-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="3b2c3-125">-Name</span></span>
<span data-ttu-id="3b2c3-126">Anger namnet på Azure Site Recovery Fabric.</span><span class="sxs-lookup"><span data-stu-id="3b2c3-126">Specifies the name of the Azure Site Recovery Fabric.</span></span>

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

### <span data-ttu-id="3b2c3-127">– Skriv</span><span class="sxs-lookup"><span data-stu-id="3b2c3-127">-Type</span></span>
<span data-ttu-id="3b2c3-128">Anger Fabric-typen för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="3b2c3-128">Specifies the Azure Site Recovery Fabric Type.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases:
Accepted values: HyperVSite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b2c3-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b2c3-129">-WhatIf</span></span>
<span data-ttu-id="3b2c3-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3b2c3-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3b2c3-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3b2c3-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b2c3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b2c3-132">CommonParameters</span></span>
<span data-ttu-id="3b2c3-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b2c3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b2c3-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b2c3-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b2c3-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3b2c3-135">INPUTS</span></span>

### <span data-ttu-id="3b2c3-136">Ingen</span><span class="sxs-lookup"><span data-stu-id="3b2c3-136">None</span></span>

## <span data-ttu-id="3b2c3-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3b2c3-137">OUTPUTS</span></span>

### <span data-ttu-id="3b2c3-138">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="3b2c3-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="3b2c3-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3b2c3-139">NOTES</span></span>

## <span data-ttu-id="3b2c3-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3b2c3-140">RELATED LINKS</span></span>

[<span data-ttu-id="3b2c3-141">Get-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="3b2c3-141">Get-AzureRmRecoveryServicesAsrFabric</span></span>](./Get-AzureRmRecoveryServicesAsrFabric.md)

[<span data-ttu-id="3b2c3-142">Remove-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="3b2c3-142">Remove-AzureRmRecoveryServicesAsrFabric</span></span>](./Remove-AzureRmRecoveryServicesAsrFabric.md)
