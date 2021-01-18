---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsdeletedworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDeletedWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDeletedWorkspace.md
ms.openlocfilehash: ce40458262d095f0e1fe58def1cf3d4508a6c6b8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98527395"
---
# <span data-ttu-id="e6aca-101">Get-AzOperationalInsightsDeletedWorkspace</span><span class="sxs-lookup"><span data-stu-id="e6aca-101">Get-AzOperationalInsightsDeletedWorkspace</span></span>

## <span data-ttu-id="e6aca-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e6aca-102">SYNOPSIS</span></span>
<span data-ttu-id="e6aca-103">Lista borttagna arbets ytor.</span><span class="sxs-lookup"><span data-stu-id="e6aca-103">List deleted workspaces.</span></span>

## <span data-ttu-id="e6aca-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e6aca-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsDeletedWorkspace [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6aca-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e6aca-105">DESCRIPTION</span></span>
<span data-ttu-id="e6aca-106">Lista borttagna arbets ytor.</span><span class="sxs-lookup"><span data-stu-id="e6aca-106">List deleted workspaces.</span></span>

## <span data-ttu-id="e6aca-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e6aca-107">EXAMPLES</span></span>

### <span data-ttu-id="e6aca-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e6aca-108">Example 1</span></span>
```powershell
PS C:\> $workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
PS C:\> $workspace | Remove-AzOperationalInsightsWorkspace
PS C:\> Get-AzOperationalInsightsDeletedWorkspace -ResourceGroupName $rgname
```

<span data-ttu-id="e6aca-109">Lista borttagna arbets ytor.</span><span class="sxs-lookup"><span data-stu-id="e6aca-109">List deleted workspaces.</span></span>

## <span data-ttu-id="e6aca-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e6aca-110">PARAMETERS</span></span>

### <span data-ttu-id="e6aca-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6aca-111">-DefaultProfile</span></span>
<span data-ttu-id="e6aca-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e6aca-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6aca-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6aca-113">-ResourceGroupName</span></span>
<span data-ttu-id="e6aca-114">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="e6aca-114">The resource group name.</span></span>

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

### <span data-ttu-id="e6aca-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6aca-115">CommonParameters</span></span>
<span data-ttu-id="e6aca-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6aca-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6aca-117">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e6aca-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6aca-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e6aca-118">INPUTS</span></span>

### <span data-ttu-id="e6aca-119">System. String</span><span class="sxs-lookup"><span data-stu-id="e6aca-119">System.String</span></span>

## <span data-ttu-id="e6aca-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e6aca-120">OUTPUTS</span></span>

### <span data-ttu-id="e6aca-121">Microsoft. Azure. commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="e6aca-121">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="e6aca-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e6aca-122">NOTES</span></span>

## <span data-ttu-id="e6aca-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e6aca-123">RELATED LINKS</span></span>
