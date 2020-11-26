---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdsessionhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdSessionHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdSessionHost.md
ms.openlocfilehash: 94f4c5ad9c401c429c9ef2f2f1c146f83a407196
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102900"
---
# <span data-ttu-id="4384c-101">Get-AzWvdSessionHost</span><span class="sxs-lookup"><span data-stu-id="4384c-101">Get-AzWvdSessionHost</span></span>

## <span data-ttu-id="4384c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4384c-102">SYNOPSIS</span></span>
<span data-ttu-id="4384c-103">Skaffa en värd för en session.</span><span class="sxs-lookup"><span data-stu-id="4384c-103">Get a session host.</span></span>

## <span data-ttu-id="4384c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4384c-104">SYNTAX</span></span>

### <span data-ttu-id="4384c-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="4384c-105">List (Default)</span></span>
```
Get-AzWvdSessionHost -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4384c-106">Lära</span><span class="sxs-lookup"><span data-stu-id="4384c-106">Get</span></span>
```
Get-AzWvdSessionHost -HostPoolName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4384c-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4384c-107">GetViaIdentity</span></span>
```
Get-AzWvdSessionHost -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="4384c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4384c-108">DESCRIPTION</span></span>
<span data-ttu-id="4384c-109">Skaffa en värd för en session.</span><span class="sxs-lookup"><span data-stu-id="4384c-109">Get a session host.</span></span>

## <span data-ttu-id="4384c-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4384c-110">EXAMPLES</span></span>

### <span data-ttu-id="4384c-111">Exempel 1: skaffa en Windows Virtual Desktop-SessionHost med namn</span><span class="sxs-lookup"><span data-stu-id="4384c-111">Example 1: Get a Windows Virtual Desktop SessionHost by name</span></span>
```powershell
PS C:\> Get-AzWvdSessionHost -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -Name SessionHostName

Name                                               Type
----                                               ----
HostPoolName/SessionHostName Microsoft.DesktopVirtualization/hostpools/sessionhosts
```

<span data-ttu-id="4384c-112">Det här kommandot får en Windows-SessionHost för virtuella skriv bord i en adresspool.</span><span class="sxs-lookup"><span data-stu-id="4384c-112">This command gets a Windows Virtual Desktop SessionHost in a Host Pool.</span></span>

### <span data-ttu-id="4384c-113">Exempel 2: lista SessionHosts för virtuella skriv bord i Windows</span><span class="sxs-lookup"><span data-stu-id="4384c-113">Example 2: List Windows Virtual Desktop SessionHosts</span></span>
```powershell
PS C:\> Get-AzWvdSessionHost -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName

Name                                               Type
----                                               ----
HostPoolName/SessionHostName1 Microsoft.DesktopVirtualization/hostpools/sessionhosts
HostPoolName/SessionHostName2 Microsoft.DesktopVirtualization/hostpools/sessionhosts
```

<span data-ttu-id="4384c-114">Det här kommandot listar en SessionHosts för Windows virtuella skriv bord i en adresspool.</span><span class="sxs-lookup"><span data-stu-id="4384c-114">This command lists a Windows Virtual Desktop SessionHosts in a Host Pool.</span></span>

## <span data-ttu-id="4384c-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4384c-115">PARAMETERS</span></span>

### <span data-ttu-id="4384c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4384c-116">-DefaultProfile</span></span>
<span data-ttu-id="4384c-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4384c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4384c-118">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="4384c-118">-HostPoolName</span></span>
<span data-ttu-id="4384c-119">Namnet på den värdbaserade adresspoolen i den angivna resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="4384c-119">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="4384c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4384c-120">-InputObject</span></span>
<span data-ttu-id="4384c-121">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="4384c-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4384c-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="4384c-122">-Name</span></span>
<span data-ttu-id="4384c-123">Namnet på sessions värden i den angivna poolen</span><span class="sxs-lookup"><span data-stu-id="4384c-123">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: SessionHostName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4384c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4384c-124">-ResourceGroupName</span></span>
<span data-ttu-id="4384c-125">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="4384c-125">The name of the resource group.</span></span>
<span data-ttu-id="4384c-126">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="4384c-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="4384c-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4384c-127">-SubscriptionId</span></span>
<span data-ttu-id="4384c-128">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="4384c-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="4384c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4384c-129">CommonParameters</span></span>
<span data-ttu-id="4384c-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4384c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4384c-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4384c-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4384c-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4384c-132">INPUTS</span></span>

### <span data-ttu-id="4384c-133">Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="4384c-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="4384c-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4384c-134">OUTPUTS</span></span>

### <span data-ttu-id="4384c-135">Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. Api20191210Preview. ISessionHost</span><span class="sxs-lookup"><span data-stu-id="4384c-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.ISessionHost</span></span>

## <span data-ttu-id="4384c-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4384c-136">NOTES</span></span>

<span data-ttu-id="4384c-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="4384c-137">ALIASES</span></span>

<span data-ttu-id="4384c-138">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="4384c-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4384c-139">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="4384c-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4384c-140">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4384c-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4384c-141">INPUTOBJECT <IDesktopVirtualizationIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="4384c-141">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4384c-142">`[ApplicationGroupName <String>]`: Namnet på program gruppen</span><span class="sxs-lookup"><span data-stu-id="4384c-142">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="4384c-143">`[ApplicationName <String>]`: Namnet på programmet i den angivna program gruppen</span><span class="sxs-lookup"><span data-stu-id="4384c-143">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="4384c-144">`[DesktopName <String>]`: Namnet på Skriv bordet i angiven Skriv bords grupp</span><span class="sxs-lookup"><span data-stu-id="4384c-144">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="4384c-145">`[HostPoolName <String>]`: Namnet på den värdbaserade poolen i den angivna resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="4384c-145">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="4384c-146">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="4384c-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4384c-147">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="4384c-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="4384c-148">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="4384c-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="4384c-149">`[SessionHostName <String>]`: Namnet på sessions värden i den angivna poolen</span><span class="sxs-lookup"><span data-stu-id="4384c-149">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="4384c-150">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="4384c-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="4384c-151">`[UserSessionId <String>]`: Namnet på användarsessionen inom den angivna värd</span><span class="sxs-lookup"><span data-stu-id="4384c-151">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="4384c-152">`[WorkspaceName <String>]`: Arbets ytans namn</span><span class="sxs-lookup"><span data-stu-id="4384c-152">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="4384c-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4384c-153">RELATED LINKS</span></span>
