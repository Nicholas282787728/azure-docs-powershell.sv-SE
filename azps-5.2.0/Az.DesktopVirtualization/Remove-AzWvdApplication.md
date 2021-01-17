---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdApplication.md
ms.openlocfilehash: c65fd55599a78bbaa558ba7ec8efa94fdc3b40e2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98396763"
---
# <span data-ttu-id="46d95-101">Remove-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="46d95-101">Remove-AzWvdApplication</span></span>

## <span data-ttu-id="46d95-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="46d95-102">SYNOPSIS</span></span>
<span data-ttu-id="46d95-103">Ta bort ett program.</span><span class="sxs-lookup"><span data-stu-id="46d95-103">Remove an application.</span></span>

## <span data-ttu-id="46d95-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="46d95-104">SYNTAX</span></span>

### <span data-ttu-id="46d95-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="46d95-105">Delete (Default)</span></span>
```
Remove-AzWvdApplication -GroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="46d95-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="46d95-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdApplication -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="46d95-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="46d95-107">DESCRIPTION</span></span>
<span data-ttu-id="46d95-108">Ta bort ett program.</span><span class="sxs-lookup"><span data-stu-id="46d95-108">Remove an application.</span></span>

## <span data-ttu-id="46d95-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="46d95-109">EXAMPLES</span></span>

### <span data-ttu-id="46d95-110">Exempel 1: ta bort ett virtuellt skriv bord i Windows med namn</span><span class="sxs-lookup"><span data-stu-id="46d95-110">Example 1: Delete a Windows Virtual Desktop Application by name</span></span>
```powershell
PS C:\> Remove-AzWvdApplication -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName -Name ApplicationName
```

<span data-ttu-id="46d95-111">Det här kommandot tar bort ett virtuellt Windows-program i en applicaton-grupp.</span><span class="sxs-lookup"><span data-stu-id="46d95-111">This command deletes a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="46d95-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="46d95-112">PARAMETERS</span></span>

### <span data-ttu-id="46d95-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46d95-113">-DefaultProfile</span></span>
<span data-ttu-id="46d95-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="46d95-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46d95-115">-Grupp namn</span><span class="sxs-lookup"><span data-stu-id="46d95-115">-GroupName</span></span>
<span data-ttu-id="46d95-116">Namnet på program gruppen</span><span class="sxs-lookup"><span data-stu-id="46d95-116">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46d95-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="46d95-117">-InputObject</span></span>
<span data-ttu-id="46d95-118">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="46d95-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="46d95-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="46d95-119">-Name</span></span>
<span data-ttu-id="46d95-120">Namnet på programmet i den angivna program gruppen</span><span class="sxs-lookup"><span data-stu-id="46d95-120">The name of the application within the specified application group</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ApplicationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46d95-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="46d95-121">-PassThru</span></span>
<span data-ttu-id="46d95-122">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="46d95-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="46d95-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46d95-123">-ResourceGroupName</span></span>
<span data-ttu-id="46d95-124">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="46d95-124">The name of the resource group.</span></span>
<span data-ttu-id="46d95-125">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="46d95-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="46d95-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="46d95-126">-SubscriptionId</span></span>
<span data-ttu-id="46d95-127">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="46d95-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="46d95-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="46d95-128">-Confirm</span></span>
<span data-ttu-id="46d95-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="46d95-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46d95-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46d95-130">-WhatIf</span></span>
<span data-ttu-id="46d95-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="46d95-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46d95-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="46d95-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46d95-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46d95-133">CommonParameters</span></span>
<span data-ttu-id="46d95-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46d95-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46d95-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="46d95-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46d95-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="46d95-136">INPUTS</span></span>

### <span data-ttu-id="46d95-137">Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="46d95-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="46d95-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="46d95-138">OUTPUTS</span></span>

### <span data-ttu-id="46d95-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="46d95-139">System.Boolean</span></span>

## <span data-ttu-id="46d95-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="46d95-140">NOTES</span></span>

<span data-ttu-id="46d95-141">ALIAS</span><span class="sxs-lookup"><span data-stu-id="46d95-141">ALIASES</span></span>

<span data-ttu-id="46d95-142">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="46d95-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="46d95-143">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="46d95-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="46d95-144">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="46d95-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="46d95-145">INPUTOBJECT <IDesktopVirtualizationIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="46d95-145">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="46d95-146">`[ApplicationGroupName <String>]`: Namnet på program gruppen</span><span class="sxs-lookup"><span data-stu-id="46d95-146">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="46d95-147">`[ApplicationName <String>]`: Namnet på programmet i den angivna program gruppen</span><span class="sxs-lookup"><span data-stu-id="46d95-147">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="46d95-148">`[DesktopName <String>]`: Namnet på Skriv bordet i angiven Skriv bords grupp</span><span class="sxs-lookup"><span data-stu-id="46d95-148">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="46d95-149">`[HostPoolName <String>]`: Namnet på den värdbaserade poolen i den angivna resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="46d95-149">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="46d95-150">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="46d95-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="46d95-151">`[MsixPackageFullName <String>]`: Det versions specifika paketet fullständigt namn för MSIX paketet i angivet hostpool</span><span class="sxs-lookup"><span data-stu-id="46d95-151">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="46d95-152">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="46d95-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="46d95-153">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="46d95-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="46d95-154">`[SessionHostName <String>]`: Namnet på sessions värden i den angivna poolen</span><span class="sxs-lookup"><span data-stu-id="46d95-154">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="46d95-155">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="46d95-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="46d95-156">`[UserSessionId <String>]`: Namnet på användarsessionen inom den angivna värd</span><span class="sxs-lookup"><span data-stu-id="46d95-156">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="46d95-157">`[WorkspaceName <String>]`: Arbets ytans namn</span><span class="sxs-lookup"><span data-stu-id="46d95-157">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="46d95-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="46d95-158">RELATED LINKS</span></span>

