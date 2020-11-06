---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 612D343A-89BA-491C-B20B-147715A2EF4F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoveryfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryFabric.md
ms.openlocfilehash: 43d9603a5938ecef084191ebe77888a5f1769673
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582944"
---
# <span data-ttu-id="1a482-101">Remove-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="1a482-101">Remove-AzureRmSiteRecoveryFabric</span></span>

## <span data-ttu-id="1a482-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1a482-102">SYNOPSIS</span></span>
<span data-ttu-id="1a482-103">Tar bort en Azure Site Recovery-Fabric.</span><span class="sxs-lookup"><span data-stu-id="1a482-103">Removes an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a482-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1a482-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryFabric -Fabric <ASRFabric> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a482-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1a482-105">DESCRIPTION</span></span>
<span data-ttu-id="1a482-106">Cmdleten **Remove-AzureRmSiteRecoveryFabric** tar bort en Azure Site Recovery-Fabric.</span><span class="sxs-lookup"><span data-stu-id="1a482-106">The **Remove-AzureRmSiteRecoveryFabric** cmdlet removes an Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="1a482-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1a482-107">EXAMPLES</span></span>

## <span data-ttu-id="1a482-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1a482-108">PARAMETERS</span></span>

### <span data-ttu-id="1a482-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a482-109">-DefaultProfile</span></span>
<span data-ttu-id="1a482-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1a482-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a482-111">-Fabric</span><span class="sxs-lookup"><span data-stu-id="1a482-111">-Fabric</span></span>
<span data-ttu-id="1a482-112">Anger ett Fabric-objekt för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="1a482-112">Specifies the Azure Site Recovery Fabric object.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1a482-113">-Force</span><span class="sxs-lookup"><span data-stu-id="1a482-113">-Force</span></span>
<span data-ttu-id="1a482-114">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="1a482-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a482-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1a482-115">-Confirm</span></span>
<span data-ttu-id="1a482-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1a482-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a482-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a482-117">-WhatIf</span></span>
<span data-ttu-id="1a482-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1a482-118">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="1a482-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1a482-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a482-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a482-120">CommonParameters</span></span>
<span data-ttu-id="1a482-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a482-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a482-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a482-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a482-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1a482-123">INPUTS</span></span>

### <span data-ttu-id="1a482-124">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="1a482-124">ASRFabric</span></span>
<span data-ttu-id="1a482-125">Parametern ' Fabric ' godkänner värdet av typen ' ASRFabric ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="1a482-125">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

## <span data-ttu-id="1a482-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1a482-126">OUTPUTS</span></span>

### <span data-ttu-id="1a482-127">Microsoft. Azure. commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="1a482-127">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="1a482-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1a482-128">NOTES</span></span>

## <span data-ttu-id="1a482-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1a482-129">RELATED LINKS</span></span>

[<span data-ttu-id="1a482-130">Get-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="1a482-130">Get-AzureRmSiteRecoveryFabric</span></span>](./Get-AzureRmSiteRecoveryFabric.md)

[<span data-ttu-id="1a482-131">New-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="1a482-131">New-AzureRmSiteRecoveryFabric</span></span>](./New-AzureRmSiteRecoveryFabric.md)
