---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: B1D914F8-4181-4BF1-B1D3-A5857DA8254C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryProtectionContainerMapping.md
ms.openlocfilehash: a0de6cc5594b019275cb14785cbae3b969d44301
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755912"
---
# <span data-ttu-id="01df5-101">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="01df5-101">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span></span>

## <span data-ttu-id="01df5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="01df5-102">SYNOPSIS</span></span>
<span data-ttu-id="01df5-103">Tar bort en Azure Site Recovery-mappning för en behållare.</span><span class="sxs-lookup"><span data-stu-id="01df5-103">Removes an Azure Site Recovery Protection Container mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01df5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="01df5-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryProtectionContainerMapping
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01df5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="01df5-105">DESCRIPTION</span></span>
<span data-ttu-id="01df5-106">Cmdleten **Remove-AzureRmSiteRecoveryProtectionContainerMapping** tar bort en Azure Site Recovery Protection-mappning.</span><span class="sxs-lookup"><span data-stu-id="01df5-106">The **Remove-AzureRmSiteRecoveryProtectionContainerMapping** cmdlet removes an Azure Site Recovery Protection Container mapping.</span></span>

## <span data-ttu-id="01df5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="01df5-107">EXAMPLES</span></span>

## <span data-ttu-id="01df5-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="01df5-108">PARAMETERS</span></span>

### <span data-ttu-id="01df5-109">-Force</span><span class="sxs-lookup"><span data-stu-id="01df5-109">-Force</span></span>
<span data-ttu-id="01df5-110">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="01df5-110">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01df5-111">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="01df5-111">-ProtectionContainerMapping</span></span>
<span data-ttu-id="01df5-112">Anger mappnings objekt för en behållare för Azure Site Recovery-skydd.</span><span class="sxs-lookup"><span data-stu-id="01df5-112">Specifies the Azure Site Recovery Protection Container mapping object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="01df5-113">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="01df5-113">-Confirm</span></span>
<span data-ttu-id="01df5-114">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="01df5-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01df5-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01df5-115">-WhatIf</span></span>
<span data-ttu-id="01df5-116">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="01df5-116">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="01df5-117">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="01df5-117">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01df5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01df5-118">-DefaultProfile</span></span>
<span data-ttu-id="01df5-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="01df5-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01df5-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01df5-120">CommonParameters</span></span>
<span data-ttu-id="01df5-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01df5-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01df5-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01df5-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01df5-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="01df5-123">INPUTS</span></span>

### <span data-ttu-id="01df5-124">ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="01df5-124">ASRProtectionContainerMapping</span></span>
<span data-ttu-id="01df5-125">Parametern ' ProtectionContainerMapping ' godkänner värdet av typen ' ASRProtectionContainerMapping ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="01df5-125">Parameter 'ProtectionContainerMapping' accepts value of type 'ASRProtectionContainerMapping' from the pipeline</span></span>

## <span data-ttu-id="01df5-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="01df5-126">OUTPUTS</span></span>

### <span data-ttu-id="01df5-127">Microsoft. Azure. commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="01df5-127">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="01df5-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="01df5-128">NOTES</span></span>

## <span data-ttu-id="01df5-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="01df5-129">RELATED LINKS</span></span>

[<span data-ttu-id="01df5-130">Get-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="01df5-130">Get-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./Get-AzureRmSiteRecoveryProtectionContainerMapping.md)

[<span data-ttu-id="01df5-131">New-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="01df5-131">New-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./New-AzureRmSiteRecoveryProtectionContainerMapping.md)
