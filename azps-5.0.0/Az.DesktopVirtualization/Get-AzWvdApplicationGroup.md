---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplicationGroup.md
ms.openlocfilehash: 1ad8b51a39cdde66728200af28c77f7b094f19c0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320068"
---
# <span data-ttu-id="b5644-101">Get-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="b5644-101">Get-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="b5644-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b5644-102">SYNOPSIS</span></span>
<span data-ttu-id="b5644-103">Skaffa en program grupp.</span><span class="sxs-lookup"><span data-stu-id="b5644-103">Get an application group.</span></span>

## <span data-ttu-id="b5644-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b5644-104">SYNTAX</span></span>

### <span data-ttu-id="b5644-105">List1 (standard)</span><span class="sxs-lookup"><span data-stu-id="b5644-105">List1 (Default)</span></span>
```
Get-AzWvdApplicationGroup [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="b5644-106">Lära</span><span class="sxs-lookup"><span data-stu-id="b5644-106">Get</span></span>
```
Get-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b5644-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b5644-107">GetViaIdentity</span></span>
```
Get-AzWvdApplicationGroup -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="b5644-108">Förteckning</span><span class="sxs-lookup"><span data-stu-id="b5644-108">List</span></span>
```
Get-AzWvdApplicationGroup -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="b5644-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b5644-109">DESCRIPTION</span></span>
<span data-ttu-id="b5644-110">Skaffa en program grupp.</span><span class="sxs-lookup"><span data-stu-id="b5644-110">Get an application group.</span></span>

## <span data-ttu-id="b5644-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b5644-111">EXAMPLES</span></span>

### <span data-ttu-id="b5644-112">Exempel 1: skaffa en Windows Virtual Desktop-ApplicationGroup med namn</span><span class="sxs-lookup"><span data-stu-id="b5644-112">Example 1: Get a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> Get-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName -Name ApplicationGroupName

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="b5644-113">Det här kommandot får en Windows-ApplicationGroup för virtuella skriv bord i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="b5644-113">This command gets a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

### <span data-ttu-id="b5644-114">Exempel 2: lista ApplicationGroups för virtuella skriv bord i Windows</span><span class="sxs-lookup"><span data-stu-id="b5644-114">Example 2: List Windows Virtual Desktop ApplicationGroups</span></span>
```powershell
PS C:\> Get-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName

Location   Name                  Type
--------   ----                  ----
eastus     ApplicationGroupName1 Microsoft.DesktopVirtualization/applicationgroups
eastus     ApplicationGroupName2 Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="b5644-115">Det här kommandot listar en ApplicationGroups för Windows virtuella skriv bord i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="b5644-115">This command lists a Windows Virtual Desktop ApplicationGroups in a Resource Group.</span></span>

## <span data-ttu-id="b5644-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b5644-116">PARAMETERS</span></span>

### <span data-ttu-id="b5644-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5644-117">-DefaultProfile</span></span>
<span data-ttu-id="b5644-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b5644-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5644-119">-Filter</span><span class="sxs-lookup"><span data-stu-id="b5644-119">-Filter</span></span>
<span data-ttu-id="b5644-120">OData filter-uttryck.</span><span class="sxs-lookup"><span data-stu-id="b5644-120">OData filter expression.</span></span>
<span data-ttu-id="b5644-121">Giltiga egenskaper för filtrering är applicationGroupType.</span><span class="sxs-lookup"><span data-stu-id="b5644-121">Valid properties for filtering are applicationGroupType.</span></span>

```yaml
Type: System.String
Parameter Sets: List, List1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5644-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b5644-122">-InputObject</span></span>
<span data-ttu-id="b5644-123">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="b5644-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b5644-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="b5644-124">-Name</span></span>
<span data-ttu-id="b5644-125">Namnet på program gruppen</span><span class="sxs-lookup"><span data-stu-id="b5644-125">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5644-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5644-126">-ResourceGroupName</span></span>
<span data-ttu-id="b5644-127">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="b5644-127">The name of the resource group.</span></span>
<span data-ttu-id="b5644-128">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="b5644-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b5644-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b5644-129">-SubscriptionId</span></span>
<span data-ttu-id="b5644-130">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="b5644-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b5644-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5644-131">CommonParameters</span></span>
<span data-ttu-id="b5644-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5644-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5644-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b5644-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5644-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b5644-134">INPUTS</span></span>

### <span data-ttu-id="b5644-135">Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="b5644-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="b5644-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b5644-136">OUTPUTS</span></span>

### <span data-ttu-id="b5644-137">Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. Api20191210Preview. IApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="b5644-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IApplicationGroup</span></span>

## <span data-ttu-id="b5644-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b5644-138">NOTES</span></span>

<span data-ttu-id="b5644-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="b5644-139">ALIASES</span></span>

<span data-ttu-id="b5644-140">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="b5644-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b5644-141">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="b5644-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b5644-142">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b5644-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b5644-143">INPUTOBJECT <IDesktopVirtualizationIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="b5644-143">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b5644-144">`[ApplicationGroupName <String>]`: Namnet på program gruppen</span><span class="sxs-lookup"><span data-stu-id="b5644-144">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="b5644-145">`[ApplicationName <String>]`: Namnet på programmet i den angivna program gruppen</span><span class="sxs-lookup"><span data-stu-id="b5644-145">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="b5644-146">`[DesktopName <String>]`: Namnet på Skriv bordet i angiven Skriv bords grupp</span><span class="sxs-lookup"><span data-stu-id="b5644-146">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="b5644-147">`[HostPoolName <String>]`: Namnet på den värdbaserade poolen i den angivna resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="b5644-147">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="b5644-148">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="b5644-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b5644-149">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="b5644-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b5644-150">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="b5644-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="b5644-151">`[SessionHostName <String>]`: Namnet på sessions värden i den angivna poolen</span><span class="sxs-lookup"><span data-stu-id="b5644-151">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="b5644-152">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="b5644-152">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="b5644-153">`[UserSessionId <String>]`: Namnet på användarsessionen inom den angivna värd</span><span class="sxs-lookup"><span data-stu-id="b5644-153">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="b5644-154">`[WorkspaceName <String>]`: Arbets ytans namn</span><span class="sxs-lookup"><span data-stu-id="b5644-154">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="b5644-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b5644-155">RELATED LINKS</span></span>

