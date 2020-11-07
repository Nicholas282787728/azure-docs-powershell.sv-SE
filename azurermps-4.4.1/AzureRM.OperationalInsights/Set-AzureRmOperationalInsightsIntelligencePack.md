---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 23ED4D24-66BD-46E9-BB57-6E0DA679B733
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsIntelligencePack.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsIntelligencePack.md
ms.openlocfilehash: 266ee7c7dd8327a43de20faf0687e2f6a67ca6ed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755434"
---
# <span data-ttu-id="3bc4d-101">Set-AzureRmOperationalInsightsIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="3bc4d-101">Set-AzureRmOperationalInsightsIntelligencePack</span></span>

## <span data-ttu-id="3bc4d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3bc4d-102">SYNOPSIS</span></span>
<span data-ttu-id="3bc4d-103">Aktiverar eller inaktiverar angivet intelligens-paket.</span><span class="sxs-lookup"><span data-stu-id="3bc4d-103">Enables or disables the specified Intelligence Pack.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3bc4d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3bc4d-104">SYNTAX</span></span>

```
Set-AzureRmOperationalInsightsIntelligencePack [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-IntelligencePackName] <String> [-Enabled] <Boolean> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3bc4d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3bc4d-105">DESCRIPTION</span></span>
<span data-ttu-id="3bc4d-106">Cmdleten **set-AzureRmOperationalInsightsIntelligencePack** aktiverar det angivna intelligens paketet om det är *aktiverat* $True och inaktiverar det om det är *aktiverat* för $false.</span><span class="sxs-lookup"><span data-stu-id="3bc4d-106">The **Set-AzureRmOperationalInsightsIntelligencePack** cmdlet enables the specified Intelligence Pack if *Enabled* is set to $True and disables it if *Enabled* is set to $False.</span></span>

## <span data-ttu-id="3bc4d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3bc4d-107">EXAMPLES</span></span>

### <span data-ttu-id="3bc4d-108">Exempel 1: Ange intelligens</span><span class="sxs-lookup"><span data-stu-id="3bc4d-108">Example 1: Set Intelligence Packs</span></span>
```
PS C:\>Set-AzureOperationalInsightsIntelligencePack -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -IntelligencePackName "ContosoWorkspace" -Enabled $True
```

<span data-ttu-id="3bc4d-109">Det här kommandot aktiverar det angivna intelligens-paketet.</span><span class="sxs-lookup"><span data-stu-id="3bc4d-109">This command enables the specified Intelligence Pack.</span></span>

## <span data-ttu-id="3bc4d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3bc4d-110">PARAMETERS</span></span>

### <span data-ttu-id="3bc4d-111">-Aktiverad</span><span class="sxs-lookup"><span data-stu-id="3bc4d-111">-Enabled</span></span>
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

### <span data-ttu-id="3bc4d-112">-IntelligencePackName</span><span class="sxs-lookup"><span data-stu-id="3bc4d-112">-IntelligencePackName</span></span>
<span data-ttu-id="3bc4d-113">Anger namnet på Intelligenss paketet.</span><span class="sxs-lookup"><span data-stu-id="3bc4d-113">Specifies the Intelligence Pack name.</span></span>

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

### <span data-ttu-id="3bc4d-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bc4d-114">-ResourceGroupName</span></span>
<span data-ttu-id="3bc4d-115">Anger resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="3bc4d-115">Specifies the resource group name</span></span>

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

### <span data-ttu-id="3bc4d-116">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3bc4d-116">-WorkspaceName</span></span>
<span data-ttu-id="3bc4d-117">Anger namnet på arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="3bc4d-117">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="3bc4d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bc4d-118">-DefaultProfile</span></span>
<span data-ttu-id="3bc4d-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3bc4d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3bc4d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bc4d-120">CommonParameters</span></span>
<span data-ttu-id="3bc4d-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bc4d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bc4d-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3bc4d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bc4d-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3bc4d-123">INPUTS</span></span>

## <span data-ttu-id="3bc4d-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3bc4d-124">OUTPUTS</span></span>

## <span data-ttu-id="3bc4d-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3bc4d-125">NOTES</span></span>

## <span data-ttu-id="3bc4d-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3bc4d-126">RELATED LINKS</span></span>

[<span data-ttu-id="3bc4d-127">Cmdlets för Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="3bc4d-127">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


