---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: f3d00ba82bbafce42cca49c60d443cd244f83df3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262164"
---
# <span data-ttu-id="2df1c-101">Get-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="2df1c-101">Get-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="2df1c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2df1c-102">SYNOPSIS</span></span>
<span data-ttu-id="2df1c-103">Hämta en resurs för webbprogramsomfattande privata länkar</span><span class="sxs-lookup"><span data-stu-id="2df1c-103">Get for private link scoped resource</span></span>

## <span data-ttu-id="2df1c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2df1c-104">SYNTAX</span></span>

### <span data-ttu-id="2df1c-105">ByScopeParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="2df1c-105">ByScopeParameterSet (Default)</span></span>
```
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName <String> -ScopeName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2df1c-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2df1c-106">ByInputObjectParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScopedResource [-Name <String>] -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2df1c-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2df1c-107">ByResourceIdParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScopedResource -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2df1c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2df1c-108">DESCRIPTION</span></span>
<span data-ttu-id="2df1c-109">Hämta eller lista för den privata länk omfattnings resursen, omfattnings resursen kan vara logganalys-arbetsyta eller Application Insights-komponent</span><span class="sxs-lookup"><span data-stu-id="2df1c-109">Get or list for private link scoped resource, scoped resource could be Log Analytics workspace or Application Insights component</span></span>

## <span data-ttu-id="2df1c-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2df1c-110">EXAMPLES</span></span>

### <span data-ttu-id="2df1c-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2df1c-111">Example 1</span></span>
```powershell
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name"
```

<span data-ttu-id="2df1c-112">Lista över webbprogramsomfattande resurser under den privata länk omfattningen "scope_name"</span><span class="sxs-lookup"><span data-stu-id="2df1c-112">List scoped resource under private link scope "scope_name"</span></span>

### <span data-ttu-id="2df1c-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="2df1c-113">Example 2</span></span>
```powershell
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="2df1c-114">Hämta den webbprogramsomfattande resursen under den privata länk omfattningen "scope_name" med namnet "scoped_resource_name"</span><span class="sxs-lookup"><span data-stu-id="2df1c-114">Get scoped resource under private link scope "scope_name" with name "scoped_resource_name"</span></span>

## <span data-ttu-id="2df1c-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2df1c-115">PARAMETERS</span></span>

### <span data-ttu-id="2df1c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2df1c-116">-DefaultProfile</span></span>
<span data-ttu-id="2df1c-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2df1c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2df1c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2df1c-118">-InputObject</span></span>
<span data-ttu-id="2df1c-119">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="2df1c-119">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="2df1c-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="2df1c-120">-Name</span></span>
<span data-ttu-id="2df1c-121">Omfångs resurs namn</span><span class="sxs-lookup"><span data-stu-id="2df1c-121">Scoped resource Name</span></span>

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

### <span data-ttu-id="2df1c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2df1c-122">-ResourceGroupName</span></span>
<span data-ttu-id="2df1c-123">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="2df1c-123">Resource Group Name</span></span>

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

### <span data-ttu-id="2df1c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2df1c-124">-ResourceId</span></span>
<span data-ttu-id="2df1c-125">Resurs-ID</span><span class="sxs-lookup"><span data-stu-id="2df1c-125">Resource Id</span></span>

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

### <span data-ttu-id="2df1c-126">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="2df1c-126">-ScopeName</span></span>
<span data-ttu-id="2df1c-127">Namn på privat länk</span><span class="sxs-lookup"><span data-stu-id="2df1c-127">Private Link Scope Name</span></span>

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

### <span data-ttu-id="2df1c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2df1c-128">CommonParameters</span></span>
<span data-ttu-id="2df1c-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2df1c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2df1c-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2df1c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2df1c-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2df1c-131">INPUTS</span></span>

### <span data-ttu-id="2df1c-132">System. String</span><span class="sxs-lookup"><span data-stu-id="2df1c-132">System.String</span></span>

## <span data-ttu-id="2df1c-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2df1c-133">OUTPUTS</span></span>

### <span data-ttu-id="2df1c-134">icrosoft. Azure. commands. Insights. OutputClasses. PSMonitorPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="2df1c-134">icrosoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span></span>

## <span data-ttu-id="2df1c-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2df1c-135">NOTES</span></span>

## <span data-ttu-id="2df1c-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2df1c-136">RELATED LINKS</span></span>
