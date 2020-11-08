---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvddesktop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdDesktop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdDesktop.md
ms.openlocfilehash: 7aec3e71e65c20810d8a17e8f7fa14df3c69f577
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102887"
---
# <span data-ttu-id="1479a-101">Update-AzWvdDesktop</span><span class="sxs-lookup"><span data-stu-id="1479a-101">Update-AzWvdDesktop</span></span>

## <span data-ttu-id="1479a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1479a-102">SYNOPSIS</span></span>
<span data-ttu-id="1479a-103">Uppdatera ett skriv bord.</span><span class="sxs-lookup"><span data-stu-id="1479a-103">Update a desktop.</span></span>

## <span data-ttu-id="1479a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1479a-104">SYNTAX</span></span>

### <span data-ttu-id="1479a-105">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="1479a-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdDesktop -ApplicationGroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1479a-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="1479a-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdDesktop -InputObject <IDesktopVirtualizationIdentity> [-Description <String>]
 [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="1479a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1479a-107">DESCRIPTION</span></span>
<span data-ttu-id="1479a-108">Uppdatera ett skriv bord.</span><span class="sxs-lookup"><span data-stu-id="1479a-108">Update a desktop.</span></span>

## <span data-ttu-id="1479a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1479a-109">EXAMPLES</span></span>

### <span data-ttu-id="1479a-110">Exempel 1: uppdatera ett virtuellt skriv bord i Windows</span><span class="sxs-lookup"><span data-stu-id="1479a-110">Example 1: Update a Windows Virtual Desktop Desktop</span></span>
```powershell
PS C:\> Update-AzWvdDesktop -ResourceGroupName ResourceGroupName `
                             -GroupName ApplicationGroupName `
                             -Name DesktopName `
                             -FriendlyName 'Friendly name' `
                             -Description 'Description' `

Name                             Type
----                             ----
ApplicationGroupName/DesktopName Microsoft.DesktopVirtualization/applicationgroups/desktops
```

<span data-ttu-id="1479a-111">Det här kommandot uppdaterar ett virtuellt skriv bord i Windows i en applicaton-grupp.</span><span class="sxs-lookup"><span data-stu-id="1479a-111">This command updates a Windows Virtual Desktop Desktop in an applicaton Group.</span></span>

## <span data-ttu-id="1479a-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1479a-112">PARAMETERS</span></span>

### <span data-ttu-id="1479a-113">-ApplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="1479a-113">-ApplicationGroupName</span></span>
<span data-ttu-id="1479a-114">Namnet på program gruppen</span><span class="sxs-lookup"><span data-stu-id="1479a-114">The name of the application group</span></span>

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

### <span data-ttu-id="1479a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1479a-115">-DefaultProfile</span></span>
<span data-ttu-id="1479a-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1479a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1479a-117">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="1479a-117">-Description</span></span>
<span data-ttu-id="1479a-118">Beskrivning av skriv bord.</span><span class="sxs-lookup"><span data-stu-id="1479a-118">Description of Desktop.</span></span>

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

### <span data-ttu-id="1479a-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="1479a-119">-FriendlyName</span></span>
<span data-ttu-id="1479a-120">Eget namn på Skriv bordet.</span><span class="sxs-lookup"><span data-stu-id="1479a-120">Friendly name of Desktop.</span></span>

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

### <span data-ttu-id="1479a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1479a-121">-InputObject</span></span>
<span data-ttu-id="1479a-122">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="1479a-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1479a-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="1479a-123">-Name</span></span>
<span data-ttu-id="1479a-124">Namnet på Skriv bordet i angiven Skriv bords grupp</span><span class="sxs-lookup"><span data-stu-id="1479a-124">The name of the desktop within the specified desktop group</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: DesktopName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1479a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1479a-125">-ResourceGroupName</span></span>
<span data-ttu-id="1479a-126">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="1479a-126">The name of the resource group.</span></span>
<span data-ttu-id="1479a-127">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="1479a-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="1479a-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1479a-128">-SubscriptionId</span></span>
<span data-ttu-id="1479a-129">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="1479a-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="1479a-130">-Tagg</span><span class="sxs-lookup"><span data-stu-id="1479a-130">-Tag</span></span>
<span data-ttu-id="1479a-131">Taggar som ska uppdateras</span><span class="sxs-lookup"><span data-stu-id="1479a-131">tags to be updated</span></span>

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

### <span data-ttu-id="1479a-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1479a-132">-Confirm</span></span>
<span data-ttu-id="1479a-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1479a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1479a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1479a-134">-WhatIf</span></span>
<span data-ttu-id="1479a-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1479a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1479a-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1479a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1479a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1479a-137">CommonParameters</span></span>
<span data-ttu-id="1479a-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1479a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1479a-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1479a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1479a-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1479a-140">INPUTS</span></span>

### <span data-ttu-id="1479a-141">Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="1479a-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="1479a-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1479a-142">OUTPUTS</span></span>

### <span data-ttu-id="1479a-143">Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. Api20191210Preview. IDesktop</span><span class="sxs-lookup"><span data-stu-id="1479a-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IDesktop</span></span>

## <span data-ttu-id="1479a-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1479a-144">NOTES</span></span>

<span data-ttu-id="1479a-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="1479a-145">ALIASES</span></span>

<span data-ttu-id="1479a-146">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="1479a-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1479a-147">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="1479a-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1479a-148">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1479a-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1479a-149">INPUTOBJECT <IDesktopVirtualizationIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="1479a-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1479a-150">`[ApplicationGroupName <String>]`: Namnet på program gruppen</span><span class="sxs-lookup"><span data-stu-id="1479a-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="1479a-151">`[ApplicationName <String>]`: Namnet på programmet i den angivna program gruppen</span><span class="sxs-lookup"><span data-stu-id="1479a-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="1479a-152">`[DesktopName <String>]`: Namnet på Skriv bordet i angiven Skriv bords grupp</span><span class="sxs-lookup"><span data-stu-id="1479a-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="1479a-153">`[HostPoolName <String>]`: Namnet på den värdbaserade poolen i den angivna resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="1479a-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="1479a-154">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="1479a-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1479a-155">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="1479a-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="1479a-156">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="1479a-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="1479a-157">`[SessionHostName <String>]`: Namnet på sessions värden i den angivna poolen</span><span class="sxs-lookup"><span data-stu-id="1479a-157">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="1479a-158">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="1479a-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="1479a-159">`[UserSessionId <String>]`: Namnet på användarsessionen inom den angivna värd</span><span class="sxs-lookup"><span data-stu-id="1479a-159">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="1479a-160">`[WorkspaceName <String>]`: Arbets ytans namn</span><span class="sxs-lookup"><span data-stu-id="1479a-160">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="1479a-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1479a-161">RELATED LINKS</span></span>

