---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 23ED4D24-66BD-46E9-BB57-6E0DA679B733
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsintelligencepack
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsIntelligencePack.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsIntelligencePack.md
ms.openlocfilehash: 73dd6e62ba6bac6ec2684822e257bbf5a02d6e31
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/13/2020
ms.locfileid: "94100514"
---
# <span data-ttu-id="39f02-101">Set-AzOperationalInsightsIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="39f02-101">Set-AzOperationalInsightsIntelligencePack</span></span>

## <span data-ttu-id="39f02-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="39f02-102">SYNOPSIS</span></span>
<span data-ttu-id="39f02-103">Aktiverar eller inaktiverar angivet intelligens-paket.</span><span class="sxs-lookup"><span data-stu-id="39f02-103">Enables or disables the specified Intelligence Pack.</span></span>

## <span data-ttu-id="39f02-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="39f02-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsIntelligencePack [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-IntelligencePackName] <String> [-Enabled] <Boolean> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="39f02-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="39f02-105">DESCRIPTION</span></span>
<span data-ttu-id="39f02-106">Cmdleten **set-AzOperationalInsightsIntelligencePack** aktiverar det angivna intelligens paketet om det är *aktiverat* $True och inaktiverar det om det är *aktiverat* för $false.</span><span class="sxs-lookup"><span data-stu-id="39f02-106">The **Set-AzOperationalInsightsIntelligencePack** cmdlet enables the specified Intelligence Pack if *Enabled* is set to $True and disables it if *Enabled* is set to $False.</span></span>

## <span data-ttu-id="39f02-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="39f02-107">EXAMPLES</span></span>

### <span data-ttu-id="39f02-108">Exempel 1: Ange intelligens</span><span class="sxs-lookup"><span data-stu-id="39f02-108">Example 1: Set Intelligence Packs</span></span>
```
PS C:\>Set-AzOperationalInsightsIntelligencePack -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -IntelligencePackName "ContosoWorkspace" -Enabled $True
```

<span data-ttu-id="39f02-109">Det här kommandot aktiverar det angivna intelligens-paketet.</span><span class="sxs-lookup"><span data-stu-id="39f02-109">This command enables the specified Intelligence Pack.</span></span>

## <span data-ttu-id="39f02-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="39f02-110">PARAMETERS</span></span>

### <span data-ttu-id="39f02-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39f02-111">-DefaultProfile</span></span>
<span data-ttu-id="39f02-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="39f02-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="39f02-113">-Aktiverad</span><span class="sxs-lookup"><span data-stu-id="39f02-113">-Enabled</span></span>
```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39f02-114">-IntelligencePackName</span><span class="sxs-lookup"><span data-stu-id="39f02-114">-IntelligencePackName</span></span>
<span data-ttu-id="39f02-115">Anger namnet på Intelligenss paketet.</span><span class="sxs-lookup"><span data-stu-id="39f02-115">Specifies the Intelligence Pack name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39f02-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39f02-116">-ResourceGroupName</span></span>
<span data-ttu-id="39f02-117">Anger resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="39f02-117">Specifies the resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39f02-118">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="39f02-118">-WorkspaceName</span></span>
<span data-ttu-id="39f02-119">Anger namnet på arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="39f02-119">Specifies the name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39f02-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39f02-120">CommonParameters</span></span>
<span data-ttu-id="39f02-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39f02-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39f02-122">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39f02-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39f02-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="39f02-123">INPUTS</span></span>

### <span data-ttu-id="39f02-124">System. String</span><span class="sxs-lookup"><span data-stu-id="39f02-124">System.String</span></span>

### <span data-ttu-id="39f02-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="39f02-125">System.Boolean</span></span>

## <span data-ttu-id="39f02-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="39f02-126">OUTPUTS</span></span>

### <span data-ttu-id="39f02-127">Microsoft. Azure. commands. OperationalInsights. Models. PSIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="39f02-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span></span>

## <span data-ttu-id="39f02-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="39f02-128">NOTES</span></span>

## <span data-ttu-id="39f02-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="39f02-129">RELATED LINKS</span></span>

[<span data-ttu-id="39f02-130">Cmdlets för Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="39f02-130">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


