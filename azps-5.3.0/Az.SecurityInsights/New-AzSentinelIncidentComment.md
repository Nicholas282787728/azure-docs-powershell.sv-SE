---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentinelincidentcomment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncidentComment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncidentComment.md
ms.openlocfilehash: 8824832b1b3d09a24998891ad4636e3a3e0f1e19
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525573"
---
# <span data-ttu-id="37cd9-101">New-AzSentinelIncidentComment</span><span class="sxs-lookup"><span data-stu-id="37cd9-101">New-AzSentinelIncidentComment</span></span>

## <span data-ttu-id="37cd9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="37cd9-102">SYNOPSIS</span></span>
<span data-ttu-id="37cd9-103">Lägga till en incident kommentar till en händelse.</span><span class="sxs-lookup"><span data-stu-id="37cd9-103">Add an Incident Comment to an Incident.</span></span>

## <span data-ttu-id="37cd9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="37cd9-104">SYNTAX</span></span>

```
New-AzSentinelIncidentComment -ResourceGroupName <String> -WorkspaceName <String> -IncidentId <String>
 [-IncidentCommentId <String>] -Message <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37cd9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="37cd9-105">DESCRIPTION</span></span>
<span data-ttu-id="37cd9-106">Cmdleten **New-AzSentinelIncidentComment** skapar en incident kommentar från den angivna arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="37cd9-106">The **New-AzSentinelIncidentComment** cmdlet creates a Incident Comment from the specified workspace.</span></span>
<span data-ttu-id="37cd9-107">Du kan använda *Confirm* -parametern och $ConfirmPreference Windows PowerShell-variabel för att kontrol lera om cmdleten uppmanar dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="37cd9-107">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="37cd9-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="37cd9-108">EXAMPLES</span></span>

### <span data-ttu-id="37cd9-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="37cd9-109">Example 1</span></span>
```powershell
PS C:\> $Incident = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
PS C:\> $IncidentComment = New-AzSentinelIncidentComment -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId ($Incident.Name) -Message "Still needs investigation"
```

<span data-ttu-id="37cd9-110">I det här exemplet skapas en **IncidentComment** på den angivna arbets ytan och sedan lagras den i $IncidentComment variabel.</span><span class="sxs-lookup"><span data-stu-id="37cd9-110">This example creates an **IncidentComment** in the specified workspace, and then stores it in the $IncidentComment variable.</span></span>

## <span data-ttu-id="37cd9-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="37cd9-111">PARAMETERS</span></span>

### <span data-ttu-id="37cd9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37cd9-112">-DefaultProfile</span></span>
<span data-ttu-id="37cd9-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="37cd9-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37cd9-114">-IncidentCommentId</span><span class="sxs-lookup"><span data-stu-id="37cd9-114">-IncidentCommentId</span></span>
<span data-ttu-id="37cd9-115">ID för incident kommentar.</span><span class="sxs-lookup"><span data-stu-id="37cd9-115">Incident Comment Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37cd9-116">-IncidentId</span><span class="sxs-lookup"><span data-stu-id="37cd9-116">-IncidentId</span></span>
<span data-ttu-id="37cd9-117">Incident-ID.</span><span class="sxs-lookup"><span data-stu-id="37cd9-117">Incident Id.</span></span>

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

### <span data-ttu-id="37cd9-118">– Meddelande</span><span class="sxs-lookup"><span data-stu-id="37cd9-118">-Message</span></span>
<span data-ttu-id="37cd9-119">Händelse meddelande.</span><span class="sxs-lookup"><span data-stu-id="37cd9-119">Incident Message.</span></span>

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

### <span data-ttu-id="37cd9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37cd9-120">-ResourceGroupName</span></span>
<span data-ttu-id="37cd9-121">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="37cd9-121">Resource group name.</span></span>

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

### <span data-ttu-id="37cd9-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="37cd9-122">-WorkspaceName</span></span>
<span data-ttu-id="37cd9-123">Namn på arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="37cd9-123">Workspace Name.</span></span>

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

### <span data-ttu-id="37cd9-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="37cd9-124">-Confirm</span></span>
<span data-ttu-id="37cd9-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="37cd9-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37cd9-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37cd9-126">-WhatIf</span></span>
<span data-ttu-id="37cd9-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="37cd9-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="37cd9-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="37cd9-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37cd9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37cd9-129">CommonParameters</span></span>
<span data-ttu-id="37cd9-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37cd9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37cd9-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="37cd9-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37cd9-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="37cd9-132">INPUTS</span></span>

### <span data-ttu-id="37cd9-133">Ingen</span><span class="sxs-lookup"><span data-stu-id="37cd9-133">None</span></span>
## <span data-ttu-id="37cd9-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="37cd9-134">OUTPUTS</span></span>

### <span data-ttu-id="37cd9-135">Microsoft. Azure. commands. SecurityInsights. Models. IncidentComments. PSSentinelIncidentComment</span><span class="sxs-lookup"><span data-stu-id="37cd9-135">Microsoft.Azure.Commands.SecurityInsights.Models.IncidentComments.PSSentinelIncidentComment</span></span>
## <span data-ttu-id="37cd9-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="37cd9-136">NOTES</span></span>

## <span data-ttu-id="37cd9-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="37cd9-137">RELATED LINKS</span></span>
