---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdMsixPackage.md
ms.openlocfilehash: 8fe887f754c5a5a9f45d38d646a1edd03d1cc006
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426323"
---
# <span data-ttu-id="35e1c-101">Update-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="35e1c-101">Update-AzWvdMsixPackage</span></span>

## <span data-ttu-id="35e1c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="35e1c-102">SYNOPSIS</span></span>
<span data-ttu-id="35e1c-103">Uppdatera ett MSIX-paket.</span><span class="sxs-lookup"><span data-stu-id="35e1c-103">Update an  MSIX Package.</span></span>

## <span data-ttu-id="35e1c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="35e1c-104">SYNTAX</span></span>

### <span data-ttu-id="35e1c-105">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="35e1c-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DisplayName <String>] [-IsActive] [-IsRegularRegistration]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="35e1c-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="35e1c-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdMsixPackage -InputObject <IDesktopVirtualizationIdentity> [-DisplayName <String>] [-IsActive]
 [-IsRegularRegistration] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="35e1c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="35e1c-107">DESCRIPTION</span></span>
<span data-ttu-id="35e1c-108">Uppdatera ett MSIX-paket.</span><span class="sxs-lookup"><span data-stu-id="35e1c-108">Update an  MSIX Package.</span></span>

## <span data-ttu-id="35e1c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="35e1c-109">EXAMPLES</span></span>

### <span data-ttu-id="35e1c-110">Exempel 1: uppdatera ett MSIX-paket</span><span class="sxs-lookup"><span data-stu-id="35e1c-110">Example 1: Update a MSIX Package</span></span> 
```powershell
PS C:\> Update-AzWvdMsixPackage -HostPoolName HostPoolName `
                -ResourceGroupName ResourceGroupName `
                -SubscriptionId SubscriptionId `
                -displayName 'Updated-display-Name' `
                    -IsRegularRegistration:$False `
                -IsActive:$True

Name                                                  Type
----                                                  ----
HostPoolName/MSIXPackage_FullName1                    Microsoft.DesktopVirtualization/hostpools/msixpackages
```

<span data-ttu-id="35e1c-111">Det här kommandot uppdaterar ett MSIX-paket i ett HostPool.</span><span class="sxs-lookup"><span data-stu-id="35e1c-111">This command updates a MSIX Package in a HostPool.</span></span>

## <span data-ttu-id="35e1c-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="35e1c-112">PARAMETERS</span></span>

### <span data-ttu-id="35e1c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35e1c-113">-DefaultProfile</span></span>
<span data-ttu-id="35e1c-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="35e1c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35e1c-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="35e1c-115">-DisplayName</span></span>
<span data-ttu-id="35e1c-116">Visnings namn för MSIX-paketet.</span><span class="sxs-lookup"><span data-stu-id="35e1c-116">Display name for MSIX Package.</span></span>

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

### <span data-ttu-id="35e1c-117">-FullName</span><span class="sxs-lookup"><span data-stu-id="35e1c-117">-FullName</span></span>
<span data-ttu-id="35e1c-118">Det versions specifika paketet fullständigt namn för MSIX paketet i angivet hostpool</span><span class="sxs-lookup"><span data-stu-id="35e1c-118">The version specific package full name of the MSIX package within specified hostpool</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: MsixPackageFullName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35e1c-119">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="35e1c-119">-HostPoolName</span></span>
<span data-ttu-id="35e1c-120">Namnet på den värdbaserade adresspoolen i den angivna resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="35e1c-120">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="35e1c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35e1c-121">-InputObject</span></span>
<span data-ttu-id="35e1c-122">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="35e1c-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="35e1c-123">-IsActive</span><span class="sxs-lookup"><span data-stu-id="35e1c-123">-IsActive</span></span>
<span data-ttu-id="35e1c-124">Ange att en version av paketet ska aktive ras på hostpool.</span><span class="sxs-lookup"><span data-stu-id="35e1c-124">Set a version of the package to be active across hostpool.</span></span>

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

### <span data-ttu-id="35e1c-125">-IsRegularRegistration</span><span class="sxs-lookup"><span data-stu-id="35e1c-125">-IsRegularRegistration</span></span>
<span data-ttu-id="35e1c-126">Ange registrerings läge.</span><span class="sxs-lookup"><span data-stu-id="35e1c-126">Set Registration mode.</span></span>
<span data-ttu-id="35e1c-127">Vanligt eller försenat.</span><span class="sxs-lookup"><span data-stu-id="35e1c-127">Regular or Delayed.</span></span>

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

### <span data-ttu-id="35e1c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35e1c-128">-ResourceGroupName</span></span>
<span data-ttu-id="35e1c-129">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="35e1c-129">The name of the resource group.</span></span>
<span data-ttu-id="35e1c-130">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="35e1c-130">The name is case insensitive.</span></span>

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

### <span data-ttu-id="35e1c-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="35e1c-131">-SubscriptionId</span></span>
<span data-ttu-id="35e1c-132">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="35e1c-132">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="35e1c-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="35e1c-133">-Confirm</span></span>
<span data-ttu-id="35e1c-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="35e1c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35e1c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35e1c-135">-WhatIf</span></span>
<span data-ttu-id="35e1c-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="35e1c-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35e1c-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="35e1c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35e1c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35e1c-138">CommonParameters</span></span>
<span data-ttu-id="35e1c-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35e1c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35e1c-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="35e1c-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35e1c-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="35e1c-141">INPUTS</span></span>

### <span data-ttu-id="35e1c-142">Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="35e1c-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="35e1c-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="35e1c-143">OUTPUTS</span></span>

### <span data-ttu-id="35e1c-144">Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. Api20201102Preview. IMsixPackage</span><span class="sxs-lookup"><span data-stu-id="35e1c-144">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackage</span></span>

## <span data-ttu-id="35e1c-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="35e1c-145">NOTES</span></span>

<span data-ttu-id="35e1c-146">ALIAS</span><span class="sxs-lookup"><span data-stu-id="35e1c-146">ALIASES</span></span>

<span data-ttu-id="35e1c-147">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="35e1c-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="35e1c-148">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="35e1c-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="35e1c-149">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="35e1c-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="35e1c-150">INPUTOBJECT <IDesktopVirtualizationIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="35e1c-150">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="35e1c-151">`[ApplicationGroupName <String>]`: Namnet på program gruppen</span><span class="sxs-lookup"><span data-stu-id="35e1c-151">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="35e1c-152">`[ApplicationName <String>]`: Namnet på programmet i den angivna program gruppen</span><span class="sxs-lookup"><span data-stu-id="35e1c-152">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="35e1c-153">`[DesktopName <String>]`: Namnet på Skriv bordet i angiven Skriv bords grupp</span><span class="sxs-lookup"><span data-stu-id="35e1c-153">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="35e1c-154">`[HostPoolName <String>]`: Namnet på den värdbaserade poolen i den angivna resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="35e1c-154">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="35e1c-155">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="35e1c-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="35e1c-156">`[MsixPackageFullName <String>]`: Det versions specifika paketet fullständigt namn för MSIX paketet i angivet hostpool</span><span class="sxs-lookup"><span data-stu-id="35e1c-156">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="35e1c-157">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="35e1c-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="35e1c-158">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="35e1c-158">The name is case insensitive.</span></span>
  - <span data-ttu-id="35e1c-159">`[SessionHostName <String>]`: Namnet på sessions värden i den angivna poolen</span><span class="sxs-lookup"><span data-stu-id="35e1c-159">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="35e1c-160">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="35e1c-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="35e1c-161">`[UserSessionId <String>]`: Namnet på användarsessionen inom den angivna värd</span><span class="sxs-lookup"><span data-stu-id="35e1c-161">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="35e1c-162">`[WorkspaceName <String>]`: Arbets ytans namn</span><span class="sxs-lookup"><span data-stu-id="35e1c-162">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="35e1c-163">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="35e1c-163">RELATED LINKS</span></span>

