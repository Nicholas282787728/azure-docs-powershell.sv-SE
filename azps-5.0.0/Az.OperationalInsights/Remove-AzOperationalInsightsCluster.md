---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsCluster.md
ms.openlocfilehash: 4bcc62d3b5bd52382c5d02eb3761c51af27c1ca3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322196"
---
# <span data-ttu-id="3af95-101">Remove-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="3af95-101">Remove-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="3af95-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3af95-102">SYNOPSIS</span></span>
<span data-ttu-id="3af95-103">Ta bort kluster</span><span class="sxs-lookup"><span data-stu-id="3af95-103">Delete cluster</span></span>

## <span data-ttu-id="3af95-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3af95-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsCluster [-ResourceGroupName] <String> [-ClusterName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3af95-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3af95-105">DESCRIPTION</span></span>
<span data-ttu-id="3af95-106">Ta bort kluster, Använd bara för kluster med etablerings status "lyckades"</span><span class="sxs-lookup"><span data-stu-id="3af95-106">Delete cluster, only apply to clusters with provisioning state "Succeeded"</span></span>

## <span data-ttu-id="3af95-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3af95-107">EXAMPLES</span></span>

### <span data-ttu-id="3af95-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3af95-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsCluster -ResourceGroupName {rg-name} -ClusterName {cluster-name}

true
```

<span data-ttu-id="3af95-109">Ta bort kluster</span><span class="sxs-lookup"><span data-stu-id="3af95-109">Delete cluster</span></span>

## <span data-ttu-id="3af95-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3af95-110">PARAMETERS</span></span>

### <span data-ttu-id="3af95-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3af95-111">-AsJob</span></span>
<span data-ttu-id="3af95-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="3af95-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3af95-113">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="3af95-113">-ClusterName</span></span>
<span data-ttu-id="3af95-114">Kluster namnet.</span><span class="sxs-lookup"><span data-stu-id="3af95-114">The cluster name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3af95-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3af95-115">-DefaultProfile</span></span>
<span data-ttu-id="3af95-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3af95-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3af95-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3af95-117">-ResourceGroupName</span></span>
<span data-ttu-id="3af95-118">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="3af95-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3af95-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3af95-119">-Confirm</span></span>
<span data-ttu-id="3af95-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3af95-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3af95-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3af95-121">-WhatIf</span></span>
<span data-ttu-id="3af95-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3af95-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3af95-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3af95-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3af95-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3af95-124">CommonParameters</span></span>
<span data-ttu-id="3af95-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3af95-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3af95-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3af95-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3af95-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3af95-127">INPUTS</span></span>

### <span data-ttu-id="3af95-128">System. String</span><span class="sxs-lookup"><span data-stu-id="3af95-128">System.String</span></span>

## <span data-ttu-id="3af95-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3af95-129">OUTPUTS</span></span>

### <span data-ttu-id="3af95-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3af95-130">System.Boolean</span></span>

## <span data-ttu-id="3af95-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3af95-131">NOTES</span></span>

## <span data-ttu-id="3af95-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3af95-132">RELATED LINKS</span></span>