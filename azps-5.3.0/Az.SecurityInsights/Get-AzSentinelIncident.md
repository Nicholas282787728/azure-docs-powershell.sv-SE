---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentinelincident
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelIncident.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelIncident.md
ms.openlocfilehash: eb0854ee3a71af3bdf19d2258187c435fb0f5860
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525589"
---
# <span data-ttu-id="2cd3d-101">Get-AzSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="2cd3d-101">Get-AzSentinelIncident</span></span>

## <span data-ttu-id="2cd3d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2cd3d-102">SYNOPSIS</span></span>
<span data-ttu-id="2cd3d-103">Få ett problem.</span><span class="sxs-lookup"><span data-stu-id="2cd3d-103">Get an Incident.</span></span>

## <span data-ttu-id="2cd3d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2cd3d-104">SYNTAX</span></span>

### <span data-ttu-id="2cd3d-105">WorkspaceScope (standard)</span><span class="sxs-lookup"><span data-stu-id="2cd3d-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cd3d-106">IncidentId</span><span class="sxs-lookup"><span data-stu-id="2cd3d-106">IncidentId</span></span>
```
Get-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String> [-IncidentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cd3d-107">ID</span><span class="sxs-lookup"><span data-stu-id="2cd3d-107">ResourceId</span></span>
```
Get-AzSentinelIncident -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2cd3d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2cd3d-108">DESCRIPTION</span></span>
<span data-ttu-id="2cd3d-109">Cmdleten **Get-AzSentinelIncident** hämtar en incident från den angivna arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="2cd3d-109">The **Get-AzSentinelIncident** cmdlet gets an Incident from the specified workspace.</span></span>
<span data-ttu-id="2cd3d-110">Om du anger parametern *IncidentId* returneras ett enskilt **incident** objekt.</span><span class="sxs-lookup"><span data-stu-id="2cd3d-110">If you specify the *IncidentId* parameter, a single **Incident** object is returned.</span></span>
<span data-ttu-id="2cd3d-111">Om du inte anger parametern *IncidentId* returneras en matris med alla händelser på den angivna arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="2cd3d-111">If you do not specify the *IncidentId* parameter, an array containing all of the Incidents in the specified workspace are returned.</span></span>
<span data-ttu-id="2cd3d-112">Du kan använda **händelsen incident** för att uppdatera händelsen, till **exempel att lägga till anteckningar om felet**.</span><span class="sxs-lookup"><span data-stu-id="2cd3d-112">You can use the **Incident** object to update the Incident, for example you can add Notes the **Incident**.</span></span>

## <span data-ttu-id="2cd3d-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2cd3d-113">EXAMPLES</span></span>

### <span data-ttu-id="2cd3d-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2cd3d-114">Example 1</span></span>
```powershell
PS C:\> $Incidents = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="2cd3d-115">Det här exemplet får alla **händelser** på den angivna arbets ytan och lagrar dem sedan i $incidents variabel.</span><span class="sxs-lookup"><span data-stu-id="2cd3d-115">This example gets all of the **Incidents** in the specified workspace, and then stores it in the $Incidents variable.</span></span>

### <span data-ttu-id="2cd3d-116">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="2cd3d-116">Example 2</span></span>
```powershell
PS C:\> $Incident = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
```

<span data-ttu-id="2cd3d-117">Det här exemplet får en **incident** på den angivna arbets ytan och lagrar den sedan i $incident variabel.</span><span class="sxs-lookup"><span data-stu-id="2cd3d-117">This example gets an **Incident** in the specified workspace, and then stores it in the $Incident variable.</span></span>

## <span data-ttu-id="2cd3d-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2cd3d-118">PARAMETERS</span></span>

### <span data-ttu-id="2cd3d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cd3d-119">-DefaultProfile</span></span>
<span data-ttu-id="2cd3d-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2cd3d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2cd3d-121">-IncidentId</span><span class="sxs-lookup"><span data-stu-id="2cd3d-121">-IncidentId</span></span>
<span data-ttu-id="2cd3d-122">Incident-ID.</span><span class="sxs-lookup"><span data-stu-id="2cd3d-122">Incident Id.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cd3d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cd3d-123">-ResourceGroupName</span></span>
<span data-ttu-id="2cd3d-124">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="2cd3d-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cd3d-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2cd3d-125">-ResourceId</span></span>
<span data-ttu-id="2cd3d-126">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="2cd3d-126">Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cd3d-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2cd3d-127">-WorkspaceName</span></span>
<span data-ttu-id="2cd3d-128">Namn på arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="2cd3d-128">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cd3d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cd3d-129">CommonParameters</span></span>
<span data-ttu-id="2cd3d-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cd3d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cd3d-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2cd3d-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cd3d-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2cd3d-132">INPUTS</span></span>

### <span data-ttu-id="2cd3d-133">System. String</span><span class="sxs-lookup"><span data-stu-id="2cd3d-133">System.String</span></span>
## <span data-ttu-id="2cd3d-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2cd3d-134">OUTPUTS</span></span>

### <span data-ttu-id="2cd3d-135">Microsoft. Azure. commands. SecurityInsights. Models. incidenter. PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="2cd3d-135">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>
## <span data-ttu-id="2cd3d-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2cd3d-136">NOTES</span></span>

## <span data-ttu-id="2cd3d-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2cd3d-137">RELATED LINKS</span></span>
