---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: F94415DA-1A4A-4D37-A626-1EDF5D1EFE74
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 05bcd77a732be66c426f456f6058e74107b6eb8d
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/13/2020
ms.locfileid: "93928346"
---
# <span data-ttu-id="2c615-101">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="2c615-101">Get-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="2c615-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2c615-102">SYNOPSIS</span></span>
<span data-ttu-id="2c615-103">Hämtar information om en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="2c615-103">Gets information about a workspace.</span></span>

## <span data-ttu-id="2c615-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2c615-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c615-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2c615-105">DESCRIPTION</span></span>
<span data-ttu-id="2c615-106">Cmdleten **Get-AzOperationalInsightsWorkspace** hämtar information om en befintlig arbets yta.</span><span class="sxs-lookup"><span data-stu-id="2c615-106">The **Get-AzOperationalInsightsWorkspace** cmdlet gets information about an existing workspace.</span></span>
<span data-ttu-id="2c615-107">Om du anger ett namn på en arbets yta får denna cmdlet information om den arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="2c615-107">If you specify a workspace name, this cmdlet gets information about that workspace.</span></span>
<span data-ttu-id="2c615-108">Om du inte anger ett namn hämtas den här cmdleten information om alla arbets ytor i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="2c615-108">If you do not specify a name, this cmdlet gets information about all workspaces in a resource group.</span></span>
<span data-ttu-id="2c615-109">Om du inte anger ett namn och en resurs grupp får denna cmdlet information om alla arbets ytor i ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="2c615-109">If you do not specify a name and resource group, this cmdlet gets information about all workspaces in a subscription.</span></span>

## <span data-ttu-id="2c615-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2c615-110">EXAMPLES</span></span>

### <span data-ttu-id="2c615-111">Exempel 1: Hämta en arbets yta efter namn</span><span class="sxs-lookup"><span data-stu-id="2c615-111">Example 1: Get a workspace by name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -Name "MyWorkspace" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="2c615-112">Med det här kommandot får du en arbets yta som heter min arbets yta i resurs gruppen med namnet ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="2c615-112">This command gets a workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="2c615-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2c615-113">PARAMETERS</span></span>

### <span data-ttu-id="2c615-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c615-114">-DefaultProfile</span></span>
<span data-ttu-id="2c615-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="2c615-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2c615-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="2c615-116">-Name</span></span>
<span data-ttu-id="2c615-117">Anger arbets ytans namn.</span><span class="sxs-lookup"><span data-stu-id="2c615-117">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="2c615-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c615-118">-ResourceGroupName</span></span>
<span data-ttu-id="2c615-119">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="2c615-119">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="2c615-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c615-120">CommonParameters</span></span>
<span data-ttu-id="2c615-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c615-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c615-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c615-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c615-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2c615-123">INPUTS</span></span>

### <span data-ttu-id="2c615-124">System. String</span><span class="sxs-lookup"><span data-stu-id="2c615-124">System.String</span></span>

## <span data-ttu-id="2c615-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2c615-125">OUTPUTS</span></span>

### <span data-ttu-id="2c615-126">Microsoft. Azure. commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="2c615-126">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="2c615-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2c615-127">NOTES</span></span>

## <span data-ttu-id="2c615-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2c615-128">RELATED LINKS</span></span>

[<span data-ttu-id="2c615-129">Cmdlets för Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="2c615-129">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


