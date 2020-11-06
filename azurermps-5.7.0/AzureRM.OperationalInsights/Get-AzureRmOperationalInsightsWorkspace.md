---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: F94415DA-1A4A-4D37-A626-1EDF5D1EFE74
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspace.md
ms.openlocfilehash: b2bd8855d9c8b125b4bef72f42f0bd4a63071adb
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/21/2020
ms.locfileid: "93586628"
---
# <span data-ttu-id="4da8c-101">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="4da8c-101">Get-AzureRmOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="4da8c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4da8c-102">SYNOPSIS</span></span>
<span data-ttu-id="4da8c-103">Hämtar information om en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="4da8c-103">Gets information about a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4da8c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4da8c-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsWorkspace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4da8c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4da8c-105">DESCRIPTION</span></span>
<span data-ttu-id="4da8c-106">Cmdleten **Get-AzureRmOperationalInsightsWorkspace** hämtar information om en befintlig arbets yta.</span><span class="sxs-lookup"><span data-stu-id="4da8c-106">The **Get-AzureRmOperationalInsightsWorkspace** cmdlet gets information about an existing workspace.</span></span>
<span data-ttu-id="4da8c-107">Om du anger ett namn på en arbets yta får denna cmdlet information om den arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="4da8c-107">If you specify a workspace name, this cmdlet gets information about that workspace.</span></span>
<span data-ttu-id="4da8c-108">Om du inte anger ett namn hämtas den här cmdleten information om alla arbets ytor i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="4da8c-108">If you do not specify a name, this cmdlet gets information about all workspaces in a resource group.</span></span>
<span data-ttu-id="4da8c-109">Om du inte anger ett namn och en resurs grupp får denna cmdlet information om alla arbets ytor i ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="4da8c-109">If you do not specify a name and resource group, this cmdlet gets information about all workspaces in a subscription.</span></span>

## <span data-ttu-id="4da8c-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4da8c-110">EXAMPLES</span></span>

### <span data-ttu-id="4da8c-111">Exempel 1: Hämta en arbets yta efter namn</span><span class="sxs-lookup"><span data-stu-id="4da8c-111">Example 1: Get a workspace by name</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -Name "MyWorkspace" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="4da8c-112">Med det här kommandot får du en arbets yta som heter min arbets yta i resurs gruppen med namnet ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="4da8c-112">This command gets a workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="4da8c-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4da8c-113">PARAMETERS</span></span>

### <span data-ttu-id="4da8c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4da8c-114">-DefaultProfile</span></span>
<span data-ttu-id="4da8c-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="4da8c-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4da8c-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="4da8c-116">-Name</span></span>
<span data-ttu-id="4da8c-117">Anger arbets ytans namn.</span><span class="sxs-lookup"><span data-stu-id="4da8c-117">Specifies the workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4da8c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4da8c-118">-ResourceGroupName</span></span>
<span data-ttu-id="4da8c-119">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="4da8c-119">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4da8c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4da8c-120">CommonParameters</span></span>
<span data-ttu-id="4da8c-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4da8c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4da8c-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4da8c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4da8c-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4da8c-123">INPUTS</span></span>

### <span data-ttu-id="4da8c-124">Ingen</span><span class="sxs-lookup"><span data-stu-id="4da8c-124">None</span></span>
<span data-ttu-id="4da8c-125">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="4da8c-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4da8c-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4da8c-126">OUTPUTS</span></span>

### <span data-ttu-id="4da8c-127">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. OperationalInsights. Models. PSWorkspace]</span><span class="sxs-lookup"><span data-stu-id="4da8c-127">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace]</span></span>

### <span data-ttu-id="4da8c-128">Microsoft. Azure. commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="4da8c-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="4da8c-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4da8c-129">NOTES</span></span>

## <span data-ttu-id="4da8c-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4da8c-130">RELATED LINKS</span></span>

[<span data-ttu-id="4da8c-131">Cmdlets för Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="4da8c-131">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


