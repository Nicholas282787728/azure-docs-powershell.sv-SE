---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: c62dcefc2a4cfabc908c45454f3907c2da060f6c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98527324"
---
# <span data-ttu-id="defca-101">Remove-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="defca-101">Remove-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="defca-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="defca-102">SYNOPSIS</span></span>
<span data-ttu-id="defca-103">Koppla bort en tjänst för arbets ytan</span><span class="sxs-lookup"><span data-stu-id="defca-103">Unlink service for workspace</span></span>

## <span data-ttu-id="defca-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="defca-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="defca-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="defca-105">DESCRIPTION</span></span>
<span data-ttu-id="defca-106">Koppla bort en tjänst för arbets ytan</span><span class="sxs-lookup"><span data-stu-id="defca-106">Unlink service for workspace</span></span>

## <span data-ttu-id="defca-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="defca-107">EXAMPLES</span></span>

### <span data-ttu-id="defca-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="defca-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsLinkedService -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -LinkedServiceName cluster

true
```

<span data-ttu-id="defca-109">Koppla bort länkad tjänst för arbets yta</span><span class="sxs-lookup"><span data-stu-id="defca-109">Unlink linked service for workspace</span></span>

## <span data-ttu-id="defca-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="defca-110">PARAMETERS</span></span>

### <span data-ttu-id="defca-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="defca-111">-AsJob</span></span>
<span data-ttu-id="defca-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="defca-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="defca-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="defca-113">-DefaultProfile</span></span>
<span data-ttu-id="defca-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="defca-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="defca-115">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="defca-115">-LinkedServiceName</span></span>
<span data-ttu-id="defca-116">Arbets ytans namn.</span><span class="sxs-lookup"><span data-stu-id="defca-116">The Workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="defca-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="defca-117">-ResourceGroupName</span></span>
<span data-ttu-id="defca-118">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="defca-118">The resource group name.</span></span>

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

### <span data-ttu-id="defca-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="defca-119">-WorkspaceName</span></span>
<span data-ttu-id="defca-120">Arbets ytans namn.</span><span class="sxs-lookup"><span data-stu-id="defca-120">The Workspace name.</span></span>

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

### <span data-ttu-id="defca-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="defca-121">-Confirm</span></span>
<span data-ttu-id="defca-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="defca-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="defca-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="defca-123">-WhatIf</span></span>
<span data-ttu-id="defca-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="defca-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="defca-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="defca-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="defca-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="defca-126">CommonParameters</span></span>
<span data-ttu-id="defca-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="defca-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="defca-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="defca-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="defca-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="defca-129">INPUTS</span></span>

### <span data-ttu-id="defca-130">System. String</span><span class="sxs-lookup"><span data-stu-id="defca-130">System.String</span></span>

## <span data-ttu-id="defca-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="defca-131">OUTPUTS</span></span>

### <span data-ttu-id="defca-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="defca-132">System.Boolean</span></span>

## <span data-ttu-id="defca-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="defca-133">NOTES</span></span>

## <span data-ttu-id="defca-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="defca-134">RELATED LINKS</span></span>
