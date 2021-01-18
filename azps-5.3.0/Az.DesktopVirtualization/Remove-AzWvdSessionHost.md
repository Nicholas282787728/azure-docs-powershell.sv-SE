---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdsessionhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdSessionHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdSessionHost.md
ms.openlocfilehash: fa480a867cbbe93a756ea38b4534818ca119c098
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523711"
---
# <span data-ttu-id="9dbf8-101">Remove-AzWvdSessionHost</span><span class="sxs-lookup"><span data-stu-id="9dbf8-101">Remove-AzWvdSessionHost</span></span>

## <span data-ttu-id="9dbf8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9dbf8-102">SYNOPSIS</span></span>
<span data-ttu-id="9dbf8-103">Ta bort en SessionHost.</span><span class="sxs-lookup"><span data-stu-id="9dbf8-103">Remove a SessionHost.</span></span>

## <span data-ttu-id="9dbf8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9dbf8-104">SYNTAX</span></span>

### <span data-ttu-id="9dbf8-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="9dbf8-105">Delete (Default)</span></span>
```
Remove-AzWvdSessionHost -HostPoolName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="9dbf8-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9dbf8-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdSessionHost -InputObject <IDesktopVirtualizationIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9dbf8-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9dbf8-107">DESCRIPTION</span></span>
<span data-ttu-id="9dbf8-108">Ta bort en SessionHost.</span><span class="sxs-lookup"><span data-stu-id="9dbf8-108">Remove a SessionHost.</span></span>

## <span data-ttu-id="9dbf8-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9dbf8-109">EXAMPLES</span></span>

### <span data-ttu-id="9dbf8-110">Exempel 1: ta bort en Windows Virtual Desktop SessionHost efter namn</span><span class="sxs-lookup"><span data-stu-id="9dbf8-110">Example 1: Delete a Windows Virtual Desktop SessionHost by name</span></span>
```powershell
PS C:\> Remove-AzWvdSessionHost -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -Name SessionHostName
```

<span data-ttu-id="9dbf8-111">Det här kommandot tar bort en Windows Virtual Desktop-SessionHost i en adresspool.</span><span class="sxs-lookup"><span data-stu-id="9dbf8-111">This command deletes a Windows Virtual Desktop SessionHost in a Host Pool.</span></span>

## <span data-ttu-id="9dbf8-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9dbf8-112">PARAMETERS</span></span>

### <span data-ttu-id="9dbf8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dbf8-113">-DefaultProfile</span></span>
<span data-ttu-id="9dbf8-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9dbf8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9dbf8-115">-Force</span><span class="sxs-lookup"><span data-stu-id="9dbf8-115">-Force</span></span>
<span data-ttu-id="9dbf8-116">Tvinga flaggan att tvinga sessionHost borttagning även när userSession finns.</span><span class="sxs-lookup"><span data-stu-id="9dbf8-116">Force flag to force sessionHost deletion even when userSession exists.</span></span>

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

### <span data-ttu-id="9dbf8-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="9dbf8-117">-HostPoolName</span></span>
<span data-ttu-id="9dbf8-118">Namnet på den värdbaserade adresspoolen i den angivna resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="9dbf8-118">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="9dbf8-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9dbf8-119">-InputObject</span></span>
<span data-ttu-id="9dbf8-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="9dbf8-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9dbf8-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="9dbf8-121">-Name</span></span>
<span data-ttu-id="9dbf8-122">Namnet på sessions värden i den angivna poolen</span><span class="sxs-lookup"><span data-stu-id="9dbf8-122">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: SessionHostName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dbf8-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9dbf8-123">-PassThru</span></span>
<span data-ttu-id="9dbf8-124">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="9dbf8-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="9dbf8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9dbf8-125">-ResourceGroupName</span></span>
<span data-ttu-id="9dbf8-126">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="9dbf8-126">The name of the resource group.</span></span>
<span data-ttu-id="9dbf8-127">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="9dbf8-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="9dbf8-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9dbf8-128">-SubscriptionId</span></span>
<span data-ttu-id="9dbf8-129">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="9dbf8-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="9dbf8-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9dbf8-130">-Confirm</span></span>
<span data-ttu-id="9dbf8-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9dbf8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9dbf8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9dbf8-132">-WhatIf</span></span>
<span data-ttu-id="9dbf8-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9dbf8-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9dbf8-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9dbf8-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9dbf8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dbf8-135">CommonParameters</span></span>
<span data-ttu-id="9dbf8-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9dbf8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dbf8-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9dbf8-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dbf8-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9dbf8-138">INPUTS</span></span>

### <span data-ttu-id="9dbf8-139">Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="9dbf8-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="9dbf8-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9dbf8-140">OUTPUTS</span></span>

### <span data-ttu-id="9dbf8-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9dbf8-141">System.Boolean</span></span>

## <span data-ttu-id="9dbf8-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9dbf8-142">NOTES</span></span>

<span data-ttu-id="9dbf8-143">ALIAS</span><span class="sxs-lookup"><span data-stu-id="9dbf8-143">ALIASES</span></span>

<span data-ttu-id="9dbf8-144">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="9dbf8-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9dbf8-145">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="9dbf8-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9dbf8-146">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9dbf8-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9dbf8-147">INPUTOBJECT <IDesktopVirtualizationIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="9dbf8-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9dbf8-148">`[ApplicationGroupName <String>]`: Namnet på program gruppen</span><span class="sxs-lookup"><span data-stu-id="9dbf8-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="9dbf8-149">`[ApplicationName <String>]`: Namnet på programmet i den angivna program gruppen</span><span class="sxs-lookup"><span data-stu-id="9dbf8-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="9dbf8-150">`[DesktopName <String>]`: Namnet på Skriv bordet i angiven Skriv bords grupp</span><span class="sxs-lookup"><span data-stu-id="9dbf8-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="9dbf8-151">`[HostPoolName <String>]`: Namnet på den värdbaserade poolen i den angivna resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="9dbf8-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="9dbf8-152">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="9dbf8-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9dbf8-153">`[MsixPackageFullName <String>]`: Det versions specifika paketet fullständigt namn för MSIX paketet i angivet hostpool</span><span class="sxs-lookup"><span data-stu-id="9dbf8-153">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="9dbf8-154">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="9dbf8-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="9dbf8-155">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="9dbf8-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="9dbf8-156">`[SessionHostName <String>]`: Namnet på sessions värden i den angivna poolen</span><span class="sxs-lookup"><span data-stu-id="9dbf8-156">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="9dbf8-157">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="9dbf8-157">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="9dbf8-158">`[UserSessionId <String>]`: Namnet på användarsessionen inom den angivna värd</span><span class="sxs-lookup"><span data-stu-id="9dbf8-158">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="9dbf8-159">`[WorkspaceName <String>]`: Arbets ytans namn</span><span class="sxs-lookup"><span data-stu-id="9dbf8-159">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="9dbf8-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9dbf8-160">RELATED LINKS</span></span>

