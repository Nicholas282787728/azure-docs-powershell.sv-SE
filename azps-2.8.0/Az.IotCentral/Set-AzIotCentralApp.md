---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/set-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Set-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Set-AzIotCentralApp.md
ms.openlocfilehash: 78fdf68ecb8c50d0eebf4611b51a2fad14c66e5d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744033"
---
# <span data-ttu-id="ca683-101">Set-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="ca683-101">Set-AzIotCentralApp</span></span>

## <span data-ttu-id="ca683-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ca683-102">SYNOPSIS</span></span>
<span data-ttu-id="ca683-103">Uppdaterar metadata för ett IoT Central program.</span><span class="sxs-lookup"><span data-stu-id="ca683-103">Updates the metadata for an IoT Central Application.</span></span>

## <span data-ttu-id="ca683-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ca683-104">SYNTAX</span></span>

### <span data-ttu-id="ca683-105">ResourceIdParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="ca683-105">ResourceIdParameterSet (Default)</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca683-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca683-106">InputObjectParameterSet</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>]
 -InputObject <PSIotCentralApp> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ca683-107">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca683-107">InteractiveIotCentralParameterSet</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-AsJob]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ca683-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ca683-108">DESCRIPTION</span></span>
<span data-ttu-id="ca683-109">Uppdatera metadata för ett IoT Central program.</span><span class="sxs-lookup"><span data-stu-id="ca683-109">Update the metadata for an IoT Central Application.</span></span> 

## <span data-ttu-id="ca683-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ca683-110">EXAMPLES</span></span>

### <span data-ttu-id="ca683-111">Exempel 1 uppdatera visnings namn</span><span class="sxs-lookup"><span data-stu-id="ca683-111">Example 1 Update Display Name</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -DisplayName "My New Custom Display Name"
```

<span data-ttu-id="ca683-112">Uppdatera visnings namnet på ett befintligt IoT Central program.</span><span class="sxs-lookup"><span data-stu-id="ca683-112">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="ca683-113">Exempel på utdata:</span><span class="sxs-lookup"><span data-stu-id="ca683-113">Example Output:</span></span>

<span data-ttu-id="ca683-114">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName namn: MyAppResourceName typ: Microsoft. IoTCentral/IoTApps Location: taggning for tag: SKU: Microsoft. Azure. commands. IotCentral. Models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: mitt nya namn under iotc-default@1.0.0 domän: MyAppSubdomain</span><span class="sxs-lookup"><span data-stu-id="ca683-114">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My New Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="ca683-115">Exempel 2 uppdatera under domän</span><span class="sxs-lookup"><span data-stu-id="ca683-115">Example 2 Update Subdomain</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "new-subdomain"
```

<span data-ttu-id="ca683-116">Uppdatera visnings namnet på ett befintligt IoT Central program.</span><span class="sxs-lookup"><span data-stu-id="ca683-116">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="ca683-117">Exempel på utdata:</span><span class="sxs-lookup"><span data-stu-id="ca683-117">Example Output:</span></span>

<span data-ttu-id="ca683-118">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName namn: MyAppResourceName typ: Microsoft. IoTCentral/IoTApps Location: taggning tag: SKU: Microsoft. Azure. commands. IotCentral. Models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: visnings namn under domän: mallen ny under domän: iotc-default@1.0.0 SubscriptionId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca683-118">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : Display Name Subdomain         : new-subdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

## <span data-ttu-id="ca683-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ca683-119">PARAMETERS</span></span>

### <span data-ttu-id="ca683-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ca683-120">-AsJob</span></span>
<span data-ttu-id="ca683-121">Kör cmdlet som ett jobb i bakgrunden.</span><span class="sxs-lookup"><span data-stu-id="ca683-121">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="ca683-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca683-122">-DefaultProfile</span></span>
<span data-ttu-id="ca683-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ca683-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca683-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ca683-124">-DisplayName</span></span>
<span data-ttu-id="ca683-125">Anpassat visnings namn för IoT Central-programmet.</span><span class="sxs-lookup"><span data-stu-id="ca683-125">Custom Display Name of the Iot Central Application.</span></span>

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

### <span data-ttu-id="ca683-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ca683-126">-InputObject</span></span>
<span data-ttu-id="ca683-127">IoT Central Application input-objekt.</span><span class="sxs-lookup"><span data-stu-id="ca683-127">Iot Central Application Input Object.</span></span>

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

### <span data-ttu-id="ca683-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="ca683-128">-Name</span></span>
<span data-ttu-id="ca683-129">Namnet på IoT Central program resursen.</span><span class="sxs-lookup"><span data-stu-id="ca683-129">Name of the Iot Central Application Resource.</span></span>

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

### <span data-ttu-id="ca683-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca683-130">-ResourceGroupName</span></span>
<span data-ttu-id="ca683-131">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ca683-131">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="ca683-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ca683-132">-ResourceId</span></span>
<span data-ttu-id="ca683-133">IoT Central program resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="ca683-133">Iot Central Application Resource Id.</span></span>

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

### <span data-ttu-id="ca683-134">-Subdomain</span><span class="sxs-lookup"><span data-stu-id="ca683-134">-Subdomain</span></span>
<span data-ttu-id="ca683-135">Under domän till IoT Central-programmet.</span><span class="sxs-lookup"><span data-stu-id="ca683-135">Subdomain of the IoT Central Application.</span></span>

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

### <span data-ttu-id="ca683-136">-Tagg</span><span class="sxs-lookup"><span data-stu-id="ca683-136">-Tag</span></span>
<span data-ttu-id="ca683-137">IoT Central program, Resource-taggar.</span><span class="sxs-lookup"><span data-stu-id="ca683-137">Iot Central Application Resource Tags.</span></span>

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

### <span data-ttu-id="ca683-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ca683-138">-Confirm</span></span>
<span data-ttu-id="ca683-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ca683-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca683-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca683-140">-WhatIf</span></span>
<span data-ttu-id="ca683-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ca683-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca683-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ca683-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca683-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca683-143">CommonParameters</span></span>
<span data-ttu-id="ca683-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca683-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca683-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca683-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca683-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ca683-146">INPUTS</span></span>

### <span data-ttu-id="ca683-147">System. String</span><span class="sxs-lookup"><span data-stu-id="ca683-147">System.String</span></span>

### <span data-ttu-id="ca683-148">Microsoft. Azure. commands. IotCentral. Models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="ca683-148">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="ca683-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ca683-149">OUTPUTS</span></span>

### <span data-ttu-id="ca683-150">Microsoft. Azure. commands. IotCentral. Models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="ca683-150">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="ca683-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ca683-151">NOTES</span></span>

## <span data-ttu-id="ca683-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ca683-152">RELATED LINKS</span></span>
