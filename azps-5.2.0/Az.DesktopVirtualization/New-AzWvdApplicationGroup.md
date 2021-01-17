---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplicationGroup.md
ms.openlocfilehash: 6cfee237c1104a77f0e1790c4980e8eb793a771c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98398728"
---
# <span data-ttu-id="ffb1a-101">New-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="ffb1a-101">New-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="ffb1a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ffb1a-102">SYNOPSIS</span></span>
<span data-ttu-id="ffb1a-103">Skapa eller uppdatera en applicationGroup.</span><span class="sxs-lookup"><span data-stu-id="ffb1a-103">Create or update an applicationGroup.</span></span>

## <span data-ttu-id="ffb1a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ffb1a-104">SYNTAX</span></span>

```
New-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String>
 -ApplicationGroupType <ApplicationGroupType> -HostPoolArmPath <String> -Location <String>
 [-SubscriptionId <String>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ffb1a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ffb1a-105">DESCRIPTION</span></span>
<span data-ttu-id="ffb1a-106">Skapa eller uppdatera en applicationGroup.</span><span class="sxs-lookup"><span data-stu-id="ffb1a-106">Create or update an applicationGroup.</span></span>

## <span data-ttu-id="ffb1a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ffb1a-107">EXAMPLES</span></span>

### <span data-ttu-id="ffb1a-108">Exempel 1: skapa ett virtuellt skriv bord i Windows med ett ApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="ffb1a-108">Example 1: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> New-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                            -Name ApplicationGroupName `
                            -Location 'eastus' `
                            -FriendlyName 'Friendly Name' `
                            -Description 'Description' `
                            -HostPoolArmPath '/subscriptions/SubscriptionId/resourcegroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/hostPools/HostPoolName' `
                            -ApplicationGroupType 'RemoteApp'

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="ffb1a-109">Det här kommandot skapar en Windows Virtual Desktop-ApplicationGroup i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="ffb1a-109">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

### <span data-ttu-id="ffb1a-110">Exempel 2: skapa ett virtuellt skriv bord i Windows ApplicationGroup efter namn</span><span class="sxs-lookup"><span data-stu-id="ffb1a-110">Example 2: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> New-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                            -Name ApplicationGroupName `
                            -Location 'eastus' `
                            -FriendlyName 'Friendly Name' `
                            -Description 'Description' `
                            -HostPoolArmPath '/subscriptions/SubscriptionId/resourcegroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/hostPools/HostPoolName' `
                            -ApplicationGroupType 'Desktop'

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="ffb1a-111">Det här kommandot skapar en Windows Virtual Desktop-ApplicationGroup i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="ffb1a-111">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

## <span data-ttu-id="ffb1a-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ffb1a-112">PARAMETERS</span></span>

### <span data-ttu-id="ffb1a-113">-ApplicationGroupType</span><span class="sxs-lookup"><span data-stu-id="ffb1a-113">-ApplicationGroupType</span></span>
<span data-ttu-id="ffb1a-114">Resurs typ för ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="ffb1a-114">Resource Type of ApplicationGroup.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.ApplicationGroupType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffb1a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffb1a-115">-DefaultProfile</span></span>
<span data-ttu-id="ffb1a-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ffb1a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ffb1a-117">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="ffb1a-117">-Description</span></span>
<span data-ttu-id="ffb1a-118">Beskrivning av ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="ffb1a-118">Description of ApplicationGroup.</span></span>

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

### <span data-ttu-id="ffb1a-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="ffb1a-119">-FriendlyName</span></span>
<span data-ttu-id="ffb1a-120">Eget namn på ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="ffb1a-120">Friendly name of ApplicationGroup.</span></span>

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

### <span data-ttu-id="ffb1a-121">-HostPoolArmPath</span><span class="sxs-lookup"><span data-stu-id="ffb1a-121">-HostPoolArmPath</span></span>
<span data-ttu-id="ffb1a-122">HostPool arm sökväg till ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="ffb1a-122">HostPool arm path of ApplicationGroup.</span></span>

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

### <span data-ttu-id="ffb1a-123">-Plats</span><span class="sxs-lookup"><span data-stu-id="ffb1a-123">-Location</span></span>
<span data-ttu-id="ffb1a-124">Den Geo-plats där resursen bor</span><span class="sxs-lookup"><span data-stu-id="ffb1a-124">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="ffb1a-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="ffb1a-125">-Name</span></span>
<span data-ttu-id="ffb1a-126">Namnet på program gruppen</span><span class="sxs-lookup"><span data-stu-id="ffb1a-126">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffb1a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffb1a-127">-ResourceGroupName</span></span>
<span data-ttu-id="ffb1a-128">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ffb1a-128">The name of the resource group.</span></span>
<span data-ttu-id="ffb1a-129">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="ffb1a-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="ffb1a-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ffb1a-130">-SubscriptionId</span></span>
<span data-ttu-id="ffb1a-131">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="ffb1a-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="ffb1a-132">-Tagg</span><span class="sxs-lookup"><span data-stu-id="ffb1a-132">-Tag</span></span>
<span data-ttu-id="ffb1a-133">Resource-taggar.</span><span class="sxs-lookup"><span data-stu-id="ffb1a-133">Resource tags.</span></span>

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

### <span data-ttu-id="ffb1a-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ffb1a-134">-Confirm</span></span>
<span data-ttu-id="ffb1a-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ffb1a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffb1a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffb1a-136">-WhatIf</span></span>
<span data-ttu-id="ffb1a-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ffb1a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffb1a-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ffb1a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffb1a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffb1a-139">CommonParameters</span></span>
<span data-ttu-id="ffb1a-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffb1a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffb1a-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ffb1a-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffb1a-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ffb1a-142">INPUTS</span></span>

## <span data-ttu-id="ffb1a-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ffb1a-143">OUTPUTS</span></span>

### <span data-ttu-id="ffb1a-144">Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. Api20201019Preview. IApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="ffb1a-144">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IApplicationGroup</span></span>

## <span data-ttu-id="ffb1a-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ffb1a-145">NOTES</span></span>

<span data-ttu-id="ffb1a-146">ALIAS</span><span class="sxs-lookup"><span data-stu-id="ffb1a-146">ALIASES</span></span>

## <span data-ttu-id="ffb1a-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ffb1a-147">RELATED LINKS</span></span>

