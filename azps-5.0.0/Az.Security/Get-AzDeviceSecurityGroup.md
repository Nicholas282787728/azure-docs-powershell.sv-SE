---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzDeviceSecurityGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDeviceSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDeviceSecurityGroup.md
ms.openlocfilehash: 3d43407c9f7e58d7a5d29ef56412f6d38c5c957b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322769"
---
# <span data-ttu-id="f6172-101">Get-AzDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f6172-101">Get-AzDeviceSecurityGroup</span></span>

## <span data-ttu-id="f6172-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f6172-102">SYNOPSIS</span></span>
<span data-ttu-id="f6172-103">Gruppen skaffa enhets säkerhet (IoT Hub Security)</span><span class="sxs-lookup"><span data-stu-id="f6172-103">Get device security group (IoT Hub security)</span></span>

## <span data-ttu-id="f6172-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f6172-104">SYNTAX</span></span>

### <span data-ttu-id="f6172-105">ResourceIdScope (standard)</span><span class="sxs-lookup"><span data-stu-id="f6172-105">ResourceIdScope (Default)</span></span>
```
Get-AzDeviceSecurityGroup -HubResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f6172-106">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="f6172-106">ResourceIdLevelResource</span></span>
```
Get-AzDeviceSecurityGroup -HubResourceId <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f6172-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f6172-107">DESCRIPTION</span></span>
<span data-ttu-id="f6172-108">Get-AzDeviceSecurityGroup cmdlet returnerar en enhets säkerhets grupp som definierats i IoT-säkerhetslösningen</span><span class="sxs-lookup"><span data-stu-id="f6172-108">The Get-AzDeviceSecurityGroup cmdlet returns a device security group defined in iot security solution</span></span>

## <span data-ttu-id="f6172-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f6172-109">EXAMPLES</span></span>

### <span data-ttu-id="f6172-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f6172-110">Example 1</span></span>
```powershell
PS C:\> Get-AzDeviceSecurityGroup -HubResourceId "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" -Name "MySecurityGroup" 

Id: "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub/providers/Microsoft.Security/deviceSecurityGroups/MySecurityGroup"
Name: "MySecurityGroup"
Type: "Microsoft.Security/deviceSecurityGroups"
ThresholdRules: []
TimeWindowRules: [
            {
              RuleType: "ActiveConnectionsNotInAllowedRange"
              DisplayName: "Number of active connections is not in allowed range"
              Description: "Get an alert when the number of active connections of a device in the time window is not in the allowed range"
              IsEnabled: false
              MinThreshold: 0
              MaxThreshold: 0
              TimeWindowSize: "PT15M"
            }
            {
              RuleType: "AmqpC2DMessagesNotInAllowedRange"
              DisplayName: "Number of cloud to device messages (AMQP protocol) is not in allowed range"
              Description: "Get an alert when the number of cloud to device messages (AMQP protocol) in the time window is not in the allowed range"
              IsEnabled: false
              MinThreshold: 0
              MaxThreshold: 0
              TimeWindowSize: "PT15M"
            }]
AllowlistRules: [
            {
              RuleType": "ConnectionToIpNotAllowed",
              DisplayName: "Outbound connection to an ip that isn't allowed"
              Description: "Get an alert when an outbound connection is created between your device and an ip that isn't allowed"
              IsEnabled: false
              ValueType: "IpCidr"
              AllowlistValues: []
            },
            {
              RuleType: "LocalUserNotAllowed"
              DisplayName: "Login by a local user that isn't allowed"
              Description: "Get an alert when a local user that isn't allowed logins to the device"
              IsEnabled: false
              ValueType: "String"
              AllowlistValues: []
            }]
DenylistRules: []
```

<span data-ttu-id="f6172-111">Hämta säkerhets gruppen "MySecurityGroup" i IoT Hub med reasource ID "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span><span class="sxs-lookup"><span data-stu-id="f6172-111">Get device security group "MySecurityGroup" in IoT Hub with reasource Id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span></span>

### <span data-ttu-id="f6172-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="f6172-112">Example 2</span></span>
```powershell
PS C:\> Get-AzDeviceSecurityGroup -HubResourceId "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" 

Array of security group items like the item returned in example 1
```

<span data-ttu-id="f6172-113">Lista med säkerhets grupp för enheter i IoT Hub med reasource ID "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span><span class="sxs-lookup"><span data-stu-id="f6172-113">Get list of device security group in IoT Hub with reasource Id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span></span>

## <span data-ttu-id="f6172-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f6172-114">PARAMETERS</span></span>

### <span data-ttu-id="f6172-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6172-115">-DefaultProfile</span></span>
<span data-ttu-id="f6172-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f6172-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6172-117">-HubResourceId</span><span class="sxs-lookup"><span data-stu-id="f6172-117">-HubResourceId</span></span>
<span data-ttu-id="f6172-118">ID för den säkerhets resurs som du vill starta kommandot på.</span><span class="sxs-lookup"><span data-stu-id="f6172-118">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="f6172-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="f6172-119">-Name</span></span>
<span data-ttu-id="f6172-120">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="f6172-120">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6172-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6172-121">CommonParameters</span></span>
<span data-ttu-id="f6172-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6172-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6172-123">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f6172-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6172-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f6172-124">INPUTS</span></span>

### <span data-ttu-id="f6172-125">Ingen</span><span class="sxs-lookup"><span data-stu-id="f6172-125">None</span></span>

## <span data-ttu-id="f6172-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f6172-126">OUTPUTS</span></span>

### <span data-ttu-id="f6172-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f6172-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span></span>

## <span data-ttu-id="f6172-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f6172-128">NOTES</span></span>

## <span data-ttu-id="f6172-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f6172-129">RELATED LINKS</span></span>
