---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplication.md
ms.openlocfilehash: 6907967acfd86f151b038e26aa9c33f62db50a5a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98396728"
---
# <span data-ttu-id="c7708-101">Update-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="c7708-101">Update-AzWvdApplication</span></span>

## <span data-ttu-id="c7708-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c7708-102">SYNOPSIS</span></span>
<span data-ttu-id="c7708-103">Uppdatera ett program.</span><span class="sxs-lookup"><span data-stu-id="c7708-103">Update an application.</span></span>

## <span data-ttu-id="c7708-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c7708-104">SYNTAX</span></span>

### <span data-ttu-id="c7708-105">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="c7708-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdApplication -GroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ApplicationType <RemoteApplicationType>] [-CommandLineArgument <String>]
 [-CommandLineSetting <CommandLineSetting>] [-Description <String>] [-FilePath <String>]
 [-FriendlyName <String>] [-IconIndex <Int32>] [-IconPath <String>] [-MsixPackageApplicationId <String>]
 [-MsixPackageFamilyName <String>] [-ShowInPortal] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c7708-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="c7708-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdApplication -InputObject <IDesktopVirtualizationIdentity>
 [-ApplicationType <RemoteApplicationType>] [-CommandLineArgument <String>]
 [-CommandLineSetting <CommandLineSetting>] [-Description <String>] [-FilePath <String>]
 [-FriendlyName <String>] [-IconIndex <Int32>] [-IconPath <String>] [-MsixPackageApplicationId <String>]
 [-MsixPackageFamilyName <String>] [-ShowInPortal] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c7708-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c7708-107">DESCRIPTION</span></span>
<span data-ttu-id="c7708-108">Uppdatera ett program.</span><span class="sxs-lookup"><span data-stu-id="c7708-108">Update an application.</span></span>

## <span data-ttu-id="c7708-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c7708-109">EXAMPLES</span></span>

### <span data-ttu-id="c7708-110">Exempel 1: uppdatera ett virtuellt Windows-program</span><span class="sxs-lookup"><span data-stu-id="c7708-110">Example 1: Update a Windows Virtual Desktop Application</span></span>
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

<span data-ttu-id="c7708-111">Det här kommandot uppdaterar ett virtuellt Windows-program i en applicaton-grupp.</span><span class="sxs-lookup"><span data-stu-id="c7708-111">This command updates a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="c7708-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c7708-112">PARAMETERS</span></span>

### <span data-ttu-id="c7708-113">-ApplicationType</span><span class="sxs-lookup"><span data-stu-id="c7708-113">-ApplicationType</span></span>
<span data-ttu-id="c7708-114">Resurs typ för program.</span><span class="sxs-lookup"><span data-stu-id="c7708-114">Resource Type of Application.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.RemoteApplicationType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7708-115">-CommandLineArgument</span><span class="sxs-lookup"><span data-stu-id="c7708-115">-CommandLineArgument</span></span>
<span data-ttu-id="c7708-116">Kommando rads argument för programmet.</span><span class="sxs-lookup"><span data-stu-id="c7708-116">Command Line Arguments for Application.</span></span>

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

### <span data-ttu-id="c7708-117">-CommandLineSetting</span><span class="sxs-lookup"><span data-stu-id="c7708-117">-CommandLineSetting</span></span>
<span data-ttu-id="c7708-118">Anger om det här publicerade programmet kan startas med kommando rads argument som tillhandahålls av klienten, kommando rads argument som angetts vid publicerings tillfället eller inga kommando rads argument alls.</span><span class="sxs-lookup"><span data-stu-id="c7708-118">Specifies whether this published application can be launched with command line arguments provided by the client, command line arguments specified at publish time, or no command line arguments at all.</span></span>

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

### <span data-ttu-id="c7708-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7708-119">-DefaultProfile</span></span>
<span data-ttu-id="c7708-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c7708-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7708-121">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="c7708-121">-Description</span></span>
<span data-ttu-id="c7708-122">Beskrivning av program.</span><span class="sxs-lookup"><span data-stu-id="c7708-122">Description of Application.</span></span>

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

### <span data-ttu-id="c7708-123">-Sökväg</span><span class="sxs-lookup"><span data-stu-id="c7708-123">-FilePath</span></span>
<span data-ttu-id="c7708-124">Anger en sökväg till den körbara filen för programmet.</span><span class="sxs-lookup"><span data-stu-id="c7708-124">Specifies a path for the executable file for the application.</span></span>

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

### <span data-ttu-id="c7708-125">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="c7708-125">-FriendlyName</span></span>
<span data-ttu-id="c7708-126">Eget namn på programmet.</span><span class="sxs-lookup"><span data-stu-id="c7708-126">Friendly name of Application.</span></span>

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

### <span data-ttu-id="c7708-127">-Grupp namn</span><span class="sxs-lookup"><span data-stu-id="c7708-127">-GroupName</span></span>
<span data-ttu-id="c7708-128">Namnet på program gruppen</span><span class="sxs-lookup"><span data-stu-id="c7708-128">The name of the application group</span></span>

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

### <span data-ttu-id="c7708-129">-IconIndex</span><span class="sxs-lookup"><span data-stu-id="c7708-129">-IconIndex</span></span>
<span data-ttu-id="c7708-130">Index för ikonen.</span><span class="sxs-lookup"><span data-stu-id="c7708-130">Index of the icon.</span></span>

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

### <span data-ttu-id="c7708-131">-IconPath</span><span class="sxs-lookup"><span data-stu-id="c7708-131">-IconPath</span></span>
<span data-ttu-id="c7708-132">Ikonen Path.</span><span class="sxs-lookup"><span data-stu-id="c7708-132">Path to icon.</span></span>

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

### <span data-ttu-id="c7708-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c7708-133">-InputObject</span></span>
<span data-ttu-id="c7708-134">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="c7708-134">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c7708-135">-MsixPackageApplicationId</span><span class="sxs-lookup"><span data-stu-id="c7708-135">-MsixPackageApplicationId</span></span>
<span data-ttu-id="c7708-136">Anger paket programmets ID för MSIX-program</span><span class="sxs-lookup"><span data-stu-id="c7708-136">Specifies the package application Id for MSIX applications</span></span>

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

### <span data-ttu-id="c7708-137">-MsixPackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="c7708-137">-MsixPackageFamilyName</span></span>
<span data-ttu-id="c7708-138">Anger namnet på paket familjen för MSIX-program</span><span class="sxs-lookup"><span data-stu-id="c7708-138">Specifies the package family name for MSIX applications</span></span>

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

### <span data-ttu-id="c7708-139">-Namn</span><span class="sxs-lookup"><span data-stu-id="c7708-139">-Name</span></span>
<span data-ttu-id="c7708-140">Namnet på programmet i den angivna program gruppen</span><span class="sxs-lookup"><span data-stu-id="c7708-140">The name of the application within the specified application group</span></span>

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

### <span data-ttu-id="c7708-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7708-141">-ResourceGroupName</span></span>
<span data-ttu-id="c7708-142">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="c7708-142">The name of the resource group.</span></span>
<span data-ttu-id="c7708-143">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="c7708-143">The name is case insensitive.</span></span>

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

### <span data-ttu-id="c7708-144">-ShowInPortal</span><span class="sxs-lookup"><span data-stu-id="c7708-144">-ShowInPortal</span></span>
<span data-ttu-id="c7708-145">Anger om RemoteApp-programmet ska visas i servern för webb åtkomst för fjärr skrivbord.</span><span class="sxs-lookup"><span data-stu-id="c7708-145">Specifies whether to show the RemoteApp program in the RD Web Access server.</span></span>

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

### <span data-ttu-id="c7708-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c7708-146">-SubscriptionId</span></span>
<span data-ttu-id="c7708-147">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="c7708-147">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="c7708-148">-Tagg</span><span class="sxs-lookup"><span data-stu-id="c7708-148">-Tag</span></span>
<span data-ttu-id="c7708-149">Taggar som ska uppdateras</span><span class="sxs-lookup"><span data-stu-id="c7708-149">tags to be updated</span></span>

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

### <span data-ttu-id="c7708-150">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c7708-150">-Confirm</span></span>
<span data-ttu-id="c7708-151">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c7708-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7708-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7708-152">-WhatIf</span></span>
<span data-ttu-id="c7708-153">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c7708-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7708-154">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c7708-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7708-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7708-155">CommonParameters</span></span>
<span data-ttu-id="c7708-156">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7708-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7708-157">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c7708-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7708-158">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c7708-158">INPUTS</span></span>

### <span data-ttu-id="c7708-159">Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="c7708-159">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="c7708-160">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c7708-160">OUTPUTS</span></span>

### <span data-ttu-id="c7708-161">Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. Api20201019Preview. IApplication</span><span class="sxs-lookup"><span data-stu-id="c7708-161">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IApplication</span></span>

## <span data-ttu-id="c7708-162">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c7708-162">NOTES</span></span>

<span data-ttu-id="c7708-163">ALIAS</span><span class="sxs-lookup"><span data-stu-id="c7708-163">ALIASES</span></span>

<span data-ttu-id="c7708-164">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="c7708-164">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c7708-165">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="c7708-165">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c7708-166">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c7708-166">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c7708-167">INPUTOBJECT <IDesktopVirtualizationIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="c7708-167">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c7708-168">`[ApplicationGroupName <String>]`: Namnet på program gruppen</span><span class="sxs-lookup"><span data-stu-id="c7708-168">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="c7708-169">`[ApplicationName <String>]`: Namnet på programmet i den angivna program gruppen</span><span class="sxs-lookup"><span data-stu-id="c7708-169">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="c7708-170">`[DesktopName <String>]`: Namnet på Skriv bordet i angiven Skriv bords grupp</span><span class="sxs-lookup"><span data-stu-id="c7708-170">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="c7708-171">`[HostPoolName <String>]`: Namnet på den värdbaserade poolen i den angivna resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="c7708-171">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="c7708-172">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="c7708-172">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c7708-173">`[MsixPackageFullName <String>]`: Det versions specifika paketet fullständigt namn för MSIX paketet i angivet hostpool</span><span class="sxs-lookup"><span data-stu-id="c7708-173">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="c7708-174">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="c7708-174">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="c7708-175">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="c7708-175">The name is case insensitive.</span></span>
  - <span data-ttu-id="c7708-176">`[SessionHostName <String>]`: Namnet på sessions värden i den angivna poolen</span><span class="sxs-lookup"><span data-stu-id="c7708-176">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="c7708-177">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="c7708-177">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="c7708-178">`[UserSessionId <String>]`: Namnet på användarsessionen inom den angivna värd</span><span class="sxs-lookup"><span data-stu-id="c7708-178">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="c7708-179">`[WorkspaceName <String>]`: Arbets ytans namn</span><span class="sxs-lookup"><span data-stu-id="c7708-179">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="c7708-180">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c7708-180">RELATED LINKS</span></span>

