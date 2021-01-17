---
external help file: ''
Module Name: Az.WindowsIotServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.windowsiotservices/update-azwindowsiotservicesdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Update-AzWindowsIotServicesDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Update-AzWindowsIotServicesDevice.md
ms.openlocfilehash: 5e50ad3dc1ce2396dfb7a2b498efc82c4e95e430
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98417328"
---
# <span data-ttu-id="c3f16-101">Update-AzWindowsIotServicesDevice</span><span class="sxs-lookup"><span data-stu-id="c3f16-101">Update-AzWindowsIotServicesDevice</span></span>

## <span data-ttu-id="c3f16-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c3f16-102">SYNOPSIS</span></span>
<span data-ttu-id="c3f16-103">Uppdaterar metadata för en Windows IoT-enhet.</span><span class="sxs-lookup"><span data-stu-id="c3f16-103">Updates the metadata of a Windows IoT Device Service.</span></span>
<span data-ttu-id="c3f16-104">Det vanliga mönstret för att ändra en egenskap är att hämta metadata och säkerhets-metadata för Windows IoT Device service och sedan kombinera dem med de ändrade värdena i en ny brödtext och uppdatera enhets tjänsten för Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="c3f16-104">The usual pattern to modify a property is to retrieve the Windows IoT Device Service metadata and security metadata, and then combine them with the modified values in a new body to update the Windows IoT Device Service.</span></span>

## <span data-ttu-id="c3f16-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c3f16-105">SYNTAX</span></span>

### <span data-ttu-id="c3f16-106">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="c3f16-106">UpdateExpanded (Default)</span></span>
```
Update-AzWindowsIotServicesDevice -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IfMatch <String>] [-AdminDomainName <String>] [-BillingDomainName <String>] [-Etag <String>]
 [-Location <String>] [-Note <String>] [-Quantity <Int64>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c3f16-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="c3f16-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzWindowsIotServicesDevice -InputObject <IWindowsIotServicesIdentity> [-IfMatch <String>]
 [-AdminDomainName <String>] [-BillingDomainName <String>] [-Etag <String>] [-Location <String>]
 [-Note <String>] [-Quantity <Int64>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="c3f16-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c3f16-108">DESCRIPTION</span></span>
<span data-ttu-id="c3f16-109">Uppdaterar metadata för en Windows IoT-enhet.</span><span class="sxs-lookup"><span data-stu-id="c3f16-109">Updates the metadata of a Windows IoT Device Service.</span></span>
<span data-ttu-id="c3f16-110">Det vanliga mönstret för att ändra en egenskap är att hämta metadata och säkerhets-metadata för Windows IoT Device service och sedan kombinera dem med de ändrade värdena i en ny brödtext och uppdatera enhets tjänsten för Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="c3f16-110">The usual pattern to modify a property is to retrieve the Windows IoT Device Service metadata and security metadata, and then combine them with the modified values in a new body to update the Windows IoT Device Service.</span></span>

## <span data-ttu-id="c3f16-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c3f16-111">EXAMPLES</span></span>

### <span data-ttu-id="c3f16-112">Exempel 1: uppdatera en Windows IoT-tjänst med namn</span><span class="sxs-lookup"><span data-stu-id="c3f16-112">Example 1: Update a Windows IoT services by name</span></span>
```powershell
PS C:\> Update-AzWindowsIotServicesDevice -Name wsi-t03 -ResourceGroupName azure-rg-test -Quantity 10

Location Name    Type                                Etag
-------- ----    ----                                ----
eastus   wsi-t03 Microsoft.WindowsIoT/DeviceServices "5d006a5c-0000-0700-0000-5faa46760000"
```

<span data-ttu-id="c3f16-113">Det här kommandot uppdaterar en Windows IoT-tjänst med namn.</span><span class="sxs-lookup"><span data-stu-id="c3f16-113">This command updates a Windows IoT services by name.</span></span>

### <span data-ttu-id="c3f16-114">Exempel 2: uppdatera en Windows IoT-tjänst via pipeline</span><span class="sxs-lookup"><span data-stu-id="c3f16-114">Example 2: Update a Windows IoT services by pipeline</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice -Name wsi-t03 -ResourceGroupName azure-rg-test | Update-AzWindowsIotServicesDevice-Quantity 100 -Tag @{'oper'='update'}

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5d005f5f-0000-0700-0000-5faa46ae0000"
```

<span data-ttu-id="c3f16-115">Det här kommandot uppdaterar en Windows IoT-tjänst via pipeline.</span><span class="sxs-lookup"><span data-stu-id="c3f16-115">This command updates a Windows IoT services by pipeline.</span></span>

## <span data-ttu-id="c3f16-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c3f16-116">PARAMETERS</span></span>

### <span data-ttu-id="c3f16-117">-AdminDomainName</span><span class="sxs-lookup"><span data-stu-id="c3f16-117">-AdminDomainName</span></span>
<span data-ttu-id="c3f16-118">Windows IoT-tjänsten OEM-domän</span><span class="sxs-lookup"><span data-stu-id="c3f16-118">Windows IoT Device Service OEM AAD domain</span></span>

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

### <span data-ttu-id="c3f16-119">-BillingDomainName</span><span class="sxs-lookup"><span data-stu-id="c3f16-119">-BillingDomainName</span></span>
<span data-ttu-id="c3f16-120">Windows IoT-tjänsten ODM AAD-domän</span><span class="sxs-lookup"><span data-stu-id="c3f16-120">Windows IoT Device Service ODM AAD domain</span></span>

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

### <span data-ttu-id="c3f16-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3f16-121">-DefaultProfile</span></span>
<span data-ttu-id="c3f16-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c3f16-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3f16-123">-Etag</span><span class="sxs-lookup"><span data-stu-id="c3f16-123">-Etag</span></span>
<span data-ttu-id="c3f16-124">Fältet ETAG är *inte* obligatoriskt.</span><span class="sxs-lookup"><span data-stu-id="c3f16-124">The Etag field is *not* required.</span></span>
<span data-ttu-id="c3f16-125">Om det finns med i svars texten måste det också tillhandahållas som ett huvud enligt den vanliga ETag-konventionen.</span><span class="sxs-lookup"><span data-stu-id="c3f16-125">If it is provided in the response body, it must also be provided as a header per the normal ETag convention.</span></span>

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

### <span data-ttu-id="c3f16-126">-IfMatch</span><span class="sxs-lookup"><span data-stu-id="c3f16-126">-IfMatch</span></span>
<span data-ttu-id="c3f16-127">ETag för Windows IoT-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c3f16-127">ETag of the Windows IoT Device Service.</span></span>
<span data-ttu-id="c3f16-128">Ange inte för att skapa en helt ny Windows IoT-enhet.</span><span class="sxs-lookup"><span data-stu-id="c3f16-128">Do not specify for creating a brand new Windows IoT Device Service.</span></span>
<span data-ttu-id="c3f16-129">Krävs för att uppdatera en befintlig Windows IoT-enhets tjänst.</span><span class="sxs-lookup"><span data-stu-id="c3f16-129">Required to update an existing Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="c3f16-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c3f16-130">-InputObject</span></span>
<span data-ttu-id="c3f16-131">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="c3f16-131">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c3f16-132">-Plats</span><span class="sxs-lookup"><span data-stu-id="c3f16-132">-Location</span></span>
<span data-ttu-id="c3f16-133">Azure-regionen där resursen bor</span><span class="sxs-lookup"><span data-stu-id="c3f16-133">The Azure Region where the resource lives</span></span>

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

### <span data-ttu-id="c3f16-134">-Namn</span><span class="sxs-lookup"><span data-stu-id="c3f16-134">-Name</span></span>
<span data-ttu-id="c3f16-135">Namnet på Windows IoT Device-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c3f16-135">The name of the Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="c3f16-136">-Obs!</span><span class="sxs-lookup"><span data-stu-id="c3f16-136">-Note</span></span>
<span data-ttu-id="c3f16-137">Tjänst anteckningar i Windows IoT-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c3f16-137">Windows IoT Device Service notes.</span></span>

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

### <span data-ttu-id="c3f16-138">-Antal</span><span class="sxs-lookup"><span data-stu-id="c3f16-138">-Quantity</span></span>
<span data-ttu-id="c3f16-139">Tilldelning av enhets tjänst för Windows IoT</span><span class="sxs-lookup"><span data-stu-id="c3f16-139">Windows IoT Device Service device allocation,</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3f16-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3f16-140">-ResourceGroupName</span></span>
<span data-ttu-id="c3f16-141">Namnet på resurs gruppen som innehåller Windows IoT-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c3f16-141">The name of the resource group that contains the Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="c3f16-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c3f16-142">-SubscriptionId</span></span>
<span data-ttu-id="c3f16-143">Prenumerations-ID.</span><span class="sxs-lookup"><span data-stu-id="c3f16-143">The subscription identifier.</span></span>

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

### <span data-ttu-id="c3f16-144">-Tagg</span><span class="sxs-lookup"><span data-stu-id="c3f16-144">-Tag</span></span>
<span data-ttu-id="c3f16-145">Resource-taggar.</span><span class="sxs-lookup"><span data-stu-id="c3f16-145">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3f16-146">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c3f16-146">-Confirm</span></span>
<span data-ttu-id="c3f16-147">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c3f16-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3f16-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3f16-148">-WhatIf</span></span>
<span data-ttu-id="c3f16-149">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c3f16-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3f16-150">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c3f16-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3f16-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3f16-151">CommonParameters</span></span>
<span data-ttu-id="c3f16-152">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3f16-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3f16-153">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c3f16-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3f16-154">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c3f16-154">INPUTS</span></span>

### <span data-ttu-id="c3f16-155">Microsoft. Azure. PowerShell. cmdletar. WindowsIotServices. Models. IWindowsIotServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="c3f16-155">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span></span>

## <span data-ttu-id="c3f16-156">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c3f16-156">OUTPUTS</span></span>

### <span data-ttu-id="c3f16-157">Microsoft. Azure. PowerShell. cmdletar. WindowsIotServices. Models. Api20190601. IDeviceService</span><span class="sxs-lookup"><span data-stu-id="c3f16-157">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span></span>

## <span data-ttu-id="c3f16-158">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c3f16-158">NOTES</span></span>

<span data-ttu-id="c3f16-159">ALIAS</span><span class="sxs-lookup"><span data-stu-id="c3f16-159">ALIASES</span></span>

<span data-ttu-id="c3f16-160">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="c3f16-160">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c3f16-161">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="c3f16-161">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c3f16-162">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c3f16-162">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c3f16-163">INPUTOBJECT <IWindowsIotServicesIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="c3f16-163">INPUTOBJECT <IWindowsIotServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c3f16-164">`[DeviceName <String>]`: Namnet på Windows IoT Device-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c3f16-164">`[DeviceName <String>]`: The name of the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="c3f16-165">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="c3f16-165">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c3f16-166">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller Windows IoT-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c3f16-166">`[ResourceGroupName <String>]`: The name of the resource group that contains the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="c3f16-167">`[SubscriptionId <String>]`: Prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="c3f16-167">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="c3f16-168">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c3f16-168">RELATED LINKS</span></span>

