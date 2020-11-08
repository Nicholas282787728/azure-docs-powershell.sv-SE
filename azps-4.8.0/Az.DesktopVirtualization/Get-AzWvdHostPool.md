---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdHostPool.md
ms.openlocfilehash: e04d13b96f36b96b2ae1c22f6f6e5b3c50b338f4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260520"
---
# <span data-ttu-id="9e619-101">Get-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="9e619-101">Get-AzWvdHostPool</span></span>

## <span data-ttu-id="9e619-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9e619-102">SYNOPSIS</span></span>
<span data-ttu-id="9e619-103">Skaffa en adresspool.</span><span class="sxs-lookup"><span data-stu-id="9e619-103">Get a host pool.</span></span>

## <span data-ttu-id="9e619-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9e619-104">SYNTAX</span></span>

### <span data-ttu-id="9e619-105">List1 (standard)</span><span class="sxs-lookup"><span data-stu-id="9e619-105">List1 (Default)</span></span>
```
Get-AzWvdHostPool [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9e619-106">Lära</span><span class="sxs-lookup"><span data-stu-id="9e619-106">Get</span></span>
```
Get-AzWvdHostPool -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9e619-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9e619-107">GetViaIdentity</span></span>
```
Get-AzWvdHostPool -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="9e619-108">Förteckning</span><span class="sxs-lookup"><span data-stu-id="9e619-108">List</span></span>
```
Get-AzWvdHostPool -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="9e619-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9e619-109">DESCRIPTION</span></span>
<span data-ttu-id="9e619-110">Skaffa en adresspool.</span><span class="sxs-lookup"><span data-stu-id="9e619-110">Get a host pool.</span></span>

## <span data-ttu-id="9e619-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9e619-111">EXAMPLES</span></span>

### <span data-ttu-id="9e619-112">Exempel 1: skaffa en Windows Virtual Desktop-HostPool med namn</span><span class="sxs-lookup"><span data-stu-id="9e619-112">Example 1: Get a Windows Virtual Desktop HostPool by name</span></span>
```powershell
PS C:\> Get-AzWvdHostPool -ResourceGroupName ResourceGroupName -Name HostPoolName

Location   Name                 Type
--------   ----                 ----
eastus     HostPoolName Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="9e619-113">Det här kommandot får en Windows-HostPool för virtuella skriv bord i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="9e619-113">This command gets a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

### <span data-ttu-id="9e619-114">Exempel 2: lista HostPools för virtuella skriv bord i Windows</span><span class="sxs-lookup"><span data-stu-id="9e619-114">Example 2: List Windows Virtual Desktop HostPools</span></span>
```powershell
PS C:\> Get-AzWvdHostPool -ResourceGroupName ResourceGroupName

Location   Name          Type
--------   ----          ----
eastus     HostPoolName1 Microsoft.DesktopVirtualization/hostpools
eastus     HostPoolName2 Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="9e619-115">Det här kommandot listar en HostPools för Windows virtuella skriv bord i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="9e619-115">This command lists a Windows Virtual Desktop HostPools in a Resource Group.</span></span>

## <span data-ttu-id="9e619-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9e619-116">PARAMETERS</span></span>

### <span data-ttu-id="9e619-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e619-117">-DefaultProfile</span></span>
<span data-ttu-id="9e619-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9e619-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e619-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9e619-119">-InputObject</span></span>
<span data-ttu-id="9e619-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="9e619-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9e619-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="9e619-121">-Name</span></span>
<span data-ttu-id="9e619-122">Namnet på den värdbaserade adresspoolen i den angivna resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="9e619-122">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: HostPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e619-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e619-123">-ResourceGroupName</span></span>
<span data-ttu-id="9e619-124">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="9e619-124">The name of the resource group.</span></span>
<span data-ttu-id="9e619-125">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="9e619-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="9e619-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9e619-126">-SubscriptionId</span></span>
<span data-ttu-id="9e619-127">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="9e619-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="9e619-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e619-128">CommonParameters</span></span>
<span data-ttu-id="9e619-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e619-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e619-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9e619-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e619-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9e619-131">INPUTS</span></span>

### <span data-ttu-id="9e619-132">Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="9e619-132">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="9e619-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9e619-133">OUTPUTS</span></span>

### <span data-ttu-id="9e619-134">Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. Api20191210Preview. IHostPool</span><span class="sxs-lookup"><span data-stu-id="9e619-134">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IHostPool</span></span>

## <span data-ttu-id="9e619-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9e619-135">NOTES</span></span>

<span data-ttu-id="9e619-136">ALIAS</span><span class="sxs-lookup"><span data-stu-id="9e619-136">ALIASES</span></span>

<span data-ttu-id="9e619-137">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="9e619-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9e619-138">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="9e619-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9e619-139">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9e619-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9e619-140">INPUTOBJECT <IDesktopVirtualizationIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="9e619-140">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9e619-141">`[ApplicationGroupName <String>]`: Namnet på program gruppen</span><span class="sxs-lookup"><span data-stu-id="9e619-141">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="9e619-142">`[ApplicationName <String>]`: Namnet på programmet i den angivna program gruppen</span><span class="sxs-lookup"><span data-stu-id="9e619-142">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="9e619-143">`[DesktopName <String>]`: Namnet på Skriv bordet i angiven Skriv bords grupp</span><span class="sxs-lookup"><span data-stu-id="9e619-143">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="9e619-144">`[HostPoolName <String>]`: Namnet på den värdbaserade poolen i den angivna resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="9e619-144">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="9e619-145">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="9e619-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9e619-146">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="9e619-146">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="9e619-147">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="9e619-147">The name is case insensitive.</span></span>
  - <span data-ttu-id="9e619-148">`[SessionHostName <String>]`: Namnet på sessions värden i den angivna poolen</span><span class="sxs-lookup"><span data-stu-id="9e619-148">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="9e619-149">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="9e619-149">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="9e619-150">`[UserSessionId <String>]`: Namnet på användarsessionen inom den angivna värd</span><span class="sxs-lookup"><span data-stu-id="9e619-150">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="9e619-151">`[WorkspaceName <String>]`: Arbets ytans namn</span><span class="sxs-lookup"><span data-stu-id="9e619-151">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="9e619-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9e619-152">RELATED LINKS</span></span>

