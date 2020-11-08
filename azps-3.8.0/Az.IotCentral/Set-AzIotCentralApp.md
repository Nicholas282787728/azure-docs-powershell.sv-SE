---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/set-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Set-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Set-AzIotCentralApp.md
ms.openlocfilehash: cea582481515f519e14df9f430dc1326e72a0877
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088213"
---
# <span data-ttu-id="91f44-101">Set-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="91f44-101">Set-AzIotCentralApp</span></span>

## <span data-ttu-id="91f44-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="91f44-102">SYNOPSIS</span></span>
<span data-ttu-id="91f44-103">Uppdaterar metadata för ett IoT Central program.</span><span class="sxs-lookup"><span data-stu-id="91f44-103">Updates the metadata for an IoT Central Application.</span></span>

## <span data-ttu-id="91f44-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="91f44-104">SYNTAX</span></span>

### <span data-ttu-id="91f44-105">ResourceIdParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="91f44-105">ResourceIdParameterSet (Default)</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91f44-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="91f44-106">InputObjectParameterSet</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>]
 -InputObject <PSIotCentralApp> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="91f44-107">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="91f44-107">InteractiveIotCentralParameterSet</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-AsJob]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="91f44-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="91f44-108">DESCRIPTION</span></span>
<span data-ttu-id="91f44-109">Uppdatera metadata för ett IoT Central program.</span><span class="sxs-lookup"><span data-stu-id="91f44-109">Update the metadata for an IoT Central Application.</span></span> 

## <span data-ttu-id="91f44-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="91f44-110">EXAMPLES</span></span>

### <span data-ttu-id="91f44-111">Exempel 1 uppdatera visnings namn</span><span class="sxs-lookup"><span data-stu-id="91f44-111">Example 1 Update Display Name</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -DisplayName "My New Custom Display Name"
```

<span data-ttu-id="91f44-112">Uppdatera visnings namnet på ett befintligt IoT Central program.</span><span class="sxs-lookup"><span data-stu-id="91f44-112">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="91f44-113">Exempel på utdata:</span><span class="sxs-lookup"><span data-stu-id="91f44-113">Example Output:</span></span>

<span data-ttu-id="91f44-114">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName namn: MyAppResourceName typ: Microsoft. IoTCentral/IoTApps Location: taggning for tag: SKU: Microsoft. Azure. commands. IotCentral. Models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: mitt nya namn under iotc-default@1.0.0 domän: MyAppSubdomain</span><span class="sxs-lookup"><span data-stu-id="91f44-114">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My New Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="91f44-115">Exempel 2 uppdatera under domän</span><span class="sxs-lookup"><span data-stu-id="91f44-115">Example 2 Update Subdomain</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "new-subdomain"
```

<span data-ttu-id="91f44-116">Uppdatera visnings namnet på ett befintligt IoT Central program.</span><span class="sxs-lookup"><span data-stu-id="91f44-116">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="91f44-117">Exempel på utdata:</span><span class="sxs-lookup"><span data-stu-id="91f44-117">Example Output:</span></span>

<span data-ttu-id="91f44-118">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName namn: MyAppResourceName typ: Microsoft. IoTCentral/IoTApps Location: taggning tag: SKU: Microsoft. Azure. commands. IotCentral. Models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: visnings namn under domän: mallen ny under domän: iotc-default@1.0.0 SubscriptionId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91f44-118">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : Display Name Subdomain         : new-subdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

## <span data-ttu-id="91f44-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="91f44-119">PARAMETERS</span></span>

### <span data-ttu-id="91f44-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="91f44-120">-AsJob</span></span>
<span data-ttu-id="91f44-121">Kör cmdlet som ett jobb i bakgrunden.</span><span class="sxs-lookup"><span data-stu-id="91f44-121">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="91f44-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91f44-122">-DefaultProfile</span></span>
<span data-ttu-id="91f44-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="91f44-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91f44-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="91f44-124">-DisplayName</span></span>
<span data-ttu-id="91f44-125">Anpassat visnings namn för IoT Central-programmet.</span><span class="sxs-lookup"><span data-stu-id="91f44-125">Custom Display Name of the Iot Central Application.</span></span>

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

### <span data-ttu-id="91f44-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="91f44-126">-InputObject</span></span>
<span data-ttu-id="91f44-127">IoT Central Application input-objekt.</span><span class="sxs-lookup"><span data-stu-id="91f44-127">Iot Central Application Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="91f44-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="91f44-128">-Name</span></span>
<span data-ttu-id="91f44-129">Namnet på IoT Central program resursen.</span><span class="sxs-lookup"><span data-stu-id="91f44-129">Name of the Iot Central Application Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91f44-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91f44-130">-ResourceGroupName</span></span>
<span data-ttu-id="91f44-131">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="91f44-131">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91f44-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="91f44-132">-ResourceId</span></span>
<span data-ttu-id="91f44-133">IoT Central program resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="91f44-133">Iot Central Application Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91f44-134">-Subdomain</span><span class="sxs-lookup"><span data-stu-id="91f44-134">-Subdomain</span></span>
<span data-ttu-id="91f44-135">Under domän till IoT Central-programmet.</span><span class="sxs-lookup"><span data-stu-id="91f44-135">Subdomain of the IoT Central Application.</span></span>

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

### <span data-ttu-id="91f44-136">-Tagg</span><span class="sxs-lookup"><span data-stu-id="91f44-136">-Tag</span></span>
<span data-ttu-id="91f44-137">IoT Central program, Resource-taggar.</span><span class="sxs-lookup"><span data-stu-id="91f44-137">Iot Central Application Resource Tags.</span></span>

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

### <span data-ttu-id="91f44-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="91f44-138">-Confirm</span></span>
<span data-ttu-id="91f44-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="91f44-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91f44-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91f44-140">-WhatIf</span></span>
<span data-ttu-id="91f44-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="91f44-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91f44-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="91f44-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91f44-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91f44-143">CommonParameters</span></span>
<span data-ttu-id="91f44-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91f44-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91f44-145">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91f44-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91f44-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="91f44-146">INPUTS</span></span>

### <span data-ttu-id="91f44-147">System. String</span><span class="sxs-lookup"><span data-stu-id="91f44-147">System.String</span></span>

### <span data-ttu-id="91f44-148">Microsoft. Azure. commands. IotCentral. Models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="91f44-148">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="91f44-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="91f44-149">OUTPUTS</span></span>

### <span data-ttu-id="91f44-150">Microsoft. Azure. commands. IotCentral. Models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="91f44-150">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="91f44-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="91f44-151">NOTES</span></span>

## <span data-ttu-id="91f44-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="91f44-152">RELATED LINKS</span></span>
