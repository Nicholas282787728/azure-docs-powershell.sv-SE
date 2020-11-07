---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: 198d52678bceccfd1045522881dc3a62fdebf752
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93926825"
---
# <span data-ttu-id="bd42e-101">New-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="bd42e-101">New-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="bd42e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bd42e-102">SYNOPSIS</span></span>
<span data-ttu-id="bd42e-103">skapa en privat länk</span><span class="sxs-lookup"><span data-stu-id="bd42e-103">create private link scope</span></span>

## <span data-ttu-id="bd42e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bd42e-104">SYNTAX</span></span>

```
New-AzInsightsPrivateLinkScope -Location <String> -ResourceGroupName <String> -Name <String> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd42e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bd42e-105">DESCRIPTION</span></span>
<span data-ttu-id="bd42e-106">skapa en privat länk</span><span class="sxs-lookup"><span data-stu-id="bd42e-106">create private link scope</span></span>

## <span data-ttu-id="bd42e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bd42e-107">EXAMPLES</span></span>

### <span data-ttu-id="bd42e-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="bd42e-108">Example 1</span></span>
```powershell
New-AzInsightsPrivateLinkScope -Location "eastus" -ResourceGroupName "rg_name" -Name "scope_name"
```

<span data-ttu-id="bd42e-109">skapa en privat länk omfattning med namnet "scope_name" under resurs gruppen "rg_name" i plats "öster"</span><span class="sxs-lookup"><span data-stu-id="bd42e-109">create private link scope with name "scope_name" under resource group "rg_name" in location "eastus"</span></span>

## <span data-ttu-id="bd42e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bd42e-110">PARAMETERS</span></span>

### <span data-ttu-id="bd42e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd42e-111">-DefaultProfile</span></span>
<span data-ttu-id="bd42e-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bd42e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd42e-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="bd42e-113">-Location</span></span>
<span data-ttu-id="bd42e-114">Plats</span><span class="sxs-lookup"><span data-stu-id="bd42e-114">Location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd42e-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="bd42e-115">-Name</span></span>
<span data-ttu-id="bd42e-116">Namn på privat länk</span><span class="sxs-lookup"><span data-stu-id="bd42e-116">Private Link Scope Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd42e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd42e-117">-ResourceGroupName</span></span>
<span data-ttu-id="bd42e-118">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="bd42e-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd42e-119">-Taggar</span><span class="sxs-lookup"><span data-stu-id="bd42e-119">-Tags</span></span>
<span data-ttu-id="bd42e-120">Taggen</span><span class="sxs-lookup"><span data-stu-id="bd42e-120">Tags</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd42e-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bd42e-121">-Confirm</span></span>
<span data-ttu-id="bd42e-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bd42e-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd42e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd42e-123">-WhatIf</span></span>
<span data-ttu-id="bd42e-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bd42e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd42e-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bd42e-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd42e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd42e-126">CommonParameters</span></span>
<span data-ttu-id="bd42e-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd42e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd42e-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bd42e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd42e-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bd42e-129">INPUTS</span></span>

### <span data-ttu-id="bd42e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="bd42e-130">System.String</span></span>

## <span data-ttu-id="bd42e-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bd42e-131">OUTPUTS</span></span>

### <span data-ttu-id="bd42e-132">Microsoft. Azure. commands. Insights. OutputClasses. PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="bd42e-132">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

## <span data-ttu-id="bd42e-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bd42e-133">NOTES</span></span>

## <span data-ttu-id="bd42e-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bd42e-134">RELATED LINKS</span></span>
