---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: e1966e7172bcce724702b8652b5e85fcce79260e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98398251"
---
# <span data-ttu-id="64bc9-101">New-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="64bc9-101">New-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="64bc9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="64bc9-102">SYNOPSIS</span></span>
<span data-ttu-id="64bc9-103">Skapar en Azure Site Recovery-Fabric.</span><span class="sxs-lookup"><span data-stu-id="64bc9-103">Creates an Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="64bc9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="64bc9-104">SYNTAX</span></span>

### <span data-ttu-id="64bc9-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="64bc9-105">Default (Default)</span></span>
```
New-AzRecoveryServicesAsrFabric -Name <String> [-Type <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64bc9-106">Azure</span><span class="sxs-lookup"><span data-stu-id="64bc9-106">Azure</span></span>
```
New-AzRecoveryServicesAsrFabric [-Azure] -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64bc9-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="64bc9-107">DESCRIPTION</span></span>
<span data-ttu-id="64bc9-108">Cmdleten **New-AzRecoveryServicesAsrFabric** skapar en Azure Site Recovery-Fabric av den angivna typen.</span><span class="sxs-lookup"><span data-stu-id="64bc9-108">The **New-AzRecoveryServicesAsrFabric** cmdlet creates an Azure Site Recovery Fabric of the specified type.</span></span>

## <span data-ttu-id="64bc9-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="64bc9-109">EXAMPLES</span></span>

### <span data-ttu-id="64bc9-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="64bc9-110">Example 1</span></span>
```
PS C:\>  $currentJob = New-AzRecoveryServicesAsrFabric -Name $FabricName
```

<span data-ttu-id="64bc9-111">Startar Fabric-skapandet med det passerade namnet och returnerar det ASR-jobb som används för att spåra åtgärden för att skapa infrastrukturen.</span><span class="sxs-lookup"><span data-stu-id="64bc9-111">Starts the fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

### <span data-ttu-id="64bc9-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="64bc9-112">Example 2</span></span>
```
PS C:\>  $currentJob = New-AzRecoveryServicesAsrFabric -Azure -Name $fabricName -Location "eastus"
PS C:\>  Get-ASRJob -name $currentJob.id
```

<span data-ttu-id="64bc9-113">Startar Azure Fabric-skapande med det namn som har passerat och returnerar det ASR-jobb som används för att spåra åtgärden för att skapa infrastrukturen.</span><span class="sxs-lookup"><span data-stu-id="64bc9-113">Starts the azure fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

## <span data-ttu-id="64bc9-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="64bc9-114">PARAMETERS</span></span>

### <span data-ttu-id="64bc9-115">-Azure</span><span class="sxs-lookup"><span data-stu-id="64bc9-115">-Azure</span></span>
<span data-ttu-id="64bc9-116">Switch parameter anger att Azure Fabric ska skapas.</span><span class="sxs-lookup"><span data-stu-id="64bc9-116">Switch parameter specifies to create azure fabric.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Azure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64bc9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64bc9-117">-DefaultProfile</span></span>
<span data-ttu-id="64bc9-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="64bc9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="64bc9-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="64bc9-119">-Location</span></span>
<span data-ttu-id="64bc9-120">Anger den Azure-region som motsvarar det Fabric-objekt som skapas.</span><span class="sxs-lookup"><span data-stu-id="64bc9-120">Specifies the Azure region corresponding to the Fabric object being created.</span></span> <span data-ttu-id="64bc9-121">Objektet Azure Site Recovery Fabric representerar en region.</span><span class="sxs-lookup"><span data-stu-id="64bc9-121">The Azure Site Recovery fabric object represents a region.</span></span> <span data-ttu-id="64bc9-122">För att virtuella datorer ska replikeras mellan två Azure regioner representerar det primära Azure-området och återställnings infrastrukturen.</span><span class="sxs-lookup"><span data-stu-id="64bc9-122">For virtual machines being replicated between two Azure regions  a primary fabric represents the primary Azure region and the recovery fabric .</span></span>

```yaml
Type: System.String
Parameter Sets: Azure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64bc9-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="64bc9-123">-Name</span></span>
<span data-ttu-id="64bc9-124">Anger namnet på Azure Site Recovery Fabric.</span><span class="sxs-lookup"><span data-stu-id="64bc9-124">Specifies the name of the Azure Site Recovery Fabric.</span></span>

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

### <span data-ttu-id="64bc9-125">– Skriv</span><span class="sxs-lookup"><span data-stu-id="64bc9-125">-Type</span></span>
<span data-ttu-id="64bc9-126">Anger Fabric-typen för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="64bc9-126">Specifies the Azure Site Recovery Fabric Type.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:
Accepted values: HyperVSite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64bc9-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="64bc9-127">-Confirm</span></span>
<span data-ttu-id="64bc9-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="64bc9-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64bc9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64bc9-129">-WhatIf</span></span>
<span data-ttu-id="64bc9-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="64bc9-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="64bc9-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="64bc9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64bc9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64bc9-132">CommonParameters</span></span>
<span data-ttu-id="64bc9-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64bc9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64bc9-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="64bc9-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64bc9-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="64bc9-135">INPUTS</span></span>

### <span data-ttu-id="64bc9-136">Ingen</span><span class="sxs-lookup"><span data-stu-id="64bc9-136">None</span></span>

## <span data-ttu-id="64bc9-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="64bc9-137">OUTPUTS</span></span>

### <span data-ttu-id="64bc9-138">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="64bc9-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="64bc9-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="64bc9-139">NOTES</span></span>

## <span data-ttu-id="64bc9-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="64bc9-140">RELATED LINKS</span></span>

[<span data-ttu-id="64bc9-141">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="64bc9-141">Get-AzRecoveryServicesAsrFabric</span></span>](./Get-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="64bc9-142">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="64bc9-142">Remove-AzRecoveryServicesAsrFabric</span></span>](./Remove-AzRecoveryServicesAsrFabric.md)
