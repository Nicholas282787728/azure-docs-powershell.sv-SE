---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdWorkspace.md
ms.openlocfilehash: 420a73dc1890db1b26cff5ca5289dc030666b038
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319988"
---
# <span data-ttu-id="3104b-101">Remove-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="3104b-101">Remove-AzWvdWorkspace</span></span>

## <span data-ttu-id="3104b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3104b-102">SYNOPSIS</span></span>
<span data-ttu-id="3104b-103">Ta bort en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="3104b-103">Remove a workspace.</span></span>

## <span data-ttu-id="3104b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3104b-104">SYNTAX</span></span>

### <span data-ttu-id="3104b-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="3104b-105">Delete (Default)</span></span>
```
Remove-AzWvdWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3104b-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3104b-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdWorkspace -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3104b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3104b-107">DESCRIPTION</span></span>
<span data-ttu-id="3104b-108">Ta bort en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="3104b-108">Remove a workspace.</span></span>

## <span data-ttu-id="3104b-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3104b-109">EXAMPLES</span></span>

### <span data-ttu-id="3104b-110">Exempel 1: ta bort en Windows Virtual Desktop Worksapce efter namn</span><span class="sxs-lookup"><span data-stu-id="3104b-110">Example 1: Delete a Windows Virtual Desktop Worksapce by name</span></span>
```powershell
PS C:\> Remove-AzWvdWorksapce -ResourceGroupName ResourceGroupName -Name WorkspaceName
```

<span data-ttu-id="3104b-111">Det här kommandot tar bort en Windows Virtual Desktop-arbetsyta i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="3104b-111">This command deletes a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

## <span data-ttu-id="3104b-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3104b-112">PARAMETERS</span></span>

### <span data-ttu-id="3104b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3104b-113">-DefaultProfile</span></span>
<span data-ttu-id="3104b-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3104b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3104b-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3104b-115">-InputObject</span></span>
<span data-ttu-id="3104b-116">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="3104b-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3104b-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="3104b-117">-Name</span></span>
<span data-ttu-id="3104b-118">Arbets ytans namn</span><span class="sxs-lookup"><span data-stu-id="3104b-118">The name of the workspace</span></span>

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

### <span data-ttu-id="3104b-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3104b-119">-PassThru</span></span>
<span data-ttu-id="3104b-120">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="3104b-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="3104b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3104b-121">-ResourceGroupName</span></span>
<span data-ttu-id="3104b-122">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="3104b-122">The name of the resource group.</span></span>
<span data-ttu-id="3104b-123">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="3104b-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="3104b-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3104b-124">-SubscriptionId</span></span>
<span data-ttu-id="3104b-125">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="3104b-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="3104b-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3104b-126">-Confirm</span></span>
<span data-ttu-id="3104b-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3104b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3104b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3104b-128">-WhatIf</span></span>
<span data-ttu-id="3104b-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3104b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3104b-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3104b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3104b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3104b-131">CommonParameters</span></span>
<span data-ttu-id="3104b-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3104b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3104b-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3104b-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3104b-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3104b-134">INPUTS</span></span>

### <span data-ttu-id="3104b-135">Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="3104b-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="3104b-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3104b-136">OUTPUTS</span></span>

### <span data-ttu-id="3104b-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3104b-137">System.Boolean</span></span>

## <span data-ttu-id="3104b-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3104b-138">NOTES</span></span>

<span data-ttu-id="3104b-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="3104b-139">ALIASES</span></span>

<span data-ttu-id="3104b-140">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="3104b-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3104b-141">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="3104b-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3104b-142">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3104b-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3104b-143">INPUTOBJECT <IDesktopVirtualizationIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="3104b-143">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3104b-144">`[ApplicationGroupName <String>]`: Namnet på program gruppen</span><span class="sxs-lookup"><span data-stu-id="3104b-144">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="3104b-145">`[ApplicationName <String>]`: Namnet på programmet i den angivna program gruppen</span><span class="sxs-lookup"><span data-stu-id="3104b-145">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="3104b-146">`[DesktopName <String>]`: Namnet på Skriv bordet i angiven Skriv bords grupp</span><span class="sxs-lookup"><span data-stu-id="3104b-146">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="3104b-147">`[HostPoolName <String>]`: Namnet på den värdbaserade poolen i den angivna resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="3104b-147">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="3104b-148">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="3104b-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3104b-149">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="3104b-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="3104b-150">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="3104b-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="3104b-151">`[SessionHostName <String>]`: Namnet på sessions värden i den angivna poolen</span><span class="sxs-lookup"><span data-stu-id="3104b-151">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="3104b-152">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="3104b-152">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="3104b-153">`[UserSessionId <String>]`: Namnet på användarsessionen inom den angivna värd</span><span class="sxs-lookup"><span data-stu-id="3104b-153">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="3104b-154">`[WorkspaceName <String>]`: Arbets ytans namn</span><span class="sxs-lookup"><span data-stu-id="3104b-154">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="3104b-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3104b-155">RELATED LINKS</span></span>

