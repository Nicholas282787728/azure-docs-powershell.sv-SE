---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: f3d00ba82bbafce42cca49c60d443cd244f83df3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94273283"
---
# <span data-ttu-id="ed1ca-101">Get-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="ed1ca-101">Get-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="ed1ca-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ed1ca-102">SYNOPSIS</span></span>
<span data-ttu-id="ed1ca-103">Hämta en resurs för webbprogramsomfattande privata länkar</span><span class="sxs-lookup"><span data-stu-id="ed1ca-103">Get for private link scoped resource</span></span>

## <span data-ttu-id="ed1ca-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ed1ca-104">SYNTAX</span></span>

### <span data-ttu-id="ed1ca-105">ByScopeParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="ed1ca-105">ByScopeParameterSet (Default)</span></span>
```
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName <String> -ScopeName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed1ca-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed1ca-106">ByInputObjectParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScopedResource [-Name <String>] -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed1ca-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed1ca-107">ByResourceIdParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScopedResource -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ed1ca-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ed1ca-108">DESCRIPTION</span></span>
<span data-ttu-id="ed1ca-109">Hämta eller lista för den privata länk omfattnings resursen, omfattnings resursen kan vara logganalys-arbetsyta eller Application Insights-komponent</span><span class="sxs-lookup"><span data-stu-id="ed1ca-109">Get or list for private link scoped resource, scoped resource could be Log Analytics workspace or Application Insights component</span></span>

## <span data-ttu-id="ed1ca-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ed1ca-110">EXAMPLES</span></span>

### <span data-ttu-id="ed1ca-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ed1ca-111">Example 1</span></span>
```powershell
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name"
```

<span data-ttu-id="ed1ca-112">Lista över webbprogramsomfattande resurser under den privata länk omfattningen "scope_name"</span><span class="sxs-lookup"><span data-stu-id="ed1ca-112">List scoped resource under private link scope "scope_name"</span></span>

### <span data-ttu-id="ed1ca-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="ed1ca-113">Example 2</span></span>
```powershell
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="ed1ca-114">Hämta den webbprogramsomfattande resursen under den privata länk omfattningen "scope_name" med namnet "scoped_resource_name"</span><span class="sxs-lookup"><span data-stu-id="ed1ca-114">Get scoped resource under private link scope "scope_name" with name "scoped_resource_name"</span></span>

## <span data-ttu-id="ed1ca-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ed1ca-115">PARAMETERS</span></span>

### <span data-ttu-id="ed1ca-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed1ca-116">-DefaultProfile</span></span>
<span data-ttu-id="ed1ca-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ed1ca-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed1ca-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed1ca-118">-InputObject</span></span>
<span data-ttu-id="ed1ca-119">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="ed1ca-119">PSMonitorPrivateLinkScope</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed1ca-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="ed1ca-120">-Name</span></span>
<span data-ttu-id="ed1ca-121">Omfångs resurs namn</span><span class="sxs-lookup"><span data-stu-id="ed1ca-121">Scoped resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByScopeParameterSet, ByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed1ca-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed1ca-122">-ResourceGroupName</span></span>
<span data-ttu-id="ed1ca-123">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="ed1ca-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByScopeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed1ca-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed1ca-124">-ResourceId</span></span>
<span data-ttu-id="ed1ca-125">Resurs-ID</span><span class="sxs-lookup"><span data-stu-id="ed1ca-125">Resource Id</span></span>

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

### <span data-ttu-id="ed1ca-126">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="ed1ca-126">-ScopeName</span></span>
<span data-ttu-id="ed1ca-127">Namn på privat länk</span><span class="sxs-lookup"><span data-stu-id="ed1ca-127">Private Link Scope Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByScopeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed1ca-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed1ca-128">CommonParameters</span></span>
<span data-ttu-id="ed1ca-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed1ca-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed1ca-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ed1ca-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed1ca-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ed1ca-131">INPUTS</span></span>

### <span data-ttu-id="ed1ca-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ed1ca-132">System.String</span></span>

## <span data-ttu-id="ed1ca-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ed1ca-133">OUTPUTS</span></span>

### <span data-ttu-id="ed1ca-134">icrosoft. Azure. commands. Insights. OutputClasses. PSMonitorPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="ed1ca-134">icrosoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span></span>

## <span data-ttu-id="ed1ca-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ed1ca-135">NOTES</span></span>

## <span data-ttu-id="ed1ca-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ed1ca-136">RELATED LINKS</span></span>
