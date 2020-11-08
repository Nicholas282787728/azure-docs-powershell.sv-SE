---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/disconnect-azwvdusersession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Disconnect-AzWvdUserSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Disconnect-AzWvdUserSession.md
ms.openlocfilehash: f4156fdc52ffaf01caad49517229ebf63d960fc6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260523"
---
# <span data-ttu-id="6b6f8-101">Disconnect-AzWvdUserSession</span><span class="sxs-lookup"><span data-stu-id="6b6f8-101">Disconnect-AzWvdUserSession</span></span>

## <span data-ttu-id="6b6f8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6b6f8-102">SYNOPSIS</span></span>
<span data-ttu-id="6b6f8-103">Koppla bort en userSession.</span><span class="sxs-lookup"><span data-stu-id="6b6f8-103">Disconnect a userSession.</span></span>

## <span data-ttu-id="6b6f8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6b6f8-104">SYNTAX</span></span>

### <span data-ttu-id="6b6f8-105">Koppla från (standard)</span><span class="sxs-lookup"><span data-stu-id="6b6f8-105">Disconnect (Default)</span></span>
```
Disconnect-AzWvdUserSession -HostPoolName <String> -Id <String> -ResourceGroupName <String>
 -SessionHostName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6b6f8-106">DisconnectViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6b6f8-106">DisconnectViaIdentity</span></span>
```
Disconnect-AzWvdUserSession -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6b6f8-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6b6f8-107">DESCRIPTION</span></span>
<span data-ttu-id="6b6f8-108">Koppla bort en userSession.</span><span class="sxs-lookup"><span data-stu-id="6b6f8-108">Disconnect a userSession.</span></span>

## <span data-ttu-id="6b6f8-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6b6f8-109">EXAMPLES</span></span>

### <span data-ttu-id="6b6f8-110">Exempel 1: koppla bort en virtuell Windows-UserSession efter namn</span><span class="sxs-lookup"><span data-stu-id="6b6f8-110">Example 1: Disconnect a Windows Virtual Desktop UserSession by name</span></span>
```powershell
PS C:\> Disconnect-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName -Id 2
```

<span data-ttu-id="6b6f8-111">Med det här kommandot kopplas en UserSession för Windows till en session-värd.</span><span class="sxs-lookup"><span data-stu-id="6b6f8-111">This command disconnects a Windows Virtual Desktop UserSession in a Session Host.</span></span>

## <span data-ttu-id="6b6f8-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6b6f8-112">PARAMETERS</span></span>

### <span data-ttu-id="6b6f8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b6f8-113">-DefaultProfile</span></span>
<span data-ttu-id="6b6f8-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6b6f8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b6f8-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="6b6f8-115">-HostPoolName</span></span>
<span data-ttu-id="6b6f8-116">Namnet på den värdbaserade adresspoolen i den angivna resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="6b6f8-116">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: Disconnect
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b6f8-117">-ID</span><span class="sxs-lookup"><span data-stu-id="6b6f8-117">-Id</span></span>
<span data-ttu-id="6b6f8-118">Namnet på användarsessionen inom den angivna sessionsvärdservern</span><span class="sxs-lookup"><span data-stu-id="6b6f8-118">The name of the user session within the specified session host</span></span>

```yaml
Type: System.String
Parameter Sets: Disconnect
Aliases: UserSessionId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b6f8-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6b6f8-119">-InputObject</span></span>
<span data-ttu-id="6b6f8-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="6b6f8-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: DisconnectViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b6f8-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6b6f8-121">-PassThru</span></span>
<span data-ttu-id="6b6f8-122">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="6b6f8-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="6b6f8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b6f8-123">-ResourceGroupName</span></span>
<span data-ttu-id="6b6f8-124">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="6b6f8-124">The name of the resource group.</span></span>
<span data-ttu-id="6b6f8-125">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="6b6f8-125">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Disconnect
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b6f8-126">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="6b6f8-126">-SessionHostName</span></span>
<span data-ttu-id="6b6f8-127">Namnet på sessions värden i den angivna poolen</span><span class="sxs-lookup"><span data-stu-id="6b6f8-127">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: Disconnect
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b6f8-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6b6f8-128">-SubscriptionId</span></span>
<span data-ttu-id="6b6f8-129">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="6b6f8-129">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Disconnect
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b6f8-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6b6f8-130">-Confirm</span></span>
<span data-ttu-id="6b6f8-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6b6f8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b6f8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b6f8-132">-WhatIf</span></span>
<span data-ttu-id="6b6f8-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6b6f8-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b6f8-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6b6f8-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b6f8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b6f8-135">CommonParameters</span></span>
<span data-ttu-id="6b6f8-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b6f8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b6f8-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6b6f8-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b6f8-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6b6f8-138">INPUTS</span></span>

### <span data-ttu-id="6b6f8-139">Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="6b6f8-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="6b6f8-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6b6f8-140">OUTPUTS</span></span>

### <span data-ttu-id="6b6f8-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6b6f8-141">System.Boolean</span></span>

## <span data-ttu-id="6b6f8-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6b6f8-142">NOTES</span></span>

<span data-ttu-id="6b6f8-143">ALIAS</span><span class="sxs-lookup"><span data-stu-id="6b6f8-143">ALIASES</span></span>

<span data-ttu-id="6b6f8-144">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="6b6f8-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6b6f8-145">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="6b6f8-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6b6f8-146">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6b6f8-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6b6f8-147">INPUTOBJECT <IDesktopVirtualizationIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="6b6f8-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6b6f8-148">`[ApplicationGroupName <String>]`: Namnet på program gruppen</span><span class="sxs-lookup"><span data-stu-id="6b6f8-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="6b6f8-149">`[ApplicationName <String>]`: Namnet på programmet i den angivna program gruppen</span><span class="sxs-lookup"><span data-stu-id="6b6f8-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="6b6f8-150">`[DesktopName <String>]`: Namnet på Skriv bordet i angiven Skriv bords grupp</span><span class="sxs-lookup"><span data-stu-id="6b6f8-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="6b6f8-151">`[HostPoolName <String>]`: Namnet på den värdbaserade poolen i den angivna resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="6b6f8-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="6b6f8-152">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="6b6f8-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6b6f8-153">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="6b6f8-153">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="6b6f8-154">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="6b6f8-154">The name is case insensitive.</span></span>
  - <span data-ttu-id="6b6f8-155">`[SessionHostName <String>]`: Namnet på sessions värden i den angivna poolen</span><span class="sxs-lookup"><span data-stu-id="6b6f8-155">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="6b6f8-156">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="6b6f8-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="6b6f8-157">`[UserSessionId <String>]`: Namnet på användarsessionen inom den angivna värd</span><span class="sxs-lookup"><span data-stu-id="6b6f8-157">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="6b6f8-158">`[WorkspaceName <String>]`: Arbets ytans namn</span><span class="sxs-lookup"><span data-stu-id="6b6f8-158">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="6b6f8-159">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6b6f8-159">RELATED LINKS</span></span>

