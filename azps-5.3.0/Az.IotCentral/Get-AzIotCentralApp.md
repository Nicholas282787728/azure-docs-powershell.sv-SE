---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/get-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Get-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Get-AzIotCentralApp.md
ms.openlocfilehash: cbc7e255f74943ea2aff3518d278035f72394235
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98526050"
---
# <span data-ttu-id="34bf3-101">Get-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="34bf3-101">Get-AzIotCentralApp</span></span>

## <span data-ttu-id="34bf3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="34bf3-102">SYNOPSIS</span></span>
<span data-ttu-id="34bf3-103">Hämtar egenskaper för antingen en eller flera IoT Central program.</span><span class="sxs-lookup"><span data-stu-id="34bf3-103">Gets properties for either one or several IoT Central Applications.</span></span>

## <span data-ttu-id="34bf3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="34bf3-104">SYNTAX</span></span>

### <span data-ttu-id="34bf3-105">ListIotCentralAppsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="34bf3-105">ListIotCentralAppsParameterSet (Default)</span></span>
```
Get-AzIotCentralApp [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="34bf3-106">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="34bf3-106">InteractiveIotCentralParameterSet</span></span>
```
Get-AzIotCentralApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="34bf3-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="34bf3-107">ResourceIdParameterSet</span></span>
```
Get-AzIotCentralApp -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34bf3-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="34bf3-108">DESCRIPTION</span></span>
<span data-ttu-id="34bf3-109">Hämtar metadata för antingen ett specifikt IoT Central program, eller alla program i en resurs grupp eller ett abonnemang, beroende på parameter uppsättning.</span><span class="sxs-lookup"><span data-stu-id="34bf3-109">Gets the metadata for either a specific IoT Central Application, or all the applications in a Resource Group or Subscription, depending on Parameter Set.</span></span> 

## <span data-ttu-id="34bf3-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="34bf3-110">EXAMPLES</span></span>

### <span data-ttu-id="34bf3-111">Exempel 1 skaffa specifika IoT Central program.</span><span class="sxs-lookup"><span data-stu-id="34bf3-111">Example 1 Get Specific IoT Central Application.</span></span>
```powershell
PS C:\> Get-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName"
```

<span data-ttu-id="34bf3-112">Hämtar metadata för det angivna IoT Central programmet.</span><span class="sxs-lookup"><span data-stu-id="34bf3-112">Gets the metadata for the specified IoT Central Application.</span></span>

<span data-ttu-id="34bf3-113">Exempel på utdata:</span><span class="sxs-lookup"><span data-stu-id="34bf3-113">Example Output:</span></span>

<span data-ttu-id="34bf3-114">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName namn: MyAppResourceName typ: Microsoft. IoTCentral/IoTApps plats: taggen för västkusten: {[Key, val]} SKU: Microsoft. Azure. commands. IotCentral. Models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXXXXXXXXXX:: för att visa namnet under domän: MyAppSubdomain Template: XXXXXXXX-XXXX- iotc-default@1.0.0 xxxx-ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34bf3-114">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="34bf3-115">Exempel 2 få IoT Central program i abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="34bf3-115">Example 2 Get IoT Central Applications in Subscription.</span></span>
```powershell
PS C:\> Get-AzIotCentralApp
```

<span data-ttu-id="34bf3-116">Hämtar metadata för alla IoT Central program i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="34bf3-116">Gets the metadata for all the IoT Central Applications in the current Subscription.</span></span>

<span data-ttu-id="34bf3-117">Exempel på utdata:</span><span class="sxs-lookup"><span data-stu-id="34bf3-117">Example Output:</span></span>

<span data-ttu-id="34bf3-118">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName namn: MyAppResourceName typ: Microsoft. IoTCentral/IoTApps plats: taggen för västkusten: {[Key, val]} SKU: Microsoft. Azure. commands. IotCentral. Models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXXXXXXXXXX:: för att visa namnet under domän: MyAppSubdomain Template: XXXXXXXX-XXXX- iotc-default@1.0.0 xxxx-ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34bf3-118">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="34bf3-119">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName2/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName2 namn: MyAppResourceName2 typ: Microsoft. IoTCentral/IoTApps Location: taggen väst: {[Key, val]} SKU: Microsoft. Azure. kommandon. IotCentral. Models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: mitt eget visnings namn 2 under domän: MyAppSubdomain2-mallen: iotc-default@1.0.0 SubscriptionId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName: MyResourceGroupName2</span><span class="sxs-lookup"><span data-stu-id="34bf3-119">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName2/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName2 Name              : MyAppResourceName2 Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name 2 Subdomain         : MyAppSubdomain2 Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName2</span></span>

### <span data-ttu-id="34bf3-120">Exempel 3 skaffa IoT Central program i resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="34bf3-120">Example 3 Get IoT Central Applications in Resource Group.</span></span>
```powershell
PS C:\> Get-AzIotCentralApp -ResourceGroupName "MyResourceGroupName"
```

<span data-ttu-id="34bf3-121">Hämtar metadata för alla IoT Central program i resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="34bf3-121">Gets the metadata for all IoT Central Applications in the provided Resource Group.</span></span>

<span data-ttu-id="34bf3-122">Exempel på utdata:</span><span class="sxs-lookup"><span data-stu-id="34bf3-122">Example Output:</span></span>

<span data-ttu-id="34bf3-123">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName namn: MyAppResourceName typ: Microsoft. IoTCentral/IoTApps plats: taggen för västkusten: {[Key, val]} SKU: Microsoft. Azure. commands. IotCentral. Models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXXXXXXXXXX:: för att visa namnet under domän: MyAppSubdomain Template: XXXXXXXX-XXXX- iotc-default@1.0.0 xxxx-ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34bf3-123">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="34bf3-124">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName2 namn: MyAppResourceName2 typ: Microsoft. IoTCentral/IoTApps Location: taggen väst: {[Key, val]} SKU: Microsoft. Azure. kommandon. IotCentral. Models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: mitt eget visnings namn 2 under domän: MyAppSubdomain2-mallen: iotc-default@1.0.0 SubscriptionId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34bf3-124">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName2 Name              : MyAppResourceName2 Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name 2 Subdomain         : MyAppSubdomain2 Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

## <span data-ttu-id="34bf3-125">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="34bf3-125">PARAMETERS</span></span>

### <span data-ttu-id="34bf3-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34bf3-126">-DefaultProfile</span></span>
<span data-ttu-id="34bf3-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="34bf3-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34bf3-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="34bf3-128">-Name</span></span>
<span data-ttu-id="34bf3-129">Namnet på IoT Central program resursen.</span><span class="sxs-lookup"><span data-stu-id="34bf3-129">Name of the Iot Central Application Resource.</span></span>

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

### <span data-ttu-id="34bf3-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34bf3-130">-ResourceGroupName</span></span>
<span data-ttu-id="34bf3-131">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="34bf3-131">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: ListIotCentralAppsParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### <span data-ttu-id="34bf3-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="34bf3-132">-ResourceId</span></span>
<span data-ttu-id="34bf3-133">IoT Central program resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="34bf3-133">Iot Central Application Resource Id.</span></span>

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

### <span data-ttu-id="34bf3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34bf3-134">CommonParameters</span></span>
<span data-ttu-id="34bf3-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34bf3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34bf3-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="34bf3-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34bf3-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="34bf3-137">INPUTS</span></span>

### <span data-ttu-id="34bf3-138">System. String</span><span class="sxs-lookup"><span data-stu-id="34bf3-138">System.String</span></span>

## <span data-ttu-id="34bf3-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="34bf3-139">OUTPUTS</span></span>

### <span data-ttu-id="34bf3-140">Microsoft. Azure. commands. IotCentral. Models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="34bf3-140">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="34bf3-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="34bf3-141">NOTES</span></span>

## <span data-ttu-id="34bf3-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="34bf3-142">RELATED LINKS</span></span>
