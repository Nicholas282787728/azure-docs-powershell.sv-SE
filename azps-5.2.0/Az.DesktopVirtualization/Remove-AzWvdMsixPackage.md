---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdMsixPackage.md
ms.openlocfilehash: 45e2c822bc21acfe69296f8d784a3a707dc1797f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98390576"
---
# <span data-ttu-id="22498-101">Remove-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="22498-101">Remove-AzWvdMsixPackage</span></span>

## <span data-ttu-id="22498-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="22498-102">SYNOPSIS</span></span>
<span data-ttu-id="22498-103">Ta bort ett MSIX-paket.</span><span class="sxs-lookup"><span data-stu-id="22498-103">Remove an MSIX Package.</span></span>

## <span data-ttu-id="22498-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="22498-104">SYNTAX</span></span>

### <span data-ttu-id="22498-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="22498-105">Delete (Default)</span></span>
```
Remove-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="22498-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="22498-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdMsixPackage -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="22498-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="22498-107">DESCRIPTION</span></span>
<span data-ttu-id="22498-108">Ta bort ett MSIX-paket.</span><span class="sxs-lookup"><span data-stu-id="22498-108">Remove an MSIX Package.</span></span>

## <span data-ttu-id="22498-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="22498-109">EXAMPLES</span></span>

### <span data-ttu-id="22498-110">Exempel 1: ta bort MSIX-paketet efter paket fullständigt namn</span><span class="sxs-lookup"><span data-stu-id="22498-110">Example 1: Delete MSIX Package by Package Full Name</span></span>
```powershell
PS C:\> Remove-AzWvdMsixPackage -HostPoolName HostPoolName -ResourceGroupName ResourceGroupName -SubscriptionId SubscriptionId -FullName PackageFullName
```

<span data-ttu-id="22498-111">Det här kommandot tar bort ett MSIX-paket i en HostPool</span><span class="sxs-lookup"><span data-stu-id="22498-111">This command deletes a MSIX Package in a HostPool</span></span>

## <span data-ttu-id="22498-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="22498-112">PARAMETERS</span></span>

### <span data-ttu-id="22498-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22498-113">-DefaultProfile</span></span>
<span data-ttu-id="22498-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="22498-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22498-115">-FullName</span><span class="sxs-lookup"><span data-stu-id="22498-115">-FullName</span></span>
<span data-ttu-id="22498-116">Det versions specifika paketet fullständigt namn för MSIX paketet i angivet hostpool</span><span class="sxs-lookup"><span data-stu-id="22498-116">The version specific package full name of the MSIX package within specified hostpool</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: MsixPackageFullName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22498-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="22498-117">-HostPoolName</span></span>
<span data-ttu-id="22498-118">Namnet på den värdbaserade adresspoolen i den angivna resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="22498-118">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22498-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="22498-119">-InputObject</span></span>
<span data-ttu-id="22498-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="22498-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="22498-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="22498-121">-PassThru</span></span>
<span data-ttu-id="22498-122">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="22498-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="22498-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22498-123">-ResourceGroupName</span></span>
<span data-ttu-id="22498-124">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="22498-124">The name of the resource group.</span></span>
<span data-ttu-id="22498-125">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="22498-125">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22498-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="22498-126">-SubscriptionId</span></span>
<span data-ttu-id="22498-127">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="22498-127">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22498-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="22498-128">-Confirm</span></span>
<span data-ttu-id="22498-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="22498-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22498-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22498-130">-WhatIf</span></span>
<span data-ttu-id="22498-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="22498-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22498-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="22498-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22498-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22498-133">CommonParameters</span></span>
<span data-ttu-id="22498-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22498-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22498-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="22498-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22498-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="22498-136">INPUTS</span></span>

### <span data-ttu-id="22498-137">Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="22498-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="22498-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="22498-138">OUTPUTS</span></span>

### <span data-ttu-id="22498-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="22498-139">System.Boolean</span></span>

## <span data-ttu-id="22498-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="22498-140">NOTES</span></span>

<span data-ttu-id="22498-141">ALIAS</span><span class="sxs-lookup"><span data-stu-id="22498-141">ALIASES</span></span>

<span data-ttu-id="22498-142">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="22498-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="22498-143">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="22498-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="22498-144">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="22498-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="22498-145">INPUTOBJECT <IDesktopVirtualizationIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="22498-145">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="22498-146">`[ApplicationGroupName <String>]`: Namnet på program gruppen</span><span class="sxs-lookup"><span data-stu-id="22498-146">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="22498-147">`[ApplicationName <String>]`: Namnet på programmet i den angivna program gruppen</span><span class="sxs-lookup"><span data-stu-id="22498-147">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="22498-148">`[DesktopName <String>]`: Namnet på Skriv bordet i angiven Skriv bords grupp</span><span class="sxs-lookup"><span data-stu-id="22498-148">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="22498-149">`[HostPoolName <String>]`: Namnet på den värdbaserade poolen i den angivna resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="22498-149">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="22498-150">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="22498-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="22498-151">`[MsixPackageFullName <String>]`: Det versions specifika paketet fullständigt namn för MSIX paketet i angivet hostpool</span><span class="sxs-lookup"><span data-stu-id="22498-151">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="22498-152">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="22498-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="22498-153">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="22498-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="22498-154">`[SessionHostName <String>]`: Namnet på sessions värden i den angivna poolen</span><span class="sxs-lookup"><span data-stu-id="22498-154">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="22498-155">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="22498-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="22498-156">`[UserSessionId <String>]`: Namnet på användarsessionen inom den angivna värd</span><span class="sxs-lookup"><span data-stu-id="22498-156">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="22498-157">`[WorkspaceName <String>]`: Arbets ytans namn</span><span class="sxs-lookup"><span data-stu-id="22498-157">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="22498-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="22498-158">RELATED LINKS</span></span>

