---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdMsixPackage.md
ms.openlocfilehash: 51b940df2ee26c3da53c34fd7f1ffa25d3a266a9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426387"
---
# <span data-ttu-id="48d51-101">Get-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="48d51-101">Get-AzWvdMsixPackage</span></span>

## <span data-ttu-id="48d51-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="48d51-102">SYNOPSIS</span></span>
<span data-ttu-id="48d51-103">Skaffa en msixpackage.</span><span class="sxs-lookup"><span data-stu-id="48d51-103">Get a msixpackage.</span></span>

## <span data-ttu-id="48d51-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="48d51-104">SYNTAX</span></span>

### <span data-ttu-id="48d51-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="48d51-105">List (Default)</span></span>
```
Get-AzWvdMsixPackage -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="48d51-106">Lära</span><span class="sxs-lookup"><span data-stu-id="48d51-106">Get</span></span>
```
Get-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="48d51-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="48d51-107">GetViaIdentity</span></span>
```
Get-AzWvdMsixPackage -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="48d51-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="48d51-108">DESCRIPTION</span></span>
<span data-ttu-id="48d51-109">Skaffa en msixpackage.</span><span class="sxs-lookup"><span data-stu-id="48d51-109">Get a msixpackage.</span></span>

## <span data-ttu-id="48d51-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="48d51-110">EXAMPLES</span></span>

### <span data-ttu-id="48d51-111">Exempel 1: skaffa ett MSIX-paket med namn</span><span class="sxs-lookup"><span data-stu-id="48d51-111">Example 1: Get a MSIX Package by Name</span></span>
```powershell
PS C:\> Get-AzWvdMsixPackage -HostPoolName HostPoolName -ResourceGroupName ResourceGroupName -SubscriptionId SubscriptionId -FullName PackageFullName

Name                                                  Type
----                                                  ----
HostPoolName/MSIXPackage_FullName                     Microsoft.DesktopVirtualization/hostpools/msixpackages
```

<span data-ttu-id="48d51-112">Det här kommandot får ett MSIX-paket i ett HostPool.</span><span class="sxs-lookup"><span data-stu-id="48d51-112">This command gets a MSIX Package in a HostPool.</span></span>

### <span data-ttu-id="48d51-113">Exempel 2: lista MSIX paket</span><span class="sxs-lookup"><span data-stu-id="48d51-113">Example 2: List MSIX Packages</span></span> 
```powershell
PS C:\> Get-AzWvdMsixPackage -HostPoolName HostPoolName -ResourceGroupName ResourceGroupName -SubscriptionId SubscriptionId

Name                                                  Type
----                                                  ----
HostPoolName/MSIXPackage_FullName1                    Microsoft.DesktopVirtualization/hostpools/msixpackages
HostPoolName/MSIXPackage_FullName2                    Microsoft.DesktopVirtualization/hostpools/msixpackages
HostPoolName/MSIXPackage_FullName3                    Microsoft.DesktopVirtualization/hostpools/msixpackages
```

<span data-ttu-id="48d51-114">Det här kommandot listar MSIX-paket i ett HostPool.</span><span class="sxs-lookup"><span data-stu-id="48d51-114">This command Lists MSIX Packages in a HostPool.</span></span>

## <span data-ttu-id="48d51-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="48d51-115">PARAMETERS</span></span>

### <span data-ttu-id="48d51-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48d51-116">-DefaultProfile</span></span>
<span data-ttu-id="48d51-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="48d51-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48d51-118">-FullName</span><span class="sxs-lookup"><span data-stu-id="48d51-118">-FullName</span></span>
<span data-ttu-id="48d51-119">Det versions specifika paketet fullständigt namn för MSIX paketet i angivet hostpool</span><span class="sxs-lookup"><span data-stu-id="48d51-119">The version specific package full name of the MSIX package within specified hostpool</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: MsixPackageFullName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48d51-120">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="48d51-120">-HostPoolName</span></span>
<span data-ttu-id="48d51-121">Namnet på den värdbaserade adresspoolen i den angivna resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="48d51-121">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48d51-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="48d51-122">-InputObject</span></span>
<span data-ttu-id="48d51-123">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="48d51-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="48d51-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48d51-124">-ResourceGroupName</span></span>
<span data-ttu-id="48d51-125">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="48d51-125">The name of the resource group.</span></span>
<span data-ttu-id="48d51-126">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="48d51-126">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48d51-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="48d51-127">-SubscriptionId</span></span>
<span data-ttu-id="48d51-128">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="48d51-128">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48d51-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48d51-129">CommonParameters</span></span>
<span data-ttu-id="48d51-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48d51-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48d51-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="48d51-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48d51-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="48d51-132">INPUTS</span></span>

### <span data-ttu-id="48d51-133">Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="48d51-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="48d51-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="48d51-134">OUTPUTS</span></span>

### <span data-ttu-id="48d51-135">Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. Api20201102Preview. IMsixPackage</span><span class="sxs-lookup"><span data-stu-id="48d51-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackage</span></span>

## <span data-ttu-id="48d51-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="48d51-136">NOTES</span></span>

<span data-ttu-id="48d51-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="48d51-137">ALIASES</span></span>

<span data-ttu-id="48d51-138">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="48d51-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="48d51-139">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="48d51-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="48d51-140">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="48d51-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="48d51-141">INPUTOBJECT <IDesktopVirtualizationIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="48d51-141">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="48d51-142">`[ApplicationGroupName <String>]`: Namnet på program gruppen</span><span class="sxs-lookup"><span data-stu-id="48d51-142">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="48d51-143">`[ApplicationName <String>]`: Namnet på programmet i den angivna program gruppen</span><span class="sxs-lookup"><span data-stu-id="48d51-143">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="48d51-144">`[DesktopName <String>]`: Namnet på Skriv bordet i angiven Skriv bords grupp</span><span class="sxs-lookup"><span data-stu-id="48d51-144">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="48d51-145">`[HostPoolName <String>]`: Namnet på den värdbaserade poolen i den angivna resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="48d51-145">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="48d51-146">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="48d51-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="48d51-147">`[MsixPackageFullName <String>]`: Det versions specifika paketet fullständigt namn för MSIX paketet i angivet hostpool</span><span class="sxs-lookup"><span data-stu-id="48d51-147">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="48d51-148">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="48d51-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="48d51-149">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="48d51-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="48d51-150">`[SessionHostName <String>]`: Namnet på sessions värden i den angivna poolen</span><span class="sxs-lookup"><span data-stu-id="48d51-150">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="48d51-151">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="48d51-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="48d51-152">`[UserSessionId <String>]`: Namnet på användarsessionen inom den angivna värd</span><span class="sxs-lookup"><span data-stu-id="48d51-152">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="48d51-153">`[WorkspaceName <String>]`: Arbets ytans namn</span><span class="sxs-lookup"><span data-stu-id="48d51-153">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="48d51-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="48d51-154">RELATED LINKS</span></span>

