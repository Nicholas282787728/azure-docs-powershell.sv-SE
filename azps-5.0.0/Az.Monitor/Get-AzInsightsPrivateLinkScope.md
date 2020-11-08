---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: d5986694ad0064265bbd4bad6e1efc378683ce97
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271829"
---
# <span data-ttu-id="ce101-101">Get-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="ce101-101">Get-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="ce101-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ce101-102">SYNOPSIS</span></span>
<span data-ttu-id="ce101-103">Hämta omfång för privata länkar</span><span class="sxs-lookup"><span data-stu-id="ce101-103">Get private link scope</span></span>

## <span data-ttu-id="ce101-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ce101-104">SYNTAX</span></span>

### <span data-ttu-id="ce101-105">ByResourceGroupParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="ce101-105">ByResourceGroupParameterSet (Default)</span></span>
```
Get-AzInsightsPrivateLinkScope [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ce101-106">ByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce101-106">ByResourceNameParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce101-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce101-107">ByResourceIdParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScope -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ce101-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ce101-108">DESCRIPTION</span></span>
<span data-ttu-id="ce101-109">Lista eller hämta omfattning för privat länk</span><span class="sxs-lookup"><span data-stu-id="ce101-109">List or get private link scope</span></span> 

## <span data-ttu-id="ce101-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ce101-110">EXAMPLES</span></span>

### <span data-ttu-id="ce101-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ce101-111">Example 1</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name"
```

<span data-ttu-id="ce101-112">Lista med privata länk omfattningar under resurs grupp "rg_name"</span><span class="sxs-lookup"><span data-stu-id="ce101-112">List private link scopes under resource group "rg_name"</span></span>

### <span data-ttu-id="ce101-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="ce101-113">Example 2</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name"
```

<span data-ttu-id="ce101-114">Få en privat länk med namnet "scope_name" under resurs gruppen "rg_name"</span><span class="sxs-lookup"><span data-stu-id="ce101-114">Get private link scope with name "scope_name" under resource group "rg_name"</span></span>

## <span data-ttu-id="ce101-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ce101-115">PARAMETERS</span></span>

### <span data-ttu-id="ce101-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce101-116">-DefaultProfile</span></span>
<span data-ttu-id="ce101-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ce101-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce101-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="ce101-118">-Name</span></span>
<span data-ttu-id="ce101-119">Namn på privat länk</span><span class="sxs-lookup"><span data-stu-id="ce101-119">Private Link Scope Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce101-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce101-120">-ResourceGroupName</span></span>
<span data-ttu-id="ce101-121">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="ce101-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce101-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ce101-122">-ResourceId</span></span>
<span data-ttu-id="ce101-123">Resurs-ID</span><span class="sxs-lookup"><span data-stu-id="ce101-123">Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce101-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce101-124">CommonParameters</span></span>
<span data-ttu-id="ce101-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce101-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce101-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ce101-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce101-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ce101-127">INPUTS</span></span>

### <span data-ttu-id="ce101-128">System. String</span><span class="sxs-lookup"><span data-stu-id="ce101-128">System.String</span></span>

## <span data-ttu-id="ce101-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ce101-129">OUTPUTS</span></span>

### <span data-ttu-id="ce101-130">Microsoft. Azure. commands. Insights. OutputClasses. PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="ce101-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

## <span data-ttu-id="ce101-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ce101-131">NOTES</span></span>

## <span data-ttu-id="ce101-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ce101-132">RELATED LINKS</span></span>
