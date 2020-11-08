---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdWorkspace.md
ms.openlocfilehash: 30c0734656b79f532c56b47b64e9d7e918f92fa8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94101019"
---
# <span data-ttu-id="89259-101">Update-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="89259-101">Update-AzWvdWorkspace</span></span>

## <span data-ttu-id="89259-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="89259-102">SYNOPSIS</span></span>
<span data-ttu-id="89259-103">Uppdatera en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="89259-103">Update a workspace.</span></span>

## <span data-ttu-id="89259-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="89259-104">SYNTAX</span></span>

### <span data-ttu-id="89259-105">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="89259-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-ApplicationGroupReference <String[]>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="89259-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="89259-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdWorkspace -InputObject <IDesktopVirtualizationIdentity> [-ApplicationGroupReference <String[]>]
 [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="89259-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="89259-107">DESCRIPTION</span></span>
<span data-ttu-id="89259-108">Uppdatera en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="89259-108">Update a workspace.</span></span>

## <span data-ttu-id="89259-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="89259-109">EXAMPLES</span></span>

### <span data-ttu-id="89259-110">Exempel 1: uppdatera en Windows Virtual Desktop-Worksapce efter namn</span><span class="sxs-lookup"><span data-stu-id="89259-110">Example 1: Update a Windows Virtual Desktop Worksapce by name</span></span>
```powershell
PS C:\> Update-AzWvdWorkspace -ResourceGroupName ResourceGroupName `
                        -Name WorkspaceName `
                        -FriendlyName 'Friendly Name' `
                        -ApplicationGroupReference "/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName1","/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName2" `
                        -Description 'Description'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="89259-111">Det här kommandot uppdaterar en Windows Virtual Desktop-arbetsyta i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="89259-111">This command updates a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

## <span data-ttu-id="89259-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="89259-112">PARAMETERS</span></span>

### <span data-ttu-id="89259-113">-ApplicationGroupReference</span><span class="sxs-lookup"><span data-stu-id="89259-113">-ApplicationGroupReference</span></span>
<span data-ttu-id="89259-114">Lista över applicationGroup-länkar.</span><span class="sxs-lookup"><span data-stu-id="89259-114">List of applicationGroup links.</span></span>

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

### <span data-ttu-id="89259-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89259-115">-DefaultProfile</span></span>
<span data-ttu-id="89259-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="89259-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89259-117">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="89259-117">-Description</span></span>
<span data-ttu-id="89259-118">Beskrivning av arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="89259-118">Description of Workspace.</span></span>

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

### <span data-ttu-id="89259-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="89259-119">-FriendlyName</span></span>
<span data-ttu-id="89259-120">Eget namn på arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="89259-120">Friendly name of Workspace.</span></span>

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

### <span data-ttu-id="89259-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="89259-121">-InputObject</span></span>
<span data-ttu-id="89259-122">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="89259-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89259-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="89259-123">-Name</span></span>
<span data-ttu-id="89259-124">Arbets ytans namn</span><span class="sxs-lookup"><span data-stu-id="89259-124">The name of the workspace</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89259-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89259-125">-ResourceGroupName</span></span>
<span data-ttu-id="89259-126">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="89259-126">The name of the resource group.</span></span>
<span data-ttu-id="89259-127">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="89259-127">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89259-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="89259-128">-SubscriptionId</span></span>
<span data-ttu-id="89259-129">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="89259-129">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89259-130">-Tagg</span><span class="sxs-lookup"><span data-stu-id="89259-130">-Tag</span></span>
<span data-ttu-id="89259-131">Taggar som ska uppdateras</span><span class="sxs-lookup"><span data-stu-id="89259-131">tags to be updated</span></span>

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

### <span data-ttu-id="89259-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="89259-132">-Confirm</span></span>
<span data-ttu-id="89259-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="89259-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89259-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89259-134">-WhatIf</span></span>
<span data-ttu-id="89259-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="89259-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89259-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="89259-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89259-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89259-137">CommonParameters</span></span>
<span data-ttu-id="89259-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89259-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89259-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="89259-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89259-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="89259-140">INPUTS</span></span>

### <span data-ttu-id="89259-141">Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="89259-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="89259-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="89259-142">OUTPUTS</span></span>

### <span data-ttu-id="89259-143">Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. Api20191210Preview. IWorkspace</span><span class="sxs-lookup"><span data-stu-id="89259-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span></span>

## <span data-ttu-id="89259-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="89259-144">NOTES</span></span>

<span data-ttu-id="89259-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="89259-145">ALIASES</span></span>

<span data-ttu-id="89259-146">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="89259-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="89259-147">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="89259-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="89259-148">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="89259-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="89259-149">INPUTOBJECT <IDesktopVirtualizationIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="89259-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="89259-150">`[ApplicationGroupName <String>]`: Namnet på program gruppen</span><span class="sxs-lookup"><span data-stu-id="89259-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="89259-151">`[ApplicationName <String>]`: Namnet på programmet i den angivna program gruppen</span><span class="sxs-lookup"><span data-stu-id="89259-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="89259-152">`[DesktopName <String>]`: Namnet på Skriv bordet i angiven Skriv bords grupp</span><span class="sxs-lookup"><span data-stu-id="89259-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="89259-153">`[HostPoolName <String>]`: Namnet på den värdbaserade poolen i den angivna resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="89259-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="89259-154">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="89259-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="89259-155">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="89259-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="89259-156">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="89259-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="89259-157">`[SessionHostName <String>]`: Namnet på sessions värden i den angivna poolen</span><span class="sxs-lookup"><span data-stu-id="89259-157">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="89259-158">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="89259-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="89259-159">`[UserSessionId <String>]`: Namnet på användarsessionen inom den angivna värd</span><span class="sxs-lookup"><span data-stu-id="89259-159">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="89259-160">`[WorkspaceName <String>]`: Arbets ytans namn</span><span class="sxs-lookup"><span data-stu-id="89259-160">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="89259-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="89259-161">RELATED LINKS</span></span>

