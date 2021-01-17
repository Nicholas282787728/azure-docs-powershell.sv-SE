---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/expand-azwvdmsiximage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Expand-AzWvdMsixImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Expand-AzWvdMsixImage.md
ms.openlocfilehash: 56122e8d1ae94b6a898c073f2b2f2fb891504789
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426384"
---
# <span data-ttu-id="a17b5-101">Expand-AzWvdMsixImage</span><span class="sxs-lookup"><span data-stu-id="a17b5-101">Expand-AzWvdMsixImage</span></span>

## <span data-ttu-id="a17b5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a17b5-102">SYNOPSIS</span></span>
<span data-ttu-id="a17b5-103">Expanderar och visar MSIX-paket i en bild med bild Sök vägen.</span><span class="sxs-lookup"><span data-stu-id="a17b5-103">Expands and Lists MSIX packages in an Image, given the Image Path.</span></span>

## <span data-ttu-id="a17b5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a17b5-104">SYNTAX</span></span>

### <span data-ttu-id="a17b5-105">ExpandExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="a17b5-105">ExpandExpanded (Default)</span></span>
```
Expand-AzWvdMsixImage -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Uri <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a17b5-106">Byggnad</span><span class="sxs-lookup"><span data-stu-id="a17b5-106">Expand</span></span>
```
Expand-AzWvdMsixImage -HostPoolName <String> -ResourceGroupName <String> -MsixImageUri <IMsixImageUri>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a17b5-107">ExpandViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a17b5-107">ExpandViaIdentity</span></span>
```
Expand-AzWvdMsixImage -InputObject <IDesktopVirtualizationIdentity> -MsixImageUri <IMsixImageUri>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a17b5-108">ExpandViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="a17b5-108">ExpandViaIdentityExpanded</span></span>
```
Expand-AzWvdMsixImage -InputObject <IDesktopVirtualizationIdentity> [-Uri <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a17b5-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a17b5-109">DESCRIPTION</span></span>
<span data-ttu-id="a17b5-110">Expanderar och visar MSIX-paket i en bild med bild Sök vägen.</span><span class="sxs-lookup"><span data-stu-id="a17b5-110">Expands and Lists MSIX packages in an Image, given the Image Path.</span></span>

## <span data-ttu-id="a17b5-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a17b5-111">EXAMPLES</span></span>

### <span data-ttu-id="a17b5-112">Exempel 1: expanderar angiven bild Sök väg och hämtar paket-metadata som hittats i AppxManifest.xml</span><span class="sxs-lookup"><span data-stu-id="a17b5-112">Example 1: Expands specified Image Path and retrieves Package metadata found in AppxManifest.xml</span></span>
```powershell
PS C:\> Expand-AzWvdMsixImage -HostPoolName HostPoolName `
          -ResourceGroupName resourceGroupName `
          -SubscriptionId SubscriptionId `
          -Uri ImagePathURI

Name                          Type
----                          ----
HostPoolName/extractmsiximage Microsoft.DesktopVirtualization/hostpools/extractmsiximage
```

<span data-ttu-id="a17b5-113">Det här kommandot returnerar metadata för MSIX-paketet som finns på angiven bild.</span><span class="sxs-lookup"><span data-stu-id="a17b5-113">This command returns Metadata of MSIX Package found in the given Image Path.</span></span>

## <span data-ttu-id="a17b5-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a17b5-114">PARAMETERS</span></span>

### <span data-ttu-id="a17b5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a17b5-115">-DefaultProfile</span></span>
<span data-ttu-id="a17b5-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a17b5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a17b5-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="a17b5-117">-HostPoolName</span></span>
<span data-ttu-id="a17b5-118">Namnet på den värdbaserade adresspoolen i den angivna resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="a17b5-118">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: Expand, ExpandExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a17b5-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a17b5-119">-InputObject</span></span>
<span data-ttu-id="a17b5-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="a17b5-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: ExpandViaIdentity, ExpandViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a17b5-121">-MsixImageUri</span><span class="sxs-lookup"><span data-stu-id="a17b5-121">-MsixImageUri</span></span>
<span data-ttu-id="a17b5-122">Representerar URI som hänvisar till MSIX-bild för att konstruera, se avsnittet anteckningar för MSIXIMAGEURI-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="a17b5-122">Represents URI referring to MSIX Image To construct, see NOTES section for MSIXIMAGEURI properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixImageUri
Parameter Sets: Expand, ExpandViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a17b5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a17b5-123">-ResourceGroupName</span></span>
<span data-ttu-id="a17b5-124">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a17b5-124">The name of the resource group.</span></span>
<span data-ttu-id="a17b5-125">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="a17b5-125">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Expand, ExpandExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a17b5-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a17b5-126">-SubscriptionId</span></span>
<span data-ttu-id="a17b5-127">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="a17b5-127">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Expand, ExpandExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a17b5-128">-URI</span><span class="sxs-lookup"><span data-stu-id="a17b5-128">-Uri</span></span>
<span data-ttu-id="a17b5-129">URI till bild</span><span class="sxs-lookup"><span data-stu-id="a17b5-129">URI to Image</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandExpanded, ExpandViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a17b5-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a17b5-130">-Confirm</span></span>
<span data-ttu-id="a17b5-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a17b5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a17b5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a17b5-132">-WhatIf</span></span>
<span data-ttu-id="a17b5-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a17b5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a17b5-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a17b5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a17b5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a17b5-135">CommonParameters</span></span>
<span data-ttu-id="a17b5-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a17b5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a17b5-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a17b5-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a17b5-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a17b5-138">INPUTS</span></span>

### <span data-ttu-id="a17b5-139">Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. Api20201102Preview. IMsixImageUri</span><span class="sxs-lookup"><span data-stu-id="a17b5-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixImageUri</span></span>

### <span data-ttu-id="a17b5-140">Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="a17b5-140">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="a17b5-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a17b5-141">OUTPUTS</span></span>

### <span data-ttu-id="a17b5-142">Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. Api20201102Preview. IExpandMsixImage</span><span class="sxs-lookup"><span data-stu-id="a17b5-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IExpandMsixImage</span></span>

## <span data-ttu-id="a17b5-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a17b5-143">NOTES</span></span>

<span data-ttu-id="a17b5-144">ALIAS</span><span class="sxs-lookup"><span data-stu-id="a17b5-144">ALIASES</span></span>

<span data-ttu-id="a17b5-145">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="a17b5-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a17b5-146">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="a17b5-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a17b5-147">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a17b5-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a17b5-148">INPUTOBJECT <IDesktopVirtualizationIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="a17b5-148">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a17b5-149">`[ApplicationGroupName <String>]`: Namnet på program gruppen</span><span class="sxs-lookup"><span data-stu-id="a17b5-149">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="a17b5-150">`[ApplicationName <String>]`: Namnet på programmet i den angivna program gruppen</span><span class="sxs-lookup"><span data-stu-id="a17b5-150">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="a17b5-151">`[DesktopName <String>]`: Namnet på Skriv bordet i angiven Skriv bords grupp</span><span class="sxs-lookup"><span data-stu-id="a17b5-151">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="a17b5-152">`[HostPoolName <String>]`: Namnet på den värdbaserade poolen i den angivna resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="a17b5-152">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="a17b5-153">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="a17b5-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a17b5-154">`[MsixPackageFullName <String>]`: Det versions specifika paketet fullständigt namn för MSIX paketet i angivet hostpool</span><span class="sxs-lookup"><span data-stu-id="a17b5-154">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="a17b5-155">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a17b5-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="a17b5-156">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="a17b5-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="a17b5-157">`[SessionHostName <String>]`: Namnet på sessions värden i den angivna poolen</span><span class="sxs-lookup"><span data-stu-id="a17b5-157">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="a17b5-158">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="a17b5-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="a17b5-159">`[UserSessionId <String>]`: Namnet på användarsessionen inom den angivna värd</span><span class="sxs-lookup"><span data-stu-id="a17b5-159">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="a17b5-160">`[WorkspaceName <String>]`: Arbets ytans namn</span><span class="sxs-lookup"><span data-stu-id="a17b5-160">`[WorkspaceName <String>]`: The name of the workspace</span></span>

<span data-ttu-id="a17b5-161">MSIXIMAGEURI <IMsixImageUri> : representerar URI-referenser till MSIX-bild</span><span class="sxs-lookup"><span data-stu-id="a17b5-161">MSIXIMAGEURI <IMsixImageUri>: Represents URI referring to MSIX Image</span></span>
  - <span data-ttu-id="a17b5-162">`[Uri <String>]`: URI till bild</span><span class="sxs-lookup"><span data-stu-id="a17b5-162">`[Uri <String>]`: URI to Image</span></span>

## <span data-ttu-id="a17b5-163">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a17b5-163">RELATED LINKS</span></span>

