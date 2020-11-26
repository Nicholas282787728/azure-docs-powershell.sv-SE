---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplicationGroup.md
ms.openlocfilehash: ab1f338be9d983efceac0045fec96b1a63fb66bf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102889"
---
# <span data-ttu-id="0491e-101">Update-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="0491e-101">Update-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="0491e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0491e-102">SYNOPSIS</span></span>
<span data-ttu-id="0491e-103">Uppdatera en applicationGroup.</span><span class="sxs-lookup"><span data-stu-id="0491e-103">Update an applicationGroup.</span></span>

## <span data-ttu-id="0491e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0491e-104">SYNTAX</span></span>

### <span data-ttu-id="0491e-105">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="0491e-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0491e-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="0491e-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdApplicationGroup -InputObject <IDesktopVirtualizationIdentity> [-Description <String>]
 [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="0491e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0491e-107">DESCRIPTION</span></span>
<span data-ttu-id="0491e-108">Uppdatera en applicationGroup.</span><span class="sxs-lookup"><span data-stu-id="0491e-108">Update an applicationGroup.</span></span>

## <span data-ttu-id="0491e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0491e-109">EXAMPLES</span></span>

### <span data-ttu-id="0491e-110">Exempel 1: skapa ett virtuellt skriv bord i Windows med ett ApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="0491e-110">Example 1: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> New-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                            -Name ApplicationGroupName `
                            -FriendlyName 'Friendly Name' `
                            -Description 'Description' `

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="0491e-111">Det här kommandot skapar en Windows Virtual Desktop-ApplicationGroup i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="0491e-111">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

## <span data-ttu-id="0491e-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0491e-112">PARAMETERS</span></span>

### <span data-ttu-id="0491e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0491e-113">-DefaultProfile</span></span>
<span data-ttu-id="0491e-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0491e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0491e-115">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="0491e-115">-Description</span></span>
<span data-ttu-id="0491e-116">Beskrivning av ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="0491e-116">Description of ApplicationGroup.</span></span>

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

### <span data-ttu-id="0491e-117">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="0491e-117">-FriendlyName</span></span>
<span data-ttu-id="0491e-118">Eget namn på ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="0491e-118">Friendly name of ApplicationGroup.</span></span>

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

### <span data-ttu-id="0491e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0491e-119">-InputObject</span></span>
<span data-ttu-id="0491e-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="0491e-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0491e-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="0491e-121">-Name</span></span>
<span data-ttu-id="0491e-122">Namnet på program gruppen</span><span class="sxs-lookup"><span data-stu-id="0491e-122">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0491e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0491e-123">-ResourceGroupName</span></span>
<span data-ttu-id="0491e-124">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="0491e-124">The name of the resource group.</span></span>
<span data-ttu-id="0491e-125">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="0491e-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="0491e-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0491e-126">-SubscriptionId</span></span>
<span data-ttu-id="0491e-127">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="0491e-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="0491e-128">-Tagg</span><span class="sxs-lookup"><span data-stu-id="0491e-128">-Tag</span></span>
<span data-ttu-id="0491e-129">Taggar som ska uppdateras</span><span class="sxs-lookup"><span data-stu-id="0491e-129">tags to be updated</span></span>

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

### <span data-ttu-id="0491e-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0491e-130">-Confirm</span></span>
<span data-ttu-id="0491e-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0491e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0491e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0491e-132">-WhatIf</span></span>
<span data-ttu-id="0491e-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0491e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0491e-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0491e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0491e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0491e-135">CommonParameters</span></span>
<span data-ttu-id="0491e-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0491e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0491e-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0491e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0491e-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0491e-138">INPUTS</span></span>

### <span data-ttu-id="0491e-139">Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="0491e-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="0491e-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0491e-140">OUTPUTS</span></span>

### <span data-ttu-id="0491e-141">Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. Api20191210Preview. IApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="0491e-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IApplicationGroup</span></span>

## <span data-ttu-id="0491e-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0491e-142">NOTES</span></span>

<span data-ttu-id="0491e-143">ALIAS</span><span class="sxs-lookup"><span data-stu-id="0491e-143">ALIASES</span></span>

<span data-ttu-id="0491e-144">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="0491e-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0491e-145">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="0491e-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0491e-146">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0491e-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0491e-147">INPUTOBJECT <IDesktopVirtualizationIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="0491e-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0491e-148">`[ApplicationGroupName <String>]`: Namnet på program gruppen</span><span class="sxs-lookup"><span data-stu-id="0491e-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="0491e-149">`[ApplicationName <String>]`: Namnet på programmet i den angivna program gruppen</span><span class="sxs-lookup"><span data-stu-id="0491e-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="0491e-150">`[DesktopName <String>]`: Namnet på Skriv bordet i angiven Skriv bords grupp</span><span class="sxs-lookup"><span data-stu-id="0491e-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="0491e-151">`[HostPoolName <String>]`: Namnet på den värdbaserade poolen i den angivna resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="0491e-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="0491e-152">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="0491e-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0491e-153">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="0491e-153">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="0491e-154">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="0491e-154">The name is case insensitive.</span></span>
  - <span data-ttu-id="0491e-155">`[SessionHostName <String>]`: Namnet på sessions värden i den angivna poolen</span><span class="sxs-lookup"><span data-stu-id="0491e-155">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="0491e-156">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="0491e-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="0491e-157">`[UserSessionId <String>]`: Namnet på användarsessionen inom den angivna värd</span><span class="sxs-lookup"><span data-stu-id="0491e-157">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="0491e-158">`[WorkspaceName <String>]`: Arbets ytans namn</span><span class="sxs-lookup"><span data-stu-id="0491e-158">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="0491e-159">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0491e-159">RELATED LINKS</span></span>
