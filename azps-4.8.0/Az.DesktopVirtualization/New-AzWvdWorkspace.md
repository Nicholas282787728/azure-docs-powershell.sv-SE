---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdWorkspace.md
ms.openlocfilehash: fbd71d03c6f82bcb785105d9d75e155e9f7ef498
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262738"
---
# <span data-ttu-id="63d4f-101">New-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="63d4f-101">New-AzWvdWorkspace</span></span>

## <span data-ttu-id="63d4f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="63d4f-102">SYNOPSIS</span></span>
<span data-ttu-id="63d4f-103">Skapa eller uppdatera en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="63d4f-103">Create or update a workspace.</span></span>

## <span data-ttu-id="63d4f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="63d4f-104">SYNTAX</span></span>

```
New-AzWvdWorkspace -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-ApplicationGroupReference <String[]>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="63d4f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="63d4f-105">DESCRIPTION</span></span>
<span data-ttu-id="63d4f-106">Skapa eller uppdatera en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="63d4f-106">Create or update a workspace.</span></span>

## <span data-ttu-id="63d4f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="63d4f-107">EXAMPLES</span></span>

### <span data-ttu-id="63d4f-108">Exempel 1: skapa ett virtuellt skriv bord i Windows med ett Worksapce</span><span class="sxs-lookup"><span data-stu-id="63d4f-108">Example 1: Create a Windows Virtual Desktop Worksapce by name</span></span>
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

<span data-ttu-id="63d4f-109">Det här kommandot skapar en virtuell Windows-arbetsyta i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="63d4f-109">This command creates a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

### <span data-ttu-id="63d4f-110">Exempel 2: skapa ett virtuellt skriv bord i Windows Worksapce efter namn</span><span class="sxs-lookup"><span data-stu-id="63d4f-110">Example 2: Create a Windows Virtual Desktop Worksapce by name</span></span>
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

<span data-ttu-id="63d4f-111">Det här kommandot skapar en virtuell Windows-arbetsyta i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="63d4f-111">This command creates a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

## <span data-ttu-id="63d4f-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="63d4f-112">PARAMETERS</span></span>

### <span data-ttu-id="63d4f-113">-ApplicationGroupReference</span><span class="sxs-lookup"><span data-stu-id="63d4f-113">-ApplicationGroupReference</span></span>
<span data-ttu-id="63d4f-114">Lista över applicationGroup resurs-ID: n.</span><span class="sxs-lookup"><span data-stu-id="63d4f-114">List of applicationGroup resource Ids.</span></span>

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

### <span data-ttu-id="63d4f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63d4f-115">-DefaultProfile</span></span>
<span data-ttu-id="63d4f-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="63d4f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63d4f-117">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="63d4f-117">-Description</span></span>
<span data-ttu-id="63d4f-118">Beskrivning av arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="63d4f-118">Description of Workspace.</span></span>

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

### <span data-ttu-id="63d4f-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="63d4f-119">-FriendlyName</span></span>
<span data-ttu-id="63d4f-120">Eget namn på arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="63d4f-120">Friendly name of Workspace.</span></span>

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

### <span data-ttu-id="63d4f-121">-Plats</span><span class="sxs-lookup"><span data-stu-id="63d4f-121">-Location</span></span>
<span data-ttu-id="63d4f-122">Den Geo-plats där resursen bor</span><span class="sxs-lookup"><span data-stu-id="63d4f-122">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="63d4f-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="63d4f-123">-Name</span></span>
<span data-ttu-id="63d4f-124">Arbets ytans namn</span><span class="sxs-lookup"><span data-stu-id="63d4f-124">The name of the workspace</span></span>

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

### <span data-ttu-id="63d4f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63d4f-125">-ResourceGroupName</span></span>
<span data-ttu-id="63d4f-126">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="63d4f-126">The name of the resource group.</span></span>
<span data-ttu-id="63d4f-127">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="63d4f-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="63d4f-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="63d4f-128">-SubscriptionId</span></span>
<span data-ttu-id="63d4f-129">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="63d4f-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="63d4f-130">-Tagg</span><span class="sxs-lookup"><span data-stu-id="63d4f-130">-Tag</span></span>
<span data-ttu-id="63d4f-131">Resource-taggar.</span><span class="sxs-lookup"><span data-stu-id="63d4f-131">Resource tags.</span></span>

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

### <span data-ttu-id="63d4f-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="63d4f-132">-Confirm</span></span>
<span data-ttu-id="63d4f-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="63d4f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63d4f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63d4f-134">-WhatIf</span></span>
<span data-ttu-id="63d4f-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="63d4f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63d4f-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="63d4f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63d4f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63d4f-137">CommonParameters</span></span>
<span data-ttu-id="63d4f-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63d4f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63d4f-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="63d4f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63d4f-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="63d4f-140">INPUTS</span></span>

## <span data-ttu-id="63d4f-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="63d4f-141">OUTPUTS</span></span>

### <span data-ttu-id="63d4f-142">Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. Api20191210Preview. IWorkspace</span><span class="sxs-lookup"><span data-stu-id="63d4f-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span></span>

## <span data-ttu-id="63d4f-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="63d4f-143">NOTES</span></span>

<span data-ttu-id="63d4f-144">ALIAS</span><span class="sxs-lookup"><span data-stu-id="63d4f-144">ALIASES</span></span>

## <span data-ttu-id="63d4f-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="63d4f-145">RELATED LINKS</span></span>

