---
external help file: ''
Module Name: Az.WindowsIotServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.windowsiotservices/new-azwindowsiotservicesdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/New-AzWindowsIotServicesDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/New-AzWindowsIotServicesDevice.md
ms.openlocfilehash: 4da60a6d4083992f843121cb141a453b4ef3b4b8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98402643"
---
# <span data-ttu-id="40edf-101">New-AzWindowsIotServicesDevice</span><span class="sxs-lookup"><span data-stu-id="40edf-101">New-AzWindowsIotServicesDevice</span></span>

## <span data-ttu-id="40edf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="40edf-102">SYNOPSIS</span></span>
<span data-ttu-id="40edf-103">Skapa eller uppdatera metadata för en Windows IoT-enhet.</span><span class="sxs-lookup"><span data-stu-id="40edf-103">Create or update the metadata of a Windows IoT Device Service.</span></span>
<span data-ttu-id="40edf-104">Det vanliga mönstret för att ändra en egenskap är att hämta metadata och säkerhets-metadata för Windows IoT Device service och sedan kombinera dem med de ändrade värdena i en ny brödtext och uppdatera enhets tjänsten för Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="40edf-104">The usual pattern to modify a property is to retrieve the Windows IoT Device Service metadata and security metadata, and then combine them with the modified values in a new body to update the Windows IoT Device Service.</span></span>

## <span data-ttu-id="40edf-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="40edf-105">SYNTAX</span></span>

```
New-AzWindowsIotServicesDevice -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IfMatch <String>] [-AdminDomainName <String>] [-BillingDomainName <String>] [-Etag <String>]
 [-Location <String>] [-Note <String>] [-Quantity <Int64>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="40edf-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="40edf-106">DESCRIPTION</span></span>
<span data-ttu-id="40edf-107">Skapa eller uppdatera metadata för en Windows IoT-enhet.</span><span class="sxs-lookup"><span data-stu-id="40edf-107">Create or update the metadata of a Windows IoT Device Service.</span></span>
<span data-ttu-id="40edf-108">Det vanliga mönstret för att ändra en egenskap är att hämta metadata och säkerhets-metadata för Windows IoT Device service och sedan kombinera dem med de ändrade värdena i en ny brödtext och uppdatera enhets tjänsten för Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="40edf-108">The usual pattern to modify a property is to retrieve the Windows IoT Device Service metadata and security metadata, and then combine them with the modified values in a new body to update the Windows IoT Device Service.</span></span>

## <span data-ttu-id="40edf-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="40edf-109">EXAMPLES</span></span>

### <span data-ttu-id="40edf-110">Exempel 1: skapa en ny Windows IoT-tjänst</span><span class="sxs-lookup"><span data-stu-id="40edf-110">Example 1: Create a new Windows IoT services</span></span>
```powershell
PS C:\> New-AzWindowsIotServicesDevice -Name wsi-t03 -ResourceGroupName azure-rg-test -Location eastus -Quantity 10 -BillingDomainName 'microsoft.onmicrosoft.com' -AdminDomainName 'microsoft.onmicrosoft.com'

Location Name    Type                                Etag
-------- ----    ----                                ----
eastus   wsi-t03 Microsoft.WindowsIoT/DeviceServices "6a00eee9-0000-0700-0000-5fab82870000"
```

<span data-ttu-id="40edf-111">Det här kommandot skapar en ny Windows IoT-tjänst.</span><span class="sxs-lookup"><span data-stu-id="40edf-111">This command creates a new Windows IoT services.</span></span>

## <span data-ttu-id="40edf-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="40edf-112">PARAMETERS</span></span>

### <span data-ttu-id="40edf-113">-AdminDomainName</span><span class="sxs-lookup"><span data-stu-id="40edf-113">-AdminDomainName</span></span>
<span data-ttu-id="40edf-114">Windows IoT-tjänsten OEM-domän</span><span class="sxs-lookup"><span data-stu-id="40edf-114">Windows IoT Device Service OEM AAD domain</span></span>

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

### <span data-ttu-id="40edf-115">-BillingDomainName</span><span class="sxs-lookup"><span data-stu-id="40edf-115">-BillingDomainName</span></span>
<span data-ttu-id="40edf-116">Windows IoT-tjänsten ODM AAD-domän</span><span class="sxs-lookup"><span data-stu-id="40edf-116">Windows IoT Device Service ODM AAD domain</span></span>

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

### <span data-ttu-id="40edf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40edf-117">-DefaultProfile</span></span>
<span data-ttu-id="40edf-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="40edf-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40edf-119">-Etag</span><span class="sxs-lookup"><span data-stu-id="40edf-119">-Etag</span></span>
<span data-ttu-id="40edf-120">Fältet ETAG är *inte* obligatoriskt.</span><span class="sxs-lookup"><span data-stu-id="40edf-120">The Etag field is *not* required.</span></span>
<span data-ttu-id="40edf-121">Om det finns med i svars texten måste det också tillhandahållas som ett huvud enligt den vanliga ETag-konventionen.</span><span class="sxs-lookup"><span data-stu-id="40edf-121">If it is provided in the response body, it must also be provided as a header per the normal ETag convention.</span></span>

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

### <span data-ttu-id="40edf-122">-IfMatch</span><span class="sxs-lookup"><span data-stu-id="40edf-122">-IfMatch</span></span>
<span data-ttu-id="40edf-123">ETag för Windows IoT-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="40edf-123">ETag of the Windows IoT Device Service.</span></span>
<span data-ttu-id="40edf-124">Ange inte för att skapa en ny Windows IoT-enhet.</span><span class="sxs-lookup"><span data-stu-id="40edf-124">Do not specify for creating a new Windows IoT Device Service.</span></span>
<span data-ttu-id="40edf-125">Krävs för att uppdatera en befintlig Windows IoT-enhets tjänst.</span><span class="sxs-lookup"><span data-stu-id="40edf-125">Required to update an existing Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="40edf-126">-Plats</span><span class="sxs-lookup"><span data-stu-id="40edf-126">-Location</span></span>
<span data-ttu-id="40edf-127">Azure-regionen där resursen bor</span><span class="sxs-lookup"><span data-stu-id="40edf-127">The Azure Region where the resource lives</span></span>

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

### <span data-ttu-id="40edf-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="40edf-128">-Name</span></span>
<span data-ttu-id="40edf-129">Namnet på Windows IoT Device-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="40edf-129">The name of the Windows IoT Device Service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40edf-130">-Obs!</span><span class="sxs-lookup"><span data-stu-id="40edf-130">-Note</span></span>
<span data-ttu-id="40edf-131">Tjänst anteckningar i Windows IoT-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="40edf-131">Windows IoT Device Service notes.</span></span>

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

### <span data-ttu-id="40edf-132">-Antal</span><span class="sxs-lookup"><span data-stu-id="40edf-132">-Quantity</span></span>
<span data-ttu-id="40edf-133">Tilldelning av enhets tjänst för Windows IoT</span><span class="sxs-lookup"><span data-stu-id="40edf-133">Windows IoT Device Service device allocation,</span></span>

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

### <span data-ttu-id="40edf-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40edf-134">-ResourceGroupName</span></span>
<span data-ttu-id="40edf-135">Namnet på resurs gruppen som innehåller Windows IoT-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="40edf-135">The name of the resource group that contains the Windows IoT Device Service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40edf-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="40edf-136">-SubscriptionId</span></span>
<span data-ttu-id="40edf-137">Prenumerations-ID.</span><span class="sxs-lookup"><span data-stu-id="40edf-137">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40edf-138">-Tagg</span><span class="sxs-lookup"><span data-stu-id="40edf-138">-Tag</span></span>
<span data-ttu-id="40edf-139">Resource-taggar.</span><span class="sxs-lookup"><span data-stu-id="40edf-139">Resource tags.</span></span>

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

### <span data-ttu-id="40edf-140">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="40edf-140">-Confirm</span></span>
<span data-ttu-id="40edf-141">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="40edf-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40edf-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40edf-142">-WhatIf</span></span>
<span data-ttu-id="40edf-143">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="40edf-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40edf-144">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="40edf-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40edf-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40edf-145">CommonParameters</span></span>
<span data-ttu-id="40edf-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40edf-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40edf-147">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="40edf-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40edf-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="40edf-148">INPUTS</span></span>

## <span data-ttu-id="40edf-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="40edf-149">OUTPUTS</span></span>

### <span data-ttu-id="40edf-150">Microsoft. Azure. PowerShell. cmdletar. WindowsIotServices. Models. Api20190601. IDeviceService</span><span class="sxs-lookup"><span data-stu-id="40edf-150">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span></span>

## <span data-ttu-id="40edf-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="40edf-151">NOTES</span></span>

<span data-ttu-id="40edf-152">ALIAS</span><span class="sxs-lookup"><span data-stu-id="40edf-152">ALIASES</span></span>

## <span data-ttu-id="40edf-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="40edf-153">RELATED LINKS</span></span>

