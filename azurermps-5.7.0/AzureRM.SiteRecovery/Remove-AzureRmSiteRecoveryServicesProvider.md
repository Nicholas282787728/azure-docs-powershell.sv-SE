---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 2FB62869-FF83-4D92-B08B-07AF3C393159
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoveryservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryServicesProvider.md
ms.openlocfilehash: 88b6b83f24edb06871fd87f61fec1732893b0f41
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573264"
---
# <span data-ttu-id="ee617-101">Remove-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="ee617-101">Remove-AzureRmSiteRecoveryServicesProvider</span></span>

## <span data-ttu-id="ee617-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ee617-102">SYNOPSIS</span></span>
<span data-ttu-id="ee617-103">Tar bort en Azure Site Recovery Services-leverantör.</span><span class="sxs-lookup"><span data-stu-id="ee617-103">Removes an Azure Site Recovery Services Provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee617-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ee617-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryServicesProvider -ServicesProvider <ASRRecoveryServicesProvider> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee617-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ee617-105">DESCRIPTION</span></span>
<span data-ttu-id="ee617-106">Cmdleten **Remove-AzureRmSiteRecoveryServicesProvider** tar bort en Azure Site Recovery Services-leverantör från valvet.</span><span class="sxs-lookup"><span data-stu-id="ee617-106">The **Remove-AzureRmSiteRecoveryServicesProvider** cmdlet removes an Azure Site Recovery Services Provider from the vault.</span></span>

## <span data-ttu-id="ee617-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ee617-107">EXAMPLES</span></span>

## <span data-ttu-id="ee617-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ee617-108">PARAMETERS</span></span>

### <span data-ttu-id="ee617-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee617-109">-DefaultProfile</span></span>
<span data-ttu-id="ee617-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ee617-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee617-111">-Force</span><span class="sxs-lookup"><span data-stu-id="ee617-111">-Force</span></span>
<span data-ttu-id="ee617-112">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="ee617-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ee617-113">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="ee617-113">-ServicesProvider</span></span>
<span data-ttu-id="ee617-114">Anger objekt för tjänste leverantörer.</span><span class="sxs-lookup"><span data-stu-id="ee617-114">Specifies the Services Provider object.</span></span>

```yaml
Type: ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ee617-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ee617-115">-Confirm</span></span>
<span data-ttu-id="ee617-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ee617-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee617-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee617-117">-WhatIf</span></span>
<span data-ttu-id="ee617-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ee617-118">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="ee617-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ee617-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee617-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee617-120">CommonParameters</span></span>
<span data-ttu-id="ee617-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee617-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee617-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee617-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee617-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ee617-123">INPUTS</span></span>

### <span data-ttu-id="ee617-124">ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="ee617-124">ASRRecoveryServicesProvider</span></span>
<span data-ttu-id="ee617-125">Parametern ' ServicesProvider ' godkänner värdet av typen ' ASRRecoveryServicesProvider ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="ee617-125">Parameter 'ServicesProvider' accepts value of type 'ASRRecoveryServicesProvider' from the pipeline</span></span>

## <span data-ttu-id="ee617-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ee617-126">OUTPUTS</span></span>

### <span data-ttu-id="ee617-127">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. SiteRecovery. ASRJob, Microsoft. Azure. commands. SiteRecovery, version = 2.0.1.0; Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="ee617-127">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRJob, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="ee617-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ee617-128">NOTES</span></span>

## <span data-ttu-id="ee617-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ee617-129">RELATED LINKS</span></span>

[<span data-ttu-id="ee617-130">Get-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="ee617-130">Get-AzureRmSiteRecoveryServicesProvider</span></span>](./Get-AzureRmSiteRecoveryServicesProvider.md)

[<span data-ttu-id="ee617-131">Update-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="ee617-131">Update-AzureRmSiteRecoveryServicesProvider</span></span>](./Update-AzureRmSiteRecoveryServicesProvider.md)
