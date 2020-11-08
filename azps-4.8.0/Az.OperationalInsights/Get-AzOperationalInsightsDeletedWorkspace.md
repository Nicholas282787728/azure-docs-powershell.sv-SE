---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsdeletedworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDeletedWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDeletedWorkspace.md
ms.openlocfilehash: ce40458262d095f0e1fe58def1cf3d4508a6c6b8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261766"
---
# <span data-ttu-id="f5e8c-101">Get-AzOperationalInsightsDeletedWorkspace</span><span class="sxs-lookup"><span data-stu-id="f5e8c-101">Get-AzOperationalInsightsDeletedWorkspace</span></span>

## <span data-ttu-id="f5e8c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f5e8c-102">SYNOPSIS</span></span>
<span data-ttu-id="f5e8c-103">Lista borttagna arbets ytor.</span><span class="sxs-lookup"><span data-stu-id="f5e8c-103">List deleted workspaces.</span></span>

## <span data-ttu-id="f5e8c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f5e8c-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsDeletedWorkspace [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5e8c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f5e8c-105">DESCRIPTION</span></span>
<span data-ttu-id="f5e8c-106">Lista borttagna arbets ytor.</span><span class="sxs-lookup"><span data-stu-id="f5e8c-106">List deleted workspaces.</span></span>

## <span data-ttu-id="f5e8c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f5e8c-107">EXAMPLES</span></span>

### <span data-ttu-id="f5e8c-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f5e8c-108">Example 1</span></span>
```powershell
PS C:\> $workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
PS C:\> $workspace | Remove-AzOperationalInsightsWorkspace
PS C:\> Get-AzOperationalInsightsDeletedWorkspace -ResourceGroupName $rgname
```

<span data-ttu-id="f5e8c-109">Lista borttagna arbets ytor.</span><span class="sxs-lookup"><span data-stu-id="f5e8c-109">List deleted workspaces.</span></span>

## <span data-ttu-id="f5e8c-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f5e8c-110">PARAMETERS</span></span>

### <span data-ttu-id="f5e8c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5e8c-111">-DefaultProfile</span></span>
<span data-ttu-id="f5e8c-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f5e8c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5e8c-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5e8c-113">-ResourceGroupName</span></span>
<span data-ttu-id="f5e8c-114">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="f5e8c-114">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5e8c-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5e8c-115">CommonParameters</span></span>
<span data-ttu-id="f5e8c-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5e8c-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5e8c-117">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f5e8c-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5e8c-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f5e8c-118">INPUTS</span></span>

### <span data-ttu-id="f5e8c-119">System. String</span><span class="sxs-lookup"><span data-stu-id="f5e8c-119">System.String</span></span>

## <span data-ttu-id="f5e8c-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f5e8c-120">OUTPUTS</span></span>

### <span data-ttu-id="f5e8c-121">Microsoft. Azure. commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="f5e8c-121">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="f5e8c-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f5e8c-122">NOTES</span></span>

## <span data-ttu-id="f5e8c-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f5e8c-123">RELATED LINKS</span></span>
