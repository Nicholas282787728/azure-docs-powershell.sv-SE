---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/remove-azsentinelincident
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelIncident.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelIncident.md
ms.openlocfilehash: faf2c40bc43c1b42861bc93d2398d4d26731c112
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525566"
---
# <span data-ttu-id="c2995-101">Remove-AzSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="c2995-101">Remove-AzSentinelIncident</span></span>

## <span data-ttu-id="c2995-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c2995-102">SYNOPSIS</span></span>
<span data-ttu-id="c2995-103">Ta bort ett samtal.</span><span class="sxs-lookup"><span data-stu-id="c2995-103">Delete an Incident.</span></span>

## <span data-ttu-id="c2995-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c2995-104">SYNTAX</span></span>

### <span data-ttu-id="c2995-105">IncidentId (standard)</span><span class="sxs-lookup"><span data-stu-id="c2995-105">IncidentId (Default)</span></span>
```
Remove-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String> -IncidentId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2995-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="c2995-106">InputObject</span></span>
```
Remove-AzSentinelIncident -InputObject <PSSentinelIncident> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2995-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c2995-107">DESCRIPTION</span></span>
<span data-ttu-id="c2995-108">Cmdleten **Remove-AzSentinelIncident** tar bort en incident permanent från en angiven arbets yta.</span><span class="sxs-lookup"><span data-stu-id="c2995-108">The **Remove-AzSentinelIncident** cmdlet permanently deletes a Incident from a specified workspace.</span></span>
<span data-ttu-id="c2995-109">Du kan skicka ett **incident** objekt med hjälp av en pipeline-operator eller så kan du ange de parametrar som krävs.</span><span class="sxs-lookup"><span data-stu-id="c2995-109">You can pass an **Incident** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="c2995-110">Du kan använda Confirm-parametern och $ConfirmPreference Windows PowerShell-variabel för att kontrol lera om cmdleten uppmanar dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="c2995-110">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="c2995-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c2995-111">EXAMPLES</span></span>

### <span data-ttu-id="c2995-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c2995-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
```

<span data-ttu-id="c2995-113">Det här kommandot tar bort incidenten från arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="c2995-113">This command removes the Incident from the workspace.</span></span>

## <span data-ttu-id="c2995-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c2995-114">PARAMETERS</span></span>

### <span data-ttu-id="c2995-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2995-115">-DefaultProfile</span></span>
<span data-ttu-id="c2995-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c2995-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2995-117">-IncidentId</span><span class="sxs-lookup"><span data-stu-id="c2995-117">-IncidentId</span></span>
<span data-ttu-id="c2995-118">Incident-ID.</span><span class="sxs-lookup"><span data-stu-id="c2995-118">Incident Id.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2995-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c2995-119">-InputObject</span></span>
<span data-ttu-id="c2995-120">InputObject.</span><span class="sxs-lookup"><span data-stu-id="c2995-120">InputObject.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2995-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c2995-121">-PassThru</span></span>
<span data-ttu-id="c2995-122">PassThru</span><span class="sxs-lookup"><span data-stu-id="c2995-122">PassThru</span></span>

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

### <span data-ttu-id="c2995-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2995-123">-ResourceGroupName</span></span>
<span data-ttu-id="c2995-124">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="c2995-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2995-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c2995-125">-WorkspaceName</span></span>
<span data-ttu-id="c2995-126">Namn på arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="c2995-126">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2995-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c2995-127">-Confirm</span></span>
<span data-ttu-id="c2995-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c2995-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2995-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2995-129">-WhatIf</span></span>
<span data-ttu-id="c2995-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c2995-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2995-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c2995-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2995-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2995-132">CommonParameters</span></span>
<span data-ttu-id="c2995-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2995-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2995-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c2995-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2995-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c2995-135">INPUTS</span></span>

### <span data-ttu-id="c2995-136">System. String</span><span class="sxs-lookup"><span data-stu-id="c2995-136">System.String</span></span>
### <span data-ttu-id="c2995-137">Microsoft. Azure. commands. SecurityInsights. Models. incidenter. PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="c2995-137">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>
## <span data-ttu-id="c2995-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c2995-138">OUTPUTS</span></span>

### <span data-ttu-id="c2995-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c2995-139">System.Boolean</span></span>
## <span data-ttu-id="c2995-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c2995-140">NOTES</span></span>

## <span data-ttu-id="c2995-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c2995-141">RELATED LINKS</span></span>
