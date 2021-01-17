---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdWorkspace.md
ms.openlocfilehash: 3fa80fc69679346e3462a96340f4af9fc6a251d5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426368"
---
# <span data-ttu-id="ded3f-101">Get-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="ded3f-101">Get-AzWvdWorkspace</span></span>

## <span data-ttu-id="ded3f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ded3f-102">SYNOPSIS</span></span>
<span data-ttu-id="ded3f-103">Skaffa en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="ded3f-103">Get a workspace.</span></span>

## <span data-ttu-id="ded3f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ded3f-104">SYNTAX</span></span>

### <span data-ttu-id="ded3f-105">List1 (standard)</span><span class="sxs-lookup"><span data-stu-id="ded3f-105">List1 (Default)</span></span>
```
Get-AzWvdWorkspace [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ded3f-106">Lära</span><span class="sxs-lookup"><span data-stu-id="ded3f-106">Get</span></span>
```
Get-AzWvdWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ded3f-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ded3f-107">GetViaIdentity</span></span>
```
Get-AzWvdWorkspace -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="ded3f-108">Förteckning</span><span class="sxs-lookup"><span data-stu-id="ded3f-108">List</span></span>
```
Get-AzWvdWorkspace -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="ded3f-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ded3f-109">DESCRIPTION</span></span>
<span data-ttu-id="ded3f-110">Skaffa en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="ded3f-110">Get a workspace.</span></span>

## <span data-ttu-id="ded3f-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ded3f-111">EXAMPLES</span></span>

### <span data-ttu-id="ded3f-112">Exempel 1: Hämta en Windows Virtual Desktop-arbetsyta med namn</span><span class="sxs-lookup"><span data-stu-id="ded3f-112">Example 1: Get a Windows Virtual Desktop Workspace by name</span></span>
```powershell
PS C:\> Get-AzWvdWorkspace -ResourceGroupName ResourceGroupName -Name WorkspaceName

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="ded3f-113">Det här kommandot får en Windows-arbetsyta för virtuella skriv bord i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="ded3f-113">This command gets a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

### <span data-ttu-id="ded3f-114">Exempel 2: lista arbets ytor för virtuella skriv bord i Windows</span><span class="sxs-lookup"><span data-stu-id="ded3f-114">Example 2: List Windows Virtual Desktop Workspaces</span></span>
```powershell
PS C:\> Get-AzWvdWorkspace -ResourceGroupName ResourceGroupName

Location   Name           Type
--------   ----           ----
eastus     WorkspaceName1 Microsoft.DesktopVirtualization/workspaces
eastus     WorkspaceName2 Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="ded3f-115">Det här kommandot listar arbets ytor för Windows virtuella skriv bord i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="ded3f-115">This command lists a Windows Virtual Desktop Workspaces in a Resource Group.</span></span>

## <span data-ttu-id="ded3f-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ded3f-116">PARAMETERS</span></span>

### <span data-ttu-id="ded3f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ded3f-117">-DefaultProfile</span></span>
<span data-ttu-id="ded3f-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ded3f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ded3f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ded3f-119">-InputObject</span></span>
<span data-ttu-id="ded3f-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="ded3f-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ded3f-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="ded3f-121">-Name</span></span>
<span data-ttu-id="ded3f-122">Arbets ytans namn</span><span class="sxs-lookup"><span data-stu-id="ded3f-122">The name of the workspace</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ded3f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ded3f-123">-ResourceGroupName</span></span>
<span data-ttu-id="ded3f-124">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ded3f-124">The name of the resource group.</span></span>
<span data-ttu-id="ded3f-125">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="ded3f-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="ded3f-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ded3f-126">-SubscriptionId</span></span>
<span data-ttu-id="ded3f-127">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="ded3f-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="ded3f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ded3f-128">CommonParameters</span></span>
<span data-ttu-id="ded3f-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ded3f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ded3f-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ded3f-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ded3f-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ded3f-131">INPUTS</span></span>

### <span data-ttu-id="ded3f-132">Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="ded3f-132">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="ded3f-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ded3f-133">OUTPUTS</span></span>

### <span data-ttu-id="ded3f-134">Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. Api20201102Preview. IWorkspace</span><span class="sxs-lookup"><span data-stu-id="ded3f-134">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IWorkspace</span></span>

## <span data-ttu-id="ded3f-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ded3f-135">NOTES</span></span>

<span data-ttu-id="ded3f-136">ALIAS</span><span class="sxs-lookup"><span data-stu-id="ded3f-136">ALIASES</span></span>

<span data-ttu-id="ded3f-137">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="ded3f-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ded3f-138">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="ded3f-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ded3f-139">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ded3f-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ded3f-140">INPUTOBJECT <IDesktopVirtualizationIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="ded3f-140">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ded3f-141">`[ApplicationGroupName <String>]`: Namnet på program gruppen</span><span class="sxs-lookup"><span data-stu-id="ded3f-141">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="ded3f-142">`[ApplicationName <String>]`: Namnet på programmet i den angivna program gruppen</span><span class="sxs-lookup"><span data-stu-id="ded3f-142">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="ded3f-143">`[DesktopName <String>]`: Namnet på Skriv bordet i angiven Skriv bords grupp</span><span class="sxs-lookup"><span data-stu-id="ded3f-143">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="ded3f-144">`[HostPoolName <String>]`: Namnet på den värdbaserade poolen i den angivna resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="ded3f-144">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="ded3f-145">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="ded3f-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ded3f-146">`[MsixPackageFullName <String>]`: Det versions specifika paketet fullständigt namn för MSIX paketet i angivet hostpool</span><span class="sxs-lookup"><span data-stu-id="ded3f-146">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="ded3f-147">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ded3f-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="ded3f-148">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="ded3f-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="ded3f-149">`[SessionHostName <String>]`: Namnet på sessions värden i den angivna poolen</span><span class="sxs-lookup"><span data-stu-id="ded3f-149">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="ded3f-150">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="ded3f-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="ded3f-151">`[UserSessionId <String>]`: Namnet på användarsessionen inom den angivna värd</span><span class="sxs-lookup"><span data-stu-id="ded3f-151">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="ded3f-152">`[WorkspaceName <String>]`: Arbets ytans namn</span><span class="sxs-lookup"><span data-stu-id="ded3f-152">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="ded3f-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ded3f-153">RELATED LINKS</span></span>

