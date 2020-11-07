---
external help file: Microsoft.Azure.Commands.IotCentral.dll-Help.xml
Module Name: AzureRM.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iotcentral/get-azurermiotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/Get-AzureRmIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/Get-AzureRmIotCentralApp.md
ms.openlocfilehash: fdf674b5ec2dfcefe8fcada92cfaf0fd1073f7f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758185"
---
# <span data-ttu-id="ec561-101">Get-AzureRmIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="ec561-101">Get-AzureRmIotCentralApp</span></span>

## <span data-ttu-id="ec561-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ec561-102">SYNOPSIS</span></span>
<span data-ttu-id="ec561-103">Hämtar egenskaper för antingen en eller flera IoT Central program.</span><span class="sxs-lookup"><span data-stu-id="ec561-103">Gets properties for either one or several IoT Central Applications.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec561-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ec561-104">SYNTAX</span></span>

### <span data-ttu-id="ec561-105">ListIotCentralAppsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="ec561-105">ListIotCentralAppsParameterSet (Default)</span></span>
```
Get-AzureRmIotCentralApp [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ec561-106">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec561-106">InteractiveIotCentralParameterSet</span></span>
```
Get-AzureRmIotCentralApp [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec561-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec561-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmIotCentralApp -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec561-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ec561-108">DESCRIPTION</span></span>
<span data-ttu-id="ec561-109">Hämtar metadata för antingen ett specifikt IoT Central program, eller alla program i en resurs grupp eller ett abonnemang, beroende på parameter uppsättning.</span><span class="sxs-lookup"><span data-stu-id="ec561-109">Gets the metadata for either a specific IoT Central Application, or all the applications in a Resource Group or Subscription, depending on Parameter Set.</span></span> 

## <span data-ttu-id="ec561-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ec561-110">EXAMPLES</span></span>

### <span data-ttu-id="ec561-111">Exempel 1 skaffa specifika IoT Central program.</span><span class="sxs-lookup"><span data-stu-id="ec561-111">Example 1 Get Specific IoT Central Application.</span></span>
```powershell
PS C:\> Get-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName"
```

<span data-ttu-id="ec561-112">Hämtar metadata för det angivna IoT Central programmet.</span><span class="sxs-lookup"><span data-stu-id="ec561-112">Gets the metadata for the specified IoT Central Application.</span></span>

<span data-ttu-id="ec561-113">Exempel på utdata:</span><span class="sxs-lookup"><span data-stu-id="ec561-113">Example Output:</span></span>

<span data-ttu-id="ec561-114">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName namn: MyAppResourceName typ: Microsoft. IoTCentral/IoTApps plats: taggen för västkusten: {[Key, val]} SKU: Microsoft. Azure. commands. IotCentral. Models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXXXXXXXXXX:: för att visa namnet under domän: MyAppSubdomain Template: XXXXXXXX-XXXX- iotc-default@1.0.0 xxxx-ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec561-114">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="ec561-115">Exempel 2 få IoT Central program i abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="ec561-115">Example 2 Get IoT Central Applications in Subscription.</span></span>
```powershell
PS C:\> Get-AzureRmIotCentralApp
```

<span data-ttu-id="ec561-116">Hämtar metadata för alla IoT Central program i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="ec561-116">Gets the metadata for all the IoT Central Applications in the current Subscription.</span></span>

<span data-ttu-id="ec561-117">Exempel på utdata:</span><span class="sxs-lookup"><span data-stu-id="ec561-117">Example Output:</span></span>

<span data-ttu-id="ec561-118">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName namn: MyAppResourceName typ: Microsoft. IoTCentral/IoTApps plats: taggen för västkusten: {[Key, val]} SKU: Microsoft. Azure. commands. IotCentral. Models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXXXXXXXXXX:: för att visa namnet under domän: MyAppSubdomain Template: XXXXXXXX-XXXX- iotc-default@1.0.0 xxxx-ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec561-118">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="ec561-119">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName2/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName2 namn: MyAppResourceName2 typ: Microsoft. IoTCentral/IoTApps Location: taggen väst: {[Key, val]} SKU: Microsoft. Azure. kommandon. IotCentral. Models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: mitt eget visnings namn 2 under domän: MyAppSubdomain2-mallen: iotc-default@1.0.0 SubscriptionId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName: MyResourceGroupName2</span><span class="sxs-lookup"><span data-stu-id="ec561-119">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName2/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName2 Name              : MyAppResourceName2 Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name 2 Subdomain         : MyAppSubdomain2 Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName2</span></span>

### <span data-ttu-id="ec561-120">Exempel 3 skaffa IoT Central program i resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ec561-120">Example 3 Get IoT Central Applications in Resource Group.</span></span>
```powershell
PS C:\> Get-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName"
```

<span data-ttu-id="ec561-121">Hämtar metadata för alla IoT Central program i resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ec561-121">Gets the metadata for all IoT Central Applications in the provided Resource Group.</span></span>

<span data-ttu-id="ec561-122">Exempel på utdata:</span><span class="sxs-lookup"><span data-stu-id="ec561-122">Example Output:</span></span>

<span data-ttu-id="ec561-123">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName namn: MyAppResourceName typ: Microsoft. IoTCentral/IoTApps plats: taggen för västkusten: {[Key, val]} SKU: Microsoft. Azure. commands. IotCentral. Models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXXXXXXXXXX:: för att visa namnet under domän: MyAppSubdomain Template: XXXXXXXX-XXXX- iotc-default@1.0.0 xxxx-ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec561-123">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="ec561-124">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName2 namn: MyAppResourceName2 typ: Microsoft. IoTCentral/IoTApps Location: taggen väst: {[Key, val]} SKU: Microsoft. Azure. kommandon. IotCentral. Models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: mitt eget visnings namn 2 under domän: MyAppSubdomain2-mallen: iotc-default@1.0.0 SubscriptionId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec561-124">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName2 Name              : MyAppResourceName2 Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name 2 Subdomain         : MyAppSubdomain2 Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

## <span data-ttu-id="ec561-125">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ec561-125">PARAMETERS</span></span>

### <span data-ttu-id="ec561-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec561-126">-DefaultProfile</span></span>
<span data-ttu-id="ec561-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ec561-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec561-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="ec561-128">-Name</span></span>
<span data-ttu-id="ec561-129">Namnet på IoT Central program resursen.</span><span class="sxs-lookup"><span data-stu-id="ec561-129">Name of the Iot Central Application Resource.</span></span>

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

### <span data-ttu-id="ec561-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec561-130">-ResourceGroupName</span></span>
<span data-ttu-id="ec561-131">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ec561-131">Name of the Resource Group.</span></span>

```yaml
Type: String
Parameter Sets: ListIotCentralAppsParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### <span data-ttu-id="ec561-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ec561-132">-ResourceId</span></span>
<span data-ttu-id="ec561-133">IoT Central program resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="ec561-133">Iot Central Application Resource Id.</span></span>

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

### <span data-ttu-id="ec561-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec561-134">CommonParameters</span></span>
<span data-ttu-id="ec561-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec561-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec561-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec561-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec561-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ec561-137">INPUTS</span></span>

### <span data-ttu-id="ec561-138">System. String</span><span class="sxs-lookup"><span data-stu-id="ec561-138">System.String</span></span>
## <span data-ttu-id="ec561-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ec561-139">OUTPUTS</span></span>

### <span data-ttu-id="ec561-140">Microsoft. Azure. commands. IotCentral. Models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="ec561-140">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>
## <span data-ttu-id="ec561-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ec561-141">NOTES</span></span>

## <span data-ttu-id="ec561-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ec561-142">RELATED LINKS</span></span>
