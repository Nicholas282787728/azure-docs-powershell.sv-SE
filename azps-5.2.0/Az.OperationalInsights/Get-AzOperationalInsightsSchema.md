---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 6A834F26-C3D1-46DA-A4A6-1BB5B69291D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSchema.md
ms.openlocfilehash: 12c3e54725abfd5addf33a3d31edcb8f8016e9dd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98400027"
---
# <span data-ttu-id="bbb84-101">Get-AzOperationalInsightsSchema</span><span class="sxs-lookup"><span data-stu-id="bbb84-101">Get-AzOperationalInsightsSchema</span></span>

## <span data-ttu-id="bbb84-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bbb84-102">SYNOPSIS</span></span>
<span data-ttu-id="bbb84-103">Returnerar det schema som är kopplat till en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="bbb84-103">Returns the schema associated with a workspace.</span></span>

## <span data-ttu-id="bbb84-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bbb84-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsSchema [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bbb84-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bbb84-105">DESCRIPTION</span></span>
<span data-ttu-id="bbb84-106">Cmdleten **Get-AzOperationalInsightsSchema** returnerar det schema som är kopplat till den angivna arbets ytan i den resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="bbb84-106">The **Get-AzOperationalInsightsSchema** cmdlet returns the schema associated with the specified workspace within that resource group.</span></span>

## <span data-ttu-id="bbb84-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bbb84-107">EXAMPLES</span></span>

### <span data-ttu-id="bbb84-108">Exempel 1: Hämta scheman för en arbets yta</span><span class="sxs-lookup"><span data-stu-id="bbb84-108">Example 1: Get the schemas for a workspace</span></span>
```
PS C:\>Get-AzOperationalInsightsSchema -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="bbb84-109">Det här kommandot får scheman som är associerade med en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="bbb84-109">This command gets the schemas associated with a workspace.</span></span>

## <span data-ttu-id="bbb84-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bbb84-110">PARAMETERS</span></span>

### <span data-ttu-id="bbb84-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbb84-111">-DefaultProfile</span></span>
<span data-ttu-id="bbb84-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="bbb84-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bbb84-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbb84-113">-ResourceGroupName</span></span>
<span data-ttu-id="bbb84-114">Anger namnet på en Azure-adressresurs som innehåller en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="bbb84-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="bbb84-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="bbb84-115">-WorkspaceName</span></span>
<span data-ttu-id="bbb84-116">Anger ett namn på en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="bbb84-116">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="bbb84-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbb84-117">CommonParameters</span></span>
<span data-ttu-id="bbb84-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbb84-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbb84-119">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbb84-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbb84-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bbb84-120">INPUTS</span></span>

### <span data-ttu-id="bbb84-121">System. String</span><span class="sxs-lookup"><span data-stu-id="bbb84-121">System.String</span></span>

## <span data-ttu-id="bbb84-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bbb84-122">OUTPUTS</span></span>

### <span data-ttu-id="bbb84-123">Microsoft. Azure. commands. OperationalInsights. Models. PSSearchGetSchemaResponse</span><span class="sxs-lookup"><span data-stu-id="bbb84-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSchemaResponse</span></span>

## <span data-ttu-id="bbb84-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bbb84-124">NOTES</span></span>

## <span data-ttu-id="bbb84-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bbb84-125">RELATED LINKS</span></span>

[<span data-ttu-id="bbb84-126">Cmdlets för Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="bbb84-126">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


