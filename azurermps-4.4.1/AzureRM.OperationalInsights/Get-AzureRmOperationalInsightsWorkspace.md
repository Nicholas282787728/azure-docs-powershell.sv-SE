---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: F94415DA-1A4A-4D37-A626-1EDF5D1EFE74
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspace.md
ms.openlocfilehash: 042597d8d300f57600680282dadb16e8ec221e59
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756896"
---
# <span data-ttu-id="7a535-101">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="7a535-101">Get-AzureRmOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="7a535-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7a535-102">SYNOPSIS</span></span>
<span data-ttu-id="7a535-103">Hämtar information om en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="7a535-103">Gets information about a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a535-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7a535-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsWorkspace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a535-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7a535-105">DESCRIPTION</span></span>
<span data-ttu-id="7a535-106">Cmdleten **Get-AzureRmOperationalInsightsWorkspace** hämtar information om en befintlig arbets yta.</span><span class="sxs-lookup"><span data-stu-id="7a535-106">The **Get-AzureRmOperationalInsightsWorkspace** cmdlet gets information about an existing workspace.</span></span>
<span data-ttu-id="7a535-107">Om du anger ett namn på en arbets yta får denna cmdlet information om den arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="7a535-107">If you specify a workspace name, this cmdlet gets information about that workspace.</span></span>
<span data-ttu-id="7a535-108">Om du inte anger ett namn hämtas den här cmdleten information om alla arbets ytor i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="7a535-108">If you do not specify a name, this cmdlet gets information about all workspaces in a resource group.</span></span>
<span data-ttu-id="7a535-109">Om du inte anger ett namn och en resurs grupp får denna cmdlet information om alla arbets ytor i ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="7a535-109">If you do not specify a name and resource group, this cmdlet gets information about all workspaces in a subscription.</span></span>

## <span data-ttu-id="7a535-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7a535-110">EXAMPLES</span></span>

### <span data-ttu-id="7a535-111">Exempel 1: Hämta en arbets yta efter namn</span><span class="sxs-lookup"><span data-stu-id="7a535-111">Example 1: Get a workspace by name</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -Name "MyWorkspace" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="7a535-112">Med det här kommandot får du en arbets yta som heter min arbets yta i resurs gruppen med namnet ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="7a535-112">This command gets a workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="7a535-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7a535-113">PARAMETERS</span></span>

### <span data-ttu-id="7a535-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="7a535-114">-Name</span></span>
<span data-ttu-id="7a535-115">Anger arbets ytans namn.</span><span class="sxs-lookup"><span data-stu-id="7a535-115">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a535-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a535-116">-ResourceGroupName</span></span>
<span data-ttu-id="7a535-117">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="7a535-117">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a535-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a535-118">-DefaultProfile</span></span>
<span data-ttu-id="7a535-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7a535-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a535-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a535-120">CommonParameters</span></span>
<span data-ttu-id="7a535-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a535-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a535-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a535-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a535-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7a535-123">INPUTS</span></span>

## <span data-ttu-id="7a535-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7a535-124">OUTPUTS</span></span>

### <span data-ttu-id="7a535-125">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. OperationalInsights. Models. PSWorkspace]</span><span class="sxs-lookup"><span data-stu-id="7a535-125">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace]</span></span>

### <span data-ttu-id="7a535-126">Microsoft. Azure. commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="7a535-126">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="7a535-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7a535-127">NOTES</span></span>

## <span data-ttu-id="7a535-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7a535-128">RELATED LINKS</span></span>

[<span data-ttu-id="7a535-129">Cmdlets för Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="7a535-129">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


