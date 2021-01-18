---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdusersession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdUserSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdUserSession.md
ms.openlocfilehash: 8dde4305003b97bd186a4601106a93e6f471edf4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523721"
---
# <span data-ttu-id="c4a6d-101">Get-AzWvdUserSession</span><span class="sxs-lookup"><span data-stu-id="c4a6d-101">Get-AzWvdUserSession</span></span>

## <span data-ttu-id="c4a6d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c4a6d-102">SYNOPSIS</span></span>
<span data-ttu-id="c4a6d-103">Skaffa en userSession.</span><span class="sxs-lookup"><span data-stu-id="c4a6d-103">Get a userSession.</span></span>

## <span data-ttu-id="c4a6d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c4a6d-104">SYNTAX</span></span>

### <span data-ttu-id="c4a6d-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="c4a6d-105">List (Default)</span></span>
```
Get-AzWvdUserSession -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c4a6d-106">Lära</span><span class="sxs-lookup"><span data-stu-id="c4a6d-106">Get</span></span>
```
Get-AzWvdUserSession -HostPoolName <String> -Id <String> -ResourceGroupName <String> -SessionHostName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c4a6d-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c4a6d-107">GetViaIdentity</span></span>
```
Get-AzWvdUserSession -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="c4a6d-108">List1</span><span class="sxs-lookup"><span data-stu-id="c4a6d-108">List1</span></span>
```
Get-AzWvdUserSession -HostPoolName <String> -ResourceGroupName <String> -SessionHostName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c4a6d-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c4a6d-109">DESCRIPTION</span></span>
<span data-ttu-id="c4a6d-110">Skaffa en userSession.</span><span class="sxs-lookup"><span data-stu-id="c4a6d-110">Get a userSession.</span></span>

## <span data-ttu-id="c4a6d-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c4a6d-111">EXAMPLES</span></span>

### <span data-ttu-id="c4a6d-112">Exempel 1: skaffa en Windows Virtual Desktop-UserSession med namn</span><span class="sxs-lookup"><span data-stu-id="c4a6d-112">Example 1: Get a Windows Virtual Desktop UserSession by name</span></span>
```powershell
PS C:\> Get-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName -Id 2

Name                           Type
----                           ----
HostPoolName/SessionHostName/2 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
```

<span data-ttu-id="c4a6d-113">Det här kommandot får en Windows Virtual Desktop-UserSession i en sessionsnyckel.</span><span class="sxs-lookup"><span data-stu-id="c4a6d-113">This command gets a Windows Virtual Desktop UserSession in a Session Host.</span></span>

### <span data-ttu-id="c4a6d-114">Exempel 2: lista UserSessions för virtuella skriv bord i Windows</span><span class="sxs-lookup"><span data-stu-id="c4a6d-114">Example 2: List Windows Virtual Desktop UserSessions</span></span>
```powershell
PS C:\> Get-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName

Name                           Type
----                           ----
HostPoolName/SessionHostName/2 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
HostPoolName/SessionHostName/3 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
```

<span data-ttu-id="c4a6d-115">Det här kommandot listar en UserSessions för Windows Virtual Desktop i en sessionsnyckel.</span><span class="sxs-lookup"><span data-stu-id="c4a6d-115">This command lists a Windows Virtual Desktop UserSessions in a Session Host.</span></span>

### <span data-ttu-id="c4a6d-116">Exempel 3: lista UserSessions virtuella skriv bord i Windows i pool</span><span class="sxs-lookup"><span data-stu-id="c4a6d-116">Example 3: List Windows Virtual Desktop UserSessions in host pool</span></span>
```powershell
PS C:\> Get-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName

Name                           Type
----                           ----
HostPoolName/SessionHostName/2 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
HostPoolName/SessionHostName/3 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
```

<span data-ttu-id="c4a6d-117">Det här kommandot listar en Windows Virtual Desktop-UserSessions i en sessionsnyckel i en adresspool.</span><span class="sxs-lookup"><span data-stu-id="c4a6d-117">This command lists a Windows Virtual Desktop UserSessions in a Session Host in a host pool.</span></span>

## <span data-ttu-id="c4a6d-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c4a6d-118">PARAMETERS</span></span>

### <span data-ttu-id="c4a6d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4a6d-119">-DefaultProfile</span></span>
<span data-ttu-id="c4a6d-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c4a6d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4a6d-121">-Filter</span><span class="sxs-lookup"><span data-stu-id="c4a6d-121">-Filter</span></span>
<span data-ttu-id="c4a6d-122">OData filter-uttryck.</span><span class="sxs-lookup"><span data-stu-id="c4a6d-122">OData filter expression.</span></span>
<span data-ttu-id="c4a6d-123">Giltiga egenskaper för filtrering är userPrincipalName och sessionState.</span><span class="sxs-lookup"><span data-stu-id="c4a6d-123">Valid properties for filtering are userprincipalname and sessionstate.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4a6d-124">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="c4a6d-124">-HostPoolName</span></span>
<span data-ttu-id="c4a6d-125">Namnet på den värdbaserade adresspoolen i den angivna resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="c4a6d-125">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4a6d-126">-ID</span><span class="sxs-lookup"><span data-stu-id="c4a6d-126">-Id</span></span>
<span data-ttu-id="c4a6d-127">Namnet på användarsessionen inom den angivna sessionsvärdservern</span><span class="sxs-lookup"><span data-stu-id="c4a6d-127">The name of the user session within the specified session host</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: UserSessionId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4a6d-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c4a6d-128">-InputObject</span></span>
<span data-ttu-id="c4a6d-129">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="c4a6d-129">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c4a6d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4a6d-130">-ResourceGroupName</span></span>
<span data-ttu-id="c4a6d-131">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="c4a6d-131">The name of the resource group.</span></span>
<span data-ttu-id="c4a6d-132">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="c4a6d-132">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4a6d-133">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="c4a6d-133">-SessionHostName</span></span>
<span data-ttu-id="c4a6d-134">Namnet på sessions värden i den angivna poolen</span><span class="sxs-lookup"><span data-stu-id="c4a6d-134">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4a6d-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c4a6d-135">-SubscriptionId</span></span>
<span data-ttu-id="c4a6d-136">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="c4a6d-136">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4a6d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4a6d-137">CommonParameters</span></span>
<span data-ttu-id="c4a6d-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4a6d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4a6d-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c4a6d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4a6d-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c4a6d-140">INPUTS</span></span>

### <span data-ttu-id="c4a6d-141">Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="c4a6d-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="c4a6d-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c4a6d-142">OUTPUTS</span></span>

### <span data-ttu-id="c4a6d-143">Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. Api20201102Preview. IUserSession</span><span class="sxs-lookup"><span data-stu-id="c4a6d-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IUserSession</span></span>

## <span data-ttu-id="c4a6d-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c4a6d-144">NOTES</span></span>

<span data-ttu-id="c4a6d-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="c4a6d-145">ALIASES</span></span>

<span data-ttu-id="c4a6d-146">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="c4a6d-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c4a6d-147">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="c4a6d-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c4a6d-148">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c4a6d-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c4a6d-149">INPUTOBJECT <IDesktopVirtualizationIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="c4a6d-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c4a6d-150">`[ApplicationGroupName <String>]`: Namnet på program gruppen</span><span class="sxs-lookup"><span data-stu-id="c4a6d-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="c4a6d-151">`[ApplicationName <String>]`: Namnet på programmet i den angivna program gruppen</span><span class="sxs-lookup"><span data-stu-id="c4a6d-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="c4a6d-152">`[DesktopName <String>]`: Namnet på Skriv bordet i angiven Skriv bords grupp</span><span class="sxs-lookup"><span data-stu-id="c4a6d-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="c4a6d-153">`[HostPoolName <String>]`: Namnet på den värdbaserade poolen i den angivna resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="c4a6d-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="c4a6d-154">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="c4a6d-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c4a6d-155">`[MsixPackageFullName <String>]`: Det versions specifika paketet fullständigt namn för MSIX paketet i angivet hostpool</span><span class="sxs-lookup"><span data-stu-id="c4a6d-155">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="c4a6d-156">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="c4a6d-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="c4a6d-157">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="c4a6d-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="c4a6d-158">`[SessionHostName <String>]`: Namnet på sessions värden i den angivna poolen</span><span class="sxs-lookup"><span data-stu-id="c4a6d-158">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="c4a6d-159">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="c4a6d-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="c4a6d-160">`[UserSessionId <String>]`: Namnet på användarsessionen inom den angivna värd</span><span class="sxs-lookup"><span data-stu-id="c4a6d-160">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="c4a6d-161">`[WorkspaceName <String>]`: Arbets ytans namn</span><span class="sxs-lookup"><span data-stu-id="c4a6d-161">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="c4a6d-162">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c4a6d-162">RELATED LINKS</span></span>

