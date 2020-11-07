---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: B1D914F8-4181-4BF1-B1D3-A5857DA8254C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoveryprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryProtectionContainerMapping.md
ms.openlocfilehash: 27c90687b212c0ed41dcb080df1be5686a876725
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757192"
---
# <span data-ttu-id="c505b-101">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="c505b-101">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span></span>

## <span data-ttu-id="c505b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c505b-102">SYNOPSIS</span></span>
<span data-ttu-id="c505b-103">Tar bort en Azure Site Recovery-mappning för en behållare.</span><span class="sxs-lookup"><span data-stu-id="c505b-103">Removes an Azure Site Recovery Protection Container mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c505b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c505b-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryProtectionContainerMapping
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c505b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c505b-105">DESCRIPTION</span></span>
<span data-ttu-id="c505b-106">Cmdleten **Remove-AzureRmSiteRecoveryProtectionContainerMapping** tar bort en Azure Site Recovery Protection-mappning.</span><span class="sxs-lookup"><span data-stu-id="c505b-106">The **Remove-AzureRmSiteRecoveryProtectionContainerMapping** cmdlet removes an Azure Site Recovery Protection Container mapping.</span></span>

## <span data-ttu-id="c505b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c505b-107">EXAMPLES</span></span>

## <span data-ttu-id="c505b-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c505b-108">PARAMETERS</span></span>

### <span data-ttu-id="c505b-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c505b-109">-DefaultProfile</span></span>
<span data-ttu-id="c505b-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c505b-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c505b-111">-Force</span><span class="sxs-lookup"><span data-stu-id="c505b-111">-Force</span></span>
<span data-ttu-id="c505b-112">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="c505b-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c505b-113">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="c505b-113">-ProtectionContainerMapping</span></span>
<span data-ttu-id="c505b-114">Anger mappnings objekt för en behållare för Azure Site Recovery-skydd.</span><span class="sxs-lookup"><span data-stu-id="c505b-114">Specifies the Azure Site Recovery Protection Container mapping object.</span></span>

```yaml
Type: ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c505b-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c505b-115">-Confirm</span></span>
<span data-ttu-id="c505b-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c505b-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c505b-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c505b-117">-WhatIf</span></span>
<span data-ttu-id="c505b-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c505b-118">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="c505b-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c505b-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c505b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c505b-120">CommonParameters</span></span>
<span data-ttu-id="c505b-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c505b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c505b-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c505b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c505b-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c505b-123">INPUTS</span></span>

### <span data-ttu-id="c505b-124">ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="c505b-124">ASRProtectionContainerMapping</span></span>
<span data-ttu-id="c505b-125">Parametern ' ProtectionContainerMapping ' godkänner värdet av typen ' ASRProtectionContainerMapping ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="c505b-125">Parameter 'ProtectionContainerMapping' accepts value of type 'ASRProtectionContainerMapping' from the pipeline</span></span>

## <span data-ttu-id="c505b-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c505b-126">OUTPUTS</span></span>

### <span data-ttu-id="c505b-127">Microsoft. Azure. commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="c505b-127">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c505b-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c505b-128">NOTES</span></span>

## <span data-ttu-id="c505b-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c505b-129">RELATED LINKS</span></span>

[<span data-ttu-id="c505b-130">Get-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="c505b-130">Get-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./Get-AzureRmSiteRecoveryProtectionContainerMapping.md)

[<span data-ttu-id="c505b-131">New-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="c505b-131">New-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./New-AzureRmSiteRecoveryProtectionContainerMapping.md)
