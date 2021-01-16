---
external help file: ''
Module Name: Az.WindowsIotServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.windowsiotservices/get-azwindowsiotservicesdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Get-AzWindowsIotServicesDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Get-AzWindowsIotServicesDevice.md
ms.openlocfilehash: b9236dc7c3e4a12c9be6b72cd63874044ee49065
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522036"
---
# <span data-ttu-id="0379b-101">Get-AzWindowsIotServicesDevice</span><span class="sxs-lookup"><span data-stu-id="0379b-101">Get-AzWindowsIotServicesDevice</span></span>

## <span data-ttu-id="0379b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0379b-102">SYNOPSIS</span></span>
<span data-ttu-id="0379b-103">Hämta icke-säkerhetsrelaterade metadata för en Windows IoT-enhet.</span><span class="sxs-lookup"><span data-stu-id="0379b-103">Get the non-security related metadata of a Windows IoT Device Service.</span></span>

## <span data-ttu-id="0379b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0379b-104">SYNTAX</span></span>

### <span data-ttu-id="0379b-105">List1 (standard)</span><span class="sxs-lookup"><span data-stu-id="0379b-105">List1 (Default)</span></span>
```
Get-AzWindowsIotServicesDevice [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0379b-106">Lära</span><span class="sxs-lookup"><span data-stu-id="0379b-106">Get</span></span>
```
Get-AzWindowsIotServicesDevice -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0379b-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0379b-107">GetViaIdentity</span></span>
```
Get-AzWindowsIotServicesDevice -InputObject <IWindowsIotServicesIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="0379b-108">Förteckning</span><span class="sxs-lookup"><span data-stu-id="0379b-108">List</span></span>
```
Get-AzWindowsIotServicesDevice -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="0379b-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0379b-109">DESCRIPTION</span></span>
<span data-ttu-id="0379b-110">Hämta icke-säkerhetsrelaterade metadata för en Windows IoT-enhet.</span><span class="sxs-lookup"><span data-stu-id="0379b-110">Get the non-security related metadata of a Windows IoT Device Service.</span></span>

## <span data-ttu-id="0379b-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0379b-111">EXAMPLES</span></span>

### <span data-ttu-id="0379b-112">Exempel 1: Hämta alla Windows IoT-tjänster under ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="0379b-112">Example 1: Get all Windows IoT services under a subscription</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5c006e63-0000-0700-0000-5faa37830000"
eastus   wsi-t02 Microsoft.WindowsIoT/DeviceServices "5c006ad2-0000-0700-0000-5faa3e090000"
```

<span data-ttu-id="0379b-113">Det här kommandot får alla Windows IoT-tjänster under ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="0379b-113">This command gets all Windows IoT services under a subscription.</span></span>

### <span data-ttu-id="0379b-114">Exempel 2: Hämta alla Windows IoT-tjänster under en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="0379b-114">Example 2: Get all Windows IoT services under a resource group</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice -ResourceGroupName azure-rg-test

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5c006e63-0000-0700-0000-5faa37830000"
eastus   wsi-t02 Microsoft.WindowsIoT/DeviceServices "5c006ad2-0000-0700-0000-5faa3e090000"
```

<span data-ttu-id="0379b-115">Det här kommandot får alla Windows IoT-tjänster under en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="0379b-115">This command gets all Windows IoT services under a resource group.</span></span>

### <span data-ttu-id="0379b-116">Exempel 3: skaffa en Windows IoT-tjänst utifrån namn</span><span class="sxs-lookup"><span data-stu-id="0379b-116">Example 3: Get a Windows IoT service by name</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice -ResourceGroupName azure-rg-test -Name wsi-t01

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5c006e63-0000-0700-0000-5faa37830000"
```

<span data-ttu-id="0379b-117">Det här kommandot får en Windows IoT-tjänst med namn.</span><span class="sxs-lookup"><span data-stu-id="0379b-117">This command gets a Windows IoT service by name.</span></span>

### <span data-ttu-id="0379b-118">Exempel 4: skaffa en Windows IoT-tjänst per objekt</span><span class="sxs-lookup"><span data-stu-id="0379b-118">Example 4: Get a Windows IoT service by object</span></span>
```powershell
PS C:\> $wsi = New-AzWindowsIotServicesDevice -Name wsi-t01 -ResourceGroupName azure-rg-test -Location eastus -Quantity 10 -BillingDomainName 'microsoft.onmicrosoft.com' -AdminDomainName 'microsoft.onmicrosoft.com'
PS C:\> Get-AzWindowsIotServicesDevice -InputObject $wsi

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5c006e63-0000-0700-0000-5faa37830000"
```

<span data-ttu-id="0379b-119">Det här kommandot får en Windows IoT-tjänst via objekt.</span><span class="sxs-lookup"><span data-stu-id="0379b-119">This command gets a Windows IoT service by object.</span></span>

### <span data-ttu-id="0379b-120">Exempel 4: skaffa en Windows IoT-tjänst via pipeline</span><span class="sxs-lookup"><span data-stu-id="0379b-120">Example 4: Get a Windows IoT service by pipeline</span></span>
```powershell
PS C:\> $wsi = New-AzWindowsIotServicesDevice -Name wsi-t01 -ResourceGroupName azure-rg-test -Location eastus -Quantity 10 -BillingDomainName 'microsoft.onmicrosoft.com' -AdminDomainName 'microsoft.onmicrosoft.com' | Get-AzWindowsIotServicesDevice

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5c006e63-0000-0700-0000-5faa37830000"
```

<span data-ttu-id="0379b-121">Det här kommandot får en Windows IoT-tjänst via pipeline.</span><span class="sxs-lookup"><span data-stu-id="0379b-121">This command gets a Windows IoT service by pipeline.</span></span>

## <span data-ttu-id="0379b-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0379b-122">PARAMETERS</span></span>

### <span data-ttu-id="0379b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0379b-123">-DefaultProfile</span></span>
<span data-ttu-id="0379b-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0379b-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0379b-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0379b-125">-InputObject</span></span>
<span data-ttu-id="0379b-126">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="0379b-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0379b-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="0379b-127">-Name</span></span>
<span data-ttu-id="0379b-128">Namnet på Windows IoT Device-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="0379b-128">The name of the Windows IoT Device Service.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0379b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0379b-129">-ResourceGroupName</span></span>
<span data-ttu-id="0379b-130">Namnet på resurs gruppen som innehåller Windows IoT-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="0379b-130">The name of the resource group that contains the Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="0379b-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0379b-131">-SubscriptionId</span></span>
<span data-ttu-id="0379b-132">Prenumerations-ID.</span><span class="sxs-lookup"><span data-stu-id="0379b-132">The subscription identifier.</span></span>

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

### <span data-ttu-id="0379b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0379b-133">CommonParameters</span></span>
<span data-ttu-id="0379b-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0379b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0379b-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0379b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0379b-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0379b-136">INPUTS</span></span>

### <span data-ttu-id="0379b-137">Microsoft. Azure. PowerShell. cmdletar. WindowsIotServices. Models. IWindowsIotServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="0379b-137">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span></span>

## <span data-ttu-id="0379b-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0379b-138">OUTPUTS</span></span>

### <span data-ttu-id="0379b-139">Microsoft. Azure. PowerShell. cmdletar. WindowsIotServices. Models. Api20190601. IDeviceService</span><span class="sxs-lookup"><span data-stu-id="0379b-139">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span></span>

## <span data-ttu-id="0379b-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0379b-140">NOTES</span></span>

<span data-ttu-id="0379b-141">ALIAS</span><span class="sxs-lookup"><span data-stu-id="0379b-141">ALIASES</span></span>

<span data-ttu-id="0379b-142">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="0379b-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0379b-143">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="0379b-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0379b-144">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0379b-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0379b-145">INPUTOBJECT <IWindowsIotServicesIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="0379b-145">INPUTOBJECT <IWindowsIotServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0379b-146">`[DeviceName <String>]`: Namnet på Windows IoT Device-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="0379b-146">`[DeviceName <String>]`: The name of the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="0379b-147">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="0379b-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0379b-148">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller Windows IoT-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="0379b-148">`[ResourceGroupName <String>]`: The name of the resource group that contains the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="0379b-149">`[SubscriptionId <String>]`: Prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="0379b-149">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="0379b-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0379b-150">RELATED LINKS</span></span>

