---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 23ED4D24-66BD-46E9-BB57-6E0DA679B733
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsintelligencepack
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsIntelligencePack.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsIntelligencePack.md
ms.openlocfilehash: a8d799cec6278149cb4c08faf68584fb7968f85e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258095"
---
# <span data-ttu-id="f0e98-101">Set-AzOperationalInsightsIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="f0e98-101">Set-AzOperationalInsightsIntelligencePack</span></span>

## <span data-ttu-id="f0e98-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f0e98-102">SYNOPSIS</span></span>
<span data-ttu-id="f0e98-103">Aktiverar eller inaktiverar angivet intelligens-paket.</span><span class="sxs-lookup"><span data-stu-id="f0e98-103">Enables or disables the specified Intelligence Pack.</span></span>

## <span data-ttu-id="f0e98-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f0e98-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsIntelligencePack [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-IntelligencePackName] <String> [-Enabled] <Boolean> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f0e98-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f0e98-105">DESCRIPTION</span></span>
<span data-ttu-id="f0e98-106">Cmdleten **set-AzOperationalInsightsIntelligencePack** aktiverar det angivna intelligens paketet om det är *aktiverat* $True och inaktiverar det om det är *aktiverat* för $false.</span><span class="sxs-lookup"><span data-stu-id="f0e98-106">The **Set-AzOperationalInsightsIntelligencePack** cmdlet enables the specified Intelligence Pack if *Enabled* is set to $True and disables it if *Enabled* is set to $False.</span></span>

## <span data-ttu-id="f0e98-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f0e98-107">EXAMPLES</span></span>

### <span data-ttu-id="f0e98-108">Exempel 1: Ange intelligens</span><span class="sxs-lookup"><span data-stu-id="f0e98-108">Example 1: Set Intelligence Packs</span></span>
```
PS C:\>Set-AzOperationalInsightsIntelligencePack -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -IntelligencePackName "ContosoWorkspace" -Enabled $True
```

<span data-ttu-id="f0e98-109">Det här kommandot aktiverar det angivna intelligens-paketet.</span><span class="sxs-lookup"><span data-stu-id="f0e98-109">This command enables the specified Intelligence Pack.</span></span>

## <span data-ttu-id="f0e98-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f0e98-110">PARAMETERS</span></span>

### <span data-ttu-id="f0e98-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0e98-111">-DefaultProfile</span></span>
<span data-ttu-id="f0e98-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="f0e98-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f0e98-113">-Aktiverad</span><span class="sxs-lookup"><span data-stu-id="f0e98-113">-Enabled</span></span>
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

### <span data-ttu-id="f0e98-114">-IntelligencePackName</span><span class="sxs-lookup"><span data-stu-id="f0e98-114">-IntelligencePackName</span></span>
<span data-ttu-id="f0e98-115">Anger namnet på Intelligenss paketet.</span><span class="sxs-lookup"><span data-stu-id="f0e98-115">Specifies the Intelligence Pack name.</span></span>

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

### <span data-ttu-id="f0e98-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0e98-116">-ResourceGroupName</span></span>
<span data-ttu-id="f0e98-117">Anger resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="f0e98-117">Specifies the resource group name</span></span>

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

### <span data-ttu-id="f0e98-118">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f0e98-118">-WorkspaceName</span></span>
<span data-ttu-id="f0e98-119">Anger namnet på arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="f0e98-119">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="f0e98-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0e98-120">CommonParameters</span></span>
<span data-ttu-id="f0e98-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0e98-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0e98-122">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0e98-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0e98-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f0e98-123">INPUTS</span></span>

### <span data-ttu-id="f0e98-124">System. String</span><span class="sxs-lookup"><span data-stu-id="f0e98-124">System.String</span></span>

### <span data-ttu-id="f0e98-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f0e98-125">System.Boolean</span></span>

## <span data-ttu-id="f0e98-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f0e98-126">OUTPUTS</span></span>

### <span data-ttu-id="f0e98-127">Microsoft. Azure. commands. OperationalInsights. Models. PSIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="f0e98-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span></span>

## <span data-ttu-id="f0e98-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f0e98-128">NOTES</span></span>

## <span data-ttu-id="f0e98-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f0e98-129">RELATED LINKS</span></span>

[<span data-ttu-id="f0e98-130">Cmdlets för Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="f0e98-130">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


