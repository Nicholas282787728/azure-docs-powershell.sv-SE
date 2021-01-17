---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplicationGroup.md
ms.openlocfilehash: 0bc1c5eef68abc46d43132a86afe3ab6f86b002d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98398915"
---
# <span data-ttu-id="f4f3a-101">Get-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="f4f3a-101">Get-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="f4f3a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f4f3a-102">SYNOPSIS</span></span>
<span data-ttu-id="f4f3a-103">Skaffa en program grupp.</span><span class="sxs-lookup"><span data-stu-id="f4f3a-103">Get an application group.</span></span>

## <span data-ttu-id="f4f3a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f4f3a-104">SYNTAX</span></span>

### <span data-ttu-id="f4f3a-105">List1 (standard)</span><span class="sxs-lookup"><span data-stu-id="f4f3a-105">List1 (Default)</span></span>
```
Get-AzWvdApplicationGroup [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="f4f3a-106">Lära</span><span class="sxs-lookup"><span data-stu-id="f4f3a-106">Get</span></span>
```
Get-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f4f3a-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f4f3a-107">GetViaIdentity</span></span>
```
Get-AzWvdApplicationGroup -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="f4f3a-108">Förteckning</span><span class="sxs-lookup"><span data-stu-id="f4f3a-108">List</span></span>
```
Get-AzWvdApplicationGroup -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="f4f3a-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f4f3a-109">DESCRIPTION</span></span>
<span data-ttu-id="f4f3a-110">Skaffa en program grupp.</span><span class="sxs-lookup"><span data-stu-id="f4f3a-110">Get an application group.</span></span>

## <span data-ttu-id="f4f3a-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f4f3a-111">EXAMPLES</span></span>

### <span data-ttu-id="f4f3a-112">Exempel 1: skaffa en Windows Virtual Desktop-ApplicationGroup med namn</span><span class="sxs-lookup"><span data-stu-id="f4f3a-112">Example 1: Get a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> Get-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName -Name ApplicationGroupName

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="f4f3a-113">Det här kommandot får en Windows-ApplicationGroup för virtuella skriv bord i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="f4f3a-113">This command gets a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

### <span data-ttu-id="f4f3a-114">Exempel 2: lista ApplicationGroups för virtuella skriv bord i Windows</span><span class="sxs-lookup"><span data-stu-id="f4f3a-114">Example 2: List Windows Virtual Desktop ApplicationGroups</span></span>
```powershell
PS C:\> Get-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName

Location   Name                  Type
--------   ----                  ----
eastus     ApplicationGroupName1 Microsoft.DesktopVirtualization/applicationgroups
eastus     ApplicationGroupName2 Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="f4f3a-115">Det här kommandot listar en ApplicationGroups för Windows virtuella skriv bord i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="f4f3a-115">This command lists a Windows Virtual Desktop ApplicationGroups in a Resource Group.</span></span>

## <span data-ttu-id="f4f3a-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f4f3a-116">PARAMETERS</span></span>

### <span data-ttu-id="f4f3a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4f3a-117">-DefaultProfile</span></span>
<span data-ttu-id="f4f3a-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f4f3a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4f3a-119">-Filter</span><span class="sxs-lookup"><span data-stu-id="f4f3a-119">-Filter</span></span>
<span data-ttu-id="f4f3a-120">OData filter-uttryck.</span><span class="sxs-lookup"><span data-stu-id="f4f3a-120">OData filter expression.</span></span>
<span data-ttu-id="f4f3a-121">Giltiga egenskaper för filtrering är applicationGroupType.</span><span class="sxs-lookup"><span data-stu-id="f4f3a-121">Valid properties for filtering are applicationGroupType.</span></span>

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

### <span data-ttu-id="f4f3a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4f3a-122">-InputObject</span></span>
<span data-ttu-id="f4f3a-123">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="f4f3a-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f4f3a-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="f4f3a-124">-Name</span></span>
<span data-ttu-id="f4f3a-125">Namnet på program gruppen</span><span class="sxs-lookup"><span data-stu-id="f4f3a-125">The name of the application group</span></span>

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

### <span data-ttu-id="f4f3a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4f3a-126">-ResourceGroupName</span></span>
<span data-ttu-id="f4f3a-127">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f4f3a-127">The name of the resource group.</span></span>
<span data-ttu-id="f4f3a-128">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="f4f3a-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="f4f3a-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f4f3a-129">-SubscriptionId</span></span>
<span data-ttu-id="f4f3a-130">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="f4f3a-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="f4f3a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4f3a-131">CommonParameters</span></span>
<span data-ttu-id="f4f3a-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4f3a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4f3a-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f4f3a-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4f3a-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f4f3a-134">INPUTS</span></span>

### <span data-ttu-id="f4f3a-135">Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="f4f3a-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="f4f3a-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f4f3a-136">OUTPUTS</span></span>

### <span data-ttu-id="f4f3a-137">Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. Api20201019Preview. IApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="f4f3a-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IApplicationGroup</span></span>

## <span data-ttu-id="f4f3a-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f4f3a-138">NOTES</span></span>

<span data-ttu-id="f4f3a-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="f4f3a-139">ALIASES</span></span>

<span data-ttu-id="f4f3a-140">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="f4f3a-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f4f3a-141">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="f4f3a-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f4f3a-142">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f4f3a-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f4f3a-143">INPUTOBJECT <IDesktopVirtualizationIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="f4f3a-143">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f4f3a-144">`[ApplicationGroupName <String>]`: Namnet på program gruppen</span><span class="sxs-lookup"><span data-stu-id="f4f3a-144">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="f4f3a-145">`[ApplicationName <String>]`: Namnet på programmet i den angivna program gruppen</span><span class="sxs-lookup"><span data-stu-id="f4f3a-145">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="f4f3a-146">`[DesktopName <String>]`: Namnet på Skriv bordet i angiven Skriv bords grupp</span><span class="sxs-lookup"><span data-stu-id="f4f3a-146">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="f4f3a-147">`[HostPoolName <String>]`: Namnet på den värdbaserade poolen i den angivna resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="f4f3a-147">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="f4f3a-148">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="f4f3a-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f4f3a-149">`[MsixPackageFullName <String>]`: Det versions specifika paketet fullständigt namn för MSIX paketet i angivet hostpool</span><span class="sxs-lookup"><span data-stu-id="f4f3a-149">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="f4f3a-150">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f4f3a-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="f4f3a-151">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="f4f3a-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="f4f3a-152">`[SessionHostName <String>]`: Namnet på sessions värden i den angivna poolen</span><span class="sxs-lookup"><span data-stu-id="f4f3a-152">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="f4f3a-153">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="f4f3a-153">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="f4f3a-154">`[UserSessionId <String>]`: Namnet på användarsessionen inom den angivna värd</span><span class="sxs-lookup"><span data-stu-id="f4f3a-154">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="f4f3a-155">`[WorkspaceName <String>]`: Arbets ytans namn</span><span class="sxs-lookup"><span data-stu-id="f4f3a-155">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="f4f3a-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f4f3a-156">RELATED LINKS</span></span>

