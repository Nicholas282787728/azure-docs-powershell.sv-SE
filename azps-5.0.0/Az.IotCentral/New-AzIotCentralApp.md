---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/new-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/New-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/New-AzIotCentralApp.md
ms.openlocfilehash: 1be2aa8e198ae096f445b9f1972d1e0b903ae729
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271026"
---
# <span data-ttu-id="014c2-101">New-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="014c2-101">New-AzIotCentralApp</span></span>

## <span data-ttu-id="014c2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="014c2-102">SYNOPSIS</span></span>
<span data-ttu-id="014c2-103">Skapar ett nytt IoT Central program.</span><span class="sxs-lookup"><span data-stu-id="014c2-103">Creates a new IoT Central Application.</span></span>

## <span data-ttu-id="014c2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="014c2-104">SYNTAX</span></span>

```
New-AzIotCentralApp [-Subdomain] <String> [-DisplayName <String>] [-Template <String>] [-Sku <String>]
 [-Location <String>] [-Tag <Hashtable>] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="014c2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="014c2-105">DESCRIPTION</span></span>
<span data-ttu-id="014c2-106">Skapar ett nytt IoT Central program med de tillhandahållna egenskaperna och metadata.</span><span class="sxs-lookup"><span data-stu-id="014c2-106">Creates a new IoT Central Application with the provided properties and metadata.</span></span> <span data-ttu-id="014c2-107">En introduktion till IoT Central finns i https://docs.microsoft.com/en-us/azure/iot-central/ .</span><span class="sxs-lookup"><span data-stu-id="014c2-107">For an introduction to IoT Central, see https://docs.microsoft.com/en-us/azure/iot-central/.</span></span>

## <span data-ttu-id="014c2-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="014c2-108">EXAMPLES</span></span>

### <span data-ttu-id="014c2-109">Exempel 1 skapa enkel IoT Central-program.</span><span class="sxs-lookup"><span data-stu-id="014c2-109">Example 1 Create simple IoT Central Application.</span></span>
```powershell
PS C:\> New-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "MyAppSubdomain"
```

<span data-ttu-id="014c2-110">Exempel på utdata:</span><span class="sxs-lookup"><span data-stu-id="014c2-110">Example Output:</span></span>

<span data-ttu-id="014c2-111">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName namn: MyAppResourceName typ: Microsoft. IoTCentral/IoTApps Location: Tagged tag: SKU: Microsoft. Azure. commands. IotCentral. Models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: MyAppResourceName under domän: MyAppSubdomain Template: iotc-default@1.0.0 SubscriptionId: XXXXXXXX-XXXX-XXXX-XXXX</span><span class="sxs-lookup"><span data-stu-id="014c2-111">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : MyAppResourceName Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="014c2-112">Skapa ett IoT-centralt program i standard pris nivå ST2, i området i resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="014c2-112">Create an IoT Central application in the standard pricing tier ST2, in the region of the resource group.</span></span>

### <span data-ttu-id="014c2-113">Exempel 2 skapa enkel IoT Central-program.</span><span class="sxs-lookup"><span data-stu-id="014c2-113">Example 2 Create simple IoT Central Application.</span></span>
```powershell
PS C:\> New-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "MyAppSubdomain" -Sku "ST2" -DisplayName "My Custom Display Name" -Template "iotc-default" -Location "westus"
```

<span data-ttu-id="014c2-114">Exempel på utdata:</span><span class="sxs-lookup"><span data-stu-id="014c2-114">Example Output:</span></span>

<span data-ttu-id="014c2-115">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName namn: MyAppResourceName typ: Microsoft. IoTCentral/IoTApps Location: taggning for tag: SKU: Microsoft. Azure. commands. IotCentral. Models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX-DisplayName: mitt eget visnings namn under domän: MyAppSubdomain Template: iotc-default@1.0.0 SubscriptionId: XXXXXXXX-XXXX-XXXX</span><span class="sxs-lookup"><span data-stu-id="014c2-115">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="014c2-116">Skapa ett IoT Central program med standard pris nivån ST2 i regionen "västkusten", med ett anpassat visnings namn baserat på IOTC-standard-mallen.</span><span class="sxs-lookup"><span data-stu-id="014c2-116">Create an IoT Central application with the standard pricing tier ST2 in the 'westus' region, with a custom display name, based on the iotc-default template.</span></span>

## <span data-ttu-id="014c2-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="014c2-117">PARAMETERS</span></span>

### <span data-ttu-id="014c2-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="014c2-118">-AsJob</span></span>
<span data-ttu-id="014c2-119">Kör cmdlet som ett jobb i bakgrunden.</span><span class="sxs-lookup"><span data-stu-id="014c2-119">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="014c2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="014c2-120">-DefaultProfile</span></span>
<span data-ttu-id="014c2-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="014c2-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="014c2-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="014c2-122">-DisplayName</span></span>
<span data-ttu-id="014c2-123">Anpassat visnings namn för IoT Central-programmet.</span><span class="sxs-lookup"><span data-stu-id="014c2-123">Custom display name for the IoT Central application.</span></span>
<span data-ttu-id="014c2-124">Standard är resurs namn.</span><span class="sxs-lookup"><span data-stu-id="014c2-124">Default is resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="014c2-125">-Plats</span><span class="sxs-lookup"><span data-stu-id="014c2-125">-Location</span></span>
<span data-ttu-id="014c2-126">Platsen för IoT-huvudprogrammet.</span><span class="sxs-lookup"><span data-stu-id="014c2-126">Location of your IoT Central application.</span></span>
<span data-ttu-id="014c2-127">Standard platsen för mål resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="014c2-127">Default is the location of target resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="014c2-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="014c2-128">-Name</span></span>
<span data-ttu-id="014c2-129">Namnet på IoT Central program resursen.</span><span class="sxs-lookup"><span data-stu-id="014c2-129">Name of the Iot Central Application Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="014c2-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="014c2-130">-ResourceGroupName</span></span>
<span data-ttu-id="014c2-131">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="014c2-131">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="014c2-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="014c2-132">-Sku</span></span>
<span data-ttu-id="014c2-133">Pris nivå för IoT Central program.</span><span class="sxs-lookup"><span data-stu-id="014c2-133">Pricing tier for IoT Central applications.</span></span>
<span data-ttu-id="014c2-134">Standardvärdet är ST2.</span><span class="sxs-lookup"><span data-stu-id="014c2-134">Default value is ST2.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="014c2-135">-Subdomain</span><span class="sxs-lookup"><span data-stu-id="014c2-135">-Subdomain</span></span>
<span data-ttu-id="014c2-136">Under domän för IoT Central URL.</span><span class="sxs-lookup"><span data-stu-id="014c2-136">Subdomain for the IoT Central URL.</span></span>
<span data-ttu-id="014c2-137">Varje program måste ha en unik under domän.</span><span class="sxs-lookup"><span data-stu-id="014c2-137">Each application must have a unique subdomain.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="014c2-138">-Tagg</span><span class="sxs-lookup"><span data-stu-id="014c2-138">-Tag</span></span>
<span data-ttu-id="014c2-139">IoT Central program, Resource-taggar.</span><span class="sxs-lookup"><span data-stu-id="014c2-139">Iot Central Application Resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="014c2-140">-Mall</span><span class="sxs-lookup"><span data-stu-id="014c2-140">-Template</span></span>
<span data-ttu-id="014c2-141">IoT Central program mal len namn.</span><span class="sxs-lookup"><span data-stu-id="014c2-141">IoT Central application template name.</span></span>
<span data-ttu-id="014c2-142">Standard är ett anpassat program.</span><span class="sxs-lookup"><span data-stu-id="014c2-142">Default is a custom application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="014c2-143">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="014c2-143">-Confirm</span></span>
<span data-ttu-id="014c2-144">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="014c2-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="014c2-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="014c2-145">-WhatIf</span></span>
<span data-ttu-id="014c2-146">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="014c2-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="014c2-147">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="014c2-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="014c2-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="014c2-148">CommonParameters</span></span>
<span data-ttu-id="014c2-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="014c2-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="014c2-150">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="014c2-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="014c2-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="014c2-151">INPUTS</span></span>

### <span data-ttu-id="014c2-152">System. String</span><span class="sxs-lookup"><span data-stu-id="014c2-152">System.String</span></span>

### <span data-ttu-id="014c2-153">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="014c2-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="014c2-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="014c2-154">OUTPUTS</span></span>

### <span data-ttu-id="014c2-155">Microsoft. Azure. commands. IotCentral. Models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="014c2-155">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="014c2-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="014c2-156">NOTES</span></span>

## <span data-ttu-id="014c2-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="014c2-157">RELATED LINKS</span></span>