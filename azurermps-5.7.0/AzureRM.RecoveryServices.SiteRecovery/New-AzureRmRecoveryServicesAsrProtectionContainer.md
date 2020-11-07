---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 73d57e6e73b0e7e84dd3fb8bfff04ac8705bd108
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756792"
---
# <span data-ttu-id="fdb87-101">New-AzureRmRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="fdb87-101">New-AzureRmRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="fdb87-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fdb87-102">SYNOPSIS</span></span>
<span data-ttu-id="fdb87-103">Skapar en behållare för Azure Site Recovery-skydd inom angiven infrastruktur resurs.</span><span class="sxs-lookup"><span data-stu-id="fdb87-103">Creates an Azure Site Recovery Protection Container within the specified fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fdb87-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fdb87-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrProtectionContainer -Name <String> -InputObject <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fdb87-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fdb87-105">DESCRIPTION</span></span>
<span data-ttu-id="fdb87-106">New-AzureRmRecoveryServicesAsrProtectionContainer-cmdleten skapar en skydds behållare under den angivna infrastruktur resursen för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="fdb87-106">The New-AzureRmRecoveryServicesAsrProtectionContainer cmdlet creates a Protection Container under the specified Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="fdb87-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fdb87-107">EXAMPLES</span></span>

### <span data-ttu-id="fdb87-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="fdb87-108">Example 1</span></span>
```
PS C:\> $job = New-AzureRmRecoveryServicesAsrProtectionContainer -Name xyz -Fabric $fabric
PS C:\> Get-ASRJob -name $job.id
```

<span data-ttu-id="fdb87-109">Startar skapandet av skydds behållaren med angivna parametrar och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="fdb87-109">Starts the creation of the protection container with the specified parameters, and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="fdb87-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fdb87-110">PARAMETERS</span></span>

### <span data-ttu-id="fdb87-111">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fdb87-111">-Confirm</span></span>
<span data-ttu-id="fdb87-112">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fdb87-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fdb87-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdb87-113">-DefaultProfile</span></span>
<span data-ttu-id="fdb87-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fdb87-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fdb87-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fdb87-115">-InputObject</span></span>
<span data-ttu-id="fdb87-116">Skapar en behållare för replikering i det inmatade objektet (Azure Fabric).</span><span class="sxs-lookup"><span data-stu-id="fdb87-116">Creates the replication protection container in specifed input Object (Azure Fabric).</span></span>

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases: Fabric

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fdb87-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="fdb87-117">-Name</span></span>
<span data-ttu-id="fdb87-118">Namn på skydds behållaren.</span><span class="sxs-lookup"><span data-stu-id="fdb87-118">Name of the protection container.</span></span>

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

### <span data-ttu-id="fdb87-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fdb87-119">-WhatIf</span></span>
<span data-ttu-id="fdb87-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fdb87-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fdb87-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fdb87-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fdb87-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdb87-122">CommonParameters</span></span>
<span data-ttu-id="fdb87-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdb87-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdb87-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdb87-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdb87-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fdb87-125">INPUTS</span></span>

### <span data-ttu-id="fdb87-126">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="fdb87-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="fdb87-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fdb87-127">OUTPUTS</span></span>

### <span data-ttu-id="fdb87-128">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="fdb87-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="fdb87-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fdb87-129">NOTES</span></span>

## <span data-ttu-id="fdb87-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fdb87-130">RELATED LINKS</span></span>
