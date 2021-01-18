---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdWorkspace.md
ms.openlocfilehash: bd266bf6fe8a4239a1e2f10a5b462afd0fcc3577
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523706"
---
# <span data-ttu-id="5e493-101">Remove-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="5e493-101">Remove-AzWvdWorkspace</span></span>

## <span data-ttu-id="5e493-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5e493-102">SYNOPSIS</span></span>
<span data-ttu-id="5e493-103">Ta bort en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="5e493-103">Remove a workspace.</span></span>

## <span data-ttu-id="5e493-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5e493-104">SYNTAX</span></span>

### <span data-ttu-id="5e493-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="5e493-105">Delete (Default)</span></span>
```
Remove-AzWvdWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5e493-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5e493-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdWorkspace -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5e493-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5e493-107">DESCRIPTION</span></span>
<span data-ttu-id="5e493-108">Ta bort en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="5e493-108">Remove a workspace.</span></span>

## <span data-ttu-id="5e493-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5e493-109">EXAMPLES</span></span>

### <span data-ttu-id="5e493-110">Exempel 1: ta bort en virtuell Windows-arbetsyta med namn</span><span class="sxs-lookup"><span data-stu-id="5e493-110">Example 1: Delete a Windows Virtual Desktop Workspace by name</span></span>
```powershell
PS C:\> Remove-AzWvdWorkspace -ResourceGroupName ResourceGroupName -Name WorkspaceName
```

<span data-ttu-id="5e493-111">Det här kommandot tar bort en Windows Virtual Desktop-arbetsyta i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="5e493-111">This command deletes a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

## <span data-ttu-id="5e493-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5e493-112">PARAMETERS</span></span>

### <span data-ttu-id="5e493-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e493-113">-DefaultProfile</span></span>
<span data-ttu-id="5e493-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5e493-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e493-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5e493-115">-InputObject</span></span>
<span data-ttu-id="5e493-116">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="5e493-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e493-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="5e493-117">-Name</span></span>
<span data-ttu-id="5e493-118">Arbets ytans namn</span><span class="sxs-lookup"><span data-stu-id="5e493-118">The name of the workspace</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e493-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5e493-119">-PassThru</span></span>
<span data-ttu-id="5e493-120">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="5e493-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="5e493-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e493-121">-ResourceGroupName</span></span>
<span data-ttu-id="5e493-122">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="5e493-122">The name of the resource group.</span></span>
<span data-ttu-id="5e493-123">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="5e493-123">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e493-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5e493-124">-SubscriptionId</span></span>
<span data-ttu-id="5e493-125">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="5e493-125">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e493-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5e493-126">-Confirm</span></span>
<span data-ttu-id="5e493-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5e493-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e493-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e493-128">-WhatIf</span></span>
<span data-ttu-id="5e493-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5e493-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e493-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5e493-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e493-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e493-131">CommonParameters</span></span>
<span data-ttu-id="5e493-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e493-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e493-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5e493-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e493-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5e493-134">INPUTS</span></span>

### <span data-ttu-id="5e493-135">Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="5e493-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="5e493-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5e493-136">OUTPUTS</span></span>

### <span data-ttu-id="5e493-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5e493-137">System.Boolean</span></span>

## <span data-ttu-id="5e493-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5e493-138">NOTES</span></span>

<span data-ttu-id="5e493-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="5e493-139">ALIASES</span></span>

<span data-ttu-id="5e493-140">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="5e493-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5e493-141">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="5e493-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5e493-142">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5e493-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5e493-143">INPUTOBJECT <IDesktopVirtualizationIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="5e493-143">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5e493-144">`[ApplicationGroupName <String>]`: Namnet på program gruppen</span><span class="sxs-lookup"><span data-stu-id="5e493-144">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="5e493-145">`[ApplicationName <String>]`: Namnet på programmet i den angivna program gruppen</span><span class="sxs-lookup"><span data-stu-id="5e493-145">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="5e493-146">`[DesktopName <String>]`: Namnet på Skriv bordet i angiven Skriv bords grupp</span><span class="sxs-lookup"><span data-stu-id="5e493-146">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="5e493-147">`[HostPoolName <String>]`: Namnet på den värdbaserade poolen i den angivna resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="5e493-147">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="5e493-148">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="5e493-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5e493-149">`[MsixPackageFullName <String>]`: Det versions specifika paketet fullständigt namn för MSIX paketet i angivet hostpool</span><span class="sxs-lookup"><span data-stu-id="5e493-149">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="5e493-150">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="5e493-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="5e493-151">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="5e493-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="5e493-152">`[SessionHostName <String>]`: Namnet på sessions värden i den angivna poolen</span><span class="sxs-lookup"><span data-stu-id="5e493-152">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="5e493-153">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="5e493-153">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="5e493-154">`[UserSessionId <String>]`: Namnet på användarsessionen inom den angivna värd</span><span class="sxs-lookup"><span data-stu-id="5e493-154">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="5e493-155">`[WorkspaceName <String>]`: Arbets ytans namn</span><span class="sxs-lookup"><span data-stu-id="5e493-155">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="5e493-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5e493-156">RELATED LINKS</span></span>

