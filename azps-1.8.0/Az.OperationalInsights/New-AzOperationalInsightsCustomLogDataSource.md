---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 6A08AF7C-1E18-40A1-B21E-12F94823D304
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightscustomlogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCustomLogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCustomLogDataSource.md
ms.openlocfilehash: e1b0ddc282ba72c175a13d8be18fed0bfc852b6c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747571"
---
# <span data-ttu-id="c40d5-101">New-AzOperationalInsightsCustomLogDataSource</span><span class="sxs-lookup"><span data-stu-id="c40d5-101">New-AzOperationalInsightsCustomLogDataSource</span></span>

## <span data-ttu-id="c40d5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c40d5-102">SYNOPSIS</span></span>
<span data-ttu-id="c40d5-103">Definierar en anpassad princip för logg insamling.</span><span class="sxs-lookup"><span data-stu-id="c40d5-103">Defines a custom log collection policy.</span></span>

## <span data-ttu-id="c40d5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c40d5-104">SYNTAX</span></span>

### <span data-ttu-id="c40d5-105">ByWorkspaceName (standard)</span><span class="sxs-lookup"><span data-stu-id="c40d5-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsCustomLogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-CustomLogRawJson] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c40d5-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="c40d5-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsCustomLogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-CustomLogRawJson] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c40d5-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c40d5-107">DESCRIPTION</span></span>
<span data-ttu-id="c40d5-108">Cmdleten **New-AzOperationalInsightsCustomLogDataSource** definierar en anpassad policy för logg insamling.</span><span class="sxs-lookup"><span data-stu-id="c40d5-108">The **New-AzOperationalInsightsCustomLogDataSource** cmdlet defines a custom log collection policy.</span></span>

## <span data-ttu-id="c40d5-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c40d5-109">EXAMPLES</span></span>

## <span data-ttu-id="c40d5-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c40d5-110">PARAMETERS</span></span>

### <span data-ttu-id="c40d5-111">-CustomLogRawJson</span><span class="sxs-lookup"><span data-stu-id="c40d5-111">-CustomLogRawJson</span></span>
<span data-ttu-id="c40d5-112">Anger den anpassade samlings principen som en hexadecimal-sträng (RAW Java Script Object Notation).</span><span class="sxs-lookup"><span data-stu-id="c40d5-112">Specifies the custom collection policy as a raw JavaScript Object Notation (JSON) string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c40d5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c40d5-113">-DefaultProfile</span></span>
<span data-ttu-id="c40d5-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="c40d5-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c40d5-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c40d5-115">-Force</span></span>
<span data-ttu-id="c40d5-116">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="c40d5-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c40d5-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="c40d5-117">-Name</span></span>
<span data-ttu-id="c40d5-118">Anger ett namn för data källan.</span><span class="sxs-lookup"><span data-stu-id="c40d5-118">Specifies a name for the data source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c40d5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c40d5-119">-ResourceGroupName</span></span>
<span data-ttu-id="c40d5-120">Anger namnet på en resurs grupp som innehåller datorer.</span><span class="sxs-lookup"><span data-stu-id="c40d5-120">Specifies the name of a resource group that contains computers.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c40d5-121">-Arbets yta</span><span class="sxs-lookup"><span data-stu-id="c40d5-121">-Workspace</span></span>
<span data-ttu-id="c40d5-122">Anger en arbets yta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="c40d5-122">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c40d5-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c40d5-123">-WorkspaceName</span></span>
<span data-ttu-id="c40d5-124">Anger namnet på en arbets yta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="c40d5-124">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c40d5-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c40d5-125">-Confirm</span></span>
<span data-ttu-id="c40d5-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c40d5-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c40d5-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c40d5-127">-WhatIf</span></span>
<span data-ttu-id="c40d5-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c40d5-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c40d5-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c40d5-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c40d5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c40d5-130">CommonParameters</span></span>
<span data-ttu-id="c40d5-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c40d5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c40d5-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c40d5-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c40d5-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c40d5-133">INPUTS</span></span>

### <span data-ttu-id="c40d5-134">Microsoft. Azure. commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="c40d5-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="c40d5-135">System. String</span><span class="sxs-lookup"><span data-stu-id="c40d5-135">System.String</span></span>

## <span data-ttu-id="c40d5-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c40d5-136">OUTPUTS</span></span>

### <span data-ttu-id="c40d5-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="c40d5-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="c40d5-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c40d5-138">NOTES</span></span>

## <span data-ttu-id="c40d5-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c40d5-139">RELATED LINKS</span></span>

[<span data-ttu-id="c40d5-140">Disable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="c40d5-140">Disable-AzOperationalInsightsLinuxCustomLogCollection</span></span>](./Disable-AzOperationalInsightsLinuxCustomLogCollection.md)

[<span data-ttu-id="c40d5-141">Enable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="c40d5-141">Enable-AzOperationalInsightsLinuxCustomLogCollection</span></span>](./Enable-AzOperationalInsightsLinuxCustomLogCollection.md)


