---
external help file: ''
Module Name: Az.WindowsIotServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.windowsiotservices/remove-azwindowsiotservicesdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Remove-AzWindowsIotServicesDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Remove-AzWindowsIotServicesDevice.md
ms.openlocfilehash: 265c0e68dd3f19afbefd8cf993e058f56e3ec9f3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522034"
---
# <span data-ttu-id="a3fe8-101">Remove-AzWindowsIotServicesDevice</span><span class="sxs-lookup"><span data-stu-id="a3fe8-101">Remove-AzWindowsIotServicesDevice</span></span>

## <span data-ttu-id="a3fe8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a3fe8-102">SYNOPSIS</span></span>
<span data-ttu-id="a3fe8-103">Ta bort en Windows IoT-enhet.</span><span class="sxs-lookup"><span data-stu-id="a3fe8-103">Delete a Windows IoT Device Service.</span></span>

## <span data-ttu-id="a3fe8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a3fe8-104">SYNTAX</span></span>

### <span data-ttu-id="a3fe8-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="a3fe8-105">Delete (Default)</span></span>
```
Remove-AzWindowsIotServicesDevice -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a3fe8-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a3fe8-106">DeleteViaIdentity</span></span>
```
Remove-AzWindowsIotServicesDevice -InputObject <IWindowsIotServicesIdentity> [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a3fe8-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a3fe8-107">DESCRIPTION</span></span>
<span data-ttu-id="a3fe8-108">Ta bort en Windows IoT-enhet.</span><span class="sxs-lookup"><span data-stu-id="a3fe8-108">Delete a Windows IoT Device Service.</span></span>

## <span data-ttu-id="a3fe8-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a3fe8-109">EXAMPLES</span></span>

### <span data-ttu-id="a3fe8-110">Exempel 1: ta bort en Windows IoT-tjänst utifrån namn</span><span class="sxs-lookup"><span data-stu-id="a3fe8-110">Example 1: Remove a Windows IoT services by name</span></span>
```powershell
PS C:\> Remove-AzWindowsIotServicesDevice -Name wsi-t03 -ResourceGroupName azure-rg-test

```

<span data-ttu-id="a3fe8-111">Detta kommando tar bort en Windows IoT-tjänst med namn.</span><span class="sxs-lookup"><span data-stu-id="a3fe8-111">This command removes a Windows IoT services by name.</span></span>

### <span data-ttu-id="a3fe8-112">Exempel 2: ta bort en Windows IoT-tjänst via pipeline</span><span class="sxs-lookup"><span data-stu-id="a3fe8-112">Example 2: Remove a Windows IoT services by pipeline</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice -ResourceGroupName azure-rg-test -Name wsi-t01 | Remove-AzWindowsIotServicesDevice


```

<span data-ttu-id="a3fe8-113">Det här kommandot tar bort en Windows IoT-tjänst via pipeline.</span><span class="sxs-lookup"><span data-stu-id="a3fe8-113">This command removes a Windows IoT services by pipeline.</span></span>

## <span data-ttu-id="a3fe8-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a3fe8-114">PARAMETERS</span></span>

### <span data-ttu-id="a3fe8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3fe8-115">-DefaultProfile</span></span>
<span data-ttu-id="a3fe8-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a3fe8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3fe8-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a3fe8-117">-InputObject</span></span>
<span data-ttu-id="a3fe8-118">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="a3fe8-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3fe8-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="a3fe8-119">-Name</span></span>
<span data-ttu-id="a3fe8-120">Namnet på Windows IoT Device-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="a3fe8-120">The name of the Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="a3fe8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3fe8-121">-ResourceGroupName</span></span>
<span data-ttu-id="a3fe8-122">Namnet på resurs gruppen som innehåller Windows IoT-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="a3fe8-122">The name of the resource group that contains the Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="a3fe8-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a3fe8-123">-SubscriptionId</span></span>
<span data-ttu-id="a3fe8-124">Prenumerations-ID.</span><span class="sxs-lookup"><span data-stu-id="a3fe8-124">The subscription identifier.</span></span>

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

### <span data-ttu-id="a3fe8-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a3fe8-125">-Confirm</span></span>
<span data-ttu-id="a3fe8-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a3fe8-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3fe8-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3fe8-127">-WhatIf</span></span>
<span data-ttu-id="a3fe8-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a3fe8-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3fe8-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a3fe8-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3fe8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3fe8-130">CommonParameters</span></span>
<span data-ttu-id="a3fe8-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3fe8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3fe8-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a3fe8-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3fe8-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a3fe8-133">INPUTS</span></span>

### <span data-ttu-id="a3fe8-134">Microsoft. Azure. PowerShell. cmdletar. WindowsIotServices. Models. IWindowsIotServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="a3fe8-134">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span></span>

## <span data-ttu-id="a3fe8-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a3fe8-135">OUTPUTS</span></span>

### <span data-ttu-id="a3fe8-136">Microsoft. Azure. PowerShell. cmdletar. WindowsIotServices. Models. Api20190601. IDeviceService</span><span class="sxs-lookup"><span data-stu-id="a3fe8-136">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span></span>

## <span data-ttu-id="a3fe8-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a3fe8-137">NOTES</span></span>

<span data-ttu-id="a3fe8-138">ALIAS</span><span class="sxs-lookup"><span data-stu-id="a3fe8-138">ALIASES</span></span>

<span data-ttu-id="a3fe8-139">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="a3fe8-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a3fe8-140">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="a3fe8-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a3fe8-141">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a3fe8-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a3fe8-142">INPUTOBJECT <IWindowsIotServicesIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="a3fe8-142">INPUTOBJECT <IWindowsIotServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a3fe8-143">`[DeviceName <String>]`: Namnet på Windows IoT Device-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="a3fe8-143">`[DeviceName <String>]`: The name of the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="a3fe8-144">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="a3fe8-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a3fe8-145">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller Windows IoT-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="a3fe8-145">`[ResourceGroupName <String>]`: The name of the resource group that contains the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="a3fe8-146">`[SubscriptionId <String>]`: Prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="a3fe8-146">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="a3fe8-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a3fe8-147">RELATED LINKS</span></span>

