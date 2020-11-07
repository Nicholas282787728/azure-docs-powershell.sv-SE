---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrFabric.md
ms.openlocfilehash: 28c038a6dfd29f9daaeb942afa8fcb4c479cd0aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757756"
---
# <span data-ttu-id="d94bf-101">New-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="d94bf-101">New-AzureRmRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="d94bf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d94bf-102">SYNOPSIS</span></span>
<span data-ttu-id="d94bf-103">Skapar en Azure Site Recovery-Fabric.</span><span class="sxs-lookup"><span data-stu-id="d94bf-103">Creates an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d94bf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d94bf-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrFabric -Name <String> [-Type <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d94bf-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d94bf-105">DESCRIPTION</span></span>
<span data-ttu-id="d94bf-106">Cmdleten **New-AzureRmRecoveryServicesAsrFabric** skapar en Azure Site Recovery-Fabric av den angivna typen.</span><span class="sxs-lookup"><span data-stu-id="d94bf-106">The **New-AzureRmRecoveryServicesAsrFabric** cmdlet creates an Azure Site Recovery Fabric of the specified type.</span></span>

## <span data-ttu-id="d94bf-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d94bf-107">EXAMPLES</span></span>

### <span data-ttu-id="d94bf-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d94bf-108">Example 1</span></span>
```
PS C:\>  $currentJob = New-AzureRmRecoveryServicesAsrFabric -Name $FabricName
```

<span data-ttu-id="d94bf-109">Startar Fabric-skapandet med det passerade namnet och returnerar det ASR-jobb som används för att spåra åtgärden för att skapa infrastrukturen.</span><span class="sxs-lookup"><span data-stu-id="d94bf-109">Starts the fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

## <span data-ttu-id="d94bf-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d94bf-110">PARAMETERS</span></span>

### <span data-ttu-id="d94bf-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="d94bf-111">-Name</span></span>
<span data-ttu-id="d94bf-112">Anger namnet på Azure Site Recovery Fabric.</span><span class="sxs-lookup"><span data-stu-id="d94bf-112">Specifies the name of the Azure Site Recovery Fabric.</span></span>

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

### <span data-ttu-id="d94bf-113">– Skriv</span><span class="sxs-lookup"><span data-stu-id="d94bf-113">-Type</span></span>
<span data-ttu-id="d94bf-114">Anger Fabric-typen för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="d94bf-114">Specifies the Azure Site Recovery Fabric Type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: HyperVSite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d94bf-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d94bf-115">-Confirm</span></span>
<span data-ttu-id="d94bf-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d94bf-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d94bf-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d94bf-117">-WhatIf</span></span>
<span data-ttu-id="d94bf-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d94bf-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d94bf-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d94bf-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d94bf-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d94bf-120">CommonParameters</span></span>
<span data-ttu-id="d94bf-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d94bf-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d94bf-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d94bf-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d94bf-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d94bf-123">INPUTS</span></span>

### <span data-ttu-id="d94bf-124">Ingen</span><span class="sxs-lookup"><span data-stu-id="d94bf-124">None</span></span>

## <span data-ttu-id="d94bf-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d94bf-125">OUTPUTS</span></span>

### <span data-ttu-id="d94bf-126">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="d94bf-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d94bf-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d94bf-127">NOTES</span></span>

## <span data-ttu-id="d94bf-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d94bf-128">RELATED LINKS</span></span>

[<span data-ttu-id="d94bf-129">Get-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="d94bf-129">Get-AzureRmRecoveryServicesAsrFabric</span></span>](./Get-AzureRmRecoveryServicesAsrFabric.md)

[<span data-ttu-id="d94bf-130">Remove-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="d94bf-130">Remove-AzureRmRecoveryServicesAsrFabric</span></span>](./Remove-AzureRmRecoveryServicesAsrFabric.md)
