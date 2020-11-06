---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 6A834F26-C3D1-46DA-A4A6-1BB5B69291D0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSchema.md
ms.openlocfilehash: 0dcac3fac32094cf2d9a0e42abcffd6222783e78
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578816"
---
# <span data-ttu-id="3db68-101">Get-AzureRmOperationalInsightsSchema</span><span class="sxs-lookup"><span data-stu-id="3db68-101">Get-AzureRmOperationalInsightsSchema</span></span>

## <span data-ttu-id="3db68-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3db68-102">SYNOPSIS</span></span>
<span data-ttu-id="3db68-103">Returnerar det schema som är kopplat till en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="3db68-103">Returns the schema associated with a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3db68-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3db68-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsSchema [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3db68-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3db68-105">DESCRIPTION</span></span>
<span data-ttu-id="3db68-106">Cmdleten **Get-AzureRmOperationalInsightsSchema** returnerar det schema som är kopplat till den angivna arbets ytan i den resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="3db68-106">The **Get-AzureRmOperationalInsightsSchema** cmdlet returns the schema associated with the specified workspace within that resource group.</span></span>

## <span data-ttu-id="3db68-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3db68-107">EXAMPLES</span></span>

### <span data-ttu-id="3db68-108">Exempel 1: Hämta scheman för en arbets yta</span><span class="sxs-lookup"><span data-stu-id="3db68-108">Example 1: Get the schemas for a workspace</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsSchema -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="3db68-109">Det här kommandot får scheman som är associerade med en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="3db68-109">This command gets the schemas associated with a workspace.</span></span>

## <span data-ttu-id="3db68-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3db68-110">PARAMETERS</span></span>

### <span data-ttu-id="3db68-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3db68-111">-DefaultProfile</span></span>
<span data-ttu-id="3db68-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="3db68-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3db68-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3db68-113">-ResourceGroupName</span></span>
<span data-ttu-id="3db68-114">Anger namnet på en Azure-adressresurs som innehåller en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="3db68-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="3db68-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3db68-115">-WorkspaceName</span></span>
<span data-ttu-id="3db68-116">Anger ett namn på en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="3db68-116">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="3db68-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3db68-117">CommonParameters</span></span>
<span data-ttu-id="3db68-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3db68-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3db68-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3db68-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3db68-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3db68-120">INPUTS</span></span>

### <span data-ttu-id="3db68-121">System. String</span><span class="sxs-lookup"><span data-stu-id="3db68-121">System.String</span></span>

## <span data-ttu-id="3db68-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3db68-122">OUTPUTS</span></span>

### <span data-ttu-id="3db68-123">Microsoft. Azure. commands. OperationalInsights. Models. PSSearchGetSchemaResponse</span><span class="sxs-lookup"><span data-stu-id="3db68-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSchemaResponse</span></span>

## <span data-ttu-id="3db68-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3db68-124">NOTES</span></span>

## <span data-ttu-id="3db68-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3db68-125">RELATED LINKS</span></span>

[<span data-ttu-id="3db68-126">Cmdlets för Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="3db68-126">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


