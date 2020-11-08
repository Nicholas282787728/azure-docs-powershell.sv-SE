---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvddesktop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdDesktop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdDesktop.md
ms.openlocfilehash: 72075a00cab24d9e7ac82814b2f1e644d90d74c9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102901"
---
# <span data-ttu-id="39c63-101">Get-AzWvdDesktop</span><span class="sxs-lookup"><span data-stu-id="39c63-101">Get-AzWvdDesktop</span></span>

## <span data-ttu-id="39c63-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="39c63-102">SYNOPSIS</span></span>
<span data-ttu-id="39c63-103">Få ett skriv bord.</span><span class="sxs-lookup"><span data-stu-id="39c63-103">Get a desktop.</span></span>

## <span data-ttu-id="39c63-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="39c63-104">SYNTAX</span></span>

### <span data-ttu-id="39c63-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="39c63-105">List (Default)</span></span>
```
Get-AzWvdDesktop -ApplicationGroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="39c63-106">Lära</span><span class="sxs-lookup"><span data-stu-id="39c63-106">Get</span></span>
```
Get-AzWvdDesktop -ApplicationGroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="39c63-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="39c63-107">GetViaIdentity</span></span>
```
Get-AzWvdDesktop -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="39c63-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="39c63-108">DESCRIPTION</span></span>
<span data-ttu-id="39c63-109">Få ett skriv bord.</span><span class="sxs-lookup"><span data-stu-id="39c63-109">Get a desktop.</span></span>

## <span data-ttu-id="39c63-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="39c63-110">EXAMPLES</span></span>

### <span data-ttu-id="39c63-111">Exempel 1: skaffa ett virtuellt skriv bord i Windows med namn</span><span class="sxs-lookup"><span data-stu-id="39c63-111">Example 1: Get a Windows Virtual Desktop Desktop by name</span></span>
```powershell
PS C:\> Get-AzWvdDesktop -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName -Name DesktopName

Name                             Type
----                             ----
ApplicationGroupName/DesktopName Microsoft.DesktopVirtualization/applicationgroups/desktops
```

<span data-ttu-id="39c63-112">Det här kommandot får ett virtuellt skriv bord i Windows i en applicaton-grupp.</span><span class="sxs-lookup"><span data-stu-id="39c63-112">This command gets a Windows Virtual Desktop Desktop in an applicaton Group.</span></span>

### <span data-ttu-id="39c63-113">Exempel 2: Visa en lista över virtuella skriv bord i Windows</span><span class="sxs-lookup"><span data-stu-id="39c63-113">Example 2: List Windows Virtual Desktop Desktops</span></span>
```powershell
PS C:\> Get-AzWvdDesktop -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                             Type
----                             ----
ApplicationGroupName/DesktopName Microsoft.DesktopVirtualization/applicationgroups/desktops
```

<span data-ttu-id="39c63-114">Det här kommandot listsWindows virtuella Skriv bords datorer i en applicaton-grupp.</span><span class="sxs-lookup"><span data-stu-id="39c63-114">This command listsWindows Virtual Desktop Desktops in an applicaton Group.</span></span>

## <span data-ttu-id="39c63-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="39c63-115">PARAMETERS</span></span>

### <span data-ttu-id="39c63-116">-ApplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="39c63-116">-ApplicationGroupName</span></span>
<span data-ttu-id="39c63-117">Namnet på program gruppen</span><span class="sxs-lookup"><span data-stu-id="39c63-117">The name of the application group</span></span>

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

### <span data-ttu-id="39c63-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39c63-118">-DefaultProfile</span></span>
<span data-ttu-id="39c63-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="39c63-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39c63-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="39c63-120">-InputObject</span></span>
<span data-ttu-id="39c63-121">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="39c63-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="39c63-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="39c63-122">-Name</span></span>
<span data-ttu-id="39c63-123">Namnet på Skriv bordet i angiven Skriv bords grupp</span><span class="sxs-lookup"><span data-stu-id="39c63-123">The name of the desktop within the specified desktop group</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DesktopName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39c63-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39c63-124">-ResourceGroupName</span></span>
<span data-ttu-id="39c63-125">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="39c63-125">The name of the resource group.</span></span>
<span data-ttu-id="39c63-126">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="39c63-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="39c63-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="39c63-127">-SubscriptionId</span></span>
<span data-ttu-id="39c63-128">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="39c63-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="39c63-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39c63-129">CommonParameters</span></span>
<span data-ttu-id="39c63-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39c63-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39c63-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="39c63-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39c63-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="39c63-132">INPUTS</span></span>

### <span data-ttu-id="39c63-133">Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="39c63-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="39c63-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="39c63-134">OUTPUTS</span></span>

### <span data-ttu-id="39c63-135">Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. Api20191210Preview. IDesktop</span><span class="sxs-lookup"><span data-stu-id="39c63-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IDesktop</span></span>

### <span data-ttu-id="39c63-136">Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. Api20191210Preview. IDesktopList</span><span class="sxs-lookup"><span data-stu-id="39c63-136">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IDesktopList</span></span>

## <span data-ttu-id="39c63-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="39c63-137">NOTES</span></span>

<span data-ttu-id="39c63-138">ALIAS</span><span class="sxs-lookup"><span data-stu-id="39c63-138">ALIASES</span></span>

<span data-ttu-id="39c63-139">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="39c63-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="39c63-140">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="39c63-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="39c63-141">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="39c63-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="39c63-142">INPUTOBJECT <IDesktopVirtualizationIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="39c63-142">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="39c63-143">`[ApplicationGroupName <String>]`: Namnet på program gruppen</span><span class="sxs-lookup"><span data-stu-id="39c63-143">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="39c63-144">`[ApplicationName <String>]`: Namnet på programmet i den angivna program gruppen</span><span class="sxs-lookup"><span data-stu-id="39c63-144">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="39c63-145">`[DesktopName <String>]`: Namnet på Skriv bordet i angiven Skriv bords grupp</span><span class="sxs-lookup"><span data-stu-id="39c63-145">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="39c63-146">`[HostPoolName <String>]`: Namnet på den värdbaserade poolen i den angivna resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="39c63-146">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="39c63-147">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="39c63-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="39c63-148">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="39c63-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="39c63-149">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="39c63-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="39c63-150">`[SessionHostName <String>]`: Namnet på sessions värden i den angivna poolen</span><span class="sxs-lookup"><span data-stu-id="39c63-150">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="39c63-151">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="39c63-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="39c63-152">`[UserSessionId <String>]`: Namnet på användarsessionen inom den angivna värd</span><span class="sxs-lookup"><span data-stu-id="39c63-152">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="39c63-153">`[WorkspaceName <String>]`: Arbets ytans namn</span><span class="sxs-lookup"><span data-stu-id="39c63-153">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="39c63-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="39c63-154">RELATED LINKS</span></span>

