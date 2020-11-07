---
external help file: Microsoft.Azure.Commands.IotCentral.dll-Help.xml
Module Name: AzureRM.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iotcentral/set-azurermiotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/Set-AzureRmIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/Set-AzureRmIotCentralApp.md
ms.openlocfilehash: a9b7dbc962809288979f5293c14fd875081f48bc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758184"
---
# <span data-ttu-id="4c285-101">Set-AzureRmIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="4c285-101">Set-AzureRmIotCentralApp</span></span>

## <span data-ttu-id="4c285-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4c285-102">SYNOPSIS</span></span>
<span data-ttu-id="4c285-103">Uppdaterar metadata för ett IoT Central program.</span><span class="sxs-lookup"><span data-stu-id="4c285-103">Updates the metadata for an IoT Central Application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c285-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4c285-104">SYNTAX</span></span>

### <span data-ttu-id="4c285-105">ResourceIdParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="4c285-105">ResourceIdParameterSet (Default)</span></span>
```
Set-AzureRmIotCentralApp [-DisplayName <String>] [-Tag <Hashtable>] -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c285-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c285-106">InputObjectParameterSet</span></span>
```
Set-AzureRmIotCentralApp [-DisplayName <String>] [-Tag <Hashtable>] -InputObject <PSIotCentralApp> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c285-107">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c285-107">InteractiveIotCentralParameterSet</span></span>
```
Set-AzureRmIotCentralApp [-DisplayName <String>] [-Tag <Hashtable>] [-AsJob] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c285-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4c285-108">DESCRIPTION</span></span>
<span data-ttu-id="4c285-109">Uppdatera metadata för ett IoT Central program.</span><span class="sxs-lookup"><span data-stu-id="4c285-109">Update the metadata for an IoT Central Application.</span></span> 

## <span data-ttu-id="4c285-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4c285-110">EXAMPLES</span></span>

### <span data-ttu-id="4c285-111">Exempel 1 uppdatera visnings namn</span><span class="sxs-lookup"><span data-stu-id="4c285-111">Example 1 Update Display Name</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -DisplayName "My New Custom Display Name"
```

<span data-ttu-id="4c285-112">Uppdatera visnings namnet på ett befintligt IoT Central program.</span><span class="sxs-lookup"><span data-stu-id="4c285-112">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="4c285-113">Exempel på utdata:</span><span class="sxs-lookup"><span data-stu-id="4c285-113">Example Output:</span></span>

<span data-ttu-id="4c285-114">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName namn: MyAppResourceName typ: Microsoft. IoTCentral/IoTApps Location: taggning for tag: SKU: Microsoft. Azure. commands. IotCentral. Models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: mitt nya namn under iotc-default@1.0.0 domän: MyAppSubdomain</span><span class="sxs-lookup"><span data-stu-id="4c285-114">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My New Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

## <span data-ttu-id="4c285-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4c285-115">PARAMETERS</span></span>

### <span data-ttu-id="4c285-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4c285-116">-AsJob</span></span>
<span data-ttu-id="4c285-117">Kör cmdlet som ett jobb i bakgrunden.</span><span class="sxs-lookup"><span data-stu-id="4c285-117">Run cmdlet as a job in the background.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c285-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c285-118">-DefaultProfile</span></span>
<span data-ttu-id="4c285-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4c285-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c285-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="4c285-120">-DisplayName</span></span>
<span data-ttu-id="4c285-121">Anpassat visnings namn för IoT Central-programmet.</span><span class="sxs-lookup"><span data-stu-id="4c285-121">Custom Display Name of the Iot Central Application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c285-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4c285-122">-InputObject</span></span>
<span data-ttu-id="4c285-123">IoT Central Application input-objekt.</span><span class="sxs-lookup"><span data-stu-id="4c285-123">Iot Central Application Input Object.</span></span>

```yaml
Type: PSIotCentralApp
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4c285-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="4c285-124">-Name</span></span>
<span data-ttu-id="4c285-125">Namnet på IoT Central program resursen.</span><span class="sxs-lookup"><span data-stu-id="4c285-125">Name of the Iot Central Application Resource.</span></span>

```yaml
Type: String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c285-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c285-126">-ResourceGroupName</span></span>
<span data-ttu-id="4c285-127">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="4c285-127">Name of the Resource Group.</span></span>

```yaml
Type: String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c285-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4c285-128">-ResourceId</span></span>
<span data-ttu-id="4c285-129">IoT Central program resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="4c285-129">Iot Central Application Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c285-130">-Tagg</span><span class="sxs-lookup"><span data-stu-id="4c285-130">-Tag</span></span>
<span data-ttu-id="4c285-131">IoT Central program, Resource-taggar.</span><span class="sxs-lookup"><span data-stu-id="4c285-131">Iot Central Application Resource Tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c285-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4c285-132">-Confirm</span></span>
<span data-ttu-id="4c285-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4c285-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c285-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c285-134">-WhatIf</span></span>
<span data-ttu-id="4c285-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4c285-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c285-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4c285-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c285-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c285-137">CommonParameters</span></span>
<span data-ttu-id="4c285-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c285-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c285-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c285-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c285-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4c285-140">INPUTS</span></span>

### <span data-ttu-id="4c285-141">System. String</span><span class="sxs-lookup"><span data-stu-id="4c285-141">System.String</span></span>
### <span data-ttu-id="4c285-142">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="4c285-142">System.Collections.Hashtable</span></span>
### <span data-ttu-id="4c285-143">Microsoft. Azure. commands. IotCentral. Models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="4c285-143">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>
## <span data-ttu-id="4c285-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4c285-144">OUTPUTS</span></span>

### <span data-ttu-id="4c285-145">Microsoft. Azure. commands. IotCentral. Models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="4c285-145">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>
## <span data-ttu-id="4c285-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4c285-146">NOTES</span></span>

## <span data-ttu-id="4c285-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4c285-147">RELATED LINKS</span></span>
