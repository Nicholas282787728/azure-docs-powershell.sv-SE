---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/new-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/New-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/New-AzIotCentralApp.md
ms.openlocfilehash: 636c40763c69a4c39ca0bbf8b15fe04fad318d84
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916518"
---
# <span data-ttu-id="e0071-101">New-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="e0071-101">New-AzIotCentralApp</span></span>

## <span data-ttu-id="e0071-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e0071-102">SYNOPSIS</span></span>
<span data-ttu-id="e0071-103">Skapar ett nytt IoT Central program.</span><span class="sxs-lookup"><span data-stu-id="e0071-103">Creates a new IoT Central Application.</span></span>

## <span data-ttu-id="e0071-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e0071-104">SYNTAX</span></span>

```
New-AzIotCentralApp [-Subdomain] <String> [-DisplayName <String>] [-Template <String>] [-Sku <String>]
 [-Location <String>] [-Tag <Hashtable>] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0071-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e0071-105">DESCRIPTION</span></span>
<span data-ttu-id="e0071-106">Skapar ett nytt IoT Central program med de tillhandahållna egenskaperna och metadata.</span><span class="sxs-lookup"><span data-stu-id="e0071-106">Creates a new IoT Central Application with the provided properties and metadata.</span></span> <span data-ttu-id="e0071-107">En introduktion till IoT Central finns i https://docs.microsoft.com/en-us/azure/iot-central/ .</span><span class="sxs-lookup"><span data-stu-id="e0071-107">For an introduction to IoT Central, see https://docs.microsoft.com/en-us/azure/iot-central/.</span></span>

## <span data-ttu-id="e0071-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e0071-108">EXAMPLES</span></span>

### <span data-ttu-id="e0071-109">Exempel 1 skapa enkel IoT Central-program.</span><span class="sxs-lookup"><span data-stu-id="e0071-109">Example 1 Create simple IoT Central Application.</span></span>
```powershell
PS C:\> New-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "MyAppSubdomain"
```

<span data-ttu-id="e0071-110">Exempel på utdata:</span><span class="sxs-lookup"><span data-stu-id="e0071-110">Example Output:</span></span>

<span data-ttu-id="e0071-111">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName namn: MyAppResourceName typ: Microsoft. IoTCentral/IoTApps Location: Tagged tag: SKU: Microsoft. Azure. commands. IotCentral. Models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: MyAppResourceName under domän: MyAppSubdomain Template: iotc-default@1.0.0 SubscriptionId: XXXXXXXX-XXXX-XXXX-XXXX</span><span class="sxs-lookup"><span data-stu-id="e0071-111">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : MyAppResourceName Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="e0071-112">Skapa ett IoT-centralt program i standard pris nivån S1 i området i resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="e0071-112">Create an IoT Central application in the standard pricing tier S1, in the region of the resource group.</span></span>

### <span data-ttu-id="e0071-113">Exempel 2 skapa enkel IoT Central-program.</span><span class="sxs-lookup"><span data-stu-id="e0071-113">Example 2 Create simple IoT Central Application.</span></span>
```powershell
PS C:\> New-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "MyAppSubdomain" -Sku "S1" -DisplayName "My Custom Display Name" -Template "iotc-default" -Location "westus"
```

<span data-ttu-id="e0071-114">Exempel på utdata:</span><span class="sxs-lookup"><span data-stu-id="e0071-114">Example Output:</span></span>

<span data-ttu-id="e0071-115">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName namn: MyAppResourceName typ: Microsoft. IoTCentral/IoTApps Location: taggning for tag: SKU: Microsoft. Azure. commands. IotCentral. Models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX-DisplayName: mitt eget visnings namn under domän: MyAppSubdomain Template: iotc-default@1.0.0 SubscriptionId: XXXXXXXX-XXXX-XXXX</span><span class="sxs-lookup"><span data-stu-id="e0071-115">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="e0071-116">Skapa ett IoT Central-program med standard prissättnings nivå S1 i regionen "västkusten", med ett anpassat visnings namn baserat på IOTC-standard-mallen.</span><span class="sxs-lookup"><span data-stu-id="e0071-116">Create an IoT Central application with the standard pricing tier S1 in the 'westus' region, with a custom display name, based on the iotc-default template.</span></span>

## <span data-ttu-id="e0071-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e0071-117">PARAMETERS</span></span>

### <span data-ttu-id="e0071-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e0071-118">-AsJob</span></span>
<span data-ttu-id="e0071-119">Kör cmdlet som ett jobb i bakgrunden.</span><span class="sxs-lookup"><span data-stu-id="e0071-119">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="e0071-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0071-120">-DefaultProfile</span></span>
<span data-ttu-id="e0071-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e0071-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0071-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e0071-122">-DisplayName</span></span>
<span data-ttu-id="e0071-123">Anpassat visnings namn för IoT Central-programmet.</span><span class="sxs-lookup"><span data-stu-id="e0071-123">Custom display name for the IoT Central application.</span></span>
<span data-ttu-id="e0071-124">Standard är resurs namn.</span><span class="sxs-lookup"><span data-stu-id="e0071-124">Default is resource name.</span></span>

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

### <span data-ttu-id="e0071-125">-Plats</span><span class="sxs-lookup"><span data-stu-id="e0071-125">-Location</span></span>
<span data-ttu-id="e0071-126">Platsen för IoT-huvudprogrammet.</span><span class="sxs-lookup"><span data-stu-id="e0071-126">Location of your IoT Central application.</span></span>
<span data-ttu-id="e0071-127">Standard platsen för mål resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="e0071-127">Default is the location of target resource group.</span></span>

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

### <span data-ttu-id="e0071-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="e0071-128">-Name</span></span>
<span data-ttu-id="e0071-129">Namnet på IoT Central program resursen.</span><span class="sxs-lookup"><span data-stu-id="e0071-129">Name of the Iot Central Application Resource.</span></span>

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

### <span data-ttu-id="e0071-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0071-130">-ResourceGroupName</span></span>
<span data-ttu-id="e0071-131">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="e0071-131">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="e0071-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="e0071-132">-Sku</span></span>
<span data-ttu-id="e0071-133">Pris nivå för IoT Central program.</span><span class="sxs-lookup"><span data-stu-id="e0071-133">Pricing tier for IoT Central applications.</span></span>
<span data-ttu-id="e0071-134">Standardvärdet är S1.</span><span class="sxs-lookup"><span data-stu-id="e0071-134">Default value is S1.</span></span>

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

### <span data-ttu-id="e0071-135">-Subdomain</span><span class="sxs-lookup"><span data-stu-id="e0071-135">-Subdomain</span></span>
<span data-ttu-id="e0071-136">Under domän för IoT Central URL.</span><span class="sxs-lookup"><span data-stu-id="e0071-136">Subdomain for the IoT Central URL.</span></span>
<span data-ttu-id="e0071-137">Varje program måste ha en unik under domän.</span><span class="sxs-lookup"><span data-stu-id="e0071-137">Each application must have a unique subdomain.</span></span>

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

### <span data-ttu-id="e0071-138">-Tagg</span><span class="sxs-lookup"><span data-stu-id="e0071-138">-Tag</span></span>
<span data-ttu-id="e0071-139">IoT Central program, Resource-taggar.</span><span class="sxs-lookup"><span data-stu-id="e0071-139">Iot Central Application Resource Tags.</span></span>

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

### <span data-ttu-id="e0071-140">-Mall</span><span class="sxs-lookup"><span data-stu-id="e0071-140">-Template</span></span>
<span data-ttu-id="e0071-141">IoT Central program mal len namn.</span><span class="sxs-lookup"><span data-stu-id="e0071-141">IoT Central application template name.</span></span>
<span data-ttu-id="e0071-142">Standard är ett anpassat program.</span><span class="sxs-lookup"><span data-stu-id="e0071-142">Default is a custom application.</span></span>

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

### <span data-ttu-id="e0071-143">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e0071-143">-Confirm</span></span>
<span data-ttu-id="e0071-144">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e0071-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0071-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0071-145">-WhatIf</span></span>
<span data-ttu-id="e0071-146">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e0071-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0071-147">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e0071-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0071-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0071-148">CommonParameters</span></span>
<span data-ttu-id="e0071-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0071-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0071-150">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0071-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0071-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e0071-151">INPUTS</span></span>

### <span data-ttu-id="e0071-152">System. String</span><span class="sxs-lookup"><span data-stu-id="e0071-152">System.String</span></span>

### <span data-ttu-id="e0071-153">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="e0071-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e0071-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e0071-154">OUTPUTS</span></span>

### <span data-ttu-id="e0071-155">Microsoft. Azure. commands. IotCentral. Models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="e0071-155">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="e0071-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e0071-156">NOTES</span></span>

## <span data-ttu-id="e0071-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e0071-157">RELATED LINKS</span></span>
