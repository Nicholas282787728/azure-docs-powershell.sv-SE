---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 6A834F26-C3D1-46DA-A4A6-1BB5B69291D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSchema.md
ms.openlocfilehash: 077272f15d37645de86f144424fddd7e5f026908
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/13/2020
ms.locfileid: "93755166"
---
# <span data-ttu-id="eb97c-101">Get-AzOperationalInsightsSchema</span><span class="sxs-lookup"><span data-stu-id="eb97c-101">Get-AzOperationalInsightsSchema</span></span>

## <span data-ttu-id="eb97c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="eb97c-102">SYNOPSIS</span></span>
<span data-ttu-id="eb97c-103">Returnerar det schema som är kopplat till en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="eb97c-103">Returns the schema associated with a workspace.</span></span>

## <span data-ttu-id="eb97c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="eb97c-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsSchema [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb97c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="eb97c-105">DESCRIPTION</span></span>
<span data-ttu-id="eb97c-106">Cmdleten **Get-AzOperationalInsightsSchema** returnerar det schema som är kopplat till den angivna arbets ytan i den resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="eb97c-106">The **Get-AzOperationalInsightsSchema** cmdlet returns the schema associated with the specified workspace within that resource group.</span></span>

## <span data-ttu-id="eb97c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="eb97c-107">EXAMPLES</span></span>

### <span data-ttu-id="eb97c-108">Exempel 1: Hämta scheman för en arbets yta</span><span class="sxs-lookup"><span data-stu-id="eb97c-108">Example 1: Get the schemas for a workspace</span></span>
```
PS C:\>Get-AzOperationalInsightsSchema -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="eb97c-109">Det här kommandot får scheman som är associerade med en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="eb97c-109">This command gets the schemas associated with a workspace.</span></span>

## <span data-ttu-id="eb97c-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="eb97c-110">PARAMETERS</span></span>

### <span data-ttu-id="eb97c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb97c-111">-DefaultProfile</span></span>
<span data-ttu-id="eb97c-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="eb97c-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eb97c-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb97c-113">-ResourceGroupName</span></span>
<span data-ttu-id="eb97c-114">Anger namnet på en Azure-adressresurs som innehåller en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="eb97c-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="eb97c-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="eb97c-115">-WorkspaceName</span></span>
<span data-ttu-id="eb97c-116">Anger ett namn på en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="eb97c-116">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="eb97c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb97c-117">CommonParameters</span></span>
<span data-ttu-id="eb97c-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb97c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb97c-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb97c-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb97c-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="eb97c-120">INPUTS</span></span>

### <span data-ttu-id="eb97c-121">System. String</span><span class="sxs-lookup"><span data-stu-id="eb97c-121">System.String</span></span>

## <span data-ttu-id="eb97c-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="eb97c-122">OUTPUTS</span></span>

### <span data-ttu-id="eb97c-123">Microsoft. Azure. commands. OperationalInsights. Models. PSSearchGetSchemaResponse</span><span class="sxs-lookup"><span data-stu-id="eb97c-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSchemaResponse</span></span>

## <span data-ttu-id="eb97c-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="eb97c-124">NOTES</span></span>

## <span data-ttu-id="eb97c-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="eb97c-125">RELATED LINKS</span></span>

[<span data-ttu-id="eb97c-126">Cmdlets för Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="eb97c-126">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


