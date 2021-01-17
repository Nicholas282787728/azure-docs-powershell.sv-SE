---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/send-azwvdusersessionmessage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Send-AzWvdUserSessionMessage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Send-AzWvdUserSessionMessage.md
ms.openlocfilehash: 5b5e5ba314bee8d6260985c65f46d372cce94258
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98396739"
---
# <span data-ttu-id="5ee52-101">Send-AzWvdUserSessionMessage</span><span class="sxs-lookup"><span data-stu-id="5ee52-101">Send-AzWvdUserSessionMessage</span></span>

## <span data-ttu-id="5ee52-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5ee52-102">SYNOPSIS</span></span>
<span data-ttu-id="5ee52-103">Skicka ett meddelande till en användare.</span><span class="sxs-lookup"><span data-stu-id="5ee52-103">Send a message to a user.</span></span>

## <span data-ttu-id="5ee52-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5ee52-104">SYNTAX</span></span>

### <span data-ttu-id="5ee52-105">SendExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="5ee52-105">SendExpanded (Default)</span></span>
```
Send-AzWvdUserSessionMessage -HostPoolName <String> -ResourceGroupName <String> -SessionHostName <String>
 -UserSessionId <String> [-SubscriptionId <String>] [-MessageBody <String>] [-MessageTitle <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5ee52-106">SendViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="5ee52-106">SendViaIdentityExpanded</span></span>
```
Send-AzWvdUserSessionMessage -InputObject <IDesktopVirtualizationIdentity> [-MessageBody <String>]
 [-MessageTitle <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5ee52-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5ee52-107">DESCRIPTION</span></span>
<span data-ttu-id="5ee52-108">Skicka ett meddelande till en användare.</span><span class="sxs-lookup"><span data-stu-id="5ee52-108">Send a message to a user.</span></span>

## <span data-ttu-id="5ee52-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5ee52-109">EXAMPLES</span></span>

### <span data-ttu-id="5ee52-110">Exempel 1: Skicka ett meddelande till UserSession</span><span class="sxs-lookup"><span data-stu-id="5ee52-110">Example 1: Send a message to UserSession</span></span>
```powershell
PS C:\> Send-AzWvdUserSessionMessage -ResourceGroupName ResourceGroupName `
                                     -HostPoolName HostPoolName `
                                     -SessionHostName SessionHostName `
                                     -UserSessionId 4 `
                                     -MessageBody 'Some Message' `
                                     -MessageTitle 'Some Title'
```

<span data-ttu-id="5ee52-111">Det här kommandot skickar ett meddelande till en UserSession.</span><span class="sxs-lookup"><span data-stu-id="5ee52-111">This command sends a message to a UserSession.</span></span>

## <span data-ttu-id="5ee52-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5ee52-112">PARAMETERS</span></span>

### <span data-ttu-id="5ee52-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ee52-113">-DefaultProfile</span></span>
<span data-ttu-id="5ee52-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5ee52-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ee52-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="5ee52-115">-HostPoolName</span></span>
<span data-ttu-id="5ee52-116">Namnet på den värdbaserade adresspoolen i den angivna resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="5ee52-116">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: SendExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ee52-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5ee52-117">-InputObject</span></span>
<span data-ttu-id="5ee52-118">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="5ee52-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: SendViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ee52-119">-MessageBody</span><span class="sxs-lookup"><span data-stu-id="5ee52-119">-MessageBody</span></span>
<span data-ttu-id="5ee52-120">Meddelande text.</span><span class="sxs-lookup"><span data-stu-id="5ee52-120">Body of message.</span></span>

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

### <span data-ttu-id="5ee52-121">-MessageTitle</span><span class="sxs-lookup"><span data-stu-id="5ee52-121">-MessageTitle</span></span>
<span data-ttu-id="5ee52-122">Meddelande rubrik.</span><span class="sxs-lookup"><span data-stu-id="5ee52-122">Title of message.</span></span>

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

### <span data-ttu-id="5ee52-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5ee52-123">-PassThru</span></span>
<span data-ttu-id="5ee52-124">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="5ee52-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="5ee52-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ee52-125">-ResourceGroupName</span></span>
<span data-ttu-id="5ee52-126">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="5ee52-126">The name of the resource group.</span></span>
<span data-ttu-id="5ee52-127">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="5ee52-127">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: SendExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ee52-128">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="5ee52-128">-SessionHostName</span></span>
<span data-ttu-id="5ee52-129">Namnet på sessions värden i den angivna poolen</span><span class="sxs-lookup"><span data-stu-id="5ee52-129">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: SendExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ee52-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5ee52-130">-SubscriptionId</span></span>
<span data-ttu-id="5ee52-131">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="5ee52-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: SendExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ee52-132">-UserSessionId</span><span class="sxs-lookup"><span data-stu-id="5ee52-132">-UserSessionId</span></span>
<span data-ttu-id="5ee52-133">Namnet på användarsessionen inom den angivna sessionsvärdservern</span><span class="sxs-lookup"><span data-stu-id="5ee52-133">The name of the user session within the specified session host</span></span>

```yaml
Type: System.String
Parameter Sets: SendExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ee52-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5ee52-134">-Confirm</span></span>
<span data-ttu-id="5ee52-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5ee52-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ee52-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ee52-136">-WhatIf</span></span>
<span data-ttu-id="5ee52-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5ee52-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ee52-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5ee52-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ee52-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ee52-139">CommonParameters</span></span>
<span data-ttu-id="5ee52-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ee52-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ee52-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5ee52-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ee52-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5ee52-142">INPUTS</span></span>

### <span data-ttu-id="5ee52-143">Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="5ee52-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="5ee52-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5ee52-144">OUTPUTS</span></span>

### <span data-ttu-id="5ee52-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5ee52-145">System.Boolean</span></span>

## <span data-ttu-id="5ee52-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5ee52-146">NOTES</span></span>

<span data-ttu-id="5ee52-147">ALIAS</span><span class="sxs-lookup"><span data-stu-id="5ee52-147">ALIASES</span></span>

<span data-ttu-id="5ee52-148">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="5ee52-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5ee52-149">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="5ee52-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5ee52-150">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5ee52-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5ee52-151">INPUTOBJECT <IDesktopVirtualizationIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="5ee52-151">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5ee52-152">`[ApplicationGroupName <String>]`: Namnet på program gruppen</span><span class="sxs-lookup"><span data-stu-id="5ee52-152">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="5ee52-153">`[ApplicationName <String>]`: Namnet på programmet i den angivna program gruppen</span><span class="sxs-lookup"><span data-stu-id="5ee52-153">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="5ee52-154">`[DesktopName <String>]`: Namnet på Skriv bordet i angiven Skriv bords grupp</span><span class="sxs-lookup"><span data-stu-id="5ee52-154">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="5ee52-155">`[HostPoolName <String>]`: Namnet på den värdbaserade poolen i den angivna resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="5ee52-155">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="5ee52-156">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="5ee52-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5ee52-157">`[MsixPackageFullName <String>]`: Det versions specifika paketet fullständigt namn för MSIX paketet i angivet hostpool</span><span class="sxs-lookup"><span data-stu-id="5ee52-157">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="5ee52-158">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="5ee52-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="5ee52-159">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="5ee52-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="5ee52-160">`[SessionHostName <String>]`: Namnet på sessions värden i den angivna poolen</span><span class="sxs-lookup"><span data-stu-id="5ee52-160">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="5ee52-161">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="5ee52-161">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="5ee52-162">`[UserSessionId <String>]`: Namnet på användarsessionen inom den angivna värd</span><span class="sxs-lookup"><span data-stu-id="5ee52-162">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="5ee52-163">`[WorkspaceName <String>]`: Arbets ytans namn</span><span class="sxs-lookup"><span data-stu-id="5ee52-163">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="5ee52-164">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5ee52-164">RELATED LINKS</span></span>

