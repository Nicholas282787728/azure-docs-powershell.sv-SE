---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 0F9D72C1-2E42-4A67-9FDE-6344F5DE6C30
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsintelligencepacks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsIntelligencePacks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsIntelligencePacks.md
ms.openlocfilehash: 0e63b6926f635a4260e6e3c9d658afa410f29966
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575590"
---
# <span data-ttu-id="38a0e-101">Get-AzureRmOperationalInsightsIntelligencePacks</span><span class="sxs-lookup"><span data-stu-id="38a0e-101">Get-AzureRmOperationalInsightsIntelligencePacks</span></span>

## <span data-ttu-id="38a0e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="38a0e-102">SYNOPSIS</span></span>
<span data-ttu-id="38a0e-103">Hämtar tillgängliga intelligens paket.</span><span class="sxs-lookup"><span data-stu-id="38a0e-103">Gets the available Intelligence Packs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38a0e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="38a0e-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsIntelligencePacks [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38a0e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="38a0e-105">DESCRIPTION</span></span>
<span data-ttu-id="38a0e-106">Cmdleten **Get-AzureRmOperationalInsightsIntelligencePacks** hämtar de tillgängliga intelligens paketen.</span><span class="sxs-lookup"><span data-stu-id="38a0e-106">The **Get-AzureRmOperationalInsightsIntelligencePacks** cmdlet gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="38a0e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="38a0e-107">EXAMPLES</span></span>

### <span data-ttu-id="38a0e-108">Exempel 1: skaffa paketlösningar</span><span class="sxs-lookup"><span data-stu-id="38a0e-108">Example 1: Get Intelligence Packs</span></span>
```
PS C:\>Get-AzureOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="38a0e-109">Det här kommandot får de tillgängliga intelligens-paketen.</span><span class="sxs-lookup"><span data-stu-id="38a0e-109">This command gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="38a0e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="38a0e-110">PARAMETERS</span></span>

### <span data-ttu-id="38a0e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38a0e-111">-DefaultProfile</span></span>
<span data-ttu-id="38a0e-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="38a0e-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="38a0e-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38a0e-113">-ResourceGroupName</span></span>
<span data-ttu-id="38a0e-114">Anger namnet på en Azure-adressresurs som innehåller en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="38a0e-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38a0e-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="38a0e-115">-WorkspaceName</span></span>
<span data-ttu-id="38a0e-116">Anger arbets ytans namn.</span><span class="sxs-lookup"><span data-stu-id="38a0e-116">Specifies the workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38a0e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38a0e-117">CommonParameters</span></span>
<span data-ttu-id="38a0e-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38a0e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38a0e-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38a0e-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38a0e-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="38a0e-120">INPUTS</span></span>

### <span data-ttu-id="38a0e-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="38a0e-121">None</span></span>
<span data-ttu-id="38a0e-122">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="38a0e-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="38a0e-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="38a0e-123">OUTPUTS</span></span>

### <span data-ttu-id="38a0e-124">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. OperationalInsights. Models. PSIntelligencePack]</span><span class="sxs-lookup"><span data-stu-id="38a0e-124">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack]</span></span>

## <span data-ttu-id="38a0e-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="38a0e-125">NOTES</span></span>

## <span data-ttu-id="38a0e-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="38a0e-126">RELATED LINKS</span></span>

[<span data-ttu-id="38a0e-127">Cmdlets för Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="38a0e-127">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


