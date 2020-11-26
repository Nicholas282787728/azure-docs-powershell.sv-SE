---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplication.md
ms.openlocfilehash: e75a9db71a4b20ed87d4e9564597af758af16304
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320071"
---
# <span data-ttu-id="8d2bb-101">Get-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="8d2bb-101">Get-AzWvdApplication</span></span>

## <span data-ttu-id="8d2bb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8d2bb-102">SYNOPSIS</span></span>
<span data-ttu-id="8d2bb-103">Skaffa ett program.</span><span class="sxs-lookup"><span data-stu-id="8d2bb-103">Get an application.</span></span>

## <span data-ttu-id="8d2bb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8d2bb-104">SYNTAX</span></span>

### <span data-ttu-id="8d2bb-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="8d2bb-105">List (Default)</span></span>
```
Get-AzWvdApplication -GroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8d2bb-106">Lära</span><span class="sxs-lookup"><span data-stu-id="8d2bb-106">Get</span></span>
```
Get-AzWvdApplication -GroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8d2bb-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8d2bb-107">GetViaIdentity</span></span>
```
Get-AzWvdApplication -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="8d2bb-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8d2bb-108">DESCRIPTION</span></span>
<span data-ttu-id="8d2bb-109">Skaffa ett program.</span><span class="sxs-lookup"><span data-stu-id="8d2bb-109">Get an application.</span></span>

## <span data-ttu-id="8d2bb-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8d2bb-110">EXAMPLES</span></span>

### <span data-ttu-id="8d2bb-111">Exempel 1: skaffa ett virtuellt Skriv bords program för Windows med namn</span><span class="sxs-lookup"><span data-stu-id="8d2bb-111">Example 1: Get a Windows Virtual Desktop Application by name</span></span>
```powershell
PS C:\> Get-AzWvdApplication -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName -Name ApplicationName

Name                                 Type
----                                 ----
ApplicationGroupName/ApplicationName Microsoft.DesktopVirtualization/applicationgroups/applications
```

<span data-ttu-id="8d2bb-112">Det här kommandot får ett Windows-program för virtuella skriv bord i en applicaton-grupp.</span><span class="sxs-lookup"><span data-stu-id="8d2bb-112">This command gets a Windows Virtual Desktop Application in an applicaton Group.</span></span>

### <span data-ttu-id="8d2bb-113">Exempel 2: Visa en lista över virtuella dator program i Windows</span><span class="sxs-lookup"><span data-stu-id="8d2bb-113">Example 2: List Windows Virtual Desktop Applications</span></span>
```powershell
PS C:\> Get-AzWvdApplication -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                                 Type
----                                 ----
ApplicationGroupName/ApplicationName1 Microsoft.DesktopVirtualization/applicationgroups/applications
ApplicationGroupName/ApplicationName2 Microsoft.DesktopVirtualization/applicationgroups/applications
```

<span data-ttu-id="8d2bb-114">Det här kommandot visar program för virtuella skriv bord i Windows i en applicaton-grupp.</span><span class="sxs-lookup"><span data-stu-id="8d2bb-114">This command Lists Windows Virtual Desktop Applications in an applicaton Group.</span></span>

## <span data-ttu-id="8d2bb-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8d2bb-115">PARAMETERS</span></span>

### <span data-ttu-id="8d2bb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d2bb-116">-DefaultProfile</span></span>
<span data-ttu-id="8d2bb-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8d2bb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d2bb-118">-Grupp namn</span><span class="sxs-lookup"><span data-stu-id="8d2bb-118">-GroupName</span></span>
<span data-ttu-id="8d2bb-119">Namnet på program gruppen</span><span class="sxs-lookup"><span data-stu-id="8d2bb-119">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d2bb-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8d2bb-120">-InputObject</span></span>
<span data-ttu-id="8d2bb-121">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="8d2bb-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8d2bb-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="8d2bb-122">-Name</span></span>
<span data-ttu-id="8d2bb-123">Namnet på programmet i den angivna program gruppen</span><span class="sxs-lookup"><span data-stu-id="8d2bb-123">The name of the application within the specified application group</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ApplicationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d2bb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d2bb-124">-ResourceGroupName</span></span>
<span data-ttu-id="8d2bb-125">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="8d2bb-125">The name of the resource group.</span></span>
<span data-ttu-id="8d2bb-126">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="8d2bb-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="8d2bb-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8d2bb-127">-SubscriptionId</span></span>
<span data-ttu-id="8d2bb-128">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="8d2bb-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="8d2bb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d2bb-129">CommonParameters</span></span>
<span data-ttu-id="8d2bb-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d2bb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d2bb-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8d2bb-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d2bb-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8d2bb-132">INPUTS</span></span>

### <span data-ttu-id="8d2bb-133">Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="8d2bb-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="8d2bb-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8d2bb-134">OUTPUTS</span></span>

### <span data-ttu-id="8d2bb-135">Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. Api20191210Preview. IApplication</span><span class="sxs-lookup"><span data-stu-id="8d2bb-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IApplication</span></span>

## <span data-ttu-id="8d2bb-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8d2bb-136">NOTES</span></span>

<span data-ttu-id="8d2bb-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="8d2bb-137">ALIASES</span></span>

<span data-ttu-id="8d2bb-138">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="8d2bb-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8d2bb-139">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="8d2bb-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8d2bb-140">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8d2bb-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8d2bb-141">INPUTOBJECT <IDesktopVirtualizationIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="8d2bb-141">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8d2bb-142">`[ApplicationGroupName <String>]`: Namnet på program gruppen</span><span class="sxs-lookup"><span data-stu-id="8d2bb-142">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="8d2bb-143">`[ApplicationName <String>]`: Namnet på programmet i den angivna program gruppen</span><span class="sxs-lookup"><span data-stu-id="8d2bb-143">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="8d2bb-144">`[DesktopName <String>]`: Namnet på Skriv bordet i angiven Skriv bords grupp</span><span class="sxs-lookup"><span data-stu-id="8d2bb-144">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="8d2bb-145">`[HostPoolName <String>]`: Namnet på den värdbaserade poolen i den angivna resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="8d2bb-145">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="8d2bb-146">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="8d2bb-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8d2bb-147">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="8d2bb-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="8d2bb-148">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="8d2bb-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="8d2bb-149">`[SessionHostName <String>]`: Namnet på sessions värden i den angivna poolen</span><span class="sxs-lookup"><span data-stu-id="8d2bb-149">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="8d2bb-150">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="8d2bb-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="8d2bb-151">`[UserSessionId <String>]`: Namnet på användarsessionen inom den angivna värd</span><span class="sxs-lookup"><span data-stu-id="8d2bb-151">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="8d2bb-152">`[WorkspaceName <String>]`: Arbets ytans namn</span><span class="sxs-lookup"><span data-stu-id="8d2bb-152">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="8d2bb-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8d2bb-153">RELATED LINKS</span></span>
