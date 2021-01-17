---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdsessionhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdSessionHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdSessionHost.md
ms.openlocfilehash: cdb14bfe7992d29be17ff1a576dd3a6ca8bf09b6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98398496"
---
# <span data-ttu-id="d7d99-101">Update-AzWvdSessionHost</span><span class="sxs-lookup"><span data-stu-id="d7d99-101">Update-AzWvdSessionHost</span></span>

## <span data-ttu-id="d7d99-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d7d99-102">SYNOPSIS</span></span>
<span data-ttu-id="d7d99-103">Uppdatera en värd för en session.</span><span class="sxs-lookup"><span data-stu-id="d7d99-103">Update a session host.</span></span>

## <span data-ttu-id="d7d99-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d7d99-104">SYNTAX</span></span>

### <span data-ttu-id="d7d99-105">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="d7d99-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdSessionHost -HostPoolName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-AllowNewSession] [-AssignedUser <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d7d99-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d7d99-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdSessionHost -InputObject <IDesktopVirtualizationIdentity> [-AllowNewSession]
 [-AssignedUser <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d7d99-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d7d99-107">DESCRIPTION</span></span>
<span data-ttu-id="d7d99-108">Uppdatera en värd för en session.</span><span class="sxs-lookup"><span data-stu-id="d7d99-108">Update a session host.</span></span>

## <span data-ttu-id="d7d99-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d7d99-109">EXAMPLES</span></span>

### <span data-ttu-id="d7d99-110">Exempel 1: uppdatera en Windows Virtual Desktop-SessionHost efter namn</span><span class="sxs-lookup"><span data-stu-id="d7d99-110">Example 1: Update a Windows Virtual Desktop SessionHost by name</span></span>
```powershell
PS C:\> Update-AzWvdSessionHost -ResourceGroupName ResourceGroupName `
                            -HostPoolName HostPoolName `
                            -Name SessionHostName `
                            -AllowNewSession:$false

Name                                               Type
----                                               ----
HostPoolName/SessionHostName Microsoft.DesktopVirtualization/hostpools/sessionhosts
```

<span data-ttu-id="d7d99-111">Det här kommandot uppdaterar en Windows Virtual Desktop-SessionHost i en adresspool.</span><span class="sxs-lookup"><span data-stu-id="d7d99-111">This command updates a Windows Virtual Desktop SessionHost in a Host Pool.</span></span>

## <span data-ttu-id="d7d99-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d7d99-112">PARAMETERS</span></span>

### <span data-ttu-id="d7d99-113">-AllowNewSession</span><span class="sxs-lookup"><span data-stu-id="d7d99-113">-AllowNewSession</span></span>
<span data-ttu-id="d7d99-114">Tillåt en ny session.</span><span class="sxs-lookup"><span data-stu-id="d7d99-114">Allow a new session.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7d99-115">-AssignedUser</span><span class="sxs-lookup"><span data-stu-id="d7d99-115">-AssignedUser</span></span>
<span data-ttu-id="d7d99-116">Användare tilldelad SessionHost.</span><span class="sxs-lookup"><span data-stu-id="d7d99-116">User assigned to SessionHost.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7d99-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7d99-117">-DefaultProfile</span></span>
<span data-ttu-id="d7d99-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d7d99-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7d99-119">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="d7d99-119">-HostPoolName</span></span>
<span data-ttu-id="d7d99-120">Namnet på den värdbaserade adresspoolen i den angivna resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="d7d99-120">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7d99-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d7d99-121">-InputObject</span></span>
<span data-ttu-id="d7d99-122">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="d7d99-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7d99-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="d7d99-123">-Name</span></span>
<span data-ttu-id="d7d99-124">Namnet på sessions värden i den angivna poolen</span><span class="sxs-lookup"><span data-stu-id="d7d99-124">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: SessionHostName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7d99-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7d99-125">-ResourceGroupName</span></span>
<span data-ttu-id="d7d99-126">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="d7d99-126">The name of the resource group.</span></span>
<span data-ttu-id="d7d99-127">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="d7d99-127">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7d99-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d7d99-128">-SubscriptionId</span></span>
<span data-ttu-id="d7d99-129">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="d7d99-129">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7d99-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d7d99-130">-Confirm</span></span>
<span data-ttu-id="d7d99-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d7d99-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7d99-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7d99-132">-WhatIf</span></span>
<span data-ttu-id="d7d99-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d7d99-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7d99-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d7d99-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7d99-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7d99-135">CommonParameters</span></span>
<span data-ttu-id="d7d99-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7d99-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7d99-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d7d99-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7d99-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d7d99-138">INPUTS</span></span>

### <span data-ttu-id="d7d99-139">Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="d7d99-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="d7d99-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d7d99-140">OUTPUTS</span></span>

### <span data-ttu-id="d7d99-141">Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. Api20201019Preview. ISessionHost</span><span class="sxs-lookup"><span data-stu-id="d7d99-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.ISessionHost</span></span>

## <span data-ttu-id="d7d99-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d7d99-142">NOTES</span></span>

<span data-ttu-id="d7d99-143">ALIAS</span><span class="sxs-lookup"><span data-stu-id="d7d99-143">ALIASES</span></span>

<span data-ttu-id="d7d99-144">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="d7d99-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d7d99-145">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="d7d99-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d7d99-146">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d7d99-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d7d99-147">INPUTOBJECT <IDesktopVirtualizationIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="d7d99-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d7d99-148">`[ApplicationGroupName <String>]`: Namnet på program gruppen</span><span class="sxs-lookup"><span data-stu-id="d7d99-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="d7d99-149">`[ApplicationName <String>]`: Namnet på programmet i den angivna program gruppen</span><span class="sxs-lookup"><span data-stu-id="d7d99-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="d7d99-150">`[DesktopName <String>]`: Namnet på Skriv bordet i angiven Skriv bords grupp</span><span class="sxs-lookup"><span data-stu-id="d7d99-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="d7d99-151">`[HostPoolName <String>]`: Namnet på den värdbaserade poolen i den angivna resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="d7d99-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="d7d99-152">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="d7d99-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d7d99-153">`[MsixPackageFullName <String>]`: Det versions specifika paketet fullständigt namn för MSIX paketet i angivet hostpool</span><span class="sxs-lookup"><span data-stu-id="d7d99-153">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="d7d99-154">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="d7d99-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d7d99-155">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="d7d99-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="d7d99-156">`[SessionHostName <String>]`: Namnet på sessions värden i den angivna poolen</span><span class="sxs-lookup"><span data-stu-id="d7d99-156">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="d7d99-157">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="d7d99-157">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="d7d99-158">`[UserSessionId <String>]`: Namnet på användarsessionen inom den angivna värd</span><span class="sxs-lookup"><span data-stu-id="d7d99-158">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="d7d99-159">`[WorkspaceName <String>]`: Arbets ytans namn</span><span class="sxs-lookup"><span data-stu-id="d7d99-159">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="d7d99-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d7d99-160">RELATED LINKS</span></span>

