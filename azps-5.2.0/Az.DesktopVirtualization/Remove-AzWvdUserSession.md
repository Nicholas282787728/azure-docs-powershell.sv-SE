---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdusersession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdUserSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdUserSession.md
ms.openlocfilehash: d460b3e10ccc0e2d37a4e2aeb208d0b9f8006a10
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98396736"
---
# <span data-ttu-id="3bab3-101">Remove-AzWvdUserSession</span><span class="sxs-lookup"><span data-stu-id="3bab3-101">Remove-AzWvdUserSession</span></span>

## <span data-ttu-id="3bab3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3bab3-102">SYNOPSIS</span></span>
<span data-ttu-id="3bab3-103">Ta bort en userSession.</span><span class="sxs-lookup"><span data-stu-id="3bab3-103">Remove a userSession.</span></span>

## <span data-ttu-id="3bab3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3bab3-104">SYNTAX</span></span>

### <span data-ttu-id="3bab3-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="3bab3-105">Delete (Default)</span></span>
```
Remove-AzWvdUserSession -HostPoolName <String> -Id <String> -ResourceGroupName <String>
 -SessionHostName <String> [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3bab3-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3bab3-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdUserSession -InputObject <IDesktopVirtualizationIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3bab3-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3bab3-107">DESCRIPTION</span></span>
<span data-ttu-id="3bab3-108">Ta bort en userSession.</span><span class="sxs-lookup"><span data-stu-id="3bab3-108">Remove a userSession.</span></span>

## <span data-ttu-id="3bab3-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3bab3-109">EXAMPLES</span></span>

### <span data-ttu-id="3bab3-110">Exempel 1: ta bort en Windows Virtual Desktop UserSession efter namn</span><span class="sxs-lookup"><span data-stu-id="3bab3-110">Example 1: Delete a Windows Virtual Desktop UserSession by name</span></span>
```powershell
PS C:\> Remove-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName -Id 2
```

<span data-ttu-id="3bab3-111">Det här kommandot tar bort en Windows Virtual Desktop-UserSession i en sessionsnyckel.</span><span class="sxs-lookup"><span data-stu-id="3bab3-111">This command deletes a Windows Virtual Desktop UserSession in a Session Host.</span></span>

## <span data-ttu-id="3bab3-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3bab3-112">PARAMETERS</span></span>

### <span data-ttu-id="3bab3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bab3-113">-DefaultProfile</span></span>
<span data-ttu-id="3bab3-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3bab3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3bab3-115">-Force</span><span class="sxs-lookup"><span data-stu-id="3bab3-115">-Force</span></span>
<span data-ttu-id="3bab3-116">Tvinga flaggan att logga ut userSession.</span><span class="sxs-lookup"><span data-stu-id="3bab3-116">Force flag to login off userSession.</span></span>

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

### <span data-ttu-id="3bab3-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="3bab3-117">-HostPoolName</span></span>
<span data-ttu-id="3bab3-118">Namnet på den värdbaserade adresspoolen i den angivna resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="3bab3-118">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="3bab3-119">-ID</span><span class="sxs-lookup"><span data-stu-id="3bab3-119">-Id</span></span>
<span data-ttu-id="3bab3-120">Namnet på användarsessionen inom den angivna sessionsvärdservern</span><span class="sxs-lookup"><span data-stu-id="3bab3-120">The name of the user session within the specified session host</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: UserSessionId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bab3-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3bab3-121">-InputObject</span></span>
<span data-ttu-id="3bab3-122">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="3bab3-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3bab3-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3bab3-123">-PassThru</span></span>
<span data-ttu-id="3bab3-124">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="3bab3-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="3bab3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bab3-125">-ResourceGroupName</span></span>
<span data-ttu-id="3bab3-126">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="3bab3-126">The name of the resource group.</span></span>
<span data-ttu-id="3bab3-127">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="3bab3-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="3bab3-128">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="3bab3-128">-SessionHostName</span></span>
<span data-ttu-id="3bab3-129">Namnet på sessions värden i den angivna poolen</span><span class="sxs-lookup"><span data-stu-id="3bab3-129">The name of the session host within the specified host pool</span></span>

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

### <span data-ttu-id="3bab3-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3bab3-130">-SubscriptionId</span></span>
<span data-ttu-id="3bab3-131">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="3bab3-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="3bab3-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3bab3-132">-Confirm</span></span>
<span data-ttu-id="3bab3-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3bab3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3bab3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bab3-134">-WhatIf</span></span>
<span data-ttu-id="3bab3-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3bab3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3bab3-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3bab3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3bab3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bab3-137">CommonParameters</span></span>
<span data-ttu-id="3bab3-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bab3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bab3-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3bab3-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bab3-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3bab3-140">INPUTS</span></span>

### <span data-ttu-id="3bab3-141">Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="3bab3-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="3bab3-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3bab3-142">OUTPUTS</span></span>

### <span data-ttu-id="3bab3-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3bab3-143">System.Boolean</span></span>

## <span data-ttu-id="3bab3-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3bab3-144">NOTES</span></span>

<span data-ttu-id="3bab3-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="3bab3-145">ALIASES</span></span>

<span data-ttu-id="3bab3-146">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="3bab3-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3bab3-147">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="3bab3-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3bab3-148">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3bab3-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3bab3-149">INPUTOBJECT <IDesktopVirtualizationIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="3bab3-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3bab3-150">`[ApplicationGroupName <String>]`: Namnet på program gruppen</span><span class="sxs-lookup"><span data-stu-id="3bab3-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="3bab3-151">`[ApplicationName <String>]`: Namnet på programmet i den angivna program gruppen</span><span class="sxs-lookup"><span data-stu-id="3bab3-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="3bab3-152">`[DesktopName <String>]`: Namnet på Skriv bordet i angiven Skriv bords grupp</span><span class="sxs-lookup"><span data-stu-id="3bab3-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="3bab3-153">`[HostPoolName <String>]`: Namnet på den värdbaserade poolen i den angivna resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="3bab3-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="3bab3-154">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="3bab3-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3bab3-155">`[MsixPackageFullName <String>]`: Det versions specifika paketet fullständigt namn för MSIX paketet i angivet hostpool</span><span class="sxs-lookup"><span data-stu-id="3bab3-155">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="3bab3-156">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="3bab3-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="3bab3-157">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="3bab3-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="3bab3-158">`[SessionHostName <String>]`: Namnet på sessions värden i den angivna poolen</span><span class="sxs-lookup"><span data-stu-id="3bab3-158">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="3bab3-159">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="3bab3-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="3bab3-160">`[UserSessionId <String>]`: Namnet på användarsessionen inom den angivna värd</span><span class="sxs-lookup"><span data-stu-id="3bab3-160">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="3bab3-161">`[WorkspaceName <String>]`: Arbets ytans namn</span><span class="sxs-lookup"><span data-stu-id="3bab3-161">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="3bab3-162">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3bab3-162">RELATED LINKS</span></span>

