---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: fecc6f1911a82b20d3f96643ceed83486727f29f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092422"
---
# <span data-ttu-id="82b54-101">New-AzRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="82b54-101">New-AzRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="82b54-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="82b54-102">SYNOPSIS</span></span>
<span data-ttu-id="82b54-103">Skapar en behållare för Azure Site Recovery-skydd inom angiven infrastruktur resurs.</span><span class="sxs-lookup"><span data-stu-id="82b54-103">Creates an Azure Site Recovery Protection Container within the specified fabric.</span></span>

## <span data-ttu-id="82b54-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="82b54-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrProtectionContainer -Name <String> -InputObject <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82b54-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="82b54-105">DESCRIPTION</span></span>
<span data-ttu-id="82b54-106">New-AzRecoveryServicesAsrProtectionContainer-cmdleten skapar en skydds behållare under den angivna infrastruktur resursen för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="82b54-106">The New-AzRecoveryServicesAsrProtectionContainer cmdlet creates a Protection Container under the specified Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="82b54-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="82b54-107">EXAMPLES</span></span>

### <span data-ttu-id="82b54-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="82b54-108">Example 1</span></span>
```
PS C:\> $job = New-AzRecoveryServicesAsrProtectionContainer -Name xyz -Fabric $fabric
PS C:\> Get-ASRJob -name $job.id
```

<span data-ttu-id="82b54-109">Startar skapandet av skydds behållaren med angivna parametrar och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="82b54-109">Starts the creation of the protection container with the specified parameters, and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="82b54-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="82b54-110">PARAMETERS</span></span>

### <span data-ttu-id="82b54-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82b54-111">-DefaultProfile</span></span>
<span data-ttu-id="82b54-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="82b54-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82b54-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="82b54-113">-InputObject</span></span>
<span data-ttu-id="82b54-114">Skapar objektet för replikering av replikerade objekt (Azure Fabric).</span><span class="sxs-lookup"><span data-stu-id="82b54-114">Creates the replication protection container in specified input Object (Azure Fabric).</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases: Fabric

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="82b54-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="82b54-115">-Name</span></span>
<span data-ttu-id="82b54-116">Namn på skydds behållaren.</span><span class="sxs-lookup"><span data-stu-id="82b54-116">Name of the protection container.</span></span>

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

### <span data-ttu-id="82b54-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="82b54-117">-Confirm</span></span>
<span data-ttu-id="82b54-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="82b54-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82b54-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82b54-119">-WhatIf</span></span>
<span data-ttu-id="82b54-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="82b54-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="82b54-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="82b54-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82b54-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82b54-122">CommonParameters</span></span>
<span data-ttu-id="82b54-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82b54-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82b54-124">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="82b54-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82b54-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="82b54-125">INPUTS</span></span>

### <span data-ttu-id="82b54-126">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="82b54-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="82b54-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="82b54-127">OUTPUTS</span></span>

### <span data-ttu-id="82b54-128">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="82b54-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="82b54-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="82b54-129">NOTES</span></span>

## <span data-ttu-id="82b54-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="82b54-130">RELATED LINKS</span></span>
