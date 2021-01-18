---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdWorkspace.md
ms.openlocfilehash: b97db1a21afab939e94b776b3da8d43f3d1468b2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523718"
---
# <span data-ttu-id="58e52-101">New-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="58e52-101">New-AzWvdWorkspace</span></span>

## <span data-ttu-id="58e52-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="58e52-102">SYNOPSIS</span></span>
<span data-ttu-id="58e52-103">Skapa eller uppdatera en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="58e52-103">Create or update a workspace.</span></span>

## <span data-ttu-id="58e52-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="58e52-104">SYNTAX</span></span>

```
New-AzWvdWorkspace -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-ApplicationGroupReference <String[]>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="58e52-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="58e52-105">DESCRIPTION</span></span>
<span data-ttu-id="58e52-106">Skapa eller uppdatera en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="58e52-106">Create or update a workspace.</span></span>

## <span data-ttu-id="58e52-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="58e52-107">EXAMPLES</span></span>

### <span data-ttu-id="58e52-108">Exempel 1: skapa en virtuell Windows-arbetsyta med namn</span><span class="sxs-lookup"><span data-stu-id="58e52-108">Example 1: Create a Windows Virtual Desktop Workspace by name</span></span>
```powershell
PS C:\> New-AzWvdWorkspace -ResourceGroupName ResourceGroupName `
                        -Name WorkspaceName `
                        -Location 'eastus' `
                        -FriendlyName 'Friendly Name' `
                        -ApplicationGroupReference $null `
                        -Description 'Description'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="58e52-109">Det här kommandot skapar en virtuell Windows-arbetsyta i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="58e52-109">This command creates a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

### <span data-ttu-id="58e52-110">Exempel 2: skapa en virtuell Windows-arbetsyta med namn</span><span class="sxs-lookup"><span data-stu-id="58e52-110">Example 2: Create a Windows Virtual Desktop Workspace by name</span></span>
```powershell
PS C:\> New-AzWvdWorkspace -ResourceGroupName ResourceGroupName `
                        -Name WorkspaceName `
                        -Location 'eastus' `
                        -FriendlyName 'Friendly Name' `
                        -ApplicationGroupReference "/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName1","/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName2" `
                        -Description 'Description'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="58e52-111">Det här kommandot skapar en virtuell Windows-arbetsyta i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="58e52-111">This command creates a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

## <span data-ttu-id="58e52-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="58e52-112">PARAMETERS</span></span>

### <span data-ttu-id="58e52-113">-ApplicationGroupReference</span><span class="sxs-lookup"><span data-stu-id="58e52-113">-ApplicationGroupReference</span></span>
<span data-ttu-id="58e52-114">Lista över applicationGroup resurs-ID: n.</span><span class="sxs-lookup"><span data-stu-id="58e52-114">List of applicationGroup resource Ids.</span></span>

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

### <span data-ttu-id="58e52-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58e52-115">-DefaultProfile</span></span>
<span data-ttu-id="58e52-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="58e52-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58e52-117">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="58e52-117">-Description</span></span>
<span data-ttu-id="58e52-118">Beskrivning av arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="58e52-118">Description of Workspace.</span></span>

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

### <span data-ttu-id="58e52-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="58e52-119">-FriendlyName</span></span>
<span data-ttu-id="58e52-120">Eget namn på arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="58e52-120">Friendly name of Workspace.</span></span>

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

### <span data-ttu-id="58e52-121">-Plats</span><span class="sxs-lookup"><span data-stu-id="58e52-121">-Location</span></span>
<span data-ttu-id="58e52-122">Den Geo-plats där resursen bor</span><span class="sxs-lookup"><span data-stu-id="58e52-122">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="58e52-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="58e52-123">-Name</span></span>
<span data-ttu-id="58e52-124">Arbets ytans namn</span><span class="sxs-lookup"><span data-stu-id="58e52-124">The name of the workspace</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58e52-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58e52-125">-ResourceGroupName</span></span>
<span data-ttu-id="58e52-126">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="58e52-126">The name of the resource group.</span></span>
<span data-ttu-id="58e52-127">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="58e52-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="58e52-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="58e52-128">-SubscriptionId</span></span>
<span data-ttu-id="58e52-129">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="58e52-129">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58e52-130">-Tagg</span><span class="sxs-lookup"><span data-stu-id="58e52-130">-Tag</span></span>
<span data-ttu-id="58e52-131">Resource-taggar.</span><span class="sxs-lookup"><span data-stu-id="58e52-131">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58e52-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="58e52-132">-Confirm</span></span>
<span data-ttu-id="58e52-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="58e52-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58e52-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58e52-134">-WhatIf</span></span>
<span data-ttu-id="58e52-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="58e52-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58e52-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="58e52-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58e52-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58e52-137">CommonParameters</span></span>
<span data-ttu-id="58e52-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58e52-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58e52-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="58e52-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58e52-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="58e52-140">INPUTS</span></span>

## <span data-ttu-id="58e52-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="58e52-141">OUTPUTS</span></span>

### <span data-ttu-id="58e52-142">Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. Api20201102Preview. IWorkspace</span><span class="sxs-lookup"><span data-stu-id="58e52-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IWorkspace</span></span>

## <span data-ttu-id="58e52-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="58e52-143">NOTES</span></span>

<span data-ttu-id="58e52-144">ALIAS</span><span class="sxs-lookup"><span data-stu-id="58e52-144">ALIASES</span></span>

## <span data-ttu-id="58e52-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="58e52-145">RELATED LINKS</span></span>

