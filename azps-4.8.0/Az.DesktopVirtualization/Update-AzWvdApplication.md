---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplication.md
ms.openlocfilehash: 8c2026e7ef8ed5c0eeb1e5a4cb7f605c1a030b9e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102893"
---
# <span data-ttu-id="f2bef-101">Update-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="f2bef-101">Update-AzWvdApplication</span></span>

## <span data-ttu-id="f2bef-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f2bef-102">SYNOPSIS</span></span>
<span data-ttu-id="f2bef-103">Uppdatera ett program.</span><span class="sxs-lookup"><span data-stu-id="f2bef-103">Update an application.</span></span>

## <span data-ttu-id="f2bef-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f2bef-104">SYNTAX</span></span>

### <span data-ttu-id="f2bef-105">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="f2bef-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdApplication -GroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-CommandLineArgument <String>] [-CommandLineSetting <CommandLineSetting>]
 [-Description <String>] [-FilePath <String>] [-FriendlyName <String>] [-IconIndex <Int32>]
 [-IconPath <String>] [-ShowInPortal] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="f2bef-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="f2bef-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdApplication -InputObject <IDesktopVirtualizationIdentity> [-CommandLineArgument <String>]
 [-CommandLineSetting <CommandLineSetting>] [-Description <String>] [-FilePath <String>]
 [-FriendlyName <String>] [-IconIndex <Int32>] [-IconPath <String>] [-ShowInPortal] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f2bef-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f2bef-107">DESCRIPTION</span></span>
<span data-ttu-id="f2bef-108">Uppdatera ett program.</span><span class="sxs-lookup"><span data-stu-id="f2bef-108">Update an application.</span></span>

## <span data-ttu-id="f2bef-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f2bef-109">EXAMPLES</span></span>

### <span data-ttu-id="f2bef-110">Exempel 1: uppdatera ett virtuellt Windows-program</span><span class="sxs-lookup"><span data-stu-id="f2bef-110">Example 1: Update a Windows Virtual Desktop Application</span></span>
```powershell
PS C:\> Update-AzWvdApplication -ResourceGroupName ResourceGroupName `
                             -GroupName ApplicationGroupName `
                             -Name ApplicationName `
                             -FilePath 'C:\windows\system32\mspaint.exe' `
                             -FriendlyName 'Friendly name' `
                             -Description 'Description' `
                             -IconIndex 0 `
                             -IconPath 'C:\windows\system32\mspaint.exe' `
                             -CommandLineSetting 'Allow' `
                             -ShowInPortal:$true

Name                                 Type
----                                 ----
ApplicationGroupName/ApplicationName Microsoft.DesktopVirtualization/applicationgroups/applications
```

<span data-ttu-id="f2bef-111">Det här kommandot uppdaterar ett virtuellt Windows-program i en applicaton-grupp.</span><span class="sxs-lookup"><span data-stu-id="f2bef-111">This command updates a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="f2bef-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f2bef-112">PARAMETERS</span></span>

### <span data-ttu-id="f2bef-113">-CommandLineArgument</span><span class="sxs-lookup"><span data-stu-id="f2bef-113">-CommandLineArgument</span></span>
<span data-ttu-id="f2bef-114">Kommando rads argument för programmet.</span><span class="sxs-lookup"><span data-stu-id="f2bef-114">Command Line Arguments for Application.</span></span>

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

### <span data-ttu-id="f2bef-115">-CommandLineSetting</span><span class="sxs-lookup"><span data-stu-id="f2bef-115">-CommandLineSetting</span></span>
<span data-ttu-id="f2bef-116">Anger om det här publicerade programmet kan startas med kommando rads argument som tillhandahålls av klienten, kommando rads argument som angetts vid publicerings tillfället eller inga kommando rads argument alls.</span><span class="sxs-lookup"><span data-stu-id="f2bef-116">Specifies whether this published application can be launched with command line arguments provided by the client, command line arguments specified at publish time, or no command line arguments at all.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.CommandLineSetting
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2bef-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2bef-117">-DefaultProfile</span></span>
<span data-ttu-id="f2bef-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f2bef-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2bef-119">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="f2bef-119">-Description</span></span>
<span data-ttu-id="f2bef-120">Beskrivning av program.</span><span class="sxs-lookup"><span data-stu-id="f2bef-120">Description of Application.</span></span>

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

### <span data-ttu-id="f2bef-121">-Sökväg</span><span class="sxs-lookup"><span data-stu-id="f2bef-121">-FilePath</span></span>
<span data-ttu-id="f2bef-122">Anger en sökväg till den körbara filen för programmet.</span><span class="sxs-lookup"><span data-stu-id="f2bef-122">Specifies a path for the executable file for the application.</span></span>

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

### <span data-ttu-id="f2bef-123">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="f2bef-123">-FriendlyName</span></span>
<span data-ttu-id="f2bef-124">Eget namn på programmet.</span><span class="sxs-lookup"><span data-stu-id="f2bef-124">Friendly name of Application.</span></span>

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

### <span data-ttu-id="f2bef-125">-Grupp namn</span><span class="sxs-lookup"><span data-stu-id="f2bef-125">-GroupName</span></span>
<span data-ttu-id="f2bef-126">Namnet på program gruppen</span><span class="sxs-lookup"><span data-stu-id="f2bef-126">The name of the application group</span></span>

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

### <span data-ttu-id="f2bef-127">-IconIndex</span><span class="sxs-lookup"><span data-stu-id="f2bef-127">-IconIndex</span></span>
<span data-ttu-id="f2bef-128">Index för ikonen.</span><span class="sxs-lookup"><span data-stu-id="f2bef-128">Index of the icon.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2bef-129">-IconPath</span><span class="sxs-lookup"><span data-stu-id="f2bef-129">-IconPath</span></span>
<span data-ttu-id="f2bef-130">Ikonen Path.</span><span class="sxs-lookup"><span data-stu-id="f2bef-130">Path to icon.</span></span>

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

### <span data-ttu-id="f2bef-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f2bef-131">-InputObject</span></span>
<span data-ttu-id="f2bef-132">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="f2bef-132">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f2bef-133">-Namn</span><span class="sxs-lookup"><span data-stu-id="f2bef-133">-Name</span></span>
<span data-ttu-id="f2bef-134">Namnet på programmet i den angivna program gruppen</span><span class="sxs-lookup"><span data-stu-id="f2bef-134">The name of the application within the specified application group</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ApplicationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2bef-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2bef-135">-ResourceGroupName</span></span>
<span data-ttu-id="f2bef-136">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f2bef-136">The name of the resource group.</span></span>
<span data-ttu-id="f2bef-137">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="f2bef-137">The name is case insensitive.</span></span>

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

### <span data-ttu-id="f2bef-138">-ShowInPortal</span><span class="sxs-lookup"><span data-stu-id="f2bef-138">-ShowInPortal</span></span>
<span data-ttu-id="f2bef-139">Anger om RemoteApp-programmet ska visas i servern för webb åtkomst för fjärr skrivbord.</span><span class="sxs-lookup"><span data-stu-id="f2bef-139">Specifies whether to show the RemoteApp program in the RD Web Access server.</span></span>

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

### <span data-ttu-id="f2bef-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f2bef-140">-SubscriptionId</span></span>
<span data-ttu-id="f2bef-141">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="f2bef-141">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="f2bef-142">-Tagg</span><span class="sxs-lookup"><span data-stu-id="f2bef-142">-Tag</span></span>
<span data-ttu-id="f2bef-143">Taggar som ska uppdateras</span><span class="sxs-lookup"><span data-stu-id="f2bef-143">tags to be updated</span></span>

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

### <span data-ttu-id="f2bef-144">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f2bef-144">-Confirm</span></span>
<span data-ttu-id="f2bef-145">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f2bef-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2bef-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2bef-146">-WhatIf</span></span>
<span data-ttu-id="f2bef-147">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f2bef-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2bef-148">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f2bef-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2bef-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2bef-149">CommonParameters</span></span>
<span data-ttu-id="f2bef-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2bef-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2bef-151">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f2bef-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2bef-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f2bef-152">INPUTS</span></span>

### <span data-ttu-id="f2bef-153">Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="f2bef-153">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="f2bef-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f2bef-154">OUTPUTS</span></span>

### <span data-ttu-id="f2bef-155">Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. Api20191210Preview. IApplication</span><span class="sxs-lookup"><span data-stu-id="f2bef-155">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IApplication</span></span>

## <span data-ttu-id="f2bef-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f2bef-156">NOTES</span></span>

<span data-ttu-id="f2bef-157">ALIAS</span><span class="sxs-lookup"><span data-stu-id="f2bef-157">ALIASES</span></span>

<span data-ttu-id="f2bef-158">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="f2bef-158">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f2bef-159">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="f2bef-159">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f2bef-160">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f2bef-160">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f2bef-161">INPUTOBJECT <IDesktopVirtualizationIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="f2bef-161">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f2bef-162">`[ApplicationGroupName <String>]`: Namnet på program gruppen</span><span class="sxs-lookup"><span data-stu-id="f2bef-162">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="f2bef-163">`[ApplicationName <String>]`: Namnet på programmet i den angivna program gruppen</span><span class="sxs-lookup"><span data-stu-id="f2bef-163">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="f2bef-164">`[DesktopName <String>]`: Namnet på Skriv bordet i angiven Skriv bords grupp</span><span class="sxs-lookup"><span data-stu-id="f2bef-164">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="f2bef-165">`[HostPoolName <String>]`: Namnet på den värdbaserade poolen i den angivna resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="f2bef-165">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="f2bef-166">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="f2bef-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f2bef-167">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f2bef-167">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="f2bef-168">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="f2bef-168">The name is case insensitive.</span></span>
  - <span data-ttu-id="f2bef-169">`[SessionHostName <String>]`: Namnet på sessions värden i den angivna poolen</span><span class="sxs-lookup"><span data-stu-id="f2bef-169">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="f2bef-170">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="f2bef-170">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="f2bef-171">`[UserSessionId <String>]`: Namnet på användarsessionen inom den angivna värd</span><span class="sxs-lookup"><span data-stu-id="f2bef-171">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="f2bef-172">`[WorkspaceName <String>]`: Arbets ytans namn</span><span class="sxs-lookup"><span data-stu-id="f2bef-172">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="f2bef-173">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f2bef-173">RELATED LINKS</span></span>

